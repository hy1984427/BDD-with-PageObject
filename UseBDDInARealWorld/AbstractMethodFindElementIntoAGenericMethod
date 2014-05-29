# Abstract method find_element into a generic method findElementBy(type,value)

Too keep the method `find_element` simple and easier to use, we can abstract it into a generic method `findElementBy(type,value)`.

And we will rewrite the methods in "buy_book.rb" as following:

<pre><code>def searchByKeyword (keyword)
    searchKeyword=findElementBy("id","twotabsearchtextbox")
    searchKeyword.clear
    searchKeyword.send_keys keyword
    element=findElementBy("class", "nav-submit-input")
    element.click
end

def openTheFirstItemInSearchResult
	element=findElementBy("xpath", "//div[@id=\"result_0\"]//span[@class=\"lrg bold\"]")
	element.click
end

def getCurrentItemTitle
	@bookTitle=findElementBy("id", "productTitle").text
end

def addToShoppingCart
	element=findElementBy("name", "submit.add-to-cart")
	element.click
end

def verifyItemAddedToShoppingCart
	confirm=findElementBy("id", "confirm-text")
	confirm.text.include?("1 item added to Cart")
end

def verifyItemAddedShownInShoppingCart
	book=findElementBy("xpath", "//div[@class=\"a-row a-size-base word-break\"]/a")
	book.attribute("title").should == @bookTitle
end

def findElementBy (type, value)
	if type=="class"
		element=@driver.find_element :class => value
	elsif type=="css"
		element=@driver.find_element :css => value
	elsif type=="id"
		element=@driver.find_element :id => value
	elsif type=="link"
		element=@driver.find_element :link => value
	elsif type=="name"
		element=@driver.find_element :name => value
	elsif type=="partial_link"
		element=@driver.find_element :partial_link_text => value
	elsif type=="tag"
		element=@driver.find_element :tag_name => value
	elsif type=="xpath"
		element=@driver.find_element :xpath => value
	else
		p "incorrect selector type"
	end
end
</pre></code>

![alt text](https://raw.githubusercontent.com/hy1984427/BDD-with-PageObject/master/images/AbstractFindElement1.png "Abstract FindElement and rewrite methods part 1")

![alt text](https://raw.githubusercontent.com/hy1984427/BDD-with-PageObject/master/images/AbstractFindElement2.png "Abstract FindElement and rewrite methods part 2")
