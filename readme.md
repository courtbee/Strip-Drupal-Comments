# README

Strip Comments is an extremely simple module that prevents comments from being displayed, as well as the *Add new comment* link.

This small module basically removes the annoying stuff while leaving the builder and/or themer free to display and theme comments as they wish to.

## NOTES

This may not be the most efficient way to remove/hide comments and comment links as, I believe, it's still querying the database? If you use this module, you do so at your own risk. I *am* a themer/designer... ;)

Also, this module does not mess with the text format inputs. I was worried that I would mess up the sanitization of the form so I opted to leave that out. I'd recommend using the [Better Formats](https://www.drupal.org/project/better_formats) module to handle that part of the display.

## HELP WITH CUSTOMIZING COMMENT DISPLAY

It's fairly simple to build your own comment display via Views. This is my preferred method as it gives great control over the markup of each comment. I'll outline the steps below:

1. Add New View -> Show -> Select Comments from select list
2. Fill in the other fields as necessary, making sure to uncheck "create a page" and selecting "create a block"
3. Use fields to output the elements of the comment you want to display
4. Tie the block to a node by adding the contextual filter: Content: NID
5. In the Content:NID options, select "Provide default value" and the select "Content ID from URL"
6. Place the block via your preferred method (e.g., context, block administration page)
7. To get the User picture in the comment, add the "Comment: Author" relationship which will open up the User: Picture field.

## END NOTE

If you have any suggestions on making this module better, don't hesitate to open an issue! This is actually the first module I've ever built so I doubt it's as awesome as it could be.
