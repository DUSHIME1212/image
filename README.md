# Screens 📱

This directory contains the screen widgets for the application.
Each screen should be in its own file and should be a `StatelessWidget` or `StatefulWidget`.

## SplashScreen ✨

The `SplashScreen` widget provides an engaging entry point to the application 🚀. It is displayed briefly while the app initializes, often showcasing the app's logo or a captivating animation. This screen is built using Flutter, ensuring a smooth and visually appealing experience for the user.

### Visual Components 🎨

The SplashScreen is composed of several visual elements:

*   **Background Image 🖼️:** The background features a network image sourced from `https://images.pexels.com/photos/931162/pexels-photo-931162.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=1`. It's displayed using `BoxFit.cover`, ensuring it fills the entire screen.
*   **Gradient Overlay:** A linear gradient overlays the background image, transitioning from `Colors.black` (80% opacity) at the top to `Colors.black` (20% opacity) at the bottom.
*   **Centered Content 🌟:** The following elements are centered on the screen:
    *   **Logo/Image:** An image asset (`assets/logo.png`) is displayed with a height of 120 pixels.
    *   **Welcome Text:** The text "Welcome to Our App" is displayed with a font size of 24.0, bold font weight (`FontWeight.bold`), and white color.
    *   **GET STARTED Button:** An `ElevatedButton` with the text "GET STARTED".
        *   **Appearance:** It has a white background color, horizontal padding of 50.0 and vertical padding of 10.0, and a `RoundedRectangleBorder` with a border radius of 10.0.
        *   **Action:** The `onPressed` callback is currently empty, meaning it doesn't perform any action when tapped.

### Code Structure 💻

The `SplashScreen` is implemented as a `StatelessWidget`, which is ideal as its content remains static after being built.

A `Stack` widget is utilized to layer the UI elements effectively:
*   The background image is at the bottom of the stack.
*   The gradient overlay is placed on top of the image.
*   The centered content (logo, text, and button) is positioned above the gradient.

To ensure that the content is not obscured by system UI elements like the status bar or notches, the main content within the `Scaffold` is wrapped in a `SafeArea` widget.
