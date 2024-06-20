| Rank | Team name         | Score |
| ---- | ----------------- | ----- |
| 1    | TeleAI            | 79.36 |
| 2    | BlueSpace         | 76.49 |
| 2    | TW-NLP            | 76.49 |
| 4    | ZZU_NLP Alchemist | 75.11 |
| 5    | NewFolder         | 74.54 |
| 6    | SIAT-NLP          | 74.43 |
| 7    | GG Bond Forever   | 74.31 |
| 8    | ouchnai           | 73.74 |
| 9    | freedom           | 73.28 |
| 10   | Prompt            | 72.36 |
| 11   | qust_nlp          | 70.18 |
| 12   | DUT-xlarge        | 68.69 |
| 13   | Su                | 64.68 |
| 14   | Bjs_ignore_team   | 62.16 |
| 15   | baseline          | 44.61 |

calculated at 20:40 on 2024/6/20



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
