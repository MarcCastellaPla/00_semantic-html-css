### README.md

# HTML Semantics and CSS Foundations

This project introduces the basics of semantic HTML, CSS, source version control using Git and GitHub, and deployment via CI/CD platforms such as Netlify.

---

## Semantic HTML

### What is HTML?

**HTML (HyperText Markup Language)** is the standard language used to create web pages. It structures content using elements represented by tags, allowing browsers to display text, images, and multimedia content in a structured manner.

### Principal HTML Semantic Tags

Semantic HTML tags help to clearly define the structure and meaning of content within a webpage. Here are some of the most commonly used semantic tags in HTML, along with brief explanations and examples:

- **`<header>`**: Defines the header section of a document or section. Typically contains introductory content like a logo, navigation, or heading.

  Example:

  ```html
  <header>
    <h1>Welcome to My Website</h1>
  </header>
  ```

- **`<nav>`**: Represents a section of navigation links. It's usually used for primary site navigation.

  Example:

  ```html
  <nav>
    <a href="#home">Home</a>
    <a href="#about">About</a>
    <a href="#contact">Contact</a>
  </nav>
  ```

- **`<main>`**: Represents the main content of the document. It should only be used once per page to encapsulate the central content.

  Example:

  ```html
  <main>
    <h2>Main Content</h2>
    <p>This is the primary section of the page.</p>
  </main>
  ```

- **`<section>`**: Defines a section in the document. It’s used to group related content, typically with a heading.

  Example:

  ```html
  <section>
    <h2>About Us</h2>
    <p>We are a company that specializes in web development.</p>
  </section>
  ```

- **`<article>`**: Represents a self-contained, independent piece of content, such as a blog post, news article, or forum post.

  Example:

  ```html
  <article>
    <h2>Blog Title</h2>
    <p>This is an article content, which stands alone.</p>
  </article>
  ```

- **`<aside>`**: Represents content that is related to the main content but is not essential to the overall document. It is often used for sidebars or other supplementary content.

  Example:

  ```html
  <aside>
    <h3>Related Links</h3>
    <ul>
      <li><a href="#">Link 1</a></li>
      <li><a href="#">Link 2</a></li>
    </ul>
  </aside>
  ```

- **`<footer>`**: Defines the footer for a document or section, typically containing metadata, links, or author information.

  Example:

  ```html
  <footer>
    <p>&copy; 2024 My Website</p>
  </footer>
  ```

- **`<form>`**: Defines a form for user input, containing interactive elements like input fields, buttons, etc. Forms are essential for collecting data from users.

  Example:

  ```html
  <form action="/submit" method="post">
    <label for="name">Name:</label>
    <input type="text" id="name" name="name" />
    <button type="submit">Submit</button>
  </form>
  ```

- **`<ul>` (Unordered List)**: Represents a list of items in no particular order. It typically uses bullet points.

  Example:

  ```html
  <ul>
    <li>Item 1</li>
    <li>Item 2</li>
    <li>Item 3</li>
  </ul>
  ```

- **`<ol>` (Ordered List)**: Represents a numbered list of items.

  Example:

  ```html
  <ol>
    <li>First item</li>
    <li>Second item</li>
    <li>Third item</li>
  </ol>
  ```

- **`<li>` (List Item)**: Defines an item in a list, used inside `<ul>` or `<ol>`.

  Example:

  ```html
  <ul>
    <li>Item 1</li>
    <li>Item 2</li>
  </ul>
  ```

- **`<figure>` and `<figcaption>`**: The `<figure>` tag is used to group media content like images, diagrams, or illustrations, while `<figcaption>` provides a caption for the figure.

  Example:

  ```html
  <figure>
    <img src="image.jpg" alt="Example image" />
    <figcaption>An example caption for the image</figcaption>
  </figure>
  ```

- **`<table>`**: Defines a table with rows and columns to display tabular data.

  Example:

  ```html
  <table>
    <tr>
      <th>Name</th>
      <th>Age</th>
    </tr>
    <tr>
      <td>John</td>
      <td>28</td>
    </tr>
  </table>
  ```

- **`<em>`** and **`<strong>`**: These tags are used for emphasis. `<em>` usually renders text in italics, and `<strong>` makes it bold, with added meaning of emphasis for assistive technologies.

  Example:

  ```html
  <p>This is an <em>important</em> message.</p>
  <p>This is a <strong>very important</strong> message.</p>
  ```

These semantic tags help improve both the accessibility and readability of your HTML code. They ensure that browsers and screen readers can better understand and process the structure of your web pages.

---

## CSS

### What is CSS?

**CSS (Cascading Style Sheets)** is a style sheet language used for describing the presentation of a document written in HTML. It controls the layout, colors, fonts, and overall visual appearance of the web page, allowing for separation between structure and design.

### What is a Sanitize CSS File?

A **sanitize CSS file** is a collection of CSS rules that removes inconsistencies between different browsers' default styles. It ensures a clean and consistent base for web development by resetting or normalizing browser styles.

### Most Important Ways to Define CSS Selectors

In CSS, selectors are used to target HTML elements for styling. Here’s an extended list of the most important and commonly used CSS selectors, along with brief explanations and examples:

1. **Element Selector**: Targets all instances of a specific HTML element.

   Example:

   ```css
   p {
     color: blue;
   }
   ```

   This will change the text color of all `<p>` elements to blue.

2. **Class Selector**: Targets elements with a specific class attribute. Class selectors are denoted by a period (`.`).

   Example:

   ```css
   .button {
     background-color: red;
   }
   ```

   This will apply the background color to all elements with the class `button`.

3. **ID Selector**: Targets a single, unique element with a specific `id` attribute. The ID selector is prefixed by a hash (`#`).

   Example:

   ```css
   #header {
     font-size: 2rem;
   }
   ```

   This will set the font size for the element with the ID `header`.

4. **Descendant Selector**: Targets elements that are nested inside another element. It's written by listing elements in a space-separated manner.

   Example:

   ```css
   div p {
     margin-left: 20px;
   }
   ```

   This will apply the margin to all `<p>` elements inside any `<div>`.

5. **Child Selector**: Targets elements that are direct children of a specified parent element. It is written using a greater-than sign (`>`).

   Example:

   ```css
   ul > li {
     list-style-type: none;
   }
   ```

   This will remove the bullet points for `<li>` elements that are direct children of a `<ul>`.

6. **Adjacent Sibling Selector**: Targets an element that is immediately preceded by a specific element. It is written using a plus sign (`+`).

   Example:

   ```css
   h1 + p {
     margin-top: 0;
   }
   ```

   This will remove the margin at the top of any `<p>` that directly follows an `<h1>`.

7. **General Sibling Selector**: Targets all elements that are siblings of a specified element. It is written using a tilde (`~`).

   Example:

   ```css
   h2 ~ p {
     color: gray;
   }
   ```

   This will apply the gray color to all `<p>` elements that are siblings of an `<h2>`.

8. **Attribute Selector**: Targets elements based on the presence or value of an attribute. It is written using square brackets (`[]`).

   Example:

   ```css
   input[type="text"] {
     border: 1px solid black;
   }
   ```

   This will apply a border to all `<input>` elements with the `type="text"` attribute.

9. **Pseudo-Class Selector**: Targets elements in a specific state, such as when the user hovers over or focuses on them. Pseudo-classes are prefixed with a colon (`:`).

   Example:

   ```css
   a:hover {
     color: green;
   }
   ```

   This will change the color of any `<a>` element to green when hovered over.

10. **Pseudo-Element Selector**: Targets specific parts of an element, such as the first letter or first line of text. Pseudo-elements are prefixed with two colons (`::`).

    Example:

    ```css
    p::first-letter {
      font-size: 2rem;
    }
    ```

    This will enlarge the first letter of each `<p>` element.

11. **Universal Selector**: Targets all elements on the page. It is represented by an asterisk (`*`).

    Example:

    ```css
    * {
      margin: 0;
      padding: 0;
    }
    ```

    This will remove all default margin and padding from every element on the page.

12. **Group Selector**: Targets multiple elements by separating selectors with a comma (`,`). This applies the same styles to different elements.

    Example:

    ```css
    h1,
    h2,
    h3 {
      font-family: Arial, sans-serif;
    }
    ```

    This will apply the same font family to all `<h1>`, `<h2>`, and `<h3>` elements.

> [!Tip]  
> These selectors allow for precise targeting of HTML elements, enabling you to create complex styles and behaviors across different parts of your web page. They are fundamental to applying styles efficiently and cleanly in CSS.

## CI/CD

### Git/GitHub

#### What is Git?

**Git** is a distributed version control system that tracks changes in source code during software development. It allows developers to collaborate, track code history, and manage project versions.

#### What is GitHub?

**GitHub** is a platform for hosting Git repositories. It provides additional features such as collaboration tools, issue tracking, pull requests, and project management.

### CI (Continuous Integration)

**CI (Continuous Integration)** is the practice of automating the process of merging code changes into a shared repository frequently. It ensures that any integration errors are identified and addressed quickly, allowing teams to build, test, and verify code efficiently.

---

### Deployment

#### What is Deployment?

**Deployment** is the process of releasing and distributing a web application or website to a hosting server, making it accessible to users on the internet. In modern development, deployment typically involves automating processes such as code testing, building, and pushing changes to production.

#### Why is Deployment Important?

Deployment ensures that your project is accessible to its users and operates in a live environment. With automated deployment pipelines, developers can continuously deliver updates, reduce human error, and maintain consistent, working software across development, testing, and production stages.

#### Main CI/CD Platforms

Some of the most widely used platforms for CI/CD and deployment are:

- **Netlify**: Easy-to-use, continuous deployment for static websites.
- **GitHub Actions**: GitHub's native CI/CD pipeline solution integrated directly with repositories.
- **CircleCI**: A powerful, customizable CI/CD platform with extensive integration options.
- **Jenkins**: Open-source automation server used to build, test, and deploy software.
- **Travis CI**: A continuous integration service used to build and test software projects hosted on GitHub.

### Source

Here is a list of resources and official documentation for CI/CD providers as well as HTML and CSS:

#### CI/CD Providers

- **Netlify**: [https://www.netlify.com](https://www.netlify.com)  
  Documentation: [https://docs.netlify.com](https://docs.netlify.com)
- **GitHub Actions**: [https://github.com/features/actions](https://github.com/features/actions)  
  Documentation: [https://docs.github.com/en/actions](https://docs.github.com/en/actions)
- **CircleCI**: [https://circleci.com](https://circleci.com)  
  Documentation: [https://circleci.com/docs](https://circleci.com/docs)
- **Jenkins**: [https://www.jenkins.io](https://www.jenkins.io)  
  Documentation: [https://www.jenkins.io/doc](https://www.jenkins.io/doc)
- **Travis CI**: [https://travis-ci.org](https://travis-ci.org)  
  Documentation: [https://docs.travis-ci.com](https://docs.travis-ci.com)

#### Official HTML and CSS Documentation

- **HTML Official Documentation**: [https://developer.mozilla.org/en-US/docs/Web/HTML](https://developer.mozilla.org/en-US/docs/Web/HTML)

- **CSS Official Documentation**: [https://developer.mozilla.org/en-US/docs/Web/CSS](https://developer.mozilla.org/en-US/docs/Web/CSS)

These resources will help you explore further into CI/CD processes and web development with HTML and CSS.
