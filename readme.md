# Yahoo Finance API

Simple library for getting stock information using the YQL API on yahoo.finance tables.

## Download

    $ git clone git://github.com/zvineyard/yahoo-finance-api

## Setup

    require 'php-yql-finance/lib/YahooFinance/YahooFinance.php';

    $yf = new YahooFinance;

## Usage

   $historicaldata 	= $yf->getHistoricalData('AAPL', '2012-01-01', '2012-01-31');
   $quote          	= $yf->getQuotes('AAPL');	   				// single quote
   $quotes	   		= $yf->getQuotes(array('AAPL', 'GOOG'));	// multiple quotes

## Available Methods

	getHistoricalData($symbol, $startDate, $endDate); // Returns json object of basic historical data
	getHistoricalData( 'IDA', date('Y-m-d', strtotime('-14 days')), date('Y-m-d',time()) );

	getQuotes($symbols); // Returns json object with comprehensive trade info for each stock
	getQuotes(array('AAPL', 'GOOG'));

	getQuotesList($symbols); // Returns a summarized view of getQuotes
	getQuotesList(array('AAPL', 'GOOG'));