## clojure.string/includes?



 <table border="1">
<tr>
<td>function</td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/1.7.145"><img valign="middle" alt="[+] 1.7.145" title="Added in 1.7.145" src="https://img.shields.io/badge/+-1.7.145-lightgrey.svg"></a> </td>
</tr>
</table>


 <samp>
(__includes?__ s substr)<br>
</samp>

---





Source docstring:

```
True if s includes substr.
```


Source code @ [github](https://github.com/clojure/clojurescript/blob/r1.7.166/src/main/cljs/clojure/string.cljs#L255-L258):

```clj
(defn ^boolean includes?
  [s substr]
  (gstring/contains s substr))
```

<!--
Repo - tag - source tree - lines:

 <pre>
clojurescript @ r1.7.166
└── src
    └── main
        └── cljs
            └── clojure
                └── <ins>[string.cljs:255-258](https://github.com/clojure/clojurescript/blob/r1.7.166/src/main/cljs/clojure/string.cljs#L255-L258)</ins>
</pre>

-->

---



###### External doc links:

[`clojure.string/includes?` @ crossclj](http://crossclj.info/fun/clojure.string.cljs/includes%3F.html)<br>

---

 <table>
<tr><td>
<img valign="middle" align="right" width="48px" src="http://i.imgur.com/Hi20huC.png">
</td><td>
Created for the upcoming ClojureScript website.<br>
[edit here] | [learn how]
</td></tr></table>

[edit here]:https://github.com/cljsinfo/cljs-api-docs/blob/master/cljsdoc/clojure.string/includesQMARK.cljsdoc
[learn how]:https://github.com/cljsinfo/cljs-api-docs/wiki/cljsdoc-files

<!--

This information was too distracting to show to readers, but I'll leave it
commented here since it is helpful to:

- pretty-print the data used to generate this document
- and show how to retrieve that data



The API data for this symbol:

```clj
{:return-type boolean,
 :ns "clojure.string",
 :name "includes?",
 :signature ["[s substr]"],
 :history [["+" "1.7.145"]],
 :type "function",
 :full-name-encode "clojure.string/includesQMARK",
 :source {:code "(defn ^boolean includes?\n  [s substr]\n  (gstring/contains s substr))",
          :title "Source code",
          :repo "clojurescript",
          :tag "r1.7.166",
          :filename "src/main/cljs/clojure/string.cljs",
          :lines [255 258]},
 :full-name "clojure.string/includes?",
 :docstring "True if s includes substr."}

```

Retrieve the API data for this symbol:

```clj
;; from Clojure REPL
(require '[clojure.edn :as edn])
(-> (slurp "https://raw.githubusercontent.com/cljsinfo/cljs-api-docs/catalog/cljs-api.edn")
    (edn/read-string)
    (get-in [:symbols "clojure.string/includes?"]))
```

-->