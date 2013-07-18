# [buhges v0.0.2](https://github.com/Emomteam/buhges)  [![NPM version](https://badge.fury.io/js/buhges.png)](https://npmjs.org/package/buhges)

tool for build html pages of snippets and layers, supports [mustache](http://mustache.github.io)/[handlebars](handlebars) templates

## Installing

    npm install buhges

## Usage

<pre>
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
</pre>

    $ buhges

<pre>
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
</pre>

## Contributing

TODO write

## More Resources

- [Roadmap and Issues](https://github.com/emomteam/buhges/issues)

## Copyright and license

Copyright 2013 «Emom team»

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this work except in compliance with the License.
You may obtain a copy of the License in the LICENSE file, or at:

  [http://www.apache.org/licenses/LICENSE-2.0](http://www.apache.org/licenses/LICENSE-2.0)

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.