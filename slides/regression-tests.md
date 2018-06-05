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

<pre><output>There have been no posts in the last 30 days
<span class="fragment highlight-red">1 posts in the last 30 days.</span>
2 posts in the last 30 days.</output></pre>
<!-- .element: class="fragment" -->

Note:

* Imagine we have this function, which renders a heading above a list of recent posts.
    - It looks like we might expect for 0 or 2 or more items
    - If $posts only has one post, we get the awkward and grammatically-incorrect "1 posts in the last 30 days."
