---
layout: ../../layouts/PostLayout.astro
title: Unveiling the Transformative Potential of React
author: Joseph Herrera
date: 02-29-2024
---


They say all paths lead to Rome, for Software development all projects lead to reusability. 
I'll tell you about my journey on how I discovered this developer superpower.

# The problem
I was developing an static website. After some pages, rewriting parts (which I now call components) seemed redundant. 
Why waste time making a navigation bar if every time it's going to work exactly the same? 
Well, good old copy-paste will do the trick, but then came another problem, making changes.

## Changes are tedious
Let's say you have a simple nav bar:

```html
 <nav>
    <ul>
      <li><a href="/home">Home</a></li>
      <li><a href="/about">About</a></li>
      <li><a href="/services">Services</a></li>
      <li><a href="/contact">Contact</a></li>
    </ul>
  </nav>
```

You want to call services another way, well since it's a nav bar it's going to be exactly the same for every page, so you'll need to change all of them. 
You get the point, there must be a better way.

# html inside html?
At this point I didn't know JavaScript, which as we'll see later on, is the best option. 
So, what other option did I have with my limited knowledge? html embed. 
This might seemed odd to you, since this tag primary use is to add multimedia content to the website, but I came up with something. 
At that moment I didn't know, but it was similar to components in React on some way.

## First solution
It was very simple, I had an html page named nav.html with only the nav bar, like from the example above. Then, add it using embed on top of all my pages.

```html
<body>
  <embed src="nav.html" width="100%" height="50">
  <!-- The rest of the page content -->
</body>
```

Notice how this solution brings many benefits. First of all, it's saving you code writing, instead of coding the nav on all pages,  you only need to write it once and "link it". 
Of course, you also don't need to rewrite any changes on all pages if you change something to your nav. 
If you want a truly static website with no JavaScript, this solution might save you some time.

Sadly, it comes with it's down sides. 
My main issue was that I couldn't include something a little different to every nav bar, like an underline to the current page.

# React to the rescue
I later learned about React and the use of components (Vue and Angular have a similar approach). From the React documentation it's explained that:


> React apps are made out of components. A component is a piece of the UI (user interface) that has its own logic and appearance. A component can be as small as a button, or as large as an entire page.

Now, I made a Navbar component, added to every page I needed it. 
Changes reflect on all pages and I can make something different for each one. 
The component will look like this:

```jsx
import React from 'react';
import { Link } from 'react-router-dom';

const Navbar = () => {
  return (
    <nav>
      <ul>
        <li>
          <Link to="/">Home</Link>
        </li>
        <li>
          <Link to="/about">About</Link>
        </li>
        <li>
          <Link to="/services">Services</Link>
        </li>
        <li>
          <Link to="/contact">Contact</Link>
        </li>
      </ul>
    </nav>
  );
};

export default Navbar;
```
# Even more resources
Of course, reusability doesn't stop there, there's many more resources to make your life easier.

## Tailwind
Tailwind is a very popular css framework, that helps prevent code repetition by grouping the css styles into classes that you can call.

## Flowbite
On top of that, you have flowbite; an open-source library of over 600+ UI components, sections, and pages built with the utility classes from Tailwind CSS. There's many options similar, tailwind has it's own library of components, but I like flowbite approach in what they call blocks.

## Storybook
Storybook helps you with the design. It groups all the components your project has and helps you make your design system.

# Conclusion
We looked at my journey from a simple static website to the use of more powerful tools and beyond. 
In this growing time for software development, I recommend taking some time to understand why the tools we use are made that way, 
basically what problem did they try to solve.
