---
description: The mechanics of liquidity pools on DEX by the example of TGR/TON
---

# The mechanics of liquidity pools

<figure><img src="../.gitbook/assets/image (3).png" alt=""><figcaption><p>The mechanics of liquidity pools on DEX by the example of TGR/TON</p></figcaption></figure>

Please note that this material was created in order to familiarize with the specifics of the liquidity pools on [DEX Tegro.Finance](https://tegro.finance/). The given calculations are simulated for illustrative example.&#x20;

We do not claim that the following calculations are suitable for every cryptocurrency: all DEX have their own features, commissions and so on. We also want to emphasize that, among other things, it is necessary to take into account transaction costs of TON network.&#x20;

## Features of liquidity pools on DEX-exchange Tegro.Finance <a href="#features-of-liquidity-pools-on-dex-exchange-tegro.finance" id="features-of-liquidity-pools-on-dex-exchange-tegro.finance"></a>

DEX-exchange Tegro.Finance charges a commission of 0.4% for each exchange. Of the total commission, 0.25% is included in the liquidity pool and distributed among all liquidity providers.&#x20;

Becoming a liquidity provider on the DEX exchange, it is important to know a few key components:

* When tokens are withdrawn from the pool, their amount may differ from the amount initially transferred to the liquidity pool. This is due to the fact that in the process of exchanges, the pool structure changes according to the rebalancing algorithm, which is set by the DEX-exchange;&#x20;
* The final result is influenced by transaction costs of the network and commissions for depositing and withdrawing assets from the liquidity pool;&#x20;
* The amount of commission depends on the turnover. The higher the trading volume, the higher the income of the liquidity provider;&#x20;
* Keeping a cryptocurrency in a wallet can be more profitable than depositing tokens into the liquidity pool - if one of the cryptocurrencies is strongly rising or falling, then rebalancing the pool significantly reduces the volume of the rising coin;&#x20;
* The amount of commission is distributed between all liquidity providers: the higher the provider's share in the pool, the higher income he will be able to receive.&#x20;

### **Scheme of the liquidity pool on DEX**

Let's imagine a pool of 1500 TGR and 100 TON - we'll round up the values for better understanding. Here lies the constant product formula: x\*y=k, where x is TON, y is TGR, and k is a constant.&#x20;

For this liquidity pool, k = 100 TON \* 1500 TGR = 150,000. In the rate x/y = 100 TON / 1500 TGR = 0.07 TON/TGR, we can conclude that 1 TGR equals 0.07 TON.

<figure><img src="https://telegra.ph/file/4f9527c0d88cab33951e6.png" alt=""><figcaption><p>TON and TGR amounts in the liquidity pool (the number of TGR in the screenshot may differ)</p></figcaption></figure>

Let's assume that the new liquidity provider contributes 50 TON and 750 TGR to the pool, then k = 100 TON _(current pool volume in TON)_ + 50 TON _(TON volume added to the pool)_ \* 1500 TGR _(current pool volume in TGR)_ + 750 TGR _(TGR volume added to the pool)_ = 337,500.&#x20;

It turns out that the new participant's share of the pool is 33.33%, which is calculated as follows: 50 TON _(contributed by the participant)_ / 150 TON _(total number of TONs in the pool along with his share)_.&#x20;

The estimated value of the tokens contributed: 750 TGR \* 0.07 TON/TGR + 50 TON = 102.5 TON. &#x20;

<figure><img src="https://telegra.ph/file/647a7ec7bf9b50bb78f87.png" alt=""><figcaption><p>Pooling 50 TON and 750 TGR (the number of TGR in the screenshot may vary)</p></figcaption></figure>

Suppose that DEX-exchange receives an application to exchange 10 TON for TGR. In the liquidity pool goes: 0.25% / 10 TON = 0.025, i.e. in the pool goes 10.025 TON = 10 TON + 0.025 TON.&#x20;

To save k (337,500) there must be 2109.045 TGR left in the liquidity pool. You can get this number as follows: 337,500 / (150 TON + 10.025 TON) = 2109.045.&#x20;

In exchange for the 10 TON, the user receives 140.955 TGR = 2250 TGR - 2109.045 TGR. At the actual rate, 0.0709 TON/TGR = 10 TON / 140.955 TGR.&#x20;

<figure><img src="https://telegra.ph/file/f78e30def83f98a87d04a.png" alt=""><figcaption><p>Exchanging 10 TON for 140.955 TGR (the number of TGR in the screenshot may be different)</p></figcaption></figure>

As a result, the pool rate increased and will now be used to calculate the amounts of TGR and TON, when the new participants contribute liquidity to the pool: 160.025 TON / 2109.045 TGR = 0.07587 TON/TGR.&#x20;

The scheme is identical when TGR is exchanged for TON on the DEX exchange.&#x20;

Note: the equilibrium exchange rate will decrease, but the volume of TGR in the liquidity pool will increase due to the reduction of TON.

### **Final results of the liquidity provider**&#x20;

A user with a 33.33% share in the liquidity pool owns 702.9447 TGR = 33.33% \* 2109.045 TGR, and 53.3363 TON = 33.33% \* 160.025 TON.&#x20;

The specified amounts in TGR and TON will be received upon withdrawal from the liquidity pool.

{% hint style="warning" %}
Please note: The numbers are different from the original 750 TGR and 50 TON.&#x20;
{% endhint %}

The estimated value of tokens 702.9447 TGR \* 0.07587 TON/TGR + 53.3363 = 106.6687 TON.&#x20;

The difference with the initial valuation of deposited funds: 4.1687 TON = 106.6687 TON - 102.5 TON.&#x20;

{% hint style="warning" %}
Please note: the number does not coincide with the expected commission share: 33.33% \* 0.025 = 0.00833 TON. It is explained by the change of volumes of cryptocurrency TGR and TON in the pool, the estimation is carried out on the updated equilibrium rate.&#x20;
{% endhint %}

If the user did not become a liquidity provider, he would be left with 750 TGR and 50 TON, which at the new exchange rate: 750 TGR \* 0.07587 TON/TGR + 50 TON = 106.9025 TON.&#x20;

It turns out that the difference with the initial estimate is more: 4.4025 TON.&#x20;

The difference is explained by a decrease in the volume of TGR and an increase in TON as a result of the transaction: the pool participant exchanged his share of TGR for TON.&#x20;

{% hint style="info" %}
Impermanent loss are the difference between the results of depositing assets into the liquidity pool and retention them in a cryptocurrency wallet. Over time, due to the accumulation of commissions in the pool, it is possible to compensate for the resulting difference. If the asset price movement is too strong, the difference can become significant. It will take a long time and many exchanges on the DEX exchange for the commission income to become commensurate.&#x20;
{% endhint %}
