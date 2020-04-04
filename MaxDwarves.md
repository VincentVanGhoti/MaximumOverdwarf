
# Why?

While there are many infinite combos that allow you to make copies of Seven Dwarves I wanted to see what the fastest possible method was.  Looping 7 Seven Dwarves with Lumbering Battlement and 8 Mirror Marches seemed cool, there had to be a way to make dwarves faster. 

Also, Covid-19 quarantine makes people do some crazy stuff

# Warning !!!!

I would not recommend trying this at home, the first half of loop broke Arena so badly that I couldn't login for several hours without the game crashing



## Assumptions:

#### Board and Sideboard are equivalent:   
Because we are using Mastermind's Acuisistion we can treat the Sideboard and Deck as the same when searching out combo pieces. The decklist has most 1 ofs in the sideboard for convenience in assembling the combo, but it doesn't actually matter once the combo starts.

#### Notation:  
 - For brevity the numbers of cards listed are the minimum number needed.
 - Later we will assume that the full 4 of each combo piece are in play
 - Cards where multiples matter are listed in bold
 



# First Loop: Tutor out everything  

#### Board State:  
Omniscience  
any Non-Token Creature or Saheeli, Sublime Artificer  

#### Hand:  
Mastermind's Acquisition  
Blood For Bones  
Scholar of Ages  

##### Sideboard/Deck:  
1x Dance of the Manse  
1x Phyrexian Scripture  
1x $\bf{Pitiless Plunderer}$  
1x $\bf{Mirror March}$  
1x $\bf{Mirror March / Mirrormade}$
1x $\bf{Seven Dwarves}$
1x Woe Strider  
2x Thrill of Possibility  
1x Cleansing Nova/ Creature Boardwipe

### Play Loop:

 - Mastermind Acquisition for combo piece to hand || Saheeli trigger creates Servo  
 - Scholar of Ages return Mastermind Acquisition  
 - Blood For Bones sacrificing Non-Token Creature || Saheeli trigger creates Servo  
 - Return Scholar of Ages to play and Non-Token Creature to hand  
 - Scholar returns Mastermind's Acquisition and Blood for Bones  
 - Hand and board state are the same as the start.  
 
 #### Loop yields:  
  - +1 combo piece  
  - +1 servo, maybe  

repeat until all cards are assembled

## Second Loop: Make Treasures

#### Board State:  
Omniscience  
any Non-Token Creature or Saheeli, Sublime Artificer  

#### Hand:  
Mastermind's Acquisition  
Blood For Bones  
Scholar of Ages  
1x Dance of the Manse  
1x Phyrexian Scripture  
4x $\bf{Pitiless Plunderer}$  
4x $\bf{Mirror March}$  
4x $\bf{Mirror March / Mirrormade}$  
1x Woe Strider  
2x Thrill of Possibility  
1x Cleansing Nova/ Creature Boardwipe  
7x $\bf{Seven Dwarves}$

### Setup
 - Play 4x Pitiless Plunderer
 - Play Woe Strider
### Loop
 - Sacrifice 1x Pitiless Plunderer to Woe Strider, create 3 treasures
 - Play Scholar of Ages
 - Blood For Bones sacrificing Scholar of Ages, return Scholar of Ages to play and Pitiless Plunderer to play  
  - Scholar of Ages returns Blood For Bones and any other instant/sorcery of your choice
 - Play Pitiliess Plunderer
 
#### Loop yields:  
 - +3 treasures  
 - +1 instant/sorcery  
 - +1 Pitiless Plunderer or Non-token Creature
 

## Third Loop: Lots and Lots of Treasures 
Here's where things get really nutty so hang in there. We're going to ignore non-essential triggers for brevity and save the formula for the reveal at the end. Steps with bolded numbers will be used in the final calculation.    

#### Board State:  
Omniscience  
any Non-Token Creature or Saheeli, Sublime Artificer  
4x $\bf{Pitiless Plunderer}$  
1x Woe Strider  
8+ Treasures

#### Hand:  
Mastermind's Acquisition  
Blood For Bones  
Scholar of Ages  
4x $\bf{Mirror March}$  
4x $\bf{Mirror March / Mirrormade}$  
2x Thrill of Possibility
1x Dance of the Manse  
1x Phyrexian Scripture  
1x Masterful Replication
1x Cleansing Nova/ Creature Boardwipe

### Setup:  
 - Play 4x Mirror March
 - Play 2x Thrill of possibility discarding Phrexian Scriptures and Mirrormade  

### Loop:  
 - Cast Danse of the Manse x=6+ returning Phyrexian Scriptures and 4x Mirrormade 
  - All enter the battlefield as creatures
  - Mirrormades enter as copy of Mirror March
  - Phyrexian Scriptures first lore counter target Mirrormade, Mirrormade is now an Artifact Enchantment Creature
  - $\bf{8x}$ Mirror Triggers for each Mirrormade and Phyrexian Scriptures
 - Cast Masterful replication targeting an Artifact Enchantment Creature Mirrormade, all treasures become Mirror Marches that are also creatures  
 - Cast Cleansing Nova, choose the first mode: Destroy all creatures.
  - $\bf{4x}$ Pitiless Plunderer Triggers per Copy of Mirrormade and Woe Strider 
  - $\bf{3x}$ Pitliess Plunderer Trigger per Copy of Pitiless Plunderer
  - 4x Mirrormade + 1x Phyrexian Scripture go to the graveyard
 - Loop 2  
  - Play Scholar of Ages
   - return Blood For Bones and another Instant/Sorcery to hand
  - Cast Blood For Bones sacrificing Scholar of Ages
   - Return Scholar of Ages to play and Pitiless Plunderer to hand
   - Cast Pitiless Plunderer
  - Repeat until 4x Pitiless Plunderer are in play
  - Return Danse of the Manse, Cleansing Nova, and any three other instants and sorceries 
  - $\bf{10x}$ Treasures from loop performing Loop 2 five times.  
 - Hand and board state are the same as the start.  
 
### Loops yields:
 - + Treasures 
 - Demonstrates that Treasures = Mirror Marches

# The Math: How fast does this actually grow?

 Once the first loop is assembled it is impossible to fizzle regardless of the outcomes of the Mirror March triggers. It is very likely that you will accrue additional treasures each loop so this formula represents the lower bound on the growth rate.  

## Bringing it all together:
 Let's start with the Mirror March triggers, it's random so how do we count number of tokens generated? We could simulate each flip and add them up, but that's a lot of headache. Because the loop will grow infinitely, it is sufficient to determine the expected of each flip. Here's the formula for calculating the expected valued of a flip: $$\mathop{\mathbb{E}(Trigger)} = \sum_{i=0}^\infty \left(\frac{1}{2}\right)^i$$ 
It's a scary formula, but thanks to the mathematics of infinite sums we can show that the value converges to 1 as the number of triggers approaches infinite. So the formula becomes this: $$\mathop{\mathbb{E}(Trigger)} = 1$$

Now that we've settled how to calculate the expected value of a trigger we can write our formula. We're going to start at the beginning of Loop 3. We can ignore Loops 1 and 2 are the set up for Loop 3 and may yield some number of additional treasures represented as $c$, $c>=0$.  

$m =$ # of Mirror Made + Phyrexian Scriptures each Loop
$p =$ # of Pitiless Plunderers 
$t =$ # of Treasure Tokens

Here are all the relevant triggers that we need to calculate the growth:  
  - $\bf{8x}$ Mirror March Triggers for each Mirrormade and Phyrexian Scriptures, 5 total (4 mirror + 1 Scripture)
  - $\bf{4x}$ Pitiless Plunderer Triggers per Copy of Mirrormade and Woe Strider 
  - $\bf{3x}$ Pitliess Plunderer Trigger per Copy of Pitiless Plunderer
  - $\bf{10x}$ Treasures from loop performing Loop 2 five times.

These triggers yield the following equalities:  
$$m = 5$$
$$p = 4$$
$$t_0 = 0$$
$$m^* = 8 * (m + t_{n-1}) $$
$$t_n = 4 * (m^*+1) + 3 * p + 10$$

substituting in $m*$ we get
  
$$t_n \quad= 4 * (8*(m + t_{n-1})+1) + 3p + 10$$
$$ \quad\quad= 4 * ( 8 *( 5+t_{n-1}+1) + 3 * 4 + 10$$
$$ \quad\quad= 4 * ( 8*5+8t_{n-1} + 1) + 3 * 4 + 10$$
$$ \quad\quad= 32*5+32t_{n-1}+ 4 + 12 + 10$$
$$= 32t_{n-1} + 32(5) + 26$$    



$L_0$ is the state at the beginning of Loop 3 and $t_n$ is a function of $t_n(L_n) = t_n(m,p,t_0)$ .

$$L_0 = (5,4,0) $$
$$L_1 = (5,4,t_1)$$    
$$...$$
$$L_n = (5,4,t_n)$$

Now all we have to do is substitute initial values to find the formula for how $t_n$ grows!  
Using the equalities from above we get:  

Starting from $t_0$ we can calculate the first few iterations to find the formula for $t_n$  
  
$$t_0 = 0 + c = c$$
  
$$t_1 = 32t_0 + 32(5) + 26$$
$$  = 32c + 32(6) + 22$$
  
$$t_2 = 32t_1 + 32(5) + 26$$
$$ = 32\left((32c + 32(5) + 26)\right) + 32(5) + 26$$
$$ = 32*32c + 32*32(5) + 32*26 + 32(5) + 26$$
   
$$t_3 = 32t_2 + 32(5) + 22$$
$$ = 32\left((32*32c + 32*32(5) + 32*26 + 32(5) + 26\right) + 32(5) + 26$$
$$ = 32*32*32c + 32*32*32(5) + 32*32*26 + 32*32(5) + 32*26) + 32(5) + 26$$
$$ = 32^3c + 32^3(5) + 32^2*26 + 32^2(5) + 32*26) + 32(5) + 22$$
$$ = 32^3c + 5(32^3 + 32^32 + 32) + 26(32^2 + 32 + 1)$$

Which ultimately is
$$t_n = 32^{n}c + 5\sum_{i=1}^n 32^{i} + 26\sum_{j=0}^{n-1} 32^{j}$$

With c=0 we get

$$t_n = 5\sum_{i=0}^n 32^{i+1} + 26\sum_{j=0}^{n-1} 32^j$$

The first 6 numbers in the sequence are:
186, 6138, 196602, 6291450, 201326586...


201,326,586 Mirror Marches after 5 loops!  
Now cast your 7  Seven Dwarves and drum roll...  
1,621,436,698 Dwarves attacking for 26,290,569,202,209,156,600 damage!

but we can do even better...

## Third Loop Prime: Not Quite Factorial Treasures 
Here's where things get really nutty so hang in there. We're going to ignore non-essential triggers for brevity and save the formula for the reveal at the end. Steps with bolded numbers will be used in the final calculation.    

#### Board State:    
Omniscience  
Platinum Angel (so we don't lose to accidentally decking ourselves)
any Non-Token Creature or Saheeli, Sublime Artificer  
4x $\bf{Pitiless Plunderer}$  
1x Woe Strider
1x Yarok, the Desacrated
8+ Treasures

#### Graveyard:  
1x Spark Double

#### Hand:  
Mastermind's Acquisition  
Blood For Bones  
Scholar of Ages
Rise From the Grave
4x $\bf{Mirror March}$  
4x $\bf{Mirror March / Mirrormade}$  
2x Thrill of Possibility
1x Spark Double
1x Dance of the Manse  
1x Phyrexian Scripture  
1x Masterful Replication
1x Cleansing Nova/ Creature Boardwipe

### Setup:  
 - Play 4x Mirror March
 - Play 2x Thrill of possibility discarding Phrexian Scriptures and Mirrormade  

### Loop:

 - Cast Danse of the Manse x=6+ returning Phyrexian Scriptures and 4x Mirrormade 
  - All enter the battlefield as creatures
  - Mirrormades enter as copy of Mirror March
  - Phyrexian Scriptures first lore counter target Mirrormade
    - Mirrormade is now an Artifact Enchantment Creature
  - $\bf{8}$ Mirror Triggers for each Mirrormade and Phyrexian Scriptures
 - Cast Masterful replication targeting an Artifact Enchantment Creature Mirrormade, all treasures become Mirror Marches  
  - $8 * (t_{n}+5)$ Mirror Marches on the board 


 
###  Addendum (can be looped, but it's more efficient to complete the full loop)
   - Cast Rise From the Grave bringing back Spark Double
     - Spark Double copies Yarok  
    - $\sum_{i=0}^{8 * (t_{n}+5)}  i *8 * (t_{n}+5)$ copies of Spark Doubled Yarok Enter the battlefield
   - Cast Blood For Bones, sacrificing Pitiless Plunderer  
   - Return Pitiless Plunderer to play  
   - $\left(8 * (t_{n}+5)\right)*\sum_{i=0}^{8 * (t_{n}+5)}  i *8 * (t_{n}+5)$ Mirror March triggers
### End of Addendum   


 Cast Cleansing Nova, choose the first mode: Destroy all creatures.
  - $\left(8 * (t_{n}+5)\right)*\sum_{i=0}^{8 * (t_{n}+5)}  i *8 * (t_{n}+5)$ Pitiless Plunderer Triggers per Copy of Mirrormade and Woe Strider 
  - $\left(8 * (t_{n}+5)\right)*\sum_{i=0}^{8 * (t_{n}+5)}  i *8 * (t_{n}+5)$ Pitliess Plunderer Trigger per Copy of Pitiless Plunderer
  - 4x Mirrormade + 1x Phyrexian Scripture go to the graveyard
 - Loop 2  
  - Play Scholar of Ages
   - return Blood For Bones and another Instant/Sorcery to hand
  - Cast Blood For Bones sacrificing Scholar of Ages
   - Return Scholar of Ages to play and Pitiless Plunderer to hand
   - Cast Pitiless Plunderer
  - Repeat until 4x Pitiless Plunderer are in play
  - Return Danse of the Manse, Cleansing Nova, and any three other instants and sorceries 
  - $\bf{10x}$ Treasures from loop performing Loop 2 five times.  
 - Hand and board state are the same as the start.  
 
### Loops yields:
 - + Treasures 
 - Demonstrates that Treasures = Mirror Marches

# Even More Ridiculous


Here are all the relevant triggers that we need to calculate the new growth rate  
  - $\left(8 * (t_{n}+5)\right)*\sum_{i=0}^{8 * (t_{n}+5)}  i *8 * (t_{n}+5)$ Treasures per Copy of Mirrormade, Yarok, and Woe Strider
  - $\left(8 * (t_{n}+5)\right)*\sum_{i=0}^{8 * (t_{n}+5)}  i *8 * (t_{n}+5)$ Treasures per Copy of Pitliess Plunderer

We're going to handwave a little bit here and simplify the formula to something manageable.

  - $2*\left(8 * (t_{n}+5)\right)*\sum_{i=0}^{8 * (t_{n}+5)}  i *8 * (t_{n}+5)$ Treasures per Copy of Mirrormade, Yarok, Woe Strider, $\bf{and}$ Pitliess Plunderer

first, let $\bf{t_n} =\bf{x_n^*} = 8 * (t_{n}+5))$ this reduces the equation to the following

  - $ x_{n+1}^* =  2 * (x_n^* \sum_{i=0}^{x_n^*}  i x_n^*)$

Plugging this into wolfram alpha gives us

  - $ x^3 (x + 1) $
  
With the initial condition of 
$$t_0 = 0$$  
$$x_0 = 8 * (t_0+5))$$
$$\quad = 8*(0+5)$$
$$x_0 = 40\quad\quad$$

The first 5 iterations the sequence are:  
n | x(n)  
0 | 40  
1 | 40  
2 | 2.624×10^6  
3 | 4.74084×10^25  
4 | 5.05152×10^102  
5 | 6.511601479437871×10^410  
6 | 1.797840885440867×10^1643  
7 | 1.04473227280353×10^6573  
8 | 1.19129698535941×10^26292  
9 | 2.0140960193274×10^105168  


6.511601479437871×10^410  Mirror Marches after 5 loops!  
Now cast your 7 even Dwarves and drum roll...  
4.5581210356×10^411  Dwarves attacking for 20.7764673752x10^823 damage!

That's more dwarves than there are atoms in the observable universe if every atom were also an entire universe, nested like that 3 more times.


```python

```
