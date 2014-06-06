# Create child page - wish list page

And "wish_list.rb":

`touch wish_list.rb`

![alt text](https://raw.githubusercontent.com/hy1984427/BDD-with-PageObject/master/images/CreateWishListRB.png "Create wish_list.rb")

We need to copy following content to "wish_list.rb" and delete them from "base_page.rb".

<pre><code>class WishList < Page

	def addToShoppingCartFromWishList
		clickElementBy("xpath", "//a[@class=\"a-button-text a-declarative\"]")
	end

end
</pre></code>

![alt text](https://raw.githubusercontent.com/hy1984427/BDD-with-PageObject/master/images/EditWishListRB.png "Edit wish_list.rb")

![alt text](https://raw.githubusercontent.com/hy1984427/BDD-with-PageObject/master/images/EditWishListRBBasePageRB.png "Remove methods from base_page.rb")
