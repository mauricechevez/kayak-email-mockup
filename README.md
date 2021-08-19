# Kayak Email Mockup Project
This will be a fully responsive mockup of a Kayak.com marketing email. 

## Technologies used
[Zurb's Foundations for Email Framework](https://get.foundation/emails/docs/panini.html), which includes:

* Panini templating engine
* HTML
* SCSS
* JavaScript

## Preview of Project
This is the intended result.

![project preview](./src/assets/img/email.png)

## Current Results
![Current screenshot](./img-screenshots/current-aug8.png)

## Original project idea
Codingphase.com's [HTML Email Frameworks](https://codingphase.teachable.com/p/html-email-frameworks)

## Colors Used
```
background: #f1f4f7
light orange: #ff6a10;
dark orange : #d65600
light-grey: #EFF2F6
greyish blue: #222d37;
dark color: #14191e;
```

## Important Quirks
A few issues occured along the way which I want to highlight here. 
### Columns stacking on top of each other in **Firefox**
Despite the columns aligning correctly in Chrome, Firefox was not displaying the columns in the correct order. For example, if I wanted 2 columns next to each other, Chrome would display it correctly, but Firefox did not. THe solution found was to add the following code under the container row.
```css
 white-space: nowrap;
```
The other way around this is to not stack your code. Make the closing and opening column tags sit right next to each other. I don't like the way it looks in VSCode, so I kept the first solution.
```html
<column>
....
</column><column>
...
</column>
Next bits of code....
```
### Padding issues within nested rows/columns
Foundations framework has built in settings in the _settings.scss_ file. One that kept throwing me off was the padding-bottom global setting. I ended up setting that to 0 so I could customize each column's padding as I'd like. This is under the "Grid" section.
If setting the padding of column (assigned to a class) doesn't work, then select the `<th>` element and add padding there instead.

### Centering content
Though centering content works by using a `<center>` or using class of `text-align-X(left,center, or right)`, I had to center the content of the subheader by targeting the `<th>` element. 

First target the .columns (`<columns>` in the HTML), then nest the `th` selector within and center your content there
```css
.sub-header{
 /* selectors.... */
  .columns{
    padding-top: 5px;
    padding-bottom: 5px!important;
    padding-left: 10px!important;
    padding-right: 10px!important;
 /* selectors.... */
    th{
      text-align: center;
    }
  }
}
```

---
### Copyright Notice
No copyright infringment is intended. I don't own any of the assets within. This is for educational purposes only.