
[![Build Status](https://travis-ci.org/joemccann/dillinger.svg?branch=master)](https://travis-ci.org/joemccann/dillinger) ![visitor badge](https://visitor-badge.glitch.me/badge?page_id=Capt-734gu3.h00k&left_color=white&right_color=purple&left_text=Pirates) [![Netlify Status](https://api.netlify.com/api/v1/badges/36c2507c-71eb-4179-a09d-1262b8902e76/deploy-status)](https://app.netlify.com/sites/thehook/deploys)

#TH3 H00K
>_The Ultimate_ _Opensea NFT Collection(s) Offer/Bidding Bot_


**[Th3 H00k](https://capt-734gu3.github.io/h00k/) is an NFT Collections Auto Bidding(Offer) Bot, that currently supports [The Opensea Marketplace](https://opensea.io) .**

<br>
<br>

![image](/assets/images/hook.png)

<br>

## [ F E A T U R E S ]

- <samp>[+] Compliant with latest Opensea Smart Contract(Wyvern 2.3)</samp>


- <samp>[+] 1.5k+ offers per minute</samp>


- <samp>[+] Supports All  Opensea's Collection Filters (`*highly recommended whenever possible to target specific assets in a collection`)</samp>


- <samp>[+] Supports Additional Custom Asset(*NFT) Filters  (Asset Qualifier Settings) => `**Used to additionaly filter out assets qualified to bid on`</samp>
- - <samp>+} Fixed Price (** Additionaly Filters each Asset based on a fixed price, ie. bids on asset if asset's current highest bid price is the same as the fixed price)</samp>
- - - <samp>Input Value:</samp>
- - - - <samp>[*] [Fixed Price] in Weth/selected PaymentToken`</samp>

- - <samp>+} Price Range  (**Additionally Filters each asset based on a price range, ie. bids on asset if  asset's current highest bid price is within range)</samp>
- - - <samp>Input Values:</samp>
- - - - <samp>[*] [Minimum Value] in Weth/selected PaymentToken</samp>
- - - - <samp>[*] [Maximum Value] in Weth/selected PaymentToken</samp>


- <samp>[+] Supports 3 Custom Bid Settings (Offer bid Settings) => {`**Used to dictate how the bid/offer amount is calculated`}</samp>
- - <samp>+} Fixed Price (** Bid's Offer amount will be same as the fixed price)</samp>
- - - <samp>Input Value:</samp>
- - - - <samp>[*] [Fixed Price] in Weth/selected PaymentToken</samp>

- - <samp>+} Percentage (** Bid's Offer amount will be {percentage(%) of current asset's highest bid} above in Weth/selected PaymentToken)</samp>
- - - <samp>Input Value:</samp>
- - - - <samp>[*]  [Percentage(%)] of current asset's highest bid (Supports up to 1dp, ie. 12.4%)</samp>

- - <samp>+} Points Above (** Bid's Offer amount will be {X points above current asset's highest bid} in Weth/selected PaymentToken)</samp>
- - - <samp>Input Value:</samp>
- - - - <samp>[*] [Points Above] current asset's highest bid in Weth/Chosen Token</samp>


- <samp>[+] Supports Weth(Default) & Polygon Eth Payment Tokens</samp>


- <samp>[+] Supports Custom Offer Expiration time in number of days</samp>
- - <samp>+} Expiration (** Offer expiration in number of days)</samp>
- - - <samp>Input Value</samp>
- - - - <samp>[*] [Expiration] Offer expiration in number of days</samp>


- <samp>[+] Auto Signing with Account Private Key (** Works with Metamask etc...)</samp>


- <samp>[+] Works on Testnet(*Rinkeby) & Mainnet</samp>

<br>

## [ ** R E Q U I R E D&nbsp;&nbsp;&nbsp; U S E R&nbsp;&nbsp;&nbsp; S E T T I N G S ]

<samp>=> For Security reasons, all information we consider sensitive User settings are stored as `ENVIRONMENTAL_VARIABLES`</samp>

#### ENVIRONMENTAL VARIABLES:
- <samp>[+] `WALLET_ADDRESS`</samp>
- - <samp>-- User Account Wallet Address</samp>
- - - <samp>--> Required in Creating, Hashing & Signing the offers</samp>


- <samp>[+] `WALLET_PRIVATE_KEY`</samp>
- - <samp>-- User Account's Private Key</samp>
- - -  <samp>--> Required in Signing the offers</samp>


- <samp>[+] `NETWORK`</samp>
- - <samp>-- Ethereum Network to use</samp>
- - - <samp>--> Testnet(Rinkeby) -- Offers will be made on Opensea's Testnet Assets, can use to test if your settings work as required</samp>
- - - <samp>--> Mainnet --  Offers will be made on actual Opensea Mainnet(Live/Real) Assets, **NB : THESE ARE LIVE OFFERS BEING MADE**</samp>


- <samp>[+] `WEB3_INFURA_PROJECT_ID`</samp>
- - <samp>-- Infura Project ID</samp>
- - - <samp>--> Requires an Infura Account</samp>

<br>

## [ H O W&nbsp;&nbsp;&nbsp; I T&nbsp;&nbsp;&nbsp; W O R K S]

1. <samp>Bot Takes 4 Inputs:</samp>
- - <samp>[+] \*\***Collection url** `(**Mandatory)`</samp>
- - - <samp>-- Opensea Collection url with it's included collection url filters if any</samp>

- - <samp>[+] **Asset Qualifier Settings** {Optional(recommended), if not set will bid on all assets recieved after Opensea Collection Filter if any}</samp>
- - - <samp>-- Used to additionaly filter out the assets qualified to bid on based on an asset's current highest bid price</samp>

- - <samp>[+] \*\***Bid Settings** `(**Mandatory)`</samp>
- - - <samp>-- Used to dictate how the bid/offer amount is calculated</samp>

- - <samp>[+] **Expiration** {Optional, if not set defaults to 7 days}</samp>
- - - <samp>-- Used to set offer expiration time</samp>


2. <samp>Pulls the Collection's Assets from Opensea and applies all the Collection Filters, if any.</samp>


3. <samp>Applies any Asset Qualifier Filters(\*\*Additional Custom Filters set by the User) on each asset, if any.</samp>


4. <samp>Calculates bid price for each of the qulified assets based on the Bid Settings set by the User.</samp>


5. <samp>Creates, Signs and Posts offers to each of the qualified asset based on:</samp>
- - <samp>[+] **Selected Network**</samp>
- - <samp>[+] **User Calculated Bid Price**</samp>
- - <samp>[+] **Selected payment Token**</samp>
- - <samp>[+] **User Current Wallet Balance**</samp>


<br>



## Credit

This landing page theme is built on [shorthand css framework](https://github.com/shorthandcss/shorthand)



* Picture [unsplash](https://unsplash.com)
* Icons [feathericons](https://feathericons.com)
