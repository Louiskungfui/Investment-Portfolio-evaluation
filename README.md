Investment Portfolio Evaluation

This project compares a monthly trend-following portfolio with a static 60/40portfolio. The assets used are VT for global equities, IEF for US governmentbonds and BIL as the cash proxy.

Running the analysis

Install the packages in requirements.txt.

Open Investment_Portfolio.ipynb in Jupyter or Google Colab.

Run the cells in order.

The notebook downloads adjusted daily opening and closing prices from YahooFinance for 1 July 2008 to 30 June 2026. It saves the downloaded prices,portfolio charts and the moving-average sensitivity table in the workingdirectory.

Backtest details

The signal is calculated from month-end prices. It is applied at the firstavailable market open in the following month. The previous allocation is usedfor the overnight movement into the new month, and the new allocation is usedfor the intraday return. Turnover compares the target weights with the weightsimmediately before the rebalance, so price drift is included.

The main trend rule uses a ten-month moving average. The notebook also tests8-, 10- and 12-month averages, keeps the final 25% of the sample as a holdout,and compares matched 0, 10 and 25 basis-point transaction costs for bothportfolios.

The downloaded data are not a fixed historical data vendor snapshot. YahooFinance can revise data and its availability can change, so the date range,package versions and generated files should be recorded when the analysis isrerun.
