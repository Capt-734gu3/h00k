
[![Build Status](https://travis-ci.org/joemccann/dillinger.svg?branch=master)](https://travis-ci.org/joemccann/dillinger) ![visitor badge](https://visitor-badge.glitch.me/badge?page_id=Capt-734gu3.h00k&left_color=white&right_color=purple&left_text=Pirates)

#TH3 H00K
>_The Ultimate_ _Opensea NFT Collection(s) Offer/Bidding Bot_


![Th3 H00k]() is an NFT Collections Auto Bidding(Offer) Bot, that currently supports [The Opensea Marketplace](https://opensea.io) .


[ Features ]
=============
- [+] Compliant with latest Opensea Smart Contract(Wyvern 2.3)

- [+] 1.5k+ offers per minute

- [+] Supports All  Opensea's Collection Filters (`*highly recommended whenever possible to target specific assets in a collection`)

- [+] Supports Additional Custom Asset(*NFT) Filters  (Asset Qualifier Settings) => `**Used to additionaly filter out assets qualified to bid on`
- - +} Fixed Price (** Additionaly Filters each Asset based on a fixed price, ie. bids on asset if asset's current highest bid price is the same as the fixed price)
- - - Input Value:
- - - - [*] [Fixed Price] in Weth/selected PaymentToken`

- - +} Price Range  (**Additionally Filters each asset based on a price range, ie. bids on asset if  asset's current highest bid price is within range)
- - - Input Values:
- - - - [*] [Minimum Value] in Weth/selected PaymentToken
- - - - [*] [Maximum Value] in Weth/selected PaymentToken

- [+] Supports 3 Custom Bid Settings (Offer bid Settings) => {`**Used to dictate how the bid/offer amount is calculated`}
- - +} Fixed Price (** Bid's Offer amount will be same as the fixed price)
- - - Input Value:
- - - - [*] [Fixed Price] in Weth/selected PaymentToken

- - +} Percentage (** Bid's Offer amount will be {percentage(%) of current asset's highest bid} above in Weth/selected PaymentToken)
- - - Input Value:
- - - - [*]  [Percentage(%)] of current asset's highest bid (Supports up to 1dp, ie. 12.4%)

- - +} Points Above (** Bid's Offer amount will be {X points above current asset's highest bid} in Weth/selected PaymentToken)
- - - Input Value:
- - - - [*] [Points Above] current asset's highest bid in Weth/Chosen Token

- [+] Supports Weth(Default) & Polygon Eth Payment Tokens

- [+] Supports Custom Offer Expiration time in number of days
- - +} Expiration (** Offer expiration in number of days)
- - - Input Value
- - - - [*] [Expiration] Offer expiration in number of days
- [+] Auto Signing with Account Private Key (** Works with Metamask etc...)
- [+] Works on Testnet(*Rinkeby) & Mainnet


[ ** Required User settings ]
================================
=> For Security reasons, all information we consider sensitive User settings are added as `ENVIRONMENTAL_VARIABLES` in a `.env` file

Environmental Variables:
- [+] `WALLET_ADDRESS`
- - -- User Account Wallet Address
- - - --> Required in Creating, Hashing & Signing the offers

- [+] `WALLET_PRIVATE_KEY`
- - -- User Account's Private Key
- - -  --> Required in Signing the offers

- [+] `NETWORK`
- - -- Ethereum Network to use
- - - --> Testnet(Rinkeby) -- Offers will be made on Opensea's Testnet Assets, can use to test if your settings work as required
- - - --> Mainnet --  Offers will be made on actual Opensea Mainnet(Live/Real) Assets, **NB : THESE ARE LIVE OFFERS BEING MADE**

- [+] `WEB3_INFURA_PROJECT_ID`
- - -- Infura Project ID
- - - --> Requires an Infura Account

[ How it Work]
=================

1. Bot Takes 4 Inputs:
- - [+] \*\***Collection url** `(**Mandatory)`
- - - -- Opensea Collection url with it's included collection url filters if any

- - [+] **Asset Qualifier Settings** {Optional(recommended), if not set will bid on all assets recieved after Opensea Collection Filter if any}
- - - -- Used to additionaly filter out the assets qualified to bid on based on an asset's current highest bid price

- - [+] \*\***Bid Settings** `(**Mandatory)`
- - - -- Used to dictate how the bid/offer amount is calculated

- - [+] **Expiration** {Optional, if not set defaults to 7 days}
- - - -- Used to set offer expiration time


2. Pulls the Collection's Assets from Opensea and applies all the Collection Filters, if any


3. Applies any Asset Qualifier Filters(\*\*Additional Custom Filters set by the User) on each asset, if any

4. Calculates bid price for each of the qulified assets based on the Bid Settings set by the User

5. Creates, Signs and Posts offers to each of the qualified asset based on:
- - [+] **Selected Network**
- - [+] **User Calculated Bid Price**
- - [+] **Selected payment Token**
- - [+] **User Current Wallet Balance**
a




## Credit

This landing page theme is built on [shorthand css framework](https://github.com/shorthandcss/shorthand)

![preview](/preview.jpg)


* Picture [unsplash](https://unsplash.com)
* Icons [feathericons](https://feathericons.com)
