<p align="center">
  <img src="https://i.postimg.cc/3N3H59FN/logo.png" width="200" alt="logo">
</p>

<h1 align="center">
  Bankist Website [Learning]
  <br>
<p  align="center">
<a  href="https://developer.mozilla.org/en-US/docs/Web/JavaScript"  target="_blank"  rel="noreferrer"> <img  src="https://raw.githubusercontent.com/devicons/devicon/master/icons/javascript/javascript-original.svg"  alt="javascript"  width="48"  height="48"/> </a>
</p>
</h1>

<p align="center">
  <a href="#project-description">Project Description</a> |
  <a href="#tech-stack-and-libraries">Tech Stack and Libraries</a> |
  <a href="#how-it-works">How it Works</a> |
  <a href="#code-examples">Code Examples</a> |
  <a href="#acknowledgements">Acknowledgements</a>
</p>

<br>

[![Thumbnail-4.png](https://i.postimg.cc/nVjNLXLT/Thumbnail-4.png)](https://postimg.cc/hhn2yPT7)


<div id="project-description"></div>

## 🚀 Project Description
This project is a website called "Bankist" that was built as part of a web development course. The website was built using HTML, CSS, and JavaScript and incorporates various web development concepts such as working with the DOM, handling events, implementing smooth scrolling, building tabbed components, and lazy loading images.

<div id="tech-stack-and-libraries"></div>

## 🛠️ Tech Stack and Libraries
- JavaScript
- HTML
- CSS

<div id="how-it-works"></div>

## ⚙️ How it Works
The website consists of several sections and includes various interactive components such as tabs, sliders, and smooth scrolling. The user can navigate through the sections using the navigation menu at the top of the page. The site also incorporates lazy loading of images to improve performance.

<div id="code-examples"></div>

## 💻 Code Examples
**1. An example of Lazy-loading images on a webpage**
```js
const loadImg = function (entries, observer) {
  const [entry] = entries;

  if (!entry.isIntersecting) return;

  // Replace src with data-src
  entry.target.src = entry.target.dataset.src;

  entry.target.addEventListener("load", function () {
    entry.target.classList.remove("lazy-img");
  });

  observer.unobserve(entry.target);
};
```
The ```loadImg``` function uses the IntersectionObserver API to lazy-load images on a webpage. It replaces the ```src``` attribute
with ```data-src``` when an image enters the viewport. Once the image has loaded, it removes the ```lazy-img``` class from the image
element and stops observing the current element using ```observer.unobserve```. This function can significantly improve
webpage performance by reducing unnecessary network requests and improving page load speed.

**2. An exemple of Smooth Scrolling implementation:**
```js
// Button scrolling
btnScrollTo.addEventListener("click", function (e) {
  const s1coords = section1.getBoundingClientRect();
  console.log(s1coords);

  console.log(e.target.getBoundingClientRect());

  console.log("Current scroll (X/Y)", window.pageXOffset, window.pageYOffset);

  console.log(
    "height/width viewport",
    document.documentElement.clientHeight,
    document.documentElement.clientWidth
  );

  section1.scrollIntoView({ behavior: "smooth" });
});
```
This code adds a click event listener to a button element to smoothly scroll the page to a target element. It calculates the target element's position relative to the viewport using ```getBoundingClientRect()``` and logs it, along with the position of the button element and the current scroll position, to the console. It can be used to implement smooth scrolling and aid in debugging scroll-related issues.

<div id="acknowledgements"></div>

## 📚 Acknowledgements 
This project was created with the help of the course **"The Complete JavaScript Course 2023: From Zero to Expert!"** by **Jonas Schmedtmann**. Many of the concepts and techniques used in this project were learned from this valuable resource.
