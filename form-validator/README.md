# 第 14 章： Form Validator

This is pratice from ZTM classes: [javascript-web-projects-to-build-your-portfolio-resume-第十四章](https://www.udemy.com/course/javascript-web-projects-to-build-your-portfolio-resume/?couponCode=ACCAGE0923)

> [click to watch the demo](https://joeban0608.github.io/ZTM-Form-Validator/)

---

resource:

- mdn-css-vaild: https://developer.mozilla.org/en-US/docs/Web/CSS/:valid
- form-validation: https://developer.mozilla.org/en-US/docs/Learn/Forms/Form_validation
  ```jsx
  <form>
    <div>
      <label for="choose">Would you prefer a banana or a cherry?</label>
      <input id="choose" name="i-like" required pattern="[Bb]anana|[Cc]herry" />
    </div>
    <div>
      <label for="choose">Would you prefer a banana or a cherry?</label>
      <input
        type="text"
        id="choose"
        name="i-like"
        required
        minlength="6"
        maxlength="6"
      />
    </div>
    <button>Submit</button>
  </form>
  ```
- Constraint validation: https://developer.mozilla.org/en-US/docs/Web/HTML/Constraint_validation
- rex example: https://html.com/attributes/input-pattern/?username=eeeeeqeqeqeqeqeqe
- rex and css example: https://css-tricks.com/form-validation-part-1-constraint-validation-html/
