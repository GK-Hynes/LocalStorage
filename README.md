# [LocalStorage and Event Delegation](https://gk-hynes.github.io/localstorage/)

A page built to practice working with localStorage and event delegation. Built for Wes Bos' JavaScript 30 course.

[![Screentshot of localStorage tapas site](https://res.cloudinary.com/gerhynes/image/upload/v1516213829/Screenshot-2018-1-17_LocalStorage_jnj6in.jpg)](https://gk-hynes.github.io/localstorage/)

## Notes

Select the form and the ul and create an array to store the data.

Listen for the submit event on the form and run a function, `addItem`. Use `e.preventDefault()` to prevent the page from reloading.

Make a variable, `item`, with `text` and a `done` state of `false` (so by default it is not checked).

Use `(this.querySelector("[name=item]")).value` to get the `text`.

Use `this.reset()` to clear the input form.

Push `item` into the `items` array.

Make a second function, `populateList()`. Pass in the items, with the default set to an empty array (So things don't crash if you submit without typing anything).

You also need a place to put the HTML so pass in the list of items as a destination.

Map over the plates array and use `platesList.innerHTML` to put it into the HTML.

Return a list item with a label and call `.join("")` on it (`map()` returns an array and you want a string).

Include `populateList` in `addItem` and pass it `items` and `itemsList`.

One downside to this is that it rerenders the entire list every time you update an item. Angular or React could get around this by only changing the minimum amount of HTML necessary.
