### Testdox

<pre><output class="hljs">$ ./vendor/bin/phpunit --testdox
PHPUnit 8.0.6 by Sebastian Bergmann and contributors.

Unit\Coffee
 <span class="pass">✔</span> Coffee should be large
 <span class="pass">✔</span> Coffee should be hot
 <span class="pass">✔</span> Coffee should be delicious
 <span class="fail">✘</span> Coffee should not have cream added to it
</output></pre>

Note:

When given the --testdox flag, PHPUnit can generate a really nice list that reads like a list of requirements.

The names are determined by the test method name, but can also be overridden via the `@testdox` docblock annotation.
