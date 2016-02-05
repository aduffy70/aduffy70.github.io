---
layout: page
title: VPGsim
permalink: /vpgsim/
---

### Virtual Population Genetics Simulation (VPGsim)

![VPGsim]({{ site.url }}/images/VPGsim_002-300x256.png)
We are growing virtual ferns to better understand how their lifecycle of independent, alternating haploid-diploid generations affects their genetics at the population level. The ferns' health and reproductive success are determined by the interaction of their genome with environmental factors such as competition, altitude, weather, and soiltype. Tools are provided to summarize and plot data about the population, and to visualize patterns of genetic diversity that emerge across the landscape. Research and educational applications of this project are being developed.

### About the Science:

The plant lifecycle consists of an alternation between two generations: haploid gametophytes and diploid sporophytes. Studies of plant population genetics generally focus on the more visible sporophytes and ignore the gametophytes. This may be excusable for seed plants, where the gametophyte consists of a few short-lived cells within the pollen grain or buried within the ovary of the flower. That is not the case in all plants, however.

In ferns, the gametophytes live free of the sporophyte, may be very long-lived, and can potentially occupy different microhabitats and respond to different selective forces. Because gametophytes are haploid, expressed genes may be more affected by selection since they are not shielded by allele dominance. In some ferns with atypical lifecycles, the sporophyte stage is rare (or perhaps does not exist at all) so understanding the effect of evolutionary forces working on the gametophyte stage is especially important. All of this raises some interesting questions:

* How are patterns of genetic diversity affected by selection during the "forgotten" haploid lifestages?
* How are patterns of genetic diversity affected when sporophytes are rarely (or never) produced?

This simulation system will allow us to explore the answers to these questions, and also to test the effects of interactive simulations on students' understanding of population genetics and their attitudes about science inquiry.

### About the Technology:

![Virtual Environment]({{ site.url }}/images/VirtualEnvironment-300x67.png)
VPGsim was built using OpenSimulator, an opensource server system that allows you to create simulations in 3-dimensional space. We extended OpenSimulator to allow greater control of environmental variables (terrain, weather, and soil type) and to track and report data on our virtual ferns. Users log in to the 3D environment and use an avatar to interact with the environment, the plants, and other users.

The ferns use OpenSimulator's scripting language (LSL) with custom extensions to allow them to detect and respond to their environment and each other. They exist in three different lifestages: spores, gametophytes, and sporophytes. Haploid spores are dispersed by the wind. Given the appropriate environmental conditions, spores germinate to become bisexual gametophytes. With a nearby mate and enough moisture, two gametophytes can reproduce sexually to produce a diploid sporophyte. Sporophytes undergo meiosis (genetic shuffling and reduction) to produce numerous haploid spores, and the cycle repeats.

The ferns' genome consists of 5 unlinked loci, each with one of two alleles (represented by 1 or 0) and expression is dominant-recessive. By adjusting parameters on a webform, each locus can used to control life history characteristics, response to a particular aspect of the environment, or be a neutral marker. Response to environmental variables can be customized by specifying the optimal environmental value and the shape of the fitness curve around that value and these parameters can be set separately for each lifestage and genotype. These settings, along with the environment, combine to determine the health and fitness of an individual at a particular time. More fit individuals are more likely to survive and produce more offspring. With different settings, different patterns of genetic diversity emerge across the landscape.

### Visualization Tools:

![Visualization]({{ site.url }}/images/Visualization1-300x178.png)
It is interesting to watch the population grow and develop, but it is only useful if we are able to gather and analyze data about the population. Information about the population is displayed for users through a Heads Up Display (HUD). History plots showing trends in population demographics, allele frequencies and levels of heterozygosity are produced and the plants themselves can be highlighted in different colors based on their alleles at a particular locus, their overall level of heterozygosity, their current lifestage, their haplotype or genotype, or combinations of these characteristics. All of this information can be visualized as the simulation is running. All data used to generate reports, plots, and visualizations are logged and can be downloaded and formatted for use in standard population genetics software packages.

### Future Plans:

We have two main goals for this project:

1. The simulations can be used to demonstrate fundamentals of population genetics theory and the process of scientific inquiry. We began using the system for a lab activity in undergraduate genetics courses at Utah State University in Fall 2011.
2. Currently the plants all cycle through the typical fern lifecycle, but we plan to use this system to explore the effects of deviating from that basic lifecycle and as a predictive tool in population genetics studies of ferns with atypical lifecycles. The system could also be useful in studies of dispersal & colonization, metapopulation dynamics, fitness tradeoffs, evolution of sex, selection on multi-locus traits, variable mating systems, and the effects of disturbance and environmental change.
