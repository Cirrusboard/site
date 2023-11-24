---
title: Post Layouts
---
Post layouts are a feature in Cirrusboard that originates from the Acmlmboard family of forum software. It can be enabled in the configuration file with the `$postlayouts` variable, but also requires HTML to be enabled. For users, you can see if a forum has post layouts enabled by looking at the Edit profile page, there should be a "Post layouts" section with a header and a signature.

## Making a post layout
When printing out a post, the code inputted in the header will be concatenated above the post's content, and the code inputted in the signature will be concatenated below the post's content. If you only want a traditional forum signature, you can write it in the signature field and keep the "Signature separator" option enabled.

This is an example as to how you would write a post layout into the fields:

```html
<!-- Header -->
 <style>
  /* some CSS here */
 </style>
 <div class="cool-box">
<!-- End Header -->
 Here would be the post's content... blah blah blah!
<!-- Signature -->
 </div>
<!-- End Signature -->
```

Teaching CSS (and HTML) is out of scope of this page, as there are plenty of resources on the Internet if you search around.

Most if not all desktop web browsers come with developer tools (also known as "Inspect Element"). You can open it with Ctrl+Shift+I or by right clicking and clicking "Inspect" in the context menu. This allows you to write your post layout with instant feedback, and can then copy the code you've written back into the post layout fields.

## Post table classes
In order to allow styling of the entire post table, each cell has its own user-unique class to it, suffixed with the user's ID. This image shows the class names of each cell in the post table.

![](/images/post_layout_table_trans.webp)

X represents your user ID, which can be found in the URL of your profile page. As an example, if your user ID is 6 and you'd want to change the font in your sidebar to monospace, you would write your CSS as such:

```css
.sidebar6 {
  font-family: monospace;
}
```

## Notes
- By default the Cirrusboard software prevents the use of CSS filters and animations to reduce the potential amount of lag caused by post layouts.

- For security reasons, external stylesheets, fonts and whatnot are restricted by Cirrusboard's CSP by default.
