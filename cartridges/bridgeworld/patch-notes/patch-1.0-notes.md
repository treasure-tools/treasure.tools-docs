# Patch 1.0 Notes

{% hint style="info" %}
Attention all Legions! Reveal of the Starlight Temple!
{% endhint %}

> _In this patch, we tackle concerns regarding inflation within Bridgeworld, crafting mechanics, clarify Harvesters and unveil the mysterious Starlight Temple._&#x20;
>
> _The core focus will be on reducing Treasure inflation and slowing down crafting._&#x20;

## Crafting Changes (Temporary)

As the community is already aware, the launch of harvesters will take longer pending audits, and we cannot provide exact dates when they will complete. In order to preserve the original game progression where dedicated crafters are building towards early access to harvesters, we will need to temporarily pause crafting EXP gains until harvesters are ready to safely launch.&#x20;

Pausing EXP gains is to our knowledge, a fair way to preserve the original timeline for ALL crafters, as it affects everyone equally, whether they started early or later. It avoids arbitrary cutoff points which would be unfair to some crafters.&#x20;

The longer lead time to harvesters also presents the possibility that many parts can be created and sold to unsuspecting buyers at large premiums meanwhile many more parts are created. This creates an adverse risk where buyers may both severely overpay and miss out on a place in harvesters. This would be a devastating outcome which we look to avoid.&#x20;

To offset this inconvenience, we will look to **temporarily reduce break rates by 50%** so you can still craft prisms, and mini crafts in the near future when released.&#x20;

EXP gain will be resumed **prior** to the release of the Harvesters.

**Updated (Temporary) Break Chance**

| Treasure Tier  | Probability that a Treasure will break during crafting |
| -------------- | ------------------------------------------------------ |
| Grin/Honeycomb | 0.15%                                                  |
| 1              | 1.37%                                                  |
| 2              | 2.70%                                                  |
| 3              | 3.44%                                                  |
| 4              | 5.65%                                                  |
| 5              | 7.67%                                                  |

## Summoning 2.0 Post-Corruption Era Changes

New summoning mechanics to increase the sustainability of Bridgeworld economy. The following changes incentives  opportunity costs and competition to slow down the growth rate of legions.&#x20;

**Adjustment A: Summoning now succeeds with a probability that**&#x20;

* Decreases with the number of legions simultaneously summoning (globally), and&#x20;
* Increases with the number of legions crafting (globally).
* Summoning Success Rate is **Global** (based on everyone playing Bridgeworld)&#x20;

{% hint style="danger" %}
**Summoning Success Rate Formula:**&#x20;

prob\_summon\_legion(N, k, s) = 1 / (1 + (N/k\*s)\*\*2)

* N: #current\_summoners
* k: #current\_crafters
* s: parameter to control sensitivity (currently set as s = 1, but subject to changes)
{% endhint %}

![Model of Summoning Success Rate](../../../.gitbook/assets/Screenshot\_32.jpg)

When summon fails:

* All MAGIC and prisms are refunded <mark style="color:red;">**after they return from the failed summon**</mark>
* Legion enters stasis, a **2** days lock which (cannot re-summon or engage in other activities)
* Failing with AUX legion will **NOT** count towards the 1 Summon Limit

This change links summoning to core Bridgeworld economic activities, aligning supply expansions more closely with the overall growth of active Bridgeworld users.

**Adjustment B: Increase in Summoning Time**

Base summoning duration increased from ~~7~~ => 10 days

Prisms reduce summoning time. Prisms are consumed to reduce summoning time&#x20;

* Small Prism: Decrease 12 hours (0.5 days)
* Medium Prism: Decrease 36 hours (1.5 days)
* Large Prism: Decrease 72 hours (3 days)

Prisms cannot be stacked.

{% hint style="info" %}
Prisms will now serve two purposes (1) increase odds of obtaining a rare legion and (2) decrease the base summoning duration (contingent on the prism's size).&#x20;
{% endhint %}

{% hint style="warning" %}
While this is a minor case of corruption, the Numeraires observed in some circles, further instabilities led to the need for additional prisms to improve the odds of success, and in some cases, a requirement to even initiate summoning.&#x20;
{% endhint %}

## Questing and Crafting

{% hint style="danger" %}
Adjustments **A** and **D** are <mark style="color:red;">**temporary**</mark> measures while we integrate more complex ones.&#x20;
{% endhint %}

**Adjustment A: Increase Questing Duration (Temporary)**

* "easy": ~~8 hrs~~ => 23.5 hrs
* "medium": ~~12 hr~~s => 35.5 hrs
* "hard": ~~16 hrs~~ => 47.5 hrs

**Adjustment B: Decrease Treasure drop rate from Quests**

* Treasures drop rate from quest down from ~~20%~~ => 15%

**Adjustment C: Increase Treasure Drop Rate**&#x20;

* Drop rate for T1, T2 and T3 Treasures are increased for Medium and Hard Quests&#x20;
* Medium quests: increase drop rates of \[T1, T2, T3] treasures ~~\[1.5%, 5%, 7%]~~ => \[2%, 5.5%, 8%] &#x20;
* Hard quests: increase drop rates of \[T1, T2, T3] treasures ~~\[2.5%, 9%, 8%]~~ => \[4%, 10%, 11%]&#x20;

![Updated Numbers](../../../.gitbook/assets/Screenshot\_29.jpg)

**Adjustment D: Increase Crafting Duration (Temporary)**

* "prisms": ~~24 hrs~~ => 47.5 hrs&#x20;
* "parts": ~~36 hrs~~ => 71.5 hrs
* "extractors": ~~48 hrs~~ => 71.5 hrs

**Adjust E: Update Harvester Parts and Extractor Recipes**

* Decreased the cost to craft both harvesters and extractors

![Updated numbers](../../../.gitbook/assets/Screenshot\_30.jpg)

### Rationale for Questing and Crafting Changes

#### The Issue

Since the launch of Bridgeworld, we have implemented Crafting as a key deflationary lever for Treasures to counterbalance the inflationary lever associated with Questing. From observing the data on 8 weeks of play, we saw an over-indexation of found Treasures being sold on the Marketplace versus being used for crafting.

This can be attributed to two key issues:&#x20;

1. The fear associated with breaking Treasures (especially when multiple break and/or rare Treasures being broken during the first craft).&#x20;
2. Lack of widespread utility associated with prisms

With the recent compromise to the Marketplace, we feel it is critical to take a slower and more methodological approach to ensure our products are peer-reviewed/audited for bugs. This, of course, includes the Harvester. Doing so will result in a slight launch delay.

This delay, by extension, will impact crafters who persisted with crafting since the inception of Bridgeworld (longer time intervals = more parts produced). At the core of Treasure’s ethos, however, we wish to reward active and engaged community members.

#### The Interim Solution

Given the aforementioned concerns, we felt that it would be best to significantly lengthen both questing and crafting times. Doing so serves multiple functions:

1. Control for the inflation of Treasures&#x20;
2. Give us time to carefully code and peer-review the Harvester contract.&#x20;
3. Not diluting the number of harvester parts to hit the market prior to the harvester release. By extension, this will ensure that hard working crafters are rewarded for their efforts.&#x20;
4. Allow us to review and implement more complex features (see [The Future](patch-1.0-notes.md#the-future)).

Given the multiple interconnected pieces (summoning, questing and crafting), these interim solutions provide us with more time to model different solutions (and their implications on Bridgeworld) to ensure that we can adequately test and refine more sustainable updates.

As a backup plan, crafting may also (a) have its duration increased further, and (b) be paused for a few days. This is done to ensure alignment in the release of harvesters and their parts.

We firmly believe that these short term (temporary) pains are necessary to ensure a healthy and sustainable economy in the long run. As with all economies, nothing remains static. As such, we will continue to refine and tweak gameplay as the meta and behavior changes, informed by observable data and close community engagement.

To this end, we hope that the Treasure community can believe in and continue to support us through this transition period.

### Rationale for Timing Changes

As an aside, we also received feedback about questing/crafting times being disruptive for individuals’ sleep patterns, with many users staying up late or waking up early to complete quests. In order to enable a more healthy experience, questing and crafting duration will be reduced by 30 minutes. This allows a small amount of leeway to restart these paths.

## Starlight Temple&#x20;

{% hint style="warning" %}
Using Essence of Starlight, a form of liquid Magic, Legions tattoo one of Bridgeworld's constellations onto their skin using ancient technology located at the Starlight Temple, mixing the Essence with their innate Magic in the process.

**The Starlight Temple will be released soon after patch 1.0 is live.**&#x20;
{% endhint %}

**The process to upgrade constellations are as follows:**&#x20;

1. Quest to find Essence of Starlight (EOS)&#x20;
2. Take EOS to the Starlight Temple&#x20;
3. Select one of the 6 elements (Fire, Water, Wind, Earth, Light and Dark)&#x20;
4. Upgrade is immediate, but all the EOS will be burned in the process (see table below)

Completing a Rank 7 constellation will enable you to stake MAGIC on your legion. Put simple, the constellation is the compass that guides Legion to new territories. Similarly, MAGIC represents the aura that shields Legions from the toxicity of uncharted territories.

**Legion Requirement for Exploration in Season 2:**&#x20;

* Rank 7 constellation and&#x20;
* MAGIC staked on Legion (information will be released as we approach Season 2).

The table below highlights the requirements for each constellation. To get to Rank 2, for example, you will need 25 + 38 = 63 Essences of Starlight (and 1 Small Prism).

![](../../../.gitbook/assets/Screenshot\_31.jpg)

{% hint style="info" %}
**1/1 and All-class Genesis Legion comes with Constellations pre-unlocked.**

1/1: 3 Unlocked || All-class: 1 Unlocked

Uncommon/Special/Common has 10%/3%/1% to unlock 1 Constellation through Pilgrimage
{% endhint %}

#### FAQ for Starlight Temple

* Can I stake MAGIC on my Rank 7 Legion yet? No this will be enabled closer to Season 2
* How much MAGIC will I be able to stake on a Legion? TBD&#x20;
* Can I sell Legions with Staked MAGIC on the Marketplace? Yes.
* Will I eventually be able to unstake MAGIC from a Legion? Yes.
* Which constellation do I pick? Up to you, each correspond to a different Realm in Season 2.
* Will Legions with staked MAGIC on themselves earn MAGIC? No.

## The Future <a href="#thefuture" id="thefuture"></a>

Beyond this, we are also excited to showcase some tentative ideas behind the scene. It is our hope to test and refine these ideas with the community for continued aligned interest:

{% hint style="danger" %}
The below are **IDEAS** only and **NOT** implemented in Patch 1.0

We would love feedback on some/all of these. Thank you.&#x20;
{% endhint %}

1. Providing more utility for Legion Genesis outside the mine.&#x20;
   * For example: Rarer (Genesis) Legions able to complete Quests/Crafts faster&#x20;
   * A chance of Legions being Fatigue when questing.&#x20;
2. Revamping the Recruit system.&#x20;
   * Implement features to combat bots&#x20;
   * Allow recruits to gain levels, and unlock other types of Loot.&#x20;
3. Revamping the Crafting System&#x20;
   * Adjust Treasure break chance to ensure a more positive experience.&#x20;
   * Examine alternatives for Treasure breakage to incentivize positive loop.&#x20;
   * Mini crafting recipe with lower tier Treasures (e.g., craft small prisms only)&#x20;
4. Revamping the Questing System&#x20;
   * Facilitate a more dynamic questing experience that transcends beyond a simple input-output format. This may include more world building, and different questing “zones” that require conscious decision making.&#x20;
5. Providing additional utility to Treasures&#x20;
   * On-boarding ecosystem partners to incorporate Treasures as inputs&#x20;
6. Introduction of the mysterious merchant as an alternative path to crafting&#x20;
   * Appears randomly, sometimes with good deals, other times not.

## Fortnightly AMAs

Moving forward, the Bridgeworld team will host fortnightly AMAs, where we can regularly (and formally) engage with the community. Some topics of discussion may include:

* Feedback on existing mechanisms&#x20;
* Theory crafting of new ideas&#x20;
* Discuss future plans&#x20;
* How the team go about collecting feedback and implementing them (e.g., how ideas are collated, modeled, coded, tested and ultimately implemented)

If you have any suggestions or ideas (or any constructive criticism on current implementations), please reach out to us via the Bridgeworld Feedback Form (see below).

{% hint style="info" %}
**Bridgeworld 1.0 Patch Feedback Form**: [https://forms.gle/Ez5dNQumjtxR26CB8](https://forms.gle/Ez5dNQumjtxR26CB8) &#x20;
{% endhint %}