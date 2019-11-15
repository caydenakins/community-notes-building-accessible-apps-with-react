# Heading Levels

## General

Similar to how landmark regions provide structure or layout to the page, heading levels show up on the rotor and give users the mapping page they can navigate with.

**Rules:**

- Each page has to have an h1, because each page has to
- Pages should be structured in a hierarchical manner
  - `<h1>`: being the most important (usually page titles or main content heading)
  - `<h2>`: usually major section headings
  - `<h3>`: sub-sections of the `<h2>`
- Don't skip heading LevelsDon't use text formatting (font size, bold, etc)
- Don't use headers simply for visual results  

## Exercise 1

### `/src/login/Login.js/` Before
```js
  <div className="card bg-primary">
      <header>
          <h5 className="card-header">
              Movie Wishlist Login
          </h5>
      </header>
        ...
```

### `/src/login/Login.js/` After
```js
  <header>
      <h1>Movie Wishlist</h1>
  </header>
  <main>
      <div className="card bg-primary">
          <h2 className="card-header">
               Login
          </h2>
            ...
```

Always think in efficiency when you are creating. Simply changing wording, adding a `Login` header and separating the `Movie Wishlist` from the section cleaned up a lot.

## Exercise 2

### `/src/primitives/Header.js/` Before
```js
<span className="navbar-text">
    {title}
</span>
```

### `/src/primitives/Header.js/` After
```js
<span className="navbar-text">
    <h1>{title}</h1>
</span>
```

Small changes can provide big impacts, here we simply added an `<h1>` and it assisted with the construction and view of the page.
