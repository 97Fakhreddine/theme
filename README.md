# Theme folder structure for gloab SCSS styles

[//]: # (![Project Logo]&#40;project-logo.png&#41;)

## Table of Contents

- [Overview](#overview)
- [Getting Started](#getting-started)
- [Usage](#usage)
- [Folder Structure](#folder-structure)
- [Contributing](#contributing)
- [License](#license)

## Overview

The project was design for using scss structure in multiple project. so whenever you want to start a new project
you will be able to include the ``styles`` folder into your project knowing that it will fit and you start using
it to style your component. the main reason for this is when you want to add multi theme that will be easy for you.

## Getting Started

- make sure the project that you are working on supports SCSS, otherwise add scss config for webpack.
- clone the project into your local machine
- copy paste the folder styles that already include all the styling that you need
- start using the varibles that are already included in the ``_variable.scss``

## Usage
Clone the repository
```bash
git clone https://github.com/97Fakhreddine/theme 
```

Change to the project directory
```bash
cd theme
```

## Folder Structure
```bash
styles/
|-- _variables.scss
|-- theme/
|   |-- mixins/
|   |   |-- _spacing.scss
|   |   |-- _text.scss
|   |   |-- _responsive.scss
|   |-- elements/
|   |   |-- _buttons.scss
|   |   |-- _forms.scss
|   |   |-- _navbar.scss
|   |   |-- _footer.scss
|-- main.scss
```
In this structure:
* _variables.scss is at the root and contains global variables that apply to the entire project.
* Inside the theme/ directory, you have:
* mixins/ for SCSS files containing mixins for common styling tasks.
* elements/ for SCSS files that define styles for specific UI elements such as buttons, forms, navbar, and footer.
This organization separates your variables from mixins and elements, making it easier to manage and maintain your SCSS codebase. You can import these files into your main.scss as needed to build your stylesheets efficiently.

Full article on how to use this can be found in [here](https://javascript.plainenglish.io/scss-an-in-depth-guide-with-a-comprehensive-theme-folder-structure-f371db6d84b7).

## Angular example on how you can use multi colors in your app

```javascript
import { Component } from '@angular/core';

@Component({
  selector: 'app-root',
  templateUrl: './app.component.html',
  styleUrls: ['./app.component.scss'],
})
export class AppComponent {
  /**
   * Change the global theme colors based on the selected theme name.
   *
   * @param themeName - The name of the theme ('default' or 'dark').
   */
  changeTheme(themeName: string) {
    switch (themeName) {
      case 'default':
        document.documentElement.style.setProperty('--primary-color', '#007bff');
        document.documentElement.style.setProperty('--background-color', '#ffffff');
        // Add other variables and their values for the default theme
        break;
      case 'dark':
        document.documentElement.style.setProperty('--primary-color', '#ff5722');
        document.documentElement.style.setProperty('--background-color', '#333333');
        // Add other variables and their values for the dark theme
        break;
      default:
        // Handle unsupported themes or provide a fallback
        break;
    }
  }
}
```


```bash
💬 Let's Connect! 💬
I'm open to networking opportunities, collaboration,
and sharing knowledge within the tech community. 
Feel free to reach out to me if you're interested in discussing 
exciting projects, industry trends, or if you need any assistance 
with JavaScript development.

📧 Email: fakhry.messaoudi@gmail.com
🌐 Portfolio: https://fakhreddine-messaoudi.netlify.app
🔗 LinkedIn: https://www.linkedin.com/in/97fakhreddine
🔗 Github: https://github.com/97Fakhreddine
```
## Contributing
please feel free to raise a pull request to make this project bigger !

Contributions are welcome! To contribute to this project, follow these steps:

* Fork the repository.
* Create a new branch for your feature or bug fix: git checkout -b feature/your-feature-name
* Make your changes and commit them: git commit -m 'Add a new feature'
* Push to the branch: git push origin feature/your-feature-name
* Create a pull request.

## License
This project is licensed under the MIT License.

### Happy coding