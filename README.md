# SCSS Masterclass

(S)CSS Layout Masterclass: Flexbox & Grid

## Flexbox:

- [x] flex-direction
- [x] order
- [x] justify-content
- [x] align-items
- [x] align-self
- [x] flex-wrap
- [x] align-content
- [x] flex-grow
- [x] flex-shrink
- [x] flex-basis

## Grid:

- [x] grid-template-columns
- [x] grid-template-rows
- [x] column-gap
- [x] row-gap
- [x] gap
- [x] grid-template-areas
- [x] grid-column-start
- [x] grid-column-end
- [x] grid-row-start
- [x] grid-row-end
- [x] grid-column
- [x] grid-row
- [x] grid-template
- [x] justify-items
- [x] align-items
- [x] place-items
- [x] justify-content
- [x] align-content
- [x] place-content
- [x] justify-self
- [x] align-self
- [x] place-self
- [x] grid-auto-rows
- [x] grid-auto-flow
- [x] grid-auto-columns

### Keywords & Functions:

- [x] repeat
- [x] fr
- [x] minmax
- [x] auto-fit
- [x] auto-fill
- [x] min-content
- [x] max-content

## SCSS:

- [O] Variables
  most important value like color, size
  ```
  \_filename.scss skip the compile
  ```
- [O] Nesting
  more precise targeting
  ```
  &:hover
  & => father
  ```
- [O] Mixins

  ```
    @mixin link($word) {
          text-decoration: none;
          display: block;
          @if $word == "odd" {
            color: blue;
          } @else {
            color: red;
          }
    }
  ```

- [O] Extend
  reuse other code (without argument)
  ```
  // \_buttons.scss
  %button {
    border-radius: 7px;
    font-family: inherit;
    font-size: 12px;
  }
  // styles.scss
  @import "\_buttons"
  a {
   @extend %button
  }
  ```
- [O] Responsive Mixins
  to adjust media query
  ```
  // \_mixins.scss
  @mixin responsive($device) {
    @if $device == 'iphone' {
      @media screen and (min-width: 500px) and (max-width: 600px) {
      @content;
    } else {
      @media screen and (max-width: ~)
      @content;
    }
  }
  //styles.scss
  a {
    @include responsive
  }
  ```
  Awesome SCSS
  Bourbon - really cool
  Sass Media query

## To Clone:

- [O][https://besthorrorscenes.com/](https://besthorrorscenes.com/)
- [O][https://paint-box.com/](https://paint-box.com/)
- [O][http://10x19.co/](http://10x19.co/)
- [O][http://www.z-o-o.fr/](http://www.z-o-o.fr/)
- [O][https://schwartzmedia.com.au/](https://schwartzmedia.com.au/)
- [O][https://tolv.dk/](https://tolv.dk/)
- [O][https://rodicdavidson.co.uk/](https://rodicdavidson.co.uk/)
- [O][https://beige.de/](https://beige.de/)
- [O][http://donicaida.com/](http://donicaida.com/)
- [O][https://canalstreet.market/](https://canalstreet.market/)
- [>][https://wonhundred.com/](https://wonhundred.com/)

## To figure out

1. box-sizing: border-box

## paint-box

- cursor: pointer;

```
body > *:not(.footer) {
padding: 0px 140px;
}
// select direct children of body except footer
```

- no need absolute, just use background-image with url

```
background-image: linear-gradient(rgba(0, 0, 0, 0.4), rgba(0, 0, 0, 0.4)),
url("https://images.unsplash.com/photo-1583248369069-9d91f1640fe6?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1352&q=80");
```

## 10x19

- center image is hard to adjust the size

## Zoo

- Using selector like :not() :first-of-type

## Schwartz

- grid-order
  ```
  div:nth-of-type(4n + 3) {
    grid-column: 2 / 3;
  }
  grid-auto-flow: dense;
  ```
- grid-default-size
  `grid-auto-rows: 363px;`
- get random photo with size
  `https://source.unsplash.com/random/500x360`
- align center without flexbox
  `margin: 0 auto;`

## tolv

- how to change the mouse pointer with element not image
- background blurr without affecting text

## rodicdavidson

- diffrent gap
  column-gap
  row-gap

## beige

- need to study: hover + before, after, content add
- make circle shape with empty li
  it needs to be display: block to show background-color

## donicaida

- use padding not height for the underline in table

## canalstreet

- moving border with background

## wonhundred

- simply aligning text at center without flex?
