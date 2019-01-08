### Behat (Gherkin)

<ul>
    <li class="fragment" data-fragment-index="0">Meant to be accessible to stakeholders</li>
    <li class="fragment" data-fragment-index="1">Describes behavior in plain language<pre><output class="hljs">Given I am not an administrator        <span class="hljs-comment fragment" data-fragment-index="2"># Arrange</span>
When I visit <span class="hljs-string">"/admin"</span>                  <span class="hljs-comment fragment" data-fragment-index="2"># Act</span>
Then the response code should be 403   <span class="hljs-comment fragment" data-fragment-index="2"># Assert</span></output></pre></li>
</ul>

Note:

* Another form of testing, more popular in BDD as it's focused on the overall behavior of the app
* Idea is that stakeholders should be able to understand — and maybe even write — the tests
    - Given / When / Then
    - Arrange / Act / Assert
* Best for integration tests or above, with PHPUnit focused on unit tests
    - Behat
