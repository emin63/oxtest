
# Introduction

Tools to help create dockerized tests in python.

# Tips and Tricks

## PhantomJS

PhantomJS is a great selenium driver. There are a few things you may want to keep in mind:

  1. Use `service_args=['--ignore-ssl-errors=true', '--ssl-protocol=any']`
     when creating the driver (e.g., `driver =
     webdriver.PhantomJS(service_args=...)`). This is helpful if you
     are doing tests and do not have proper SSL certificates installed.
  2. Do something like `driver.set_page_load_timeout(300)` if you have
     pages which take a while.
  3. Do something like `driver.maximize_window()` to make sure the
     window is big enough to "see" the page.

     