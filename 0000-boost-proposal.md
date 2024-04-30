# HIP-XXXX Modification to SP Hex Boosting Processes

- Author(s): Bz
- Start Date: 04/30/2024
- Category: Economic
- Original HIP PR: <!-- leave this empty; maintainer will fill in ID of this pull request -->
- Tracking Issue: <!-- leave this empty; maintainer will create a discussion issue -->

## Summary

This HIP proposes a modification to current boosting methods and burn mechanics. The HIP proposes a shift from the current multiplier based system to a "bonus" based system. It also makes modifications to how SP burns work for boosts and where the resulting boosted rewards would be pooled from.
The inention of the HIP is to better align boosted hex rewards with desired radios for a boost location by giving SPs the ability to specifically designate what a hex's bonus is worth for a specific radio's coverage (indoor/outdoor and wfif/CBRS). This would allow for better boost designations and the balancing of boosted rewards between different radios that multiplying Coverage Points unintentionally creates.

This HIP will supersede HIPs: 84, 121 (if passed), and 122 (if passed). Previously boosted hexes under these HIPs will continue until boost expiration. This HIP also builds on top of HIP-109.

<!-- Read the content requests in all sections before starting to write any section. -->

## Motivation

Gives SPs better pathways to clearly identify a boosted hex's worth.

Provides a better burn and boost mechanic between the SP and MOBILE subDAO.

Solves the issue created by multipliers disproportionally afecting one type of deployment over another.

## Stakeholders

Deployers: Effects on boosting would be a shift from multiplied MCP to a bonus approach. Rewarding "bonus" mobile for hex coverage vs mobile earned from multiplied coverage points.

Service Providers: Will be affected by the new system and burn mechanics, allowing a higher, more proportional burn required for bonuses to be dealt out by the other emission buckets (SP and PoC).

## Detailed Explanation

This HIP proposes an overhual of the existing boosting method on the MOBILE network. Proposing to: 
 
  -Replace boost multipliers with bonuses

  -Modify the burn requirments from SPs for bonuses

  -Redefine how bonuses are rewarded at the per coverage type level and where bonuses come from once a burn from an SP occurs


**Replacment of multiplier boosting with bonus incentives**
The current issue with the multiplier based boosting system is the uncertainty created by rewarding boosts based on multiplied coverage points. The issue with this model is that it moves inline with total network coverage points, meaning a boosted deployment can earn more or less from boosted rewards if networkwide coverage points fluctuate. This effect has been more obvious recently due to HIPs reallocating large ammounts of network coverage points (103 and 113). Additionally, uncovered boosted hex's boost clock does not begin to count down until that hex is first covered. Presuming a deployment happens later in said hex, the boost then maybe signifigantly different from the intended boost reward at time of burning due to the multiplier affecting coverage points and not MOBILE itself. These factors weight on deployers as well by fluctuating bonus rewards as the netowrk's coverage points shift. 
To solve these problems, this HIP proposes a bonus based system. SPs will determine hexes to recieve bonus rewards and allocate how much additional MOBILE each hex may recive per deployment type, per epoch. This bonus will be specific to one of the 4 existing deployment methods currently available (indoor/outdoor and WiFi/CBRS) and can apply to any new deployment types in the future. For example, a single res12 hex may be rewarded a bonus of X MOBILE per epoch for indoor wifi coverage, Y mobile for outdoor Wifi coverage, and Z MOBILE for indoor and outdoor CBRS coverage. Each of the 4 values for each deployment type muct be defined by the SP at burn. The ability to directly allocated set amounts of MOBILE to specific deployments vs multiplying coverage points gives better control to SPs while also making the initial burn result in a balanced net bonus emissions outcome once the bonus concludes. This also has the added benefit of allowing deployers to know exactly how much bonus MOBILE to expect on a per epoch basis.

**Modification of SP burn requirments and Bonus rewards Buckets**
This HIP proposes a more proportional burn mechanic than what currently exists. Once all bonus hexes are inentified, and the accompaying bonus values are determined for each deployment type, it is proposed the SP burns half what will be rewarded as bonuses. For example, if 100 hexes are determined to recieve bonuses of 1000 additional MOBILE per epoch for each of the 4 deployment types, a total of 400,000 MOBILE, the SP will burn 200,000 to initiate the bonus. All of the accompanying bonus will be taken from the existing PoC pool. 



## Drawbacks

- Why should we _not_ do this?
- What problems could occur if we do this?

## Rationale and Alternatives

This is your chance to discuss your proposal in the context of the whole design space. This is
probably the most important section!

- Why is this design the best in the space of possible designs?
- What other designs have been considered and what is the rationale for not choosing them?
- What is the impact of not doing this?

## Unresolved Questions

- What parts of the design do you expect to resolve through the HIP process before this gets merged?
- What parts of the design do you expect to resolve through the implementation of this feature?
- What related issues do you consider out of scope for this HIP that could be addressed in the
  future independently of the solution that comes out of this HIP?
- Are there dependencies, milestones, or dates that need to be met for this HIP to succeed?

## Deployment Impact

Describe how this design will be deployed and any potential impact it may have on current users of
this project.

- How will current users be impacted?
- How will existing documentation/knowledge base need to be supported? Any content to change at
  <http://docs.helium.com>?
- Is this backwards compatible? Can this HIP be undone?
  - If not, what is the procedure to migrate?

## Success Metrics

What metrics can be used to measure the success of this design? Are any new ETL reports needed to
measure the success?

- What should we measure to prove a performance increase?
- What should we measure to prove an improvement in stability?
- What should we measure to prove a reduction in complexity?
- What should we measure to prove an acceptance of this by its users?
