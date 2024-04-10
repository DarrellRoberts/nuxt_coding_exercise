# Notes 

## 1. Responsiveness

I saw two different approaches to implement responsiveness:
* Mobile First Design
* Desktop First Design

I decided to go for mobile first design, as this is usually best practice, and worked from the smallest width (250px) to desktop-width. 

## 2. Add the {userId} API call

I made the API call on: "pages/user/[id].vue"

## 3. SSR vs. SPA

I compared the two rendering methods and took screenshots of their rendering performance.

I used localhost:3000/user/1 as the request url. 

## SSR

![Server-side Rendering](/public/SSR.jpg)

* Server-side rendering generates the complete HTML content and sends it to the browser, whilst the data fetching is working asynchronously.
* This is why, in the screenshot, the Largest Contentful Paint (LCP), First Paint (FP) and First Contentful Paint (FCP), are rendered first before the DOMContentLoaded Event (DCL) and Onload Event (L).
* It is for these reasons why Server-side Rendering is beneficial for SEO performance, as it means crawl bots can quickly crawl and index the page. This therefore improves its SEO ranking on the search engine results page. 

## SPA/CSR

![Single Page Application/ Client-side Rendering](/public/SPA.jpg)

* Client-side rendering or Single Page Applications work differently however, in that it sends either an empty or minimal HTML page with the JavaScript code (contained within the script tag) to the browser. The browser then fetches the linked JavaScript code. Only once the JavaScript files are downloaded and executed, such as the data fetching, will the content of the page be rendered.
* This is why in this screenshot the DCL loads first, followed by the Onload Event. Contrary to what we see with the SSR screenshot, the HTML elements, such as: LCP, FP and FCP, are the last to be rendered.
* Nevertheless, this is advatageous for different reasons. Considering the JavaScript logic takes priority, it leads to richer user experiences as interactions and updates can change dynamically without the need to reload the entire page (for example, typing in a search bar).
