# Abstract the step of searching by keyword into a method

Let's package the step of searching by keyword into a method `searchByKeyword` in "buy_book.rb". An it should look like:

<pre><code>When /^I search for "(.*?)"$/ do |keyword|
    searchByKeyword (keyword)
end

def searchByKeyword (keyword)
	searchKeyword=@driver.find_element :id => "twotabsearchtextbox"
	searchKeyword.clear
	searchKeyword.send_keys keyword
	element=@driver.find_element :class =>"nav-submit-input"
	element.click
end
</pre></code>

![alt text](https://raw.githubusercontent.com/hy1984427/BDD-with-PageObject/master/images/AbstractSearchByKeyword.png "Abstract searchByKeyword into a method")
