### Example 0
[permalink](#example-0)

{% highlight clojure linenos %}
{% raw %}
user=> (take-last 2 [1 2 3 4])
(3 4)

user=> (take-last 2 [4])
(4)

user=> (take-last 2 [])
nil

user=> (take-last 2 nil)
nil{% endraw %}
{% endhighlight %}


