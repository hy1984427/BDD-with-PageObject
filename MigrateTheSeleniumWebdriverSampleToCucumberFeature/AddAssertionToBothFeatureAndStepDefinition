# Add assertion to both feature and step definition

We can aslo add assertion to verify the expected result shown. Take the browser title as an example, we can check whether partial of it contains some characters.

In "sample.feature", we need to change the last step to:

`Then I should see the browser title has "Cheese! - Google"`

![alt text](https://raw.githubusercontent.com/hy1984427/BDD-with-PageObject/master/images/SeleniumWebDriverSampleFeatureAssertion.png "Add assertion in Selenium-WebDriver sample.feature")

And in "sample.rb", we need to change the last step as well:

<pre><code>Then /I should see the browser title has "(.*?)"/ do |partial_title|
    @driver.title.include?(partial_title)
end
</pre></code>

![alt text](https://raw.githubusercontent.com/hy1984427/BDD-with-PageObject/master/images/SeleniumWebDriverSampleRBAssertion.png "Add assertion in Selenium-WebDriver sample.rb")
