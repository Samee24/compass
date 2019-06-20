---
title: Understanding Cooperative Behavior
comments: false
---

I’ve recently developed an interest in grasping the extent to which humans can collectively establish their future, especially under the current fractured political climate where nationalist thought has made a vivacious comeback.  More specifically, I wanted to see whether there are any scientifically strong claims we can make make about cooperation.

I came across a fantastic book by Robert Axelrod  [The Evolution of Cooperation](https://www.amazon.com/Evolution-Cooperation-Revised-Robert-Axelrod/dp/0465005640) which attempts to drive that discussion. This essay is mostly a summation and analysis of the book's strongest points.

## Some background motivation
Is it worth being nice? The domain of decision-making and choice utility — governed by game theory — offers us insight into how decision-making strategies perform and operate over a long span of time.

Our current suite of strategies are inherited through mimesis and biological instinct. Most people believe Darwinian and Capitalist  ideology renders zero-sum game playing as the rational and effective strategy. Is that true, or can we understand and promote cooperation using a framework provided by game theory?

## How rewarding is cooperative behavior?
Research around cooperation has centered around playing iterated versions of Prisoner’s Dilemma. Going from a one-off game to a continuous series with a familiar pool of players introduces complexity that more closely mirrors real-world scenarios.  Robert Axelrod, a researcher at University of Michigan, arranged a round-robin tournament to let different strategies compete amongst themselves. Amongst those submitted, the top performing strategy was *TIT-FOR-TAT*:

1. Cooperate unless the other player defects.
2. Revert to cooperation if the other player starts cooperating again.

There were other competing strategies that were more complicated: some were selfish, and some were nice. However, the top 8 strategies were all variants of nice strategies; ones where players would never defect first.

## When does it emerge?
Players in the real world aren’t just involved in pairwise interactions. They anticipate, take the status quo into account and adjust behavior accordingly.  The status quo is especially important as it is vital to understand whether cooperative strategies can dominate and stabilize in non-cooperative contexts.

Imagine a population consisting of players that always defect and are selfish (*Mean World*). In such a population, is there any hope for cooperation to emerge? Surprisingly, yes. Cooperation can not only snowball into dominating the equilibrium, but it can do so using very small groups of players. Quite obviously, a single agent will perform worse when injected into *Mean World* (since we are in a [Nash equilibrium](https://en.wikipedia.org/wiki/Nash_equilibrium)) , but a small cluster of cooperative players can quickly receive pay-offs that exceed those of selfish agents. To illustrate this, let’s model a simple choice matrix:


<style type="text/css">
.tg  {border-collapse:collapse;border-spacing:0;}
.tg td{font-family:Vollkorn, sans-serif;font-size:14px;padding:10px 5px;border-style:solid;border-width:1px;overflow:hidden;word-break:normal;border-color:black;}
.tg th{font-family:Vollkorn, sans-serif;font-size:14px;font-weight:normal;padding:10px 5px;border-style:solid;border-width:1px;overflow:hidden;word-break:normal;border-color:black;}
.tg .tg-f8rh{font-size:18px;font-family:"Palatino Linotype", "Book Antiqua", Palatino, serif !important;;border-color:#cadbe5;text-align:center;vertical-align:top}
.tg .tg-uyo0{font-size:18px;color:#ce534d;border-color:#cadbe5;text-align:center;vertical-align:top}
.tg .tg-cbx0{font-size:18px;border-color:#cadbe5;text-align:center;vertical-align:top}
</style>
<table class="tg">
  <tr>
    <th class="tg-f8rh"></th>
    <th class="tg-uyo0">Cooperate</th>
    <th class="tg-uyo0">Defect</th>
  </tr>
  <tr>
    <td class="tg-uyo0">Cooperate</td>
    <td class="tg-cbx0">(3, 3)</td>
    <td class="tg-cbx0">(0, 5)</td>
  </tr>
  <tr>
    <td class="tg-uyo0">Defect</td>
    <td class="tg-cbx0">(5, 0)</td>
    <td class="tg-cbx0">(1, 1)</td>
  </tr>
</table>

<span style="font-family:Vollkorn; font-size:0.9em;"> *If both players cooperate, both receive 3 util. If both players defect, both receive 1 util.
If player A defects, but player B cooperates, A receives 5 util and B 0 util. If player B defects, but player A cooperates, B receives 5 util and A 0 util.*</span>


Now, we simulate the game for a certain number of rounds (*N=10*).  Since players always defect in *Mean World*, the pay-off is **stable** at 10 for each player.  We then introduce a new player that employs *TIT-FOR-TAT*. This player will receive a pay-off of 9 since it will cooperate on the first turn (0 util), and then proceed to defect. To model the introduction of a cluster of nice players, let’s add a variable *nice_interactions* which represents the proportion of interactions with other *TIT-FOR-TAT* players. We can then model our pay-off as:

```30(nice_interactions) + 9(1 - nice_interactions)```

Given this, we see the critical value of *nice_interactions* to eclipse a pay-off consisting of only defects is a **minuscule** *0.05*. If a nice player in *Mean World* 5% of its interactions with other nice players, it will position itself to succeed over a purely selfish player. Just **5%**!

This also assumes interactions will be random; a more accurate model will integrate the idea that nice players are more likely to repeat interactions with nice players, which would plummet the 5% requirement.

## Implications
Cooperation can be visible even in symbiotic/parasitic relationships in nature, and is one of the cornerstones of kinship theory in evolutionary biology. At a more emergent level, these findings can help construct better institutions to promote mutually beneficial outcomes. One can already witness some fascinating examples that invoke cooperative principles:

* Immigrant communities that form tight-knit groups and [under-report crime](https://scholarship.law.columbia.edu/cgi/viewcontent.cgi?article=2709&context=faculty_scholarship) amongst their kin.

* Enemy soldiers [cooperating in WW1 trenches](https://www.ias.edu/ideas/2014/chiu-war) to hold unofficial truces.

The emergence of cooperation posits an optimistic vision for humanity. It allows us to search for positive-sum games when designing policy or systems, and underpins a mathematical foundation for being nice in general. Perhaps it shouldn’t come as a surprise why cultural wisdom always called for a need to forgive and collaborate.

<br>

---

<br>

## Resources
* R. Axelrod, [The Evolution of Cooperation](https://www.amazon.com/Evolution-Cooperation-Revised-Robert-Axelrod/dp/0465005640). London: Basic Books; Revised edition, 1990.
* Slides by [Martin Novak](http://web.mit.edu/9.s915/www/classes/slides_nowak.pdf).

<br>











