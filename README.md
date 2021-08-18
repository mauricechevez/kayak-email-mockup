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
Comming soon.....

## Original project idea
Codingphase.com's [HTML Email Frameworks](https://codingphase.teachable.com/p/html-email-frameworks)

## Colors Used
```
background: #f1f4f7
light orange: #ff6a10;
dark orange : 
greyish blue: #222d37;
dark blue: #14191e;
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

### Copyright Notice
No copyright infringment is intended. I don't own any of the assets within. This is for educational purposes only.