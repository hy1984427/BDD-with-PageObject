# Combine the methods findElementBy(type,value) and element.click into one single method clickElementBy(type,value)

We can see the method `findElementBy(type,value)` is followed by `element.click` many times. And according to the meaning of finding and clicking, we can combine them together into `clickElementBy(type,value)`.

And we will rewrite the methods in "buy_book.rb" as following:

<pre><code>def searchByKeyword (keyword)
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

def addToShoppingCart
	clickElementBy("name", "submit.add-to-cart")
end

def verifyItemAddedToShoppingCart
	confirm=findElementBy("id", "confirm-text")
	confirm.text.include?("1 item added to Cart")
end

def verifyItemAddedShownInShoppingCart
	book=findElementBy("xpath", "//div[@class=\"a-row a-size-base word-break\"]/a")
	book.attribute("title").should == @bookTitle
end

def clickElementBy (type, value)
	findElementBy(type, value).click
end
</pre></code>

![alt text](https://raw.githubusercontent.com/hy1984427/BDD-with-PageObject/master/images/CombineFindElementAndClick.png "Combine findElementBy(type,value) and element.click into one single method clickElementBy(type,value)")
