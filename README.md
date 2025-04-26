# cs335-endsem-lab-solved
**TO GET THIS SOLUTION VISIT:** [CS335 Endsem Lab Solved](https://www.ankitcodinghub.com/product/ai-ml-lab-cs335/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;124291&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;2&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;5&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;5\/5 - (2 votes)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;CS335 Endsem Lab Solved&quot;,&quot;width&quot;:&quot;138&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

<div class="kksr-stars">

<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>

<div class="kksr-stars-active" style="width: 138px;">
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>


<div class="kksr-legend" style="font-size: 19.2px;">
            5/5 - (2 votes)    </div>
    </div>
Instructions

1. It is an OPEN BOOK and OPEN INTERNET examination.

4. Be sure to follow the upload instructions.

5. Total time for the examination is 2 hours 30 minutes.

6. This is an open-ended assignment. You are free to use any API from the following libraries to solve the problems: pytorch, numpy, scipy, matplotlib, time.

7. Note that you are not supposed to use sklearn

1. Set Retrieval Task In this question we will train a model for set retrieval, i.e. the model ranks the items in a corpus for a given query. To this end, we assume that each query and each corpus is a set of items. For example, a query can be the set of keywords you type in google search bar and corpus is the set of words in the webpage that google returns. Google presents us with a list of corpus in a ranked order. To simplify the problem, we will work with a synthetic dataset where corpus contains a list of 63 webpages. Each webpage can contain different number of words in it. For simplicity, we consider that each query contains a set of exactly 3 keywords in it. Further, we represent words using pre-trained embeddings ∈R5. Given a query q, the task is to assign score to the 63 corpus items such that the relevant corpus receive higher scores.

Dataset Description For this problem, we are given with a dataset consisting of the following: • List of training queries: We provide 50 training queries in the form of a list. Each query is a set of items of fixed length, where each item is represented by a feature vector in R5 • List of corpus: We provide 63 corpus in the form of a list. Each corpus is a set of items of variable length ∈ [6], where each item is represented by a feature vector in R5 • Training ground truth relevance labels: We provide binary relevance labels in the form of a tensor of shape (50,63). The entry (i,j) contains 1 if the jth corpus set is relevant the the ith query set, and 0 otherwise.

• List of test queries: We provide 10 test queries in the form of a list. Each query is a set of items of fixed length, where each item is represented by a feature vector in R5

Implementation Guidelines You can train any model of your choice. However, you have to adhere to the provided template which requires you to implement the following:

1.a function set_embed in class Model: You can implement any set embedding model that you want, as long as it meets the input and output shape criteria mentioned in the code.

1.b function ranking loss: Implement the following:

X X

ReLU[score(q,c✗) − score(q,c✓) + margin]

q∈queries c✓∈Corpus relevant to q, c✗∈Corpus irrelevant to q

1.c function mean_average_precision : Implement the mean average precision (mAP) score as described in the following link: [LINK]. You can read till the end of section 2 in the link. You should not use sklearn.

1.d score: Given the query set embedding q ∈Rd and corpus set embedding c ∈Rd, compute the following relevance score:

d

score(q,c) = −XReLU[(q − c)i]

i=1

Note that you will have to compute the pairwise scores between all available query and corpus embeddings. Make sure to implement a tensorized code.

1.e You will also need to add code for training your models, in the main function.

Evaluation We will be evaluating the following:

1.a /3

1.a correctness of ranking loss

1.b /2

1.b correctness of score

1.c /5

1.c correctness of mean_average_precision

1.d evaluation of test set predictions (with respect to hidden test ground truth): We will only refer to the uploaded output.pkl. We will use the uploaded model files to check the consistency between the predicted scores in output.pkl and the model predictions.

1.d /10

1 Submission instructions

Complete the functions in assignment.py. Do not modify the function signatures. Keep the file in a folder named &lt;ROLL_NUMBER&gt;_exam and compress it to a tar file named

&lt;ROLL_NUMBER&gt;_exam.tar.gz using the command

tar -zcvf &lt;ROLL_NUMBER&gt;_exam.tar.gz &lt;ROLL_NUMBER&gt;_exam

Submit the tar file on Moodle. The directory structure should be –

&lt;ROLL_NUMBER&gt;_exam | – – – – assignment.py | – – – – output.pkl | – – – – model.pkl

Replace ROLL_NUMBER with your own roll number. If your Roll number has alphabets, they should be in “small” letters.

Total: 20
