# Update env.rb

We also need to mofidy "env.rb" again as following:

`cd ..`

![alt text](https://raw.githubusercontent.com/hy1984427/BDD-with-PageObject/master/images/ChangeFolderToSupport.png "Change folder to features/support")

<pre><code>require 'rubygems'
require 'selenium-webdriver'

Before do
	@driver = Selenium::WebDriver.for :firefox
	@driver.manage.timeouts.implicit_wait = 60
	@driver.manage.timeouts.script_timeout = 60
	@driver.manage.timeouts.page_load = 60
	@wishlist=WishList.new(@driver)
	@searchresult=SearchResult.new(@driver)
	@home=Home.new(@driver)
	@login=Login.new(@driver)
	@page=Page.new(@driver)
	@itemdetails=ItemDetails.new(@driver)
	@shoppingcart=ShoppingCart.new(@driver)
end

After do
	@driver.quit
end
</pre></code>

![alt text](https://raw.githubusercontent.com/hy1984427/BDD-with-PageObject/master/images/UpdateEnvRB.png "Update env.rb")
