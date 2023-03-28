# es6-bootstrap-dialogs
This repository provides custom ES6 implementations of the alert and confirm functions using Bootstrap 5 modals, allowing for enhanced customization and styling.


# Bootstrap ES6 Custom Methods

This repository provides custom ES6 implementations of the alert and confirm functions using Bootstrap 5 modals, allowing for enhanced customization and styling.

## Quick Start

1. Make sure you have included the necessary Bootstrap CSS and JavaScript files in your HTML file:

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <!-- Add Bootstrap CSS -->
  <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0-alpha1/dist/css/bootstrap.min.css" rel="stylesheet">
</head>
<body>
  <!-- Your content here -->

  <!-- Add Bootstrap JavaScript -->
  <script src="https://cdn.jsdelivr.net/npm/@popperjs/core@2.11.6/dist/umd/popper.min.js"></script>
  <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0-alpha1/dist/js/bootstrap.min.js"></script>
</body>
</html>
```

2. Import or include the `customAlert()` and `customConfirm()` functions from this repository in your JavaScript code.

3. Use the custom functions in your code as shown in the examples below:


// Custom alert example
(async () => {
  await customAlert("This is a custom alert message!");
  console.log("This will be logged after the custom alert is closed.");
})();

// Custom confirm example
(async () => {
  const result = await customConfirm("Are you sure?");
  if (result) {
    console.log("User clicked OK.");
  } else {
    console.log("User clicked Cancel or closed the modal.");
  }
})();


## Benefits of Destroying the Modal Element

The custom implementations of `alert()` and `confirm()` provided in this repository automatically destroy the HTML modal element after the Promise resolves and the code finishes executing. This approach ensures that the DOM remains clean and lightweight, improving the overall performance of your web application. The modal elements are removed from the DOM, freeing up memory and preventing potential conflicts with other parts of your application.

For example, if you had multiple custom alerts or confirm dialogs in your application, destroying the modal element after it is no longer needed prevents unnecessary clutter and potential issues with overlapping or duplicate modals.
