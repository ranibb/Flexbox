# Flexbox

## Flex Container Properties

*display* : Defines a flex container and is mandatory to work with flex box.

*flex-direction* : Defines the direction in which the flex items are placed in the container.

*flex-wrap* : Control the wrapping of items within a container.

*flex-flow* : A shorthand for the combination of *flex-direction* and *flex-wrap*.

*justified-content* :  Defines the alignment of the items along the main axis.

*align-items* : Defines how flex items are laid out along the cross axis.

*align-content* : Similar to justify-content with the difference being this will align along the Cross access. align-content works only when there are multiple rows of flex items in the container.

### display

The `display` property is used to create either a block level or in line level flex container.

The possible values are:
* `flex`
* `inline-flex`

### flex-direction

The `flex-direction` property sets the direction of the main access thereby controlling how the items are placed in the container.

The possible values are:
* `row`, Sets the main axes from left to right.
* `row-reversed`, Sets the main axes from right to left,
* `column`, Sets the cross axes from top to bottom and
* `column-reverse`, Sets the cross axes from bottom to top.

### flex-wrap

The `flex-wrap` property is used to control the wrapping of flex items within the container.

The possible values are:
* `no-wrap`, default.
* `wrap`, wraps the content into the next row or next column.
* `wrap-reverse`, wraps the content into the previous row or previous column.

### flex-flow

The `flex-flow` property combines the values from both `flex-direction` and `flex-wrap`. The first value is a a value of flex-direction and the second value is a value of flex-wrap.

    flex-flow: <flex-direction> <flex-wrap>

The possible values are:
* `row no-wrap`
* `row wrap`
* `row wrap-reverse`

* `row-reversed no-wrap`
* `row-reversed wrap`
* `row-reversed wrap-reverse`

* `column no-wrap`
* `column wrap`
* `column wrap-reverse`

* `column-reverse no-wrap`
* `column-reverse wrap`
* `column-reverse wrap-reverse`

### justified-content

The `justified-content` property is used to align items and distribute any extra spacing in the parent container. The alignment is always along the main axis.

The possible values are:
* `flex-start`
* `flex-and` 
* `center` 
* `space-between` 
* `space-around` 
* `space-evenly`

### align-items

The `align-items` property is used to align items along the cross axis of the container.

The possible values are:
* `flex-start`
* `flex-and` 
* `center` 
* `baseline` 
* `stretch`

### align-content

The `align-content` property is used to align lines of content along the cross axis and distribute any extra spacing in the parent container.

The possible values are:
* `flex-start`
* `flex-and` 
* `center` 
* `space-between` 
* `space-around` 
* `stretch`

## Flex item Properties

*order* : Controls the order in which the item appears in the flex container.

*flex-grow* : Defines the ability for a flex item to grow if necessary.

*flex-shrink* : Defines the ability for a flex item to shrink if necessary.

*flex-basis* : Specifies the initial main size of a flex item.

*flex* : A shorthand for *flex-grow*, *flex-shrink* and *flex-basis*.

*align-self* :  Allows alignment of individual flex items.

### order

The `order` property accepts an integer value and is used to control the order of items in the flex container. Elements with the same order value are laid out in the order in which they appear in the source code.

### flex-grow

The `flex-grow` property dictates what amount of the available space inside the flex container the items should take up. The flex-grow factor is also relative to the other items in the container.

By default, the value is 0 which dictates the items should not grow. Setting a flex-grow value of 1 on all the fixed items will cost the flex items to grow evenly when there is additional space in the container.

### flex-shrink

The `flex-shrink` property dictates the shrink factor of the flex items when the default size of the flex items is larger than the flex container. And it is always relative to other items in the container.

By default, the value is one which dictates the items should shrink evenly to a certain extent if necessary.

### flex-basis

The `flex-basis` property is used to set the initial size of a flex item. You can specify values in pixels, percentages or relative units. 

By default, the value is auto which decides the items width based on the items content.

### flex

The `flex` property can set `flex-grow`, `flex-shrink` and `flex-basis` at once.

    flex: <flex-grow> <flex-shrink> <flex-basis>

For example, this:
```CSS
.item {
    flex-grow: 2;
    flex-shrink: 5;
    flex-basis: 200px
}
```
can be shorthanded by this:
```CSS
.item {
    flex: 2 5 200px;
}
```

By default, `flex` property has a value of `0 1 auto`.

*The `flex` property can be specified using either one, two or three values:*

* One Value:

unitless number -> interpreted as flex-grow
width/height -> interpreted as flex-basis
none -> flex-grow
initial -> flex-shrink
auto -> flex-basis

* Two values:

unitless number | unitless number -> interpreted as flex-grow | flex-shrink
unitless number | width/height -> interpreted as flex-grow | flex-basis

* Three values:

unitless number | unitless number | width/height -> interpreted as flex-grow | flex-shrink | flex-basis

### align-self

The `align-self` property is used to align the items individually.

The possible values are:
* `auto`
* `flex-start`
* `flex-end`
* `center`
* `stretch`

The `align-self` property will overwrite the `align-items` value of the Flex container.