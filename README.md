# BareNecessities
The simple bare necessities to Forget about your worries and your strife!
Contains no content, except for sass mixins and default file structure.

## Getting Started

### Installing
You will need to run npm install sass and you're good to go.
To watch changes you can either use a sass compiler (https://prepros.io/) or in the terminal enter sass --watch sass/style.scss:css/style.css

For bigger projects, it is recommended to do file structure of 7-1 (https://itnext.io/structuring-your-sass-projects-c8d41fa55ed4)

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
