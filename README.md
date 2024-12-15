# Implementation Guidelines

## **Overview**
This document provides guidelines for using the components in the design system. It includes details about the button, card, and input field components, along with their API/props, styling considerations, and usage examples.

---

## **Components**

### **Button Component**

Reusable button with support for variants and sizes.

#### **Variants**:
- **Primary**: The main button for primary actions.
- **Secondary**: Used for secondary or less important actions.
- **Disabled**: A non-interactive button indicating unavailability.

#### **Sizes**:
- **Small**: Compact button for tight spaces.
- **Medium**: Default size for general use.
- **Large**: Prominent button for major actions.

#### **API/Props**
| **Prop/Class**       | **Description**                                      | **Values**                       | **Default**    |
|-----------------------|------------------------------------------------------|-----------------------------------|----------------|
| `.btn`               | Base class for all buttons.                          | —                                 | Required       |
| `.btn-primary`       | Styles the button as a primary button.               | —                                 | —              |
| `.btn-secondary`     | Styles the button as a secondary button.             | —                                 | —              |
| `.btn-disabled`      | Disables the button and applies the disabled style.  | —                                 | —              |
| `.btn-small`         | Applies small size to the button.                    | —                                 | `.btn-medium`  |
| `.btn-medium`        | Applies medium size to the button (default size).    | —                                 | Default        |
| `.btn-large`         | Applies large size to the button.                    | —                                 | —              |
| `disabled` attribute | Native HTML attribute to disable the button.         | `disabled`                        | —              |

#### **Usage Example**
```html
<!-- Primary button, medium size (default) -->
<button class="btn btn-primary">Primary</button>

<!-- Secondary button, small size -->
<button class="btn btn-secondary btn-small">Secondary</button>

<!-- Disabled button -->
<button class="btn btn-primary btn-large btn-disabled" disabled>Disabled</button>
```

---

### **Card Component**

Reusable card for displaying content with optional image, title, subtitle, and body text.

#### **API/Props**
| **Prop/Class**     | **Description**                              | **Values**          | **Default**    |
|---------------------|----------------------------------------------|---------------------|----------------|
| `.card`            | Base class for the card.                     | —                   | Required       |
| `.card-img`        | Styles the image within the card.            | —                   | Optional       |
| `.card-title`      | Styles the card title.                       | —                   | Optional       |
| `.card-subtitle`   | Styles the card subtitle.                    | —                   | Optional       |
| `.card-body`       | Styles the card body text.                   | —                   | Optional       |

#### **Usage Example**
```html
<!-- Card with an image -->
<div class="card">
  <img src="example.jpg" alt="Example Image" class="card-img" />
  <div class="card-content">
    <h3 class="card-title">Card Title</h3>
    <p class="card-subtitle">Card Subtitle</p>
    <p class="card-body">This is the body text.</p>
  </div>
</div>

<!-- Card without an image -->
<div class="card">
  <div class="card-content">
    <h3 class="card-title">Card Title</h3>
    <p class="card-subtitle">Card Subtitle</p>
  </div>
</div>
```

---

### **Input Field Component**

Reusable input field with label, error message, and states (default, focused, error).

#### **API/Props**
| **Prop/Class**       | **Description**                                      | **Values**            | **Default**    |
|-----------------------|------------------------------------------------------|-----------------------|----------------|
| `.input-field`       | Wrapper for the label and input field.               | —                     | Required       |
| `.input-default`     | Base style for the input field.                      | —                     | Required       |
| `.input-error`       | Styles the error message.                            | —                     | Optional       |
| `disabled` attribute | Native HTML attribute to disable the input field.    | `disabled`            | —              |
| `required` attribute | Native HTML attribute to mark the input as required. | `required`            | —              |

#### **Usage Example**
```html
<!-- Default input field -->
<div class="input-field">
  <label for="name">Name:</label>
  <input type="text" id="name" class="input-default" />
</div>

<!-- Input field with error -->
<div class="input-field">
  <label for="email">Email:</label>
  <input type="email" id="email" class="input-default" />
  <p class="input-error">Please enter a valid email address.</p>
</div>

<!-- Disabled input field -->
<div class="input-field">
  <label for="username">Username:</label>
  <input type="text" id="username" class="input-default" disabled />
</div>
```

---

## **Styling Considerations**
1. **Scalability**:
   - Use class-based styling for easy reusability and extension.
   - Keep the structure simple for integration across multiple projects.

2. **Responsiveness**:
   - Ensure components adapt to various screen sizes using relative units (e.g., `em`, `%`) and media queries.

3. **Consistency**:
   - Maintain a consistent design language by reusing spacing, typography, and color schemes.

4. **Accessibility**:
   - Ensure all interactive elements have proper focus states.
   - Use semantic HTML and WAI-ARIA attributes where needed.

---

## **Examples of Usage**
To view the components in action, include them in an HTML file and link the associated CSS file.

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Component Demo</title>
  <link rel="stylesheet" href="styles.css">
</head>
<body>
  <!-- Button Component -->
  <button class="btn btn-primary">Click Me</button>

  <!-- Card Component -->
  <div class="card">
    <h3 class="card-title">Hello Card</h3>
    <p class="card-body">This is a reusable card component.</p>
  </div>

  <!-- Input Component -->
  <div class="input-field">
    <label for="demo">Enter Text:</label>
    <input type="text" id="demo" class="input-default" />
  </div>
</body>
</html>
```

