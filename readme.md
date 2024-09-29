# SpotFinder

SpotFinder is a React application that allows users to create a personalized collection of places they wish to visit or have already explored. The app sorts available places by proximity to the user's current location and enables users to manage their collection of selected places.

![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![Vite](https://img.shields.io/badge/Vite-646CFF?style=for-the-badge&logo=vite&logoColor=white)
![React](https://img.shields.io/badge/React-61DAFB?style=for-the-badge&logo=react&logoColor=black)

<!-- PROJECT LOGO -->
<br />
<div align="center">
 <a href="https://spotfinder-ester.netlify.app//">
    <img src="src/assets/logo.png" alt="Logo" height="80">
  </a>
  <h1 align="center">SpotFinder</h1>

  <p align="center">
    <a href="https://spotfinder-ester.netlify.app//">View Demo</a>
  </p>
</div>

## Features

- **Geolocation-based sorting**: The app sorts available places based on the user's current location.
- **Place selection**: Users can add places to their collection and remove them.
- **Modal for confirmation**: When removing a place, the app asks for confirmation through a modal dialog.
- **LocalStorage**: The app saves the user's selected places in the browser's `localStorage`, so their collection persists across sessions.

## React Hooks Used

- **`useState`**: Manages state for selected places, available places, and modal visibility. The hook is used to update state when places are added or removed, and to toggle the modal for place deletion confirmation.
- **`useRef`**: Stores a reference to the selected place and the modal element. This allows direct manipulation, such as showing or closing the modal when triggered.

- **`useEffect`**: Handles side effects like fetching the user's current location through the `navigator.geolocation` API, and sorting the available places based on distance. It also sets up timers for auto-confirmation in the delete modal.

- **`useCallback`**: Optimizes performance by memoizing the `handleRemovePlace` function, ensuring it only gets recreated when dependencies change.

## Installation and Setup Instructions

1. **Clone the repository:**

   ```bash
   git clone https://github.com/EsterMn3/SpotFinder.git
   cd spotfinder
   ```

2. **Install dependencies:**
   npm install

3. **Run the app:**
   npm start

## Usage

- When the page loads, the app will ask for permission to access your location.
- The available places will be sorted based on their proximity to your current location.
- You can select places to add them to your collection under "I'd like to visit...".
- To remove a place from your collection, click on it, and a modal will prompt you to confirm.
- Your selected places will be saved in localStorage, so they will persist even after refreshing the page.

## Dependencies

- React (18.x)
- Geolocation API (built-in)
- LocalStorage API (built-in)

## License

This project is open-source and available under the MIT License.
