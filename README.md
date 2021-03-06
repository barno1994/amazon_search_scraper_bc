# amazon-search-scraper-bc

amazon_search_scraper_bc is a Python library for getting amazon search data and product details data in your project.
Especially when you want realtime data.

## Installation

Use the package manager [pip](https://pip.pypa.io/en/stable/) to install amazon_search_scraper_bc.

```bash
pip install amazon-search-scraper-bc
```

## Usage

You need to have webdrivers downloaded for it to work and give the program the path of the drivers. 

### To get search list:

```python
from amazon_search_scraper_bc.scraper import AmazonScraper
import os

pwd = os.path.abspath(os.getcwd())
# Location of your webdriver Ex:
path = pwd + "/webdrivers/chromedriver_linux64/chromedriver"

# You can call or select which driver to use ['chrome', 'firefox'] it will open the browsers in headless mode.

amasc =AmazonScraper("chrome", path)

print(amasc.amazon_product_search("Mobile"))
```

### To get product details:

```python
from amazon_search_scraper_bc.scraper import AmazonScraper
import os

pwd = os.path.abspath(os.getcwd())

# Location of your webdriver Ex:

path = pwd + "/webdrivers/chromedriver_linux64/chromedriver"

# You can call or select which driver to use ['chrome', 'firefox'] it will open the browsers in headless mode.

amasc =AmazonScraper("chrome", path)

url = "https://www.amazon.in/Redmi-9A-2GB-32GB-Storage/dp/B08696XB4B/ref=sr_1_3?dchild=1&keywords=mobile&qid=1629271762&sr=8-3"
print(amazonSc.get_single_product_details(url))
```

#### To change the amazon url 

```python
from amazon_search_scraper_bc.scraper import AmazonScraper
import os

pwd = os.path.abspath(os.getcwd())
# Location of your webdriver Ex:
path = pwd + "/webdrivers/chromedriver_linux64/chromedriver"
# You can call or select which driver to use ['chrome', 'firefox'] it will open the browsers in headless mode.

# By default it takes https://www.amazon.in .
# When calling get_single_product_details you need to send full url.

amasc =AmazonScraper("chrome", path, "https://www.amazon.com")
```

#### To see the time it is taking

```python
from amazon_search_scraper_bc.scraper import AmazonScraper
import os

pwd = os.path.abspath(os.getcwd())
# Location of your webdriver Ex:
path = pwd + "/webdrivers/chromedriver_linux64/chromedriver"

# You can call or select which driver to use ['chrome', 'firefox'] it will open the browsers in headless mode.

amasc =AmazonScraper("chrome", path)

# page_no needs to be greatter than 0

page_no = 1
time_show = True

print(amasc.amazon_product_search("Mobile", page_no, time_show))
```


## Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

Please make sure to update tests as appropriate.

## License

Copyright [2021] [Barno Chakraborty]

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
