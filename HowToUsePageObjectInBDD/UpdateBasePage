# Update base page

Once again, we have to mofidy "base_page.rb" again as following:

<pre><code># encoding: utf-8

class Page

	def initialize(driver)
		@driver = driver
	end

	def searchByKeyword (keyword)
		searchKeyword=findElementBy("id","twotabsearchtextbox")
		searchKeyword.clear
		searchKeyword.send_keys keyword
		clickElementBy("class", "nav-submit-input")
	end

	def getCurrentItemTitle
		$bookTitle=findElementBy("id", "productTitle").text
	end

	def openShoppingCart
		clickElementBy("id","nav-cart")
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

	def waitForJsOrAjax
		sleep (10) #it's better to wait for js or AJAX executed complete, but there is not a general way we can follow in industrys
	end
end
</pre></code>

![alt text](https://raw.githubusercontent.com/hy1984427/BDD-with-PageObject/master/images/UpdateBasePageRB1.png "Update base_page.rb part 1")

![alt text](https://raw.githubusercontent.com/hy1984427/BDD-with-PageObject/master/images/UpdateBasePageRB2.png "Update base_page.rb part 2")
