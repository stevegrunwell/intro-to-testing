### Behavior-Driven Development

* <!-- .element: class="fragment" --> Meant to be accessible to stakeholders
* <!-- .element: class="fragment" --> Describes behavior in plain language
        Given I am not an administrator
        When I visit "/admin"
        Then the response code should be 403

Note:

* BDD has similar goals, but focuses more on the behavior of the app
    - When I do X, Y should happen
* Idea of Gherkin is that stakeholders should be able to understand — and maybe even write — the tests
    - Given / When / Then
* Best for integration tests or above, with PHPUnit focused on unit tests
    - Behat
