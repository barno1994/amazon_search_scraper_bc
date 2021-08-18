# amazon_search_scraper_bc

amazon_search_scraper_bc is a Python library for getting amazon search data and product details data in your project.

## Installation

Use the package manager [pip](https://pip.pypa.io/en/stable/) to install foobar.

```bash
pip install amazon_search_scraper_bc
```

## Usage

You need to have webdrivers downloaded for it to work and give the program the path of the drivers. 

```python
from amazon_search_scraper_bc.scraper import AmazonScraper
import os

pwd = os.path.abspath(os.getcwd())
# Location of your webdriver Ex:
path = pwd + "/webdrivers/chromedriver_linux64/chromedriver"
# You can call or select which driver to use ['chrome', 'firefox'] it will open the browsers in headless mode
amasc =AmazonScraper("chrome", path)

print(amasc.amazon_product_search("Mobile"))
```

## Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

Please make sure to update tests as appropriate.

## License
[MIT](https://choosealicense.com/licenses/mit/)