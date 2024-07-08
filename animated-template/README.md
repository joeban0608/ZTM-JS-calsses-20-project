# 第 8 章： Navigation Nation
This is pratice from ZTM classes: [javascript-web-projects-to-build-your-portfolio-resume-第八章](https://www.udemy.com/course/javascript-web-projects-to-build-your-portfolio-resume/?couponCode=ACCAGE0923)
> [click to watch the demo](https://joeban0608.github.io/ZTM-Animated-Template/)
---
resource:
- Creative Tim Template: https://www.creative-tim.com/learning-lab/tailwind-starter-kit/presentation
- for class animate template:
    [--animate-template](https://prod-files-secure.s3.us-west-2.amazonaws.com/92560234-a90a-4344-8092-7edf736a18ec/276a0380-0d5f-4c90-9157-12d8dfd0d88a/Untitled.zip)    
- animate lib AOS: https://michalsnik.github.io/aos/
- async & defer: https://web.dev/articles/optimizing-content-efficiency-loading-third-party-javascript?hl=zh-tw
    - 使用`async`或`defer`
        - JavaScript 執行會阻礙剖析器。瀏覽器遇到指令碼時，必須暫停 DOM 建構作業、將指令碼傳送至 JavaScript 引擎，並允許指令碼執行後，才能繼續建構 DOM。
        - `async` 和 `defer` 屬性會變更此行為，如下所示：
        - `async` 會讓瀏覽器繼續以非同步方式下載指令碼，同時會繼續剖析 HTML 文件。指令碼下載完成後，剖析會在指令碼執行期間遭到封鎖。(google analytics)
        - `defer` 會讓瀏覽器繼續剖析 HTML 文件，以非同步方式下載指令碼，然後等到文件剖析完成後再執行指令碼。  
        除非重要轉譯路徑需要使用指令碼，否則一律針對第三方指令碼使用 `async` 或 `defer`。如果指令碼必須在載入程序較早執行時 (例如某些分析指令碼) 執行，請使用 `async`。  若是較不重要的資源，例如網頁轉譯時比使用者一開始看到的還低，請使用 `defer`。  
        如果您的主要考量在於效能，我們建議等到網頁的重要內容載入完成後，再新增非同步指令碼。我們不建議將 `async` 用於必要的程式庫，例如 jQuery。  