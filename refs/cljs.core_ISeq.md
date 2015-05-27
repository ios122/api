## <img width="48px" valign="middle" src="http://i.imgur.com/Hi20huC.png"> cljs.core/ISeq

 <table border="1">
<tr>
<td>protocol</td>
<td><a href="https://github.com/cljsinfo/api-refs/tree/0.0-927"><img valign="middle" alt="[+] 0.0-927" src="https://img.shields.io/badge/+-0.0--927-lightgrey.svg"></a> </td>
</tr>
</table>

 <samp>
</samp>

```
(no docstring)
```

---

 <pre>
clojurescript @ r1006
└── src
    └── cljs
        └── cljs
            └── <ins>[core.cljs:133-135](https://github.com/clojure/clojurescript/blob/r1006/src/cljs/cljs/core.cljs#L133-L135)</ins>
</pre>

```clj
(defprotocol ISeq
  (-first [coll])
  (-rest [coll]))
```


---

```clj
{:ns "cljs.core",
 :name "ISeq",
 :type "protocol",
 :full-name-encode "cljs.core_ISeq",
 :source {:code "(defprotocol ISeq\n  (-first [coll])\n  (-rest [coll]))",
          :filename "clojurescript/src/cljs/cljs/core.cljs",
          :lines [133 135],
          :link "https://github.com/clojure/clojurescript/blob/r1006/src/cljs/cljs/core.cljs#L133-L135"},
 :methods [{:name "-first", :signature ["[coll]"], :docstring nil}
           {:name "-rest", :signature ["[coll]"], :docstring nil}],
 :full-name "cljs.core/ISeq",
 :history [["+" "0.0-927"]]}

```