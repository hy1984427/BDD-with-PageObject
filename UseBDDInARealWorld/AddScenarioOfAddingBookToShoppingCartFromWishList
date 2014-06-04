# Add scenario of adding book to shopping cart from wish list

Like other scenarios, we will add the scenario of adding book to shopping cart from wish list to "buy_book.feature" under "features" folder.

`cd features`

![alt text](https://raw.githubusercontent.com/hy1984427/BDD-with-PageObject/master/images/ChangeFolderToFeatures.png "Change folder to features")

Then we need to append following content to it.

<pre><code>@fromWishList
Scenario: Consumer can add a book to shopping cart from wish list
	Given I open "http://www.amazon.com"
	And I login as "bddwithpageobject@gmail.com" with "bddwithpageobject"
	When I search for "The Lean Startup"
	And I open the first book
	And I add the first book to Wish List
	And I add the first book to shopping cart from Wish List
	And I open my shopping cart
	Then I should see the book in my shopping cart
</pre></code>

![alt text](https://raw.githubusercontent.com/hy1984427/BDD-with-PageObject/master/images/BuyBookFromWishListFeatureFile.png "Add from wish list scenario into buy_book.feature")
