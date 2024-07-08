# 第 18 章： drag-and-drop
This is pratice from ZTM classes: [javascript-web-projects-to-build-your-portfolio-resume-第十八章](https://www.udemy.com/course/javascript-web-projects-to-build-your-portfolio-resume/?couponCode=ACCAGE0923)

> [click to watch the demo](https://joeban0608.github.io/ZTM-drag-and-drop/)
---
resource:

- custom scroll bar: https://css-tricks.com/the-current-state-of-styling-scrollbars-in-css/
- HTML Drag and Drop API: https://www.w3schools.com/html/html5_draganddrop.asp
- HTML ondragenter Attribute: https://www.w3schools.com/tags/att_ondragenter.asp
- contenteditable (讓非 input element 也可以打字): https://developer.mozilla.org/en-US/docs/Web/HTML/Global_attributes/contenteditable
- Arrray.from()，將希望是陣列，但不是陣列的資料轉換成陣列。
    
    ```jsx
    
      
      console.log("backlogListEl.children", backlogListEl.children);
    	// prototype: HTMLCollection
      
      console.log(
        "Array.from(backlogListEl.children)",
        Array.from(backlogListEl.children)
      ); 
    	// prototype: Array(0)
    
    ```
