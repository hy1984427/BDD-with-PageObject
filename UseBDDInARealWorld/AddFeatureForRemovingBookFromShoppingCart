# Add feature for removing book from shopping cart

Like adding buying book feature, we are going to add "remove_book.feature" from shopping cart under "features" folder.

`cd features`

`touch remove_book.feature`

![alt text](https://raw.githubusercontent.com/hy1984427/BDD-with-PageObject/master/images/CreateRemoveBookFeature.png "Create remove_book.feature")

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
	And I remove the book from my shopping cart
	Then I should not see the book in my shopping cart
</pre></code>

![alt text](https://raw.githubusercontent.com/hy1984427/BDD-with-PageObject/master/images/RemoveBookFeatureFile.png "Edit remove_book.feature")
