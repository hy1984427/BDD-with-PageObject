# Add step definitions for adding book to shopping cart from wish list

Similarly, we are going to modify "buy_book.rb" under "features/step_definations".

`cd step_definations`

![alt text](https://raw.githubusercontent.com/hy1984427/BDD-with-PageObject/master/images/ChangeFolderToStepDefinitions.png "Change folder to features/step_definations")

Then edit it to contain following content:

<pre><code>And /^I login as "(.*?)" with "(.*?)"$/ do |username,password|
	loginAs(username,password)
end

And /^I add the first book to Wish List$/ do
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

def loginAs (username,password)
	clickElementBy("id", "nav-signin-text")
	inputToElementWith("id", "ap_email", username)
	inputToElementWith("id", "ap_password", password)
	clickElementBy("id","signInSubmit-input")
end

def addToShoppingCartFromWishList
	clickElementBy("xpath", "//a[@class=\"a-button-text a-declarative\"]")
end

def inputToElementWith (type, value, input)
	inputElement=findElementBy(type, value)
	inputElement.clear
	inputElement.send_keys input
end
</pre></code>

![alt text](https://raw.githubusercontent.com/hy1984427/BDD-with-PageObject/master/images/EditBuyBookFomWishListRB1.png "Edit from wish list steps in buy_book.rb part 1")

![alt text](https://raw.githubusercontent.com/hy1984427/BDD-with-PageObject/master/images/EditBuyBookFomWishListRB2.png "Edit from wish list steps in buy_book.rb part 2")

![alt text](https://raw.githubusercontent.com/hy1984427/BDD-with-PageObject/master/images/EditBuyBookFomWishListRB3.png "Edit from wish list steps in buy_book.rb part 3")
