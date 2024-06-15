| Rank | Team name  | Score |
| ---- | ---------- | ----- |
| 1    | TeleAI     | 79.24 |
| 2    | TW-NLP     | 76.49 |
| 3    | NewFolder  | 72.71 |
| 4    | SIAT-NLP   | 72.48 |
| 5    | Prompt     | 71.22 |
| 6    | DUT-xlarge | 70.18 |
| 7    | qust_nlp   | 52.87 |
| 8    | baseline   | 44.61 |

calculated at 20:50 on 2024/6/15



1. $Score = 0.5*MicroF1^{coarse}+0.5*MicroF1^{fine}$

2. The submitted file should use the following format:

   ~~~json
   { 
       "essay_ID": 35,
       "title": "张驰有度",
       "sents": [
            {
                "sentText": "生活的节奏感时刻在变化。",
                "fine_sent_type": "阐述"
            },
            ...
        ]
   }  
   ~~~

   Files didn't match this format (specially the keys) won't be considered.

3. It is recommended to submit your result before 20:00, since the evaluation script will only run once everyday between 20:00 and 22:00.

4. We will use the latest submission to calculate.
