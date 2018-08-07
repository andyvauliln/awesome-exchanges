Proof of Stake Velocity: Building the Social
Currency of the Digital Age
Larry Ren∗
ren@reddcoin.com
www.reddcoin.com
April 2014
Abstract
Proof of Stake Velocity (PoSV) is proposed as an alternative to Proof of
Work (PoW) and Proof of Stake (PoS) to secure the peer-to-peer network
and confirm transactions of Reddcoin, a cryptocurrency created specifically
to facilitate social interactions in the digital age. PoSV is designed to
encourage both ownership (Stake) and activity (Velocity) which directly
correspond to the two main functions of Reddcoin as a real currency: store
of value and medium of exchange. Reddcoin can also function as the unit
of account in heterogeneous social context. The technological aspects of
PoSV are presented after a detailed review of existing designs. The economic
aspects of Reddcoin are then analysed. Finally the unique position
of Reddcoin as a digital social currency in the competitive landscape of
cryptocurrencies is discussed.
1 Introduction
Bitcoin is among today’s most discussed and controversial topics. Ever since
Satoshi’s seminal paper [9] in 2008, Bitcoin has evolved from a technological
experiment embraced by a small group of computer enthusiasts to what some
today consider to be the most important innovation since Internet. Most recently,
there are new variants of Bitcoin, called altcoins, created everyday and a
whole new industry of altcoin trading exchanges, mining pools, gaming websites
emerged. Few topics today are more polarising than cryptocurrency. Some merits
of cryptocurrency touted by technologists are considered sins by economists.
Cryptocurrency is considered a movement by believers and a fad by disbelievers.
Instead of an open and honest discussion involving all sides, what we have witnessed
is a dialogue of the deaf, in which each camp justifies its own intellectual
laziness by pointing to the intellectual laziness of the other camps. This is one
∗The lead developer of Reddcoin, a.k.a. “laudney” PGP Public Key
1
of the main obstacles that prevent cryptocurrency from being accepted by the
general public.
What do we really know about this evolution? Is cryptocurrency just a technological
breakthrough or also an economic one [7]? Is mining cryptocurrency
a progress or retrogression [6]? Is cryptocurrency meant to replace government
and financial institutions or complement them? Is cryptocurrency designed for
hoarding or spending? And, the most fundamental question of all: is cryptocurrency
real currency or just virtual property for speculation [13]?
So far innovation in the cryptocurrency world has been almost exclusively
technical. Technologists have proposed improvement on various aspects of Bitcoin,
such as new hash functions [11] to replace SHA256 and new mechanism [4]
to replace Proof-of-Work. There have been very few cryptocurrencies designed
to address the economic and social aspects of being a real currency. Reddcoin,
at the time of writing, seems to be only one.
We write this paper with three goals in mind: 1) to give a broad overview
of the current issues around cryptocurrency, both technological and economic,
which might not have been foreseen by the original designers. 2) to address
these issues with proposals which require coordinated changes in both low-level
network protocol and high-level economic and social ecosystem. 3) to encourage
a more open and objective discussion of cryptocurrency by the general public
and promote a more complete thinking for future innovation in cryptocurrency
world.
The rest of the paper is organised as follows. Section 2 describes in detail
the merits and drawbacks of Proof-of-Work (PoW) and Proof-of-Stake (PoS)
from both technological and economic points of view. PoSV is then proposed
to address those drawbacks in the specific context of a digital social currency.
The technological design choices of PoSV are given in broad strokes. More detailed
technical analyses will be presented in a companion paper [12]. Section
3 addresses the most common criticisms by economists on cryptocurrency and
shows how Reddcoin and PoSV together provide new answers and new opportunities
for social research in general. Section 4 emphasises the main differences
between Reddcoin, a digital social currency which focuses on integration with
human social interactions and aims to concretise and quantify people’s intangible
asset of social influence, and the much more common digital commercial
currencies which aim to facilitate transactions of goods and services and offer
protection from hyperinflation.
2 Technology
A cryptocurrency uses principles of cryptography to implement a distributed,
decentralised and secure cash system. It solves the problem of double-spending
in a distributed ledger by introducing a mechanism to secure the network against
51% attacks and Distributed Denial of Service (DDoS) attacks. The underlying
principle of such a mechanism is the necessity of expending resources when confirming
transactions. Once confirmed, transactions become irreversible because
2
it’s practically infeasible for any attacker to have access to the huge amount of
resource required to modify them. Different mechanisms use different types of
resources.
2.1 Proof of Work
A Proof-of-Work (PoW) is a piece of data which is costly to produce so as to
satisfy certain requirements but is trivial to verify. Bitcoin uses the Hashcash
PoW [1]. Mining, the process of producing PoW, plays the central role in creating,
distributing and securing Bitcoin and many its variants. The most common
criticism of PoW mining is its massive waste of energy. At the time of writing,
the total daily revenue of mining Bitcoin is around 1.8 million USD. Depending
on the aggregate profit margin and the fraction of overall cost that electricity
accounts for, we estimate the daily total electricity cost at between 200K and
500K USD. In addition to this wastefulness, there are several more reasons why
mining remains a very controversial aspect of PoW cryptocurrencies.
2.1.1 Mining Arms Race
Mining is by nature extremely competitive. Mining costs include initial expenditure
on equipment plus on-going energy cost. Miners are predominantly rational
profit seekers. Their top concern is how long it takes to recover the initial cost,
i.e. the length of Return on Investment (ROI). During the very early age of
Bitcoin, mining was carried out by CPU. When mining later became available
on graphics cards (GPU), mining on CPU became immediately loss-making. As
Bitcoin price continued to soar, mining operation witnessed a mini industrial
revolution. Application Specific Integrated Circuit (ASIC) designed to carry
out PoW computation at several magnitude higher speed and lower energy cost
started to emerge and soon rendered GPU mining obsolete. This relentless arms
race causes constant worry among average miners who usually fail to recuperate
initial investment and cannot afford continuous hardware upgrade.
Bitcoin uses SHA256 [10] as the hash function in PoW and is the first to
experience this arms race. The same arms race is happening to cryptocurrencies
that use the Scrypt hash function [11]. Scrypt was initially touted as “ASICresistant”
due to its heavier memory usage. In reality, ASIC-resistance is one
of the most misleading and over-abused marketing slogans in the cryptocurrency
world. The correct word is “ASIC-ignored”. ASIC can be designed and
manufactured to perform all hash functions. The entry barrier is not technical
but financial. Unless there is sufficient market demand for mining Scrypt-based
cryptocurrencies, it’s simply financially unprofitable for manufacturers to invest
in the production of such ASICs. While Scrypt is under the threat of ASIC,
many cryptocurrencies have been created to use alternative hash functions such
as Scrypt-N, Scrypt-Jane and X11. These cryptocurrencies all market themselves
as the “latest and best generation of” ASIC-resistance when this resistance
is entirely dependent on being a minority. It’s deeply self-contradictory
3
for a cryptocurrency to pitch ASIC-resistance as its main merit to gain wide
adoption when this sole merit depends on it being unpopular.
In theory, it can be preferable to have separation between mining a cryptocurrency
and using it. It’s more efficient to leave mining operation to specialists
who use their domain knowledge to achieve economy of scale. This is
indeed the case for Bitcoin, the most established cryptocurrency. However, for
many newly created variants, average GPU-miners make up the vast majority
of user communities and the fear of ASIC directly threatens their social fabric.
2.1.2 Miner Incentive
Miners provide a paid service to cryptocurrency networks. They are all profit
seekers first and foremost. At a fixed cost, it’s perfectly rational for them to
mine the most profitable cryptocurrency and sell it quickly on market to limit
exposure to price risks. Hence were born the so-called “multipools” which fully
automate this process. Multipools create two new problems in the cryptocurrency
world.
First, the profit-seeking by multipools pushes many cryptocurrency prices
to just above mining production cost. As mining production costs inevitably
go down due to technological advances, many cryptocurrency prices suffer from
downward death spiral, which hurts the morale of the corresponding communities.
Second, multipools employ strategies that exploit the lag in readjustment
of difficulty of PoW. Multipools switch to a cryptocurrency with low difficulty
and keep mining it while its difficulty gradually catches up. The moment the
difficulty rises to its fair value, multipools switch again. As a consequence, multipools
mine blocks at a significantly lower average difficulty than other miners.
Although from a pure Darwinian point of view multipools help improve market
efficiency and filter out the weakest, they do force most cryptocurrencies
to focus on extremely short-term interests rather than long-term growth and
innovation.
2.1.3 Manufacturers of ASIC Mining Equipment
To be the most profitable miner, one must be the first to get hold of the latest
equipment that offers the highest hash rate per unit of cost. Therefore manufacturers
of ASIC mining equipment have strong financial incentive to use their own
product for mining first and only start shipping equipment to buyers after mining
profitability drops enough. This inherent conflict of interests has profound
impact on every aspect of the mining business. For example, the vast majority
of manufacturers ask for prepayment in exchange for a promise. The actual delivery
is usually delayed by months, which reduces mining profitability for their
buyers to almost zero. Manufacturers often offer no refund for shipping delay or
product defect in their terms and conditions, effectively eliminating their own
liabilities and openly exploiting the desperation of buyers. All these frustrations
reduce the confidence of average miners and undermine the soundness of PoW
mining as the guardian of cryptocurrencies’ decentralised networks.
4
2.2 Proof of Stake
Proof-of-Stake (PoS) is an alternative to PoW first introduced in Peercoin [4].
The resource used by PoS is “coin age”: currency amount times holding period.
Similar to energy, coin age as a resource is expensive to amass in huge quantity.
For an attacker to accumulate enough coin age to attack the distributed network,
he either has to buy on open market a large amount of the very currency he’s
trying to attack, driving up its price during the process and diminishing his
economic incentive, or hold coins for a very long time, reducing the frequency
of his own attacks.
One useful feature of PoS is the significant saving in energy consumption.
Another main feature is the better alignment of incentives between miners and
stakeholders because miners are now the stakeholders. PoS however has several
limitations:
2.2.1 Initial Distribution
PoS by construction relies on a fair and wide distribution of a cryptocurrency
but doesn’t deal with the logistical issue of how to achieve this fair distribution
in the first place. By comparison, mining in PoW, despite all its drawbacks,
also serves as a potent channel of distribution. This chicken-and-egg problem
was and remains a major challenge for all PoS cryptocurrencies. So far there
have been two popular workarounds: a) “pre-mine”, i.e. similar to subscription
to stock IPO in financial markets and b) a hybrid system of PoW and PoS with
PoW gradually fading away after an initial period.
The main criticism of “pre-mine” for PoS coins is its lack of guarantee of
either fair or wide adoption. The vast majority of “pre-mine” turned out to be
fraud. For those which were not, investors and speculators with deep pockets
can easily control a large stake in the currency, transforming its nature into
more as a speculative vehicle than a currency. Over-concentration of stakes also
increases the security risk of the decentralised network.
The PoW-PoS hybrid system alleviates these concerns by running PoW and
PoS in parallel. PoW mining works as both a steady distribution channel and
a fall-back network security mechanism. As PoW block rewards go down over
time, PoS has enough time to move to the spotlight.
Unfortunately, it doesn’t matter what particular model a PoS cryptocurrency
uses for initial distribution. The mere knowledge by the public that a
cryptocurrency will eventually rely on PoS compromises its ability to achieve a
fair and wide distribution. This is the inherent paradox of Proof-of-Stake.
2.2.2 Hoarding
The entire PoS network depends on coin age as the scarce resource. Coin age
can only be earned by holding coins. To earn coin age at a higher rate than
others, one must hold more coins. Coin age is consumed when a coin is spent
in a transaction. PoS mining requires a user to repeatedly send coins to herself,
thus consuming his reserve of coin age in exchange for probabilistic winning
5
a PoS block reward without reducing the size of the holding. Coins spent in
transactions facing other users also have their coin age reset to zero but this
consumption of coin age is outside the scope of PoS mining, unqualified for block
rewards and is considered a “waste” by most PoS stakeholders.
It now becomes clear that PoS has been designed to encourage hoarding
and discourage spending. Some PoS coins, such as Peercoin, openly declare
their philosophy to “function more as a long-term store of value than medium
of exchange.” In this sense, PoS coins are created to be collectibles rather than
currencies. Scarcity is a necessary but insufficient condition for collectibles to
have value. Collectibles must also offer some form of utility such as aesthetics
and historic significance. Considering the fact that anyone can access and modify
the source code of PoS coins and potentially offer an improved version, in
theory there is infinite supply. The scarcity condition doesn’t hold. It remains
an unsolved puzzle where PoS coins marketed as collectibles derive their value
from.
2.2.3 Full Nodes
PoS transforms all stakeholders into miners. All they need to do to collect
interest rate is to leave their wallets running and connected to the PoS network
and participate in the confirmation of transactions. Wallets which stay online
for extended periods of time are called full nodes. Staying online seems to be a
rather simple requirement. So it comes as quite a surprise that PoS coins tend
to suffer from insufficient number of full nodes. This seeming paradox can be
explained by two reasons.
First, coin age equals number of coins times holding period. It doesn’t
matter whether a wallet is connected to the PoS network during the holding
period. An offline wallet accumulates coin age at the same rate as an online
one. The only difference is that an always-online wallet receives block rewards in
a fashion that’s more evenly spread out over time while an occasionally-online
wallet receives block rewards in a few concentrated clusters. This difference
alone is insufficient to encourage most stakeholders to stay online.
Second, it’s commonly perceived by average PoS stakeholders that running
wallets and staying connected for long periods of time significantly increases
security risk. This was a particularly grave concern when early versions of PoS
wallets didn’t support wallet passphrase during mining. Since then there has
been workaround to reduce the security risk.
By considering the two reasons above, an average PoS stakeholder tend to
make the rational decision of connecting to PoS network only sporadically. The
lack of sufficient number of full nodes can result in higher risk of security breach
on PoS networks.
2.2.4 Mining on Multiple Forks
In PoS mining, each stakeholder spends coin age while looking for the next valid
block. If another stakeholder finds a valid block first, the coin age consumed in
6
the unsuccessful attempt is fully reimbursed.
Forks do happen on all distributed networks of cryptocurrencies. PoW addresses
this issue by enforcing at protocol level that the blockchain with the
largest sum of difficulty always wins. This allows all the nodes on the network
to converge on a consensus rapidly. Miners all have the clear incentive to mine
blocks only for the most difficult blockchain. Mining for any other fork is almost
guaranteed to be wasteful. The situation is very different when it comes to PoS.
When there are multiple forks on a PoS network, by the nature of the
blockchain, a stakeholder has the same stake replicated across all the forks.
Technically the stakeholder can simultaneously mine on all these forks by running
multiple copies of the wallet. What causes the biggest trouble is the fact
that PoS protocol picks a winning blockchain based on length. And length of
a blockchain in a decentralised network heavily depends on timing. It can be
quite common for different subsets of the network to have different ideas about
which blockchain is the longest while the information is still being propagated.
The lack of synchronisation of network time further complicates it. It’s a much
less robust way, compared to PoW, to reach a consensus. PoS can’t use the sum
of difficulty in blockchains as the criteria for chain selection because difficulty
in PoS is adjusted by each stakeholder based on their consumption of coin age
and therefore remains local knowledge. There is no network-wide agreed-upon
block difficulty.
When stakeholders on PoS networks find it difficult to pick the blockchain
winner, they have the incentive to “bet on all horses” by simultaneously mining
on all the forks. This significantly aggravates network security. Most PoS coins
alleviate, but don’t solve, this problem by enforcing “duplicate stake detection”
at client wallet level but not at protocol level. They also argue that in practice
the financial rewards for multi-fork miners are small enough to deter such
attempts.
2.3 Proof of Stake Velocity
2.3.1 What is Velocity of Money
The velocity of money is the frequency at which one unit of currency flows
through an economy while being used by members of the society within a given
time period [3]. All else being equal, a higher velocity of money indicates a
more flourishing economy, richer members and a healthier financial system. The
formula to measure velocity of money in a given time frame is the follow:
VT =
nT
M
where VT is the velocity of money; nT is the aggregate notional of transactions
and M is total amount of money in circulation. In an economy, we can also
replace nT with nQ which is the nominal national or domestic product. In other
words, given a fixed amount of money in circulation, velocity of money must be
increased in order to increase the size of the economy.
7
2.3.2 Higher Velocity for A Better Economy
The vast majority of the drawbacks of PoW and PoS aren’t due to flaws in
technical designs but the disconnect from the economic and social aspects of
being a real currency. It’s fair to say that most cryptocurrencies are created
as technological products but “mis-sold” as currencies. PoSV builds upon the
strength of PoS and introduces new features to address its flaws. PoSV is
designed to encourage both ownership (Stake) and activity (Velocity), the two
main criteria of being a social currency. It must be emphasised that PoSV
is designed specifically for the digital social currency Reddcoin and is never
intended to serve as a drop-in replacement for other cryptocurrencies that don’t
share the same economic and social goals. PoSV should be evaluated as a piece
in the Reddcoin ecosystem and not stand-alone.
Given a fixed amount of coin, coin age is calculated as a function of time.
Let’s denote this function the coin-aging function. The form of the coin-aging
function is of ultimate importance. It not only decides the growth rate of coin
age as a resource over time via its first derivative, but also decides the utility
function of stakeholders. The main limitations of PoS, too much incentive for
hoarding and too little incentive for staying online, result from the fact that the
form of its coin-aging function is linear. The linear form leads to a constant
coin age growth rate and a utility function that disobeys the law of diminishing
returns.
Changing the form of coin-aging function has profound impact. For example,
let’s assume coin-aging function in PoSV is an exponential decay function. The
coin age growth rate gradually decreases with time. The exponential decay
constant is chosen to achieve a particular half-life such as 1 month. Each coin
accumulates one coin day per calendar day during the first month, half a coin
day per calendar day during the second month, a fourth of a coin day per
calendar day during the third month etc. As the holding period of a coin
approaches infinity, the total accumulated coin age asymptotically approaches
2 coin months.
This exponential decay function dramatically changes stakeholders’ incentives.
New coin accumulates coin age at much higher rate than stale ones.
With a fine-tuned half-life, PoSV encourages stakeholders to be active in moving
their holding, either by mining or transacting with counterparties, both of
which increase money velocity and improve the health of the Reddcoin economy.
Stakeholders are also encouraged to stay online and contribute to verifying
transactions on the PoSV network. The asymptotic limit of coin age due to exponential
decay function provides extra security for the network. The maximum
amount of coin age a stakeholder can earn now equals coin amount times twice
the half-life. This significantly increases the difficulty for 51% attacks.
The coin-aging function can take on other forms. Linear and exponential
decay functions are both monotonic. What about trigonometric functions which
are non-monotonic and periodic? Non-monotonicity produces positive and negative
growth rate of coin age at different points in time which along with periodicity
translate into rewarding and penalising holding with a seasonal pattern.
8
This can be used to fine-tune the seasonality in money velocity. The bottom line
is that PoSV is designed to accommodate different forms of coin-aging functions
in order to implement the necessary monetary policies in the Reddcoin economy.
To alleviate the problem of mining on multiple forks, PoSV helps the nodes
to reach a quicker consensus by giving preference to the head block with the
largest sum of coin day spent among all the transactions.
3 Economics
There has been extensive economics debate about Bitcoin. Most economists
remain unconvinced of Bitcoin’s status as a real currency. Reddcoin and PoSV
are designed to address some of those concerns and offer new angles to reexamine
the questions.
3.1 Medium of Exchange
There is largely consensus on Bitcoin’s function as a medium of exchange. In
fact, almost all the merits of Bitcoin talked about today boil down to how it
acts as a better medium of exchange, e.g. global reach, lower fees, much quicker
transaction and easy to use. However, the fact that the Bitcoin network must
be secured by “mining” which expends real resources (energy) is considered by
many economists to be a drastic retrogression [6] - a retrogression that Adam
Smith scorned at in his immortal work The Wealth of Nations written in 1776.
By comparison, PoSV and PoS mining require little energy consumption and
can be done by any average user on any computer and even mobile device.
3.2 Unit of Account
Many economists point out that Bitcoin cannot be used as the base currency
for accounting or tax-reporting and therefore fails as a unit of account. Interestingly,
the german finance ministry has officially classified Bitcoin as a unit of
account. More and more merchants start to accept Bitcoin for payment. Especially
in the world of cryptocurrencies, Bitcoin has assumed the special status of
a reserve currency and is the choice of denomination for more and more goods
and services. Reddcoin and PoSV bring a whole new question: what is the “unit
of account” for human social interactions, if any?
Currently social interactions are quantified in different ways on different
social networks. On Facebook, it may be measured in the number of Like and
Share; on Twitter, the number of retweets; on Amazon, the number and quality
of product reviews; on blogs and forums, the number of posts and replies. The
total lack of a universal yardstick makes it impossible to measure and compare
social interactions in heterogenous context. In other words, there is no unit
of account for human social interactions right now. Social influence remains a
significant yet opaque asset.
9
Reddcoin is created to fill this gap by becoming the first digital currency
integrated with all major social networks and serving as the “unit of account” for
social interactions in the digital age. Inside the distributed ledger of Reddcoin,
transactions can be interpreted not only in pure financial terms but also as
proxies for human behaviours. Researchers in social sciences have long been
looking for a way to track, organise and study human social behaviours on large
scales. Reddcoin offers a unique global platform for these areas of research and
open up new possibilities for value-add services.
3.3 Store of Value
Economists are largely skeptical of Bitcoin’s function as a store of value. They
compare Bitcoin with gold and US dollars and point out its lack of a fundamental
floor of the value [2]:
Underpinning the value of gold is that if all else fails you can
use it to make pretty things. Underpinning the value of the dollar
is a combination of (a) the fact that you can use them to pay your
taxes to the U.S. government, and (b) that the Federal Reserve is
a potential dollar sink and has promised to buy them back and
extinguish them if their real value starts to sink at (much) more
than 2% per year. Placing a floor on the value of Bitcoins is what,
exactly?
PoSV, PoW or PoS by itself doesn’t provide a fundamental floor for the
value of a cryptocurrency. However, Reddcoin, the digital social currency that
PoSV is specifically designed for, does enjoy a floor of its value due to its aim to
function as the global reserve currency of human social influence. Humans are
by nature social animals. Social activities are embedded into the very fabric of
societies. As Aristotle famously pointed out in Politics:
Society is something that precedes the individual. Anyone who
either cannot lead the common life or is so self-sufficient as not to
need to, and therefore does not partake of society, is either a beast
or a god.
Based on Aristotle’s insight, underpinning the value of Reddcoin is simply
its utility of helping humans be human.
3.4 Deflation vs Inflation
Any discussion of monetary system is incomplete without discussing inflation.
Bitcoin and many of its variants were created with a deflation model in which
the total quantity of the cryptocurrency is capped. In effect, Bitcoin has created
a modern digital version of the gold standard world in which the money supply
is fixed rather than subject to increase via printing press.
10
Bitcoin advocates believe deflation is a virtue by preserving the value of
Bitcoin versus inflationary fiat currencies and thus making it a better store of
value. Bitcoin price has indeed soared in the last few years, further validating
the merit of deflation in its supporters’ mind.
However, deflation and a soaring price both provide strong incentives for
people to hoard Bitcoin rather than spending it. Indeed, according to [8], as
much as 64% of Bitcoin was never spent in 2013. To make matters worse,
prices of goods and services when measured in Bitcoin have plunged; the Bitcoin
economy has in effect suffered a major depression [5].
PoS and PoSV both employ an inflation model with fixed nominal interest
rate. For example Peercoin adopts a nominal interest rate of 1% per annum
compared to PoSV’s 5%. Central banks in developed countries, e.g. Bank
of England, European Central Bank and Federal Reserve, have a long-term
inflation target of around 2%. PoSV chooses 5% because Reddcoin, as the
digital social currency, should encourage more spending, i.e. social interactions,
than other cryptocurrencies which do not share this goal. Also given the global
nature of social networks which involve users in both developed and emerging
markets, 5% seems to strike the balance. The monetary system of Reddcoin is
not created to make people who hold money rich, but to facilitate transactions
and make the Reddcoin economy as a whole rich.
4 Digital Social Currency
4.1 Social vs Commercial
A commercial currency is the most common form of currency. Its main function
is to facilitate transactions in exchange for goods and services. Bitcoin and its
variants have been pushed as the latest innovation of commercial currencies and
compete head-to-head with fiat currencies, such as USD and EUR, for shares of
commercial transactions in the global economy.
A social currency is of an entirely different nature. According to Wikipedia:
Social currency is a common term that can be understood as
the entirety of actual and potential resources which arise from the
presence in social networks and communities, may they be digital
or offline. It derives from Pierre Bourdieu’s social capital theory
and is about increasing one’s sense of community, granting access
to information and knowledge, helping to form one’s identity, and
providing status and recognition.
Very recently, a small but growing number of companies have come to embrace
the concept of “social currency”, allowing customers to pay via Facebook
posts, Twitter tweets and other social media content. However the lack of a
yardstick to measure the “fair value” of social media content and influence is the
main obstacle. To our knowledge, Reddcoin is the only digital social currency
11
that was created, designed and continuously evolves to become the “reserve currency”
of people’s social interactions. Reddcoin has two main objectives: 1) to
concretise and quantify one’s intangible asset of social influence, and 2) to facilitate
social interactions within and between social networks, both online and
offline. Reddcoin doesn’t compete with commercial currencies, fiat or digital,
but rather complement them. Merchant support is encouraged, especially when
the commercial activities form parts of a collective social experience. But the
social aspect will always remain the utmost focus of Reddcoin.
The three most important assets in the ecosystem of Reddcoin are brand,
community and infrastructure. Reddcoin developers always go to great length
to create a brand that’s professional, friendly and consistent. Great care is taken
to foster a community that share a clear long-term mission and the same set
of values of being friendly, helpful, generous, caring and rational. All system
infrastructure is built with special emphasis on providing a uniform, simple and
secure user experience.
4.2 Transition from PoW to PoSV
Reddcoin was launched in January 2014 and is still using PoW. Since the very
beginning, Reddcoin has been distributed to a large and diverse user base
through multiple channels that include one of the very few successful and honest
Initial Public Coin Offering (IPCO), mining, trading on multiple exchanges,
community promotion events, generous giveaways and user tipping on multiple
social networks such as Reddit, Twitter and Twitch TV. Reddcoin stakeholders
now include people from almost 100 countries, with diverse background, age
and interests.
At the time of writing, according to information at http://bitinfocharts.com,
Reddcoin has a fairer wealth distribution per wallet address than all the top
cryptocurrencies such as Bitcoin, Litecoin, Dogecoin and Peercoin. Reddcoin
also has 2 - 3 times more coin age spent today than all the other PoW cryptocurrencies.
Reddcoin, without PoSV, is already the currency with the fairest
stake ownership and the highest monetary velocity. In coming months, Reddcoin
will gradually transition from PoW to PoSV with new features added at
incremental pace.
4.3 Hard to Clone
There is no shortcut to cloning Reddcoin. In particular, the clone cannot adopt
PoSV from inception because, as discussed in section 2, the mere knowledge of
the eventual adoption of PoSV or PoS will lead to people hoarding from the very
beginning. To achieve a fair and wide distribution, an element of surprise at
protocol level plus dedicated efforts at community level are both indispensable.
Reddcoin’s existing brand, community, infrastructure and the publication of
this paper make it very difficult to duplicate what has already been achieved.
12
5 Conclusion
We have proposed Proof-of-Stake-Velocity (PoSV) as an alternative to Proofof-Work
(PoW) and Proof-of-Stake (PoS). We started by going through all the
major drawbacks of PoW and PoS and then showed how PoSV significantly reduces
the wastefulness of mining, eliminates mining arms race, averts the threat
of multipools and ASICs, avoids the inherent conflict of interests by ASIC manufacturers,
introduces new forms of coin-aging functions to discourage hoarding
and encourage spending and greater contribution to the network. General concerns
by economists toward cryptocurrency were discussed and addressed in
light of the recent development of Reddcoin and PoSV. In particular, Reddcoin
is well positioned to fill the niche of a digital social currency that’s tightly integrated
with human social interactions and acts as the yardstick to concretise
and quantify people’s intangible asset of social influence.
References
[1] Adam Back. Hashcash - A Denial of Service Counter-Measure. 2002.
[2] Brad DeLong. Watching Bitcoin, Dogecoin Etc... 2013.
[3] Joshua Kennon. The Velocity of Money for Beginners. 2012.
[4] Sunny King and Scott Nadal. PPCoin: Peer-to-Peer Crypto-Currency with
Proof-of-Stake. 2012.
[5] Paul Krugman. Golden Cyberfetters. 2013.
[6] Paul Krugman. Adam Smith Hates Bitcoin. 2013.
[7] Paul Krugman. An Ubernerd Weighs In. 2013.
[8] Sarah Meiklejohn, Marjori Pomarole, Grant Jordan, Kirill Levchenko, Damon
McCoy, Geoffrey M. Voelker, and Stefan Savage. A Fistful of Bitcoins:
Characterizing Payments Among Men with No Names. Internet Measurement
Conference, 2013.
[9] Satoshi Nakamoto. Bitcoin: A Peer-to-Peer Electronic Cash System. 2008.
[10] National Institute of Standards and Technology. Secure Hash Standard
(SHS). 2012.
[11] Colin Percival. Stronger Key Derivation via Sequential Memory-hard Functions.
2012.
[12] Larry Ren. Proof-of-Stake-Velocity: Technical Analyses. to appear.
[13] David Yermack. Is Bitcoin a Real Currency? An economic appraisal. 2013.
13
