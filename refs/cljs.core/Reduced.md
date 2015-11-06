## cljs.core/Reduced



 <table border="1">
<tr>
<td>type</td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/0.0-1211"><img valign="middle" alt="[+] 0.0-1211" title="Added in 0.0-1211" src="https://img.shields.io/badge/+-0.0--1211-lightgrey.svg"></a> </td>
<td>
[<img height="24px" valign="middle" src="http://i.imgur.com/1GjPKvB.png"> <samp>clojure.lang/Reduced</samp>](https://github.com/clojure/clojure/blob//src/jvm/clojure/lang/Reduced.java)
</td>
</tr>
</table>


 <samp>
(__Reduced.__ val)<br>
</samp>

---







Source code @ [github](https://github.com/clojure/clojurescript/blob/r1820/src/cljs/cljs/core.cljs#L565-L567):

```clj
(deftype Reduced [val]
  IDeref
  (-deref [o] val))
```

<!--
Repo - tag - source tree - lines:

 <pre>
clojurescript @ r1820
└── src
    └── cljs
        └── cljs
            └── <ins>[core.cljs:565-567](https://github.com/clojure/clojurescript/blob/r1820/src/cljs/cljs/core.cljs#L565-L567)</ins>
</pre>

-->

---



###### External doc links:

[`clojure.lang/Reduced` @ clojuredocs](http://clojuredocs.org/clojure.lang/Reduced)<br>
[`clojure.lang/Reduced` @ grimoire](http://conj.io/store/v1/org.clojure/clojure/1.7.0-beta3/clj/clojure.lang/Reduced/)<br>
[`clojure.lang/Reduced` @ crossclj](http://crossclj.info/fun/clojure.lang/Reduced.html)<br>
[`cljs.core/Reduced` @ crossclj](http://crossclj.info/fun/cljs.core.cljs/Reduced.html)<br>

---

 <table>
<tr><td>
<img valign="middle" align="right" width="48px" src="http://i.imgur.com/Hi20huC.png">
</td><td>
Created for the upcoming ClojureScript website.<br>
[edit here] | [learn how]
</td></tr></table>

[edit here]:https://github.com/cljsinfo/cljs-api-docs/blob/master/cljsdoc/cljs.core/Reduced.cljsdoc
[learn how]:https://github.com/cljsinfo/cljs-api-docs/wiki/cljsdoc-files

<!--

This information was too distracting to show to readers, but I'll leave it
commented here since it is helpful to:

- pretty-print the data used to generate this document
- and show how to retrieve that data



The API data for this symbol:

```clj
{:ns "cljs.core",
 :name "Reduced",
 :signature ["[val]"],
 :history [["+" "0.0-1211"]],
 :type "type",
 :full-name-encode "cljs.core/Reduced",
 :source {:code "(deftype Reduced [val]\n  IDeref\n  (-deref [o] val))",
          :title "Source code",
          :repo "clojurescript",
          :tag "r1820",
          :filename "src/cljs/cljs/core.cljs",
          :lines [565 567]},
 :full-name "cljs.core/Reduced",
 :clj-symbol "clojure.lang/Reduced"}

```

Retrieve the API data for this symbol:

```clj
;; from Clojure REPL
(require '[clojure.edn :as edn])
(-> (slurp "https://raw.githubusercontent.com/cljsinfo/cljs-api-docs/catalog/cljs-api.edn")
    (edn/read-string)
    (get-in [:symbols "cljs.core/Reduced"]))
```

-->