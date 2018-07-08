# CoinPaymentsApiPHP
Coinpayments api library for php

First create and initial parameters and setup

    <?php

    require('cp/coinpayments.inc.php');

    $cps = new CoinPaymentsAPI();
    $prkey = '';  //Your private key
    $pukey = '';  //Your public key
    $cps->Setup("$prkey", "$pukey");
Then add parameters and calls(For example get callback address for Bitcoin, remember to put coin code).
    
    $result = $cps->GetCallbackAddress('BTC');

This sends the request. Now get the result.
    
    if ($result['error'] == 'ok') {

		print_r ($result);

		}

	 else {

		print 'Error: '.$result['error']."\n";

	}

The above example will print it in arrays.For getting in string just use the following:-
  
    if ($result['error'] == 'ok') {

		$address = ($result['result']['address']);
    echo $address;

		}

	 else {

		print 'Error: '.$result['error']."\n";

	}
  
  The following commands are availabe in library:-
  .)GetRates
  .)GetBalances
  .)CreateTransactionSimple
  .)CreateTransaction
  .)GetCallbackAddress
  .)CreateWithdrawal
  .)CreateTransfer
  .)SendToPayByName
  .)GetWithdrawalInformation
  .)GetTransactionInformation
 
 
 
# Contribute

Contribute in making this library more friendly and add more parameters.
