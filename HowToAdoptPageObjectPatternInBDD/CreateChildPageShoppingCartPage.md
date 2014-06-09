# Create child page - shopping cart page

And "shopping_cart.rb":

`touch shopping_cart.rb`

![alt text](https://raw.githubusercontent.com/hy1984427/BDD-with-PageObject/master/images/CreateShoppingCartRB.png "Create shopping_cart.rb")

We need to copy following content to "shopping_cart.rb" and delete them from "base_page.rb".

<pre><code>class ShoppingCart < Page

	def removeTheFirstItem
		waitForJsOrAjax
		clickElementBy("xpath","//span[@class=\"a-declarative\"]/input")
	end

	def verifyItemAddedShownInShoppingCart
		book=findElementBy("xpath", "//div[@class=\"a-row a-size-base word-break\"]/a")
		book.attribute("title").should == $bookTitle
		@driver.save_screenshot ("screenshot.png")
	end

	def verifyItemRemovedFromShoppingCart
		waitForJsOrAjax
		confirm=findElementBy("class", "a-size-base")
		confirm.text.include?("was removed from Shopping Cart")
	end

	def verifyItemRemovedNotShownInShoppingCart
		book=findElementBy("xpath", "//span[@class=\"a-size-medium a-text-bold\"]")
		book.text.should == "Subtotal (0 item): $0.00"
	end
end
</pre></code>

![alt text](https://raw.githubusercontent.com/hy1984427/BDD-with-PageObject/master/images/EditShoppingCartRB.png "Edit shopping_cart.rb")

![alt text](https://raw.githubusercontent.com/hy1984427/BDD-with-PageObject/master/images/EditShoppingCartRBBasePageRB.png "Remove methods from base_page.rb")
