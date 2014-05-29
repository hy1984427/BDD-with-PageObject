# Separate the content in Selenium-WebDriver sample.rb into different sections

We need to separate the content in Selenium-WebDriver "sample.rb" into different sections, based on the steps we defined in Selenium-WebDriver "sample.feature"

<pre><code>require 'selenium-webdriver'

Before do
    @driver = Selenium::WebDriver.for :firefox
end

Given /I opened Google/ do
    @driver.get "http://www.google.com"
end

When /I search a keyword/ do
    element = @driver.find_element :name => "q"
    element.send_keys "Cheese!"
    element.submit
end

Then /I should see the browser title/ do
    p "Page title is #{@driver.title}"
    wait = Selenium::WebDriver::Wait.new(:timeout => 10)
    wait.until { @driver.title.downcase.start_with? "cheese!" }
    p "Page title is #{@driver.title}"
end

After do
    @driver.quit
end
</pre></code>

![alt text](https://raw.githubusercontent.com/hy1984427/BDD-with-PageObject/master/images/SeleniumWebDriverSampleRBInSections.png "Separate Selenium-WebDriver sample.rb into sections")
