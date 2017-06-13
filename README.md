# Flexbox

### Two most important features
- Flex containers
- Flex items

#### Flex Container
- Sets the context for flexbox layout
- Contains flex items, the actual elements you layout using flexbox
- Can be any block-element or inline element

#### Flex Item

- Every direct child of a dlex conainer
- There can be any number of flex items inside a flex container

Flexbox follows two axis that determine the layour direction of flex items

---


### Flexbox Axes

#### Main axis
- Main axis is the primary axis, along with flex items are laid out
- It determines the direction of flex items in flex container

#### Cross axis
- Runs perpendicular to the main axis

- Each axis has a start side and an end side
- The default Main Start and Main end direction of the Main axis is left to right
- The default direction of Cross axis is top to bottom.

- But you can easily change the directions
- For instance you can change the horizontal column layout

---


### Distributing Space Inside a Flex Container (`justify-content`)

#### Justify Content

The justify-content property lets you control the position and alignment of flex Items on the main axis and how space should be distributed in a flex container.

- You apply the `justify-content` property to flex containers only.
- The justify-content property lets you control the position and alignment of flex Items on the main axis and how space should be distributed in a flex container.
- The default value for justify-content is flex-start, which places items towards the start of each flex line.
- To place items at the end of the flex line, set justify-content to flex-end.
- The value center places flex items in the center of the line, with equal amounts of empty space between the line's start edge and the first item.
- The value space-between displays equal spacing between flex items.
- For equal spacing around every flex item, use the value space-around.
- A margin set to auto will absorb any extra space around a flex item and push other flex items into different positions.

```
.container
    display: flex
    flex-wrap: wrap
    justify-content: space-between

.item-1
    margin-right: auto

## Item 1 will absorb any extra space around a flex item and push other flex items into different positions
```

---


### Changing the Order of Flex Items (`order`)

By default, flex items are laid out in the order they appear in the source code. We can use the `order` property to change the order of any flex item.

- The `order` property applies to flex items only.
- We can use the `order` property to change the order of any flex item.
- You can structure an HTML document for SEO or accessibility first, then rearrange the content without ever editing the HTML.
- The default `order` of all flex items is **0**
- `order` places flex items relative to the other items' order values.
- To place a flex item before another item, it needs to have a lower order value than the item.
- To place a flex item after another item, it needs to have a higher order value than the item.

---

### Growing Flex Items (`flex-glow`)
With flexbox you can make flex items grow or shrink in relation to other flex items and the available space inside the flex container.

- The `flex-grow` property applies to flex items only.
- `flex-grow` determines how much of the available space inside the flex container an item should take up; it assigns more or less space to flex items.
- A `flex-grow` value of 1 expands flex items to take up the full space of a line.
- The higher the `flex-grow` value, the more an item grows relative to the other items.
- A `flex-grow` affects flex-item only and does nothing to flex-container

Links:
[flex-grow MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/flex-grow?v=example),
[A Complete Guide to Flexbox](https://css-tricks.com/snippets/css/a-guide-to-flexbox/),
[`flex-grow` is weird. Or is it?](https://css-tricks.com/flex-grow-is-weird/)

---

### Smarter Layouts with flex-basis and flex

- `flex` and `flex-basis` apply to flex items only.
- `flex-basis` specifies the initial main size of a flex item.
- You set the initial size you want the flex items to be, then flexbox evenly distributes the free space according that size.
- `flex` is the shorthand for `flex-grow`, `flex-basis` and `flex-shrink.`
- Using only one number value for `flex` sets the flex-grow value of an item.
- The second and third values are **optional** in the `flex` shorthand.
- Setting only one number value for `flex` automatically sets the `flex-basis` value to 0.

Links:
[`flex` MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/flex?v=example),
[`flex-basis` MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/flex-basis?v=example),
[`flex-shrink` MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/flex-shrink?v=example)

---


### Aligning Flex Items on the Cross Axis

Learn how to align flex items on the cross axis with the align-items and align-self properties.

- The `align-items` property applies to flex containers only.
- The `align-self` property applies to flex items only.
- `align-items` aligns flex items vertically in the flex container.
- To align all flex items to the start of the cross axis, use the `align-items: flex-start`.
- `align-items`: flex-end; packs the items toward the end of the cross axis.
- `align-items`: center; perfectly centers items along the cross axis.
- `align-self`: `flex-start`; aligns a flex item to the **start** of the cross axis.
- `align-self`: `flex-end`; aligns a flex item to the **end** of the cross axis.
- `align-self`: `center`; aligns a flex item to the **center** of the cross axis.

Links:
[`align-items` MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/align-items?v=example)
[`align-self` MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/align-self)

---

### Vertical and Horizontal Centering

Centering content is one of the trickiest and more difficult things to do in CSS layout when using properties like float, display or position. In this video, you'll learn why flexbox is the smartest solution when it comes to centering content.

**Three ways to center-align elements using flexbox**

Set the flex container's `justify-content` and `align-items` values to `center`:

```
.container
  justify-content: center
  align-items: center
```

Set the flex container's `justify-content` value to `center`, while setting the flex item's `align-self` value to `center`:
```
.container
  justify-content: center

.item
  align-self: center

```
Set the flex item's `margin` value to auto:

```
.item
  margin: auto;

```
Links:
[**Flexbugs** - A community-curated list of flexbox issues and cross-browser workarounds for them](https://github.com/philipwalton/flexbugs)
