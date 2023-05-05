Download Link: https://assignmentchef.com/product/solved-ece269-homework-3
<br>
<ol>

 <li><strong>Problem 1: Orthogonal Complement of a Subspace. </strong>Suppose that V is a subspace of <strong>R</strong><em><sup>n</sup></em>. Let</li>

</ol>

V<sup>⊥ </sup>= {<strong>x </strong>∈ <strong>R</strong><em><sup>n </sup></em>: <strong>x</strong><em><sup>T</sup></em><strong>y </strong>= 0, ∀<strong>y </strong>∈ V}

be the set of vectors orthogonal to every element in V.

<ul>

 <li>Verify that V<sup>⊥ </sup>is a subspace of <strong>R</strong><em><sup>n</sup></em>.</li>

 <li>Suppose that V = span(<strong>v</strong><sub>1</sub>, <strong>v</strong><sub>2</sub>, . . . , <strong>v</strong><em><sub>k</sub></em>) for some <strong>v</strong><sub>1</sub>, <strong>v</strong><sub>2</sub>, . . . , <strong>v</strong><em><sub>k </sub></em>∈ <strong>R</strong><em><sup>n</sup></em>. Express V and V<sup>⊥</sup></li>

</ul>

as subspaces induced by the matrix <strong>A </strong><strong>R</strong><em><sup>n</sup></em><sup>×<em>k </em></sup>and its transpose

<strong>A</strong><em>T</em>.

<ul>

 <li>Show that (V<sup>⊥</sup>)<sup>⊥ </sup>= V.</li>

 <li>Show that dim(V) + dim(V<sup>⊥</sup>) = <em>n</em>.</li>

 <li>Show that V ⊆ W for another subspace W implies W<sup>⊥ </sup>⊆ V<sup>⊥</sup>.</li>

 <li>Show that every <strong>x </strong>∈ <strong>R</strong><em><sup>n </sup></em>can be expressed uniquely as <strong>x </strong>= <strong>v </strong>+ <strong>v</strong><sup>⊥</sup>, where <strong>v </strong>∈ V and <strong>v</strong><sup>⊥ </sup>∈ V<sup>⊥</sup>. (Hint: Let <strong>v </strong>be the projection of <strong>x </strong>on V.)</li>

</ul>

<ol start="2">

 <li><strong>Problem 2: Projection Matrices. </strong>A symmetric matrix <strong>P </strong>= <strong>P</strong><em><sup>T </sup></em>∈ <strong>R</strong><em><sup>n</sup></em><sup>×<em>n </em></sup>is said to be a <em>projection matrix </em>if <strong>P </strong>= <strong>P</strong><sup>2</sup>.</li>

</ol>

*For more information on Academic Integrity Policies at UCSD, please visit http://academicintegrity.ucsd.

edu/excel-integrity/define-cheating/index.html

<ul>

 <li>Show that if <strong>P </strong>is a projection matrix, then so is <strong>I </strong>− <strong>P</strong>.</li>

 <li>Suppose that the columns of <strong>U </strong>∈ <strong>R</strong><em><sup>n</sup></em><sup>×<em>k </em></sup>are orthonormal. Show that <strong>UU</strong><em><sup>T </sup></em>is a projection matrix.</li>

 <li>Suppose that <strong>A </strong>∈ <strong>R</strong><em><sup>n</sup></em><sup>×<em>k </em></sup>is full-rank with <em>k </em>≤ <em>n</em>. Show that <strong>A</strong>(<strong>A</strong><em><sup>T</sup></em><strong>A</strong>)<sup>−</sup><sup>1</sup><strong>A</strong><em><sup>T </sup></em>is a projection matrix.</li>

 <li>Recall from lectures that the point <strong>y </strong>∈ S ⊆ <strong>R</strong><em><sup>n </sup></em>closest to <strong>x </strong>∈ <strong>R</strong><em><sup>n </sup></em>is said to be the <em>orthogonal projection </em>(or <em>projection </em>in short) of <strong>x </strong>onto S. Show that if <strong>P </strong>is a projection matrix, then <strong>y </strong>= <strong>Px </strong>is the projection of <strong>x </strong>onto R(<strong>P</strong>).</li>

 <li>Let <strong>u </strong>be a unit vector (A unit vector is a vector normalized by its norm). Find the projection matrix <strong>P </strong>such that <strong>y </strong>= <strong>Px </strong>is the projection of <strong>x </strong>onto span(<strong>u</strong>).</li>

</ul>

<strong>Programming Assignment:</strong>

<strong>Finding Sparse Solutions via Orthogonal Matching Pursuit (OMP)</strong>

In this mini project, we will implement and study the performance of the Orthogonal Matching Pursuit (OMP) algorithm for recovering sparse signals and images.

<strong>Required Reading: </strong>Read the paper “Greed is good: algorithmic results for sparse approximation” by Joel Tropp to learn about OMP (available on Canvas under Files&gt;Homework), and relevant lectures and discussion sessions. For this assignment, you will mainly need to understand the algorithm (and not the proofs concerning the theoretical performance guarantees of OMP), although you are certainly encouraged to go over them and discuss with Prof. Pal if you are interested.

Consider the measurement model

<strong>y </strong>= <strong>Ax </strong>+ <strong>n</strong>

where <strong>y </strong>∈ <strong>R</strong><em><sup>M </sup></em>is the (compressed, <em>M </em><em>&lt; N</em>) measurement, <strong>A </strong>∈ <strong>R</strong><em><sup>M</sup></em><sup>×<em>N </em></sup>is the measurement matrix, and <strong>n </strong>∈ <strong>R</strong><em><sup>N </sup></em>is the additive noise. Here, <strong>x </strong>∈ <strong>R</strong><em><sup>N </sup></em>is the unknown signal (to be estimated) with <em>s </em>≪ <em>N </em>non-zero elements. The indices of the non-zero entries of <strong>x </strong>(also known as the support of <strong>x</strong>) is denoted by S = {<em>i</em>|<em>x<sub>i </sub></em≯= 0}, with |S| = <em>s</em>.

<ol>

 <li><strong>Performance Metrics: </strong>Let <strong>xˆ </strong>be the estimate of <strong>x </strong>obtained from OMP. To measure the performance of OMP, we consider the Normalized Error defined as</li>

</ol>

The average Normalized Error is obtained by averaging the Normalized Error over 2000 Monte Carlo runs.

<ol start="2">

 <li><strong>Experimental setup:</strong>

  <ul>

   <li>Generate <strong>A </strong>as a random matrix with independent and identically distributed entries drawn from the standard normal distribution. Normalize the columns of <strong>A</strong>.</li>

   <li>Generate the sparse vector <strong>x </strong>with random support of cardinality <em>s </em>(i.e. <em>s </em>indices are generated uniformly at random from integers 1 to <em>N</em>), and non-zero entries drawn as uniform random variables in the range [−10, −1] ∪ [1, 10].</li>

   <li>The entries of noise <strong>n </strong>are drawn independently from the normal distribution with standard deviation <em>σ </em>and zero mean.</li>

   <li>For each cardinality <em>s </em>∈ [1, <em>s<sub>max</sub></em>], the average Normalized Error should be computed by repeating step (a) to step (c) 2000 times and averaging the results over these 2000 Monte Carlo runs.</li>

  </ul></li>

 <li><strong>Noiseless case: (n </strong>= <strong>0)</strong></li>

</ol>

Implement OMP (you may stop the OMP iterations once ∥<strong>y </strong>− <strong>Ax</strong><sup>(<em>k</em></sup><sup>)</sup>∥<sub>2 </sub>is close to 0 and evaluate its performance. Calculate the probability of Exact Support Recovery (i.e. the fraction of runs when Sˆ = S) by averaging over 2000 random realizations of <strong>A</strong>, as a function of <em>M </em>and <em>s<sub>max </sub></em>(for different fixed values of <em>N</em>). For each <em>N</em>, the probability of exact support recovery is a two dimensional plot (function of <em>M </em>and <em>s<sub>max</sub></em>) and you can display it as an image. The resulting plot is called the “noiseless phase transition” plot, and it shows how many measurements (<em>M</em>) are needed for OMP to successfully recover the sparse signal, as a function of <em>s<sub>max</sub></em>. Do you observe a sharp transition region where the probability quickly transitions from a large value (close to 1) to a very small value (close to 0)? Generate different phase transition plots for the following values of N: 20, 50 and 100. Regenerate phase transition plots for average Normalized Error (instead of probability of successful recovery). Comment on both kinds of plots.

<ol start="4">

 <li><strong>Noisy case: (n </strong≯= <strong>0)</strong></li>

</ol>

<ul>

 <li>Assume that sparsity <em>s </em>is known. Implement OMP (terminate the algorithm after first <em>s </em>columns of <strong>A </strong>are selected). Generate “noisy phase transition” plots (for fixed <em>N </em>and <em>σ</em>) where success is defined as the event that the Normalized Error is less than 10<sup>−3</sup>. Repeat the experiment for two values of <em><sub>σ </sub></em>(one small and one large) and choose <em>N </em>as 20, 50 and 100. Comment on the results.</li>

 <li>Assume the sparsity <em>s </em>is NOT known, but ∥<strong>n</strong>∥<sub>2 </sub>is known. Implement OMP where you may stop the OMP iterations once ∥<strong>y </strong>− <strong>Ax</strong><sup>(<em>k</em></sup><sup>)</sup>∥ ≤ ∥<strong>n</strong>∥<sub>2</sub>). Generate phase transition plots using the same criterion for success as the previous part. Comment on the results.</li>

</ul>

<ol start="5">

 <li><strong>Decode a Compressed Message: </strong>In this part of the assignment, you will uncover a hidden message from their compressed sketches (generated using random measurement matrices) using the OMP algorithm that seeks the sparsest solution. An unknown and sparse image <strong>X</strong>, containing a message, has been compressed using three different random matrices (of different sizes) <strong>A</strong><sub>1</sub>, <strong>A</strong><sub>2</sub>, <strong>A</strong><sub>3 </sub>to produce three corrupted images as follows</li>

</ol>

<strong>Y</strong><em><sub>i </sub></em>= <strong>A</strong><em><sub>i</sub></em><strong>X</strong>

The corrupted images and the measurement matrices are provided to you under Files&gt;Homework.

<ul>

 <li>Can you guess the message by simply displaying the compressed images?</li>

 <li>Using OMP, recover <strong>X </strong>from <strong>Y</strong><sub>1</sub>, <strong>Y</strong><sub>2</sub>, <strong>Y</strong><sub>3</sub>. Figure out the appropriate stopping criteria. Reshape the recovered <strong>X </strong>into a 2D image of size 90 × 160 and decode the message. Show your results for each case. Compare these results with the Least Squares Solution.</li>

 <li>Which corrupted image gave you the best result for OMP? Can you explain why?</li>

 <li>(<em>For Fun</em>) Can you make an (educated) guess about the meaning of this message?</li>

</ul>