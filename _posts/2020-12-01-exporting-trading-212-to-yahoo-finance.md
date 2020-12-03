---
title: Export Trading212 transactions to CSV
categories:
  - Tech
  - Finance
  - Investing
header:
  teaser: /assets/images/blog/trading-212-to-csv.png
  og_image: /assets/images/blog/trading-212-to-csv.png
---


Trading212 has been amazing since I started using it in January 2020. However, despite many requests, linked below, from the community to support exporting of transactions, there is no solution from the team, yet.

- [How to export to CSV](https://community.trading212.com/t/how-to-export-to-csv/9855)
- [Export data to csv](https://community.trading212.com/t/export-data-to-csv/24839)
- [How to: export positions + official T212 document for tax declaration?](https://community.trading212.com/t/how-to-export-positions-official-t212-document-for-tax-declaration/584)
- [Transactions history export in csv/xls](https://community.trading212.com/t/transactions-history-export-in-csv-xls/9798)

Existing options
----
Despite all the amazing features, the gains and analysis of portfolios on their apps are fairly limited. I wanted to export all my transactions to a tool like Yahoo Finance Portfolios - since many other popular tools support importing from Yahoo Finance in one form or the other, this is a good start in my opinion.

If you are just looking to get a snapshot of your account, rather than the entire transactions, I would recommend to try this [Chrome add-on](https://chrome.google.com/webstore/detail/trading212-csv-exporter/pbmnfpbckdhhbcooafacfomhmiemcphf?hl=en-GB) instead.

Trading 212 Exporter
----
What's discussed below is a few hours work to write a super simple and quick tool to export your Trading 212 transactions to CSV - the CSV format is fully compatible with Yahoo Finance.

The advantage of the exporter discussed below is that it exports all your transactions rather than just current snapshot - this is useful to know the actual performance of your portfolio rather than the performance of your current stocks.
Trading 212 Exporter
{: .notice--success}

Before going into the details, here's it in action - you run a simple command and you get a CSV, and you can watch as it progress.

{% include figure image_path="/assets/images/blog/trading212-exporter.gif" caption="Trading 212 exporter in action" %}

The tool is open source and I encourage you to review it before jumping ahead and using it - since it will be accessing your account to export the transactions. [Source code on GitHub](https://github.com/praveendath92/Trading212-CSV-Exporter).


Setup
----
If you are not a very technical person and get stuck somewhere, __feel free ask for help in the comments.__

- Install Python3
- Install Pip3
- Download the repository above - either using git or as a zip file (and extract it)
- Make a copy of `config.ini.sample` as `config.ini`
- Edit the `config.ini` file and set your credentials and start and end dates
- Update Chrome browser to latest version (tested with version 87)
- [Download and extract](http://chromedriver.chromium.org/downloads) latest version of selenium webdriver to driver/ (tested with version 87)
- Run setup.sh

2FA authentication
----
If you have 2FA enabled, you should enter the 2FA code after the login page. Alternatively, you could do the full login manually - without putting your credentials in the config file. This is to be done after you start the export process below.
Export
Just use the command run.sh and the rest will be taken care of.
Yahoo Finance
Yahoo Finance doesn't use the same symbols as Trading212 for non-US stocks. For UK stocks this mapping is taken care of automatically. However, you can manual add symbol mappings in the export.py and it looks like:

```python
class YahooFinanceImporter():    
    SymbolMap = {
        "BTCE": "DE000A27Z304.SG",
        "WDI": "WDI.DE",
        "ECAR": "ECAR.L"
    }
```

Support
----
If you found this tool helpful, show your support by:
- Clapping and sharing this post
- Starring and sharing the GitHub repo