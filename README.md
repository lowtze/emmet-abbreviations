# emmet-abbreviations

A collection of helpful [Emmet](https://docs.emmet.io/abbreviations/) abbreviations.

Emmet says TO NOT do what I'm doing, but here we are.

## Contents

- [CSS Test Page](#css-test-page)
- [Holy Grail](#holy-grail)
- [Lorem Ipsum](#lorem-ipsum)


## CSS Test Page

Set up a page with some common elements to test out CSS styling. It ain't pretty but it works.

First: 

```
!
```

Then:

```
h1{h1 header}+h2{h2 header}+p>lorem^h3{h3 header}+p>lorem^h4{h4 header}+h5{h5 header}+h6{h6 header}+ul>lorem10*5^ol>lorem10*5^p*3>lorem^a{test link}+p>b{this is bold}^p>i{this is italic}^p>strong{and now strong}^p>em{this is emphasized}^pre{preformatted text in a row}+block{A blockquote of my famous words by me of all people.}+table>tr>th{headers}*3^(tr>td{table rows}*3)*3
```

Which makes this beast:

```html
<h1>h1 header</h1>
<h2>h2 header</h2>
<p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Deleniti soluta error dicta id ab quae dolor officia ex, harum, aliquam nulla sapiente perspiciatis culpa doloremque eius suscipit omnis autem. Quaerat.</p>
<h3>h3 header</h3>
<p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Vel quod qui odit sunt similique at doloribus quae esse perspiciatis voluptatum, sint repellat explicabo nemo exercitationem, corporis maxime sed dicta quos.</p>
<h4>h4 header</h4>
<h5>h5 header</h5>
<h6>h6 header</h6>
<ul>
  <li>Lorem ipsum dolor sit amet consectetur adipisicing elit. Perferendis, incidunt!</li>
  <li>Iure laudantium veritatis provident, vero officiis inventore porro in minus?</li>
  <li>Voluptates alias impedit dolorem eligendi minima voluptatum dicta id accusantium.</li>
  <li>Quam, corrupti aspernatur porro maxime ipsum obcaecati nostrum vitae fugiat.</li>
  <li>Ut, minus. Qui alias dicta officiis explicabo commodi officia facilis.</li>
</ul>
<ol>
  <li>Lorem ipsum dolor sit amet consectetur adipisicing elit. Ex, cumque!</li>
  <li>Alias quidem dolores incidunt tempora ea, nam dignissimos quae totam!</li>
  <li>Nisi unde praesentium, molestias maxime atque accusantium nobis delectus illum!</li>
  <li>Sint iste possimus architecto quidem maxime in omnis, veritatis nesciunt.</li>
  <li>Delectus voluptates quam saepe vitae officiis, deleniti repudiandae! Animi, delectus?</li>
</ol>
<p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Hic, ratione aliquid expedita labore accusamus, officiis laudantium adipisci minima possimus eligendi asperiores ut maiores mollitia molestias provident, dolore voluptates quasi repellat.</p>
<p>Inventore sint quam sit aliquam, atque accusantium voluptas itaque, deserunt nulla quae reprehenderit a voluptate, totam dolorum harum fugiat explicabo! Magnam molestias voluptates eligendi numquam! Ullam adipisci architecto natus maxime.</p>
<p>Dicta velit expedita distinctio, praesentium autem iste impedit iure perferendis unde omnis voluptas tempora eveniet quibusdam delectus, molestias, eos eius officia quo voluptatibus ducimus ipsam ipsum quis. Doloribus, eveniet omnis.</p>
<a href="">test link</a>
<p><b>this is bold</b></p>
<p><i>this is italic</i></p>
<p><strong>and now strong</strong></p>
<p><em>this is emphasized</em></p>
<pre>preformatted text in a row</pre>
<block>A blockquote of my famous words by me of all people.</block>
<table>
  <tr>
    <th>headers</th>
    <th>headers</th>
    <th>headers</th>
  </tr>
  <tr>
    <td>table rows</td>
    <td>table rows</td>
    <td>table rows</td>
  </tr>
  <tr>
    <td>table rows</td>
    <td>table rows</td>
    <td>table rows</td>
  </tr>
  <tr>
    <td>table rows</td>
    <td>table rows</td>
    <td>table rows</td>
  </tr>
</table>
```
[(back to top)](#contents)

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
[(back to top)](#contents)

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

[(back to top)](#contents)