# WazirX Public Rest API

## General Information
1. Base API Endpoint: https://x.wazirx.com
1. All public api will return either JSON or Array object.

### Public API Endpoints

1. GET `/api/v2/market-status`

    Returns JSON object which has current market and currency status. Response object will have 2 keys `markets`(all market related configs will be in this key) and `assets`(all currency related configs will be here). 
    ##### Response:
    ```
    {
        "markets": [
            {
                "baseMarket": "btc",
                "quoteMarket": "inr",
                "minBuyAmount": 0.001,
                "minSellAmount": 0.001,
                "fee": {
                    "bid": {
                        "maker": 0.001,
                        "taker": 0.0025
                    },
                    "ask": {
                        "maker": 0.001,
                        "taker": 0.0025
                    }
                },
                "basePrecision": 4,
                "quotePrecision": 2,
                "low": "460001.01",
                "high": "505000.0",
                "last": "480102.0",
                "open": 505002,
                "volume": "0.2071",
                "sell": "490000.0",
                "buy": "485001.0"
            },
            ...
        ],
        "assets": [
            {
                "type": "inr",
                "name": "Rupee",
                "withdrawFee": 0,
                "minWithdrawAmount": 50,
                "maxWithdrawAmount": 50000,
                "deposit": "enabled",
                "withdrawal": "enabled"
            },
            ...
        ]
    }
    ```