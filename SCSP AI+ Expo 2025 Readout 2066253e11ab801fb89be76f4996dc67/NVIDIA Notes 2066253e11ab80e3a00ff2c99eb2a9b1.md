# NVIDIA Notes

- Policymakers involved at all layers, NVIDIA focusing on the lowest level, hardware
- Identifying smuggled chips: location verifications embedded into chips.
- Disabling, throttling chips: time based remote listening.
- Concretely introduced with the CHIP security act.
    1. Export control chips with location verifications 
    2. RESEARCH into Secondary remote licensing. 
- Opportunity vs challenges
    - Opportunity: intelligence on finding smugglers, how many are smuggled
        - Ability to evaluate measures of control
    - Challenge:
        - Usefulness; limited endorsements, how valuable is this actually?
        - Robustness: will the adversary be able to crack the methods?
        - Precision: what about edge cases? Borders?
        - COST: its extra bureaucracy and overhead. the burden is on the chip designer. Maybe big companies would do fine, but what about smaller companies?
- Software vs Hardware: it’s easier to patch software than recall hardware. How do you determine what chips are actually subject to this? What constitutes frontier?
    - Should BIS require a specific implementation? How much control should they have, and what incentives should they provide? How export assistance on compliance or a pure ban?
- Takeaway: policymakers are conscious of improving security at all layers. They have key mechanisms they want to target. We have a specific example in the chips security act.

Equity Labs with Jonathan (EQTY)

- working with DOS, DOE, FDA
- How do we define trust, through the lens of cryptography? Encryption and authentication of information.
- How do you prove everyone is following the rules?
- March 2024: more than half of the traffic on the web is non-human, most of that is malicious.
    - 91% of public sector and commercial are hit by supply chain attacks annually.
    - ABERAGE in the millions per attack
- AI supply chain: PyTorch, OpenAI, Ultralytics
- Analogies that already work; secure procurement (NIST trusted computing group), prescription drugs, secure data for model risk management
- Jen Huang imagines NVIDIA with 50k employees and 100mil agents; the new scale is on a completely different scale according to NVIDIA.
- Trust evolves, must start with hardware.
- Req:
    - Security
    - Transparency
    - Verify ability
- Must be privacy first: we don’t want the same tech to turn us into a surveillance state
    - Any authentication technology is surveillance technology. The difference is consent.
- Ex: Signal
    - Insanely strict security standards rooted in HARDWARE. Firmware and OS, build verification, encrypted memory, a fully trustworthy stack.
    - Apple also does a good job here, rooting security in silicon
- Nvidia has also been doing this since 2018, but in 2022, even more leading into “Verify able compute”

![IMG_2310.jpeg](NVIDIA%20Notes%202066253e11ab80e3a00ff2c99eb2a9b1/IMG_2310.jpeg)

- Agents: compile the full attestation and have agents, when meeting, presenting that to each other. Like a passport for agents.
- selective disclosure, open source software.
    - Places trust in the USER
    - Provides an example, from the US. Free world let’s ducking goooo

**Open Discussion** 

- Building in capabilities in the hardware to monitor people. Let’s look at history.
    - Encryption wars: most people aren’t really interested in whether or not your chip is compromised, as stated by the USG. The discussion and hand of the government ultimately slowed the adoption of tech needed to encrypt the internet as we know it today.
        - Salt Typhoon: Lawful Access Systems were the main flaw here; systems created with the intention for the Gov to monitor the systems they were attached to.
        - ATT being hacked.
- What guarantees do we want to see? What do we want to drive home going forward?
    - Ex: HTTPS session so we know we aren’t getting spoofed when checking bank information. We would want a similar guarantee for our compute.
    - Legislation: we need to have capabilities for our chips ot work everywhere.
        - Still lots of disputes about how big chip smuggling is, if this is the best way to address our problems.
            - Spoofing, enclaves, provide immense barriers. If we invest so heavily, is it going to have a reasonable return?
        - SNS: US companies must be at the frontier otherwise our conventions won’t even be followed. It doesn’t matter if we care if someone else does it cheaper and better.
- What are the concrete benefits for the user/consumers from the hardware innovations?
    - Ex: Signal app, where hardware components are crucial to verify that the authenticity. Additionally, server signatures to say that we have an official build to work on.
- Solving actual problems? What would someone want to buy? (Weird framing)
    - Guy in the middle with meta raybans: people shoudl care. we shoudl go after law enforcement to actually follow the rules. (Kevin)
    - Distillation: what value does compliance have? what value does “forced” compliance have? Key innovators should want to pay for trustworthy interactions.
    - Theft of model weights: would it be possible to verify in hardware that weights have not been stolen? Maybe some value there?
        - Even today, many companies have pretty robust guarantees about their models.
- Older fellow is driving home, again and again, that we want to process to be up to the user. It’s all about freedom.
- Where could policymakers, government lead? NTIA, NIST work? Industry doesn’t want government to overstep.
    - Government can, should, has been leading on looking into alignment or issues that are more unique to them.
    - AI caucus: Gov has the power of the purse, one of the biggest purchasers in the world.
    - EX: NSA cryptography work can benefit everyone, not just sigint. Goes into commerce, everyday.
- How do we actually govern AI? Is it normal tech, or WMD? Baked in by default are the expectations for AI in the next 15 years.
- History: How is AI similar to the past, how is it different?
    - Advantage: diffusion of chips is actually easier to diffuse software. Code is expression under case law. Compute, however, is still on the chopping block, but at least not there yet.
        - Near term thresholds are possible.
    - Clipper chip? Encryption history. Failed experiment.