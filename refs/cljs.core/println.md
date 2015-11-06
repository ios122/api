## cljs.core/println



 <table border="1">
<tr>
<td>function</td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/0.0-927"><img valign="middle" alt="[+] 0.0-927" title="Added in 0.0-927" src="https://img.shields.io/badge/+-0.0--927-lightgrey.svg"></a> </td>
<td>
[<img height="24px" valign="middle" src="http://i.imgur.com/1GjPKvB.png"> <samp>clojure.core/println</samp>](http://clojure.github.io/clojure/branch-master/clojure.core-api.html#clojure.core/println)
</td>
</tr>
</table>


 <samp>
(__println__ & objs)<br>
</samp>

---





Source docstring:

```
Same as print followed by (newline)
```


Source code @ [github](https://github.com/clojure/clojurescript/blob/r1820/src/cljs/cljs/core.cljs#L6675-L6679):

```clj
(defn println
  [& objs]
  (pr-with-opts objs (assoc (pr-opts) :readably false))
  (newline (pr-opts)))
```

<!--
Repo - tag - source tree - lines:

 <pre>
clojurescript @ r1820
└── src
    └── cljs
        └── cljs
            └── <ins>[core.cljs:6675-6679](https://github.com/clojure/clojurescript/blob/r1820/src/cljs/cljs/core.cljs#L6675-L6679)</ins>
</pre>

-->

---



###### External doc links:

[`clojure.core/println` @ clojuredocs](http://clojuredocs.org/clojure.core/println)<br>
[`clojure.core/println` @ grimoire](http://conj.io/store/v1/org.clojure/clojure/1.7.0-beta3/clj/clojure.core/println/)<br>
[`clojure.core/println` @ crossclj](http://crossclj.info/fun/clojure.core/println.html)<br>
[`cljs.core/println` @ crossclj](http://crossclj.info/fun/cljs.core.cljs/println.html)<br>

---

 <table>
<tr><td>
<img valign="middle" align="right" width="48px" src="http://i.imgur.com/Hi20huC.png">
</td><td>
Created for the upcoming ClojureScript website.<br>
[edit here] | [learn how]
</td></tr></table>

[edit here]:https://github.com/cljsinfo/cljs-api-docs/blob/master/cljsdoc/cljs.core/println.cljsdoc
[learn how]:https://github.com/cljsinfo/cljs-api-docs/wiki/cljsdoc-files

<!--

This information was too distracting to show to readers, but I'll leave it
commented here since it is helpful to:

- pretty-print the data used to generate this document
- and show how to retrieve that data



The API data for this symbol:

```clj
{:ns "cljs.core",
 :name "println",
 :signature ["[& objs]"],
 :history [["+" "0.0-927"]],
 :type "function",
 :full-name-encode "cljs.core/println",
 :source {:code "(defn println\n  [& objs]\n  (pr-with-opts objs (assoc (pr-opts) :readably false))\n  (newline (pr-opts)))",
          :title "Source code",
          :repo "clojurescript",
          :tag "r1820",
          :filename "src/cljs/cljs/core.cljs",
          :lines [6675 6679]},
 :full-name "cljs.core/println",
 :clj-symbol "clojure.core/println",
 :docstring "Same as print followed by (newline)"}

```

Retrieve the API data for this symbol:

```clj
;; from Clojure REPL
(require '[clojure.edn :as edn])
(-> (slurp "https://raw.githubusercontent.com/cljsinfo/cljs-api-docs/catalog/cljs-api.edn")
    (edn/read-string)
    (get-in [:symbols "cljs.core/println"]))
```

-->