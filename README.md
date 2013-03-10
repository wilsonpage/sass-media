sass-media
==========

Media query shorthand sugar to make complex media queries a little more legible.

## API

### @include media(breakpoint [[,] breakpoint ...]);

Prints a media query. Spaces resolve to `and` and commas resolve to `,`.

## USAGE

```css
$small: 'min-width: 0px';
$medium: 'min-width: 480px';
$large: 'min-width: 1024px';
$portrait: 'orientation: portrait';
$short: 'max-height: 500px';

@include media($medium) { ... }
// => @media (min-width: 480px) { ... }

@include media($medium, $large) { ... }
// => @media (min-width: 480px), (min-width: 1024px) { ... }

@include media($large $portrait) { ... }
// => @media (min-width: 1024px) and (orientation: portrait) { ... }
```