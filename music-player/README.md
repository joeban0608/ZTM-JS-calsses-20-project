# 第 10 章： Music Player
This is pratice from ZTM classes: [javascript-web-projects-to-build-your-portfolio-resume-第十章](https://www.udemy.com/course/javascript-web-projects-to-build-your-portfolio-resume/?couponCode=ACCAGE0923)
> [click to watch the demo](https://joeban0608.github.io/ZTM-Music-Player/)
---
resoure:
  - mdn img object-fit: https://developer.mozilla.org/en-US/docs/Web/CSS/object-fit
  - w3s HTML Audio/Video DOM Reference: https://www.w3schools.com/tags/ref_av_dom.asp
  - w3s object this: https://www.w3schools.com/js/js_this.asp
      - **this** in Event Handlers
          
          In HTML event handlers, `this` refers to the HTML element that received the event:
          
          ```jsx
          <button onclick="this.style.display='none'">
            Click to Remove Me!
          </button>
          ```
      - what is this  
          <img width="829" alt="w3s-this" src="https://github.com/joeban0608/ZTM-Music-Player/assets/80736596/776e7252-a7fe-417c-8be1-56261e60e9a6">
          
  - textContent: https://developer.mozilla.org/en-US/docs/Web/API/Node/textContent
      
      ### [Differences from innerText](https://developer.mozilla.org/en-US/docs/Web/API/Node/textContent#differences_from_innertext)
      
      Don't get confused by the differences between `Node.textContent` and `[HTMLElement.innerText](https://developer.mozilla.org/en-US/docs/Web/API/HTMLElement/innerText)`. Although the names seem similar, there are important differences:
      
      - `textContent` gets the content of *all* elements, including `[<script>](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/script)` and `[<style>](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/style)` elements. In contrast, `innerText` only shows "human-readable" elements.
      - `textContent` returns every element in the node. In contrast, `innerText` is aware of styling and won't return the text of "hidden" elements.
          - Moreover, since `innerText` takes CSS styles into account, reading the value of `innerText` triggers a [reflow](https://developer.mozilla.org/en-US/docs/Glossary/Reflow) to ensure up-to-date computed styles. (Reflows can be computationally expensive, and thus should be avoided when possible.)
          - `innerText` 因為 css styles 的緣故需要每次 reflow，耗費的資源較大
          - `textContent` 如果 text 一樣，不會重新渲染
