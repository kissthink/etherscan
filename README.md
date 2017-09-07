# etherscan

<p>This lib is created for connecting to etherscan.io's api using php.</p>
<p>There are 2 possible ways of using the lib:
<ul>
<li>sync

```
$esApiConnector = new ApiConnector('BZ34DW4M5J6XZIQV5DWBC2MJV32V955Q1H', EtherScan::MODE_API);
$etherScan = new EtherScan($esApiConnector);

echo $etherScan->getStats()->getEthPrice() . PHP_EOL;
echo "END OF FILE" . PHP_EOL;
```

</li>
<li>async

```
$esApiConnector = new ApiConnector('BZ34DW4M5J6XZIQV5DWBC2MJV32V955Q1H', EtherScan::MODE_API);
$etherScan = new EtherScan($esApiConnector);

echo $etherScan->getStats()->getEthPriceAsync(
        function ($responseOnResolve) {
            echo 'Called on resolve: ' . $responseOnResolve . PHP_EOL;
        },
        function ($responseOnReject) {
            echo 'Called on resolve: ' . $responseOnReject . PHP_EOL;
        }
    );
echo "END OF FILE" . PHP_EOL;
```

</li>
</ul>
</p>
