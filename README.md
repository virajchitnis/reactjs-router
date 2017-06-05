# ReactJS Router

Router for ReactJS

## Installation

Via npm

```
npm install reactjs-router
```

Via yarn

```
yarn add reactjs-router
```

## Usage

I recommend using webpack for your project. I have tested this module with webpack.

*I have not tested it with browserify or plain browser `<script></script>` tags. If you are successfully use it with either, please let me know so I can update this page.*

### The router

Import in ES6

```
import {RouterRoute} from 'reactjs-router';
```

In your react app, each page should be encompassed by the `RouterRoute` component. The properties accepted by the component are:

- `url` - The relative URL for the page
- `title` - The title of the page

Here is an example defining two pages with their respective titles and URLs:

```
<RouterRoute url="/" title="Viraj Chitnis">
  <HomePage />
</RouterRoute>
<RouterRoute url="/resume" title="Resumé - Viraj Chitnis">
  <ResumePage />
</RouterRoute>
```

### The link

Import in ES6

```
import {RouterLink} from 'reactjs-router';
```

Replace your links with a `RouterLink` component. The properties supported by it are:

- `className` - CSS class name
- `title` - Title of the destination
- `href` - Relative URL of the destination
- `resetScrollPos` - Whether or not you would like the scroll position to be reset.

Here is an example where the destination page requires its scroll position to be reset:

```
<RouterLink className="nav-standard" title="Resumé - Viraj Chitnis" href="/resume" resetScrollPos>resumé</RouterLink>
```

Here is an example where the destination page does not require its scroll position to be reset:

```
<RouterLink className="nav-home" title="Viraj Chitnis" href="/">VC</RouterLink>
```

Below is the standard HTML ouput of the above component to give you an idea on how the above code is to be used:

```
<a href="/" class="nav-home">VC</a>
```

## Demo

My website [virajchitnis.com](https://www.virajchitnis.com) uses this module. The example code above is from my website.

## Contribution

Fork this repo and send me a pull request.

## Issues

Please create an issue in the issues section of this repository.
