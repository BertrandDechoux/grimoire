### Example 0
[permalink](#example-0)

{% highlight clojure linenos %}
{% raw %}
user=> (drop -1 [1 2 3 4])
(1 2 3 4)

user=> (drop 0 [1 2 3 4])
(1 2 3 4)

user=> (drop 2 [1 2 3 4])
(3 4)

user=> (drop 5 [1 2 3 4])
(){% endraw %}
{% endhighlight %}


