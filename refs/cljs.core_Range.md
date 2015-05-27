## <img width="48px" valign="middle" src="http://i.imgur.com/Hi20huC.png"> cljs.core/Range

 <table border="1">
<tr>
<td>type</td>
<td><a href="https://github.com/cljsinfo/api-refs/tree/0.0-927"><img valign="middle" alt="[+] 0.0-927" src="https://img.shields.io/badge/+-0.0--927-lightgrey.svg"></a> </td>
</tr>
</table>

 <samp>
(__Range.__ meta start end step)<br>
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
            └── <ins>[core.cljs:2819-2874](https://github.com/clojure/clojurescript/blob/r1006/src/cljs/cljs/core.cljs#L2819-L2874)</ins>
</pre>

```clj
(deftype Range [meta start end step]
  IWithMeta
  (-with-meta [rng meta] (Range. meta start end step))

  IMeta
  (-meta [rng] meta)

  ISeq
  (-first [rng] start)
  (-rest [rng]
    (if (-seq rng)
      (Range. meta (+ start step) end step)
      (list)))

  ICollection
  (-conj [rng o] (cons o rng))

  IEmptyableCollection
  (-empty [rng] (with-meta cljs.core.List/EMPTY meta))

  ISequential
  IEquiv
  (-equiv [rng other] (equiv-sequential rng other))

  IHash
  (-hash [rng] (hash-coll rng))

  ICounted
  (-count [rng]
    (if-not (-seq rng)
      0
      (js/Math.ceil (/ (- end start) step))))

  IIndexed
  (-nth [rng n]
    (if (< n (-count rng))
      (+ start (* n step))
      (if (and (> start end) (= step 0))
        start
        (throw (js/Error. "Index out of bounds")))))
  (-nth [rng n not-found]
    (if (< n (-count rng))
      (+ start (* n step))
      (if (and (> start end) (= step 0))
        start
        not-found)))

  ISeqable
  (-seq [rng]
    (let [comp (if (pos? step) < >)]
      (when (comp start end)
        rng)))

  IReduce
  (-reduce [rng f] (ci-reduce rng f))
  (-reduce [rng f s] (ci-reduce rng f s)))
```


---

```clj
{:full-name "cljs.core/Range",
 :ns "cljs.core",
 :name "Range",
 :type "type",
 :signature ["[meta start end step]"],
 :source {:code "(deftype Range [meta start end step]\n  IWithMeta\n  (-with-meta [rng meta] (Range. meta start end step))\n\n  IMeta\n  (-meta [rng] meta)\n\n  ISeq\n  (-first [rng] start)\n  (-rest [rng]\n    (if (-seq rng)\n      (Range. meta (+ start step) end step)\n      (list)))\n\n  ICollection\n  (-conj [rng o] (cons o rng))\n\n  IEmptyableCollection\n  (-empty [rng] (with-meta cljs.core.List/EMPTY meta))\n\n  ISequential\n  IEquiv\n  (-equiv [rng other] (equiv-sequential rng other))\n\n  IHash\n  (-hash [rng] (hash-coll rng))\n\n  ICounted\n  (-count [rng]\n    (if-not (-seq rng)\n      0\n      (js/Math.ceil (/ (- end start) step))))\n\n  IIndexed\n  (-nth [rng n]\n    (if (< n (-count rng))\n      (+ start (* n step))\n      (if (and (> start end) (= step 0))\n        start\n        (throw (js/Error. \"Index out of bounds\")))))\n  (-nth [rng n not-found]\n    (if (< n (-count rng))\n      (+ start (* n step))\n      (if (and (> start end) (= step 0))\n        start\n        not-found)))\n\n  ISeqable\n  (-seq [rng]\n    (let [comp (if (pos? step) < >)]\n      (when (comp start end)\n        rng)))\n\n  IReduce\n  (-reduce [rng f] (ci-reduce rng f))\n  (-reduce [rng f s] (ci-reduce rng f s)))",
          :filename "clojurescript/src/cljs/cljs/core.cljs",
          :lines [2819 2874],
          :link "https://github.com/clojure/clojurescript/blob/r1006/src/cljs/cljs/core.cljs#L2819-L2874"},
 :full-name-encode "cljs.core_Range",
 :history [["+" "0.0-927"]]}

```