## fn\*



 <table border="1">
<tr>
<td>special form</td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/0.0-927"><img valign="middle" alt="[+] 0.0-927" title="Added in 0.0-927" src="https://img.shields.io/badge/+-0.0--927-lightgrey.svg"></a> </td>
</tr>
</table>









Parser code @ [github](https://github.com/clojure/clojurescript/blob/r1820/src/clj/cljs/analyzer.clj#L390-L442):

```clj
(defmethod parse 'fn*
  [op env [_ & args :as form] name]
  (let [[name meths] (if (symbol? (first args))
                       [(first args) (next args)]
                       [name (seq args)])
        ;;turn (fn [] ...) into (fn ([]...))
        meths (if (vector? (first meths)) (list meths) meths)
        locals (:locals env)
        locals (if (and locals name) (assoc locals name {:name name :shadow (locals name)}) locals)
        type (-> form meta ::type)
        fields (-> form meta ::fields)
        protocol-impl (-> form meta :protocol-impl)
        protocol-inline (-> form meta :protocol-inline)
        locals (reduce (fn [m fld]
                         (assoc m fld
                                {:name fld
                                 :line (get-line fld env)
                                 :column (get-col fld env)
                                 :field true
                                 :mutable (-> fld meta :mutable)
                                 :unsynchronized-mutable (-> fld meta :unsynchronized-mutable)
                                 :volatile-mutable (-> fld meta :volatile-mutable)
                                 :tag (-> fld meta :tag)
                                 :shadow (m fld)}))
                       locals fields)

        menv (if (> (count meths) 1) (assoc env :context :expr) env)
        menv (merge menv
               {:protocol-impl protocol-impl
                :protocol-inline protocol-inline})
        methods (map #(analyze-fn-method menv locals % type) meths)
        max-fixed-arity (apply max (map :max-fixed-arity methods))
        variadic (boolean (some :variadic methods))
        locals (if name
                 (update-in locals [name] assoc
                            :fn-var true
                            :variadic variadic
                            :max-fixed-arity max-fixed-arity
                            :method-params (map :params methods))
                 locals)
        methods (if name
                  ;; a second pass with knowledge of our function-ness/arity
                  ;; lets us optimize self calls
                  (no-warn (doall (map #(analyze-fn-method menv locals % type) meths)))
                  methods)]
    ;;todo - validate unique arities, at most one variadic, variadic takes max required args
    {:env env :op :fn :form form :name name :methods methods :variadic variadic
     :recur-frames *recur-frames* :loop-lets *loop-lets*
     :jsdoc [(when variadic "@param {...*} var_args")]
     :max-fixed-arity max-fixed-arity
     :protocol-impl protocol-impl
     :protocol-inline protocol-inline
     :children (mapv :expr methods)}))
```

<!--
Repo - tag - source tree - lines:

 <pre>
clojurescript @ r1820
└── src
    └── clj
        └── cljs
            └── <ins>[analyzer.clj:390-442](https://github.com/clojure/clojurescript/blob/r1820/src/clj/cljs/analyzer.clj#L390-L442)</ins>
</pre>

-->

---




 <table>
<tr><td>
<img valign="middle" align="right" width="48px" src="http://i.imgur.com/Hi20huC.png">
</td><td>
Created for the upcoming ClojureScript website.<br>
[edit here] | [learn how]
</td></tr></table>

[edit here]:https://github.com/cljsinfo/cljs-api-docs/blob/master/cljsdoc/special/fnSTAR.cljsdoc
[learn how]:https://github.com/cljsinfo/cljs-api-docs/wiki/cljsdoc-files

<!--

This information was too distracting to show to readers, but I'll leave it
commented here since it is helpful to:

- pretty-print the data used to generate this document
- and show how to retrieve that data



The API data for this symbol:

```clj
{:ns "special",
 :name "fn*",
 :type "special form",
 :source {:code "(defmethod parse 'fn*\n  [op env [_ & args :as form] name]\n  (let [[name meths] (if (symbol? (first args))\n                       [(first args) (next args)]\n                       [name (seq args)])\n        ;;turn (fn [] ...) into (fn ([]...))\n        meths (if (vector? (first meths)) (list meths) meths)\n        locals (:locals env)\n        locals (if (and locals name) (assoc locals name {:name name :shadow (locals name)}) locals)\n        type (-> form meta ::type)\n        fields (-> form meta ::fields)\n        protocol-impl (-> form meta :protocol-impl)\n        protocol-inline (-> form meta :protocol-inline)\n        locals (reduce (fn [m fld]\n                         (assoc m fld\n                                {:name fld\n                                 :line (get-line fld env)\n                                 :column (get-col fld env)\n                                 :field true\n                                 :mutable (-> fld meta :mutable)\n                                 :unsynchronized-mutable (-> fld meta :unsynchronized-mutable)\n                                 :volatile-mutable (-> fld meta :volatile-mutable)\n                                 :tag (-> fld meta :tag)\n                                 :shadow (m fld)}))\n                       locals fields)\n\n        menv (if (> (count meths) 1) (assoc env :context :expr) env)\n        menv (merge menv\n               {:protocol-impl protocol-impl\n                :protocol-inline protocol-inline})\n        methods (map #(analyze-fn-method menv locals % type) meths)\n        max-fixed-arity (apply max (map :max-fixed-arity methods))\n        variadic (boolean (some :variadic methods))\n        locals (if name\n                 (update-in locals [name] assoc\n                            :fn-var true\n                            :variadic variadic\n                            :max-fixed-arity max-fixed-arity\n                            :method-params (map :params methods))\n                 locals)\n        methods (if name\n                  ;; a second pass with knowledge of our function-ness/arity\n                  ;; lets us optimize self calls\n                  (no-warn (doall (map #(analyze-fn-method menv locals % type) meths)))\n                  methods)]\n    ;;todo - validate unique arities, at most one variadic, variadic takes max required args\n    {:env env :op :fn :form form :name name :methods methods :variadic variadic\n     :recur-frames *recur-frames* :loop-lets *loop-lets*\n     :jsdoc [(when variadic \"@param {...*} var_args\")]\n     :max-fixed-arity max-fixed-arity\n     :protocol-impl protocol-impl\n     :protocol-inline protocol-inline\n     :children (mapv :expr methods)}))",
          :title "Parser code",
          :repo "clojurescript",
          :tag "r1820",
          :filename "src/clj/cljs/analyzer.clj",
          :lines [390 442]},
 :full-name "special/fn*",
 :full-name-encode "special/fnSTAR",
 :history [["+" "0.0-927"]]}

```

Retrieve the API data for this symbol:

```clj
;; from Clojure REPL
(require '[clojure.edn :as edn])
(-> (slurp "https://raw.githubusercontent.com/cljsinfo/cljs-api-docs/catalog/cljs-api.edn")
    (edn/read-string)
    (get-in [:symbols "special/fn*"]))
```

-->