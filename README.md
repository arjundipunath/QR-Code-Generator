## 📱 QR Code Generator

A simple, fast, and user-friendly web application for generating QR codes from any text or URL. This project utilizes vanilla JavaScript to interact with an external QR code generation API.

### ✨ Features

  * **Instant QR Code Generation:** Quickly generates a QR code image based on the input text or URL.
  * **API Integration:** Uses the **[QR Server API](https://goqr.me/api/)** (`https://api.qrserver.com/v1/create-qr-code/`) to handle image creation.
  * **Input Validation:** Checks if the input field is empty and displays a message if it is.
  * **Responsive Design:** Styled to be centered and easy to use on various screen sizes (though primarily fixed-width at 400px).
  * **Smooth Animation:** Uses CSS transitions (`max-height 1s`) to reveal the QR code box smoothly.
  * **Modern Styling:** Features a clean interface with a dark blue background and a prominent blue generation button.

-----

### 🛠️ Technology Stack

| Technology | Purpose |
| :--- | :--- |
| **HTML5** | Defines the structure, including the input field (`#qrtext`), the image container (`#imgbox`), and the "Generate" button. |
| **CSS3** | Styles the container, centers the element, applies background colors, and manages the smooth transition for the image display. |
| **Vanilla JavaScript** | Handles user input, constructs the API URL, dynamically sets the `src` of the image, and manages input validation/error messages. |

-----

### 🚀 Getting Started

To run this application, you only need a web browser and an internet connection (to access the QR code API).

#### Prerequisites

  * A modern web browser (Chrome, Firefox, Edge, Safari, etc.)
  * An active internet connection.

#### Installation and Execution

1.  **Clone the Repository:**
    ```bash
    git clone https://github.com/arjundipunath/QR-Code-Generator.git
    ```
2.  **Navigate to the Project Directory:**
    ```bash
    cd QR-Code-Generator
    ```
3.  **Open the File:**
    Double-click the **`index.html`** file, or right-click it and select "Open with" your preferred web browser.

The generator interface will load, ready for your input.

-----

### 💻 Code Logic

The core functionality resides in the **`index.html`** file:

1.  **`generate()` Function:**

    ```javascript
    qrimage.src = "https://api.qrserver.com/v1/create-qr-code/?size=150x150&data=" + qrtext.value;
    imgbox.classList.add("show-img");
    ```

    This function dynamically constructs the API endpoint URL by appending the value entered by the user to the base API URL, and then assigns this URL to the `src` attribute of the image element (`#qrimage`).

2.  **`checkInput()` Function:**
    This function is called immediately after `generate()` and handles validation:

      * It checks if the input is empty (`input.trim() === ""`).
      * If empty, it displays the message "Input box cannot be empty\!" and hides the image box.
      * If valid, it clears the message and shows the image box.

-----

### ⚙️ API Reference

This project uses the following public API:

  * **Endpoint:** `https://api.qrserver.com/v1/create-qr-code/`
  * **Parameters Used:**
      * `size=150x150`: Defines the dimensions of the generated QR code image.
      * `data=...`: Contains the text or URL provided by the user.

-----

### ✍️ Author

  * **Arjun Dipunath** - (@arjundipunath)

-----

