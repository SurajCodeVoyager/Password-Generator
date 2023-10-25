# React + Vite

This template provides a minimal setup to get React working in Vite with HMR and some ESLint rules.

Currently, two official plugins are available:

- [@vitejs/plugin-react](https://github.com/vitejs/vite-plugin-react/blob/main/packages/plugin-react/README.md) uses [Babel](https://babeljs.io/) for Fast Refresh
- [@vitejs/plugin-react-swc](https://github.com/vitejs/vite-plugin-react-swc) uses [SWC](https://swc.rs/) for Fast Refresh

<h1>Hooks in this project</h1>
This Password Generator project makes extensive use of React Hooks. Hooks were introduced in React 16.8 and have become a fundamental part of React development. They allow functional components to have state and side-effects, making it easier to manage and organize your code. Here are some of the key hooks used in this project:

#useState
useState is used to manage and update the component's state. In this project, it is used to manage the length, numberAllowed, charAllowed, and password states. These states control the length of the password, whether numbers and characters are included, and store the generated password.

#useRef
useRef is used to create a reference to the password input element. It allows direct access to the DOM element, which is needed for selecting and copying the generated password to the clipboard.

#useCallback
useCallback is used to memoize the functions passwordGenerator and copyPasswordToClipboard. Memoization ensures that these functions are only recreated when their dependencies (specified in the second argument) change. This can help optimize performance by avoiding unnecessary function recreations.

#useEffect
useEffect is used to introduce side effects into functional components. In this project, it is utilized to trigger the passwordGenerator function when there are changes in the length, numberAllowed, or charAllowed state. This ensures that the password is re-generated when the user interacts with the settings.

Hooks make it possible to write more readable and maintainable code in React by allowing you to manage component state and side effects within functional components, as opposed to using class components and lifecycle methods. This project demonstrates how hooks can be effectively used to create a simple and user-friendly password generator.

<h2> Features </h2>
Generate random passwords with customizable options.
Choose the length of the password using a slider.
Include or exclude numbers and special characters in the generated password.
Easily copy the generated password to the clipboard.
Responsive design for desktop and mobile devices.
