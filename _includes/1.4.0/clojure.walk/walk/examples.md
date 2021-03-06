### Example 0
[permalink](#example-0)

{% highlight clojure linenos %}
{% raw %}
(use 'clojure.walk)

user=> (walk #(* 2 %) #(apply + %) [1 2 3 4 5])
30

user=> (walk second #(apply max %) [ [1 2] [3 4] [5 6] ])
6

user=> (walk first #(apply max %) [ [1 2] [3 4] [5 6] ])
5

user=> (walk first reverse [ [1 2] [3 4] [5 6] ])
(5 3 1){% endraw %}
{% endhighlight %}


### Example 1
[permalink](#example-1)

{% highlight clojure linenos %}
{% raw %}
(require '[clojure.walk :as w])

user=> (w/walk (fn [[k v]] [k (* 10 v)]) identity {:a 1 :b 2 :c 3})
{:a 10, :c 30, :b 20}

user=> (w/postwalk #(if (number? %) (* 2 %) %) [[1 2 3] [4 7 2] [2 5 2]])
[[2 4 6] [8 14 4] [4 10 4]]

user=> (let [s [1 '(2 3 [1])]]
         (w/postwalk #(if (seq? %) (vec %) %) s))
[1 [2 3 [1]]]

user=> (w/walk (comp vec reverse) identity {0 :start 1 :inprogress 2 :end})
{:start 0, :inprogress 1, :end 2}{% endraw %}
{% endhighlight %}


