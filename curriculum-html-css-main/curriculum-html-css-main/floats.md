# Floats and positioning elements

## Learning objectives

- Use industry-standard tools (floats) to place elements on the page.

### Estimated time: 2h

## Floats

HTML elements are usually blocks that stack one below another, so you will find a new block below the previous one, in the order you have them in the HTML file. `float` is a CSS property that allows you to "float" elements to the right or to the left of other elements in the HTML file. Something that you already know how to do with Flexbox, right?

### Why are floats important?
Even though floats have decreased in usage with the addition of new techniques like Flexbox or CSS Grid, it's worth knowing how to use them. For example, when you have to float an image inside a block of text, the best tool to do it is still a `float`. 
Also, there are plenty of CSS codebases that still use floats. When you need to work on existing code based on floats you should be able to do it.

### Learn more about floats

- Read this nice [guide about CSS floats](https://alistapart.com/article/css-floats-101/) by A List Apart

## Position

`position` is a CSS property that allows you to place elements on the page. Similar to `float`, many `position` use cases have been taken over by new methods of positioning HTML elements such as Flexbox.

### Why is position important?

Again, there are specific use cases that require you to use the `position` property, such as creating a header that stays at the top of the page by positioning an element `fixed` with the page set to scroll. Also, the `position` property is widely used in existing codebases, so it is important to understand how it works when modifying existing code.

### Learn more about position

- First, read the documentation about [CSS position](https://www.w3schools.com/cssref/pr_class_position.asp). Make sure that you check the description of all possible values. In order to better understand **the basic values of the CSS position property** read the parts of the article written by "A List Apart" (it is from 2010 but it explains each value in a creative way).
    - [Static and relative](https://alistapart.com/article/css-positioning-101/#section3)
    - [Absolute](https://alistapart.com/article/css-positioning-101/#section3)
    - [Fixed](https://alistapart.com/article/css-positioning-101/#section5)
    - [Inherit](https://alistapart.com/article/css-positioning-101/#section5)

## Challenge yourself

*Use these questions to check what you learned during this lesson.*
- [20 question quiz about floats and position](https://docs.google.com/forms/d/e/1FAIpQLSfpbzkXZymwals6acIdqrGpazaNU58XuoPcqRZxWRXykT80Eg/viewform)

## Additional materials

*These are all optional, but if you're interested in exploring this topic further, here are some resources to help you. Any exploration here should be done outside program time.*
- Practice with this [visual tutorial of positioning](http://www.barelyfitz.com/screencast/html-training/css/positioning/).

------

_If you spot any bugs or issues in this activity, you can [open an issue with your proposed change](https://github.com/microverseinc/curriculum-transversal-skills/blob/main/git-github/articles/open_issue.md)._
