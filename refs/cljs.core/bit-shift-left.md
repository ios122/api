## cljs.core/bit-shift-left



 <table border="1">
<tr>
<td>function/macro</td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/0.0-927"><img valign="middle" alt="[+] 0.0-927" title="Added in 0.0-927" src="https://img.shields.io/badge/+-0.0--927-lightgrey.svg"></a> </td>
<td>
[<img height="24px" valign="middle" src="http://i.imgur.com/1GjPKvB.png"> <samp>clojure.core/bit-shift-left</samp>](http://clojure.github.io/clojure/branch-master/clojure.core-api.html#clojure.core/bit-shift-left)
</td>
</tr>
</table>


 <samp>
(__bit-shift-left__ x n)<br>
</samp>

---

Bitwise shift left `n` bits.  Same as `x << n` in JavaScript.



---

###### Examples:

Bits can be entered using radix notation:

```clj
(bit-shift-left 2r0101 1)
;;=> 10
;; 10 = 2r1010
```

Same numbers in decimal:

```clj
(bit-shift-left 5 1)
;;=> 10
```



---

###### See Also:

[`cljs.core/bit-shift-right`](../cljs.core/bit-shift-right.md)<br>

---


Source docstring:

```
Bitwise shift left
```


Function code @ [github](https://github.com/clojure/clojurescript/blob/r1820/src/cljs/cljs/core.cljs#L1659-L1661):

```clj
(defn bit-shift-left
  [x n] (cljs.core/bit-shift-left x n))
```

<!--
Repo - tag - source tree - lines:

 <pre>
clojurescript @ r1820
└── src
    └── cljs
        └── cljs
            └── <ins>[core.cljs:1659-1661](https://github.com/clojure/clojurescript/blob/r1820/src/cljs/cljs/core.cljs#L1659-L1661)</ins>
</pre>

-->

---

Macro code @ [github](https://github.com/clojure/clojurescript/blob/r1820/src/clj/cljs/core.clj#L438-L439):

```clj
(defmacro bit-shift-left [x n]
  (list 'js* "(~{} << ~{})" x n))
```

<!--
Repo - tag - source tree - lines:

 <pre>
clojurescript @ r1820
└── src
    └── clj
        └── cljs
            └── <ins>[core.clj:438-439](https://github.com/clojure/clojurescript/blob/r1820/src/clj/cljs/core.clj#L438-L439)</ins>
</pre>
-->

---


###### External doc links:

[`clojure.core/bit-shift-left` @ clojuredocs](http://clojuredocs.org/clojure.core/bit-shift-left)<br>
[`clojure.core/bit-shift-left` @ grimoire](http://conj.io/store/v1/org.clojure/clojure/1.7.0-beta3/clj/clojure.core/bit-shift-left/)<br>
[`clojure.core/bit-shift-left` @ crossclj](http://crossclj.info/fun/clojure.core/bit-shift-left.html)<br>
[`cljs.core/bit-shift-left` @ crossclj](http://crossclj.info/fun/cljs.core.cljs/bit-shift-left.html)<br>

---

 <table>
<tr><td>
<img valign="middle" align="right" width="48px" src="http://i.imgur.com/Hi20huC.png">
</td><td>
Created for the upcoming ClojureScript website.<br>
[edit here] | [learn how]
</td></tr></table>

[edit here]:https://github.com/cljsinfo/cljs-api-docs/blob/master/cljsdoc/cljs.core/bit-shift-left.cljsdoc
[learn how]:https://github.com/cljsinfo/cljs-api-docs/wiki/cljsdoc-files

<!--

This information was too distracting to show to readers, but I'll leave it
commented here since it is helpful to:

- pretty-print the data used to generate this document
- and show how to retrieve that data



The API data for this symbol:

```clj
{:description "Bitwise shift left `n` bits.  Same as `x << n` in JavaScript.",
 :ns "cljs.core",
 :name "bit-shift-left",
 :signature ["[x n]"],
 :history [["+" "0.0-927"]],
 :type "function/macro",
 :related ["cljs.core/bit-shift-right"],
 :full-name-encode "cljs.core/bit-shift-left",
 :source {:code "(defn bit-shift-left\n  [x n] (cljs.core/bit-shift-left x n))",
          :title "Function code",
          :repo "clojurescript",
          :tag "r1820",
          :filename "src/cljs/cljs/core.cljs",
          :lines [1659 1661]},
 :extra-sources [{:code "(defmacro bit-shift-left [x n]\n  (list 'js* \"(~{} << ~{})\" x n))",
                  :title "Macro code",
                  :repo "clojurescript",
                  :tag "r1820",
                  :filename "src/clj/cljs/core.clj",
                  :lines [438 439]}],
 :examples [{:id "67c34a",
             :content "Bits can be entered using radix notation:\n\n```clj\n(bit-shift-left 2r0101 1)\n;;=> 10\n;; 10 = 2r1010\n```\n\nSame numbers in decimal:\n\n```clj\n(bit-shift-left 5 1)\n;;=> 10\n```"}],
 :full-name "cljs.core/bit-shift-left",
 :clj-symbol "clojure.core/bit-shift-left",
 :docstring "Bitwise shift left"}

```

Retrieve the API data for this symbol:

```clj
;; from Clojure REPL
(require '[clojure.edn :as edn])
(-> (slurp "https://raw.githubusercontent.com/cljsinfo/cljs-api-docs/catalog/cljs-api.edn")
    (edn/read-string)
    (get-in [:symbols "cljs.core/bit-shift-left"]))
```

-->