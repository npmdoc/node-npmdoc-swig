# api documentation for  [swig (v1.4.2)](https://github.com/paularmstrong/swig)  [![npm package](https://img.shields.io/npm/v/npmdoc-swig.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-swig) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-swig.svg)](https://travis-ci.org/npmdoc/node-npmdoc-swig)
#### A simple, powerful, and extendable templating engine for node.js and browsers, similar to Django, Jinja2, and Twig.

[![NPM](https://nodei.co/npm/swig.png?downloads=true)](https://www.npmjs.com/package/swig)

[![apidoc](https://npmdoc.github.io/node-npmdoc-swig/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-swig_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-swig/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-swig/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-swig/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Paul Armstrong",
        "email": "paul@paularmstrongdesigns.com"
    },
    "bin": {
        "swig": "./bin/swig.js"
    },
    "bugs": {
        "url": "https://github.com/paularmstrong/swig/issues"
    },
    "dependencies": {
        "optimist": "~0.6",
        "uglify-js": "~2.4"
    },
    "deprecated": "This package is no longer maintained",
    "description": "A simple, powerful, and extendable templating engine for node.js and browsers, similar to Django, Jinja2, and Twig.",
    "devDependencies": {
        "blanket": "~1.1",
        "browserify": "~2",
        "expect.js": "~0.2",
        "express": "~3",
        "file": "~0.2",
        "jsdoc": "~3.2",
        "less": "~1.4",
        "lodash": "~1.3.1",
        "mocha": "1.12.0",
        "mocha-phantomjs": "~3.1",
        "nodelint": "~0.6",
        "phantomjs": "~1.9.1",
        "still": "0.0.7",
        "travis-cov": "~0.2"
    },
    "directories": {},
    "dist": {
        "shasum": "4085ca0453369104b5d483e2841b39b7ae1aaba5",
        "tarball": "https://registry.npmjs.org/swig/-/swig-1.4.2.tgz"
    },
    "engines": {
        "node": ">=0.10.0"
    },
    "homepage": "https://github.com/paularmstrong/swig",
    "keywords": [
        "template",
        "templating",
        "html",
        "django",
        "jinja",
        "twig",
        "express",
        "block"
    ],
    "license": "MIT",
    "main": "index",
    "maintainers": [
        {
            "name": "paularmstrong",
            "email": "paul@paularmstrongdesigns.com"
        }
    ],
    "name": "swig",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git+ssh://git@github.com/paularmstrong/swig.git"
    },
    "scripts": {
        "prepublish": "npm prune && make build",
        "test": "make lint && make test reporter=spec && make test-browser && make coverage cov-reporter=travis-cov"
    },
    "version": "1.4.2"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module swig](#apidoc.module.swig)
1.  [function <span class="apidocSignatureSpan">swig.</span>Swig (opts)](#apidoc.element.swig.Swig)
1.  [function <span class="apidocSignatureSpan">swig.</span>compile (source, options)](#apidoc.element.swig.compile)
1.  [function <span class="apidocSignatureSpan">swig.</span>compileFile (pathname, options, cb)](#apidoc.element.swig.compileFile)
1.  [function <span class="apidocSignatureSpan">swig.</span>invalidateCache ()](#apidoc.element.swig.invalidateCache)
1.  [function <span class="apidocSignatureSpan">swig.</span>parseFile (pathname, options)](#apidoc.element.swig.parseFile)
1.  [function <span class="apidocSignatureSpan">swig.</span>precompile (source, options)](#apidoc.element.swig.precompile)
1.  [function <span class="apidocSignatureSpan">swig.</span>render (source, options)](#apidoc.element.swig.render)
1.  [function <span class="apidocSignatureSpan">swig.</span>renderFile (pathName, locals, cb)](#apidoc.element.swig.renderFile)
1.  [function <span class="apidocSignatureSpan">swig.</span>run (tpl, locals, filepath)](#apidoc.element.swig.run)
1.  [function <span class="apidocSignatureSpan">swig.</span>setDefaultTZOffset (offset)](#apidoc.element.swig.setDefaultTZOffset)
1.  [function <span class="apidocSignatureSpan">swig.</span>setDefaults (options)](#apidoc.element.swig.setDefaults)
1.  [function <span class="apidocSignatureSpan">swig.</span>setExtension (name, object)](#apidoc.element.swig.setExtension)
1.  [function <span class="apidocSignatureSpan">swig.</span>setFilter (name, method)](#apidoc.element.swig.setFilter)
1.  [function <span class="apidocSignatureSpan">swig.</span>setTag (name, parse, compile, ends, blockLevel)](#apidoc.element.swig.setTag)
1.  object <span class="apidocSignatureSpan">swig.</span>dateformatter
1.  object <span class="apidocSignatureSpan">swig.</span>filters
1.  object <span class="apidocSignatureSpan">swig.</span>lexer
1.  object <span class="apidocSignatureSpan">swig.</span>loaders
1.  object <span class="apidocSignatureSpan">swig.</span>parser
1.  object <span class="apidocSignatureSpan">swig.</span>utils
1.  string <span class="apidocSignatureSpan">swig.</span>version

#### [module swig.dateformatter](#apidoc.module.swig.dateformatter)
1.  [function <span class="apidocSignatureSpan">swig.dateformatter.</span>A (input)](#apidoc.element.swig.dateformatter.A)
1.  [function <span class="apidocSignatureSpan">swig.dateformatter.</span>B (input)](#apidoc.element.swig.dateformatter.B)
1.  [function <span class="apidocSignatureSpan">swig.dateformatter.</span>D (input)](#apidoc.element.swig.dateformatter.D)
1.  [function <span class="apidocSignatureSpan">swig.dateformatter.</span>DateZ ()](#apidoc.element.swig.dateformatter.DateZ)
1.  [function <span class="apidocSignatureSpan">swig.dateformatter.</span>F (input)](#apidoc.element.swig.dateformatter.F)
1.  [function <span class="apidocSignatureSpan">swig.dateformatter.</span>G (input)](#apidoc.element.swig.dateformatter.G)
1.  [function <span class="apidocSignatureSpan">swig.dateformatter.</span>H (input)](#apidoc.element.swig.dateformatter.H)
1.  [function <span class="apidocSignatureSpan">swig.dateformatter.</span>L (input)](#apidoc.element.swig.dateformatter.L)
1.  [function <span class="apidocSignatureSpan">swig.dateformatter.</span>M (input)](#apidoc.element.swig.dateformatter.M)
1.  [function <span class="apidocSignatureSpan">swig.dateformatter.</span>N (input)](#apidoc.element.swig.dateformatter.N)
1.  [function <span class="apidocSignatureSpan">swig.dateformatter.</span>O (input)](#apidoc.element.swig.dateformatter.O)
1.  [function <span class="apidocSignatureSpan">swig.dateformatter.</span>S (input)](#apidoc.element.swig.dateformatter.S)
1.  [function <span class="apidocSignatureSpan">swig.dateformatter.</span>U (input)](#apidoc.element.swig.dateformatter.U)
1.  [function <span class="apidocSignatureSpan">swig.dateformatter.</span>W (input)](#apidoc.element.swig.dateformatter.W)
1.  [function <span class="apidocSignatureSpan">swig.dateformatter.</span>Y (input)](#apidoc.element.swig.dateformatter.Y)
1.  [function <span class="apidocSignatureSpan">swig.dateformatter.</span>Z (input)](#apidoc.element.swig.dateformatter.Z)
1.  [function <span class="apidocSignatureSpan">swig.dateformatter.</span>a (input)](#apidoc.element.swig.dateformatter.a)
1.  [function <span class="apidocSignatureSpan">swig.dateformatter.</span>c (input)](#apidoc.element.swig.dateformatter.c)
1.  [function <span class="apidocSignatureSpan">swig.dateformatter.</span>d (input)](#apidoc.element.swig.dateformatter.d)
1.  [function <span class="apidocSignatureSpan">swig.dateformatter.</span>g (input)](#apidoc.element.swig.dateformatter.g)
1.  [function <span class="apidocSignatureSpan">swig.dateformatter.</span>h (input)](#apidoc.element.swig.dateformatter.h)
1.  [function <span class="apidocSignatureSpan">swig.dateformatter.</span>i (input)](#apidoc.element.swig.dateformatter.i)
1.  [function <span class="apidocSignatureSpan">swig.dateformatter.</span>j (input)](#apidoc.element.swig.dateformatter.j)
1.  [function <span class="apidocSignatureSpan">swig.dateformatter.</span>l (input)](#apidoc.element.swig.dateformatter.l)
1.  [function <span class="apidocSignatureSpan">swig.dateformatter.</span>m (input)](#apidoc.element.swig.dateformatter.m)
1.  [function <span class="apidocSignatureSpan">swig.dateformatter.</span>n (input)](#apidoc.element.swig.dateformatter.n)
1.  [function <span class="apidocSignatureSpan">swig.dateformatter.</span>o (input)](#apidoc.element.swig.dateformatter.o)
1.  [function <span class="apidocSignatureSpan">swig.dateformatter.</span>r (input)](#apidoc.element.swig.dateformatter.r)
1.  [function <span class="apidocSignatureSpan">swig.dateformatter.</span>s (input)](#apidoc.element.swig.dateformatter.s)
1.  [function <span class="apidocSignatureSpan">swig.dateformatter.</span>t (input)](#apidoc.element.swig.dateformatter.t)
1.  [function <span class="apidocSignatureSpan">swig.dateformatter.</span>w (input)](#apidoc.element.swig.dateformatter.w)
1.  [function <span class="apidocSignatureSpan">swig.dateformatter.</span>y (input)](#apidoc.element.swig.dateformatter.y)
1.  [function <span class="apidocSignatureSpan">swig.dateformatter.</span>z (input, offset, abbr)](#apidoc.element.swig.dateformatter.z)
1.  number <span class="apidocSignatureSpan">swig.dateformatter.</span>tzOffset

#### [module swig.filters](#apidoc.module.swig.filters)
1.  [function <span class="apidocSignatureSpan">swig.filters.</span>addslashes (input)](#apidoc.element.swig.filters.addslashes)
1.  [function <span class="apidocSignatureSpan">swig.filters.</span>capitalize (input)](#apidoc.element.swig.filters.capitalize)
1.  [function <span class="apidocSignatureSpan">swig.filters.</span>date (input, format, offset, abbr)](#apidoc.element.swig.filters.date)
1.  [function <span class="apidocSignatureSpan">swig.filters.</span>default (input, def)](#apidoc.element.swig.filters.default)
1.  [function <span class="apidocSignatureSpan">swig.filters.</span>e (input, type)](#apidoc.element.swig.filters.e)
1.  [function <span class="apidocSignatureSpan">swig.filters.</span>escape (input, type)](#apidoc.element.swig.filters.escape)
1.  [function <span class="apidocSignatureSpan">swig.filters.</span>first (input)](#apidoc.element.swig.filters.first)
1.  [function <span class="apidocSignatureSpan">swig.filters.</span>groupBy (input, key)](#apidoc.element.swig.filters.groupBy)
1.  [function <span class="apidocSignatureSpan">swig.filters.</span>join (input, glue)](#apidoc.element.swig.filters.join)
1.  [function <span class="apidocSignatureSpan">swig.filters.</span>json (input, indent)](#apidoc.element.swig.filters.json)
1.  [function <span class="apidocSignatureSpan">swig.filters.</span>json_encode (input, indent)](#apidoc.element.swig.filters.json_encode)
1.  [function <span class="apidocSignatureSpan">swig.filters.</span>last (input)](#apidoc.element.swig.filters.last)
1.  [function <span class="apidocSignatureSpan">swig.filters.</span>lower (input)](#apidoc.element.swig.filters.lower)
1.  [function <span class="apidocSignatureSpan">swig.filters.</span>raw (input)](#apidoc.element.swig.filters.raw)
1.  [function <span class="apidocSignatureSpan">swig.filters.</span>replace (input, search, replacement, flags)](#apidoc.element.swig.filters.replace)
1.  [function <span class="apidocSignatureSpan">swig.filters.</span>reverse (input)](#apidoc.element.swig.filters.reverse)
1.  [function <span class="apidocSignatureSpan">swig.filters.</span>safe (input)](#apidoc.element.swig.filters.safe)
1.  [function <span class="apidocSignatureSpan">swig.filters.</span>sort (input, reverse)](#apidoc.element.swig.filters.sort)
1.  [function <span class="apidocSignatureSpan">swig.filters.</span>striptags (input)](#apidoc.element.swig.filters.striptags)
1.  [function <span class="apidocSignatureSpan">swig.filters.</span>title (input)](#apidoc.element.swig.filters.title)
1.  [function <span class="apidocSignatureSpan">swig.filters.</span>uniq (input)](#apidoc.element.swig.filters.uniq)
1.  [function <span class="apidocSignatureSpan">swig.filters.</span>upper (input)](#apidoc.element.swig.filters.upper)
1.  [function <span class="apidocSignatureSpan">swig.filters.</span>url_decode (input)](#apidoc.element.swig.filters.url_decode)
1.  [function <span class="apidocSignatureSpan">swig.filters.</span>url_encode (input)](#apidoc.element.swig.filters.url_encode)

#### [module swig.lexer](#apidoc.module.swig.lexer)
1.  [function <span class="apidocSignatureSpan">swig.lexer.</span>read (str)](#apidoc.element.swig.lexer.read)
1.  object <span class="apidocSignatureSpan">swig.lexer.</span>types

#### [module swig.loaders](#apidoc.module.swig.loaders)
1.  [function <span class="apidocSignatureSpan">swig.loaders.</span>fs (basepath, encoding)](#apidoc.element.swig.loaders.fs)
1.  [function <span class="apidocSignatureSpan">swig.loaders.</span>memory (mapping, basepath)](#apidoc.element.swig.loaders.memory)

#### [module swig.parser](#apidoc.module.swig.parser)
1.  [function <span class="apidocSignatureSpan">swig.parser.</span>compile (template, parents, options, blockName)](#apidoc.element.swig.parser.compile)
1.  [function <span class="apidocSignatureSpan">swig.parser.</span>parse (swig, source, opts, tags, filters)](#apidoc.element.swig.parser.parse)

#### [module swig.utils](#apidoc.module.swig.utils)
1.  [function <span class="apidocSignatureSpan">swig.utils.</span>each (obj, fn)](#apidoc.element.swig.utils.each)
1.  [function <span class="apidocSignatureSpan">swig.utils.</span>endsWith (str, suffix)](#apidoc.element.swig.utils.endsWith)
1.  [function <span class="apidocSignatureSpan">swig.utils.</span>extend ()](#apidoc.element.swig.utils.extend)
1.  [function <span class="apidocSignatureSpan">swig.utils.</span>isArray ()](#apidoc.element.swig.utils.isArray)
1.  [function <span class="apidocSignatureSpan">swig.utils.</span>keys (obj)](#apidoc.element.swig.utils.keys)
1.  [function <span class="apidocSignatureSpan">swig.utils.</span>map (obj, fn)](#apidoc.element.swig.utils.map)
1.  [function <span class="apidocSignatureSpan">swig.utils.</span>some (obj, fn)](#apidoc.element.swig.utils.some)
1.  [function <span class="apidocSignatureSpan">swig.utils.</span>startsWith (str, prefix)](#apidoc.element.swig.utils.startsWith)
1.  [function <span class="apidocSignatureSpan">swig.utils.</span>strip (input)](#apidoc.element.swig.utils.strip)
1.  [function <span class="apidocSignatureSpan">swig.utils.</span>throwError (message, line, file)](#apidoc.element.swig.utils.throwError)



# <a name="apidoc.module.swig"></a>[module swig](#apidoc.module.swig)

#### <a name="apidoc.element.swig.Swig"></a>[function <span class="apidocSignatureSpan">swig.</span>Swig (opts)](#apidoc.element.swig.Swig)
- description and source-code
```javascript
Swig = function (opts) {
  validateOptions(opts);
  this.options = utils.extend({}, defaultOptions, opts || {});
  this.cache = {};
  this.extensions = {};
  var self = this,
    tags = _tags,
    filters = _filters;

<span class="apidocCodeCommentSpan">  /**
   * Get combined locals context.
   * @param  {?SwigOpts} [options] Swig options object.
   * @return {object}         Locals context.
   * @private
   */
</span>  function getLocals(options) {
    if (!options || !options.locals) {
      return self.options.locals;
    }

    return utils.extend({}, self.options.locals, options.locals);
  }

  /**
   * Determine whether caching is enabled via the options provided and/or defaults
   * @param  {SwigOpts} [options={}] Swig Options Object
   * @return {boolean}
   * @private
   */
  function shouldCache(options) {
    options = options || {};
    return (options.hasOwnProperty('cache') && !options.cache) || !self.options.cache;
  }

  /**
   * Get compiled template from the cache.
   * @param  {string} key           Name of template.
   * @return {object|undefined}     Template function and tokens.
   * @private
   */
  function cacheGet(key, options) {
    if (shouldCache(options)) {
      return;
    }

    if (self.options.cache === 'memory') {
      return self.cache[key];
    }

    return self.options.cache.get(key);
  }

  /**
   * Store a template in the cache.
   * @param  {string} key Name of template.
   * @param  {object} val Template function and tokens.
   * @return {undefined}
   * @private
   */
  function cacheSet(key, options, val) {
    if (shouldCache(options)) {
      return;
    }

    if (self.options.cache === 'memory') {
      self.cache[key] = val;
      return;
    }

    self.options.cache.set(key, val);
  }

  /**
   * Clears the in-memory template cache.
   *
   * @example
   * swig.invalidateCache();
   *
   * @return {undefined}
   */
  this.invalidateCache = function () {
    if (self.options.cache === 'memory') {
      self.cache = {};
    }
  };

  /**
   * Add a custom filter for swig variables.
   *
   * @example
   * function replaceMs(input) { return input.replace(/m/g, 'f'); }
   * swig.setFilter('replaceMs', replaceMs);
   * // => {{ "onomatopoeia"|replaceMs }}
   * // => onofatopeia
   *
   * @param {string}    name    Name of filter, used in templates. <strong>Will</strong> overwrite previously defined filters, if
 using the same name.
   * @param {function}  method  Function that acts against the input. See <a href="/docs/filters/#custom">Custom Filters</a> for
 more information.
   * @return {undefined}
   */
  this.setFilter = function (name, method) {
    if (typeof method !== "function") {
      throw new Error('Filter "' + name + '" is not a valid function.');
    }
    filters[name] = method;
  };

  /**
   * Add a custom tag. To expose your own extensions to compiled template code, see <code data-language="js">swig.setExtension</
code>.
   *
   * For a more in-depth explanation of writing custom tags, see <a href="../extending/#tags">Custom Tags</a>.
   *
   * @example
   * var tacotag = require('./tacotag');
   * swig.setTag('tacos', tacotag.parse, tacotag.compile, tacotag.ends, tacotag.blockLevel);
   * // => {% tacos %}Make this be tacos.{% endtacos %}
   * // => Tacos tacos tacos tacos.
   *
   * @param  {string} name      Tag name.
   * @param  {function} parse   Method for parsing tokens.
   * @param  {function} compile Method for compiling renderable output.
   * @param  {boolean} [ends=false]     Whether or not this tag requires an <i>end</i> tag.
   * @param  {boolean} [blockLevel=false] If false, this tag will not be compiled outside of <code>block</code> tags when extending
 a parent template.
   * @return {undefined}
   */
  this.setTag = function (name, parse, compile, ends, blockLevel) {
    if (typeof parse !== 'function') {
      throw new Error('Tag "' + name + '" parse method is not a valid function.');
    }

    if (typeof compile !== 'function') {
      throw new Error('Tag "' + name + '" compile method is not a valid function.');
    }

    tags[name] = {
      parse: parse,
      compile: compi ...
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.swig.compile"></a>[function <span class="apidocSignatureSpan">swig.</span>compile (source, options)](#apidoc.element.swig.compile)
- description and source-code
```javascript
compile = function (source, options) {
  var key = options ? options.filename : null,
    cached = key ? cacheGet(key, options) : null,
    context,
    contextLength,
    pre;

  if (cached) {
    return cached;
  }

  context = getLocals(options);
  contextLength = utils.keys(context).length;
  pre = this.precompile(source, options);

  function compiled(locals) {
    var lcls;
    if (locals && contextLength) {
      lcls = utils.extend({}, context, locals);
    } else if (locals && !contextLength) {
      lcls = locals;
    } else if (!locals && contextLength) {
      lcls = context;
    } else {
      lcls = {};
    }
    return pre.tpl(self, lcls, filters, utils, efn);
  }

  utils.extend(compiled, pre.tokens);

  if (key) {
    cacheSet(key, options, compiled);
  }

  return compiled;
}
```
- example usage
```shell
...
     * @param {parserCompiler} compiler
     * @param {array} [args] Array of parsed arguments on the for the token.
     * @param {array} [content] Array of content within the token.
     * @param {array} [parents] Array of parent templates for the current template context.
     * @param {SwigOpts} [options] Swig Options Object
     * @param {string} [blockName] Name of the direct block parent, if any.
     */
    o = token.compile(exports.compile, token.args ? token.args.slice(0) : [], token.content ? token.content.slice(0) : [], parents
, options, blockName);
    out += o || '';
  });

  return out;
};
...
```

#### <a name="apidoc.element.swig.compileFile"></a>[function <span class="apidocSignatureSpan">swig.</span>compileFile (pathname, options, cb)](#apidoc.element.swig.compileFile)
- description and source-code
```javascript
compileFile = function (pathname, options, cb) {
  var src, cached;

  if (!options) {
    options = {};
  }

  pathname = self.options.loader.resolve(pathname, options.resolveFrom);
  if (!options.filename) {
    options = utils.extend({ filename: pathname }, options);
  }
  cached = cacheGet(pathname, options);

  if (cached) {
    if (cb) {
      cb(null, cached);
      return;
    }
    return cached;
  }

  if (cb) {
    self.options.loader.load(pathname, function (err, src) {
      if (err) {
        cb(err);
        return;
      }
      var compiled;

      try {
        compiled = self.compile(src, options);
      } catch (err2) {
        cb(err2);
        return;
      }

      cb(err, compiled);
    });
    return;
  }

  src = self.options.loader.load(pathname);
  return self.compile(src, options);
}
```
- example usage
```shell
...
</ul>
'''

### node.js code

'''js
var swig  = require('swig');
var template = swig.compileFile('/absolute/path/to/template.html');
var output = template({
    pagename: 'awesome people',
    authors: ['Paul', 'Jim', 'Jane']
});
'''

### Output
...
```

#### <a name="apidoc.element.swig.invalidateCache"></a>[function <span class="apidocSignatureSpan">swig.</span>invalidateCache ()](#apidoc.element.swig.invalidateCache)
- description and source-code
```javascript
invalidateCache = function () {
  if (self.options.cache === 'memory') {
    self.cache = {};
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.swig.parseFile"></a>[function <span class="apidocSignatureSpan">swig.</span>parseFile (pathname, options)](#apidoc.element.swig.parseFile)
- description and source-code
```javascript
parseFile = function (pathname, options) {
  var src;

  if (!options) {
    options = {};
  }

  pathname = self.options.loader.resolve(pathname, options.resolveFrom);

  src = self.options.loader.load(pathname);

  if (!options.filename) {
    options = utils.extend({ filename: pathname }, options);
  }

  return self.parse(src, options);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.swig.precompile"></a>[function <span class="apidocSignatureSpan">swig.</span>precompile (source, options)](#apidoc.element.swig.precompile)
- description and source-code
```javascript
precompile = function (source, options) {
  var tokens = self.parse(source, options),
    parents = getParents(tokens, options),
    tpl,
    err;

  if (parents.length) {
    // Remap the templates first-parent's tokens using this template's blocks.
    tokens.tokens = remapBlocks(tokens.blocks, parents[0].tokens);
    importNonBlocks(tokens.blocks, tokens.tokens);
  }

  try {
    tpl = new Function('_swig', '_ctx', '_filters', '_utils', '_fn',
      '  var _ext = _swig.extensions,\n' +
      '    _output = "";\n' +
      parser.compile(tokens, parents, options) + '\n' +
      '  return _output;\n'
      );
  } catch (e) {
    utils.throwError(e, null, options.filename);
  }

  return { tpl: tpl, tokens: tokens };
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.swig.render"></a>[function <span class="apidocSignatureSpan">swig.</span>render (source, options)](#apidoc.element.swig.render)
- description and source-code
```javascript
render = function (source, options) {
  return self.compile(source, options)();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.swig.renderFile"></a>[function <span class="apidocSignatureSpan">swig.</span>renderFile (pathName, locals, cb)](#apidoc.element.swig.renderFile)
- description and source-code
```javascript
renderFile = function (pathName, locals, cb) {
  if (cb) {
    self.compileFile(pathName, {}, function (err, fn) {
      var result;

      if (err) {
        cb(err);
        return;
      }

      try {
        result = fn(locals);
      } catch (err2) {
        cb(err2);
        return;
      }

      cb(null, result);
    });
    return;
  }

  return self.compileFile(pathName)(locals);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.swig.run"></a>[function <span class="apidocSignatureSpan">swig.</span>run (tpl, locals, filepath)](#apidoc.element.swig.run)
- description and source-code
```javascript
run = function (tpl, locals, filepath) {
  var context = getLocals({ locals: locals });
  if (filepath) {
    cacheSet(filepath, {}, tpl);
  }
  return tpl(self, context, filters, utils, efn);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.swig.setDefaultTZOffset"></a>[function <span class="apidocSignatureSpan">swig.</span>setDefaultTZOffset (offset)](#apidoc.element.swig.setDefaultTZOffset)
- description and source-code
```javascript
setDefaultTZOffset = function (offset) {
  dateformatter.tzOffset = offset;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.swig.setDefaults"></a>[function <span class="apidocSignatureSpan">swig.</span>setDefaults (options)](#apidoc.element.swig.setDefaults)
- description and source-code
```javascript
setDefaults = function (options) {
  validateOptions(options);
  defaultInstance.options = utils.extend(defaultInstance.options, options);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.swig.setExtension"></a>[function <span class="apidocSignatureSpan">swig.</span>setExtension (name, object)](#apidoc.element.swig.setExtension)
- description and source-code
```javascript
setExtension = function (name, object) {
  self.extensions[name] = object;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.swig.setFilter"></a>[function <span class="apidocSignatureSpan">swig.</span>setFilter (name, method)](#apidoc.element.swig.setFilter)
- description and source-code
```javascript
setFilter = function (name, method) {
  if (typeof method !== "function") {
    throw new Error('Filter "' + name + '" is not a valid function.');
  }
  filters[name] = method;
}
```
- example usage
```shell
...
*
* To disable auto-escaping on a custom filter, simply add a property to the filter method 'safe = true;' and the output from this
 will not be escaped, no matter what the global settings are for Swig.
*
* @typedef {function} Filter
*
* @example
* // This filter will return 'bazbop' if the idx on the input is not 'foobar'
* swig.setFilter('foobar', function (input, idx) {
*   return input[idx] === 'foobar' ? input[idx] : 'bazbop';
* });
* // myvar = ['foo', 'bar', 'baz', 'bop'];
* // => {{ myvar|foobar(3) }}
* // Since myvar[3] !== 'foobar', we render:
* // => bazbop
*
...
```

#### <a name="apidoc.element.swig.setTag"></a>[function <span class="apidocSignatureSpan">swig.</span>setTag (name, parse, compile, ends, blockLevel)](#apidoc.element.swig.setTag)
- description and source-code
```javascript
setTag = function (name, parse, compile, ends, blockLevel) {
  if (typeof parse !== 'function') {
    throw new Error('Tag "' + name + '" parse method is not a valid function.');
  }

  if (typeof compile !== 'function') {
    throw new Error('Tag "' + name + '" compile method is not a valid function.');
  }

  tags[name] = {
    parse: parse,
    compile: compile,
    ends: ends || false,
    block: !!blockLevel
  };
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.swig.dateformatter"></a>[module swig.dateformatter](#apidoc.module.swig.dateformatter)

#### <a name="apidoc.element.swig.dateformatter.A"></a>[function <span class="apidocSignatureSpan">swig.dateformatter.</span>A (input)](#apidoc.element.swig.dateformatter.A)
- description and source-code
```javascript
A = function (input) {
  return input.getHours() < 12 ? 'AM' : 'PM';
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.swig.dateformatter.B"></a>[function <span class="apidocSignatureSpan">swig.dateformatter.</span>B (input)](#apidoc.element.swig.dateformatter.B)
- description and source-code
```javascript
B = function (input) {
  var hours = input.getUTCHours(), beats;
  hours = (hours === 23) ? 0 : hours + 1;
  beats = Math.abs(((((hours * 60) + input.getUTCMinutes()) * 60) + input.getUTCSeconds()) / 86.4).toFixed(0);
  return ('000'.concat(beats).slice(beats.length));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.swig.dateformatter.D"></a>[function <span class="apidocSignatureSpan">swig.dateformatter.</span>D (input)](#apidoc.element.swig.dateformatter.D)
- description and source-code
```javascript
D = function (input) {
  return _days.abbr[input.getDay()];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.swig.dateformatter.DateZ"></a>[function <span class="apidocSignatureSpan">swig.dateformatter.</span>DateZ ()](#apidoc.element.swig.dateformatter.DateZ)
- description and source-code
```javascript
DateZ = function () {
  var members = {
      'default': ['getUTCDate', 'getUTCDay', 'getUTCFullYear', 'getUTCHours', 'getUTCMilliseconds', 'getUTCMinutes', 'getUTCMonth
', 'getUTCSeconds', 'toISOString', 'toGMTString', 'toUTCString', 'valueOf', 'getTime'],
      z: ['getDate', 'getDay', 'getFullYear', 'getHours', 'getMilliseconds', 'getMinutes', 'getMonth', 'getSeconds', 'getYear', '
toDateString', 'toLocaleDateString', 'toLocaleTimeString']
    },
    d = this;

  d.date = d.dateZ = (arguments.length > 1) ? new Date(Date.UTC.apply(Date, arguments) + ((new Date()).getTimezoneOffset() * 60000
)) : (arguments.length === 1) ? new Date(new Date(arguments['0'])) : new Date();

  d.timezoneOffset = d.dateZ.getTimezoneOffset();

  utils.each(members.z, function (name) {
    d[name] = function () {
      return d.dateZ[name]();
    };
  });
  utils.each(members['default'], function (name) {
    d[name] = function () {
      return d.date[name]();
    };
  });

  this.setTimezoneOffset(exports.tzOffset);
}
```
- example usage
```shell
...
  return (d % 10 === 1 && d !== 11 ? 'st' : (d % 10 === 2 && d !== 12 ? 'nd' : (d % 10 === 3 && d !== 13 ? 'rd' : 'th')));
};
exports.w = function (input) {
  return input.getDay();
};
exports.z = function (input, offset, abbr) {
  var year = input.getFullYear(),
    e = new exports.DateZ(year, input.getMonth(), input.getDate(), 12, 0, 0),
    d = new exports.DateZ(year, 0, 1, 12, 0, 0);

  e.setTimezoneOffset(offset, abbr);
  d.setTimezoneOffset(offset, abbr);
  return Math.round((e - d) / 86400000);
};
...
```

#### <a name="apidoc.element.swig.dateformatter.F"></a>[function <span class="apidocSignatureSpan">swig.dateformatter.</span>F (input)](#apidoc.element.swig.dateformatter.F)
- description and source-code
```javascript
F = function (input) {
  return _months.full[input.getMonth()];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.swig.dateformatter.G"></a>[function <span class="apidocSignatureSpan">swig.dateformatter.</span>G (input)](#apidoc.element.swig.dateformatter.G)
- description and source-code
```javascript
G = function (input) {
  return input.getHours();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.swig.dateformatter.H"></a>[function <span class="apidocSignatureSpan">swig.dateformatter.</span>H (input)](#apidoc.element.swig.dateformatter.H)
- description and source-code
```javascript
H = function (input) {
  var h = input.getHours();
  return (h < 10 ? '0' : '') + h;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.swig.dateformatter.L"></a>[function <span class="apidocSignatureSpan">swig.dateformatter.</span>L (input)](#apidoc.element.swig.dateformatter.L)
- description and source-code
```javascript
L = function (input) {
  return new Date(input.getFullYear(), 1, 29).getDate() === 29;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.swig.dateformatter.M"></a>[function <span class="apidocSignatureSpan">swig.dateformatter.</span>M (input)](#apidoc.element.swig.dateformatter.M)
- description and source-code
```javascript
M = function (input) {
  return _months.abbr[input.getMonth()];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.swig.dateformatter.N"></a>[function <span class="apidocSignatureSpan">swig.dateformatter.</span>N (input)](#apidoc.element.swig.dateformatter.N)
- description and source-code
```javascript
N = function (input) {
  var d = input.getDay();
  return (d >= 1) ? d : 7;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.swig.dateformatter.O"></a>[function <span class="apidocSignatureSpan">swig.dateformatter.</span>O (input)](#apidoc.element.swig.dateformatter.O)
- description and source-code
```javascript
O = function (input) {
  var tz = input.getTimezoneOffset();
  return (tz < 0 ? '-' : '+') + (tz / 60 < 10 ? '0' : '') + Math.abs((tz / 60)) + '00';
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.swig.dateformatter.S"></a>[function <span class="apidocSignatureSpan">swig.dateformatter.</span>S (input)](#apidoc.element.swig.dateformatter.S)
- description and source-code
```javascript
S = function (input) {
  var d = input.getDate();
  return (d % 10 === 1 && d !== 11 ? 'st' : (d % 10 === 2 && d !== 12 ? 'nd' : (d % 10 === 3 && d !== 13 ? 'rd' : 'th')));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.swig.dateformatter.U"></a>[function <span class="apidocSignatureSpan">swig.dateformatter.</span>U (input)](#apidoc.element.swig.dateformatter.U)
- description and source-code
```javascript
U = function (input) {
  return input.getTime() / 1000;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.swig.dateformatter.W"></a>[function <span class="apidocSignatureSpan">swig.dateformatter.</span>W (input)](#apidoc.element.swig.dateformatter.W)
- description and source-code
```javascript
W = function (input) {
  var target = new Date(input.valueOf()),
    dayNr = (input.getDay() + 6) % 7,
    fThurs;

  target.setDate(target.getDate() - dayNr + 3);
  fThurs = target.valueOf();
  target.setMonth(0, 1);
  if (target.getDay() !== 4) {
    target.setMonth(0, 1 + ((4 - target.getDay()) + 7) % 7);
  }

  return 1 + Math.ceil((fThurs - target) / 604800000);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.swig.dateformatter.Y"></a>[function <span class="apidocSignatureSpan">swig.dateformatter.</span>Y (input)](#apidoc.element.swig.dateformatter.Y)
- description and source-code
```javascript
Y = function (input) {
  return input.getFullYear();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.swig.dateformatter.Z"></a>[function <span class="apidocSignatureSpan">swig.dateformatter.</span>Z (input)](#apidoc.element.swig.dateformatter.Z)
- description and source-code
```javascript
Z = function (input) {
  return input.getTimezoneOffset() * 60;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.swig.dateformatter.a"></a>[function <span class="apidocSignatureSpan">swig.dateformatter.</span>a (input)](#apidoc.element.swig.dateformatter.a)
- description and source-code
```javascript
a = function (input) {
  return input.getHours() < 12 ? 'am' : 'pm';
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.swig.dateformatter.c"></a>[function <span class="apidocSignatureSpan">swig.dateformatter.</span>c (input)](#apidoc.element.swig.dateformatter.c)
- description and source-code
```javascript
c = function (input) {
  return input.toISOString();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.swig.dateformatter.d"></a>[function <span class="apidocSignatureSpan">swig.dateformatter.</span>d (input)](#apidoc.element.swig.dateformatter.d)
- description and source-code
```javascript
d = function (input) {
  return (input.getDate() < 10 ? '0' : '') + input.getDate();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.swig.dateformatter.g"></a>[function <span class="apidocSignatureSpan">swig.dateformatter.</span>g (input)](#apidoc.element.swig.dateformatter.g)
- description and source-code
```javascript
g = function (input) {
  var h = input.getHours();
  return h === 0 ? 12 : (h > 12 ? h - 12 : h);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.swig.dateformatter.h"></a>[function <span class="apidocSignatureSpan">swig.dateformatter.</span>h (input)](#apidoc.element.swig.dateformatter.h)
- description and source-code
```javascript
h = function (input) {
  var h = input.getHours();
  return ((h < 10 || (12 < h && 22 > h)) ? '0' : '') + ((h < 12) ? h : h - 12);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.swig.dateformatter.i"></a>[function <span class="apidocSignatureSpan">swig.dateformatter.</span>i (input)](#apidoc.element.swig.dateformatter.i)
- description and source-code
```javascript
i = function (input) {
  var m = input.getMinutes();
  return (m < 10 ? '0' : '') + m;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.swig.dateformatter.j"></a>[function <span class="apidocSignatureSpan">swig.dateformatter.</span>j (input)](#apidoc.element.swig.dateformatter.j)
- description and source-code
```javascript
j = function (input) {
  return input.getDate();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.swig.dateformatter.l"></a>[function <span class="apidocSignatureSpan">swig.dateformatter.</span>l (input)](#apidoc.element.swig.dateformatter.l)
- description and source-code
```javascript
l = function (input) {
  return _days.full[input.getDay()];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.swig.dateformatter.m"></a>[function <span class="apidocSignatureSpan">swig.dateformatter.</span>m (input)](#apidoc.element.swig.dateformatter.m)
- description and source-code
```javascript
m = function (input) {
  return (input.getMonth() < 9 ? '0' : '') + (input.getMonth() + 1);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.swig.dateformatter.n"></a>[function <span class="apidocSignatureSpan">swig.dateformatter.</span>n (input)](#apidoc.element.swig.dateformatter.n)
- description and source-code
```javascript
n = function (input) {
  return input.getMonth() + 1;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.swig.dateformatter.o"></a>[function <span class="apidocSignatureSpan">swig.dateformatter.</span>o (input)](#apidoc.element.swig.dateformatter.o)
- description and source-code
```javascript
o = function (input) {
  var target = new Date(input.valueOf());
  target.setDate(target.getDate() - ((input.getDay() + 6) % 7) + 3);
  return target.getFullYear();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.swig.dateformatter.r"></a>[function <span class="apidocSignatureSpan">swig.dateformatter.</span>r (input)](#apidoc.element.swig.dateformatter.r)
- description and source-code
```javascript
r = function (input) {
  return input.toUTCString();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.swig.dateformatter.s"></a>[function <span class="apidocSignatureSpan">swig.dateformatter.</span>s (input)](#apidoc.element.swig.dateformatter.s)
- description and source-code
```javascript
s = function (input) {
  var s = input.getSeconds();
  return (s < 10 ? '0' : '') + s;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.swig.dateformatter.t"></a>[function <span class="apidocSignatureSpan">swig.dateformatter.</span>t (input)](#apidoc.element.swig.dateformatter.t)
- description and source-code
```javascript
t = function (input) {
  return 32 - (new Date(input.getFullYear(), input.getMonth(), 32).getDate());
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.swig.dateformatter.w"></a>[function <span class="apidocSignatureSpan">swig.dateformatter.</span>w (input)](#apidoc.element.swig.dateformatter.w)
- description and source-code
```javascript
w = function (input) {
  return input.getDay();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.swig.dateformatter.y"></a>[function <span class="apidocSignatureSpan">swig.dateformatter.</span>y (input)](#apidoc.element.swig.dateformatter.y)
- description and source-code
```javascript
y = function (input) {
  return (input.getFullYear().toString()).substr(2);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.swig.dateformatter.z"></a>[function <span class="apidocSignatureSpan">swig.dateformatter.</span>z (input, offset, abbr)](#apidoc.element.swig.dateformatter.z)
- description and source-code
```javascript
z = function (input, offset, abbr) {
  var year = input.getFullYear(),
    e = new exports.DateZ(year, input.getMonth(), input.getDate(), 12, 0, 0),
    d = new exports.DateZ(year, 0, 1, 12, 0, 0);

  e.setTimezoneOffset(offset, abbr);
  d.setTimezoneOffset(offset, abbr);
  return Math.round((e - d) / 86400000);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.swig.filters"></a>[module swig.filters](#apidoc.module.swig.filters)

#### <a name="apidoc.element.swig.filters.addslashes"></a>[function <span class="apidocSignatureSpan">swig.filters.</span>addslashes (input)](#apidoc.element.swig.filters.addslashes)
- description and source-code
```javascript
addslashes = function (input) {
  var out = iterateFilter.apply(exports.addslashes, arguments);
  if (out !== undefined) {
    return out;
  }

  return input.replace(/\\/g, '\\\\').replace(/\'/g, "\\'").replace(/\"/g, '\\"');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.swig.filters.capitalize"></a>[function <span class="apidocSignatureSpan">swig.filters.</span>capitalize (input)](#apidoc.element.swig.filters.capitalize)
- description and source-code
```javascript
capitalize = function (input) {
  var out = iterateFilter.apply(exports.capitalize, arguments);
  if (out !== undefined) {
    return out;
  }

  return input.toString().charAt(0).toUpperCase() + input.toString().substr(1).toLowerCase();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.swig.filters.date"></a>[function <span class="apidocSignatureSpan">swig.filters.</span>date (input, format, offset, abbr)](#apidoc.element.swig.filters.date)
- description and source-code
```javascript
date = function (input, format, offset, abbr) {
  var l = format.length,
    date = new dateFormatter.DateZ(input),
    cur,
    i = 0,
    out = '';

  if (offset) {
    date.setTimezoneOffset(offset, abbr);
  }

  for (i; i < l; i += 1) {
    cur = format.charAt(i);
    if (cur === '\\') {
      i += 1;
      out += (i < l) ? format.charAt(i) : cur;
    } else if (dateFormatter.hasOwnProperty(cur)) {
      out += dateFormatter[cur](date, offset, abbr);
    } else {
      out += cur;
    }
  }
  return out;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.swig.filters.default"></a>[function <span class="apidocSignatureSpan">swig.filters.</span>default (input, def)](#apidoc.element.swig.filters.default)
- description and source-code
```javascript
default = function (input, def) {
  return (typeof input !== 'undefined' && (input || typeof input === 'number')) ? input : def;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.swig.filters.e"></a>[function <span class="apidocSignatureSpan">swig.filters.</span>e (input, type)](#apidoc.element.swig.filters.e)
- description and source-code
```javascript
e = function (input, type) {
  var out = iterateFilter.apply(exports.escape, arguments),
    inp = input,
    i = 0,
    code;

  if (out !== undefined) {
    return out;
  }

  if (typeof input !== 'string') {
    return input;
  }

  out = '';

  switch (type) {
  case 'js':
    inp = inp.replace(/\\/g, '\\u005C');
    for (i; i < inp.length; i += 1) {
      code = inp.charCodeAt(i);
      if (code < 32) {
        code = code.toString(16).toUpperCase();
        code = (code.length < 2) ? '0' + code : code;
        out += '\\u00' + code;
      } else {
        out += inp[i];
      }
    }
    return out.replace(/&/g, '\\u0026')
      .replace(/</g, '\\u003C')
      .replace(/>/g, '\\u003E')
      .replace(/\'/g, '\\u0027')
      .replace(/"/g, '\\u0022')
      .replace(/\=/g, '\\u003D')
      .replace(/-/g, '\\u002D')
      .replace(/;/g, '\\u003B');

  default:
    return inp.replace(/&(?!amp;|lt;|gt;|quot;|#39;)/g, '&amp;')
      .replace(/</g, '&lt;')
      .replace(/>/g, '&gt;')
      .replace(/"/g, '&quot;')
      .replace(/'/g, '&#39;');
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.swig.filters.escape"></a>[function <span class="apidocSignatureSpan">swig.filters.</span>escape (input, type)](#apidoc.element.swig.filters.escape)
- description and source-code
```javascript
escape = function (input, type) {
  var out = iterateFilter.apply(exports.escape, arguments),
    inp = input,
    i = 0,
    code;

  if (out !== undefined) {
    return out;
  }

  if (typeof input !== 'string') {
    return input;
  }

  out = '';

  switch (type) {
  case 'js':
    inp = inp.replace(/\\/g, '\\u005C');
    for (i; i < inp.length; i += 1) {
      code = inp.charCodeAt(i);
      if (code < 32) {
        code = code.toString(16).toUpperCase();
        code = (code.length < 2) ? '0' + code : code;
        out += '\\u00' + code;
      } else {
        out += inp[i];
      }
    }
    return out.replace(/&/g, '\\u0026')
      .replace(/</g, '\\u003C')
      .replace(/>/g, '\\u003E')
      .replace(/\'/g, '\\u0027')
      .replace(/"/g, '\\u0022')
      .replace(/\=/g, '\\u003D')
      .replace(/-/g, '\\u002D')
      .replace(/;/g, '\\u003B');

  default:
    return inp.replace(/&(?!amp;|lt;|gt;|quot;|#39;)/g, '&amp;')
      .replace(/</g, '&lt;')
      .replace(/>/g, '&gt;')
      .replace(/"/g, '&quot;')
      .replace(/'/g, '&#39;');
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.swig.filters.first"></a>[function <span class="apidocSignatureSpan">swig.filters.</span>first (input)](#apidoc.element.swig.filters.first)
- description and source-code
```javascript
first = function (input) {
  if (typeof input === 'object' && !utils.isArray(input)) {
    var keys = utils.keys(input);
    return input[keys[0]];
  }

  if (typeof input === 'string') {
    return input.substr(0, 1);
  }

  return input[0];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.swig.filters.groupBy"></a>[function <span class="apidocSignatureSpan">swig.filters.</span>groupBy (input, key)](#apidoc.element.swig.filters.groupBy)
- description and source-code
```javascript
groupBy = function (input, key) {
  if (!utils.isArray(input)) {
    return input;
  }

  var out = {};

  utils.each(input, function (value) {
    if (!value.hasOwnProperty(key)) {
      return;
    }

    var keyname = value[key],
      newVal = utils.extend({}, value);
    delete value[key];

    if (!out[keyname]) {
      out[keyname] = [];
    }

    out[keyname].push(value);
  });

  return out;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.swig.filters.join"></a>[function <span class="apidocSignatureSpan">swig.filters.</span>join (input, glue)](#apidoc.element.swig.filters.join)
- description and source-code
```javascript
join = function (input, glue) {
  if (utils.isArray(input)) {
    return input.join(glue);
  }

  if (typeof input === 'object') {
    var out = [];
    utils.each(input, function (value) {
      out.push(value);
    });
    return out.join(glue);
  }
  return input;
}
```
- example usage
```shell
...
 *
 * @param  {*}  input
 * @param  {string} glue    String value to join items together.
 * @return {string}
 */
exports.join = function (input, glue) {
if (utils.isArray(input)) {
  return input.join(glue);
}

if (typeof input === 'object') {
  var out = [];
  utils.each(input, function (value) {
    out.push(value);
  });
...
```

#### <a name="apidoc.element.swig.filters.json"></a>[function <span class="apidocSignatureSpan">swig.filters.</span>json (input, indent)](#apidoc.element.swig.filters.json)
- description and source-code
```javascript
json = function (input, indent) {
  return JSON.stringify(input, null, indent || 0);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.swig.filters.json_encode"></a>[function <span class="apidocSignatureSpan">swig.filters.</span>json_encode (input, indent)](#apidoc.element.swig.filters.json_encode)
- description and source-code
```javascript
json_encode = function (input, indent) {
  return JSON.stringify(input, null, indent || 0);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.swig.filters.last"></a>[function <span class="apidocSignatureSpan">swig.filters.</span>last (input)](#apidoc.element.swig.filters.last)
- description and source-code
```javascript
last = function (input) {
  if (typeof input === 'object' && !utils.isArray(input)) {
    var keys = utils.keys(input);
    return input[keys[keys.length - 1]];
  }

  if (typeof input === 'string') {
    return input.charAt(input.length - 1);
  }

  return input[input.length - 1];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.swig.filters.lower"></a>[function <span class="apidocSignatureSpan">swig.filters.</span>lower (input)](#apidoc.element.swig.filters.lower)
- description and source-code
```javascript
lower = function (input) {
  var out = iterateFilter.apply(exports.lower, arguments);
  if (out !== undefined) {
    return out;
  }

  return input.toString().toLowerCase();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.swig.filters.raw"></a>[function <span class="apidocSignatureSpan">swig.filters.</span>raw (input)](#apidoc.element.swig.filters.raw)
- description and source-code
```javascript
raw = function (input) {
  return exports.safe(input);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.swig.filters.replace"></a>[function <span class="apidocSignatureSpan">swig.filters.</span>replace (input, search, replacement, flags)](#apidoc.element.swig.filters.replace)
- description and source-code
```javascript
replace = function (input, search, replacement, flags) {
  var r = new RegExp(search, flags);
  return input.replace(r, replacement);
}
```
- example usage
```shell
...
*/
exports.addslashes = function (input) {
 var out = iterateFilter.apply(exports.addslashes, arguments);
 if (out !== undefined) {
   return out;
 }

 return input.replace(/\\/g, '\\\\').replace(/\'/g, "\\'").replace(/\"/g, '\\"');
};

/**
* Upper-case the first letter of the input and lower-case the rest.
*
* @example
* {{ "i like Burritos"|capitalize }}
...
```

#### <a name="apidoc.element.swig.filters.reverse"></a>[function <span class="apidocSignatureSpan">swig.filters.</span>reverse (input)](#apidoc.element.swig.filters.reverse)
- description and source-code
```javascript
reverse = function (input) {
  return exports.sort(input, true);
}
```
- example usage
```shell
...
  switch (typeof input) {
  case 'object':
    out = utils.keys(input).sort();
    break;
  case 'string':
    out = input.split('');
    if (reverse) {
      return out.reverse().join('');
    }
    return out.sort().join('');
  }
}

if (out && reverse) {
  return out.reverse();
...
```

#### <a name="apidoc.element.swig.filters.safe"></a>[function <span class="apidocSignatureSpan">swig.filters.</span>safe (input)](#apidoc.element.swig.filters.safe)
- description and source-code
```javascript
safe = function (input) {
  // This is a magic filter. Its logic is hard-coded into Swig's parser.
  return input;
}
```
- example usage
```shell
...
 return input.toString().toLowerCase();
};

/**
* Deprecated in favor of <a href="#safe">safe</a>.
*/
exports.raw = function (input) {
 return exports.safe(input);
};
exports.raw.safe = true;

/**
* Returns a new string with the matched search pattern replaced by the given replacement string. Uses JavaScript's built-in String
.replace() method.
*
* @example
...
```

#### <a name="apidoc.element.swig.filters.sort"></a>[function <span class="apidocSignatureSpan">swig.filters.</span>sort (input, reverse)](#apidoc.element.swig.filters.sort)
- description and source-code
```javascript
sort = function (input, reverse) {
  var out;
  if (utils.isArray(input)) {
    out = input.sort();
  } else {
    switch (typeof input) {
    case 'object':
      out = utils.keys(input).sort();
      break;
    case 'string':
      out = input.split('');
      if (reverse) {
        return out.reverse().join('');
      }
      return out.sort().join('');
    }
  }

  if (out && reverse) {
    return out.reverse();
  }

  return out || input;
}
```
- example usage
```shell
...
* {{ val|reverse }}
* // => 3,2,1
*
* @param  {array}  input
* @return {array}        Reversed array. The original input object is returned if it was not an array.
*/
exports.reverse = function (input) {
 return exports.sort(input, true);
};

/**
* Forces the input to not be auto-escaped. Use this only on content that you know is safe to be rendered on your page.
*
* @example
* // my_var = "<p>Stuff</p>";
...
```

#### <a name="apidoc.element.swig.filters.striptags"></a>[function <span class="apidocSignatureSpan">swig.filters.</span>striptags (input)](#apidoc.element.swig.filters.striptags)
- description and source-code
```javascript
striptags = function (input) {
  var out = iterateFilter.apply(exports.striptags, arguments);
  if (out !== undefined) {
    return out;
  }

  return input.toString().replace(/(<([^>]+)>)/ig, '');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.swig.filters.title"></a>[function <span class="apidocSignatureSpan">swig.filters.</span>title (input)](#apidoc.element.swig.filters.title)
- description and source-code
```javascript
title = function (input) {
  var out = iterateFilter.apply(exports.title, arguments);
  if (out !== undefined) {
    return out;
  }

  return input.toString().replace(/\w\S*/g, function (str) {
    return str.charAt(0).toUpperCase() + str.substr(1).toLowerCase();
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.swig.filters.uniq"></a>[function <span class="apidocSignatureSpan">swig.filters.</span>uniq (input)](#apidoc.element.swig.filters.uniq)
- description and source-code
```javascript
uniq = function (input) {
  var result;

  if (!input || !utils.isArray(input)) {
    return '';
  }

  result = [];
  utils.each(input, function (v) {
    if (result.indexOf(v) === -1) {
      result.push(v);
    }
  });
  return result;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.swig.filters.upper"></a>[function <span class="apidocSignatureSpan">swig.filters.</span>upper (input)](#apidoc.element.swig.filters.upper)
- description and source-code
```javascript
upper = function (input) {
  var out = iterateFilter.apply(exports.upper, arguments);
  if (out !== undefined) {
    return out;
  }

  return input.toString().toUpperCase();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.swig.filters.url_decode"></a>[function <span class="apidocSignatureSpan">swig.filters.</span>url_decode (input)](#apidoc.element.swig.filters.url_decode)
- description and source-code
```javascript
url_decode = function (input) {
  var out = iterateFilter.apply(exports.url_decode, arguments);
  if (out !== undefined) {
    return out;
  }
  return decodeURIComponent(input);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.swig.filters.url_encode"></a>[function <span class="apidocSignatureSpan">swig.filters.</span>url_encode (input)](#apidoc.element.swig.filters.url_encode)
- description and source-code
```javascript
url_encode = function (input) {
  var out = iterateFilter.apply(exports.url_encode, arguments);
  if (out !== undefined) {
    return out;
  }
  return encodeURIComponent(input);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.swig.lexer"></a>[module swig.lexer](#apidoc.module.swig.lexer)

#### <a name="apidoc.element.swig.lexer.read"></a>[function <span class="apidocSignatureSpan">swig.lexer.</span>read (str)](#apidoc.element.swig.lexer.read)
- description and source-code
```javascript
read = function (str) {
  var offset = 0,
    tokens = [],
    substr,
    match;
  while (offset < str.length) {
    substr = str.substring(offset);
    match = reader(substr);
    offset += match.length;
    tokens.push(match);
  }
  return tokens;
}
```
- example usage
```shell
...
   * Parse a variable.
   * @param  {string} str  String contents of the variable, between <i>{{</i> and <i>}}</i>
   * @param  {number} line The line number that this variable starts on.
   * @return {VarToken}      Parsed variable token object.
   * @private
   */
  function parseVariable(str, line) {
var tokens = lexer.read(utils.strip(str)),
  parser,
  out;

parser = new TokenParser(tokens, filters, escape, line, opts.filename);
out = parser.parse().join('');

if (parser.state.length) {
...
```



# <a name="apidoc.module.swig.loaders"></a>[module swig.loaders](#apidoc.module.swig.loaders)

#### <a name="apidoc.element.swig.loaders.fs"></a>[function <span class="apidocSignatureSpan">swig.loaders.</span>fs (basepath, encoding)](#apidoc.element.swig.loaders.fs)
- description and source-code
```javascript
fs = function (basepath, encoding) {
  var ret = {};

  encoding = encoding || 'utf8';
  basepath = (basepath) ? path.normalize(basepath) : null;

<span class="apidocCodeCommentSpan">  /**
   * Resolves <var>to</var> to an absolute path or unique identifier. This is used for building correct, normalized, and absolute
 paths to a given template.
   * @alias resolve
   * @param  {string} to        Non-absolute identifier or pathname to a file.
   * @param  {string} [from]    If given, should attempt to find the <var>to</var> path in relation to this given, known path.
   * @return {string}
   */
</span>  ret.resolve = function (to, from) {
    if (basepath) {
      from = basepath;
    } else {
      from = (from) ? path.dirname(from) : process.cwd();
    }
    return path.resolve(from, to);
  };

  /**
   * Loads a single template. Given a unique <var>identifier</var> found by the <var>resolve</var> method this should return the
 given template.
   * @alias load
   * @param  {string}   identifier  Unique identifier of a template (possibly an absolute path).
   * @param  {function} [cb]        Asynchronous callback function. If not provided, this method should run synchronously.
   * @return {string}               Template source string.
   */
  ret.load = function (identifier, cb) {
    if (!fs || (cb && !fs.readFile) || !fs.readFileSync) {
      throw new Error('Unable to find file ' + identifier + ' because there is no filesystem to read from.');
    }

    identifier = ret.resolve(identifier);

    if (cb) {
      fs.readFile(identifier, encoding, cb);
      return;
    }
    return fs.readFileSync(identifier, encoding);
  };

  return ret;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.swig.loaders.memory"></a>[function <span class="apidocSignatureSpan">swig.loaders.</span>memory (mapping, basepath)](#apidoc.element.swig.loaders.memory)
- description and source-code
```javascript
memory = function (mapping, basepath) {
  var ret = {};

  basepath = (basepath) ? path.normalize(basepath) : null;

<span class="apidocCodeCommentSpan">  /**
   * Resolves <var>to</var> to an absolute path or unique identifier. This is used for building correct, normalized, and absolute
 paths to a given template.
   * @alias resolve
   * @param  {string} to        Non-absolute identifier or pathname to a file.
   * @param  {string} [from]    If given, should attempt to find the <var>to</var> path in relation to this given, known path.
   * @return {string}
   */
</span>  ret.resolve = function (to, from) {
    if (basepath) {
      from = basepath;
    } else {
      from = (from) ? path.dirname(from) : '/';
    }
    return path.resolve(from, to);
  };

  /**
   * Loads a single template. Given a unique <var>identifier</var> found by the <var>resolve</var> method this should return the
 given template.
   * @alias load
   * @param  {string}   identifier  Unique identifier of a template (possibly an absolute path).
   * @param  {function} [cb]        Asynchronous callback function. If not provided, this method should run synchronously.
   * @return {string}               Template source string.
   */
  ret.load = function (pathname, cb) {
    var src, paths;

    paths = [pathname, pathname.replace(/^(\/|\\)/, '')];

    src = mapping[paths[0]] || mapping[paths[1]];
    if (!src) {
      utils.throwError('Unable to find template "' + pathname + '".');
    }

    if (cb) {
      cb(null, src);
      return;
    }
    return src;
  };

  return ret;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.swig.parser"></a>[module swig.parser](#apidoc.module.swig.parser)

#### <a name="apidoc.element.swig.parser.compile"></a>[function <span class="apidocSignatureSpan">swig.parser.</span>compile (template, parents, options, blockName)](#apidoc.element.swig.parser.compile)
- description and source-code
```javascript
compile = function (template, parents, options, blockName) {
  var out = '',
    tokens = utils.isArray(template) ? template : template.tokens;

  utils.each(tokens, function (token) {
    var o;
    if (typeof token === 'string') {
      out += '_output += "' + token.replace(/\\/g, '\\\\').replace(/\n|\r/g, '\\n').replace(/"/g, '\\"') + '";\n';
      return;
    }

<span class="apidocCodeCommentSpan">    /**
     * Compile callback for VarToken and TagToken objects.
     * @callback compile
     *
     * @example
     * exports.compile = function (compiler, args, content, parents, options, blockName) {
     *   if (args[0] === 'foo') {
     *     return compiler(content, parents, options, blockName) + '\n';
     *   }
     *   return '_output += "fallback";\n';
     * };
     *
     * @param {parserCompiler} compiler
     * @param {array} [args] Array of parsed arguments on the for the token.
     * @param {array} [content] Array of content within the token.
     * @param {array} [parents] Array of parent templates for the current template context.
     * @param {SwigOpts} [options] Swig Options Object
     * @param {string} [blockName] Name of the direct block parent, if any.
     */
</span>    o = token.compile(exports.compile, token.args ? token.args.slice(0) : [], token.content ? token.content.slice(0) : [], parents
, options, blockName);
    out += o || '';
  });

  return out;
}
```
- example usage
```shell
...
     * @param {parserCompiler} compiler
     * @param {array} [args] Array of parsed arguments on the for the token.
     * @param {array} [content] Array of content within the token.
     * @param {array} [parents] Array of parent templates for the current template context.
     * @param {SwigOpts} [options] Swig Options Object
     * @param {string} [blockName] Name of the direct block parent, if any.
     */
    o = token.compile(exports.compile, token.args ? token.args.slice(0) : [], token.content ? token.content.slice(0) : [], parents
, options, blockName);
    out += o || '';
  });

  return out;
};
...
```

#### <a name="apidoc.element.swig.parser.parse"></a>[function <span class="apidocSignatureSpan">swig.parser.</span>parse (swig, source, opts, tags, filters)](#apidoc.element.swig.parser.parse)
- description and source-code
```javascript
parse = function (swig, source, opts, tags, filters) {
  source = source.replace(/\r\n/g, '\n');
  var escape = opts.autoescape,
    tagOpen = opts.tagControls[0],
    tagClose = opts.tagControls[1],
    varOpen = opts.varControls[0],
    varClose = opts.varControls[1],
    escapedTagOpen = escapeRegExp(tagOpen),
    escapedTagClose = escapeRegExp(tagClose),
    escapedVarOpen = escapeRegExp(varOpen),
    escapedVarClose = escapeRegExp(varClose),
    tagStrip = new RegExp('^' + escapedTagOpen + '-?\\s*-?|-?\\s*-?' + escapedTagClose + '$', 'g'),
    tagStripBefore = new RegExp('^' + escapedTagOpen + '-'),
    tagStripAfter = new RegExp('-' + escapedTagClose + '$'),
    varStrip = new RegExp('^' + escapedVarOpen + '-?\\s*-?|-?\\s*-?' + escapedVarClose + '$', 'g'),
    varStripBefore = new RegExp('^' + escapedVarOpen + '-'),
    varStripAfter = new RegExp('-' + escapedVarClose + '$'),
    cmtOpen = opts.cmtControls[0],
    cmtClose = opts.cmtControls[1],
    anyChar = '[\\s\\S]*?',
    // Split the template source based on variable, tag, and comment blocks
    // /(\{%[\s\S]*?%\}|\{\{[\s\S]*?\}\}|\{#[\s\S]*?#\})/
    splitter = new RegExp(
      '(' +
        escapedTagOpen + anyChar + escapedTagClose + '|' +
        escapedVarOpen + anyChar + escapedVarClose + '|' +
        escapeRegExp(cmtOpen) + anyChar + escapeRegExp(cmtClose) +
        ')'
    ),
    line = 1,
    stack = [],
    parent = null,
    tokens = [],
    blocks = {},
    inRaw = false,
    stripNext;

<span class="apidocCodeCommentSpan">  /**
   * Parse a variable.
   * @param  {string} str  String contents of the variable, between <i>{{</i> and <i>}}</i>
   * @param  {number} line The line number that this variable starts on.
   * @return {VarToken}      Parsed variable token object.
   * @private
   */
</span>  function parseVariable(str, line) {
    var tokens = lexer.read(utils.strip(str)),
      parser,
      out;

    parser = new TokenParser(tokens, filters, escape, line, opts.filename);
    out = parser.parse().join('');

    if (parser.state.length) {
      utils.throwError('Unable to parse "' + str + '"', line, opts.filename);
    }

    /**
     * A parsed variable token.
     * @typedef {object} VarToken
     * @property {function} compile Method for compiling this token.
     */
    return {
      compile: function () {
        return '_output += ' + out + ';\n';
      }
    };
  }
  exports.parseVariable = parseVariable;

  /**
   * Parse a tag.
   * @param  {string} str  String contents of the tag, between <i>{%</i> and <i>%}</i>
   * @param  {number} line The line number that this tag starts on.
   * @return {TagToken}      Parsed token object.
   * @private
   */
  function parseTag(str, line) {
    var tokens, parser, chunks, tagName, tag, args, last;

    if (utils.startsWith(str, 'end')) {
      last = stack[stack.length - 1];
      if (last && last.name === str.split(/\s+/)[0].replace(/^end/, '') && last.ends) {
        switch (last.name) {
        case 'autoescape':
          escape = opts.autoescape;
          break;
        case 'raw':
          inRaw = false;
          break;
        }
        stack.pop();
        return;
      }

      if (!inRaw) {
        utils.throwError('Unexpected end of tag "' + str.replace(/^end/, '') + '"', line, opts.filename);
      }
    }

    if (inRaw) {
      return;
    }

    chunks = str.split(/\s+(.+)?/);
    tagName = chunks.shift();

    if (!tags.hasOwnProperty(tagName)) {
      utils.throwError('Unexpected tag "' + str + '"', line, opts.filename);
    }

    tokens = lexer.read(utils.strip(chunks.join(' ')));
    parser = new TokenParser(tokens, filters, false, line, opts.filename);
    tag = tags[tagName];

    /**
     * Define custom parsing methods for your tag.
     * @callback parse
     *
     * @example
     * exports.parse = function (str, line, parser, types, options, swig) {
     *   parser.on('start', function () {
     *     // ...
     *   });
     *   parser.on(types.STRING, function (token) {
     *     // ...
     *   });
     * };
     *
     * @param {string} str The full token string of the tag.
     * @param {number} line ...
```
- example usage
```shell
...
 }
};

/**
* Parse a source string into tokens that are ready for compilation.
*
* @example
* exports.parse('{{ tacos }}', {}, tags, filters);
* // => [{ compile: [Function], ... }]
*
* @params {object} swig    The current Swig instance
* @param  {string} source  Swig template source.
* @param  {object} opts    Swig options object.
* @param  {object} tags    Keyed object of tags that can be parsed and compiled.
* @param  {object} filters Keyed object of filters that may be applied to variables.
...
```



# <a name="apidoc.module.swig.utils"></a>[module swig.utils](#apidoc.module.swig.utils)

#### <a name="apidoc.element.swig.utils.each"></a>[function <span class="apidocSignatureSpan">swig.utils.</span>each (obj, fn)](#apidoc.element.swig.utils.each)
- description and source-code
```javascript
each = function (obj, fn) {
  var i, l;

  if (isArray(obj)) {
    i = 0;
    l = obj.length;
    for (i; i < l; i += 1) {
      if (fn(obj[i], i, obj) === false) {
        break;
      }
    }
  } else {
    for (i in obj) {
      if (obj.hasOwnProperty(i)) {
        if (fn(obj[i], i, obj) === false) {
          break;
        }
      }
    }
  }

  return obj;
}
```
- example usage
```shell
...
  },
  d = this;

d.date = d.dateZ = (arguments.length > 1) ? new Date(Date.UTC.apply(Date, arguments) + ((new Date()).getTimezoneOffset() * 60000
)) : (arguments.length === 1) ? new Date(new Date(arguments['0'])) : new Date();

d.timezoneOffset = d.dateZ.getTimezoneOffset();

utils.each(members.z, function (name) {
  d[name] = function () {
    return d.dateZ[name]();
  };
});
utils.each(members['default'], function (name) {
  d[name] = function () {
    return d.date[name]();
...
```

#### <a name="apidoc.element.swig.utils.endsWith"></a>[function <span class="apidocSignatureSpan">swig.utils.</span>endsWith (str, suffix)](#apidoc.element.swig.utils.endsWith)
- description and source-code
```javascript
endsWith = function (str, suffix) {
  return str.indexOf(suffix, str.length - suffix.length) !== -1;
}
```
- example usage
```shell
...
var token, lines, stripPrev, prevToken, prevChildToken;

if (!chunk) {
  return;
}

// Is a variable?
if (!inRaw && utils.startsWith(chunk, varOpen) && utils.endsWith(chunk, varClose)) {
  stripPrev = varStripBefore.test(chunk);
  stripNext = varStripAfter.test(chunk);
  token = parseVariable(chunk.replace(varStrip, ''), line);
// Is a tag?
} else if (utils.startsWith(chunk, tagOpen) && utils.endsWith(chunk, tagClose)) {
  stripPrev = tagStripBefore.test(chunk);
  stripNext = tagStripAfter.test(chunk);
...
```

#### <a name="apidoc.element.swig.utils.extend"></a>[function <span class="apidocSignatureSpan">swig.utils.</span>extend ()](#apidoc.element.swig.utils.extend)
- description and source-code
```javascript
extend = function () {
  var args = arguments,
    target = args[0],
    objs = (args.length > 1) ? Array.prototype.slice.call(args, 1) : [],
    i = 0,
    l = objs.length,
    key,
    obj;

  for (i; i < l; i += 1) {
    obj = objs[i] || {};
    for (key in obj) {
      if (obj.hasOwnProperty(key)) {
        target[key] = obj[key];
      }
    }
  }
  return target;
}
```
- example usage
```shell
...

  utils.each(input, function (value) {
if (!value.hasOwnProperty(key)) {
  return;
}

var keyname = value[key],
  newVal = utils.extend({}, value);
delete value[key];

if (!out[keyname]) {
  out[keyname] = [];
}

out[keyname].push(value);
...
```

#### <a name="apidoc.element.swig.utils.isArray"></a>[function <span class="apidocSignatureSpan">swig.utils.</span>isArray ()](#apidoc.element.swig.utils.isArray)
- description and source-code
```javascript
function isArray() { [native code] }
```
- example usage
```shell
...
 * @return {*}
 * @private
 */
function iterateFilter(input) {
var self = this,
  out = {};

if (utils.isArray(input)) {
  return utils.map(input, function (value) {
    return self.apply(null, arguments);
  });
}

if (typeof input === 'object') {
  utils.each(input, function (value, key) {
...
```

#### <a name="apidoc.element.swig.utils.keys"></a>[function <span class="apidocSignatureSpan">swig.utils.</span>keys (obj)](#apidoc.element.swig.utils.keys)
- description and source-code
```javascript
keys = function (obj) {
  if (!obj) {
    return [];
  }

  if (Object.keys) {
    return Object.keys(obj);
  }

  return exports.map(obj, function (v, k) {
    return k;
  });
}
```
- example usage
```shell
...
 * // T
 *
 * @param  {*} input
 * @return {*}        The first item of the array or first character of the string input.
 */
exports.first = function (input) {
if (typeof input === 'object' && !utils.isArray(input)) {
  var keys = utils.keys(input);
  return input[keys[0]];
}

if (typeof input === 'string') {
  return input.substr(0, 1);
}
...
```

#### <a name="apidoc.element.swig.utils.map"></a>[function <span class="apidocSignatureSpan">swig.utils.</span>map (obj, fn)](#apidoc.element.swig.utils.map)
- description and source-code
```javascript
map = function (obj, fn) {
  var i = 0,
    result = [],
    l;

  if (isArray(obj)) {
    l = obj.length;
    for (i; i < l; i += 1) {
      result[i] = fn(obj[i], i);
    }
  } else {
    for (i in obj) {
      if (obj.hasOwnProperty(i)) {
        result[i] = fn(obj[i], i);
      }
    }
  }
  return result;
}
```
- example usage
```shell
...
 * @private
 */
function iterateFilter(input) {
var self = this,
  out = {};

if (utils.isArray(input)) {
  return utils.map(input, function (value) {
    return self.apply(null, arguments);
  });
}

if (typeof input === 'object') {
  utils.each(input, function (value, key) {
    out[key] = self.apply(null, arguments);
...
```

#### <a name="apidoc.element.swig.utils.some"></a>[function <span class="apidocSignatureSpan">swig.utils.</span>some (obj, fn)](#apidoc.element.swig.utils.some)
- description and source-code
```javascript
some = function (obj, fn) {
  var i = 0,
    result,
    l;
  if (isArray(obj)) {
    l = obj.length;

    for (i; i < l; i += 1) {
      result = fn(obj[i], i, obj);
      if (result) {
        break;
      }
    }
  } else {
    exports.each(obj, function (value, index) {
      result = fn(value, index, obj);
      return !(result);
    });
  }
  return !!result;
}
```
- example usage
```shell
...
 * @param  {string} str String chunk.
 * @return {LexerToken}     Defined type, potentially stripped or replaced with more suitable content.
 * @private
 */
function reader(str) {
  var matched;

  utils.some(rules, function (rule) {
    return utils.some(rule.regex, function (regex) {
var match = str.match(regex),
  normalized;

if (!match) {
  return;
}
...
```

#### <a name="apidoc.element.swig.utils.startsWith"></a>[function <span class="apidocSignatureSpan">swig.utils.</span>startsWith (str, prefix)](#apidoc.element.swig.utils.startsWith)
- description and source-code
```javascript
startsWith = function (str, prefix) {
  return str.indexOf(prefix) === 0;
}
```
- example usage
```shell
...
   * @param  {number} line The line number that this tag starts on.
   * @return {TagToken}      Parsed token object.
   * @private
   */
  function parseTag(str, line) {
var tokens, parser, chunks, tagName, tag, args, last;

if (utils.startsWith(str, 'end')) {
  last = stack[stack.length - 1];
  if (last && last.name === str.split(/\s+/)[0].replace(/^end/, '') && last.ends) {
    switch (last.name) {
    case 'autoescape':
      escape = opts.autoescape;
      break;
    case 'raw':
...
```

#### <a name="apidoc.element.swig.utils.strip"></a>[function <span class="apidocSignatureSpan">swig.utils.</span>strip (input)](#apidoc.element.swig.utils.strip)
- description and source-code
```javascript
strip = function (input) {
  return input.replace(/^\s+|\s+$/g, '');
}
```
- example usage
```shell
...
   * Parse a variable.
   * @param  {string} str  String contents of the variable, between <i>{{</i> and <i>}}</i>
   * @param  {number} line The line number that this variable starts on.
   * @return {VarToken}      Parsed variable token object.
   * @private
   */
  function parseVariable(str, line) {
var tokens = lexer.read(utils.strip(str)),
  parser,
  out;

parser = new TokenParser(tokens, filters, escape, line, opts.filename);
out = parser.parse().join('');

if (parser.state.length) {
...
```

#### <a name="apidoc.element.swig.utils.throwError"></a>[function <span class="apidocSignatureSpan">swig.utils.</span>throwError (message, line, file)](#apidoc.element.swig.utils.throwError)
- description and source-code
```javascript
throwError = function (message, line, file) {
  if (line) {
    message += ' on line ' + line;
  }
  if (file) {
    message += ' in file ' + file;
  }
  throw new Error(message + '.');
}
```
- example usage
```shell
...
case _t.BOOL:
  self.filterApplyIdx.push(self.out.length);
  self.out.push(match);
  break;

case _t.FILTER:
  if (!self.filters.hasOwnProperty(match) || typeof self.filters[match] !== "function") {
    utils.throwError('Invalid filter "' + match + '"', self.line, self.filename);
  }
  self.escape = self.filters[match].safe ? false : self.escape;
  self.out.splice(self.filterApplyIdx[self.filterApplyIdx.length - 1], 0, '_filters["' + match + '"](');
  self.state.push(token.type);
  break;

case _t.FILTEREMPTY:
...
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
