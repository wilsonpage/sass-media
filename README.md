sass-media
==========

Media query shorthand sugar to make complex media queries a little more legible.

## API

### @include media(breakpoint [[,] breakpoint ...]);

Prints a media query. Spaces resolve to `and` and commas resolve to `,`.

## USAGE

```scss
$medium: 'min-width: 480px';
$large: 'min-width: 1024px';
$portrait: 'orientation: portrait';

@include media($medium) { ... }
// => @media (min-width: 480px) { ... }

@include media($medium, $large) { ... }
// => @media (min-width: 480px), (min-width: 1024px) { ... }

@include media($large $portrait) { ... }
// => @media (min-width: 1024px) and (orientation: portrait) { ... }
```