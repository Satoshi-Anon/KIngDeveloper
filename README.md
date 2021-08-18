# KIngDeveloper
Smart Contract Specialist, Bot Specialist
A Pancakeswap and Uniswap trading client (and bot) with market orders, limit orders, stop-loss, custom gas strategies, a GUI and much more.
If you have any questions or inquiries, or want this bot, you can contact my support: 

Satoshi-Anon@protonmail.com

Price: 0.5 BNB / Wallet: 0xB2f177671fb2d28914738e990F9B586ed3F7Ee67

Send me a E-Mail with the Transactionhash.

Changelog v2.0

    Added multiple DEXs (Pcs v1, Uniswap v2)
    Force Buy and Force Sell buttons, when clicked it will buy or sell with your chosen settings (excluding limit price)
    Speed improvements
    Many, many bug fixes (no more force closes or not working tokens)
    Added USDT as maincoin option
    The program now determines the name and decimals of the token automatically

![gif bot](https://user-images.githubusercontent.com/89160919/129960877-cbe34cf7-0eb8-42d7-8faa-132367baac81.gif)

Prerequisites

    An ethereum/bsc address
    A Windows machine (adding support for Mac OS and Linux soon)
    When trading on Uniswap: infura.io
    Not sure whether needed anymore: Visual C++ build tools (www.visualstudio.microsoft.com/visual-cpp-build-tools/)



Getting started

    Read prerequisites

    Download the latest release or download "configfile.py" and "tradingbot.exe" from the repository.

    Open "configfile.py" (with notepad for instance) and add your ethereum address and personal key at the bottom of the file between the quotation marks('').

...
my_address = ''
my_pk = ''

    Run "tradingbot.exe"

    Make sure configfile.py and bot.exe are in the same folder.

    Edit settings according to choice.



Functions

Main coin/token: The token or coin you want to trade tokens for and with

Token address: Fill the token address of the token you want to trade (such as 0x0000000000000000000000000000000000000000)

Notes: A place to fill in notes, such as the name of the token

Sell($): The price you want the trader to sell the token for (0.01 = 1 dollar cent)

Buy($): The price you want the trader to buy the token for (0.01 = 1 dollar cent)

Trade w/ main: Toggle if you want to activate trading with your main-coin/token

Trade w/ token (Experimental!): Toggle if you want to trade the token with other BEP20 tokens of which this option is activated (see tokentokennumerator)

Stoploss: Toggle to activate stoploss (0.01 = 1 dollar cent)

Second(s) between checking price: Standard is 4 seconds. With a infura server with max 100.000tx/day 4 seconds is good for 2 activated token 24hr/day

Seconds waiting between trades: depends on how fast transactions finalize

Max slippage: The maximum slippage you want to allow while trading (3 = 3%)

$ to keep in ETH/BNB after trade: The amount of ETH/BNB you want to keep after each trade (excluding transaction fees) in terms of $.

GWEI: The amount of gas you want to use for each trade (5 GWEI is fine for PCS). When trading on uniswap, This becomes the max GWEI you want to pay on the eth network, the GWEI will be determined from ethgasstation.com

Different deposit address: Use this if you want the swap output to go to a different address (without extra fees).

Tokentokennumerator (Experimental!): This value lets you trade ERC tokens with each other. The code to create the value is as followed:

if pricetoken1usd > ((token1high + token1low) / 2) and pricetoken2usd < ((token2high + token2low) / 2):
  token1totoken2 = ((pricetoken1usd - token1low) / (token1high - token1low)) / ((pricetoken2usd - token2low) / (token2high - token2low))

If you dont want to wait till the token1 is sold for the maincoinoption, because you are uncertain whether token2 will still be at this price level or think that token1 will drop, you can use this function. To use this function, "Trade with ERC" should be activated for at least 2 tokens, and the highs and lows should be set seriously.

As an example, if the current price of token1 is $0.9 and its set "high"=$1 and "low"=$0, the value of this token is seen as "90%". Token2 also has a high of $1, but the current price is 0.2$, value of this token is seen as 20%. The tokentokenmnumerator is set at 3.3. If we divide the 90% by the 20%, we get 4.5, which is higher than 3.3, which means that token1 gets traded for token2 instantly. If the tokentokennumerator was set to 5, the swap would not happen.



Changelog v2.0

    Added multiple DEXs (Pcs v1, Uniswap v2)
    Force Buy and Force Sell buttons, when clicked it will buy or sell with your chosen settings (excluding limit price)
    Speed improvements
    Many, many bug fixes (no more force closes or not working tokens)
    Added USDT as maincoin option
    The program now determines the name and decimals of the token automatically



Current bugs

    Let me know!



To do

    Add uniswap V3 support
    Add Linux and Mac OS executables
    Create manual and update github text
    Let me know what other DEX's should be added (solidity based ones only)

(Depends on whether the application is used)



Author



Contact: Satoshi-Anon@protonmail.com



