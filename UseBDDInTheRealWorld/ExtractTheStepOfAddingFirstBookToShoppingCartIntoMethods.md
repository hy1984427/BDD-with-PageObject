# Extract the step of adding first book to shopping cart into methods: getCurrentItemTitle addToShoppingCart

Let's package the step of adding first book to shopping cart into methods: `getCurrentItemTitle` and `addToShoppingCart` in "buy_book.rb". An it should look like:

<pre><code>And /^I add the first book to shopping cart$/ do
    getCurrentItemTitle
    addToShoppingCart
end

def getCurrentItemTitle
	@bookTitle=@driver.find_element(:id => "productTitle").text
end

def addToShoppingCart
	element=@driver.find_element :name => "submit.add-to-cart"
	element.click
end
</pre></code>

![alt text](https://raw.githubusercontent.com/hy1984427/BDD-with-PageObject/master/images/ExtractAddingTheFirstBookToShoppingCart.png "Extract addTheFirstBookToShoppingCart into methods")
