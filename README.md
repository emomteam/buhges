# buhges

tool for build html pages from snippets html on mustache/handlebars version 0.0.1 alfa

## install

    npm install buhges

## use

project/
  │
  ├── layouts/
  │   ├── default.hbs
  │   └── etc.hbs
  │
  ├── pages/
  │   ├── default
  │   │   ├── index.hbs
  │   │   └── inner.hbs
  │   └── etc
  │       └── etc.hbs
  │
  └── snippets/
      ├── header
      │   ├── header.html {{>header}}
      │   ├── nav.json
      │   └── nav.hbs {{>header_nav}}
      ├── content
      │   ├── news.html {{>content_new}}
      │   └── etc.hbs {{>content_etc}}
      └── footer
          └── footer.hbs {{>footer}}

    buhges

project/
  │
  ├── layouts/
  │   ├── default.hbs
  │   └── etc.hbs
  │
  ├── pages/
  │   ├── default
  │   │   ├── index.hbs
  │   │   └── inner.hbs
  │   └── etc
  │       └── etc.hbs
  │
  ├── snippets/
  │   ├── header
  │   │   ├── header.html
  │   │   ├── nav.json
  │   │   ├── nav.hbs
  │   │   └── nav.html (from nav.hbs + nav.json)
  │   ├── content
  │   │   ├── news.html
  │   │   ├── etc.hbs
  │   │   └── etc.html (from etc.hbs)
  │   └── footer
  │       ├── footer.hbs
  │       └── footer.html (from footer.hbs)
  │
  ├── index.html (layouts/default.hbs + pages/default/index.hbs)
  ├── inner.html (layouts/default.hbs + pages/default/inner.hbs)
  └── etc.html (layouts/etc.hbs + pages/etc/etc.hbs)