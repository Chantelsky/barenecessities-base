# BareNecessities
The simple bare necessities to Forget about your worries and your strife!
Contains no content, except for sass mixins and default file structure.

## Getting Started

### Installing
You will need to run npm install sass and you're good to go.
To watch changes you can either use a sass compiler (https://prepros.io/) or in the terminal enter sass --watch sass/style.scss:css/style.css

## Code Example
```
/*
usage: @include mediaQ(insert maxwidth,minwidth); or @include mediaQ(insert maxwidth);
*/

@mixin mediaQ($arg...) {
    @if length($arg) == 1 {
        @media screen and (max-width: nth($arg, 1)) {
            @content;
        }
    }

    @if length($arg) == 2 {
        @media screen and (max-width: nth($arg,1)) and (min-width: nth($arg,2)) {
            @content;
        }
    }
}
```

MIT © [Chantel Laver]()
