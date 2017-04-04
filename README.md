# api documentation for  [node-restful (v0.2.6)](https://github.com/baugarten/node-restful#readme)  [![npm package](https://img.shields.io/npm/v/npmdoc-node-restful.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-node-restful) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-node-restful.svg)](https://travis-ci.org/npmdoc/node-npmdoc-node-restful)
#### A library for making REST API's in node.js with express

[![NPM](https://nodei.co/npm/node-restful.png?downloads=true)](https://www.npmjs.com/package/node-restful)

[![apidoc](https://npmdoc.github.io/node-npmdoc-node-restful/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-node-restful_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-node-restful/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-node-restful/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-node-restful/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "bugs": {
        "url": "https://github.com/baugarten/node-restful/issues"
    },
    "dependencies": {
        "underscore": "1.8.3"
    },
    "description": "A library for making REST API's in node.js with express",
    "devDependencies": {
        "body-parser": "1.12.4",
        "express": "4.12.4",
        "jade": "1.11.0",
        "method-override": "2.3.3",
        "mocha": "2.2.5",
        "mongodb": "2.0.33",
        "mongoose": "~4",
        "morgan": "1.5.3",
        "pow-mongodb-fixtures": "git+https://github.com/riyadhalnur/pow-mongodb-fixtures.git#upgrade-mongodb-drivers",
        "should": "6.0.3",
        "sinon": "1.15.3",
        "supertest": "1.0.1"
    },
    "directories": {},
    "dist": {
        "shasum": "42ab3adc8c1a5f94ed864799845f8efe311e632e",
        "tarball": "https://registry.npmjs.org/node-restful/-/node-restful-0.2.6.tgz"
    },
    "gitHead": "a018736a30b0979ea5f848258ba34549e60fc04e",
    "homepage": "https://github.com/baugarten/node-restful#readme",
    "keywords": [
        "node-restful",
        "restful",
        "framework",
        "rest",
        "api"
    ],
    "main": "index.js",
    "maintainers": [
        {
            "name": "baugarten",
            "email": "baugarten@gmail.com"
        }
    ],
    "name": "node-restful",
    "optionalDependencies": {},
    "peerDependencies": {
        "mongoose": "~4"
    },
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git://github.com/baugarten/node-restful.git"
    },
    "scripts": {
        "test": "make test"
    },
    "version": "0.2.6"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module node-restful](#apidoc.module.node-restful)
1.  [function <span class="apidocSignatureSpan">node-restful.</span>authFailure ()](#apidoc.element.node-restful.authFailure)
1.  [function <span class="apidocSignatureSpan">node-restful.</span>badRequest (errobj)](#apidoc.element.node-restful.badRequest)
1.  [function <span class="apidocSignatureSpan">node-restful.</span>delete (req, res, next)](#apidoc.element.node-restful.delete)
1.  [function <span class="apidocSignatureSpan">node-restful.</span>get (req, res, next)](#apidoc.element.node-restful.get)
1.  [function <span class="apidocSignatureSpan">node-restful.</span>getDetail (req, res, next)](#apidoc.element.node-restful.getDetail)
1.  [function <span class="apidocSignatureSpan">node-restful.</span>getPath (pathName)](#apidoc.element.node-restful.getPath)
1.  [function <span class="apidocSignatureSpan">node-restful.</span>last (req, res, next)](#apidoc.element.node-restful.last)
1.  [function <span class="apidocSignatureSpan">node-restful.</span>model ()](#apidoc.element.node-restful.model)
1.  [function <span class="apidocSignatureSpan">node-restful.</span>objectNotFound ()](#apidoc.element.node-restful.objectNotFound)
1.  [function <span class="apidocSignatureSpan">node-restful.</span>post (req, res, next)](#apidoc.element.node-restful.post)
1.  [function <span class="apidocSignatureSpan">node-restful.</span>put (req, res, next)](#apidoc.element.node-restful.put)
1.  [function <span class="apidocSignatureSpan">node-restful.</span>respond (res, statusCode, content)](#apidoc.element.node-restful.respond)
1.  [function <span class="apidocSignatureSpan">node-restful.</span>respond404 ()](#apidoc.element.node-restful.respond404)
1.  [function <span class="apidocSignatureSpan">node-restful.</span>respondOrErr (res, errStatusCode, err, statusCode, content)](#apidoc.element.node-restful.respondOrErr)
1.  [function <span class="apidocSignatureSpan">node-restful.</span>schema (req, res, next)](#apidoc.element.node-restful.schema)
1.  object <span class="apidocSignatureSpan">node-restful.</span>mongoose



# <a name="apidoc.module.node-restful"></a>[module node-restful](#apidoc.module.node-restful)

#### <a name="apidoc.element.node-restful.authFailure"></a>[function <span class="apidocSignatureSpan">node-restful.</span>authFailure ()](#apidoc.element.node-restful.authFailure)
- description and source-code
```javascript
authFailure = function () {
  return {
    status: 401,
    message: 'Unauthorized',
    name: "Unauthorized",
    errors: 'Operation not authorzed on ' + this.modelName
  };
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.node-restful.badRequest"></a>[function <span class="apidocSignatureSpan">node-restful.</span>badRequest (errobj)](#apidoc.element.node-restful.badRequest)
- description and source-code
```javascript
badRequest = function (errobj) {
  return {
    status: 400,
    message: 'Bad Request',
    name: "BadRequest",
    errors: errobj || "Your request was invalid"
  };
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.node-restful.delete"></a>[function <span class="apidocSignatureSpan">node-restful.</span>delete (req, res, next)](#apidoc.element.node-restful.delete)
- description and source-code
```javascript
delete = function (req, res, next) {
  // Delete in 1 atomic operation on the database if not specified otherwise
  if (this.shouldUseAtomicUpdate) {
    req.quer.findOneAndRemove({}, this.delete_options, function(err, obj) {
      if (err) {
        exports.respond(res, 500, err);
      }
      exports.respondOrErr(res, 404, !obj && exports.objectNotFound(), 204, {});
      next();
    });
  } else {
    // Preform the remove in two steps allowing mongoose to fire its schema update hook
    req.quer.findOne({"_id": req.params.id}, function(err, docToRemove) {
      if (err) {
        exports.respond(res, 500, err);
      }
      var objNotFound = !docToRemove && exports.objectNotFound();
      if (objNotFound) {
        exports.respond(res, 404, objNotFound);
        return next();
      }

      docToRemove.remove(function (err, obj) {
        exports.respondOrErr(res, 400, err, 204, {});
        next();
      });
    });
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.node-restful.get"></a>[function <span class="apidocSignatureSpan">node-restful.</span>get (req, res, next)](#apidoc.element.node-restful.get)
- description and source-code
```javascript
get = function (req, res, next) {
  if (req.params.id && !mongoose.Types.ObjectId.isValid(req.params.id)) {
    exports.respond(res, 404, exports.objectNotFound());
    next();
  } else {
    req.quer.exec(function(err, list) {
      if (err) {
        exports.respond(res, 500, err);
      } else if (req.params.id) {
        exports.respondOrErr(res, 404, !list && exports.objectNotFound(), 200, (list && _.isArray(list)) ? list[0] : list);
      } else {
        exports.respondOrErr(res, 500, err, 200, list);
      }
      next();
    });
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.node-restful.getDetail"></a>[function <span class="apidocSignatureSpan">node-restful.</span>getDetail (req, res, next)](#apidoc.element.node-restful.getDetail)
- description and source-code
```javascript
getDetail = function (req, res, next) {
  req.quer.exec(function(err, one) {
    exports.respondOrErr(res, 500, err, 200, one);
    next();
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.node-restful.getPath"></a>[function <span class="apidocSignatureSpan">node-restful.</span>getPath (pathName)](#apidoc.element.node-restful.getPath)
- description and source-code
```javascript
getPath = function (pathName) {
  return function(req, res, next) {
    req.quer = req.quer.populate(pathName);
    req.quer.exec(function(err, one) {
      var errStatus = ((err && err.status) ? err.status : 500);
      exports.respondOrErr(res, errStatus, err, 200, (one && one.get(pathName)) || {});
      next();
    });
  };
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.node-restful.last"></a>[function <span class="apidocSignatureSpan">node-restful.</span>last (req, res, next)](#apidoc.element.node-restful.last)
- description and source-code
```javascript
last = function (req, res, next) {
  if (res.locals.bundle) {
    if (req.body.format === 'js') {
      return res.send(res.locals.bundle);
    } else if (req.body.format === 'html' || req.query.format === 'html') {
      return res.render(this.templateRoot + '/' + req.templatePath, res.locals.bundle);
    } else {
      return res.status(res.locals.status_code).json(res.locals.bundle);
    }
  }
  res.send();
}
```
- example usage
```shell
...
var handler = this.routes;
req.quer = this.filter(req.filters, req.body, req.query, this.Model.find({}));
req.templatePath = this.template(routes, req.filters);
routes.forEach(function(route) {
  if (route in handler) handler = handler[route];
  else if (!('all' in handler)) {
    handlers.respond(res, 404, handlers.respond404());
    handlers.last(req, res);
  }
});
if ('all' in handler) handler = handler.all;

if ('function' === typeof handler) {
  return handler.call(this, req, res, next);
}
...
```

#### <a name="apidoc.element.node-restful.model"></a>[function <span class="apidocSignatureSpan">node-restful.</span>model ()](#apidoc.element.node-restful.model)
- description and source-code
```javascript
function model() {
  var result = mongoose.model.apply(mongoose, arguments),
      default_properties = defaults();
  if (1 === arguments.length) return result;

  for (var key in default_properties) {
   result[key] = default_properties[key];
  }

  return result;
}
```
- example usage
```shell
...
app.use(bodyParser.urlencoded({'extended':'true'}));
app.use(bodyParser.json());
app.use(bodyParser.json({type:'application/vnd.api+json'}));
app.use(methodOverride());

mongoose.connect("mongodb://localhost/resources");

var Resource = app.resource = restful.model('resource', mongoose.Schema({
    title: String,
    year: Number,
  }))
  .methods(['get', 'post', 'put', 'delete']);

Resource.register(app, '/resources');
...
```

#### <a name="apidoc.element.node-restful.objectNotFound"></a>[function <span class="apidocSignatureSpan">node-restful.</span>objectNotFound ()](#apidoc.element.node-restful.objectNotFound)
- description and source-code
```javascript
objectNotFound = function () {
  return {
    status: 404,
    message: 'Object not found',
    name: 'ObjectNotFound',
    errors: {
      _id: {
        message: "Could not find object with specified attributes"
      }
    }
  };
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.node-restful.post"></a>[function <span class="apidocSignatureSpan">node-restful.</span>post (req, res, next)](#apidoc.element.node-restful.post)
- description and source-code
```javascript
post = function (req, res, next) {
  var obj = new this(req.body);
  obj.save(function(err) {
    exports.respondOrErr(res, 400, err, 201, obj);
    next();
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.node-restful.put"></a>[function <span class="apidocSignatureSpan">node-restful.</span>put (req, res, next)](#apidoc.element.node-restful.put)
- description and source-code
```javascript
put = function (req, res, next) {
  // Remove immutable ObjectId from update attributes to prevent request failure
  if (req.body._id && req.body._id === req.params.id) {
    delete req.body._id;
  }

  // Update in 1 atomic operation on the database if not specified otherwise
  if (this.shouldUseAtomicUpdate) {
    req.quer.findOneAndUpdate({}, req.body, this.update_options, function(err, newObj) {
      if (err) {
        exports.respond(res, 500, err);
      } else if (!newObj) {
        exports.respond(res, 404, exports.objectNotFound());
      } else {
        exports.respond(res, 200, newObj);
      }
      next();
    });
  } else {
    // Preform the update in two operations allowing mongoose to fire its schema update hook
    req.quer.findOne({"_id": req.params.id}, function(err, docToUpdate) {
      if (err) {
        exports.respond(res, 500, err);
      }
      var objNotFound = !docToUpdate && exports.objectNotFound();
      if (objNotFound) {
        exports.respond(res, 404, objNotFound);
        return next();
      }

      docToUpdate.set(req.body);
      docToUpdate.save(function (err, obj) {
        exports.respondOrErr(res, 400, err, 200, obj);
        next();
      });
    });
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.node-restful.respond"></a>[function <span class="apidocSignatureSpan">node-restful.</span>respond (res, statusCode, content)](#apidoc.element.node-restful.respond)
- description and source-code
```javascript
respond = function (res, statusCode, content) {
  res.locals.status_code = statusCode;
  res.locals.bundle = content;
}
```
- example usage
```shell
...
Model.prototype.send = function(routes, req, res, next) {
var handler = this.routes;
req.quer = this.filter(req.filters, req.body, req.query, this.Model.find({}));
req.templatePath = this.template(routes, req.filters);
routes.forEach(function(route) {
  if (route in handler) handler = handler[route];
  else if (!('all' in handler)) {
    handlers.respond(res, 404, handlers.respond404());
    handlers.last(req, res);
  }
});
if ('all' in handler) handler = handler.all;

if ('function' === typeof handler) {
  return handler.call(this, req, res, next);
...
```

#### <a name="apidoc.element.node-restful.respond404"></a>[function <span class="apidocSignatureSpan">node-restful.</span>respond404 ()](#apidoc.element.node-restful.respond404)
- description and source-code
```javascript
respond404 = function () {
  return {
    status: 404,
    message: 'Page Not Found',
    name: "PageNotFound",
    errors: 'Endpoint not found for model ' + this.modelName
  };
}
```
- example usage
```shell
...
Model.prototype.send = function(routes, req, res, next) {
var handler = this.routes;
req.quer = this.filter(req.filters, req.body, req.query, this.Model.find({}));
req.templatePath = this.template(routes, req.filters);
routes.forEach(function(route) {
  if (route in handler) handler = handler[route];
  else if (!('all' in handler)) {
    handlers.respond(res, 404, handlers.respond404());
    handlers.last(req, res);
  }
});
if ('all' in handler) handler = handler.all;

if ('function' === typeof handler) {
  return handler.call(this, req, res, next);
...
```

#### <a name="apidoc.element.node-restful.respondOrErr"></a>[function <span class="apidocSignatureSpan">node-restful.</span>respondOrErr (res, errStatusCode, err, statusCode, content)](#apidoc.element.node-restful.respondOrErr)
- description and source-code
```javascript
respondOrErr = function (res, errStatusCode, err, statusCode, content) {
  if (err) {
    exports.respond(res, errStatusCode, err);
  } else {
    exports.respond(res, statusCode, content);
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.node-restful.schema"></a>[function <span class="apidocSignatureSpan">node-restful.</span>schema (req, res, next)](#apidoc.element.node-restful.schema)
- description and source-code
```javascript
schema = function (req, res, next) {
  // We can mount a model to multiple apps, so we need to get the base url from the request url
  var baseuri = req.url.split('/');
  baseuri = baseuri.slice(0, baseuri.length - 1).join('/');
  var detailuri = baseuri + '/:id';
  exports.respond(res, 200, {
    resource: this.modelName,
    allowed_methods: Object.keys(this.allowed_methods),
    list_uri: baseuri,
    detail_uri: detailuri,
    fields: keep(this.schema.paths, ['regExp', 'path', 'instance', 'isRequired'])
  });
  next();
}
```
- example usage
```shell
n/a
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
