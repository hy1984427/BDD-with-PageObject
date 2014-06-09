# Add step definitions for buying book

Similarly, we are going to add "buy_book.rb" under "features/step_definations".

`cd step_definations`

`touch buy_book.rb`

![alt text](https://raw.githubusercontent.com/hy1984427/BDD-with-PageObject/master/images/CreateBuyBookRB.png "Create buy_book.rb")

Then edit it to contain following content:

<pre><code># encoding: utf-8
Given /^I open "(.*?)"$/ do |site|
    @driver.get site
end

When /^I search for "(.*?)"$/ do |keyword|
	searchKeyword=@driver.find_element :id => "twotabsearchtextbox"
	searchKeyword.clear
	searchKeyword.send_keys keyword
	element=@driver.find_element :class =>"nav-submit-input"
	element.click
end

And /^I open the first book$/ do
	element=@driver.find_element :xpath => "//div[@id=\"result_0\"]//span[@class=\"lrg bold\"]"
    element.click
end

And /^I add the first book to shopping cart$/ do
	@bookTitle=@driver.find_element(:id => "productTitle").text
	element=@driver.find_element :name => "submit.add-to-cart"
	element.click
end

Then /^I should see the book in my shopping cart$/ do
	confirm=@driver.find_element :id => "confirm-text"
	confirm.text.include?("1 item added to Cart")
	book=@driver.find_element :xpath => "//div[@class=\"a-row a-size-base word-break\"]/a"
	book.attribute("title").should == @bookTitle
end
</pre></code>

*The `# encoding: utf-8` here is to support multiple languages, if you just want to use English all the time and anywhere in your test, you can get rid of it.*

![alt text](https://raw.githubusercontent.com/hy1984427/BDD-with-PageObject/master/images/EditBuyBookRB.png "Edit buy_book.rb")

*If you need to change control to a new popuped window, you can use `@driver.switch_to.window @driver.window_handles.last`.*
