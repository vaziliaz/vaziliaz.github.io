---
layout: post
title: "The Gerge"
---
Geregè is a trust-minimised bridge that connects the Cosmos Ecosystem with Ethereum Layer 2s, powered by zero-knowledge. Geregè is designed to become the largest zkbridge ecosystem that connects all blockchains through trustless bridging.

Press enter or click to view image in full size

🧭 Mission
The Pax Mongolica

Over centuries, the Mongol Empire’s peaceful reign facilitated uninterrupted trade and cultural exchange between Europe and Asia along the Silk Road. This inspired the growth of multicultural cities and the spread of ideas and technologies.

At Geregè Protocol, we are inspired by this historical legacy and strive to usher in a new era of “Multi-Chain Peace” across diverse blockchains. Our goal is to enable seamless asset and data transfer, and facilitate the emergence of groundbreaking innovations that will shape the future of Web3.

To foster a harmonious and interconnected multi-chain ecosystem for seamless exchange of value, ideas and innovation.

🔍 Vision
The Trust-minimised Bridge

Geregè is the first dedicated trust-minimised IBC routing chain. It leverages an innovative consensus engine, zero-knowledge technology to achieve a highly efficient and scalable IBC packet routing solution. We are positioning Geregè as part of a longer trajectory where blockchains will be shifted more than its monolithic presence.

Due to IBC’s rigorous security standards and specifications, it is not natively compatible with all major blockchains, which has prevented industry-wide adoption. Amherst Labs is tackling the challenge of upgrading IBC functionality and expanding the IBC network across the blockchain industry.

Inspire confidence through multi-chain security and robustness.

How did it started?
Throughout the history of trade, few things have been as important as trust. Merchants and traders, from ancient times to the present day, have relied on trust to build relationships and facilitate transactions. However, in an age of global trade where merchants and buyers may never meet face-to-face, how can trust be established?

Press enter or click to view image in full size

The trust-minimised trade with zero-knowledge — Geregè
At Amherst Labs, we are building Geregè to operate in a trust-minimised environment with the help of zero-knowledge proof technology, providing a high level of security and reliability for users. The Geregè Protocol is inspired by the ancient “Gerege”, a golden tablet that served as a foreign passport of the highest order, granting Marco Polo seamless travels through the Silk Road to connect the West with the East. Just as it served a key role in the explosion of trade between east and west, Geregé is the future of cross-chain protocols, promising to revolutionize the way we think about trade across different blockchains, starting with Cosmos and Layer 2s.

⚖️ The Stability — Standardised Bridging
The stability brought about by Mongols opened up the ancient trade routes to an undisturbed exchange of goods between peoples from Europe to East Asia. This trade route facilitated the exchange of various goods, including silk, paper, compasses, and gunpowder, which played a significant role in shaping modern technology.

However, just as the ancient Silk Road was threatened by raiders, current blockchain ecosystems face significant losses from insecure bridges due to hacker attacks. To address these concerns, we are promoting IBC as the practical industry standardised bridging solution, and we developed Geregè zkIBC, a trust-minimised cross-chain bridge.

Become a member
We recognize that the current state of blockchain interoperability is fragmented and lacks security, with competing standards and solutions causing developer friction. We see Geregè zkIBC as an antidote to this chaos, providing stability to cross-chain communication. We believe that Geregè zkIBC, built on the IBC protocol, can offer the necessary security and standardisation for efficient blockchain interoperability without the need for trust assumptions, thanks to the zero-knowledge technology. While some currently view IBC as only serving the Cosmos ecosystem, we sees it as ideal standard for interoperability across all chains, credits to its superior security and decentralisation compared to other solutions.

🪝 Raiders — The Bridges’ Pain Point
The problem: current cross-chain bridge solutions either have poor performance or rely on centralised parties, leading to recurring attacks that have cost users over 1.5 billion USD following hacks on bridges like Wormhole and Nomad.

The success of a bridge relies on the consensus protocols of both involved chains. For example, if one chain, T1, runs Proof-of-Work, a light client protocol may be used. In this case, a smart contract on the other chain, T2, referred to as ST2, would keep track of T1’s block headers to verify transaction inclusion and other events using zero-knowledge proofs. However, this approach results in significant computation and storage overhead for ST2, as it needs to verify all block headers and maintain a continuously growing list of them. Verification can be even more expensive for non-PoW chains. For instance, verifying a single block header on Ethereum for a bridge between Ethereum and a Proof-of-Stake chain, such as Cosmos, would cost around 64 million gas, which is impractical.

Current Solutions:
At present, many bridge protocols employ a committee-based approach as an efficient alternative. In these systems, a committee of validators is responsible for approving state transfers. However, this approach has major issues. Firstly, it relies on an extra trust assumption in the committee, which makes bridged assets less secure than native ones, thus complicating the security analysis of downstream applications. Secondly, relying on a small committee can result in single points of failure. For example, in the recent Ronin bridge exploit, attackers were able to steal 624 million USD by obtaining five of the nine validator keys, making it the largest attack in the history of DeFi as of April 2022. The second and third largest attacks also targeted bridges, with $611m stolen from PolyNetwork and $326m stolen from Wormhole, with key compromise suspected in the PolyNetwork attack.

📝 Geregé — Steppingstone to Becoming Trust-minimised Bridge Ecosystem
Geregè approach:
Our proposed solution, zkIBC, offers an efficient and secure cross-chain bridge without relying on a centralized committee. We achieve this by combining zk-SNARK and zk-STARK proofs to enable a prover to convince ST2 that a state transition has taken place on T1. To keep ST2 in sync with T1, anyone can submit a proof that shows the latest block header of T1 and the corresponding Merkle proofs.

The benefits of this design are three-fold. First, the use of zk-SNARK and zk-STARK ensures the security of the bridge without the need for additional security requirements beyond those of the underlying blockchains. This means that zkIBC does not rely on a committee for security, making it more resilient to attacks. Second, by using a purpose-built zk-SNARK and zk-STARK, T2 can verify state transitions on T1 much more efficiently than encoding the consensus logic of T1 in ST2. This reduces the storage overhead of the bridge to a constant value. Finally, the separation of the bridge from application-specific logic makes it easy to enable additional applications on top of the bridge.

Technical challenges:
To prove correctness of a given computation outcome using a zk-SNARK, one first needs to express the computation as an arithmetic circuit. While zk-SNARK verification is fast (logarithmic in the size of the circuit or even constant), proof generation time is at least linear, and in practice can be prohibitively expensive. Moreover, components used by real-world blockchains are not easily expressed as an arithmetic circuit. For example, the widely used ED25519 digital signature scheme is very efficient to verify on a CPU, but is expensive to express as an arithmetic circuit, requiring more than 2 million gates. In a cross-chain bridge, each state transition could require the verification of hundreds of signatures depending on the chains, making it prohibitively expensive to generate the required zk-SNARK proof. In order to make zkBridge practical, we must reduce proof generation time. While verifying ED25519 signatures is computationally inexpensive, it can cost up to 500K gas or around $49 on Ethereum. Similarly, storing even 1KB of data can cost around $90 on Ethereum. This problem is not unique to Ethereum but is a characteristic of most permissionless blockchains. As a result, reducing the on-chain computational and storage overhead has become a crucial objective.

Our team’s objective is to significantly reduce the circuit size of ZKED25519 on a large scale, and to compare it with existing solutions such as [plonky2-ed25519].

Drawing from our experience working on the common-ec-cairo project, we have decided to represent reduced big numbers using a unique 3-limbs format, with each limb in the range of [0, ²⁸⁶). To facilitate calculation, we will utilize a 3-limbs format with limb in the range of [-k²⁸⁶, k²⁸⁶) and a 5-limbs format with limb in the range of [-k²¹⁷², k²¹⁷²) to represent unreduced big numbers.

At the core of our solution lies the function bigint_div_mod, which calculates x/y mod p, where both x and y are in unreduced format, and returns a reduced 3-limbs format. However, computing x/y mod p directly in circom is challenging, as circom is built on the babyjubjub field.

To overcome this, we are leveraging two additional inputs, r and k, that will greatly aid in the calculation of x/y mod p. By verifying that yr-x=k p, we can obtain r=x/y mod p. This approach is not only more straightforward than direct calculation, but also yields better results in terms of circuit size reduction. We are utilizing Python to output all the additional inputs needed to verify a signature.

Closing Note
As a team working on the Geregè Protocol, we believe that we are on the verge of a new era in decentralized applications. We envision a future where blockchain technology is widely adopted and used by individuals and businesses alike, making it the backbone of the digital economy.

We see bridging solutions like Geregè as a critical piece of the puzzle in achieving this vision. By enabling interoperability between different blockchain networks, we can unlock new opportunities for developers and users to build innovative and secure solutions that were previously not possible.

Our team is excited about our first integration between Cosmos Hub and Ethereum Layer 2s, specifically the zk-rollups, which offer far superior transaction speeds compared to the main chain, making them suitable for applications that require real-time processing, such as high-frequency trading or real-time payments.

As we work towards realizing our vision for the future of decentralized applications, we remain committed to building a trustless, decentralized, and scalable solution that empowers developers and users alike. We believe that our efforts will contribute to the wider adoption of blockchain technology and the creation of a more decentralized and equitable digital economy for all.
