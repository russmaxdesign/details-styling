# details-styling

Demo version: https://russmaxdesign.github.io/details-styling/

A quick demo showing how to style the `<details>` element icons.

**Note**: Rather than directly style the details and summary elements, I have chosen to style BEM-based class names instead. I prefer not to style native elements unless the chosen style is going to be used for every instance of that element.

## The HTML

```html
<details class="details">
  <summary class="details__summary">This is summary example 1</summary>
  <p class="details__content">Lorem ipsum dolor...</p>
</details>
```

## The SCSS

```scss
// details

.details {
  position: relative;
  margin: 0 0 .3em;
}

.details__summary {
  padding: .3em .3em .4em 28px;
  cursor: pointer;
  background: #eee;
}

.details__summary:hover,
.details__summary:focus {
  background: #ddd;
}

.details__summary:active {
  background: #ccc;
}

.details__summary::-webkit-details-marker {
  display: none;
}

.details__summary:before {
  position: absolute;
  top: 4px;
  left: 5px;
  display: block;
  width: 20px;
  height: 20px;
  content: '';
  background: url(../img/details-closed.png);
}

.details[open] .details__summary:before {
  background: url(../img/details-open.png);
}

.details__content {
  margin: .6em 0 1.5em;
}
```

See [Licence information](LICENCE) for use.
