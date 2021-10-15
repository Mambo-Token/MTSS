# MTSS
Mambo Token Security Standard MTSS

https://mambo.li/mambo-infos/mtss

Why this Mambo Token Security Standard?
Read why we needed to make the following security rules for our Stabelcoins an Mambo Token at the end of this page.

We hope this standard will become common use and minimal security standard for all tokens which claims to be decentralized.
MTSS is about burning and minting, other aspects of a fungible token contract code or functionality are not discussed.
There maybe use cases where it makes sense to Not apply the mtts standard. It is possible that exactly the function to burn tokens out of wallets or mint into wallets is wished and anybody knows about it - specially in some kind of games imaginable. But for most tokens this is just a no go.

Mambo.li wrote a token security standard MTSS for secure minting and burning for decentralized Stablecoins.
It contains minimum 5 points
with 12 test questions
and minimum 22 check smart contract transitions to check the questions.
Every check transitions should give the exepted error or true output.

-.-.-.-.-.-.-.-.-.-.-.-.-.-.-.-.-.-.-.-.-.-.

More test questions may be added in future.

Even with the strict impossibility to burn tokens of someones wallet,
the fact that the contract owner can mint or burn in itself is still a huge centralized power.
It is not easy to make it completely decentralized with those functions. But what can easily be done, must be done!
As it is with any currency, if a central authority over abuses it`s power over a currency, the trust in the currency shrinks and it begins to lose value.
The same will be true with any stablecoin or token where the contract owner abuses the minting or burning function concsiously or in good will or if the minting and burning is made with lack of understanding of the possible consequences or with bad timing or false quantity or simply with bad will.

.......
Expected results of the 22 transactions for the 12 test questions
1: 2x true, success (mint and burn)
2: 2x error 6 (not sender)
3: 2x error 5 (not minterburner)
4: error 4 (not owner)
5. true, success
6. 2x error 5, not minterburner
7. 2x error 6, not sender
8. 2x error 6, not sender
9. 2x true, success
10. error 4, not owner
11. 3x true, success
12. 2x error 5, not minterburner

Mambo Token Security Standard (MTSS) <br>

Requirements for decentralized Stable Coins and Tokens <br>

This applies only for Tokens, that are aimed to have the mint and burn function, as it is normally the case for any kind of stable coins, since the quantity of tokens is adapted to the supply and demand to help maintain the pegged price in the market.
For some other coins, only minting or only burning or both functions makes sense. But it must be clearly described in the tokenomy or withepaper why it has those functions.
A Stable Coin or Token that aims to be as decentralized as possible must have following functions and restriction:
1. Only the contract owner or delegated MinterBurner can mint or burn tokens.
2. The contract owner or MinterBurner can only mint into his account or burn from his account.
This makes abusive burn intervention by central authorities, blackmail, corruption or error impossible.
3. The delegated MinterBurner has no authority to delegated the mint or burn function to others.
4. The contract owner can take back the MintBurn function from the delegated minterburner to himself or delegate another one.
5. No one can burn his own tokens.
-.-.-.-.-
The following tests and checks should be made to make sure that the token contract code fulfills those requirements:
1. Contract owner can burn his token or mint into his account. True, true
2. Contract owner can burn others tokens or mint into others accounts: No, no
3. Anybody can mint or burn: No, no
4. Someone can self authorize ChangeMinterBurner to himself: No
5. Contract owner can delegate a MinterBurner: True
6. Contract owner can no longer mint or burn: true, true
7. New MinterBurner can mint to or burn form contract owner tokens: No
8. New MinterBurner can burn someone else token or mint to someone else: No
9. New MinterBurner can mint into or burn out from his account: true, true
10. New MinterBurner can delegate the mint-burn role to another account: No
11. Contract owner can take back the mint burn funciton: take back true, mint true, burn true
12. Old MinterBurner can no longer mint or burn: true, true
13. 
-.-.-.-.-.-.-.-.-.-.-.-.-.-.-.-.-.--.-.-.-.-.-.-.-.-.-.-.-.-.-.-.-.-.-.-.-.-.-.-.-.-.

Zilliqa testnet contract example which fulfills those requirements fully:<br>
zil1k3hxq95yxaf6urdzpp0kafcl8tglsnwymmn3uh
Token: Choco1 <br>
.....<br>
Zilliqa mainnet example:
Our first stablecoin FRANC Chocolate Stablecoin fulfills the MSST.
zil1z4hxwnqk9gu6tamcw4umxss9wjpmrkhzdh4n85 <br>
0x156e674C162A39a5F7787579B342057483B1Dae2 <br>
All mStabelcoins will fulfill the MSST, if not otherwise declared because of a specific reason.

.-.-.-.-.-.-.-.-.-.-.-.-.-.-.-.-.-.-.-.

Why this Mambo Token Security Standard?
During the developpment of our stablecoins we discovered to our surprise, that some good known tokens had a burning funcitonality, that allows the token owner to burn tokens out of any wallet.
This is diametral against any decentralized secure network, community or philosophy.
XSGD has it conciously in the code and names it "lawenforcementWipeBurn". This shows the typical presumptuousness of the totalitarian minded government controll freaks.
They just think they can steal others wealth out of their wallet, as they do with more and more unjustified taxes. To make such a lawenforcementWipeBurn they only need a corrupt judge to do so. Contemporary history shows, that they are mostly corrupt, justifiying rigged elections, child abuse, child murder, etc....
This is the reason, WE CANNOT TRUST fully XSGD as we cannot trust in any fiat or government (of the deliberate great reset destruction of society) and we will use xsgd only for trading, but not as collateral, or only at a minor percentage. We hope SGD is among the better fiat currencies, but we dont have any knowledge about local politics there.
And WE CANNOT TRUST in any other Token with such a dangerous burning function, even if they issued it unconsious of this possibilty.
Solutions for respectiv tokens were proposed, but NOT yet made.
We encourage it to make and one can "sell" it in a positiv way, if its a migration: Pointing out the advatages of the migrated token.
If it's multisig, that builds trust. That can be "sold", communicated without having to fear much of negativ impact or even positiv impact on the token!
1. migration to a new token version (with better burning (and minting) code).
2. transferring the minterburner account to a multisig account (better than nothing, but not best solution)
