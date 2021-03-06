### Test Doubles

<dl>
    <dt>Dummy</dt>
    <dd>Does nothing but satisfy requirements</dd>
    <dt>Fake</dt>
    <dd>Implementation of the contract for testing only</dd>
</dl>

[Jessica Mauerhan's excellent post on test doubles](https://jmauerhan.wordpress.com/2018/10/04/the-5-types-of-test-doubles-and-how-to-create-them-in-phpunit/)

Note:

* Dummies are useful if you need to satisfy type-hinted dependencies
* Fakes are implementations of systems for testing only
    - Think of a logger that writes logs to an array you can later analyze
    - Writing to SQLite during testing instead of the production database engine
* The Five Types of Test Doubles & How to Create Them in PHPUnit
* Larry Garfield pointed out at Midwest PHP that a lot of times these can be a little fuzzy, so treat them as guidelines rather than hard-and-fast rules.
