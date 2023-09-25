## Web Scraping on an E-commerce website to extract Product Information such as ProductName, Description, Price and Ratings.
"""

## If the website is not Flipkart then use this method to iterate over multiple pages.
while True:
  np = soup.find('a', class_ = "_1LKTO3").get("href")                                                                # Finding class of NEXT-page button, then getting a link of NEXT-page b
  Complete_np = "https://www.flipkart.com" + np                                                                      # adding link of flipkart to complete the Url
  print(Complete_np)

  #requesting data of next page
  Url = Complete_np
  page = requests.get(Url)
  soup = BeautifulSoup(page.content, 'html.parser')

"""
