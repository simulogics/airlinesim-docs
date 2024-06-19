---
title: "Payment System"
weight: 4
---

# Payment System

AirlineSim utilizes a payment model that is geared towards fairness, transparency and ease-of-use.

This article covers everything you need to know about credits, credit consumption, prices, payment methods and the game's premium features. If you have any questions regarding the payment process, please refer to our [Payment FAQ]({{< relref "docs/faqs/payments.md" >}}).

## Motivation

AirlineSim is a very niche game (= comparatively few active players). It is also intended to be a serious business simulation, and its servers run elaborate simulation models that are very resource-intensive (= high operational costs). 

With this in mind, there are certain requirements our payment model needs to meet:

1. It has to cover fairly high costs per active player.
2. It has to be flexible enough to account for different usage intensities, like different amounts of active holdings per player or long-running game worlds.
3. It must not provide any in-game advantages for real-world money besides an initial "anti-cheat unlock" through a single purchase (details below).
4. It has to generate enough revenue despite a relatively small playerbase.
5. It still needs to allow for perpetually free game play for players who are unable or do not want to spend money.
6. It has to be as fair as possible to players because that is just something we care about.

These requirements rule out most common payment models:

- A **single purchase** would not cover ongoing server costs.
- A mandatory **recurring subscription** tricks players into paying even after they have stopped using the game, is not very flexible and causes higher technical and administration complexity.
- And **ad-supported model** is just "meh" and likely would not generate enough revenue to cover our expenses due to low player numbers.
- Most **free-2-play models** are out because they either require **pay-2-win** mechanisms which are a no-go for a serious simulation like AirlineSim and/or rely on **exploiting a handful of players** for pointless cosmetics, something that is neither fair nor feasible given AirlineSim's size.

Consequently, we implemented a system based on credits that has served us very well over the years.

## Credits: Our Payment Model in a Nutshell

Our payment model revolves around so-called **credits**. After signing up for AirlineSim, your account starts out with a balance of **60 free credits**.

In most game worlds, you are charged a small amount of credits for every [holding]({{< relref "docs/advanced/setup/holdings-vs-subsidiaries.en.md" >}}) you create. This amount varies depending on the duration of the game world. But given the initial amount of free credits and the typical cost of a short-term game world of 4 credits/day, you could try such a game world free of charge for as long as 15 days.

Once the credits run out, you need to recharge your account to continue playing. As such, the credit system is a prepaid model and thus completely flexible. Buying credits does not constitute a recurring subscription. You can buy credits whenever you like. If you ever decide to stop playing the game, all you have to do is let your credits run out.

And that's almost it! There's one caveat: There is a difference between free accounts, meaning such that have never completed a payment, and premium accounts, meaning such that have at some point completed at least one payment. But we will touch on that below.

## Credit Consumption & Running out of Credits

Once you create a holding, credits are deducted from your account on a daily basis. In game worlds where you can create more than one holding, discounts apply to every additional holding.

Currently, the typical costs are as follows:
* short-term worlds: 4 credits/day (2 per additional holding)
* medium-term worlds: 5 credits/day (3 per additional holding)
* long-term worlds: 6 credits/day (4 per additional holding)

If you run out of credits, your account's holdings and companies will be locked until you top up your balance. Credits will still be subtracted at the normal daily rate during this period, meaning your balance will become increasingly negative. The intention here is to prevent companies from gaining an unfair advantage by abandoning accounts and returning to them several weeks later, having avoided paying for their growth and the in-game resources they occupied in the meantime.

{{< hint info >}}
**Example**  
If an account owns one holding in a short-term game world and runs out of credits, it will have a balance of -20 credits after 5 days. These must be paid before access to the game is restored.
{{< /hint >}}

If an account's credits balance stays negative for more than 28 days, **all holdings and airlines** of that account will be deleted **in all game worlds** in order to free blocked in-game resources like slots and aircraft that would otherwise remain inaccessible to other players. The AirlineSim account itself will remain active and its credit balance will be automatically topped up to the initial 60 credits, effectively resetting your account to its initial state. If it had premium status before, it will keep it beyond the reset. 

Please keep in mind that the grace period of 28 days applies to premium accounts which have previously purchased credits. For trial accounts, it takes 7 days after running out of credits until the airlines are deleted.

{{< hint danger >}}
**Danger!**  
Note that automatic deletions due to a negative credit balance affect **all game worlds** an account has holdings in, **including free ones**!
{{< /hint >}}

## Playing for Free: Free vs. Premium Accounts

AirlineSim offers free short-term game worlds, meaning no credits are charged to play there. As such, you could play AirlineSim without paying a cent indefinitely. 

But there are some limitations: Unless you have completed at least one payment, your account remains in a **free or trial** state. This means that some features of the game are unavailable to you even when playing in free game worlds.

The majority of those features imply direct interaction between multiple accounts and the requirement to complete at least one payment is a very effective anti-cheat mechanism. Features in this category are:

* Creating more than one holding
* Multiple airlines in one holding
* Offering or accepting private contracts (for example for leasing out aircraft or interlining)
* Selling aircraft
* Bidding on non-official aircraft offers
* Layoffs (as fired staff ends up in a pool available to other players)
* Stock exchange functions ([Initial Public Offerings]({{< relref "docs/advanced/finances/initial-public-offerings/index.md" >}}) and share trading)
* Player-owned buildings

There are a couple features that are restricted for mostly historic reasons. Back when current-generation AirlineSim launched - around 2007 - these features caused higher load on our servers and hence were restricted to premium accounts:

* [The Online Reservation System (ORS)]({{< relref "docs/advanced/bookings/online-reservation-system/index.md" >}})
* Integrated flight operations control

These restrictions will likely fall once those features are modernized.

## Pricing

AirlineSim offers a tiered pricing model with different package sizes, which allows you to choose the right amount of credits for every situation: Buy a small one if you just want to dip your toe into the water or get premium status cheaply. Buy larger ones if you intend to play for a longer time, benefiting from bulk discounts.

At the time of writing this, the smallest package at 50 Credits costs 2.49 EUR. So at this tier, a simple account with a daily consumption of 4 credits would cost around 6 EUR per month. At a much more common 500 Credits for 19.10 EUR, that price is already down to around 4.60 EUR.

You can find a full, up-to-date list of all prices and the respective bulk discounts on the [account management page](https://accounts.airlinesim.aero/account/credits).

## Payment Methods & Checkout

In order to buy credits for AirlineSim, simply log into your account and click on Buy Credits. Here you can choose your desired package size, optionally enter a voucher code (currently only outside of Steam) and select your payment method.

{{< hint info >}}
**Info**  
Currently, the following payment methods can be used during checkout: Credit or Debit Card (Visa, MasterCard, American Express), PayPal, paysafecard, Online Bank Transfer and Prepayment. If playing through Steam, all payment methods offered by Steam are available.
{{< /hint >}}

Please note: Which payment methods are actually available might depend on both the country you are paying from and the selected package size.

Once your payment has been processed, the credits will be added to your account.
