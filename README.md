# React Contact Form Component

A customizable contact form component built with React with built-in error handling.

![App Screenshot](./screenshot.png)

[Live Demo](https://matt-miguel.github.io/react-contact-form-component/) · [View Code](https://github.com/matt-miguel/react-contact-form-component)

---

## Overview

A contact form with multiple inputs, including name, email, radio selectors, and textarea. Errors are shown on blur and cleared on input to provide instant feedback without being intrusive and disrupting the user's flow. Success submissions display success toast notification.

---

## Features

- Success toast notification upon successful submission
- Each field is validated as the user moves throughout the form
- Errors are cleared as soon as the user starts typing
- Built-in accessibility with aria-live, aria-invalid, aria-describedby
- Responsive design (mobile first)

---

## Technical Highlights

**Custom Form Group Component**

This form uses a custom Form Group component. Rather than manually adding error spans next to each input, the FormGroup component accepts any input or textarea as children and handles displaying errors automatically via props.

**Error Handling with Constraint Validation API**

This form uses the native Constraint Validation API. By taking advantage of the native validation in browsers, input errors can be checked easily in one line of code and stored in a state variable to dynamically provide error messages in real time to the user as they fill out the form.

---

## Tech Stack

- React 19 + Vite
- CSS (Grid, Flexbox, custom properties, mobile-first)
- Constraint Validation API — used for native input error handling

---

## Getting Started

```bash
git clone https://github.com/matt-miguel/react-contact-form-component
cd react-contact-form-component
npm install
npm run dev
```

---

## Challenges & What I Learned

**Setting up the Form Group**

My initial idea for the form group was to put the inputs inside the FormGroup component and just pass the input type as a prop. But I quickly realized that I would then not be able to use textarea or multiple inputs in one form group. This taught me to design components around flexibility. By wrapping the children instead of owning it, the component became more composable and reusable.

---

## What I'd Improve

**Error handling in the Form Group Component**

I would move the error handling into the FormGroup component so that all of the validation and error display is kept in one place. This would make the component more maintainable and self-contained.
