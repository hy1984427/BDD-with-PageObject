# Create base page to contains all methods

Let's create a base page first:
`touch base_page.rb`

![alt text](https://raw.githubusercontent.com/hy1984427/BDD-with-PageObject/master/images/CreateBasePageRB.png "Create base_page.rb")

We will edit the "base_page.rb" and can simple copy all the methods start from `def openSite (site)` in the "buy_book.rb" and `def openShoppingCart` in "remove_book.rb" into it. It should contains following content:

<pre><code># encoding: utf-8
def openSite (site)
	@driver.get site
end

def loginAs (username,password)
	clickElementBy("id", "nav-signin-text")
	inputToElementWith("id", "ap_email", username)
	inputToElementWith("id", "ap_password", password)
	clickElementBy("id","signInSubmit-input")
end

def searchByKeyword (keyword)
	searchKeyword=findElementBy("id","twotabsearchtextbox")
	searchKeyword.clear
	searchKeyword.send_keys keyword
	clickElementBy("class", "nav-submit-input")
end

def openTheFirstItemInSearchResult
	clickElementBy("xpath", "//div[@id=\"result_0\"]//span[@class=\"lrg bold\"]")
end

def getCurrentItemTitle
	@bookTitle=findElementBy("id", "productTitle").text
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

def addToShoppingCart
	clickElementBy("name", "submit.add-to-cart")
end

def addToShoppingCartFromWishList
	clickElementBy("xpath", "//a[@class=\"a-button-text a-declarative\"]")
end

def verifyItemAddedToShoppingCart
	confirm=findElementBy("id", "confirm-text")
	confirm.text.include?("1 item added to Cart")
end

def verifyItemAddedShownInShoppingCart
	book=findElementBy("xpath", "//div[@class=\"a-row a-size-base word-break\"]/a")
	book.attribute("title").should == @bookTitle
	@driver.save_screenshot ("screenshot.png")
end

def clickElementBy (type, value)
	findElementBy(type, value).click
end

def inputToElementWith (type, value, input)
	inputElement=findElementBy(type, value)
	inputElement.clear
	inputElement.send_keys input
end

def findElementBy (type, value)
	if type=="class"
		@element=@driver.find_element :class => value
	elsif type=="css"
		@element=@driver.find_element :css => value
	elsif type=="id"
		@element=@driver.find_element :id => value
	elsif type=="link"
		@element=@driver.find_element :link => value
	elsif type=="name"
		@element=@driver.find_element :name => value
	elsif type=="partial_link"
		@element=@driver.find_element :partial_link_text => value
	elsif type=="tag"
		@element=@driver.find_element :tag_name => value
	elsif type=="xpath"
		@element=@driver.find_element :xpath => value
	else
		p "incorrect selector type"
	end
end

def removeTheFirstItem
	sleep (10) #it's better to wait for js or AJAX executed complete, but there is not a general way we can follow in industry
	clickElementBy("xpath","//span[@class=\"a-declarative\"]/input")
end

def verifyItemRemovedFromShoppingCart
	confirm=findElementBy("class", "a-size-base")
	confirm.text.include?("was removed from Shopping Cart")
end

def verifyItemRemovedNotShownInShoppingCart
	book=findElementBy("xpath", "//span[@class=\"a-size-medium a-text-bold\"]")
	book.text.should == "Subtotal (0 item): $0.00"
end
</pre></code>

*Ruby will load the pages according to their name ascendingly, so it's better to name your base page to be loaded first.*

![alt text](https://raw.githubusercontent.com/hy1984427/BDD-with-PageObject/master/images/EditBasePageRB1.png "Edit base_page.rb part 1")

![alt text](https://raw.githubusercontent.com/hy1984427/BDD-with-PageObject/master/images/EditBasePageRB2.png "Edit base_page.rb part 2")

![alt text](https://raw.githubusercontent.com/hy1984427/BDD-with-PageObject/master/images/EditBasePageRB3.png "Edit base_page.rb part 3")

Please DO remember to delete the methods we copied in "buy_book.rb" and "remove_book.rb". they should look like:

![alt text](https://raw.githubusercontent.com/hy1984427/BDD-with-PageObject/master/images/EditNewBuyBookRB.png "Remove methods in buy_book.rb")

![alt text](https://raw.githubusercontent.com/hy1984427/BDD-with-PageObject/master/images/EditNewRemoveBookRB.png "Remove methods in remive_book.rb")
