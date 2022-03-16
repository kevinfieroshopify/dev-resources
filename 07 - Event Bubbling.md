* [Event Bubbling](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Building_blocks/Events)
    * Events occur in response to actions in the code. This can be user triggered such as clicking a button or resizing the window. This can also be programmatic such as when an error occurs or a video finishes being played.
    * A simple example is a button being clicked by the user. This fires a click handler event which performs an action such as changing the background color.
    * Event listeners can be added or removed. 
    * There can be more than one event on an element such as two functions being present on a single button.
    * Event objects (sometimes used as `e`) passes additional information to the even handler. Many of these event objects are standardized based on the action taken. An example includes `click` or `keydown` events.
    * Using `e.preventDefault()` overrides the normal behavior of forms and html elements.
        * [Documentation](https://developer.mozilla.org/en-US/docs/Web/API/Event/preventDefault) 
        * [Video Example](https://www.youtube.com/watch?v=3SNyh57XSIA&ab_channel=dcode)
    * Bubbling vs. Capturing
        * Defines the order events are fired when there are parents/children with event handlers.
        * [Video Example](https://www.youtube.com/watch?v=Q6HAJ6bz7bY&ab_channel=dcode)
        * Bubbling - start with child then up to parent.
        * Capturing - start with parent and work down to child (`true` in third argument of `addEventListener`).
        * `e.stopPropagation()` prevents continuation of the bubbling or capturing chain.
