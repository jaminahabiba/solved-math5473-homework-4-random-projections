Download Link: https://assignmentchef.com/product/solved-math5473-homework-4-random-projections
<br>



<ol>

 <li><em>SNPs of World-wide Populations: </em>This dataset contains a data matrix <em>X </em>∈ R<em><sup>n</sup></em><sup>×<em>p </em></sup>of about <em>p </em>= 650<em>,</em>000 columns of SNPs (Single Nucleid Polymorphisms) and <em>n </em>= 1064 rows of peoples around the world (but there are 21 rows mostly with missing values). Each element is of three choices, 0 (for ‘AA’), 1 (for ‘AC’), 2 (for ‘CC’), and some missing values marked by 9. <a href="https://drive.google.com/file/d/1KMLPEG91mnzdK2pUlq2BkjOx2BsaZy9s/view?usp=sharing">https://drive.google.com/file/d/1KMLPEG91mnzdK2pUlq2BkjOx2BsaZy9s/view?usp=sharing </a>which is big (151MB in zip and 2GB original txt). Moreover, the following file contains the region where each people comes from, as well as two variables ind1 andind2 such that <em>X</em>(ind1<em>,</em>ind2) removes all missing values.</li>

</ol>

<a href="https://github.com/yao-lab/yao-lab.github.io/blob/master/data/HGDP_region.mat">https://github.com/yao-lab/yao-lab.github.io/blob/master/data/HGDP_region.mat </a>Another cleaned dataset is due to Quanhua MU and Yoonhee Nam:

<ul>

 <li>Genotyped data of the 1043 (<em>n</em>) subjects. 0(AA), 1(AC), 2(CC). Missing values are removed, only autosomal SNPs were selected (<em>p </em>≈ 400<em>K</em>). Google drive link:</li>

</ul>

<a href="https://drive.google.com/file/d/1a9I8_akfCMHBRrPMdnWkjyL9fKcQbJJq/view?usp=sharing">https://drive.google.com/file/d/1a9I8_akfCMHBRrPMdnWkjyL9fKcQbJJq/view?us</a>p= <a href="https://drive.google.com/file/d/1a9I8_akfCMHBRrPMdnWkjyL9fKcQbJJq/view?usp=sharing">sharing</a>

<ul>

 <li>Sample Information of 1043 subjects. Google drive link: <a href="https://drive.google.com/file/d/11Q-8B57WDQnrIV92b-h_WLqDGviiYsm2/view?usp=sharing">https://drive.google.com/file/d/11Q-8B57WDQnrIV92b-h_WLqDGviiYsm2/view?us</a>p= <a href="https://drive.google.com/file/d/11Q-8B57WDQnrIV92b-h_WLqDGviiYsm2/view?usp=sharing">sharing</a></li>

</ul>

A good reference for this data can be the following paper in Science, <a href="https://www.sciencemag.org/content/319/5866/1100.abstract">http://www.sciencemag.org/content/319/5866/1100.abstract</a>

Explore the genetic variation of those persons with their geographic variations, by MDS/PCA. Since <em>p </em>is big, explore random projections for dimensionality reduction.

<ol start="2">

 <li><em>Phase Transition in Compressed Sensing: </em>Let <em>A </em>∈ R<em><sup>n</sup></em><sup>×<em>d </em></sup>be a Gaussian random matrix, <em>e. A<sub>ij </sub></em>∼ N(0<em>,</em>1). In the following experiments, fix <em>d </em>= 20. For each <em>n </em>= 1<em>,…,d</em>, and each <em>k </em>= 1<em>,…,d</em>, repeat the following procedure 50 times:</li>

</ol>

1

<em>Homework 4. Random Projections                                                                                                                                          </em>2

<ul>

 <li>Construct a sparse vector <em>x</em><sub>0 </sub>∈ R<em><sup>d </sup></em>with <em>k </em>nonzero entries. The locations of the nonzero entries are selected at random and each nonzero equals ±1 with equal probability;</li>

 <li>Draw a standard Gaussian random matrix <em>A </em>∈ R<em><sup>n</sup></em><sup>×<em>d</em></sup>, and set <em>b </em>= <em>Ax</em><sub>0</sub>;</li>

 <li>Solve the following linear programming problem to obtain an optimal point ˆ<em>x</em>,</li>

</ul>

min<em><sub>x              </sub></em>k<em>x</em>k<sub>1 </sub>:= <sup>X</sup>|<em>x<sub>i</sub></em>|

<em>s.t.        Ax </em>= <em>b,</em>

for example, matlab toolbox cvx can be an easy solver;

(d) Declare success if k<em>x</em>ˆ − <em>x</em><sub>0</sub>k ≤ 10<sup>−3</sup>;

After repeating 50 times, compute the success probability <em>p</em>(<em>n,k</em>); draw a figure with x-axis for <em>k </em>and y-axis for <em>n</em>, to visualize the success probability. For example, matlab command imagesc(p) can be a choice.

Can you try to give an analysis of the phenomenon observed? The following paper by Tropp et al. may give you a good starting point to think.

<ul>

 <li>Dennis Amelunxen, Martin Lotz, Michael B. McCoy, Joel A. Tropp. Living on the edge: Phase transitions in convex programs with random data. arXiv:1303.6672. URL:</li>

</ul>

<a href="https://arxiv.org/abs/1303.6672">https://arxiv.org/abs/1303.6672</a>