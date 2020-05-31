<p align="center">
    <a href="https://splidejs.com" target="_blank">
        <img width="120px" src="images/splide-logo.png">
    </a>
    <a href="https://reactjs.org/" target="_blank">
        <img width="120px" src="images/react-logo.png">
    </a>
</p>

# React Splide
**React Splide is the [Splide](https://github.com/Splidejs/splide) component for React.**
* [Document](https://splidejs.com/integration-react-splide/)
* [Splide](https://github.com/Splidejs/splide)

## Installation
Get the latest version by NPM:
```bash
$ npm install @splidejs/react-splide
```

## Usage
### Components
Import `Splide` and `SplideSlide` components:
```javascript
import { Splide, SplideSlide } from '@splidejs/react-splide';
```
And render them like this:
```javascript
<Splide>
  <SplideSlide>
    <img src="image1.jpg" alt="Image 1"/>
  </SplideSlide>
  <SplideSlide>
    <img src="image2.jpg" alt="Image 2"/>
  </SplideSlide>
</Splide>
```

### CSS
Import [styles](https://splidejs.com/themes/) if you need.
```javascript
import '@splidejs/splide/dist/css/themes/splide-default.min.css';
// or
import '@splidejs/splide/dist/css/themes/splide-sea-green.min.css';
// or
import '@splidejs/splide/dist/css/themes/splide-skyblue.min.css';
```

## Options
The `Splide` component accepts [options](https://splidejs.com/options/) as an object:
```javascript
<Splide
  options={ {
    rewind : true,
    width  : 800,
    gap    : '1rem',
  } }
>
</Splide>
```

## Listening to Events
You can listen to all [Splide events](https://splidejs.com/events/) through the `Splide` component. The callback function name is generated by the original event name, adding an "on" prefix, converted to the camelcase and removed semicolon. For example, "arrow:mounted" will be "onArrowMounted".
```javascript
<Splide onArrowMounted={ ( splide, prev, next ) => { console.log( prev, next ) } }>
```
Note that the first argument is the splide instance, meaning original arguments are shifted by one.

## Examples
Here is a small example:
```javascript
import React from 'react';
import { Splide, SplideSlide } from '@splidejs/react-splide';

export default () => {
  return (
    <Splide
      options={ {
        rewind : true,
        width  : 800,
        gap    : '1rem',
      } }
    >
      <SplideSlide>
        <img src="image1.jpg" alt="Image 1"/>
      </SplideSlide>
      <SplideSlide>
        <img src="image2.jpg" alt="Image 2"/>
      </SplideSlide>
      <SplideSlide>
        <img src="image3.jpg" alt="Image 3"/>
      </SplideSlide>
    </Splide>
  );
}
```
More examples:
* [Basic example](https://github.com/Splidejs/react-splide/blob/master/src/js/examples/BasicExample.jsx)
* [Autoplay](https://github.com/Splidejs/react-splide/blob/master/src/js/examples/AutoplayExample.jsx)
* [Thumbnails](https://github.com/Splidejs/react-splide/blob/master/src/js/examples/ThumbnailsExample.jsx)
* [Dynamic slides](https://github.com/Splidejs/react-splide/blob/master/src/js/examples/DynamicSlidesExample.jsx)

## License
React Splide and Splide are released under the MIT license.  
© 2020 Naotoshi Fujita