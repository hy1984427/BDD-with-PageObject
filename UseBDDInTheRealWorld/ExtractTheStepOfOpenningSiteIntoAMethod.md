# Extract the step of opening site into a method

Let's extract the `@driver.get site` into a method `openSite` in "buy_book.rb". An it should look like:

<pre><code>Given /^I open "(.*?)"$/ do |site|
    openSite (site)
end

def openSite (site)
	@driver.get site
end
</pre></code>

![alt text](https://raw.githubusercontent.com/hy1984427/BDD-with-PageObject/master/images/ExtractOpenSite.png "Extract openSite into a method")
