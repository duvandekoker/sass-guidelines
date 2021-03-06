
# Tools

What’s nice about a CSS preprocessor as popular as Sass is that it comes with a whole ecosystem of frameworks, plugins, libraries and tools. After 8 years of existence, we are getting closer and closer to the point where [everything that can be written in Sass has been written in Sass](https://hugogiraudel.com/2014/10/27/rethinking-atwoods-law/).

However my advice would be to lower the number of dependencies to the strict minimum. Managing dependencies is some sort of hell you don’t want to be part of. Plus, there is little to no need for external dependencies when it comes to Sass.

## Compass

[Compass](http://compass-style.org/) is the main [Sass framework](https://www.sitepoint.com/compass-or-bourbon-sass-frameworks/) out there. Developed by [Chris Eppstein](https://twitter.com/chriseppstein), one of the two core designers of Sass, I don’t see it dramatically losing in popularity for a while, if you want my opinion.

Still, [I do not use Compass anymore](https://www.sitepoint.com/dont-use-compass-anymore/), the main reason is that it slows Sass down a lot. Ruby Sass is quite slow in itself, so adding more Ruby and more Sass on top of it doesn’t really help.

The thing is, we use very little from the whole framework. Compass is huge. Cross-browser compatibility mixins is just the tip of the iceberg. Math functions, image helpers, spriting… There is so much that can be done with this great piece of software.

Unfortunately, this is all sugar and there is no killer feature in there. An exception could be made of the sprite builder which is *really great*, but [Grunticon](https://github.com/filamentgroup/grunticon) and [Grumpicon](http://grumpicon.com/) do the job as well, and have the benefit of being pluggable in the build process.

Anyway, I do not forbid the use of Compass although I would not recommend it either, especially since it is not LibSass-compatible (even if efforts have been made in that direction). If you feel better using it, fair enough, but I don’t think you’ll get much from it at the end of the day.

<div class="note">
  <p>Ruby Sass is currently going under some outstanding optimizations that are specifically targeted at logic-heavy styles with many functions and mixins. They should dramatically improve performance to the point where Compass and other frameworks might not be slowing Sass anymore.</p>
</div>

## Grid systems

Not using a grid system is not an option now that Responsive Web Design is all over the place. To make designs look consistent and solid across all sizes, we use some sort of grid to lay out the elements. To avoid having to code this grid work over and over again, some brilliant minds made theirs reusable.

Let me put this straight: I am not a big fan of grid systems. Of course I do see the potential, but I think most of them are completely overkill and are mostly used to draw red columns on a white background in nerdy designers’ speaker decks. When is the last time you thought *thank-God-I-have-this-tool-to-build-this-2-5-3.1-π-grid*? That’s right, never. Because in most cases, you just want the usual regular 12-columns grid, nothing fancy.

If you are using a CSS framework for your project like [Bootstrap](https://getbootstrap.com/) or [Foundation](https://get.foundation/), chances are high it includes a grid system already in which case I would recommend to use it to avoid having to deal with yet another dependency.

If you are not tied to a specific grid system, you will be pleased to know there are two top-notch Sass powered grid engines out there: [Susy](https://www.oddbird.net/susy/) and [Singularity](https://github.com/at-import/Singularity). Both do much more than you will ever need so you can pick the one you prefer between these two and be sure all your edge cases&mdash;even the most nifty ones&mdash;will be covered. If you ask me, Susy has a slightly better community, but that’s my opinion.

Or you can head over to something a bit more casual, like [csswizardry-grids](https://github.com/csswizardry/csswizardry-grids). All in all, the choice will not have much of an impact on your coding style, so this is pretty much up to you at this point.

## SCSS-lint

Linting code is very important. Usually, following guidelines from a styleguide helps reducing the amount of code quality mistakes but nobody’s perfect and there are always things to improve. So you could say that linting code is as important as commenting it.

[SCSS-lint](https://github.com/causes/scss-lint) is a tool to help you keep your SCSS files clean and readable. It is fully customisable and easy to integrate with your own tools.

Fortunately, SCSS-lint recommendations are very similar to those described in this document. In order to configure SCSS-lint according to Sass Guidelines, may I recommend the following setup:

{% include snippets/tools/01/index.html %}

If you are not convinced of the necessity to use SCSS-lint, I recommend reading these great articles: [Clean Up your Sass with SCSS-lint](https://blog.martinhujer.cz/clean-up-your-sass-with-scss-lint/), [Improving Sass code quality on theguardian.com](https://www.theguardian.com/info/developer-blog/2014/may/13/improving-sass-code-quality-on-theguardiancom) and [An Auto-Enforceable SCSS Styleguide](https://davidtheclark.com/scss-lint-styleguide/).

<div class="note">
  <p>If you want to plug SCSS lint into your Grunt build process, you will be pleased to know there is a Grunt plugin for that called <a href="https://github.com/ahmednuaman/grunt-scss-lint">grunt-scss-lint</a>.</p>
  <p>Also, if you are on the hunt for a neat application that works with SCSS-lint and the like, the guys at <a href="https://thoughtbot.com/">Thoughtbot</a> (Bourbon, Neat…) are working on <a href="https://houndci.com/">Hound</a>.</p>
</div>
