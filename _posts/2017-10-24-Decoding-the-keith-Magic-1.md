---
layout: post
title: Decoding the Keith Magic-The Division Theorem
---
`**`A slight detailed look into the world of Keith Konrad.`**`


So I decided to work on my Number theory concepts this semester for my Cryptography course.
The initial stages were not so great for me as the concepts such as Chinese Remainder theorems etc were a bit too overwhelming for me. That is when I came to a decision where, instead of just working on the superficial level, I will be concentrating more on the proofs side to make things more vivid than how they were currently.
Thanks to one of my friend’s mutual interest in Number theory I was fortunate enough to be introduced to Expository papers by Keith Konrad.
Hence I decided to work on one paper every two days. 
I would like to call this series as “Decoding the Keith magic”. The thoughts that I will be presenting  here are my own personal thoughs and I would say quite noobish too. While studying these papers, I came across so many supposedly trivial things which made me question the entire existance of Mathematics at times. (Aah! Yes I’m a bit slow and abnormally inquisitive)

So the first paper that I read is `**`THE DIVISION THEOREM IN Z AND F [T ]`**`, which is the first paper in the Keith Konrad Elemantary series.

The link to the paper:-

My personal viewpoints on this paper:-

So the paper begins by talking about the most commonly used theorem in Mathematics, which is the remainder theorem.
According to the Theorem 1.1. For any integers a and b, with b 6= 0 there are unique integers q and r such
that
a = bq + r; 0 ≤ r < jbj:
and the Thorem 1.2 is the more generic form of the previously stated theorem according to which,  Let F be a field. For any f(T ) and g(T ) in F [T ], with g(T ) != 0, there are
unique q(T ) and r(T ) in F [T ] such that
f(T ) = g(T )q(T ) + r(T ); r(T ) = 0 or deg r(T ) < deg g(T )
To be frank this is a very trivial paper, and the difficulty level is not that high. For understanding these poofs we first need to clearly imagine what the theorem is trying to state. 
So I will not be writing the proof step by step here as you can quite easily refer to the original paper that I have given in the link above. This post is directed more towards my self understanding and for people who find such Mathematics way beyond understanding.
All we need to do for understanding these proofs is to proceed logically and understand why and how everything is happening.

So the first theorem as it is seems pretty obvious where a number  ‘a’ can be represented in the form of a = bq + r; 0 ≤ r < jbj:

Moving on to the 2nd Theorem that is stated here, it starts by stating let F be a field. Having a slight base in Linear Algebra certainly helps at times.
What do they mean by field here?
Well, a field is a set or collection on which we can perform certain operations. Basically operations such as +,*. Examples of fields are Q,R,C i.e Rational, Real and Complex numbers.
SO do you spot some co relation between the 1st and the 2nd theorem? Isn’t 1st theorem one of the cases of the 2nd one?????? 

Now think a bit logically, the moment we look at the theorem what all can we infer?
->Well, we can see that if suppose b is a number that is exactly divisible by a, then in that case the remainder value comes out be ZERO(DUH) Is that not obvious?
 ->The value of r HAS to be less than b. Think a little logically, IF the value of r = b then what happens? The same statement can be written as  a = bq + b which basically is  a = b(q+1) + 0.
Similarly if r > b then it means that is not the true remainder. ( True remainder? could’t find the right term to go with this one).

Now that some obvious things are clear the first proof becomes quite evident.
Case: b > 0
	bq ≤ a < b(q + 1)
 Is that not the case? for some q including Z
	subtract bq from all terms
	0 ≤ a − bq < b
	Set r = a − bq, 
	so 0 ≤ r < b = jbj
Does it seem obvious now? It should, it was just logical deductions.

Now we go for the 2nd proof, which is a more fullproof solution to this. This solution can also be extented to the 2nd theorem unlike the previous proof (Will explain why, soon).

SO we are going to enter the world of (Strong) Induction. Okay so currently I am at a stage where I cannot really deduce if to use Strong or weak induction, maybe one of the readers can help me out with that or I will read about it soon.
Anyway so here Konrad makes use of Strong induction to prove this theorem.

Case 1: a > 0
	 We FIX b > 0
	Case a: If 0 ≤ a < b
		=> q = 0 and r = a
	Case b:  a ≥ b
		  all integers a0 with 0 ≤ a0 < a 
		  existence of a q0 and r0 for a0 
		  and b in Theorem 1.1
		a0 := a − b. Since a ≥ b > 0, we have 0 ≤ a0 < a

		We get a − b = bq0 + r0; 0 ≤ r0 < b;
		Add b to both the sides
		a = b(q0 + 1) + r0 (BAM)
		Replace the required stuff

Case 2: Think a bit or directly check out Konrads paper.

Now to the interesting part, that is proving the second theorem.
Well like I said the 1st theorem is just one of the cases of 2nd  theorem. 
It is claimed that F(T) is a field. So we are picking f(T) and g(T) from that field. Remember, the fact that they are being picked up from a field is an integral part of the proof.
 The fact that we cannot use the first proof of the previous theorem here is because how do we divide the polynomials in equal spaces?

SO what are we expected to prove here?
	(1) f(T ) = g(T )q(T ) + r(T ),
	(2) r(T ) = 0 or deg r(T ) < deg g(T )

For proving it for functions we can proceed by taking different cases:
Case 1: IF your f(T) = 0
	Then it automatically tells us that for ANY g(T), q(T) and r(T), both are zero.
Case 2: g(T ) is constant (that is, deg g(T ) = 0) 
	 q(T ) = (1=c)f(T ) and r(T ) = 0
	 Quite obvious again.
Case 3:nonconstant g(T ) E F [T ]
	Case a:  n < deg g(T )
		   q(T ) = 0 and r(T ) = f(T )
		  Do you see this? If in the equation  f(T ) = g(T )q(T ) + r(T )
		  Is not similar to the first case in the previous theorem
	Case b: n ≥ deg g(T ) and the existence of q(T ) and r(T ) is true for g(T ) and all
		polynomials f(T ) of degree less than n
		
		f(T ) = anT n + lower order terms;
		g(T ) = cdT d + lower order terms:

		And BAM by manipulating these, you can refer Konrads paper for more details as he has given it quite well we can come to the conclusion.
 Well I will explain it in words as from my next article I WILL HAVE TO shift to LATEX.
It is getting really difficult here.

But anyway look at f(T) and g(T),  Multiplying g(T) by T n−d raises its degree to n
Now when we get that we rearragne and get it in this form
![_config.yml]({{ site.baseurl }}/Images/kmath1.jpg)

The only reason we can divide the term is because it is contained in a field.
And comparing these two equations we can bring it down to the form that we want.
Hurray we are done with the  first paper of the series. 
