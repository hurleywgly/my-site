---
date: 2022-03-20T11:13:32-04:00
description: "Idea for revenue distribution using blockchain technology and tokens."
featured_image: "/how-to-web3-royalties.png"
omit_header_text: true
tags: ["music", "tech"]
title: "How music royalties could work on-chain"
---

I’ve been really inspired by the work Justin Blau (3LAU) has been doing with [Royal.io](https://royal.io/). Their vision is to change music industry mold, by creating a holistic relationship between fan and artist using blockchain technology. Coming off the recent success of Nas’ new project (NFTs for his new single, “Rare”), I started to wonder about how the music royalties would work.

![Different rates for royalty earnings purchased by super fans](/nas-royalty-split.jpg "3 tiers of royalty splits — 1,110 tokens — 50% royalty split between them")

After spending most of the last decade building music licensing and royalty accounting technology, I tend to gravitate towards the attribution systems working the backend. *How will Royal handle the royalty allocation among fans? How will they convert earnings and divide them evenly among NFT owners? How do you handle changes in ownership when consumption data only arrives monthly?*

I was curious enough to map these challenges out: writing out my thoughts and thinking about would-be solutions. But before we dive into those ideas, let’s cover some basics about Royal.

**What is Royal?** Royal has enabled tokenized royalties for music artists. Artists can sell Royal NFTs, collectors can buy them, and everyone can accrue earnings.

**What is a Royal NFT?** Let’s say you’re an artist looking to distribute a new song. You can create a collection of NFTs, which represent a fan collectible and a certain royalty percentage. Any fan can purchase the NFT from Royal or via secondary market. When royalty payments are sent out, crypto wallets owning NFTs from the collection will get their designated share. This means fans can invest in artists directly and artists can reward investors with a share of future earnings.

**How is this similar to traditional music licensing?** Copyright ownership for music content is divided among multiple parties. Typically, labels and artist own the ‘sound recording’ (i.e. the song itself) while publishers and composers own the composition rights (i.e. lyrics, instruments, musical score). Each own a specific portion of final product, dictating royalty splits. So, Royal’s model is similar in the sense earnings will be accumulated and then divided according to ownership %.

**How is this different from traditional music licensing?** Ownership of the content is in the public domain. These transactions are written into the Ethtereum blockchain, so there is no confusion over who owns what percentage of the royalties. Royal has a chance to standardize licensing data. Traditional music licensing is far from standardized.

**One more thing.** What I find most interesting about Royal is it’s willingness to bridge web2 music services (e.g. music services like Spotify & Amazon Music) with blockchain technology. I am also assuming they will leverage web3 music streaming services like Audius or Sound.xyz. This flexibility positions Royal to capture the most value for their customers, no matter where the fans are consuming music.

## Hypothetical Solution Design

### What is the problem we’re trying to solve?
Music intellectual property is extremely complex. Splitting royalties accurately is a challenge the industry has yet to solve. That challenge boils down to three main problems:

1. Ownership differs per country — When content is consumed, there are a specific set of rights for the country in 
which that content was consumed. This means consumption has to be tracked and mapped specifically to the rights holders for that region.

2. Song owners can change over time — Even after you isolate the consumption to a specific country, there are likely dozens of different versions of the same song, all claiming rights for that country. Distribution companies have to determine which is the correct set of rights to honor that day, then split the royalties accordingly.

3. Metadata is inconsistent — There are very few standards when it comes to music licensing metadata. Licensing systems are loaded with typos, manual errors, issues with special characters, issues with capitalization, and inconsistent identifiers (e.g. ISRCs). This creates a lot of manual overhead for companies trying to use this information and makes automation a challenge.

### What is the solution?
Building a smart contract based payments system that enables royalties to be accurately tracked and split to owners. This solution would require high quality rights filtering and identification logic, however to keep this exercise focused, I will keep things at a high level.

![Diagram of music consumption to automated royalty earnings accrual and payment](/web3-royalty-split.jpg "Hypothetical solution design for divvying up royalties to NFT holders")


* **A) Stream:** Music is streamed by fans and funded by advertising, subscriptions, purchases, and token allocation.

* **B) Pool:** Payments come from multiple sources and need to be pooled prior to allocating to songs.

* **C) Identify:** Clean up and filter metadata then match it to licensed songs in Royal’s database.

* **D) Convert:** In order to make the most for owners, royalties should be converted to relieve tax burden. I would probably recommend a strategy that varies depending on where content is consumed and the country in which the artist lives.

* **E) Split:** Leverage smart contracts to automatically and transparently divide the royalties.

* **F) Pay:** Lastly, get the payments into the owners of the collection and IP (e.g. the artist). Royalty payments are typically low — pursuing ways to pay that reduces gas fees (e.g. efficient contracts or layer 2 blockchains) would be ideal.

## Closing Thoughts

Royal’s ‘secret sauce’ lies in the logic handling data across the system. Data grading, merging, and storing are critical to paying the owners accurately. While allocation will remain a challenge, there are many projects (like [Splits](https://splits.org/)) building blockchain technology for intelligent splits of ownership. Smart contracts could significantly improve how royalties are distributed today. These advancements could help Royal build a system where attribution and payments happen consistently, automatically, and securely. That’s a game changer for the music industry.
