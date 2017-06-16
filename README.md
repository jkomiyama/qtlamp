QTLAMP: A library for Emerging Pattern Mining with Multiple Hypothesis Testing Correction

- - -
1\. [About](#about)  
2\. [Environment](#environment)  
3\. [Quick run](#quick)  
4\. [Misc](#misc)  
- - -

.
<a name="about"></a>

## 1\. About
  This is a C++ package for statistical emerging pattern mining (SEPM) simulations.
  For the details of SEPM, see [our paper](http://www.tkl.iis.u-tokyo.ac.jp/~jkomiyama/pdf/kdd-statistical-emerging.pdf)
  The implementation of this package is based on [LCM++](https://code.google.com/archive/p/lcmplusplus/).

     
<a name="environment"></a>

## 2\. Environment
  This program supports a linux/GNU C++ environment. We do not check windows/MacOSX.
  
  Required packages:
  - C++0x: modern C++ compiler (preferably GNU C++ (g++))
  -  waf (included) [7]: build script
  
<a name="quick"></a>

## 3\. Quick run
  Type 

    ./script/download.sh
    make
    time ./script/compare_methods.sh datasets/converted/svmguide3.label 0.3 10000000 6
    
  , which will finish within ten minutes with modern hardware. The result of the runs will be like
    
    qtlamp$ cat out/svmguide3-result-0.3-10000000-6-txt
    Result of file out/svmguide3-6.fdr.out
    Num of patterns found: 4971
    Result of file out/svmguide3-6.fdrby.out
    Num of patterns found: 1729
    Result of file out/svmguide3-6.fwer.out
    Num of patterns found: 536
    Result of file out/svmguide3-6.bh.out
    Num of patterns found: 1345
    Result of file out/svmguide3-6.ep.out
    Num of patterns found: 43461
  
  Note that the result of fdr minings can change slightly for each run due to its stochastic nature.

  This package also includes a simple plot tool (simpleplot.py) that is dependent on Python/Matplotlib.
  If your environment is g++/Python ready, try
  
    ./example.sh

<a name="misc"></a>

## 4\. Misc
  The ascii art is from [9].
  
## 5\. Acknowledgement
  The author thanks Huasen Wu for pointing out our misimplementation (fixed) of the Condorcet SAVAGE algortihm.

  
##References
    [1] Junpei Komiyama, Junya Honda, Hisashi Kashima, Hiroshi Nakagawa: Regret Lower Bound and Optimal Algorithm in Dueling Bandit Problem. In COLT, 2015
    [2] Yisong Yue, Josef Broder, Robert Kleinberg, and Thorsten Joachims: The k-armed dueling bandits problem. J. Comput. Syst. Sci., 78(5):1538–1556, 2012.
    [3] Yisong Yue and Thorsten Joachims. Beat the mean bandit. In ICML, pp 241–248, 2011.
    [4] Tanguy Urvoy, Fabrice Clerot, Raphael Feraud, and Sami Naamane. Generic exploration and k-armed voting bandits. In ICML, pp 91–99, 2013 
    [5] Masrour Zoghi, Shimon Whiteson, Remi Munos, and Maarten de Rijke. Relative upper confidence bound for the k-armed dueling bandit problem. In ICML, pp 10–18, 2014.
    [6] Nir Ailon, Zohar Shay Karnin, and Thorsten Joachims. Reducing dueling bandits to cardinal bandits. In ICML, pp 856–864, 2014
    [7] Waf - The meta build system: https://code.google.com/p/waf/
    [8] Hideyuki Tanaka: cmdline https://github.com/tanakh/cmdline
    [9] Duel (ascii art): http://ascii.co.uk/art/duel

##Author
  Junpei Komiyama (junpei.komiyama atmark gmail.com)


  Please acknowledge its use with a citation: 
+  Junpei Komiyama, Junya Honda, Hisashi Kashima, Hiroshi Nakagawa. Regret Lower Bound and Optimal Algorithm in Dueling Bandit Problem. In Proceedings of the 28th Annual Conference on Learning Theory (COLT 2015), pages 1141-1154
, July 2015
