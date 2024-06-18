| Rank | Team name         | Score |
| ---- | ----------------- | ----- |
| 1    | TeleAI            | 79.36 |
| 2    | ZZU_NLP Alchemist | 76.72 |
| 3    | BlueSpace         | 75.92 |
| 4    | TW-NLP            | 75.69 |
| 5    | SIAT-NLP          | 75.11 |
| 6    | NewFolder         | 74.43 |
| 7    | freedom           | 72.25 |
| 8    | DUT-xlarge        | 70.18 |
| 9    | Prompt            | 69.15 |
| 10   | baseline          | 44.61 |
| 11   | Bjs_ignore_team   | 39.33 |
| 12   | qust_nlp          | 29.59 |

calculated at 20:38 on 2024/6/18



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

3. It is recommended to submit your result before 20:00, since the evaluation script will only run once everyday between 20:00 and 22:00. The evaluation process will end on 2024/6/20 (a final update will be conducted this day), so make sure you submitted the result before 2024/6/20 20:00.

4. We will use the latest submission to calculate.
