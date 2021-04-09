# duyb-gulp-project

> auto build by [duyb-cli-gulp](https://github.com/thxl2010/duyb-cli-gulp)

## Installation

```shell
$ yarn add duyb-cli-gulp

# or npm
$ npm install duyb-cli-gulp
```

## Usage

- create pages.config.js file in root

```js
module.exports = {
  // demo: data object for swig ...
  data: {
    menus: [
      {
        name: 'Home',
        icon: 'aperture',
        link: 'index.html',
      },
      {
        name: 'Features',
        link: 'features.html',
      },
      {
        name: 'About',
        link: 'about.html',
      },
      {
        name: 'Contact',
        link: '#',
        children: [
          {
            name: 'Twitter',
            link: 'https://twitter.com/thxl2010',
          },
          {
            name: 'About',
            link: 'https://weibo.com/thxl2010',
          },
          {
            name: 'divider',
          },
          {
            name: 'About',
            link: 'https://github.com/thxl2010',
          },
        ],
      },
    ],
    pkg: require('./package.json'),
    date: new Date(),
    // ...
  },
};
```

- gulp task in NPM Scripts

  ```json
  {
    "scripts": {
      "clean": "duyb-cli-gulp clean",
      "dev": "duyb-cli-gulp dev",
      "build": "duyb-cli-gulp build"
    }
  }
  ```
