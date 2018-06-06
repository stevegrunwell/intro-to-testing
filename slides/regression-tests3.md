### Regression tests

<pre class="fragment-replacement"><code class="hljs lang-php fragment fade-out" data-fragment-index="0">function recentPostsHeading(array $posts)
{
    if (empty($posts)) {
        echo 'There have been no posts in the last 30 days.';
    } else {
        printf('%d posts in the last 30 days.', count($posts));
    }
}</code><code class="hljs lang-php fragment fade-in" data-fragment-index="0">function recentPostsHeading(array $posts)
{
    if (empty($posts)) {
        echo 'There have been no posts in the last 30 days.';
    } elseif (1 === count($posts)) {
        echo 'One post in the last 30 days.';
    } else {
        printf('%d posts in the last 30 days.', count($posts));
    }
}</code></pre>

<pre><output>There have been no posts in the last 30 days
<span style="color: #D8000C;" class="fragment highlight-green" data-fragment-index="0">One post in the last 30 days.</span>
2 posts in the last 30 days.</output></pre>

Note:

* When we run our test, we start in a red state
* Our tests help push us towards another conditional, which makes our new test pass (green)
* If this function changes in the future, our test will break, alerting us to a regression
