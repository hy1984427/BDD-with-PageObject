# Update remove_book.rb

And we need to update the content in "remove_book.rb" as following:

<pre><code># encoding: utf-8
When /^I remove the book from my shopping cart$/ do
	@itemdetails.openShoppingCart
	@shoppingcart.removeTheFirstItem
end

Then /^I should not see the book in my shopping cart$/ do
	@shoppingcart.verifyItemRemovedFromShoppingCart
	@shoppingcart.verifyItemRemovedNotShownInShoppingCart
end
</pre></code>

![alt text](https://raw.githubusercontent.com/hy1984427/BDD-with-PageObject/master/images/UpdateRemoveBookRB.png "Update remove_book.rb")
