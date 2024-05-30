# Liquid Grid
Shopify's section-based layout system is very flexible, for both developers and merchants. When a developer's theme doesn't provide quite what the merchant needs however, Liquid layout blocks are the ace up your sleeve that can complete the perfect page. 

## The Problem
The [Expanse](https://themes.shopify.com/themes/expanse/styles/classic) theme by [Archetype](https://archetypethemes.co/) provides a flexible three-column layout for Liquid markup blocks, but it's not quite perfect. It's based off of flexbox, and I found myself dealing with issues like hanging margins and limited block slots. I wanted to be able to create a custom number of columns and have them reflow cleanly to fit different screen sizes. In trying to fix these issues however, I realized that the limited capabilities of Liquid and flexbox would make it virtually impossible to achieve what I wanted.

## My Solution
I turned to modern CSS features to solve these issues, creating a customizable and responsive grid-based layout to hold custom liquid blocks. For both desktop and tablet layouts, you can choose the number of columns in the parent container, and the number of columns that each child block should span. The Liquid does the rest, calculating appropriate grid layout rules and interpolating them into CSS variables. The stylesheet picks up the work from there, using media queries to apply the appropriate values as the viewport changes width.
