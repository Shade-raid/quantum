Braid Works
A factory puzzle about non-commuting machines. Made for Quantum Game Jam 2026.

You run a tiny workshop on a flat 2-D chip, where particles are anyons and theonly way to process material is to braid strands around each other. There is no"over" in two dimensions, so every exchange history is permanent — and fornon-abelian anyons, every exchange changes the state. Swap strands 1 and 2, then2 and 3, and you get a different product than doing it in the other order.Same machines, different order, different product.

How to play
Orders show a target arrangement of colored strands (top to bottom) and apar: the minimum number of swaps that can reach it.
Build a line of sigma machines. Each machine σi swaps adjacent strandsi and i+1. The diagram shows your bundle entering left and exiting right.
Ship. A run takes 0.9 s per machine. Matching an order pays full price,at-or-under par pays a 1.5x bonus, no match scraps the bundle for $1.
Recipes. Your shortest build for each arrangement is remembered. Load itanytime, or let the Foreman upgrade auto-ship saved recipes at 70%.
Decoherence is the prestige reset: money and upgrades collapse, recipessurvive (measurement keeps the classical record), and each coherence pointadds +10% payouts permanently.
Controls
Everything is clickable with mouse or touch. Keyboard: 1–3 add a machine,Backspace removes the last one, Enter ships, Escape closes a panel or returnsto the menu.

The physics
In 2-D, particle worldlines cannot pass through each other, so exchangehistories form braids — this is the braid group.
Non-abelian anyons attach a matrix to each exchange. Matrices do notcommute, so the order of exchanges is the physics. This is the entire game.
The game's swap operators satisfy the Yang–Baxter relation,σ1σ2σ1 = σ2σ1σ2. You can exploit it: two different three-machine linesproduce the same output.
Par is the Coxeter length of the target permutation, computed exactly bybreadth-first search over S3 and S4.
Topological quantum computing works the same way: qubits live in fusionspaces of anyons and gates are performed by braiding, protected from localnoise because the information lives in the topology, not in any local wiggle.
Tech
One HTML file. No dependencies, no network requests, no build step.
Saves to localStorage. Nothing leaves your device.
Braid diagrams are inline SVG; audio is synthesized live with WebAudio.
