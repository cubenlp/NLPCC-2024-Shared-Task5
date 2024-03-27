# **Argument Mining for Chinese Argumentative Essay**

## **Task Introduction**

Argumentative essay writing is an important way to promote the development and enhancement of students' higher-order thinking skills at the high school level, and is an important form of discursive expression. As Chinese national document for the teaching of language subjects, the *Language Curriculum Standards for General Senior Secondary Schools* (Revised in 2017 and 2020) explicitly states that senior secondary school students should "learn to express and explain their own views, and strive to make correct arguments, use accurate language, make appropriate arguments, and speak logically."[1]. High school students need to master effective argumentative essay writing methods, effectively improve the argumentative essay writing ability, but also expresses the need for teachers to provide more efficient guidance and effective training. By mining students' arguments in their argumentative essays, students are better able to verify the reliability of data, and identify reasonable reasoning processes to improve their logical expression skills. At the same time, teachers can assess the effectiveness of their teaching methods by analyzing the level of students' scientific argumentation, and adjust the course design and teaching methods according to the evaluation results to improve the quality of education.

With the continuous development of computer technology, many researchers and educational institutions have begun to use computer technology to provide smarter and more efficient support for language teaching. There are researchers who focus on identifying the main claim, claim and premise from the whole text [2]. There are also researchers who classify sentences into two categories based on whether they contain a thesis and conclusion statement [3\][4], and there are also researchers who categorize sentences, as well as paragraphs, into introduction, thesis, main idea, evidence, elaboration, and conclusion based on the function they play [5\][6]. But none of these works provide a detailed breakdown of the types of arguments. A detailed division of the types of arguments can reflect the logic of the argument as well as students’ accumulation of essay materials, which can help teachers to better understand and analyze the essay, as well as help students to improve their essay writing and argumentation skills.

The data for this task were derived from Chinese native-speaking high school students' argumentative essays, and the argumentative components appearing in high school students' argumentative essays were defined in terms of sentences. Based on the four coarse-grained argumentative components of assertion, evidence, elaboration, and others, the assertion was further subdivided into main claim, claim, and restate claim based on the content and location of the argument, and the evidence was further classified into fact, anecdote, quotation, proverb, and axiom, considering the source and type of the argument. The purpose of this review is to define more detailed components of argumentation to provide more references for argumentative essay comprehension and analysis.

### **Task Description**

Argument components identification for argumentative essays is important for the assessment of argumentative essays. This task takes the whole argumentative essay as an input unit and categorizes each sentence in it into 4 categories of assertion, evidence, elaboration, and others at a coarse-level. Considering the variety of argumentative techniques used in students' compositions, this task further categorized assertion into main claim, claim and restate claim, and further classify evidence into fact, anecdote, quotation, proverb and axiom as well. 

### **Task** **Definition**

This task can be regarded as a classification problem, in which an essay will be inputted and the model needs to predict the category of argumentative components to which each sentence belongs, as well as the fine-grained categorization under that category. This task defined 4 coarse-grained categories and 10 fine-grained categories as displayed in the Table below.

| Coarse-grained | Fine-grained  | Definition                                                   | Example                                                      |
| -------------- | ------------- | ------------------------------------------------------------ | ------------------------------------------------------------ |
| Assertion      | Main Claim    | The main idea or proposition of the entire document, indicating the author's point of view or claim | 当此之时，我们当如何抉择这些影响，如何决定自我判断？我以为，当构筑自我之思，以实践抉择之，检验之。 |
|                | Claim         | Secondary ideas around the main claim                        | 唯有前人经验不断地积累，方有如今科技之进步，文明之发展。     |
|                | Restate Claim | Restatement of the main claims or claims                     | 勇于探索，永于探索，以实践构建自我之思。                     |
| Evidence       | Fact          | Specific facts, historical facts or phenomena in society     | 恰如《诗经》《楚辞》开创我国悠长诗歌文脉，西方科学技术的发展也依托于牛顿，欧几里得等先贤的智慧结晶。 |
|                | Anecdote      | Examples that happened to the author                         | 我们最常做的，就是“向多数人学习”，别人做，我也做。           |
|                | Quotation     | Citing of the writings of famous people                      | 马克思曾以辩证唯物论告诉我们认识当从实践中来，也当经过实践检验，掷于实践中去。 |
|                | Proverb       | Idioms or phrases passed down among the masses               | 良言一句三冬暖，恶语伤人六月寒。                             |
|                | Axiom         | Recognized common sense or scientific laws                   | 因为人类对于事物的认识总是螺旋前进的。                       |
| Elaboration    | -             | Explanatory notes or analytical discussions of the assertion | 在认识事物时，我们常受外界因素来决定自己的判断。             |
| Others         | -             | Sentences that do not fall into the above categories         | 那么，如何抉择？                                             |

## **Dataset**

### **Example of dataset**

~~~json
{
    "essay_ID": 38,
    "title": "构筑自我之思",
    "doc": "在认识事物时，我们常受外界因素来决定自己的判断。当此之时，我们当如何抉择这些影响，如何决定自我判断？我以为，当构筑自我之思，以实践抉择之，检验之。...",
    "sents": [
        {
            "sentText": "在认识事物时，我们常受外界因素来决定自己的判断。",
            "fine_sent_type": "阐述",
            "coarse_sent_type": "论证"
        },
        {
            "sentText": "当此之时，我们当如何抉择这些影响，如何决定自我判断？我以为，当构筑自我之思，以实践抉择之，检验之。",
            "fine_sent_type": "中心论点",
            "coarse_sent_type": "论点"
        },
        ...
    ]
}
~~~

This shows an sample of data from the dataset used in this task, including the essay ID, title, document, and the coarse- and fine-grained categorization to which each sentence in the document belongs.

### **Distribution**

| Dataset    | Number of essays | Number of sentences |
| ---------- | ---------------- | ------------------- |
| Train      | 135              | 2777                |
| Test       | 20               | 428                 |
| Evaluation | 551              | 11750               |

## **Evaluation**

The total score for this task consists of two parts: a coarse-grained categorization score as well as a fine-grained categorization score, which is calculated as follows:

$Score=0.5×F_1^{Coarse}+0.5×F_1^{Fine}$

In which $F_1^{Coarse}$ is the F1 score for coarse-grained categories, while $F_1^{Fine}$ is the F1 score for the fine-grained ones.

## **Contacts**

chaos_yin@qq.com

 

## **References**

[1] Janda, Harneet & Pawar, Atish & Du, Shan & Mago, Vijay. (2019). Syntactic, Semantic and Sentiment Analysis: The Joint Effect on Automated Essay Evaluation. IEEE Access. PP. 1-1. 10.1109/ACCESS.2019.2933354. 

[2] Hao Wang, Zhen Huang, Yong Dou, and Yu Hong. 2020. Argumentation Mining on Essays at Multi Scales. In Proceedings of the 28th International Conference on Computational Linguistics, pages 5480–5493, Barcelona, Spain (Online). International Committee on Computational Linguistics.	

[3] Beata Beigman Klebanov, Binod Gyawali, and Yi Song. 2017. Detecting Good Arguments in a Non-Topic-Specific Way: An Oxymoron?. In Proceedings of the 55th Annual Meeting of the Association for Computational Linguistics (Volume 2: Short Papers), pages 244–249, Vancouver, Canada. Association for Computational Linguistics.	

[4] Wang, Xinyu et al. “Automated Evaluation for Student Argumentative Writing: A Survey.” ArXiv abs/2205.04083 (2022): n. pag.

[5] Wei Song, Ziyao Song, Lizhen Liu, and Ruiji Fu. 2021. Hierarchical multi-task learning for organization evaluation of argumentative student essays. In Proceedings of the Twenty-Ninth International Joint Conference on Artificial Intelligence (IJCAI'20). Article 536, 3875–3881.

[6] Yang, H.; He, Y.; Bu, X.; Xu, H.; Guo, W. Automatic Essay Evaluation Technologies in Chinese Writing—A Systematic Literature Review. Appl. Sci. 2023, 13, 10737. https://doi.org/10.3390/app131910737 