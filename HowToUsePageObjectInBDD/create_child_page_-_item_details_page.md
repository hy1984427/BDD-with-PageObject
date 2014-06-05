# Create child page - item details page

Now, it's "item_details.rb":

`touch item_details.rb`

![alt text](https://raw.githubusercontent.com/hy1984427/BDD-with-PageObject/master/images/CreateItemDetailsRB.png "Create item_details.rb")

We need to copy following content to "item_details.rb" and delete them from "base_page.rb".

<pre><code>class ItemDetails < Page

	def addToShoppingCart
		lickElementBy("name", "submit.add-to-cart")
	end

	def addToWishList
		clickElementBy("id","add-to-wishlist-button-submit")
	end

	def openWishList
		waitForJsOrAjax
		clickElementBy("class","w-button-inner")
	end

	def openShoppingCart
		clickElementBy("id","nav-cart")
	end

end
</pre></code>

![alt text](https://raw.githubusercontent.com/hy1984427/BDD-with-PageObject/master/images/EditItemDetailsRB.png "Edit item_details.rb")

![alt text](https://raw.githubusercontent.com/hy1984427/BDD-with-PageObject/master/images/EditItemDetailsRBBasePageRB.png "Remove methods from base_page.rb")
