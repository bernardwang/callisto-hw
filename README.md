**[callisto-hw](https://bernard.wang/callisto-hw)**
==============

## Development Notes

### JS
This website is written in Vue.js using the Webpack/vue-loader [boilerplate](https://vuejs-templates.github.io/webpack/). I chose this boilerplate because it comes with many features built in, such as SCSS, Autoprefixer for browser cross-compatibility, Babel for ES2015+, and ESLint. I also chose Vue.js because it is very similar to React while being slightly lighter and faster to prototype with. The only other package I used was the [smoothscroll](https://github.com/iamdustan/smoothscroll) polyfill for scrolling behavior.

Because this assignment is a static page, this setup might be unnecessarily feature rich. However, I decided this project structure demonstrates how a page like this could scale into a fully featured website.

### CSS
For styling I used a combination of global theme styles and component scoped styles using SCSS as my preprocessor. The theme settings were organized into a common variables (i.e. colors, breakpoints), typography, util classes, and global resets. With a larger project I would have prefered to simplify the scoped styling by making more components (for example a typography component), or by using a standard set of util classes.

## Usage
After running `npm install`, the following scripts are provided by the Vue Webpack [template](https://vuejs-templates.github.io/webpack/)

``` bash
# install dependencies
npm install

# serve with hot reload at localhost:8080
npm run dev

# build for production with minification
npm run build

# build for production and view the bundle analyzer report
npm run build --report

# run unit tests
npm run unit

# run all tests
npm test
```
I also added a command `npm run deploy` to deploy to github pages, but current it is not working because the build files are meant to be served through a server rather than static files. The files on master are modified as a quick fix for this, but running locally will work fine.

For a detailed explanation on how things work, check out the [guide](http://vuejs-templates.github.io/webpack/) and [docs for vue-loader](http://vuejs.github.io/vue-loader).

### Folder Structure
```
.
├── ...
├── src                     # Relevant code
│   ├── assets              # Static images & other assets
│   ├── components          # Vue components
│   │   ├── core            # Reuseable components
│   │   └── ...             # Page specific components
│   ├── router              # Frontend routes (using vue-router)
│   ├── styles              # SCSS theme styles
│   ├── App.vue             # Top level Vue component
│   └── main.js             # JS entry file
└── ...
```

## Testing
- Tested on Chrome, Safari & Firefox with autoprefixer set to compatability with `last 2 versions`.
- Used semantic HTML and ARIA attributes for accessibility. Google Lighthouse and [tota11y](https://khan.github.io/tota11y/) for a11y smoke testing.
- No unit tests

## Risks
- Mobile navigation menu could be improved and needs further testing especially with accessibility
- Page assets (images & web fonts) could be optimized to reduce load time
