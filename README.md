# Jest Coverage Theme

Are those coverage reports too bright? Not enough contrast? Not colourful enough? Well, this package is for you!

This package allows you to change the colours of your Jest coverage reports to make them more readable and visually appealing.
By default, it will use a dark theme. However, you can provide whatever CSS you want to customise the look of your coverage reports.

_If you find this package useful, please consider donating to help support its development._

[![Donate](https://img.shields.io/badge/Donate-GitHub-GITHUB?style=for-the-badge&logo=github&labelColor=%23211c30&color=%239100ff)](https://github.com/sponsors/chadcromwell)

_Thanks!_

## Installation

1. Install the package

```bash
    npm i jest-coverage-theme
```

## Usage

### Default Dark Theme

_To style the coverage report with the default dark theme_

1. When running jest tests with `--coverage`, add `; npx jest-coverage-theme` to the end of your command.

For example:

```bash
    npx jest --coverage; npx jest-coverage-theme,
```

_**Note**: by including the `;` before calling `npx jest-coverage-theme`, you ensure the style is applied to the coverage report even if your tests fail. If you wish to not apply the style to coverage upon test failure, replace `;` with `&&`._

### Custom Theme

_To style the coverage report with a custom theme_

1. Copy the default theme from `node_modules/jest-coverage-theme/dark-theme.css` and paste it into a new file in your project.
2. Modify the CSS to your liking.
3. When running jest tests with `--coverage`, add `; npx jest-coverage-theme --css-path=<path-to-your-css-file-relative-to-project-root>` to the end of your command.

For example:

You've created `custom-theme.css` in the following directory: `<project root>/themes/custom-theme.css`

```bash
    npx jest --coverage; npx jest-coverage-theme --css-path=themes/custom-theme.css
```

_**Note**: by including the `;` before calling `npx jest-coverage-theme`, you ensure the style is applied to the coverage report even if your tests fail. If you wish to not apply the style to coverage upon test failure, replace `;` with `&&`._
