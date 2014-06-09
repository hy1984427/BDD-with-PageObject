# Add feature for buying book

Like the sample in last chapter, we need to add "buy_book.feature" under "features" folder.

`cd features`

`touch buy_book.feature`

![alt text](https://raw.githubusercontent.com/hy1984427/BDD-with-PageObject/master/images/CreateBuyBookFeature.png "Create buy_book.feature")

Then we need to add following content to it.

<pre><code>Feature:
In order to purchase it later
As a consumer
I want to add a book to my shopping cart

Scenario: Consumer can add a book to shopping cart
	Given I open "http://www.amazon.com"
    When I search for "The Lean Startup"
    And I open the first book
	And I add the first book to shopping cart
	Then I should see the book in my shopping cart
</pre></code>

![alt text](https://raw.githubusercontent.com/hy1984427/BDD-with-PageObject/master/images/BuyBookFeatureFile.png "Edit buy_book.feature")
