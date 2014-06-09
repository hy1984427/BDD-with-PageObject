# Extract the step of verifying item in shopping cart into methods

Let's package the step of verifying item in shopping cart into methods: `verifyItemAddedToShoppingCart` and `verifyItemAddedShownInShoppingCart` in "buy_book.rb". An it should look like:

<pre><code>Then /^I should see the book in my shopping cart$/ do
    verifyItemAddedToShoppingCart
    verifyItemAddedShownInShoppingCart
end

def verifyItemAddedToShoppingCart
	confirm=@driver.find_element :id => "confirm-text"
	confirm.text.include?("1 item added to Cart")
end

def verifyItemAddedShownInShoppingCart
	book=@driver.find_element :xpath => "//div[@class=\"a-row a-size-base word-break\"]/a"
	book.attribute("title").should == @bookTitle
end
</pre></code>

![alt text](https://raw.githubusercontent.com/hy1984427/BDD-with-PageObject/master/images/ExtractVerifyingItemInShoppingCart.png "Extract verifyItemInShoppingCart into methods")
