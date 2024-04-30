# HIP-XXXX Modification to SP Hex Boosting Processes

- Author(s): Bz
- Start Date: 04/30/2024
- Category: Economic
- Original HIP PR: <!-- leave this empty; maintainer will fill in ID of this pull request -->
- Tracking Issue: <!-- leave this empty; maintainer will create a discussion issue -->

## Summary

This HIP proposes a modification to current boosting methods and burn mechanics. The HIP proposes a shift from the current multiplier based system to a "bonus" based system. It also makes modifications to how SP burns work for boosts and where the resulting boosted rewards would be pooled from.
The inention of the HIP is to better align boosted hex rewards with desired radios for a boost location by giving SPs the ability to specifically designate what a hex's bonus is worth for a specific radio's coverage (indoor/outdoor and wfif/CBRS). This would allow for better boost designations and the balancing of boosted rewards between different radios that multiplying Coverage Points unintentionally creates.

This HIP will supersede HIPs: 84, 121 (if passed), and 122 (if passed). Previously boosted hexes under these HIPs will continue until boost expiration.

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
