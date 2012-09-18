# crate-bind

[Crate](https://github.com/ibdknox/crate) is a ClojureScript implementation of the awesome [Hiccup](https://github.com/weavejester/hiccup/) html templating library.

Crate-bind is modified version of Crate. With crate-bind you can easily bind elements into a hashmap.

## Usage

```clojure
(ns myapp
 (:require [crate-bind.core :as crateb]))

(crateb/build [:div])
=> {:el #<[object HTMLDivElement]>}

(crateb/build [:div
                [:span :date-el "2012/9/19"]
                [:a {:href "/foo"} :link-el "hello"]])
=> {:el #<[object HTMLDivElement]>,
    :link-el #<http://localhost:8080/foo>,
    :date-el #<[object HTMLSpanElement]>}

```

## License

Copyright (C) 2011 Chris Granger

Distributed under the Eclipse Public License, the same as Clojure.
