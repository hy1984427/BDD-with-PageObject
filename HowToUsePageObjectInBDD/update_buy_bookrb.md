# Update buy_book.rb

We also need to mofidy "buy_book.rb" again as following:

`cd ../step_definitions/`

![alt text](https://raw.githubusercontent.com/hy1984427/BDD-with-PageObject/master/images/ChangeFolderToStepDefinitionsAgain.png "Change folder to features/step_definitions")

<pre><code># encoding: utf-8
Given /^I open "(.*?)"$/ do |site|
	@home.openSite (site)
end

And /^I login as "(.*?)" with "(.*?)"$/ do |username,password|
	@login.loginAs(username,password)
end

When /^I search for "(.*?)"$/ do |keyword|
	@page.searchByKeyword (keyword)
end

And /^I open the first book$/ do
	@searchresult.openTheFirstItemInSearchResult
end

And /^I add the first book to Wish List$/ do
	@itemdetails.getCurrentItemTitle
	@itemdetails.addToWishList
end

And /^I add the first book to shopping cart$/ do
	@itemdetails.getCurrentItemTitle
	@itemdetails.addToShoppingCart
end

And /^I add the first book to shopping cart from Wish List$/ do
	@itemdetails.openWishList
	@wishlist.addToShoppingCartFromWishList
end

And /^I open my shopping cart$/ do
	@wishlist.openShoppingCart
end

Then /^I should see the book in my shopping cart$/ do
	@shoppingcart.verifyItemAddedToShoppingCart
	@shoppingcart.verifyItemAddedShownInShoppingCart
end
</pre></code>

![alt text](https://raw.githubusercontent.com/hy1984427/BDD-with-PageObject/master/images/UpdateBuyBookRB.png "Update buy_book.rb")
