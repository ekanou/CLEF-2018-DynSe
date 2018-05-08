## Task 1: Query Suggestion

Given a verbose description of a task (topic) generate a sequence of queries and their corresponding rankings of the collection.

### Submission Guidelines:
For each topic you are allowed to submit 10 query suggestions. Each query should be accompanied by the top-10 results collected from the Indri index provided to you. Hence, in your submission file, for each topic there should be 100 lines.

### Submission Format
The lab will use TREC-style submissions. In TREC, a "run" is the output of a search system over ALL topics. Run Format:

TOPIC	QUESTION	DOCNO	RANK	SCORE	RUN

TOPIC is the topic id and can be found in the released topics
QUESTION is the suggested query of this round. The question should be included into quotes, e.g. "london hotels". Each suggested query should be repeated over a maximum of 10 rows
DOCNO is the document number in the corpus
RANK is the rank of the document returned for this given round (in increasing order)
SCORE is the score of the ranking/classification algorithm
RUN is an identifier/name for the system producing the run

Below is an example file on the training data. You need to create one such file for each algorithm/system for your test data.

dd17-51	"Katrina most costly hurricane"	1783276	10	ILPS-run1
dd17-51	"Katrina most costly hurricane"	1775816	9	ILPS-run1
dd17-51	"Katrina most costly hurricane"	1718269	8	ILPS-run1
dd17-51	"Katrina most costly hurricane"	1724162	7	ILPS-run1
dd17-51	"Katrina most costly hurricane"	1701311	6	ILPS-run1
dd17-51	"Katrina most costly hurricane"	1834929	5	ILPS-run1
dd17-51	"Katrina most costly hurricane"	1818307	4	ILPS-run1
dd17-51	"Katrina most costly hurricane"	1780634	3	ILPS-run1
dd17-51	"Katrina most costly hurricane"	1704548	2	ILPS-run1
dd17-51	"Katrina most costly hurricane"	1704526	1	ILPS-run1
dd17-51	"Hurricane Katrina's path of destruction"	1704322	10	ILPS-run1

...
...
...
...

dd17-60	"Tupac Amaru and Shining Path relationship"	0896459	1	ILPS-run1

You are allowed to submit as many runs as you wish. Just place all your runs for Task 1 in a folder named Task 1 and add it to the repository.

## Task 2: Results Composition

Given the ranking in Task 1 merge them in a single composite ranking.

### Submission Guidelines:

At the end of round 10, 100 search results will have been collected for each topic. These 100 results coming from 10 queries should be re-ranked in a single optimal ranking.

### Submission Format:
The lab will use TREC-style submissions. In TREC, a "run" is the output of a search system over ALL topics. Run Format:

TOPIC	DUMMY	DOCNO	RANK	SCORE	RUN

TOPIC is the topic id and can be found in the released topics
DUMMY is a dummy column to be filled in with 0.
DOCNO is the document number in the corpus
RANK is the rank of the document returned for this given round (in increasing order)
SCORE is the score of the ranking/classification algorithm
RUN is an identifier/name for the system producing the run

Below is an example file on the training data. You need to create one such file for each algorithm/system for your test data.

dd17-51	0	1783276	100	ILPS-run1
dd17-51	0	1704322	99	ILPS-run1
dd17-51	0	1718269	98	ILPS-run1
dd17-51	0	1724162	97	ILPS-run1
dd17-51	0	1704548	96	ILPS-run1
dd17-51	0	1834929	95	ILPS-run1
dd17-51	0	1818307	94	ILPS-run1
dd17-51	0	1780634	93	ILPS-run1
dd17-51	0	1701311	92	ILPS-run1
dd17-51	0	1704526	91	ILPS-run1
dd17-51	0	1775816	90	ILPS-run1

...
...
...
...

dd17-60	0	0896459	1	ILPS-run1

You are allowed to submit as many runs as you wish. Just place all your runs for Task 1 in a folder named Task 1 and add it to the repository.