# 12 column grid

Responsive, simple, intuitive CSS grid system built with flexbox.

This grid doesn't include even a line of unnecessary code, so if you add it to your site it will stand only for grid!

## Installation

Just take this piece of [CSS](https://raw.githubusercontent.com/Rostyk27/grid/master/grid.css) and have fun building your awesome websites.

## Demo

You can visit the [demo](https://grid.rostyk.dev/) page to see how simple and flexible this grid is.

Demo reflects each step of usage described below.

## Usage

#### 1. The easiest way to use it - just add the class `.flex_grid` to the parent element.

```html
<div class="flex_grid">
    <div>col 1</div> <!--width: 25%-->
    <div>col 2</div> <!--width: 25%-->
    <div>col 3</div> <!--width: 25%-->
    <div>col 4</div> <!--width: 25%-->
</div>
```

Without specifying classes to child `div` elements they will stand equally.  
Because by default child of `.flex_grid` has style `flex: 1;`

---

#### 2. You also have an option to specify grid in a mobile-first way.
* use only for desktop `.flex_grid__rwd`
* use for desktop & tablet `.flex_grid__mob`

---

#### 3. Basic customization of column width. 

Based on the 12-column system.

Classes: `._col_1`, `._col_2`, `._col_3`, `._col_4`, `._col_5`, `._col_6`, `._col_7`, `._col_8`, `._col_9`, `._col_10`, `._col_11`, `._col_12`

```html
<div class="flex_grid">
    <div class="_col_4">col 1</div> <!--width: 33.3%-->
    <div class="_col_5">col 2</div> <!--width: 41.7%-->
    <div class="_col_3">col 3</div> <!--width: 25%-->
</div>
```

---

#### 4. Easily configure the gap between columns.

Just assign new value to `--grid-gap` property of current `.flex_grid` container. Default gap is `20px`.

```css
.new_gap {
  --grid-gap: 10px;
} 
```

---

#### 5. Use the flexibility of `flex: 1;`

There is an option to add a class only to one child element and let another fill the rest of the space.

It could be useful for default `article` & `aside` combination.

```html
<div class="flex_grid">
    <article>article</article> <!--flex: 1-->
    <aside class="_col_3">aside</aside> <!--width: 25%-->
</div>
```

---

#### 6. Change the column width for a tablet.

**Note that this width will stay for mobile if you won't specify for mobile separately.*

Just apply additional child classes like `.__50_rwd` to specify the new width.

Classes:  
`.__rwd = flex: 1;`,  
`.__25_rwd = width: 25%;`,  
`.__33_rwd = width: 33.3%;`,  
`.__50_rwd = width: 50%;`,  
`.__full_rwd = width: 100%;`

```html
<div class="flex_grid">
    <div class="_col_2 __50_rwd">col 1</div> <!--50% on tablet-->
    <div class="_col_3 __50_rwd">col 2</div> <!--50% on tablet-->
    <div class="_col_2 __full_rwd">col 3</div> <!--100% on tablet-->
    <div class="_col_2 __33_rwd">col 4</div> <!--33.3% on tablet-->
    <div class="_col_3 __rwd">col 5</div> <!--flex: 1 on tablet-->
</div>
```

**Tablet breakpoint starts on `1024px`*

---

#### 7. Change the column width for a mobile.

**Pretty much the same logic as for tablet.*

Just apply additional child classes like `.__50_mob` to specify the new width.

Classes:  
`.__mob = flex: 1;`,  
`.__25_mob = width: 25%;`,  
`.__33_mob = width: 33.3%;`,  
`.__50_mob = width: 50%;`,  
`.__full_mob = width: 100%;`

```html
<div class="flex_grid">
    <div class="_col_2 __33_rwd __50_mob">col 1</div> <!--33.3% on tablet, 50% on mobile-->
    <div class="_col_2 __33_rwd __50_mob">col 2</div> <!--33.3% on tablet, 50% on mobile-->
    <div class="_col_2 __33_rwd __full_mob">col 3</div> <!--33.3% on tablet, 100% on mobile-->
    <div class="_col_2 __33_rwd __50_mob">col 4</div> <!--33.3% on tablet, 50% on mobile-->
    <div class="_col_2 __33_rwd __50_mob">col 5</div> <!--33.3% on tablet, 50% on mobile-->
    <div class="_col_2 __33_rwd __full_mob">col 6</div> <!--33.3% on tablet, 100% on mobile-->
</div>
```

**Mobile breakpoint starts on `767px`*

---

## Contributing
Pull requests are welcome.  
If you'll find a way to make this grid even better - let me know!

## License
[MIT](https://choosealicense.com/licenses/mit/)
