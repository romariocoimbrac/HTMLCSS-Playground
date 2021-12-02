# Responsive Web Design

When starting a new project, it is important to analyze all the points that will influence your design. There is no right or wrong between mobile-first or desktop-first concepts, it all depends on your project's needs.
With the mobile-first method, the design is minimalist and simplified, with total focus on content. It's worth remembering that most access and sales currently come from mobile devices.

On desktop-first, the interface can contain richer and more detailed features, as the desktop environment usually offers more Internet quality and processing. Some products are desktop-optimized, like Google Docs for example.

## Relative measurement units

REM and EM are relative measurement units that adapt to different types of devices.
It's important that the content automatically adapts to different sizes and spaces. But it's also interesting that these units can be related to situations other than this one.

Understand better when using REM or EM:

**REM** <br>
Is relative to the font-size property of the \<html> tag, I mean, if the \<html> tag has 16px font-size, 1REM will be equivalent to 16px.

**EM** <br>
It is relative to the parent tag, so if the top tag has a font-size of 14px, 1EM will inherit this feature and be equivalent to 14px.

Another interesting trick is to use fixed measurement units to help with responsiveness.
Examples of this are min/max-width or min/max-height or vh (viewport height) / vw (viewport width)

## Adapting the layout through Media Queries

As we've seen, we can start development from different strategies and now we'll see how to adapt your project to different screens and environments.
For this, we use Media Queries, which allow us to create pages with different styles in the same CSS file for different conditions.

An example of these conditions are breakpoints (a true/false condition) which is based for example on the screen width.

There are different conventions about what the value of these breakpoints is, I particularly like 300px for mobile phones, 768px for tablets and 1024 for desktop. You can try and see which measurement suits your project best!

Syntax example:

```
@media screen and (min-width: 768px) {
“styles here”
}
```

You can scale your media queries in different ways. <br>
Using logical operators and media characteristics, for example, can make them even more precise and adequate.

You can learn more about the media queries checking the [MDN documentation](https://developer.mozilla.org/pt-BR/docs/Web/CSS/Media_Queries/Using_media_queries).
