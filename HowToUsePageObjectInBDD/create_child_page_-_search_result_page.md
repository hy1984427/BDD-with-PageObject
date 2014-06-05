# Create child page - search result page

And "search_result.rb":

`touch search_result.rb`

![alt text](https://raw.githubusercontent.com/hy1984427/BDD-with-PageObject/master/images/CreateSearchResultRB.png "Create search_result.rb")

We need to copy following content to "search_result.rb" and delete them from "base_page.rb".

<pre><code>class SearchResult < Page

	def openTheFirstItemInSearchResult
		clickElementBy("xpath", "//div[@id=\"result_0\"]//span[@class=\"lrg bold\"]")
	end

end
</pre></code>

![alt text](https://raw.githubusercontent.com/hy1984427/BDD-with-PageObject/master/images/EditSearchResultRB.png "Edit search_result.rb")

![alt text](https://raw.githubusercontent.com/hy1984427/BDD-with-PageObject/master/images/EditSearchResultRBBasePageRB.png "Remove methods from base_page.rb")
