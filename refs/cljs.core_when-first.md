## <img width="48px" valign="middle" src="http://i.imgur.com/Hi20huC.png"> cljs.core/when-first

 <table border="1">
<tr>
<td>macro</td>
<td><a href="https://github.com/cljsinfo/api-refs/tree/0.0-927"><img valign="middle" alt="[+] 0.0-927" src="https://img.shields.io/badge/+-0.0--927-lightgrey.svg"></a> </td>
<td>
imported [<img height="24px" valign="middle" src="http://i.imgur.com/1GjPKvB.png"> <samp>clojure.core/when-first</samp>](http://clojure.github.io/clojure/branch-master/clojure.core-api.html#clojure.core/when-first)
</td>
</tr>
</table>

 <samp>
(__when-first__ bindings & body)<br>
</samp>

```
bindings => x xs

Same as (when (seq xs) (let [x (first xs)] body))
```

---

 <pre>
clojure @ clojure-1.3.0
└── src
    └── clj
        └── clojure
            └── <ins>[core.clj:4050-4062](https://github.com/clojure/clojure/blob/clojure-1.3.0/src/clj/clojure/core.clj#L4050-L4062)</ins>
</pre>

```clj
(defmacro when-first
  [bindings & body]
  (assert-args when-first
     (vector? bindings) "a vector for its binding"
     (= 2 (count bindings)) "exactly 2 forms in binding vector")
  (let [[x xs] bindings]
    `(when (seq ~xs)
       (let [~x (first ~xs)]
         ~@body))))
```


---

```clj
{:ns "cljs.core",
 :name "when-first",
 :signature ["[bindings & body]"],
 :history [["+" "0.0-927"]],
 :type "macro",
 :full-name-encode "cljs.core_when-first",
 :source {:code "(defmacro when-first\n  [bindings & body]\n  (assert-args when-first\n     (vector? bindings) \"a vector for its binding\"\n     (= 2 (count bindings)) \"exactly 2 forms in binding vector\")\n  (let [[x xs] bindings]\n    `(when (seq ~xs)\n       (let [~x (first ~xs)]\n         ~@body))))",
          :filename "clojure/src/clj/clojure/core.clj",
          :lines [4050 4062],
          :link "https://github.com/clojure/clojure/blob/clojure-1.3.0/src/clj/clojure/core.clj#L4050-L4062"},
 :full-name "cljs.core/when-first",
 :clj-symbol "clojure.core/when-first",
 :docstring "bindings => x xs\n\nSame as (when (seq xs) (let [x (first xs)] body))"}

```