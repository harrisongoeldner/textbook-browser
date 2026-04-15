# Textbook Browser

🔗 [Live Demo](https://textbook-browser.funkyavocado.dev)

**Author**: Harrison Goeldner  
**Date**: February 1, 2026  

## Overview

This is a multi-page, responsive website that displays a grid of textbook thumbnails. The user can click on the "See more" pop up to view a book's details. This was implemented using HTML5 and CSS3 only, with no Javascript elements. CSS transitions and animations were used to provide a fluid user experience.

## Technical Highlights

- Structuring `index.html` and subsequent book detail pages to convey semantic meaning was a core focus. On the main page this was achieved by breaking it up using sections giving each section an id. The content of each section was broken further by other tags such as `article` or `nav`. The use of `div` was unavoidable, especially for the bootstrap grids, but by wrapping it with semantic tags, the meaning of the section could be conveyed.
- Deciding what animations to include for the "See more" pop up required some iteration. A book jump transition was added first to show which book you were hovering over. Then a "See more" pop up animation followed, with both movement and opacity being animated. Lastly, an arrow nudge animation was added once you hovered over the "See more" button.
- Displaying a book's rating using only CSS required some creative thinking. A CSS variable of percent is passed from the HTML, which is then used to set the width to cover up some of the stars. The following Stack Overflow article was used as inspiration: https://stackoverflow.com/questions/33858426/only-fill-60-percent-star-using-css-width
- Implementing dark mode required converting many of the hardcoded colors in the CSS to variables that could be changed. AI was used to help choose colors that would compliment their light counterpart.
- `prefers-reduced-motion: reduce` was not working as expected. It turned out `!important` was needed after `none`.

## File Structure

The following structure was implemented with books, images, and stylesheets having their own subdirectory.

```text
/ (Root)
├── index.html          # Main gallery page
├── README.md           # Project documentation
├── css/
│   └── styles.css      # Main stylesheet (contains all custom styling)
├── books/
│   ├── book-1.html     # Detail pages for individual books
│   ├── ...
│   └── book-8.html
└── img/
    ├── icon.png        # Site favicon/logo
    ├── 0.jpg           # Textbook thumbnails
    └── ...
```

## References

**Documentation**
- [CSS Reference](https://developer.mozilla.org/en-US/docs/Web/CSS/Reference) — MDN reference for CSS attributes and properties
- [Bootstrap Docs](https://getbootstrap.com/docs/5.3/getting-started/introduction/) — used for grid layout and components

**Assets**
- Logo/favicon sourced from [Flaticon](https://www.flaticon.com/free-icon/text-book_7505034?term=textbooks&page=1&position=9&origin=search&related_id=7505034)
- Fonts sourced from [Google Fonts](https://fonts.google.com/) — [Roboto](https://fonts.google.com/specimen/Roboto) for body text and [Roboto Slab](https://fonts.google.com/specimen/Roboto+Slab?query=roboto+slab) for the logo

## AI Usage

[Gemini](https://gemini.google.com) Pro was used to clarify concepts, look up tags and attributes, and write the four sentence description for each textbook. It was not used to generate any of the code.
