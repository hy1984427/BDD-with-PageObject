# Abstract the step of opening site into a method

Let's package the `@driver.get site` into a method `opening site` in "buy_book.rb". An it should look like:

<pre><code>Given /^I open "(.*?)"$/ do |site|
    openSite (site)
end

def openSite (site)
	@driver.get site
end
</pre></code>

![alt text](https://raw.githubusercontent.com/hy1984427/BDD-with-PageObject/master/images/AbstractOpenSite.png "Abstract openSite into a method")
