## cljs.reader/\*tag-table\*



 <table border="1">
<tr>
<td>var</td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/0.0-1236"><img valign="middle" alt="[+] 0.0-1236" title="Added in 0.0-1236" src="https://img.shields.io/badge/+-0.0--1236-lightgrey.svg"></a> </td>
</tr>
</table>









Source code @ [github](https://github.com/clojure/clojurescript/blob/r1820/src/cljs/cljs/reader.cljs#L526-L528):

```clj
(def *tag-table* (atom {"inst"  read-date
                        "uuid"  read-uuid
                        "queue" read-queue}))
```

<!--
Repo - tag - source tree - lines:

 <pre>
clojurescript @ r1820
└── src
    └── cljs
        └── cljs
            └── <ins>[reader.cljs:526-528](https://github.com/clojure/clojurescript/blob/r1820/src/cljs/cljs/reader.cljs#L526-L528)</ins>
</pre>

-->

---



###### External doc links:

[`cljs.reader/*tag-table*` @ crossclj](http://crossclj.info/fun/cljs.reader.cljs/*tag-table*.html)<br>

---

 <table>
<tr><td>
<img valign="middle" align="right" width="48px" src="http://i.imgur.com/Hi20huC.png">
</td><td>
Created for the upcoming ClojureScript website.<br>
[edit here] | [learn how]
</td></tr></table>

[edit here]:https://github.com/cljsinfo/cljs-api-docs/blob/master/cljsdoc/cljs.reader/STARtag-tableSTAR.cljsdoc
[learn how]:https://github.com/cljsinfo/cljs-api-docs/wiki/cljsdoc-files

<!--

This information was too distracting to show to readers, but I'll leave it
commented here since it is helpful to:

- pretty-print the data used to generate this document
- and show how to retrieve that data



The API data for this symbol:

```clj
{:ns "cljs.reader",
 :name "*tag-table*",
 :type "var",
 :source {:code "(def *tag-table* (atom {\"inst\"  read-date\n                        \"uuid\"  read-uuid\n                        \"queue\" read-queue}))",
          :title "Source code",
          :repo "clojurescript",
          :tag "r1820",
          :filename "src/cljs/cljs/reader.cljs",
          :lines [526 528]},
 :full-name "cljs.reader/*tag-table*",
 :full-name-encode "cljs.reader/STARtag-tableSTAR",
 :history [["+" "0.0-1236"]]}

```

Retrieve the API data for this symbol:

```clj
;; from Clojure REPL
(require '[clojure.edn :as edn])
(-> (slurp "https://raw.githubusercontent.com/cljsinfo/cljs-api-docs/catalog/cljs-api.edn")
    (edn/read-string)
    (get-in [:symbols "cljs.reader/*tag-table*"]))
```

-->