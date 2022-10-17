# Lifelog-PKBQAC2.0-Dataset

A Dataset for Personal Knowledge Base Question Ansewring and Unanswerable Question Correction

# Introduction
PKBQAC 2.0 is an extension of PKBQAC in which unanswered questions are confirmed to have only one correction.
The questions in PKBQAC 2.0 are constructed by consulting the personal knowledge base ([LiveKB](https://github.com/ntunlplab/Lifelog-LiveKB)) which consists of 137 relations and 15,525 events written in Chinese collected from Twitter 18 users.
To construct an experimental dataset for both correction and explanation, we removed those questions in the PKBQAC dataset with multiple corrections. 
We invited annotators to compose new unanswerable questions that have only one correction based on PKB.
We also added some answerable questions.
The resulting PKBQAC~2.0 contains 43,549 questions, of which 38,963 and 4,586 questions are answerable and unanswerable, respectively.
In other words, there are two types of answerable questions: (1) the answers can be retrieved from the KB, and (2) the questions can be answered with "True" or "False" based on the KB. The rest of the questions are unanswerable.

# Format
Each entry in the JSON format is consisted of "tweet_id" (the ids of the related tweets), "answerable" (is the question answerable), "question", "correct_questions" (the possible corrected questions of the unanswerable question), "question_type" (seven types of questions, including "who", "what", "where", "when", "how many", "duration", and "True or False"), and "split" (denotes the instance belongs to training, validation, or test sets).

"question" and "correct_questions" are consist of "question" and "triples", where triples in "triples" means which events comprise the question, and the answer is in "tripleA".

# Example
```yaml
{'answer': {'triple_idx': None, 'tweet_id': None},
  'answerable': False,
  'correct_question': {'answer': {'triple_idx': 0,
                                  'tweet_id': '63166644754710528'},
                       'question': '我租什么去北横经过外澳服务区伯朗咖啡',
                       'triples': {'tripleA': {'object': '单车',
                                               'predicate': '租',
                                               'subject': '我'},
                                   'tripleB': {'object': '外澳服务区伯朗咖啡',
                                               'predicate': '@',
                                               'subject': '我'},
                                   'tripleC': {'object': '北横',
                                               'predicate': '在',
                                               'subject': '我'}}},
  'question': {'question': '我租什么去北横经过学校的图书馆',
               'triples': {'tripleA': {'object': '单车',
                                       'predicate': '租',
                                       'subject': '我'},
                           'tripleB': {'object': '校图书馆',
                                       'predicate': '去',
                                       'subject': '我'},
                           'tripleC': {'object': '北横',
                                       'predicate': '在',
                                       'subject': '我'}}},
  'question_type': 'what',
  'split': 'train',
  'tweet_ids': ['65035030010925056',
                '64280754770812928',
                '64896955318403072',
                '64960662308265984',
                '64341700734226432',
                '64578159307264001',
                '64914000235855872',
                '64863620894433280',
                '64503447835250690',
                '64215735244816384',
                '63568196883578880',
                '64669311163314176',
                '64861298684469248',
                '64960662366994432',
                '64671200013594624',
                '64877696022347776',
                '65040228779425794',
                '64654201615163392',
                '64232645214740480',
                '64336905436807168',
                '64540594885767168',
                '63166644754710528',
                '63414743309877248']}
```
# Download
Please click [Google Form](https://forms.gle/U1hRx5biQMC7qaGRA) to fill out the questionnaire survey, the download link of the PKBQAC 2.0 dataset will be sent to your e-mail inbox.

Please feel free to contact me if you have any questions.

Email Address: azyen@nlg.csie.ntu.edu.tw

# How to Cite the Corpus
Please cite the following papers when referring to the PKBQAC 2.0 dataset in academic publications and papers.

An-Zi Yen, Hen-Hsen Huang and Hsin-Hsi Chen (2022). “Unanswerable Question Correction and Explanation over Personal Knowledge Base.” In Proceedings of the 31st ACM International Conference on Information and Knowledge Management (CIKM 2022), October 17-21, Hybrid Conference, Hosted in Atlanta, Georgia, USA.
