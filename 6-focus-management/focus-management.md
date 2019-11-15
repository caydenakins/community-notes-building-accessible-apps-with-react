# Focus Management

## General

Keyboard/screen reader navigation relies on focus proceeding in a logical order. We don't want the user to not know where they are or how to get back to the desired point in a web page.

The way we do this is by using `refs`. They are elements that can be passed with the variable or a callback to set the variable. We can call the `focus()` function on the ref variable.

If you have anything in your `useEffect()`, any dependencies you've identified that might cause it to not fire, then you may end up not calling `focus()` when you wanted to. So, if you run into any behavior where `focus()` isn't being called or the ref is not set, be clear if you had any dependencies that would cause a re-render when you didn't need it to.

If you were using a stateless functional component, not a class-based component, be open to using the `useRef()` hook. It is similar to calling `createRef()`. It will create a ref object, which you pass to the ref attribute and instead of having a `componentDidMount()` (which you won't have in a functional stateless component), you could use a `useEffect()` hook.

If your focus is staying on a button that was present on the previous page, it may be because you did not set the focus anywhere. If you don't set the focus somewhere, it will default to the body and the cursor will stay where it's at.
- It's worth noting you also should use your best judgement to find out where to place the user's cursor/focus once they arrive to a new page. You want to decide the experience you want to convey to the user, which is usually the first statement/instructions.

You can't focus an element that isn't focusable, so you have to give it a tabIndex of a positive number.
- `tabIndex={0}` -> `tabIndex={1}`

We can pass in booleans like `doFocus` for controlling whether or not we want an element to focus.
- `doFocus={hasMovies}` would focus if we had movies,

## User Questions

Mike Polowick: *Any reason not to use -1 for the tabIndex on the \<h1>?*
- -1 is a way of saying something is not focusable, it needs to be a positive number for it to be focusable. There's not really a reason to add numbers greater than 0.
  - _Learner's Advocate Note_ - Despite the program still functioning when you use a `tabIndex` greater than 0, it is considered an **anti-pattern**. It shifts the affected element to the end of the tab order.
