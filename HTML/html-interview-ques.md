# HTML Interview Questions

## What is HTML, and why is it important in web development?

HTML is a markup language that defines the structure of the web pages.
It consist of series of elements, represented by tags which wrap around content to give it meaning and purpose. These elements tell browsers how to display and interpret the content of a web page.

KEY POINTS :

-     It uses tags(enclosed in angle brackets) to define elements.
- Elements often come in pairs with opening and closing tags.
-     HTML documents consist of a series of nested elements.

## What are semantic HTML tags?

Semantic HTML tags are elements that conveys the meaning of the content they contain, unlike non-semantic tags like <div> and <span> which serves only as generic containers.
Ex: <header> , <article>, <footer> <nav>, <section>

Key points about semantic HTML tags:

- They clearly indicate the role of the content they contain.
- They improve the accessibility and SEO of web pages.
- They were introduces in HTML5 to provide better structure to web documents.

These tags help organize the structure of a web page, making it easier for browsers, search engines, and assistive technologies to understand the layout and importance of different sections.

Benefits of using Sematic HTML tags:

1. Improved Accessibility
2. Better SEO
3. Easier Maintenance
4. Enhanced User Exp.

## Q. How do semantic HTML tags improve SEO compared to non-semantic tags?

Semantic HTML tags can significantly improve SEO compared to non-semantic tags by providing clearer structure and meaning to web content.
Semantic HTML tags help search engines better understand the structure and hierarchy of a webpage’s content .

- Tags like <header> <nav> <main> and <footer> clearly define different sections of a page.
- Elements like <article> <section> group related content together.
- Tags like <h1> to <h6> establish a clear heading hierarchy.

This improved understanding allows search engines to more accurately interpret and index page content.
Semantic readers and assistive technologies can better navigate and interpret content structure.
Improved accessibility leads to better user experiences across devices and browsers. In conclusion, while semantic HTML doesn’t directly boost rankings, it significantly enhances how search engines interpret and index content. This leads to improved SEO outcomes through better content understanding, enhanced accessibility, and potential advantages in emerging search technologies.

## Q. What is the difference between div and span?

The main difference between <div> and <span> tags in HTML are:
Display type: div is a block-level element whereas <span> is an inline element.
It means <div> creates a new block on the page, while <span< stays inline with surrounding content.

- Usage: <div> is used to group block-level elements or create sections of a document while <span> is used to apply styles to small portions of a text or inline elements within a larger container.
- Default Styling: <div> typically starts on a new line and takes up full width whereas <span> does not start on a new line and only takes spaces needed for its content.

In practice, <div> is often used for layout purposes, while <span> is commonly used for inline styling or wrapping small portions of text. However, with introduction of semantic HTML5 elements, its generally recommended to use more meaningful tags when possible, reserving <div> and <span> for situations where no semantic tags fits the purpose.

## Q. What is the purpose of the alt attribute in the img tag?

The alt attribute provides alternative text for an image. Its main purposes are:

1. To describe the content of the image for users who cannot see it.
2. To provide information about the image when it fails to load due to network issues or incorrect file paths.
3. It provides another opportunity to include relevant keywords associated with the image content. This can potentially improve how search engines index and rank images.

## Q. Explain the difference between block-level and inline-level elements.

The main differences between block-level and inline-level elements in HTML are

1. Block-level start a new line -> Inline-level do not start on a new line
2. Block-level take up the full width available -> inline-level only takes up as much width as necessary.
3. Block level elements automatically add some space(margin) before and after the elements.
4. Block-level elements are often used for grouping other elements -> Inline-level represents smaller pieces of content with a larger unit.
   Example of block-level elements include : <div> <p> <h1> <article> <section>
   Example of inline-level elements include : <span> <strong> <em> <a>

## Q. What is the purpose of the DOCTYPE declaration in HTML?

The DOCTYPE declaration in HTML serves several important purposes:

1. It informs the browser which version of HTML the document is written in.
2. It triggers standards mode rendering in browsers, ensuring consistent interpretation in HTML and CSS.
3. In older HTML version, it referred to a Document Type Definition (DTD) that defined the allowed structure and elements.
4. It enables proper functioning of HTML validators and other development tools.
5. By declaring HTML version, it helps ensure that different browsers render the page similarly.

In summary, the DOCTYPE declaration is crucial for proper HTML document structure, cross-browser compatibility, and standard-compliant rendering, It ensure that browsers interpret and display web pages consistently according to the specified HTML version.

## What is the meta tag used for in HTML?

The meta tag in HTML serves several important purposes:

1. Provides metadata about the document :

- - Includes information like character encoding, document type, author, copyright, etc.
- - Helps browsers and search engines understand the content and structure of the page.
    Key Points:

1. Meta tags are invisible to regular users but crucial for search engines and browsers.
2. They don’t directly affect page content but influence how it’s interpreted and displayed.
3. Different types of meta tags serve various purposes, from SEO to device optimization.
4. While some meta tags are important for SEO, others are more focused on user experience and accessibility.

In summary, meta tags provide essential information about a web page that goes beyond its visible content. They help optimize the page search engines, improve accessibility, and control how the page behaves in different context.

## Q. What is the purpose of the href attribute in the a tag?

The href attributes in the <a> tag specifies the URL or link destination the user will be directed to when the link is clicked. It stands for “Hypertext reference”. It can be used for linking to various resources, such as:

1. Internal Links: Navigating within the same website (href=”/about”).
2. External Links: Naviagting to another website (href=https://example.com).
3. Email Links: Opening a new email in the default mail app ( href: “mailto:someone@example.com”)
4. Fragment Identifiers: Jumping to a specific section of the same page (href=”#section”).
   Without href attribute, the <a> tag won’t be clickable, and it won’t function as a link.

## Q. What is the difference between id and class attributes in HTML?

The id and class attributes in HTML are both for selecting elements and applying styles or scripts, but they serve different purposes:

1. Id Attribute:

- - Uniqueness : the id is unique within a document, meaning it can only be assigned to one element. It is ideal for identifying a single element for styling, scripting, or linking.
- - Usage : It is typically used for targeting a specific element in JS or CSS . For Example, #header {} in CSS refers to an element with the id=”header”
- - Example: <div id=”header”>Header Content</div>

2. class Attribute:

- - Reusability : The class attribute is not unique and can be assigned to multiple elements. This makes it suitable for grouping elements that share the same styles or behaviour.
- - Usage: It is primarily used for applying the same styles or JS behaviour to multiple elements. For example, .button {} in CSS can be applied to any element with class=”button”.
- - Example: <div class=”button”>Button 1</div> and <div class=”button”>Button 2></div>
- The id is unique and used for one element while class can be reused across multiple elements. In CSS and JS, id selectors have higher specificity than class selectors.

## Q. What is the purpose of the data-\* attribute in HTML?

The data-\* attribute in HTML is used to store custom data that can be accessed in JS, while still adhering to HTML standards. These attributes allow developers to add additional information to HTML elements without cluttering the element with non-standard attributes or relying on classes or IDs for data storage.

## Q. What are input types in HTML forms? Can you name a few?

In HTML forms, the <input /> element is used to create interactive fields where users can input data. The type attribute of the <input/> element determines what kind of data the input will accept and how the browser will render the field.

There are several types of input fields in HTML, each designed for specific types of data collection. Some commonly used input types include:

1. Text : <input type=”text” name=”username”>
2. Email : <input  type=”email” name=”useremail” >
3. Password : <input type=”password” name=”userpassword”>
4. Number : <input type=”number” name=”age” min=”18” max=”99”>
5. Date: <input type=”date” name=”dob”>
6. Radio: <input type=”radio” name=”gender” value=”male>Male
7. Checkbox: <input type=”radio” name=”subscribe” checked>Subscribe
8. File: <input type=”file” name=”resume”>
9. Submit: <input type=”submit” value=”submit>
   Different input types enhance user experience by providing appropriate input controls for various data types, helping with validation and improving accessibility.

## Q. Explain the concept of accessibility in HTML. How can you improve it?

Accessibility in HTML refers to designing and developing web pages in a way that they are usable by everyone, including individuals with disabilities such as visual, auditory, motor, or cognitive impairments. The goal is to make the web accessible to as many users as possible, regardless of their abilities or the assistive technologies they may use such as scrren readers or voice inputs tools.
Ways to improve accessibility:

1. Use Semantic HTML
2. Provide alternative text for images (alt attributes)
3. Accessible Forms: Using associated <labels> elements
4. Keyboard navigation
5. Provide text alternatives for Media

## Q. What is localStorage in HTML5, and how is it different from sessionStorage?

localStorage in HTML5 is a web storage feature that allows you to store key-value pairs in a web browser. The stored data persists even after the browsers is closed and reopened, making it useful for saving data that needs to be available across multiple sessions.

Key features:

1. Persistent Storage : Data stored in localStorage remains until explicitly deleted by the user or programmatically through JS
2. Capacity : localStorage typically allows around 5-10MB of storage, depending on the browser.
3. Same-origin Policy : The data is accessible only by the pages of the same domain and protocol.

```bash
// Storing data
localStorage.setItem('username', 'Abhishek');

// Retrieving data
let username = localStorage.getItem('username');

// Removing data
localStorage.removeItem('username');

// Clearing all data
localStorage.clear();
```

- How is localStorage different from sessionStorage?
  While both are part of the web storage API, they differ in terms of lifetime and use cases:
- - Data Persistence:
- localStorage: Persists indefinitely, even after the browser is closed and reopened.
  sessionStorage: Data is available only for the duration of the page session. Once the browser or tab is closed, the data is lost.
- - Scope:
- localStorage: Data is shared across all browser tabs and windows that have the same origin (domain and protocol).
  sessionStorage: Data is confined to the specific tab or window where it was created. Each tab has its own separate sessionStorage.
- - Use Case:
- localStorage is ideal for storing data that needs to persist across sessions, like user preferences, theme settings, or cart items in an e-commerce site.
- - sessionStorage is better suited for temporary data that’s needed only for a single session, such as form data while navigating between pages.

```bash
// Storing data
sessionStorage.setItem('sessionID', '12345');

// Retrieving data
let sessionID = sessionStorage.getItem('sessionID');

// Removing data
sessionStorage.removeItem('sessionID');

// Clearing all session data
sessionStorage.clear();

```

## Q. What are some common HTML tags used for table creation, and what are their purposes?
