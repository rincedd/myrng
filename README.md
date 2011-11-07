# MyRNG: A convenient random number generator

The MyRNG C++ classes provide two very efficient random number generators 
and several methods for generating random variates. You can choose between 
the Mersenne Twister MT19937a algorithm in the implementation of [Makoto
Matsumoto and Takuji Nishimura][1] and the well-equidistributed long-period 
linear generator [WELL1024a][2] implemented by Marton Morvai. Both generators are
essentially shuffled linear congruential random number generators; they should
not be used for cryptography applications but should otherwise cover most 
scientific needs. While the WELL1024a is slightly faster in the current 
implementation, the MT19937a has an astronomical recurrence time of 2^19937. 
Furthermore, the methods are provided to generate several random variates 
including uniform, Gaussian, Beta, and Gamma distributions. Generation of most
random variates is based on [Law and Kelton, 2000][3]. Generation of the Gamma 
distribution is based on [Marsagli and Tsang, 2000][4].

[1]: http://www.math.sci.hiroshima-u.ac.jp/~m-mat/MT/emt.html "M. Matsumoto and T. Nishimura. Personal web pages." 
[2]: http://dx.doi.org/10.1145/1132973.1132974 "F. Panneton et al.: Improved long-period generators based on linear recurrences modulo 2, ACM Transactions on Mathematical Software, 32(1), 1-16,2006."
[3]: http://dl.acm.org/citation.cfm?id=550113 "A.M. Law and W.D. Kelton: Simulation, modeling and analysis, Third Edition, McGraw Hill, 2006."
[4]: http://dx.doi.org/10.1145/358407.358414 "G. Marsaglia and W.W. Tsang: A simple method for generating gamma variables, ACM TOMS 26, 2000."
