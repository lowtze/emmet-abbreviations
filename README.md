# emmet-abbreviations

A collection of helpful [Emmet](https://docs.emmet.io/abbreviations/) abbreviations.

Emmet says TO NOT do what I'm doing, but here we are.

- [Holy Grail](#holy-grail)
- [Lorem Ipsum](#lorem-ipsum)


## Holy Grail

Skeleton for a [Holy Grail](https://en.wikipedia.org/wiki/Holy_grail_(web_design)) web layout:

```
header+(div.content>div.sidebar+div.container)+footer
```

```html
<header></header>
<div class="content">
  <div class="sidebar"></div>
  <div class="container"></div>
</div>
<footer></footer>
```

Or include a nav and some cards:

```
header+(div.content>div.sidebar>(nav>li*4>a)^div.container>div.card*6)+footer
```

```html
<header></header>
<div class="content">
  <div class="sidebar">
    <nav>
      <li><a href=""></a></li>
      <li><a href=""></a></li>
      <li><a href=""></a></li>
      <li><a href=""></a></li>
    </nav>
    <div class="container">
      <div class="card"></div>
      <div class="card"></div>
      <div class="card"></div>
      <div class="card"></div>
      <div class="card"></div>
      <div class="card"></div>
    </div>
  </div>
</div>
<footer></footer>
```

And the CSS to go with it:

```css
    body {
      display: flex;
      flex-direction: column;
      min-height: 100vh;
      padding: 10px;
    }

    header {
      display: flex;
      align-items: center;
      justify-content: space-between;
    }

    .content {
      display: flex;
      flex-wrap: wrap;
      flex: 1;
    }

    .sidebar {
      flex-basis;
    }

    .container {
      flex-basis: 80%;
      display: flex;
      justify-content: space-around;
      flex-wrap: wrap;
    }

    .card {
      display: flex;
      flex-direction: column;
      width: 250px;
    }
```

## Lorem Ipsum

Now you probably need some dummy text. We can use `lorem` plus an optional number to specify the number of words (e.g. `lorem100` for 100 words of lorem ipsum; otherwise the default is 30). Let's start with a classic five-paragraph essay.

```
p*5>lorem
```

```html
<p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Ratione rem facilis eum in adipisci nesciunt harum veniam amet? Quo ad exercitationem iure veniam voluptates explicabo voluptatum eum mollitia numquam nostrum.</p>
<p>Ratione ea dolore exercitationem a! Nihil a iste ad repellat dolorum. Pariatur omnis sunt tempore eius quas perferendis illo voluptatem, aperiam optio! Non veniam corrupti impedit voluptate magni quas iste!</p>
<p>Possimus qui id dolore praesentium accusantium error, ab magnam iusto explicabo sunt iure ducimus assumenda sit necessitatibus eveniet ut eius? Optio quos a excepturi est iusto. Autem error incidunt enim.</p>
<p>Consectetur ullam debitis dignissimos odio enim aperiam eius, deserunt libero voluptates quis eos veritatis dicta! Sint accusamus dolores culpa, corporis voluptates et temporibus distinctio dolorem officia incidunt officiis delectus nesciunt?</p>
<p>Eveniet et a omnis! Autem quibusdam incidunt ipsa enim cumque sapiente sint eos quidem minus deleniti delectus inventore, vitae labore cum, ea veritatis eveniet, impedit eaque ducimus et obcaecati illum!</p>
```