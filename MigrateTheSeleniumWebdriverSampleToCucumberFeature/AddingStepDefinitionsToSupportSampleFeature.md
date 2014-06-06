# Add step definitions to support sample feature

Create "sample.rb" to support sample feature under "features/step_definations" folder:

`cd step_definitions`

`touch sample.rb`

![alt text](https://raw.githubusercontent.com/hy1984427/BDD-with-PageObject/master/images/CreateSeleniumWebDriverSampleRB.png "Selenium-WebDriver sample.rb")

Copy content of previous sample.rb to the new one:

<pre><code>require 'selenium-webdriver'
driver = Selenium::WebDriver.for :firefox
driver.get "http://www.google.com"
element = driver.find_element :name => "q"
element.send_keys "Cheese!"
element.submit
p "Page title is #{driver.title}"
wait = Selenium::WebDriver::Wait.new(:timeout => 10)
wait.until { driver.title.downcase.start_with? "cheese!" }
p "Page title is #{driver.title}"
driver.quit
</pre></code>

![alt text](https://raw.githubusercontent.com/hy1984427/BDD-with-PageObject/master/images/SeleniumWebDriverSampleRB.png "Selenium-WebDriver sample.rb content")
