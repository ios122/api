## cljs.build.api/build



 <table border="1">
<tr>
<td>function</td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/0.0-3208"><img valign="middle" alt="[+] 0.0-3208" title="Added in 0.0-3208" src="https://img.shields.io/badge/+-0.0--3208-lightgrey.svg"></a> </td>
</tr>
</table>


 <samp>
(__build__ source opts)<br>
</samp>
 <samp>
(__build__ source opts compiler-env)<br>
</samp>

---





Source docstring:

```
Given a source which can be compiled, produce runnable JavaScript.
```


Source code @ [github](https://github.com/clojure/clojurescript/blob/r3264/src/main/clojure/cljs/build/api.clj#L116-L121):

```clj
(defn build
  ([source opts]
   (closure/build source opts))
  ([source opts compiler-env]
   (closure/build source opts compiler-env)))
```

<!--
Repo - tag - source tree - lines:

 <pre>
clojurescript @ r3264
└── src
    └── main
        └── clojure
            └── cljs
                └── build
                    └── <ins>[api.clj:116-121](https://github.com/clojure/clojurescript/blob/r3264/src/main/clojure/cljs/build/api.clj#L116-L121)</ins>
</pre>

-->

---



###### External doc links:

[`cljs.build.api/build` @ crossclj](http://crossclj.info/fun/cljs.build.api/build.html)<br>

---

 <table>
<tr><td>
<img valign="middle" align="right" width="48px" src="http://i.imgur.com/Hi20huC.png">
</td><td>
Created for the upcoming ClojureScript website.<br>
[edit here] | [learn how]
</td></tr></table>

[edit here]:https://github.com/cljsinfo/cljs-api-docs/blob/master/cljsdoc/cljs.build.api/build.cljsdoc
[learn how]:https://github.com/cljsinfo/cljs-api-docs/wiki/cljsdoc-files

<!--

This information was too distracting to show to readers, but I'll leave it
commented here since it is helpful to:

- pretty-print the data used to generate this document
- and show how to retrieve that data



The API data for this symbol:

```clj
{:ns "cljs.build.api",
 :name "build",
 :signature ["[source opts]" "[source opts compiler-env]"],
 :history [["+" "0.0-3208"]],
 :type "function",
 :full-name-encode "cljs.build.api/build",
 :source {:code "(defn build\n  ([source opts]\n   (closure/build source opts))\n  ([source opts compiler-env]\n   (closure/build source opts compiler-env)))",
          :title "Source code",
          :repo "clojurescript",
          :tag "r3264",
          :filename "src/main/clojure/cljs/build/api.clj",
          :lines [116 121]},
 :full-name "cljs.build.api/build",
 :docstring "Given a source which can be compiled, produce runnable JavaScript."}

```

Retrieve the API data for this symbol:

```clj
;; from Clojure REPL
(require '[clojure.edn :as edn])
(-> (slurp "https://raw.githubusercontent.com/cljsinfo/cljs-api-docs/catalog/cljs-api.edn")
    (edn/read-string)
    (get-in [:symbols "cljs.build.api/build"]))
```

-->