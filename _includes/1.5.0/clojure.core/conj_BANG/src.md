{% highlight clojure linenos %}
(defn conj!
  "Alpha - subject to change.
  Adds x to the transient collection, and return coll. The 'addition'
  may happen at different 'places' depending on the concrete type."
  {:added "1.1"
   :static true}
  [^clojure.lang.ITransientCollection coll x]
  (.conj coll x))
{% endhighlight %}
