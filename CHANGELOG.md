# Sourcery CHANGELOG

---

## master

### Bug Fixes

* Fixes a bug with flattening `inherits`, `implements` for protocols implementing other protocols
* Improve `rawType` logic for Enums

### New Features

* Annotations can now be declared also with sections e.g. `sourcery:begin: attribute1, attribute2 = 234`
* Adds scanning class variables as static

### Internal changes

* Refactored models
* Improved performance of annotation scanning

## 0.4.1

### New Features

* Implements inherits, implements, based reflection on each Type
* Flattens inheritance, e.g. Foo implements Decodable, then FooSubclass also implements it

### Internal changes

* Stop parsing private variables as they wouldn't be accessible to code-generated code

## 0.4.0

### New Features

* improve detecting raw type
* add `isGeneric` property

## 0.3.9

### New Features

* Enables support for scanning extensions of unknown type, providing partial metadata via types.based or types.all reflection

## 0.3.8
### New Features

* Adds real type reflection into Variable, not only it's name
* Resolves known typealiases

## 0.3.7
### Bug Fixes

* Fixes a bug that caused Sourcery to drop previous type information when encountering generated code, closes #33

## 0.3.6
### Bug Fixes

* Fixes bug in escaping path
* Fixes missing protocol variant in kind


## 0.3.5

### New Features
* added support for type/variable source annotations
* added property kind to Type, it contains info whether this is struct, class or enum entry
* Automatically skips .swift files that were generated with Sourcery

### Internal changes

* improved detecting enums with rawType