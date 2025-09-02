# frontend-questions-1
# Exercise 1 
**Scenario:**  
You’re asked to style a **navigation bar** with this HTML:  
```html
<nav class="navbar">
  <ul>
    <li><a href="/">Home</a></li>
    <li><a href="/blog">Blog</a></li>
    <li><a href="/about">About</a></li>
  </ul>
</nav>
```
**Task:**  
- Write SCSS to:  
  1. Display the links horizontally on desktop, vertically on mobile (< 600px).  
  2. Highlight the current page link.  
- Briefly explain **how you’d organize SCSS for a large project** (e.g., BEM, utility classes, partials).

# Exercise 2 
**Scenario:**  
You’re asked to improve a form for newsletter signup:  
```html
<form>
  <input type="text" placeholder="Your email" />
  <button>Submit</button>
</form>
```  
**Task:**  
- Rewrite this form to:  
  1. Be semantic and accessible.  
  2. Support basic HTML5 validation.  
  3. Be keyboard-friendly.
 
# Exercise 3 
**Scenario:**  
You’re asked to manage the state of a **shopping cart** in a small e-commerce app. Requirements:  
- Add/remove products.  
- Persist cart between page reloads.  
- Allow multiple tabs to stay in sync.  

**Task:**  
- Propose a **state management approach** (e.g., localStorage, custom store, IndexedDB).  
- Implement a minimal TypeScript example of how adding/removing products would work.  

# Exercise 4 

**Scenario:**
You're building an administrative dashboard to display a list of sales leads. The data for these leads needs to be fetched from an API.

**Task:**

1.  Using `fetch` or a similar method, **fetch data** from a public API endpoint.
2.  **Display the data** in a clean, responsive table.
3.  Implement basic client-side **sorting and filtering** of the data.
4.  **Handle and display loading and error states** to the user.

# Exercise 5 

**Scenario:**
You need to display a list of financial transactions that have a `date` and a `total` amount. The application is used globally.
**Task:**

1.  Write a function that takes a transaction date (as a string) and a user's `timezone` string (e.g., `'Europe/Madrid'`) and **formats the date** for display.
2.  Write a second function that takes a total amount and a `currency` code (e.g., `'EUR'`) and **formats it using the correct currency symbol and locale**.
3.  Ensure that you are always seeing the correct timezone and currency independently of where you are loading your data

# Exercise 6 
**Scenario:**
You're working on a feature that allows a user to update their profile information. The update logic is handled by a function called `updateProfile(data)`. This function makes an API call to a backend service.

**Task:**
1. Using a testing framework like **Jest** or **Playwright**, write a **test** for the `updateProfile` function.
2. Show how you would **assert that the function behaves correctly** in both scenarios (e.g., that it returns the expected data on success or throws an error on failure).
3. Briefly explain the difference between a unit test and an end-to-end test and when you would use each.
  

***

# Exercise 7 
**Scenario:**
You need to build a form for a user to create a new invoice. An invoice has three main fields:
* `invoiceNumber`: a string that must be unique.
* `invoiceDate`: a date that cannot be in the future.
* `customerEmail`: a valid email format.


  **Task:**
1. Write a function called `validateInvoice(data)` that takes an object containing these three fields and returns an object of validation errors (e.g., `{ invoiceNumber: 'Invoice number is already taken.', invoiceDate: 'Date cannot be in the future.' }`).
2. Your validation logic for `invoiceNumber` should simulate an **asynchronous check** against a backend service to ensure it's unique.
3. Show how you would **display these errors** to the user in the UI, ensuring the user can correct the input and resubmit the form.

# Exercise 8 
**Scenario:**  
A dashboard renders a `<ul>` with thousands of `<li>` rows. Each `<li>` has a click handler attached individually like this:
```ts
items.forEach(item => {
  const li = document.createElement("li");
  li.innerText = item;
  li.addEventListener("click", () => select(item));
  ul.appendChild(li);
});
```  

Over time, the UI becomes **slow and unresponsive**.

**Task:**
1. Identify the **performance bottleneck**.
2. Refactor the code to make it more efficient, while keeping the same functionality.

# Exercise 9 

**Scenario:**
You are working on an internal tool where different users have different levels of access.
**Task:**

1.  Assume a user object with a `role` property (e.g., `'admin'`, `'editor'`, `'viewer'`).
2.  Write a function that handles the users permissions and accesses to sections of your app
3.  Provide an example of how you would **conditionally render a "Delete" button** in the UI based on this function.

# Exercise 10 
**Scenario:**
A B2B dashboard displays a large, complex table of data. A user reports that they are having trouble finding the data they need, and the UI feels overwhelming.

**Task:**
1. Given this scenario, describe your **process for addressing this user feedback**. What questions would you ask the user or the product manager?
2. Propose **three concrete, UI/UX-focused solutions** to improve the user's experience. Explain the **tradeoffs** of each solution (e.g., development effort, performance impact, user learning curve).
3. If you had to choose just one solution to implement in the next sprint, which would you pick and why?
