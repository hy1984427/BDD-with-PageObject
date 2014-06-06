# Create child page - home page

We will create severals pages accordingly, and put their own methods into them. Such as "home.rb":

`touch home.rb`

![alt text](https://raw.githubusercontent.com/hy1984427/BDD-with-PageObject/master/images/CreateHomeRB.png "Create home.rb")

We need to copy following content to "home.rb" and delete them from "base_page.rb".

<pre><code>class Home < Page

def openSite (site)
    @driver.get site
end

end
</pre></code>

![alt text](https://raw.githubusercontent.com/hy1984427/BDD-with-PageObject/master/images/EditHomeRB.png "Edit home.rb")

![alt text](https://raw.githubusercontent.com/hy1984427/BDD-with-PageObject/master/images/EditHomeRBBasePageRB.png "Remove methods from base_page.rb")
