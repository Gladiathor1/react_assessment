# React Multi-Step Checkout Form

A multi-step checkout form built with React as a coding assessment. The user moves through **personal details → shipping details → payment details → thank-you**, with validation at each step and the entered data kept in shared state across pages.

## Features

- Four-step flow with React Router
- Form handling with **Formik** and schema validation with **Yup**:
  - required first/last name, valid email
  - street, city, state and ZIP for shipping (US states dropdown)
  - card number (max 16 digits), expiry and CVC (3–4 digits)
- Form data shared between steps through a React Context (`AppContext`)
- Summary on the thank-you page

## Tech stack

- React 18 (Create React App)
- React Router 6
- Formik + Yup

## Project structure

```
src/
  App.js                   Routes for each step
  contexts/app.context.js  Shared form state
  schemas/form.schema.js   Yup validation schemas
  views/                   PersonalDetailsPage, ShippingDetailsPage, PaymentDetailsPage, ThankyouPage
  utils/constants.util.js  US states list
  styles/app.css
```

## Getting started

```bash
npm install
npm start
```

Open [http://localhost:3000](http://localhost:3000).

Other scripts:

```bash
npm test        # run tests
npm run build   # production build
```
