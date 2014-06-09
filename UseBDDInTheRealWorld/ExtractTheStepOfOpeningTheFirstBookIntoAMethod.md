# Extract the step of opening the first book into a method openTheFirstItemInSearchResult

Let's package the step of opening the first book into a method `openTheFirstItemInSearchResult` in "buy_book.rb". An it should look like:

<pre><code>And /^I open the first book$/ do
    openTheFirstItemInSearchResult
end

def openTheFirstItemInSearchResult
	element=@driver.find_element :xpath => "//div[@id=\"result_0\"]//span[@class=\"lrg bold\"]"
	element.click
end
</pre></code>

![alt text](https://raw.githubusercontent.com/hy1984427/BDD-with-PageObject/master/images/ExtractOpenTheFirstItemInSearchResult.png "Extract openTheFirstItemInSearchResult into a method")
