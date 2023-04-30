Download Link: https://assignmentchef.com/product/solved-csc421-2516-homework-1
<br>
<strong>Submission: </strong>You must submit your solutions as a PDF file through MarkUs<a href="#_ftn1" name="_ftnref1"><sup>[1]</sup></a>. You can produce the file however you like (e.g. LaTeX, Microsoft Word, scanner), as long as it is readable.

<strong>Late Submission: </strong>MarkUs will remain open until 3 days after the deadline, after which no late submissions will be accepted.

Weekly homeworks are individual work. See the Course Information handout<a href="#_ftn2" name="_ftnref2"><sup>[2]</sup></a> for detailed policies.

<ol>

 <li><strong>Hard-Coding a Network. [2pts] </strong>In this problem, you need to find a set of weights and biases for a multilayer perceptron which determines if a list of length 4 is in sorted order. More specifically, you receive four inputs <em>x</em><sub>1</sub><em>,…,x</em><sub>4</sub>, where <em>x<sub>i </sub></em>∈ R, and the network must output 1 if <em>x</em><sub>1 </sub><em>&lt; x</em><sub>2 </sub><em>&lt; x</em><sub>3 </sub><em>&lt; x</em><sub>4</sub>, and 0 otherwise. You will use the following architecture:</li>

</ol>

All of the hidden units and the output unit use a hard threshold activation function:

Please give a set of weights and biases for the network which correctly implements this function (including cases where some of the inputs are equal). Your answer should include:

<ul>

 <li>A 3 × 4 weight matrix <strong>W</strong><sup>(1) </sup>for the hidden layer</li>

 <li>A 3-dimensional vector of biases <strong>b</strong><sup>(1) </sup>for the hidden layer</li>

 <li>A 3-dimensional weight vector <strong>w</strong><sup>(2) </sup>for the output layer</li>

 <li>A scalar bias <em>b</em><sup>(2) </sup>for the output layer</li>

</ul>

You do not need to show your work.

<ol start="2">

 <li>Consider a neural network with <em>N </em>input units, <em>N </em>output units, and <em>K </em>hidden units. The activations are computed as follows:</li>

</ol>

<strong>z </strong>= <strong>W</strong>(1)<strong>x </strong>+ <strong>b</strong>(1)

<strong>h </strong>= <em>σ</em>(<strong>z</strong>) <strong>y </strong>= <strong>x </strong>+ <strong>W</strong>(2)<strong>h </strong>+ <strong>b</strong>(2)<em>,</em>

1

CSC421/2516 Winter 2019                                                                                                                            Homework 1

where <em>σ </em>denotes the logistic function, applied elementwise. The cost will involve both <strong>h </strong>and <strong>y</strong>:

J = R + S R = <strong>r</strong><sup>&gt;</sup><strong>h</strong>

for given vectors <strong>r </strong>and <strong>s</strong>.

<ul>

 <li><strong>[1pt] </strong>Draw the computation graph relating <strong>x</strong>, <strong>z</strong>, <strong>h</strong>, <strong>y</strong>, R, S, and J.</li>

 <li><strong>[3pts] </strong>Derive the backprop equations for computing <strong>x </strong>= <em>∂</em>J<em>/∂</em><strong>x</strong>. You may use <em>σ</em><sup>0 </sup>to denote the derivative of the logistic function (so you don’t need to write it out explicitly).</li>

</ul>

<ol start="3">

 <li><strong>Sparsifying Activation Function. [4pts] </strong>One of the interesting features of the ReLU activation function is that it sparsifies the activations and the derivatives, i.e. sets a large fraction of the values to zero for any given input vector. Consider the following network:</li>

</ol>

Note that each <em>w<sub>i </sub></em>refers to the weight on a <em>single </em>connection, not the whole layer. Suppose we are trying to minimize a loss function L which depends only on the activation of the output unit <em>y</em>. (For instance, L could be the squared error loss .) Suppose the unit <em>h</em><sub>1 </sub>receives an input of -1 on a particular training case, so the ReLU evaluates to 0. Based only on this information, which of the weight derivatives

are <strong>guaranteed </strong>to be 0 for this training case? Write YES or NO for each. Justify your answers.

2

<a href="#_ftnref1" name="_ftn1">[1]</a> <a href="https://markus.teach.cs.toronto.edu/csc421-2019-01">https://markus.teach.cs.toronto.edu/csc421-2019-01</a>

<a href="#_ftnref2" name="_ftn2">[2]</a> <a href="http://www.cs.toronto.edu/~rgrosse/courses/csc421_2019/syllabus.pdf">http://www.cs.toronto.edu/</a><a href="http://www.cs.toronto.edu/~rgrosse/courses/csc421_2019/syllabus.pdf">~</a><a href="http://www.cs.toronto.edu/~rgrosse/courses/csc421_2019/syllabus.pdf">rgrosse/courses/csc421_2019/syllabus.pdf</a>