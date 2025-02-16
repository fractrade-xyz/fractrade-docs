# FRAC Score: A Fair and Transparent Access / Reward Mechanism for Utility Token Holders

The FRAC Score system is designed to provide fair access to Fractrade's advanced trading features and reward loyal token holders. This document explains how the system works and its benefits.

## Overview

Fractrade.xyz helps traders by using AI agents to improve their trading on Hyperliquid Spot and PERP markets. The agents watch on- and off chain market data and help users to trade better, manage risks, and spot profitable opportunities.

Fractrade offers trading strategies that users can customize for their AI agents to follow. Some of these strategies need many resources or can only handle a limited number of traders at once for different reasons, like limited available liquidity or time-based constraints.

To limit the access to these strategies, we need a utility token. Think of it like a membership card — holding tokens lets you access special strategies while keeping the system fair for everyone, as the tokens are available on the Hyperliquid spot market.

The second use case for the token is as a decentralized governance mechanism. The FRAC token also lets users have a say in how Fractrade develops. By holding tokens, users can vote on what new features to build next, making sure the platform grows in ways that actually help its users.

In this article today, we would like to explore two different ideas on how to use a utility token to archive fair access to limited resources. These ideas are in a very early stage as we focus mainly on our product. They might have flaws and numbers might change, but if you have any feedback, let's get in touch and talk about it.

## Traditional Token Access Models and Their Limitations

Common approaches require users to hold a specific number of tokens (e.g., 1,000 tokens for basic access or 5,000 tokens for premium features). With FRAC's limited supply of under 4 million tokens, this model creates several problems:

**Price Barrier:**
If FRAC reaches $20 per token, which would give the total project a market cap of 80 Million — which is compared to other less useful projects in this space still small. A 5,000 token requirement would mean $100,000 for premium access, making it prohibitively expensive for most users.

**Limited User Capacity:**
With a fixed supply of 4 million tokens and a 5,000 token requirement for pro accounts, the platform would be limited to fewer than 800 pro users, severely restricting platform growth.

**Token Distribution Issues:**
- Large holders must maintain their full balance to retain platform access
- This creates artificial scarcity as tokens are locked in wallets
- New users face increasing difficulty entering the ecosystem
- Early investors cannot take profits
- Token price may become inflated due to reduced market supply
- Token distribution becomes concentrated as holders are incentivized not to sell

To solve this problem, we explored two different ideas.

## Idea 1: Percentage-based Access System

The first idea is a dynamic percentage-based access system that allocates platform features based on relative token holdings rather than fixed amounts.

This new model starts with anonymous access, allowing users to explore basic platform features and trial selected strategies without holding tokens. As users acquire tokens, they enter a tier system based on their relative position among all holders.

The proposed tier structure places users into categories based on their holdings: the bottom 30% of holders gain access to beginner level strategies, the middle tier (33–66%) unlocks advanced strategies, and the top 33% receives access to degen strategies.

This approach ensures that access requirements automatically adjust with market conditions, maintaining proportional entry barriers regardless of token price and ensures a fair distribution over time as early investors can take profits for their risks and new users can enter the platform for a fair price.

To prevent market manipulation and ensure system stability, the model implements a time-weighted calculation mechanism. The system takes daily snapshots of holder balances and calculates a 7-day moving average to determine each holder's position. Access levels only update when a holder's average position changes for seven consecutive days, preventing rapid tier switching.

This approach solves multiple problems inherent in traditional token access models. Users can sell portions of their holdings without losing all access privileges, platform capacity isn't limited by token supply, and entry barriers remain proportional regardless of token price.

The system promotes active token trading and market liquidity while maintaining stable access periods for users engaged in various trading strategies.

By eliminating fixed token requirements and implementing a percentage-based system, FRAC creates a more inclusive and sustainable platform that can scale with user growth while maintaining fair access to advanced trading features.

## Idea 2: The FRAC Score: A Dynamic Loyalty Measurement System

Our second idea, which we currently use, is called the **FRAC score** and the basic idea is to measure FRAC holders loyalty through multiple weighted factors. Unlike traditional fixed balance requirements, this system creates a more equitable and flexible environment for all participants. You can find an example implementation here in our Github.

Hint: This purpose of this article is to explain the idea. The numbers might and details might change and will be documented on our official website fractrade.xyz.

**The FRAC Score is our solution to make token-based platform access fairer for everyone. Instead of requiring users to hold a fixed amount of tokens, which can become very expensive as token prices rise, we measure how loyal and engaged our token holders are through different factors.**

## The FRAC Score Solution

The FRAC Score is a dynamic loyalty measurement system that considers multiple factors to determine platform access and rewards.

To be included in the FRAC Score system, a wallet needs to show basic engagement with our platform. This means:
- Holding at least 100 FRAC tokens
- Keeping these tokens for at least 7 days

Once these basic requirements are met, the system starts calculating a loyalty score based on three main factors:

**Balance Factor:** How many tokens you hold matters, but in a fair way. Whether you hold 200 or 20,000 tokens, the system calculates your score so that smaller holders still get meaningful points while larger holders don't completely dominate the system.

**Time Factor:** How long you hold your tokens is the most important factor in our system. The longer you hold, the more points you earn, with special bonuses for each month you maintain your position. This rewards our most loyal community members who stick with us long-term.

**Trading Pattern Factor:** We look at how you manage your tokens over time. Small trades won't affect your score much, but large sales, especially from big holders, will have a bigger impact. This encourages everyone, especially large holders, to trade responsibly.

Building on these three main factors, here's how the FRAC Score calculates your final loyalty rating:

**Starting Score:**
Everyone begins with 100 base points. From there, the system adds points based on your token holding behavior:

**Balance Points (up to 100 extra points):**
Your current token balance is compared to other holders. The more tokens you hold, the more points you get, but in a way that's still fair to smaller holders. For example, someone with 1,000 tokens can still earn significant points compared to someone with 10,000 tokens.

**Time Holding Points (up to 200 extra points + monthly bonuses):**
This is where long-term holders really benefit:
- Every day you hold adds to your score
- After each month, you get bonus points
- These bonuses grow larger the longer you hold
- Someone holding for 3 months gets significantly more points than someone holding for 1 month

**Trading Behavior Impact:**
The system also looks at how you trade:
- Small trades have minimal impact on your score
- Bigger trades based on the percentage of the total available tokens have a higher impact on your score. So someone who dumps 0.3% of the supply or more in a single transaction will have a much higher penalty than someone selling 0.01% of the tokens over a longer period of time

**Final FRAC Score:**
Final FRAC Score = Base 100 + Balance Points + Time Points + Trading Impact

### Advantages

- **Access Stays Affordable**: Unlike fixed token requirements that get expensive as token price rises, your access is based on your loyalty score instead of how many tokens you own.
- **Everyone Can Join**: New users can start with basic features and work their way up, without needing large amounts of tokens from day one.
- **No User Limits**: The platform can grow without limits since access isn't tied to a fixed number of tokens.
- **Keep Your Access While Trading**: You can sell some of your tokens without losing all your platform access, making the market more active.
- **Long-term Holders Win**: The longer you hold your tokens, the higher your score gets, even if you don't have as many tokens as others.
- **Fair for All Sizes**: Whether you're a small or large holder, you can earn a good score through loyal holding.
- **Market Stability**: Large holders are encouraged to trade responsibly, helping keep the market stable.
- **Growth with Platform**: As more people join, access levels adjust automatically, keeping the system fair for everyone.


## Distributing Rewards or Granting Access

Now based on that FRAC Score we can easily build upon it to grant access to different platform features. Some of our AI agent strategies require a lower FRAC score, while others require a higher one to access them. Simple as that.

Another interesting solution would be to automatically distribute rewards from platform fees, the Hyperliquid vaults of our Agents and trading activities to users. The distribution would work by:

 - Adding up all users' FRAC scores
 - Calculating each user's percentage of the total score
 - Distributing rewards based on these percentages

This approach offers significant advantages over traditional staking:
- No need to lock tokens in smart contracts
- Users maintain trading flexibility
- Reduced smart contract risks
- Natural incentives through rewards instead of forced holding
- Automatic distribution based on loyalty
- Rewards could just be paid in USDC to the holders' wallet.

## Summary & Outlook

We've explored two alternative approaches to create a fairer system: the percentage-based tier system and the FRAC Score loyalty algorithm.

Currently, we're using the FRAC Score approach, which measures user loyalty through balance, holding time, and trading behavior. You can find our current implementation in our GitHub repository. However, we view this as just the beginning — the weights and calculations may evolve as we gather more data and community feedback.

We're committed to creating the fairest possible access system for our users. If you have ideas for improving the FRAC Score algorithm or suggestions for alternative approaches, we'd love to hear from you. Our goal is to build a system that works for everyone, from new users to long-term holders.

You are welcome to share your thoughts or improvements through our GitHub issues or community channels.
