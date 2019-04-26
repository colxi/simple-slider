# Slideshow builder
Simple-slider.js generates customizable slideshows from HTML structures. Is responsive, allows slides footers, and navigation. All its parts are easily customizable using CSS.

# Usage
You need to set first the HTML template : A container with the img elements used by the slider.

```html
    <div id="mySlider">
        <img src="https://placekitten.com/208/287"/>
        <img src="https://placekitten.com/408/287"/>
        <img src="https://placekitten.com/408/287"/>
        <img src="https://placekitten.com/408/287"/>
        <img src="https://placekitten.com/408/287"/>
    </div>    
```
Just , import the library and call the `Slider` method, providing a reference to the container, and the slider spinning speed in ms :
```javascript
    import {Slider} from './simple-slider.js';
    let container = document.getElementById('mySlider');
    Slider(container, 3000); 
```

Some attributes can be set in the container, in order to activate certain features :
- `[slider-nav]` : Displays navigation buttons
- `[slider-footer]` : Displays a footer in each slide. The footer text can be set in each image using the attribute `[slide-title]`.

# CSS customization

The following CSS selectors configure the whole interface :

- `.simple-slider`: General slider container

- `.simple-slider-contents` : Internal spinning container

- `.simple-slider-slide` : Each individual slide container

- `.simple-slider-slide-footer` : Slide footer container

- `.simple-slider[slider-footer]:hover .simple-slider-slide-footer` : Appearance of the footer on mouse over
   
- `.simple-slider-navigation` : Styles for both navigation buttons

- `.simple-slider[slider-nav]:hover .simple-slider-navigation` : Appearance of the navigation buttons on slider mouse over

- `.simple-slider-navigation-prev ` : Navigation previous button

- `.simple-slider-navigation-next` : Navigation next button

# Notes

- The original container is preserved, with its id attributes and classes, but its contents are removed and replaced with the necessary parts to behave as expected.

- The engine will inject in the header a `styles` element , containing the default styling, most of those CSS properties can be overwritten to customize the look and feel.

- The responsivity will be applied only when the slider spins.