# Abstract findElementBy and ClickElementBy in steps into meaningful methods

We can see findElementBy and ClickElementBy are called directly in steps, it's better to give them meaningful names:
<pre><code>And /^I add the first book to Wish List$/ do
	getCurrentItemTitle
	clickElementBy("id","add-to-wishlist-button-submit")
end

And /^I add the first book to shopping cart from Wish List$/ do
	clickElementBy("class","w-button-inner")
	addToShoppingCartFromWishList
end

And /^I open my shopping cart$/ do
	clickElementBy("id","nav-cart")
end
</pre></code>

So we can abstract them into methods:
<pre><code>And /^I add the first book to Wish List$/ do
	getCurrentItemTitle
	addToWishList
end

And /^I add the first book to shopping cart from Wish List$/ do
	openWishList
	addToShoppingCartFromWishList
end

And /^I open my shopping cart$/ do
	openShoppingCart
end

def addToWishList
	clickElementBy("id","add-to-wishlist-button-submit")
end

def openWishList
	clickElementBy("class","w-button-inner")
end

def openShoppingCart
	clickElementBy("id","nav-cart")
end
</pre></code>

![alt text](https://raw.githubusercontent.com/hy1984427/BDD-with-PageObject/master/images/AbstractFindElementBuyBookFromWishList1.png "Abstract findElementBy and clickElementBy in Buy Book from wish list part 1")

![alt text](https://raw.githubusercontent.com/hy1984427/BDD-with-PageObject/master/images/AbstractFindElementBuyBookFromWishList2.png "Abstract findElementBy and clickElementBy in Buy Book from wish list part 2")
