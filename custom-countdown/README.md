# 第 11 章： Custom Countdown

This is pratice from ZTM classes: [javascript-web-projects-to-build-your-portfolio-resume-第十一章](https://www.udemy.com/course/javascript-web-projects-to-build-your-portfolio-resume/?couponCode=ACCAGE0923)

> [click to watch the demo](https://joeban0608.github.io/ZTM-Custom-Countdown/)

---
resource：
- video background https://pixabay.com/videos/
- video 壓縮與轉換 https://www.youcompress.com/
- form 可讀性 https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/form_role
    - label
    - 表單標籤: input, select, textarea…
- input type=”date”: https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input/date
    
    ```jsx
    <label for="start">Start date:</label>
    <input 
    	type="date" 
    	id="start" 
    	name="trip-start" 
    	value="2018-07-22" 
    	min="2018-01-01" 
    	max="2018-12-31" 
    />
    ```
    
- today
    - new Date: https://www.w3schools.com/jsref/jsref_obj_date.asp
    - toISOString: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date/toISOString
    - string.split: https://www.w3schools.com/jsref/jsref_split.asp
    
    ```jsx
    const today = new Date().toISOString().split("T")[0] // "2024-05-08"
    
    ```
    
- submit event: https://developer.mozilla.org/en-US/docs/Web/API/HTMLFormElement/submit_event
- preventdefault: https://www.w3schools.com/jsref/event_preventdefault.asp
    
    For example, this can be useful when:
    
    - Clicking on a "Submit" button, prevent it from submitting a form
    - Clicking on a link, prevent the link from following the URL
    
    ```jsx
    document.getElementById("myAnchor").addEventListener("submit", function(event){
      event.preventDefault()
    });
    // 可以取消 submit 時，refresh 畫面的功能。
    ```
    
- setInterval: https://www.w3schools.com/js/js_timing.asp

- localstorage + JSON.stringfy + JSON.parse
    
    ```jsx
    savedCountdown = {
      title: countdownTitle,
      date: countdownDate,
    };
      
    // set localStorage
    localStorage.setItem('countdown', JSON.stringify(savedCountdown));
      
    // get localStorage
    if (localStorage.getItem('countdown')) {
      inputContainer.hidden = true; 
      savedCountdown = JSON.parse(localStorage.getItem('countdown'));
      countdownTitle = savedCountdown.title;
      countdownDate = savedCountdown.date;
      countdownValue = new Date(countdownDate).getTime();
      updateDOM();
    }
     
    // remove localStorage
    function reset() {
      // Hide countdowns, show input form
      countdownEl.hidden = true;
      completeEl.hidden = true;
      inputContainer.hidden = false;
      // Stop the countdown
      clearInterval(countdownActive);
      // Reset values, remove localStorage item
      countdownTitle = '';
      countdownDate = '';
      localStorage.removeItem('countdown');
    }
    
    ```