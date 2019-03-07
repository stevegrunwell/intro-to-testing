### Regression tests

```php
function recentPostsHeading(array $posts)
{
    if (empty($posts)) {
        echo 'There have been no posts in the last 30 days.';
    } else {
        printf('%d posts in the last 30 days.', count($posts));
    }
}
```

<pre><output><span class="fragment highlight-green" data-fragment-index="1"><span class="fragment status-icon" data-fragment-index="1">&#x2714;</span> There have been no posts in the last 30 days.</span>
<span class="fragment highlight-red" data-fragment-index="1"><span class="fragment status-icon" data-fragment-index="1">&#x1D5EB;</span> 1 posts in the last 30 days.</span>
<span class="fragment highlight-green" data-fragment-index="1"><span class="fragment status-icon" data-fragment-index="1">&#x2714;</span> 2 posts in the last 30 days.</span></output></pre>
<!-- .element: class="fragment" data-fragment-index="0" -->

Note:

* Imagine we have this function, which renders a heading above a list of recent posts.
    - It looks like we might expect for 0 or 2 or more items
    - If $posts only has one post, we get the awkward and grammatically-incorrect "1 posts in the last 30 days."
