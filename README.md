Yarn incorrectly installs an additional version of Backbone for the `backbone-validation` package.

```
$ npm i
$ npm ls

├─┬ backbone@1.0.0
│ └── underscore@1.8.3
└── backbone-validation@0.9.1 (git://github.com/thedersen/backbone.validation.git#08d01da529549faa5fdadf5be4f46a823d8dc9a1)

$ rm -rf node_modules
$ yarn
$ npm ls

├── backbone@1.0.0
└─┬ backbone-validation@0.9.1 invalid
  ├── backbone@1.3.3 extraneous
  └── underscore@1.8.3
```

