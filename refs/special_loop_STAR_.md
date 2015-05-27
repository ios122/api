## <img width="48px" valign="middle" src="http://i.imgur.com/Hi20huC.png"> special/loop\*

 <table border="1">
<tr>
<td>special form</td>
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
    └── clj
        └── cljs
            └── <ins>[compiler.clj:798-800](https://github.com/clojure/clojurescript/blob/r1006/src/clj/cljs/compiler.clj#L798-L800)</ins>
</pre>

```clj
(defmethod parse 'loop*
  [op encl-env form _]
  (analyze-let encl-env form true))
```


---

```clj
{:full-name "special/loop*",
 :ns "special",
 :name "loop*",
 :type "special form",
 :source {:code "(defmethod parse 'loop*\n  [op encl-env form _]\n  (analyze-let encl-env form true))",
          :filename "clojurescript/src/clj/cljs/compiler.clj",
          :lines [798 800],
          :link "https://github.com/clojure/clojurescript/blob/r1006/src/clj/cljs/compiler.clj#L798-L800"},
 :full-name-encode "special_loop_STAR_",
 :history [["+" "0.0-927"]]}

```