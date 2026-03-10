## SEG301
### Obsidian Chapter 1: Introduction

1. **Question 1: What is the primary focus of Information Retrieval (IR)?**
    
    - [ ] A. Managing relational databases efficiently.
        
    - [x] B. Representing, searching, and manipulating large collections of human-language data.
        
    - [ ] C. Developing new image compression algorithms.
        
    - [ ] D. Optimizing network protocols for data transfer.
        
2. **Question 2: Which of the following is NOT typically considered an IR application?**
    
    - [ ] A. Web search engines
        
    - [ ] B. Digital libraries
        
    - [x] C. Real-time operating system scheduling
        
    - [ ] D. Desktop search systems
        
3. **Question 3: What is the initial trigger for a user initiating a search in an IR system?**
    
    - [ ] A. An inverted index
        
    - [ ] B. A query
        
    - [x] C. An information need
        
    - [ ] D. A document collection
        
4. **Question 4: In IR terminology, what is the core data structure mapping terms to their locations in a collection?**
    
    - [ ] A. B-Tree
        
    - [ ] B. Hash Table
        
    - [ ] C. Relational Database
        
    - [x] D. Inverted Index
        
5. **Question 5: What does RSV stand for in the context of ranking?**
    
    - [ ] A. Relevant Score Value
        
    - [x] B. Retrieval Status Value
        
    - [ ] C. Ranked Selection Value
        
    - [ ] D. Retrieval System Validity
        
6. **Question 6: What is the primary difference between "effectiveness" and "efficiency" in IR evaluation?**
    
    - [ ] A. Effectiveness measures speed, efficiency measures result quality.
        
    - [x] B. Effectiveness measures result quality, efficiency measures resource usage (speed/space).
        
    - [ ] C. Effectiveness measures storage space, efficiency measures relevance.
        
    - [ ] D. Effectiveness measures user satisfaction, efficiency measures algorithm complexity.
        
7. **Question 7: The Probability Ranking Principle (PRP) states that optimal effectiveness is achieved by ranking documents in decreasing order of their...?**
    
    - [ ] A. Size
        
    - [x] B. Probability of relevance
        
    - [ ] C. Number of query terms contained
        
    - [ ] D. Date of publication
        
8. **Question 8: Which text format is fundamental for Web pages and includes inherent support for hyperlinks?**
    
    - [ ] A. PDF
        
    - [ ] B. XML
        
    - [x] C. HTML
        
    - [ ] D. RTF
        
9. **Question 9: What is the process of converting a document's text into a sequence of discrete units for indexing?**
    
    - [ ] A. Compression
        
    - [x] B. Tokenization
        
    - [ ] C. Encryption
        
    - [ ] D. Normalization
        
10. **Question 10: What law describes the relationship where a few terms occur very frequently, while most terms occur rarely?**
    
    - [ ] A. Moore's Law
        
    - [x] B. Zipf's Law
        
    - [ ] C. Bayes' Theorem
        
    - [ ] D. Little's Law
        
11. **Question 11: A simple language model (like MLE) estimates the probability of a term based on its...?**
    
    - [ ] A. Inverse document frequency in the collection.
        
    - [x] B. Frequency within a specific document.
        
    - [ ] C. Position within the document.
        
    - [ ] D. Semantic relationship to other terms.
        
12. **Question 12: What technique is used in language modeling to assign non-zero probabilities to terms not seen in the training text?**
    
    - [ ] A. Stemming
        
    - [ ] B. Stopping
        
    - [x] C. Smoothing
        
    - [ ] D. Indexing
        
13. **Question 13: What is a collection of documents, topics, and relevance judgments used for evaluation called?**
    
    - [ ] A. A corpus
        
    - [ ] B. An inverted index
        
    - [x] C. A test collection
        
    - [ ] D. A language model
        
14. **Question 14: What annual conference organized by NIST has been central to IR evaluation?**
    
    - [ ] A. SIGIR
        
    - [ ] B. WWW
        
    - [x] C. TREC
        
    - [ ] D. CIKM
        
15. **Question 15: What type of search task involves finding relevant documents from a static collection for new, previously unseen queries?**
    
    - [ ] A. Routing
        
    - [ ] B. Filtering
        
    - [x] C. Ad hoc retrieval
        
    - [ ] D. Clustering
        
16. **Question 16: Which open-source IR system is known for being implemented in Java and widely used (e.g., by Wikipedia)?**
    
    - [ ] A. Indri
        
    - [ ] B. Wumpus
        
    - [x] C. Lucene
        
    - [ ] D. Terrier
        
17. **Question 17: What structural feature of XML allows it to serve as a metalanguage for defining document formats?**
    
    - [ ] A. Hyperlinks
        
    - [ ] B. Fixed-length records
        
    - [x] C. Tagging and nesting of elements
        
    - [ ] D. Lack of a schema
        
18. **Question 18: What is the purpose of smoothing in language modeling?**
    
    - [x] A. To handle out-of-vocabulary words or unseen events.
        
    - [ ] B. To speed up the calculation of probabilities.
        
    - [ ] C. To reduce the size of the vocabulary.
        
    - [ ] D. To ensure all probabilities are integers.
        
19. **Question 19: What does a Markov model represent in the context of language modeling?**
    
    - [ ] A. The hierarchical structure of a document.
        
    - [x] B. Probabilities of transitions between states (representing context).
        
    - [ ] C. The frequency distribution of all terms.
        
    - [ ] D. The relevance of terms to a specific topic.
        
20. **Question 20: Text clustering and categorization both group documents, but categorization requires...?**
    
    - [ ] A. Documents to be in XML format.
        
    - [x] B. Pre-defined categories illustrated by training data.
        
    - [ ] C. Documents to be sorted chronologically.
        
    - [ ] D. The use of an inverted index.
        

### Chapter 2: Basic Techniques

21. **Question 1: What are the two principal components of an inverted index?**
    
    - [ ] A. Query log and document map
        
    - [x] B. Dictionary and postings lists
        
    - [ ] C. Stemmer and stop list
        
    - [ ] D. Cache and relevance judgments
        
22. **Question 2: In a schema-independent index, what does a posting typically represent?**
    
    - [ ] A. A document identifier (docid).
        
    - [ ] B. A term frequency within a document.
        
    - [x] C. A specific token position within the entire collection.
        
    - [ ] D. A relevance score.
        
23. **Question 3: Which abstract data type (ADT) method for an inverted index returns the first position of a term** _**after**_ **a given current position?**
    
    - [ ] A. first(t)
        
    - [ ] B. last(t)
        
    - [x] C. next(t, current)
        
    - [ ] D. prev(t, current)
        
24. **Question 4: What is the primary purpose of the phrase search algorithm discussed?**
    
    - [ ] A. To rank documents based on term frequency.
        
    - [x] B. To find all occurrences of an exact sequence of terms.
        
    - [ ] C. To handle Boolean NOT operators efficiently.
        
    - [ ] D. To compress the inverted index.
        
25. **Question 5: What technique involves performing a binary search on an array representation of a postings list?**
    
    - [ ] A. Galloping search
        
    - [ ] B. Sequential scan
        
    - [x] C. Standard binary search implementation of next/prev.
        
    - [ ] D. Hashing
        
26. **Question 6: What is galloping search designed to optimize in postings list traversal?**
    
    - [ ] A. Handling very short postings lists.
        
    - [ ] B. Reducing disk I/O for very long lists compared to pure binary search.
        
    - [x] C. Skipping over large portions of a list efficiently when jumps are large.
        
    - [ ] D. Compressing the postings list data.
        
27. **Question 7: What information is typically stored in a positional index posting beyond docid and term frequency?**
    
    - [ ] A. The relevance score of the document.
        
    - [x] B. The specific positions of the term within the document.
        
    - [ ] C. The language of the document.
        
    - [ ] D. Pointers to related terms.
        
28. **Question 8: The vector space model represents documents and queries as:**
    
    - [ ] A. Finite state automata
        
    - [ ] B. Strings of characters
        
    - [x] C. Vectors in a high-dimensional space
        
    - [ ] D. Probability distributions
        
29. **Question 9: In the basic vector space model, how is the similarity between a document and a query typically measured?**
    
    - [ ] A. By the number of overlapping terms.
        
    - [ ] B. By the Euclidean distance between their vectors.
        
    - [x] C. By the cosine of the angle between their vectors.
        
    - [ ] D. By the difference in their lengths.
        
30. **Question 10: What does TF-IDF stand for?**
    
    - [x] A. Term Frequency - Inverse Document Frequency
        
    - [ ] B. True Frequency - Index Document Frequency
        
    - [ ] C. Term Factor - Inverse Data Factor
        
    - [ ] D. Total Frequency - Indexed Data Format
        
31. **Question 11: What is the intuition behind the IDF component of TF-IDF weighting?**
    
    - [ ] A. Terms appearing frequently in a document are more important.
        
    - [x] B. Terms appearing in many documents are less informative for distinguishing documents.
        
    - [ ] C. Longer documents should be penalized.
        
    - [ ] D. The first occurrence of a term is the most important.
        
32. **Question 12: Proximity ranking primarily scores documents based on:**
    
    - [ ] A. The frequency of query terms.
        
    - [x] B. The closeness of query terms to each other within the document.
        
    - [ ] C. The document's length relative to the average.
        
    - [ ] D. The static rank of the document.
        
33. **Question 13: A "cover" in proximity ranking is defined as:**
    
    - [ ] A. The set of all documents containing at least one query term.
        
    - [x] B. An interval containing query terms that doesn't contain a smaller interval also containing them.
        
    - [ ] C. The first paragraph of a document.
        
    - [ ] D. The metadata associated with a document.
        
34. **Question 14: Standard Boolean retrieval operators include:**
    
    - [ ] A. NEAR, ADJ, WITH
        
    - [ ] B. TF, IDF, BM25
        
    - [x] C. AND, OR, NOT
        
    - [ ] D. MAP, P@k, MRR
        
35. **Question 15: What is the typical output of a Boolean retrieval query?**
    
    - [ ] A. A ranked list of documents.
        
    - [ ] B. A single relevance score.
        
    - [x] C. A set of documents satisfying the Boolean predicate.
        
    - [ ] D. A probability distribution over terms.
        
36. **Question 16: What does "Recall" measure in IR evaluation?**
    
    - [ ] A. The fraction of retrieved documents that are relevant.
        
    - [x] B. The fraction of relevant documents that are retrieved.
        
    - [ ] C. The time taken to retrieve documents.
        
    - [ ] D. The storage space used by the index.
        
37. **Question 17: What does "Precision" measure in IR evaluation?**
    
    - [x] A. The fraction of retrieved documents that are relevant.
        
    - [ ] B. The fraction of relevant documents that are retrieved.
        
    - [ ] C. The speed of the ranking algorithm.
        
    - [ ] D. The accuracy of term frequency counts.
        
38. **Question 18: What does P@10 measure?**
    
    - [ ] A. The average precision across the top 10 documents.
        
    - [ ] B. The recall achieved within the top 10 documents.
        
    - [x] C. The precision within the top 10 retrieved documents.
        
    - [ ] D. The time taken to retrieve the top 10 documents.
        
39. **Question 19: Mean Average Precision (MAP) provides a single-figure measure of quality across:**
    
    - [ ] A. Different query lengths.
        
    - [ ] B. Different numbers of users.
        
    - [ ] C. Different storage devices.
        
    - [x] D. Various recall levels.
        
40. **Question 20: The TREC evaluation methodology often uses "pooling" to:**
    
    - [ ] A. Increase the size of the document collection.
        
    - [x] B. Reduce the number of documents that need relevance judgments.
        
    - [ ] C. Automatically generate queries from topics.
        
    - [ ] D. Combine results from multiple search engines.
        

### Chapter 3: Tokens and Terms

41. **Question 1: What is the primary goal of tokenization?**
    
    - [ ] A. To compress the text documents.
        
    - [x] B. To divide documents into a sequence of units (tokens) for indexing.
        
    - [ ] C. To check the spelling of words.
        
    - [ ] D. To determine the language of a document.
        
42. **Question 2: Handling punctuation like apostrophes in English (e.g., "it's", "Bill's") presents a challenge for tokenization because:**
    
    - [ ] A. Apostrophes are not valid ASCII characters.
        
    - [x] B. The desired tokenization (e.g., "it is" vs. "Bill") depends on the word's function.
        
    - [ ] C. All punctuation must be simply discarded.
        
    - [ ] D. Apostrophes indicate the start of a new sentence.
        
43. **Question 3: Case normalization (converting to lowercase) is common but can cause problems by conflating:**
    
    - [ ] A. Verbs and nouns.
        
    - [ ] B. Short words and long words.
        
    - [x] C. Acronyms (like "US") with common words (like "us").
        
    - [ ] D. Singular and plural forms.
        
44. **Question 4: What is the purpose of stemming?**
    
    - [ ] A. To remove common words like "the" and "a".
        
    - [x] B. To reduce words to a common root form to match variations (e.g., "running", "runs" -> "run").
        
    - [ ] C. To correct spelling errors in queries.
        
    - [ ] D. To handle punctuation correctly.
        
45. **Question 5: A potential downside of aggressive stemming (like the Porter stemmer) is:**
    
    - [ ] A. It significantly increases index size.
        
    - [ ] B. It fails to handle plural forms.
        
    - [x] C. It can incorrectly conflate unrelated words (e.g., "university" and "universe" might stem similarly).
        
    - [ ] D. It only works for capitalized words.
        
46. **Question 6: What is the goal of stopping (stop word removal)?**
    
    - [ ] A. To reduce words to their root form.
        
    - [ ] B. To handle punctuation marks.
        
    - [x] C. To remove very common words (like "the", "a", "is") assumed to have little retrieval value.
        
    - [ ] D. To increase the number of tokens per document.
        
47. **Question 7: Why might removing stopwords be problematic for certain queries?**
    
    - [ ] A. Stopwords increase index size significantly.
        
    - [x] B. Stopwords are essential for phrase queries like "to be or not to be".
        
    - [ ] C. Stopwords are difficult to identify automatically.
        
    - [ ] D. Stopwords cause stemming algorithms to fail.
        
48. **Question 8: Which character encoding standard supports a vast range of characters from most living languages and is backward compatible with ASCII?**
    
    - [ ] A. EBCDIC
        
    - [ ] B. ISO-8859-1
        
    - [x] C. UTF-8 (Unicode)
        
    - [ ] D. KOI8-R
        
49. **Question 9: In UTF-8, how is the length of a multi-byte character sequence typically indicated?**
    
    - [ ] A. By a separate length field stored before the character.
        
    - [ ] B. By the value of the last byte in the sequence.
        
    - [x] C. By the pattern of high-order bits in the first byte.
        
    - [ ] D. It is always a fixed length of 4 bytes.
        
50. **Question 10: What is character n-gram indexing?**
    
    - [ ] A. Indexing only the first n characters of each word.
        
    - [x] B. Indexing overlapping sequences of n characters as tokens.
        
    - [ ] C. Indexing sequences of n words (word n-grams).
        
    - [ ] D. Indexing only words that contain the character 'n'.
        
51. **Question 11: An advantage of character n-gram indexing is that it:**
    
    - [x] A. Requires no stemming or complex tokenization rules.
        
    - [ ] B. Significantly reduces the size of the index compared to word indexing.
        
    - [ ] C. Is very fast during query processing.
        
    - [ ] D. Perfectly handles phrase queries.
        
52. **Question 12: A disadvantage of character n-gram indexing compared to word-based indexing is:**
    
    - [ ] A. It cannot handle non-English languages.
        
    - [x] B. It typically increases index size and query processing time.
        
    - [ ] C. It requires manual definition of n-grams.
        
    - [ ] D. It cannot handle punctuation.
        
53. **Question 13: What is a common tokenization challenge in many European languages not typically found in English?**
    
    - [ ] A. Lack of whitespace between words.
        
    - [ ] B. Use of very large character sets (thousands of characters).
        
    - [x] C. Presence of essential diacritical marks (accents).
        
    - [ ] D. Writing direction (right-to-left).
        
54. **Question 14: How might an IR system handle missing or inconsistently used diacritics?**
    
    - [ ] A. Refuse to index documents with diacritics.
        
    - [ ] B. Treat words with and without diacritics as completely different terms.
        
    - [x] C. Normalize text by removing diacritics, or use methods to match variations.
        
    - [ ] D. Require users to always type queries with correct diacritics.
        
55. **Question 15: What phenomenon in Germanic languages involves writing compound concepts (like "bicycle wheel") as single words?**
    
    - [ ] A. Stemming
        
    - [ ] B. Diacritics
        
    - [x] C. Compound nouns
        
    - [ ] D. Case normalization
        
56. **Question 16: What is "segmentation" in the context of CJK languages?**
    
    - [ ] A. Breaking text into sentences.
        
    - [x] B. Identifying the correct word boundaries in text written without spaces.
        
    - [ ] C. Removing punctuation marks.
        
    - [ ] D. Converting characters to a standard encoding.
        
57. **Question 17: Why is word segmentation particularly challenging in languages like Chinese?**
    
    - [ ] A. Chinese uses multiple scripts simultaneously.
        
    - [x] B. A character can form a word with characters both before and after it, depending on context.
        
    - [ ] C. Chinese has no function words.
        
    - [ ] D. All Chinese words are single characters.
        
58. **Question 18: What is Pinyin?**
    
    - [ ] A. A standard system for segmenting Chinese words.
        
    - [ ] B. A character encoding for Japanese.
        
    - [x] C. A standard system for transliterating Chinese characters into the Roman alphabet.
        
    - [ ] D. A type of stemming algorithm for Korean.
        
59. **Question 19: What ambiguity arises when using Pinyin (especially without tone marks) for queries?**
    
    - [x] A. Multiple Chinese characters can map to the same Pinyin syllable.
        
    - [ ] B. Pinyin cannot represent all Chinese sounds.
        
    - [ ] C. Pinyin uses characters not found on standard keyboards.
        
    - [ ] D. Pinyin requires whitespace segmentation.
        
60. **Question 20: According to Table 3.3, which tokenization method often performs best for several European languages?**
    
    - [ ] A. Unstemmed words
        
    - [ ] B. Snowball stemmer
        
    - [x] C. Character 5-grams
        
    - [ ] D. Removing all stopwords
        

### Chapter 4: Static Inverted Indices

61. **Question 1: In the context of this chapter, what does a "static" text collection mean?**
    
    - [ ] A. The collection is stored entirely in static RAM (SRAM).
        
    - [x] B. The collection does not change after the index is built.
        
    - [ ] C. All documents in the collection have the same size.
        
    - [ ] D. The collection only contains HTML documents.
        
62. **Question 2: What is the primary reason for not always keeping the entire inverted index in main memory?**
    
    - [ ] A. RAM is slower than disk for sequential access.
        
    - [ ] B. Index compression works better on disk.
        
    - [x] C. The index size can exceed available RAM, especially for large collections.
        
    - [ ] D. Dictionaries cannot be stored in RAM.
        
63. **Question 3: What are the two main components of an inverted index structure discussed?**
    
    - [ ] A. Document map and query cache
        
    - [x] B. Dictionary and postings lists
        
    - [ ] C. Stemmer and stop list
        
    - [ ] D. Forward index and backward index
        
64. **Question 4: What is the primary function of the dictionary component at query time?**
    
    - [ ] A. To store the actual text of the documents.
        
    - [ ] B. To compress the postings lists.
        
    - [x] C. To map query terms to the locations of their postings lists.
        
    - [ ] D. To store relevance scores for documents.
        
65. **Question 5: Which data structure for the dictionary typically offers faster single-term lookups?**
    
    - [ ] A. Sorted array (with binary search)
        
    - [ ] B. B-Tree
        
    - [x] C. Hash table
        
    - [ ] D. Linked list
        
66. **Question 6: What is a disadvantage of a hash-based dictionary compared to a sort-based one?**
    
    - [ ] A. It uses significantly more memory.
        
    - [ ] B. It is much slower for single-term lookups.
        
    - [x] C. It does not efficiently support prefix queries (e.g., "inform*").
        
    - [ ] D. It cannot handle collisions.
        
67. **Question 7: What is the "dictionary-as-a-string" approach designed to reduce?**
    
    - [ ] A. The number of postings lists.
        
    - [ ] B. The time required for prefix queries.
        
    - [x] C. Memory usage by eliminating internal fragmentation from fixed-size term storage.
        
    - [ ] D. The need for postings list compression.
        
68. **Question 8: In large collections like GOV2, what percentage of the total (uncompressed) index size does the dictionary typically represent?**
    
    - [ ] A. Around 50%
        
    - [ ] B. Around 25%
        
    - [x] C. Less than 10%
        
    - [ ] D. More than 75%
        
69. **Question 9: What is the purpose of storing postings lists for terms in lexicographical order on disk?**
    
    - [ ] A. To make compression easier.
        
    - [x] B. To support efficient prefix query processing.
        
    - [ ] C. To reduce the size of the dictionary.
        
    - [ ] D. To allow random updates to the lists.
        
70. **Question 10: What is the primary challenge when performing random access (like binary search) directly on postings lists stored on disk?**
    
    - [ ] A. Disk storage capacity is limited.
        
    - [x] B. Disk seek operations are very slow compared to sequential reads.
        
    - [ ] C. Postings lists on disk cannot be compressed.
        
    - [ ] D. The dictionary cannot point to disk locations.
        
71. **Question 11: What is a "per-term index" or "self-indexing" structure used for?**
    
    - [ ] A. To store the dictionary terms themselves.
        
    - [x] B. To provide efficient random access into long, on-disk postings lists.
        
    - [ ] C. To compress the dictionary.
        
    - [ ] D. To handle dynamic updates.
        
72. **Question 12: The entries stored in a per-term index to facilitate random access are called:**
    
    - [ ] A. Anchor points
        
    - [ ] B. Stop points
        
    - [x] C. Synchronization points
        
    - [ ] D. Merge points
        
73. **Question 13: What is dictionary interleaving?**
    
    - [ ] A. Storing the entire dictionary within the postings lists.
        
    - [x] B. Storing dictionary entries on disk immediately before their corresponding postings lists, with a smaller in-memory dictionary pointing to blocks.
        
    - [ ] C. Using multiple hash functions for the dictionary.
        
    - [ ] D. Compressing dictionary terms using Huffman coding.
        
74. **Question 14: Combining dictionary interleaving and grouping/compression techniques can reduce the in-memory dictionary size for large collections to:**
    
    - [ ] A. Roughly 50% of its original size.
        
    - [ ] B. Roughly 25% of its original size.
        
    - [ ] C. Roughly 10% of its original size.
        
    - [x] D. Less than 1-3% of its original size (potentially under 1MB).
        
75. **Question 15: What is the core operation involved in sort-based index construction?**
    
    - [ ] A. Hashing each term to find its postings list.
        
    - [x] B. Reordering (term, position) tuples from document order to term order.
        
    - [ ] C. Compressing postings lists using γ codes.
        
    - [ ] D. Merging multiple dictionaries.
        
76. **Question 16: What is a major limitation of simple sort-based index construction regarding disk space?**
    
    - [ ] A. It requires very little temporary disk space.
        
    - [x] B. It requires temporary disk space potentially larger than the original collection size.
        
    - [ ] C. It cannot write temporary data to disk.
        
    - [ ] D. It only works if the entire index fits in RAM.
        
77. **Question 17: What is merge-based index construction?**
    
    - [ ] A. Building the entire index in memory, then sorting it.
        
    - [ ] B. Repeatedly sorting small chunks of (term, position) tuples on disk.
        
    - [x] C. Building multiple independent index partitions (sub-indices) and then merging them.
        
    - [ ] D. Using a B-tree structure for the entire index.
        
78. **Question 18: What is a key advantage of merge-based index construction over sort-based?**
    
    - [ ] A. It requires significantly less CPU time.
        
    - [ ] B. It does not require disk storage.
        
    - [x] C. It does not require a complete in-memory dictionary or globally unique term IDs during partitioning.
        
    - [ ] D. It produces a pre-compressed index automatically.
        
79. **Question 19: In merge-based indexing, why does performance degrade if the available RAM for merging partitions becomes too small?**
    
    - [ ] A. The dictionary lookups become slower.
        
    - [ ] B. The individual partitions become too large.
        
    - [x] C. Insufficient read-ahead buffer size for each partition leads to excessive disk seeking during the merge phase.
        
    - [ ] D. Compression cannot be applied effectively.
        
80. **Question 20: Which data structure is often used for the dictionary during** _**in-memory**_ **index construction for optimal performance?**
    
    - [ ] A. A sorted array
        
    - [ ] B. A B-tree
        
    - [x] C. A hash table with move-to-front or insert-at-back heuristic
        
    - [ ] D. A skip list
        

### Chapter 5: Query Processing

81. **Question 1: What are the two main paradigms for processing ranked retrieval queries discussed?**
    
    - [ ] A. Hashing and Sorting
        
    - [ ] B. Compressing and Decompressing
        
    - [x] C. Document-at-a-time and Term-at-a-time
        
    - [ ] D. Indexing and Searching
        
82. **Question 2: In document-at-a-time processing, how are documents typically processed?**
    
    - [ ] A. All postings for one term are processed, then the next term, etc.
        
    - [x] B. Documents are processed one by one, accumulating scores from all relevant query terms.
        
    - [ ] C. Only documents containing all query terms are considered.
        
    - [ ] D. Documents are processed in random order.
        
83. **Question 3: What data structure is commonly used in efficient document-at-a-time processing to manage the next document candidates from each query term's postings list?**
    
    - [ ] A. A stack
        
    - [ ] B. A queue
        
    - [ ] C. A hash table
        
    - [x] D. A min-heap
        
84. **Question 4: What is the primary benefit of using a heap in document-at-a-time processing?**
    
    - [ ] A. It allows efficient compression of scores.
        
    - [x] B. It efficiently identifies the next document ID to process across all query term lists.
        
    - [ ] C. It stores the final ranked list of documents.
        
    - [ ] D. It helps in handling prefix queries.
        
85. **Question 5: What is the MaxScore optimization used for?**
    
    - [ ] A. To pre-calculate document scores during indexing.
        
    - [x] B. To estimate the maximum possible score contribution of remaining terms for a document.
        
    - [ ] C. To prune low IDF terms from the query.
        
    - [ ] D. To dynamically adjust the number of results (k) returned.
        
86. **Question 6: How does MaxScore improve query processing efficiency?**
    
    - [ ] A. By compressing the postings lists more effectively.
        
    - [x] B. By allowing the algorithm to potentially skip processing postings for documents that cannot possibly make it into the top-k results.
        
    - [ ] C. By using a faster sorting algorithm for the final results.
        
    - [ ] D. By caching frequently computed scores.
        
87. **Question 7: In term-at-a-time processing, what data structure is typically used to store intermediate document scores?**
    
    - [ ] A. A heap
        
    - [ ] B. A postings list
        
    - [x] C. Accumulators (often an array or hash map)
        
    - [ ] D. The dictionary
        
88. **Question 8: What is accumulator pruning designed to address in term-at-a-time processing?**
    
    - [x] A. The potential for the set of accumulators to become too large to fit in memory.
        
    - [ ] B. Inaccurate score calculations.
        
    - [ ] C. Slow processing of short postings lists.
        
    - [ ] D. Difficulties with Boolean operators.
        
89. **Question 9: How does processing query terms in order of increasing frequency (shortest postings list first) help in** _**unpruned**_ **term-at-a-time processing?**
    
    - [ ] A. It ensures higher precision in the results.
        
    - [x] B. It minimizes the number of accumulators that need to be copied/updated in intermediate steps.
        
    - [ ] C. It allows for better compression.
        
    - [ ] D. It simplifies handling document length normalization.
        
90. **Question 10: What does "impact ordering" refer to?**
    
    - [ ] A. Sorting documents by their final relevance score.
        
    - [x] B. Sorting postings within a list based on their potential score contribution (impact).
        
    - [ ] C. Ordering query terms by their IDF values.
        
    - [ ] D. Processing queries based on their estimated response time.
        
91. **Question 11: What is a major challenge when implementing impact ordering naively?**
    
    - [ ] A. It significantly increases index size.
        
    - [x] B. Standard index access methods (like `next`) can lose their logarithmic complexity.
        
    - [ ] C. It prevents the use of TF-IDF scoring.
        
    - [ ] D. It requires a full pass over the collection for each query.
        
92. **Question 12: Static index pruning involves:**
    
    - [ ] A. Removing entire documents from the index before construction.
        
    - [x] B. Removing low-impact postings from the index _during or after_ construction.
        
    - [ ] C. Removing query terms that have low IDF.
        
    - [ ] D. Using a smaller data type to store postings.
        
93. **Question 13: What is a potential drawback of static index pruning?**
    
    - [ ] A. It always increases query processing time.
        
    - [ ] B. It makes index construction much more complex.
        
    - [x] C. It may lead to incorrect top-k results compared to an unpruned index.
        
    - [ ] D. It prevents the use of compression.
        
94. **Question 14: The Ntoulas and Cho (2007) method allows checking if results from a pruned index are guaranteed to be correct by:**
    
    - [ ] A. Rerunning the query on a full index.
        
    - [x] B. Using score upper bounds derived from pruning thresholds for missing postings.
        
    - [ ] C. Comparing the pruned index size to the original size.
        
    - [ ] D. Analyzing the query terms for ambiguity.
        
95. **Question 15: What is a region algebra used for in IR?**
    
    - [ ] A. Performing algebraic operations on relevance scores.
        
    - [x] B. Defining and manipulating sets of text intervals (regions) to handle lightweight structure.
        
    - [ ] C. Optimizing matrix multiplications for PageRank.
        
    - [ ] D. Compressing query logs.
        
96. **Question 16: What is a Generalized Concordance List (GC-list)?**
    
    - [ ] A. A list of all terms sorted alphabetically.
        
    - [ ] B. A list where each posting includes document context.
        
    - [x] C. A set of text intervals [u, v] where no interval is nested within another.
        
    - [ ] D. A log of user queries and clicks.
        
97. **Question 17: Which region algebra operator is analogous to concatenation or sequence?**
    
    - [ ] A. Containing (>)
        
    - [ ] B. Both Of (^)
        
    - [x] C. Before (...)
        
    - [ ] D. Contained In (<)
        
98. **Question 18: The implementation of the region algebra operators often relies on methods similar to:**
    
    - [ ] A. Huffman coding
        
    - [ ] B. Term-at-a-time processing with accumulators
        
    - [ ] C. PageRank iteration
        
    - [x] D. The next/prev methods of the inverted index ADT applied to GC-lists
        
99. **Question 19: Which query processing strategy typically relies on merging postings lists?**
    
    - [ ] A. Document-at-a-time
        
    - [ ] B. Term-at-a-time
        
    - [ ] C. Boolean AND processing
        
    - [x] D. Both A and C
        
100. **Question 20: What is a primary motivation for using term-at-a-time processing, especially with on-disk indices?** 
- [ ] A. It is conceptually simpler than document-at-a-time. 

- [x] B. It avoids potentially costly random disk seeks by processing lists sequentially. 

- [ ] C. It naturally handles proximity ranking. 

- [ ] D. It requires less memory for the dictionary.
    
### Chapter 6: Index Compression

101. **Question 1: What are the two primary reasons for using index compression?** 
- [ ] A. To increase retrieval effectiveness and support phrase queries. 

- [x] B. To reduce storage requirements and potentially improve query performance (by reducing I/O). 

- [ ] C. To handle dynamic updates and ensure fault tolerance. 

- [ ] D. To encrypt the index and prevent unauthorized access.
    
102. **Question 2: Lossless compression ensures that:** 
- [ ] A. The compressed data is always smaller than the original. 

- [x] B. The decoder can reconstruct an exact copy of the original data. 

- [ ] C. Compression ratios are always better than 50%. 

- [ ] D. Only text data can be compressed.
    
103. **Question 3: Symbolwise data compression typically works in which two phases?** - [ ] A. Indexing and Searching - [ ] B. Encoding and Decoding - [x] C. Modeling and Coding - [ ] D. Static and Dynamic
    
104. **Question 4: Huffman coding achieves compression by:** - [x] A. Assigning shorter codewords to more frequent symbols. - [ ] B. Removing redundant symbols from the data. - [ ] C. Using a fixed-length code for all symbols. - [ ] D. Representing sequences as intervals on the [0, 1) line.
    
105. **Question 5: Arithmetic coding can sometimes achieve better compression than Huffman coding because:** - [ ] A. It uses a simpler algorithm. - [x] B. It can effectively assign fractional bits to symbols. - [ ] C. It does not require a model of the data. - [ ] D. It is inherently faster to decode.
    
106. **Question 6: When compressing postings lists (sequences of integers), what transformation is typically applied first?** - [ ] A. Sorting the integers in descending order. - [ ] B. Converting integers to floating-point numbers. - [x] C. Calculating differences between consecutive integers (Δ-gaps). - [ ] D. Applying Huffman coding directly to the integers.
    
107. **Question 7: What is the simplest nonparametric code for positive integers, representing k with k-1 zeros and one one?** - [ ] A. γ code - [ ] B. δ code - [x] C. Unary code - [ ] D. Rice code
    
108. **Question 8: Elias's γ code represents a positive integer k using:** - [ ] A. A fixed number of bits determined by the largest integer. - [ ] B. A unary code for k. - [x] C. A unary code for the length of k's binary representation, followed by k's binary representation (minus leading 1). - [ ] D. Arithmetic coding based on k's probability.
    
109. **Question 9: Compared to γ coding, δ coding is generally more efficient for:** - [ ] A. Very small integers. - [ ] B. Lists where all gaps are identical. - [x] C. Lists with predominantly large gaps. - [ ] D. Lists following a perfect geometric distribution.
    
110. **Question 10: Golomb/Rice codes are parametric codes optimal for integers following which distribution?** - [ ] A. Normal distribution - [ ] B. Uniform distribution - [x] C. Geometric distribution - [ ] D. Poisson distribution
    
111. **Question 11: What is the difference between Golomb codes and Rice codes?** 

- [ ] A. Golomb codes are faster to decode. 

- [x] B. Rice codes use a modulus M that is a power of 2, simplifying encoding/decoding. 

- [ ] C. Golomb codes achieve better compression ratios. 

- [ ] D. Rice codes are adaptive, while Golomb codes are static.
    
112. **Question 12: The LLRUN compression method is based on:** - [ ] A. Arithmetic coding - [ ] B. Golomb coding with run-length encoding - [x] C. Huffman coding applied to buckets of gap sizes - [ ] D. Interpolative coding
    
113. **Question 13: Interpolative coding achieves high compression, especially for small gaps, by:** - [ ] A. Using unary codes. - [x] B. Encoding a value based on its position relative to known surrounding values in a sorted sequence. - [ ] C. Applying arithmetic coding recursively. - [ ] D. Grouping gaps into fixed-size blocks.
    
114. **Question 14: Which type of code focuses on decoding speed by encoding gaps using an integer number of bytes?** - [ ] A. γ code - [ ] B. Interpolative code - [x] C. Byte-aligned codes (like vByte) - [ ] D. Arithmetic code
    
115. **Question 15: Simple-9 is an example of what type of coding?** - [ ] A. Bit-aligned coding using Huffman trees. - [x] B. Word-aligned coding, packing multiple small gaps into a machine word. - [ ] C. Adaptive arithmetic coding. - [ ] D. Lossy compression based on sampling.
    
116. **Question 16: Table-driven decoding significantly improves the speed of decoding bit-aligned codes (like γ or LLRUN) by:** - [ ] A. Using arithmetic operations instead of bit shifts. - [x] B. Precomputing results for small sequences of bits to avoid bit-by-bit processing. - [ ] C. Storing the entire decompressed list in memory. - [ ] D. Using a simpler compression model.
    
117. **Question 17: Why can document reordering improve index compression?** - [ ] A. It reduces the number of unique terms in the collection. - [ ] B. It increases the average document length. - [x] C. By assigning similar documents adjacent docids, it tends to create smaller Δ-gaps in postings lists. - [ ] D. It eliminates the need for a dictionary.
    
118. **Question 18: Which document reordering strategy often yields good compression improvements for Web collections?** - [ ] A. Ordering by document size. - [ ] B. Ordering randomly. - [ ] C. Ordering by the number of unique terms per document. - [x] D. Ordering by URL.
    
119. **Question 19: What is front coding used for?** - [ ] A. Compressing postings lists. - [x] B. Compressing dictionary terms by storing only the difference from the previous term. - [ ] C. Compressing query logs. - [ ] D. Compressing document metadata.
    
120. **Question 20: Combining techniques like grouping, front coding, vByte for pointers, and general-purpose compression (like LZ) can significantly reduce:** - [ ] A. The size of postings lists. - [x] B. The memory footprint of the query-time dictionary. - [ ] C. The time needed for index construction. - [ ] D. The number of unique terms.
    

### Chapter 7: Dynamic Inverted Indices

121. **Question 1: Why is managing dynamic text collections more complex than static ones?** - [ ] A. Static collections are always smaller. - [x] B. Dynamic collections require handling insertions, deletions, and modifications over time. - [ ] C. Static collections do not need inverted indices. - [ ] D. Dynamic collections cannot be compressed.
    
122. **Question 2: What is a "batch update" strategy?** - [ ] A. Updating the index immediately after every single document change. - [x] B. Accumulating changes and updating the index periodically in a single operation. - [ ] C. Using only an in-memory index without disk persistence. - [ ] D. Rebuilding the entire operating system when the index changes.
    
123. **Question 3: What are the two primary batch update strategies discussed?** - [ ] A. Insert and Delete - [ ] B. Compress and Decompress - [x] C. Rebuild and Remerge - [ ] D. Static and Dynamic
    
124. **Question 4: What is the main disadvantage of the Rebuild strategy?** - [ ] A. It cannot handle document deletions. - [ ] B. It is difficult to implement. - [x] C. It requires re-processing the entire collection, even unchanged documents. - [ ] D. The resulting index is usually fragmented.
    
125. **Question 5: The Remerge strategy involves:** - [ ] A. Re-indexing the entire collection from scratch. - [x] B. Building an index for new documents and merging it with the existing index. - [ ] C. Only deleting postings without adding new ones. - [ ] D. Storing the entire index in main memory.
    
126. **Question 6: Compared to Rebuild, Remerge is generally more efficient unless:** - [ ] A. Only insertions are occurring. - [ ] B. The collection size is very small. - [x] C. A very large percentage (e.g., >60%) of the documents are being deleted in the batch. - [ ] D. The index is stored in memory.
    
127. **Question 7: What is an "incremental" text collection?** - [ ] A. A collection where documents are only deleted, never added. - [x] B. A collection where new documents can be added, but existing ones are not modified or removed. - [ ] C. A collection that grows by exactly one document per day. - [ ] D. A collection stored entirely on incremental backup tapes.
    
128. **Question 8: The "No Merge" strategy for incremental updates involves:** - [ ] A. Merging all index partitions after each document addition. - [x] B. Keeping all index partitions separate and concatenating results at query time. - [ ] C. Using only an in-memory index. - [ ] D. Performing in-place updates on a single large index file.
    
129. **Question 9: What is the main drawback of the "No Merge" strategy?** - [ ] A. Very high index update cost. - [ ] B. Inability to handle new documents. - [x] C. Potentially very poor query performance due to many disk seeks across partitions. - [ ] D. Requires excessive RAM.
    
130. **Question 10: The "Immediate Merge" strategy involves:** - [ ] A. Keeping all index partitions separate. - [x] B. Merging the in-memory index with the _entire_ existing on-disk index whenever memory is full. - [ ] C. Only merging partitions once a week. - [ ] D. Using in-place updates.
    
131. **Question 11: What is the primary performance issue with "Immediate Merge"?** - [ ] A. Poor query performance due to fragmentation. - [x] B. High disk I/O cost for updates (quadratic in collection size). - [ ] C. Inability to handle document deletions. - [ ] D. Requires a very large amount of RAM.
    
132. **Question 12: "In-place update" strategies attempt to reduce update I/O by:** - [ ] A. Keeping the entire index in memory. - [ ] B. Rebuilding the index from scratch frequently. - [x] C. Appending new postings to the end of existing on-disk lists, relocating lists only when space runs out. - [ ] D. Merging index partitions logarithmically.
    
133. **Question 13: What is a major performance bottleneck for naive in-place updates, especially with many short lists?** - [ ] A. Excessive sequential disk reads. - [ ] B. The cost of merging lists. - [x] C. High number of random disk seeks for list relocations. - [ ] D. Inability to compress postings.
    
134. **Question 14: The hybrid strategy (HIMC) combines Immediate Merge and Inplace by:** - [ ] A. Randomly choosing which strategy to use for each update. - [x] B. Using Immediate Merge for short lists and Inplace updates for long lists (above a threshold). - [ ] C. Performing merges only during off-peak hours. - [ ] D. Replicating the index across multiple servers.
    
135. **Question 15: What is an index partitioning scheme?** - [ ] A. Dividing a single postings list among multiple nodes. - [x] B. Storing the index as multiple independent sub-indices (partitions). - [ ] C. Compressing the index using partitioning codes. - [ ] D. Assigning documents to partitions based on relevance.
    
136. **Question 16: Logarithmic Merging maintains multiple index partitions organized by "generation" and merges partitions when:** - [ ] A. The total index size exceeds a threshold. - [ ] B. A query requests data from multiple partitions. - [x] C. Two partitions are found with the same generation label. - [ ] D. A certain amount of time has passed.
    
137. **Question 17: Compared to Immediate Merge, Logarithmic Merging typically has:** - [ ] A. Much higher update costs but similar query performance. - [x] B. Lower update costs but potentially slightly worse query performance (due to fragmentation). - [ ] C. Similar update costs and similar query performance. - [ ] D. Much lower update costs and much better query performance.
    
138. **Question 18: How are document deletions typically handled without immediately modifying the main index?** - [ ] A. Deleted documents are ignored by the query processor. - [x] B. An invalidation list (or deletion list) is maintained and checked during query processing or merging. - [ ] C. The index is rebuilt whenever a deletion occurs. - [ ] D. Deleted documents are moved to a separate "deleted" index.
    
139. **Question 19: What is garbage collection in the context of dynamic indices?** - [ ] A. Freeing up unused RAM. - [x] B. Removing obsolete postings (corresponding to deleted documents) during a merge operation. - [ ] C. Deleting queries from the query log. - [ ] D. Archiving old index partitions.
    
140. **Question 20: Why is handling arbitrary document modifications (like appends) difficult with standard index structures?** - [ ] A. Modifications require re-indexing the entire document anyway. - [x] B. It can lead to multiple postings for the same (term, document) pair across different partitions or locations. - [ ] C. Compression cannot be used with modified documents. - [ ] D. Standard inverted indices do not store positional information.
    

### Chapter 8: Probabilistic Retrieval

141. **Question 1: The probabilistic retrieval model ranks documents based on their estimated:** - [ ] A. Size in bytes. - [ ] B. Number of incoming links. - [x] C. Probability of relevance to the query. - [ ] D. Similarity to the query vector in vector space.
    
142. **Question 2: The "Basic Question" underlying the probabilistic model is:** - [ ] A. How many terms does the document contain? - [x] B. What is the probability this document is relevant to this query? - [ ] C. How fast can this query be processed? - [ ] D. Is the document about the query terms?
    
143. **Question 3: The Binary Independence Model (BIM) makes which key assumption about terms?** - [ ] A. All terms appear with equal frequency. - [ ] B. Term occurrences are dependent on document length. - [x] C. Given relevance, terms occur in documents independently of each other. - [ ] D. All query terms must be present for a document to be relevant.
    
144. **Question 4: In the BIM, document ranking depends primarily on:** - [ ] A. Terms present in the document but not the query. - [ ] B. Terms present in the query but not the document. - [x] C. Terms present in both the query and the document. - [ ] D. The total number of terms in the document.
    
145. **Question 5: The Robertson/Spärck Jones weighting formula (Equation 8.23) provides a probabilistic derivation for a weight similar to:** - [ ] A. Term Frequency (TF) - [x] B. Inverse Document Frequency (IDF) - [ ] C. Document Length - [ ] D. Query Term Frequency
    
146. **Question 6: When no relevance information is available, the Robertson/Spärck Jones weight `wt` is typically estimated using:** - [ ] A. A constant value of 1. - [x] B. The standard IDF formula (e.g., log(N/Nt)). - [ ] C. The term frequency ft,d. - [ ] D. The document length ld.
    
147. **Question 7: What concept is introduced to bridge the gap between term frequency and relevance, suggesting a document is "about" a term's topic?** - [ ] A. Polysemy - [x] B. Eliteness - [ ] C. Stopwording - [ ] D. Smoothing
    
148. **Question 8: Bookstein's Two-Poisson model attempts to model term frequency by assuming:** - [ ] A. A single Poisson distribution for all documents. - [x] B. A mixture of two Poisson distributions, one for 'elite' documents and one for 'non-elite'. - [ ] C. A binomial distribution based on document length. - [ ] D. A Gaussian distribution of term frequencies.
    
149. **Question 9: A key property derived from the Two-Poisson model and its approximations (like Equation 8.41) is that the contribution of term frequency to the document score:** - [ ] A. Increases linearly without bound. - [ ] B. Decreases as term frequency increases. - [x] C. Saturates, reaching a maximum value. - [ ] D. Is ignored completely.
    
150. **Question 10: The parameter `k1` in BM25 and related formulae controls:** - [ ] A. The influence of document length. - [ ] B. The importance of IDF. - [x] C. How quickly the term frequency component saturates. - [ ] D. The number of expansion terms in relevance feedback.
    
151. **Question 11: Why is simple TF normalization (like dividing by document length) often inadequate?** - [ ] A. It makes TF values too small. - [ ] B. It assumes all documents are about the same topic. - [ ] C. It doesn't account for the non-linear relationship between raw TF and relevance contribution. - [x] D. It over-penalizes long documents containing many term occurrences proportionally.
    
152. **Question 12: The BM25 formula introduces a parameter `b` (typically 0 <= b <= 1) primarily to control:** - [ ] A. The degree of term frequency saturation. - [ ] B. The influence of query term frequency. - [x] C. The level of document length normalization. - [ ] D. The smoothing applied to IDF weights.
    
153. **Question 13: What does "Okapi BM25" refer to?** - [ ] A. A specific test collection. - [ ] B. A probabilistic model based purely on term presence. - [x] C. A specific, widely used ranking formula incorporating TF and document length normalization (Equation 8.48). - [ ] D. A type of relevance feedback.
    
154. **Question 14: Relevance Feedback aims to improve retrieval performance by:** - [x] A. Using user judgments on initial results to refine the query or term weights. - [ ] B. Compressing the index more effectively. - [ ] C. Pre-filtering documents based on static rank. - [ ] D. Increasing the speed of query processing.
    
155. **Question 15: Pseudo-Relevance Feedback (PRF) or blind feedback differs from traditional relevance feedback in that it:** - [ ] A. Requires users to judge non-relevant documents. - [x] B. Assumes the top-k retrieved documents are relevant, without explicit user judgments. - [ ] C. Only adjusts term weights, without adding new terms. - [ ] D. Uses a different underlying probabilistic model.
    
156. **Question 16: A potential risk of Pseudo-Relevance Feedback is:** - [ ] A. It significantly slows down the initial query. - [ ] B. It requires large amounts of training data. - [x] C. If initial results are poor, it can cause "query drift" by adding non-relevant expansion terms. - [ ] D. It cannot be automated.
    
157. **Question 17: The term selection value `wt * (pt - pt_bar)` (Equation 8.49) prioritizes terms that are:** - [ ] A. Frequent in the collection overall. - [x] B. Much more likely to occur in relevant documents than in non-relevant documents. - [ ] C. Short words. - [ ] D. Present in the initial query.
    
158. **Question 18: BM25F is an extension of BM25 designed to:** - [ ] A. Handle very long queries more efficiently. - [ ] B. Incorporate passage-level evidence. - [x] C. Use different weights for terms appearing in different document fields (e.g., title vs. body). - [ ] D. Perform query expansion automatically.
    
159. **Question 19: In BM25F, `f'_t,d` represents:** - [ ] A. The IDF weight for term t. - [ ] B. A normalized term frequency based only on document length. - [x] C. A field-weighted and normalized pseudo-frequency for term t in document d. - [ ] D. The query frequency of term t.
    
160. **Question 20: The development of the probabilistic models (leading to BM25) involved:** - [ ] A. Relying purely on mathematical theory without experimentation. - [x] B. A series of theoretical developments, assumptions, approximations, and experimental validations. - [ ] C. Directly adopting models from particle physics. - [ ] D. Primarily focusing on computational efficiency.
    

### Chapter 9: Language Modeling and Related Methods

161. **Question 1: The Language Modeling (LM) approach to IR ranks documents based on:** - [ ] A. The probability of the document being relevant to the query. - [x] B. The probability that the document's language model would generate the query. - [ ] C. The cosine similarity between document and query language models. - [ ] D. The number of query terms present in the document.
    
162. **Question 2: In the query generation model, the document `d` is viewed as:** - [ ] A. A sequence of relevance judgments. - [ ] B. A vector in term space. - [x] C. A generative model for the query `q`. - [ ] D. A node in the Web graph.
    
163. **Question 3: The simplest document language model, M_ml(d)(t), is the Maximum Likelihood Estimate based on:** - [ ] A. Collection-wide term frequency (lt/lC). - [x] B. Within-document term frequency (ft,d/ld). - [ ] C. Inverse document frequency (log(N/Nt)). - [ ] D. BM25 score.
    
164. **Question 4: Why is smoothing essential when using document language models for retrieval?** - [ ] A. To make the models faster to compute. - [x] B. To handle query terms that do not appear in a relevant document (avoiding zero probabilities). - [ ] C. To account for document length. - [ ] D. To compress the language model.
    
165. **Question 5: Jelinek-Mercer smoothing creates a document model by:** - [ ] A. Adding a fixed count to each term frequency. - [ ] B. Using only the collection language model. - [x] C. Taking a linear interpolation between the document model (MLE) and a background (collection) model. - [ ] D. Applying a logarithmic transformation to term frequencies.
    
166. **Question 6: Dirichlet smoothing conceptually involves:** - [ ] A. Removing common terms from the document. - [x] B. Pretending a certain number (μ) of "extra" tokens, distributed according to the collection model, were added to the document. - [ ] C. Using a mixture of Gaussian distributions. - [ ] D. Interpolating between TF and IDF scores.
    
167. **Question 7: In the language modeling ranking formulas (Eq 9.21, 9.22), what does Md(t) represent?** - [ ] A. The query language model probability for term t. - [x] B. The smoothed document language model probability for term t. - [ ] C. The inverse document frequency of term t. - [ ] D. The TF-IDF weight of term t in document d.
    
168. **Question 8: Compared to BM25, a notable characteristic of the basic LM ranking formulas (like Eq 9.31) is the absence of:** - [ ] A. Term frequency (ft,d). - [ ] B. Document length (ld). - [x] C. Explicit collection statistics like N (total documents) and Nt (document frequency). - [ ] D. Logarithms.
    
169. **Question 9: What theoretical framework provides an alternative justification for the LM approach by measuring the "distance" between probability distributions?** - [ ] A. Vector Space Model - [ ] B. Bayesian Inference - [x] C. Kullback-Leibler (KL) Divergence - [ ] D. Queueing Theory
    
170. **Question 10: Using KL divergence, ranking documents involves minimizing the divergence between:** - [ ] A. The document model and the collection model. - [x] B. The query model and the document model. - [ ] C. The relevant document model and the non-relevant document model. - [ ] D. The smoothed model and the unsmoothed model.
    
171. **Question 11: The Divergence From Randomness (DFR) approach ranks documents by:** - [x] A. Measuring how much the term distribution in a document diverges from a random distribution. - [ ] B. Calculating the KL divergence between the query and document models. - [ ] C. Using a smoothed language model based on Dirichlet priors. - [ ] D. Applying the PageRank algorithm to term co-occurrences.
    
172. **Question 12: In the basic DFR formula (1 - P2) * (-log P1), what does P1 represent?** - [ ] A. The probability of the document being relevant. - [x] B. The probability that a random process generates exactly ft,d occurrences of term t in the document. - [ ] C. The probability of eliteness (finding at least one more occurrence). - [ ] D. The smoothing parameter.
    
173. **Question 13: In the basic DFR formula (1 - P2) * (-log P1), what does (1 - P2) represent?** - [ ] A. The IDF component. - [ ] B. The document length normalization factor. - [x] C. A correction factor based on the probability of the document _not_ being elite in term t. - [ ] D. The query term frequency.
    
174. **Question 14: Laplace's Law of Succession is used in DFR to estimate which component?** - [x] A. P1 (probability of observed term frequency by chance) - [ ] B. P2 (probability of eliteness) - [ ] C. Document length normalization - [ ] D. Query term frequency
    
175. **Question 15: How does DFR typically handle document length normalization?** - [ ] A. It is ignored, assuming all documents have the same length. - [ ] B. By dividing term frequency by document length. - [ ] C. By incorporating a factor similar to BM25's length normalization. - [x] D. By computing an adjusted term frequency (e.g., using Eq 9.52).
    
176. **Question 16: What is passage retrieval concerned with?** - [ ] A. Retrieving entire documents only. - [x] B. Retrieving arbitrary fragments of text within documents. - [ ] C. Retrieving only document titles. - [ ] D. Retrieving only documents from a specific passage of time.
    
177. **Question 17: An "m-cover" extends the concept of a cover by considering intervals that contain:** - [ ] A. All n query terms exactly once. - [x] B. At least m distinct query terms (where m <= n). - [ ] C. Exactly m query terms in the correct order. - [ ] D. Only query terms with high IDF.
    
178. **Question 18: The passage scoring formula (Eq 9.58) derived in the chapter resembles:** - [ ] A. The BM25 formula. - [x] B. A TF-IDF calculation, emphasizing collection frequency (lC/lt) and penalizing passage length (l). - [ ] C. The PageRank formula. - [ ] D. A simple count of query terms.
    
179. **Question 19: Implementing the search for m-covers can be seen as an extension of the algorithm used for:** - [ ] A. Calculating PageRank. - [ ] B. Building a suffix tree. - [x] C. Finding covers in proximity ranking (Chapter 2). - [ ] D. Calculating TF-IDF weights.
    
180. **Question 20: Compared to probabilistic models like BM25, language modeling approaches place less direct emphasis on:** - [ ] A. Term frequency - [ ] B. Document length - [x] C. Explicit modeling of relevance - [ ] D. Collection statistics
    

### Chapter 10: Categorization and Filtering

181. **Question 1: What is the primary difference between categorization and filtering?** - [ ] A. Categorization uses relevance feedback, filtering does not. - [x] B. Categorization labels existing documents; filtering processes incoming documents based on standing needs. - [ ] C. Categorization outputs a ranked list, filtering outputs a set. - [ ] D. Categorization is always supervised, filtering is always unsupervised.
    
182. **Question 2: Routing and Selective Dissemination of Information (SDI) are synonyms for:** - [ ] A. Ad hoc search - [ ] B. Language identification - [x] C. Filtering - [ ] D. Document clustering
    
183. **Question 3: A key difference between filtering/categorization and ad hoc search is that the information need is often:** - [ ] A. Temporary and specific. - [x] B. Longstanding, recurring, or commonly understood. - [ ] C. Expressed as a Boolean query. - [ ] D. Irrelevant to the process.
    
184. **Question 4: A classifier that outputs a continuous score instead of a binary label is called a:** - [ ] A. Hard classifier - [x] B. Soft classifier (or ranker) - [ ] C. Generative model - [ ] D. Decision stump
    
185. **Question 5: What evaluation measure is typically used for hard binary classification (assigning to one of two categories)?** - [ ] A. Mean Average Precision (MAP) - [x] B. Accuracy (or Error Rate) - [ ] C. Reciprocal Rank (RR) - [ ] D. Throughput
    
186. **Question 6: In diagnostic testing terms, sensitivity (or true positive rate) measures the fraction of:** - [ ] A. Negative instances correctly identified. - [x] B. Positive instances correctly identified. - [ ] C. Negative instances incorrectly identified as positive. - [ ] D. Positive instances incorrectly identified as negative.
    
187. **Question 7: Specificity (or true negative rate) measures the fraction of:** - [x] A. Negative instances correctly identified. - [ ] B. Positive instances correctly identified. - [ ] C. Negative instances incorrectly identified as positive. - [ ] D. Positive instances incorrectly identified as negative.
    
188. **Question 8: An ROC curve plots:** - [ ] A. Precision vs. Recall - [x] B. True Positive Rate vs. False Positive Rate (or related error rates) - [ ] C. Accuracy vs. Number of training examples - [ ] D. Latency vs. Throughput
    
189. **Question 9: What does the Area Under the ROC Curve (AUC) represent probabilistically?** - [ ] A. The probability that the classifier makes an error. - [x] B. The probability that a randomly chosen positive instance has a higher score than a randomly chosen negative instance. - [ ] C. The overall accuracy of the classifier. - [ ] D. The F1 score.
    
190. **Question 10: Which learning mode uses labeled training data (T, label) to build a classifier?** - [ ] A. Unsupervised learning - [ ] B. Semi-supervised learning - [x] C. Supervised learning - [ ] D. Reinforcement learning
    
191. **Question 11: On-line learning differs from batch learning in that:** - [ ] A. It uses no training data. - [x] B. Examples are processed sequentially, testing then training. - [ ] C. It only works for linear classifiers. - [ ] D. It cannot adapt over time.
    
192. **Question 12: What is "feature engineering"?** - [ ] A. Automatically selecting the best learning algorithm. - [x] B. Defining and extracting features from documents to represent them for a classifier. - [ ] C. Tuning the parameters of a classifier. - [ ] D. Compressing the feature vectors.
    
193. **Question 13: Naive Bayes classifiers combine evidence from different features by assuming the features are:** - [ ] A. Highly correlated. - [ ] B. Linearly separable. - [x] C. Conditionally independent given the class. - [ ] D. All binary.
    
194. **Question 14: Logistic Regression is a probabilistic method that directly models the:** - [ ] A. Probability density function of features. - [x] B. Log-odds of a document belonging to the positive class. - [ ] C. Margin between classes. - [ ] D. Entropy of the feature distribution.
    
195. **Question 15: A linear classifier, such as a Perceptron or SVM, typically defines a:** - [ ] A. Decision tree - [x] B. Hyperplane separating the feature space - [ ] C. Probability distribution - [ ] D. Set of clusters
    
196. **Question 16: What is the goal of a Support Vector Machine (SVM)?** - [x] A. To find the hyperplane that maximizes the margin between classes. - [ ] B. To build a probabilistic model based on feature independence. - [ ] C. To create a decision tree by maximizing information gain. - [ ] D. To find the nearest neighbors in the training set.
    
197. **Question 17: What is the "kernel trick" used for in methods like SVMs?** - [ ] A. To speed up matrix inversion. - [x] B. To implicitly map data to a higher-dimensional space using a kernel function, allowing non-linear separation. - [ ] C. To smooth probability estimates. - [ ] D. To handle missing feature values.
    
198. **Question 18: Nearest Neighbor (NN) classifiers categorize a document based on:** - [ ] A. A predefined set of rules. - [x] B. The category of the most similar document(s) in the training set. - [ ] C. A probabilistic model learned from the training set. - [ ] D. The output of a linear function.
    
199. **Question 19: Information-theoretic classifiers often work by:** - [ ] A. Maximizing the margin between classes. - [x] B. Comparing data compression models built from positive and negative examples. - [ ] C. Finding the nearest neighbor in the training data. - [ ] D. Using logistic regression.
    
200. **Question 20: What does LAM (Logit Average) provide?** - [ ] A. A micro-averaged error rate. - [x] B. A macro-averaged measure less sensitive to threshold setting and prevalence than simple error rates. - [ ] C. An estimate of the AUC score. - [ ] D. The F1 score averaged across categories.
    

### Chapter 11: Fusion and Metalearning

201. **Question 1: What is the general goal of the methods discussed in this chapter (fusion, stacking, bagging, boosting, etc.)?** - [ ] A. To compress the inverted index more effectively. - [x] B. To combine results from multiple methods to achieve better performance than any single method. - [ ] C. To evaluate the efficiency of different ranking functions. - [ ] D. To perform query expansion automatically.
    
202. **Question 2: Search-result fusion aims to combine:** - [ ] A. Multiple queries into one. - [ ] B. Dictionaries from different indices. - [x] C. Ranked lists of documents from different search systems or methods. - [ ] D. Features extracted from documents.
    
203. **Question 3: The "election" method for fixed-cutoff aggregation selects documents based on:** - [ ] A. Their average relevance score. - [ ] B. Their rank in the best individual system. - [x] C. The number of input lists they appear in. - [ ] D. Their document length.
    
204. **Question 4: Reciprocal Rank Fusion (RRF) combines ranked lists by scoring documents based on:** - [ ] A. The sum of their ranks across lists. - [x] B. The sum of the inverse of their rank (plus a constant k) across lists. - [ ] C. The minimum rank achieved in any list. - [ ] D. A majority vote on pairwise preferences.
    
205. **Question 5: CombMNZ combines lists by considering both:** - [ ] A. Document length and query length. - [ ] B. Rank and score of documents. - [ ] C. Precision and recall. - [x] D. The number of lists a document appears in and the sum of its scores.
    
206. **Question 6: What is "stacking" in the context of combining classifiers?** - [ ] A. Physically stacking servers in a rack. - [x] B. Using the output of base classifiers as input features for a meta-classifier. - [ ] C. Averaging the results of classifiers trained on bootstrap samples. - [ ] D. Iteratively reweighting training examples.
    
207. **Question 7: What is the purpose of calibrating scores (e.g., converting to log-odds) before stacking adaptive filters?** - [ ] A. To make the scores positive. - [x] B. To provide a more meaningful basis for combination by the meta-learner. - [ ] C. To compress the scores. - [ ] D. To ensure the scores are integers.
    
208. **Question 8: Holdout validation involves:** - [ ] A. Training a classifier on the entire dataset. - [x] B. Splitting the labeled data into a training set and a separate validation set. - [ ] C. Using only unlabeled data for training. - [ ] D. Averaging results from multiple runs.
    
209. **Question 9: k-fold cross-validation is a technique used to:** - [ ] A. Select the best features for a classifier. - [x] B. Get more robust estimates of performance by repeatedly partitioning data into training/validation sets. - [ ] C. Speed up the training process. - [ ] D. Combine the results of k different classifiers.
    
210. **Question 10: What is Bagging (Bootstrap Aggregation)?** - [ ] A. Training multiple classifiers on different subsets of features. - [ ] B. Training a sequence of classifiers, focusing on misclassified examples. - [x] C. Training multiple classifiers on bootstrap samples (resamples) of the training data and averaging their outputs. - [ ] D. Stacking classifiers using a logistic regression meta-learner.
    
211. **Question 11: Bagging is particularly effective for learning methods that are:** - [ ] A. Very stable and insensitive to training data changes. - [x] B. Unstable, meaning their output changes significantly with small changes in training data. - [ ] C. Linear classifiers. - [ ] D. Unsupervised methods.
    
212. **Question 12: What is Boosting?** - [ ] A. Averaging classifiers trained on bootstrap samples. - [x] B. Training a sequence of classifiers, where each focuses on examples misclassified by previous ones, and combining them with weights. - [ ] C. Stacking classifiers using a support vector machine. - [ ] D. Using hardware acceleration for training.
    
213. **Question 13: Compared to Bagging, Boosting primarily aims to reduce:** - [ ] A. Generalization error by randomizing. - [x] B. Training error by focusing on difficult examples. - [ ] C. Computational cost. - [ ] D. The number of features required.
    
214. **Question 14: When ranking categories for a document (multicategory ranking), what assumption is made about the scores s(d, q)?** - [ ] A. Scores for different categories q are independent. - [x] B. Scores are comparable across different categories for the same document. - [ ] C. Scores are always binary (0 or 1). - [ ] D. Scores are identical to document ranking scores.
    
215. **Question 15: The "one versus rest" approach to multicategory classification involves:** - [ ] A. Training one classifier to distinguish all categories simultaneously. - [x] B. Training n binary classifiers, each separating one category from all the others. - [ ] C. Training n(n-1)/2 binary classifiers, one for each pair of categories. - [ ] D. Using k-nearest neighbors.
    
216. **Question 16: The "one versus one" approach to multicategory classification involves:** - [ ] A. Training one classifier to distinguish all categories simultaneously. - [ ] B. Training n binary classifiers, each separating one category from all the others. - [x] C. Training n(n-1)/2 binary classifiers, one for each pair of categories, often combined via voting. - [ ] D. Using a single decision tree.
    
217. **Question 17: What does "Learning to Rank" specifically refer to?** - [ ] A. Any method that produces a ranked list. - [x] B. Learning a function that directly optimizes the ordering of items based on training data consisting of preferences or ranks. - [ ] C. Using unsupervised learning for ranking. - [ ] D. The process of calculating PageRank.
    
218. **Question 18: Pointwise learning-to-rank methods typically reduce the problem to:** - [x] A. A standard regression or classification problem for each individual item. - [ ] B. A problem of ordering pairs of items. - [ ] C. A problem of optimizing the entire ranked list directly. - [ ] D. A clustering problem.
    
219. **Question 19: Pairwise learning-to-rank methods typically focus on:** - [ ] A. Predicting the relevance score for each item. - [x] B. Minimizing the number of incorrectly ordered pairs of items. - [ ] C. Optimizing list-based metrics like nDCG directly. - [ ] D. Using decision trees.
    
220. **Question 20: LETOR is a:** - [ ] A. Specific learning-to-rank algorithm. - [x] B. Benchmark dataset and framework for evaluating learning-to-rank methods. - [ ] C. Software package for SVMs. - [ ] D. Type of feature used in Web search.
    

### Chapter 12: Measuring Effectiveness

221. **Question 1: What are the two fundamental assumptions underlying traditional IR evaluation?** - [ ] A. All documents are relevant; relevance depends on ranking. - [x] B. Documents are either relevant or nonrelevant w.r.t an information need; relevance is independent of ranking. - [ ] C. Relevance is graded; effectiveness is measured by speed. - [ ] D. All queries are navigational; users only click the first result.
    
222. **Question 2: Which measure is defined as |Res ) Rel| / |Rel|?** - [ ] A. Precision - [x] B. Recall - [ ] C. F-measure - [ ] D. Accuracy
    
223. **Question 3: Which measure is defined as |Res ) Rel| / |Res|?** - [x] A. Precision - [ ] B. Recall - [ ] C. F-measure - [ ] D. Accuracy
    
224. **Question 4: P@k is suitable for modeling user satisfaction when the user typically examines:** - [ ] A. All relevant documents, regardless of list length. - [ ] B. Only the documents ranked below k. - [x] C. A small, fixed number (k) of top-ranked documents. - [ ] D. Only documents marked as non-relevant.
    
225. **Question 5: Average Precision (AP) provides a single-figure summary of a ranking by averaging:** - [ ] A. Recall values at different document cutoffs. - [x] B. Precision values obtained after each relevant document is retrieved. - [ ] C. The time taken to retrieve each relevant document. - [ ] D. The scores assigned by the ranking function.
    
226. **Question 6: Mean Average Precision (MAP) is calculated by:** - [x] A. Averaging AP scores across multiple topics. - [ ] B. Finding the maximum AP score achieved across all topics. - [ ] C. Averaging P@k scores across multiple topics. - [ ] D. Calculating the geometric mean of AP scores.
    
227. **Question 7: Reciprocal Rank (RR) is particularly suitable for evaluating which type of task?** - [ ] A. Tasks where finding all relevant documents is crucial. - [ ] B. Tasks where many relevant documents are expected. - [x] C. Tasks where the user wants to find a single specific correct answer (e.g., navigational queries). - [ ] D. Tasks involving filtering rather than ad hoc search.
    
228. **Question 8: Why might the geometric mean (like GMAP) be preferred over the arithmetic mean (like MAP) for averaging scores like AP?** - [ ] A. It is simpler to calculate. - [ ] B. It gives more weight to topics with high AP scores. - [x] C. It is less sensitive to occasional very low (e.g., zero) scores on some topics, better reflecting overall utility. - [ ] D. It directly measures user satisfaction.
    
229. **Question 9: The TREC methodology uses pooling primarily to:** - [ ] A. Increase the number of topics in the test collection. - [x] B. Create a manageable subset of documents for relevance judging. - [ ] C. Ensure all participating systems perform equally well. - [ ] D. Automatically determine document relevance.
    
230. **Question 10: In statistics, what does a confidence interval provide?** - [ ] A. A guarantee that the true value falls within the interval. - [x] B. A range of values likely to contain the true value, with a specified probability (confidence level). - [ ] C. The exact p-value for a hypothesis test. - [ ] D. The point estimate of the measured value.
    
231. **Question 11: A p-value represents:** - [ ] A. The probability that the measurement is correct. - [x] B. The probability of observing the measured result (or more extreme) if the null hypothesis were true. - [ ] C. The magnitude of the difference between two systems. - [ ] D. The confidence level (1 - α).
    
232. **Question 12: Why is reporting only "statistical significance" (p < 0.05) often considered insufficient?** - [ ] A. It doesn't indicate the magnitude or substantiveness of the difference. - [ ] B. The 0.05 threshold is arbitrary. - [ ] C. It doesn't provide information about precision. - [x] D. All of the above.
    
233. **Question 13: The paired t-test is generally preferred over the unpaired t-test for comparing IR systems on the same topic set because:** - [ ] A. It is easier to compute. - [x] B. It accounts for the correlation between system scores on the same topic, usually yielding higher precision. - [ ] C. It does not assume a normal distribution. - [ ] D. It works better with small numbers of topics.
    
234. **Question 14: What non-parametric test uses only the sign (+/-) of the differences between paired measurements?** - [ ] A. t-test - [ ] B. Wilcoxon signed-rank test - [x] C. Sign test - [ ] D. ANOVA
    
235. **Question 15: Meta-analysis is a technique for:** - [ ] A. Evaluating a single system on multiple test collections. - [x] B. Statistically combining the results of several independent experiments. - [ ] C. Analyzing the metadata associated with documents. - [ ] D. Speeding up relevance assessments.
    
236. **Question 16: What is a major challenge when reusing test collections with unjudged documents?** - [ ] A. The collection size might be too small. - [x] B. The assumption that unjudged documents are non-relevant can introduce bias, especially against new systems. - [ ] C. The topics may become outdated. - [ ] D. The relevance judgments might be incorrect.
    
237. **Question 17: Inferred Average Precision (infAP) is designed to:** - [x] A. Estimate AP scores when only a random sample of the pool has been judged. - [ ] B. Measure precision for navigational queries only. - [ ] C. Incorporate graded relevance judgments. - [ ] D. Measure diversity in the results.
    
238. **Question 18: Graded relevance judgments are useful when:** - [ ] A. All documents are equally relevant. - [x] B. Documents can satisfy an information need to varying degrees, or vary in quality. - [ ] C. Only binary judgments are available. - [ ] D. Evaluating system efficiency.
    
239. **Question 19: Normalized Discounted Cumulative Gain (nDCG) is specifically designed to evaluate rankings based on:** - [ ] A. Binary relevance judgments. - [x] B. Graded relevance judgments, incorporating rank discounting. - [ ] C. The time taken by the user. - [ ] D. The diversity of results only.
    
240. **Question 20: Measures of novelty and diversity aim to address the problem of:** - [ ] A. Unjudged documents in the collection. - [x] B. Retrieval systems returning multiple redundant or overly similar documents. - [ ] C. Queries with only one relevant document. - [ ] D. Evaluating efficiency rather than effectiveness.
    

### Chapter 13: Measuring Efficiency

241. **Question 1: Besides effectiveness (result quality), what is the other crucial aspect of IR system usefulness?** - [ ] A. Index size - [ ] B. Algorithm complexity - [x] C. Efficiency (resource consumption, speed) - [ ] D. Programming language used
    
242. **Question 2: What does "latency" (or response time) measure?** - [ ] A. The number of queries processed per second. - [ ] B. The total storage space used by the index. - [x] C. The time elapsed between query receipt and results being sent. - [ ] D. The CPU utilization percentage.
    
243. **Question 3: What does "throughput" (or service rate) measure?** - [ ] A. The time taken for a single query. - [x] B. The number of queries processed within a given time period (e.g., queries per second). - [ ] C. The network bandwidth required. - [ ] D. The accuracy of the results.
    
244. **Question 4: Why might average latency be a misleading indicator of user experience?** - [ ] A. Users prefer higher latency. - [x] B. Averages can hide a poor experience for a subset of users facing very high latency (long tail). - [ ] C. Latency is difficult to measure accurately. - [ ] D. Throughput is always more important.
    
245. **Question 5: Using latency quantiles (e.g., "99% of queries processed in under 1 second") provides a better measure of:** - [ ] A. Theoretical maximum throughput. - [x] B. Consistent user experience across most queries. - [ ] C. Average service time. - [ ] D. Disk I/O performance only.
    
246. **Question 6: Queueing theory is used to:** - [ ] A. Design better caching algorithms. - [x] B. Model and analyze system behavior (like latency) under various loads (arrival rates). - [ ] C. Compress postings lists. - [ ] D. Determine optimal document ranking.
    
247. **Question 7: In the M/M/1 queueing model notation, what does the first 'M' signify?** - [ ] A. Multiple servers. - [x] B. Markovian (exponential) arrival process. - [ ] C. Measured service time. - [ ] D. Maximum queue length.
    
248. **Question 8: In the M/M/1 model, what does the second 'M' signify?** - [x] A. Markovian (exponential) service time distribution. - [ ] B. Minimum arrival rate. - [ ] C. Memoryless property of arrivals only. - [ ] D. Multiple queues.
    
249. **Question 9: In the M/M/1 model, what does the '1' signify?** - [ ] A. Infinite queue capacity. - [x] B. A single server processing queries one at a time. - [ ] C. An arrival rate of 1 query per second. - [ ] D. A service time of 1 second.
    
250. **Question 10: What is traffic intensity or utilization (ρ) in the M/M/1 model?** - [ ] A. The average service time (1/μ). - [ ] B. The average arrival rate (λ). - [x] C. The ratio of arrival rate to service rate (λ/μ). - [ ] D. The number of queries in the queue.
    
251. **Question 11: According to the M/M/1 model, what happens to average latency as utilization (ρ) approaches 1 (100%)?** - [ ] A. It approaches zero. - [ ] B. It approaches the average service time. - [x] C. It increases dramatically, approaching infinity. - [ ] D. It remains constant.
    
252. **Question 12: Little's Law relates average number of queries in the system (n), arrival rate (λ), and average response time (r) by which formula?** - [ ] A. r = n * λ - [ ] B. r = λ / n - [x] C. r = n / λ - [ ] D. n = r * λ
    
253. **Question 13: What is the primary goal of query scheduling algorithms like SJF or DDS?** - [ ] A. To ensure perfect fairness (strict FCFS). - [x] B. To minimize average latency or reduce the number of queries missing a deadline. - [ ] C. To increase the theoretical throughput (service rate). - [ ] D. To simplify cache management.
    
254. **Question 14: What is a potential drawback of the Shortest Job First (SJF) scheduling algorithm?** - [ ] A. It is difficult to implement. - [x] B. It can lead to starvation for queries with long predicted service times. - [ ] C. It increases average latency compared to FCFS. - [ ] D. It requires knowing the exact arrival time of future queries.
    
255. **Question 15: What is caching in the context of search engines?** - [ ] A. Storing the inverted index in main memory. - [x] B. Storing frequently used data (like results, list intersections, postings) to avoid recomputing or re-fetching them. - [ ] C. Using a faster CPU. - [ ] D. Compressing query logs.
    
256. **Question 16: Why does caching query results have limitations in improving overall performance significantly?** - [ ] A. Caching uses too much disk space. - [x] B. Many queries are unique (long tail of Zipf distribution) and won't be found in the cache. - [ ] C. Caching introduces significant latency. - [ ] D. Result caches cannot be updated.
    
257. **Question 17: Caching list intersections is most relevant for search engines using which retrieval model?** - [ ] A. Vector Space Model - [ ] B. Probabilistic Model (BM25) - [ ] C. Language Modeling - [x] D. Boolean AND (Conjunctive)
    
258. **Question 18: What is a common general-purpose cache replacement policy?** - [ ] A. First-In, First-Out (FIFO) - [x] B. Least Recently Used (LRU) - [ ] C. Most Frequently Used (MFU) - [ ] D. Random Replacement
    
259. **Question 19: Cost-aware cache policies (like using ENB) improve upon simple LRU/LFU by considering:** - [ ] A. Only the size of the cached item. - [ ] B. Only the frequency of use. - [x] C. The cost to fetch/recompute the item, its expected gain, and its expected frequency of use. - [ ] D. The physical location of the item on disk.
    
260. **Question 20: What is prefetching in the context of caching?** - [ ] A. Evicting items from the cache before they are needed. - [ ] B. Increasing the size of the cache dynamically. - [x] C. Loading items into the cache proactively based on predicted future requests. - [ ] D. Using multiple cache levels.
    

### Chapter 14: Parallel Information Retrieval

261. **Question 1: Why is parallel processing often necessary for large-scale IR systems like Web search engines?** - [ ] A. To improve retrieval effectiveness (MAP). - [x] B. Single machines lack the computational power and storage for huge datasets and query volumes. - [ ] C. To simplify index compression algorithms. - [ ] D. To support Boolean NOT queries.
    
262. **Question 2: What is inter-query parallelism?** - [ ] A. Processing different parts of a single query on multiple machines simultaneously. - [x] B. Processing multiple different queries on multiple machines (or replicas) simultaneously. - [ ] C. Using multiple threads within a single query process. - [ ] D. Caching query results.
    
263. **Question 3: What is intra-query parallelism?** - [ ] A. Processing multiple different queries on a single machine. - [x] B. Processing different parts of a single query on multiple machines simultaneously. - [ ] C. Using query scheduling to optimize latency. - [ ] D. Replicating the entire index.
    
264. **Question 4: Index replication primarily improves which performance metric?** - [ ] A. Latency for a single query. - [x] B. Theoretical throughput (service rate). - [ ] C. Index compression ratio. - [ ] D. Retrieval effectiveness (MAP).
    
265. **Question 5: Index partitioning primarily improves which performance metric(s)?** - [ ] A. Only throughput. - [ ] B. Only latency. - [x] C. Both throughput and latency (though speedup may be less than 100%). - [ ] D. Index size.
    
266. **Question 6: In document partitioning, each node holds:** - [ ] A. An index for a subset of the terms in the collection. - [ ] B. A complete replica of the entire index. - [x] C. An index for a subset of the documents in the collection. - [ ] D. A cache of query results.
    
267. **Question 7: When processing a query with document partitioning, which nodes are typically involved?** - [ ] A. Only the node containing the query terms. - [ ] B. A single, randomly selected node. - [x] C. All index nodes. - [ ] D. Only the receptionist node.
    
268. **Question 8: In term partitioning, each node holds:** - [x] A. An index for a subset of the terms in the collection. - [ ] B. A complete replica of the entire index. - [ ] C. An index for a subset of the documents in the collection. - [ ] D. The query log.
    
269. **Question 9: When processing a query with term partitioning, which nodes are involved?** - [ ] A. All index nodes. - [x] B. Only the nodes responsible for the terms present in the query. - [ ] C. A single receptionist node. - [ ] D. Nodes selected based on document relevance.
    
270. **Question 10: For indices stored on disk, why might term partitioning offer a latency advantage over document partitioning?** - [ ] A. It reduces the number of terms processed per query. - [ ] B. It allows document-at-a-time processing. - [x] C. It reduces the number of random disk seeks required across all nodes for a given query. - [ ] D. It inherently supports fault tolerance.
    
271. **Question 11: A major challenge/limitation of basic term partitioning is:** - [ ] A. It scales poorly with the number of documents. - [ ] B. It cannot handle short queries. - [ ] C. It requires excessive network bandwidth for merging results. - [x] D. Load imbalance (popular/long lists concentrate work) and incompatibility with document-at-a-time ranking.
    
272. **Question 12: Hybrid partitioning schemes attempt to:** - [x] A. Combine features of document and term partitioning or replication. - [ ] B. Use both disk and RAM for index storage. - [ ] C. Mix different ranking algorithms. - [ ] D. Support both keyword and phrase queries.
    
273. **Question 13: Why is fault tolerance important in large distributed search engines?** - [ ] A. To improve MAP scores. - [ ] B. To reduce index size. - [x] C. With many machines, individual node failures become likely and the system should degrade gracefully. - [ ] D. To handle dynamic updates efficiently.
    
274. **Question 14: Compared to term partitioning, document partitioning generally offers better:** - [ ] A. Load balancing. - [x] B. Handling of single node failures (graceful degradation). - [ ] C. Performance for disk-based indices. - [ ] D. Support for Boolean AND queries.
    
275. **Question 15: Dormant replication involves:** - [ ] A. Keeping multiple active replicas of each index shard. - [x] B. Storing backup copies of index fragments on other nodes, activated only upon failure. - [ ] C. Partially replicating only the most important documents. - [ ] D. Using RAID storage for the index.
    
276. **Question 16: What is MapReduce primarily designed for?** - [ ] A. Real-time query processing with low latency. - [x] B. Massively parallel processing of large datasets for offline tasks (like index building). - [ ] C. Caching query results. - [ ] D. Compressing postings lists.
    
277. **Question 17: What are the three main phases of a MapReduce job?** - [ ] A. Index, Query, Rank - [x] B. Map, Shuffle, Reduce - [ ] C. Read, Process, Write - [ ] D. Partition, Replicate, Merge
    
278. **Question 18: What is the purpose of the 'shuffle' phase in MapReduce?** - [ ] A. To execute the user-defined map function. - [x] B. To sort and group intermediate key/value pairs so all values for the same key reach the same reducer. - [ ] C. To execute the user-defined reduce function. - [ ] D. To randomly distribute data across nodes.
    
279. **Question 19: What is a 'combiner' in MapReduce used for?** - [ ] A. To merge the final output files. - [x] B. To perform a local reduce operation on the output of a map task to reduce network traffic. - [ ] C. To combine multiple MapReduce jobs into a workflow. - [ ] D. To handle machine failures.
    
280. **Question 20: What do 'secondary keys' allow in MapReduce?** - [ ] A. Using multiple keys for the map output. - [x] B. Controlling the order in which values are presented to the reduce function for a given primary key. - [ ] C. Encrypting the intermediate data. - [ ] D. Combining map and reduce into a single function.
    

### Chapter 15: Web Search

281. **Question 1: Which feature, largely unique to Web IR, provides crucial structural information?** - [ ] A. Document length - [ ] B. Term frequency - [x] C. Hyperlinks between pages - [ ] D. Publication date
    
282. **Question 2: What is "spam" in the context of Web search?** - [ ] A. Unsolicited commercial email. - [x] B. Malicious pages designed to manipulate search engine rankings or deceive users. - [ ] C. Duplicate copies of legitimate Web pages. - [ ] D. Automatically generated query logs.
    
283. **Question 3: A Web crawler's primary function is to:** - [ ] A. Rank search results. - [ ] B. Process user queries. - [x] C. Discover and download Web pages to create a local snapshot for indexing. - [ ] D. Compress the search index.
    
284. **Question 4: The relationship between pages and links on the Web can be modeled as a:** - [ ] A. Relational database - [ ] B. B-Tree - [x] C. Web graph - [ ] D. Finite automaton
    
285. **Question 5: What is the difference between a static and a dynamic Web page?** - [ ] A. Static pages use HTML, dynamic pages use XML. - [x] B. Static pages have fixed content; dynamic pages are generated on demand, often based on parameters or database content. - [ ] C. Static pages are always more important than dynamic pages. - [ ] D. Static pages cannot contain links.
    
286. **Question 6: The "hidden Web" refers to pages that are:** - [ ] A. Encrypted for security. - [x] B. Not easily discoverable by crawlers (e.g., require login, database query, or have no incoming links). - [ ] C. Written in unsupported languages. - [ ] D. Stored offline.
    
287. **Question 7: The distribution of Web query frequencies typically follows:** - [ ] A. A normal distribution. - [ ] B. A uniform distribution. - [x] C. Zipf's Law (few very frequent queries, long tail of infrequent ones). - [ ] D. A Poisson distribution.
    
288. **Question 8: A query like "cnn" where the user seeks the main page of a specific known site is classified as:** - [ ] A. Informational - [ ] B. Transactional - [x] C. Navigational - [ ] D. Ambiguous
    
289. **Question 9: A query like "buy cheap flights to london" is best classified as:** - [ ] A. Informational - [x] B. Transactional - [ ] C. Navigational - [ ] D. Undirected
    
290. **Question 10: A "clickthrough curve" typically shows:** - [ ] A. The number of pages crawled per second. - [x] B. The distribution of clicks across different search result ranks for a specific query. - [ ] C. The growth of the Web over time. - [ ] D. The relationship between query length and relevance.
    
291. **Question 11: What is static rank (like PageRank)?** - [ ] A. A query-dependent score calculated at query time. - [x] B. A query-independent score assigned to pages during indexing, often based on link structure. - [ ] C. The rank of a page in a specific search result list. - [ ] D. A measure of how often a page is updated.
    
292. **Question 12: The basic idea behind PageRank is modeling a "random surfer" who:** - [ ] A. Always follows the link with the most descriptive anchor text. - [x] B. Randomly follows links from the current page or jumps to a random page in the collection. - [ ] C. Only visits pages bookmarked by the user. - [ ] D. Clicks on every link on a page before moving on.
    
293. **Question 13: In the PageRank formula, the damping factor δ represents:** - [ ] A. The probability of stopping the surf. - [x] B. The probability of following a link (as opposed to jumping). - [ ] C. The probability of jumping to a specific page. - [ ] D. The number of iterations needed for convergence.
    
294. **Question 14: What problem does the PageRank jump vector address?** - [ ] A. Pages with no incoming links (sources). - [x] B. Pages with no outgoing links (sinks) and disconnected graph components. - [ ] C. The slow convergence rate of the algorithm. - [ ] D. The large storage requirements of the link graph.
    
295. **Question 15: The HITS algorithm assigns two scores to each page:** - [ ] A. Static rank and dynamic rank - [x] B. Hub score and Authority score - [ ] C. In-degree and out-degree - [ ] D. Relevance score and novelty score
    
296. **Question 16: What is anchor text?** - [ ] A. The main text content of a Web page. - [ ] B. Text specifically marked as important using HTML tags. - [x] C. The visible, clickable text associated with a hyperlink. - [ ] D. Metadata describing the page's author.
    
297. **Question 17: Why is anchor text valuable for ranking?** - [ ] A. It is usually very short. - [x] B. It often provides a concise description of the target page's content, potentially using different terms than the target page itself. - [ ] C. It indicates the static rank of the source page. - [ ] D. It is guaranteed to be accurate and free of spam.
    
298. **Question 18: How does novelty/diversity influence Web search results?** - [ ] A. Search engines try to return only the single most relevant page. - [x] B. Results may be filtered to avoid showing too many pages from the same site or multiple near-duplicates. - [ ] C. Only novel (recently created) pages are included in the index. - [ ] D. Diversity measures are used instead of MAP for evaluation.
    
299. **Question 19: What are shingles used for?** - [ ] A. Calculating PageRank efficiently. - [x] B. Detecting near-duplicate Web pages by comparing sets of substrings. - [ ] C. Crawling the hidden Web. - [ ] D. Extracting anchor text from links.
    
300. **Question 20: Evaluating Web search often requires considering different user intents. Which task specifically evaluates the ability to find a single known page?** - [ ] A. Ad hoc retrieval - [ ] B. Filtering - [x] C. Named page finding - [ ] D. Query expansion
    

### Chapter 16: XML Retrieval

301. **Question 1: What is a key difference between XML retrieval and standard document retrieval?** - [ ] A. XML retrieval only works on very small collections. - [x] B. XML retrieval allows returning specific document components (elements) as results, not just whole documents. - [ ] C. XML documents cannot be indexed using inverted indices. - [ ] D. XML retrieval does not involve ranking.
    
302. **Question 2: What does XML stand for?** - [ ] A. Extended Meta Language - [ ] B. Examinable Markup Language - [ ] C. Executable Machine Language - [x] D. Extensible Markup Language
    
303. **Question 3: Unlike HTML (in practice), XML strictly enforces that elements must:** - [ ] A. Have unique IDs. - [x] B. Be properly nested without overlapping. - [ ] C. Contain only plain text. - [ ] D. Be defined in a DTD.
    
304. **Question 4: What is a Document Type Definition (DTD) used for?** - [ ] A. To define the visual presentation style of an XML document. - [x] B. To specify constraints on the structure and nesting of elements and attributes in an XML document. - [ ] C. To provide a query language for XML. - [ ] D. To store the actual content of the XML document.
    
305. **Question 5: Compared to DTDs, XML Schema offers:** - [ ] A. Simpler syntax. - [x] B. More powerful type system and constraints (e.g., specifying data types like integers, dates). - [ ] C. Faster parsing speed. - [ ] D. Compatibility with HTML.
    
306. **Question 6: XML documents are often viewed abstractly as what kind of data structure?** - [ ] A. A relational table - [ ] B. A linear sequence of tokens - [x] C. A tree - [ ] D. A directed acyclic graph
    
307. **Question 7: What is XPath primarily used for?** - [ ] A. Defining the structure of XML documents (like DTD or Schema). - [x] B. Specifying paths to select sets of nodes (elements, attributes) within an XML document. - [ ] C. Transforming XML documents into HTML for display. - [ ] D. Performing ranked retrieval over XML elements.
    
308. **Question 8: In XPath, what does the double slash "//" typically denote?** - [ ] A. A comment. - [ ] B. A direct child relationship. - [ ] C. The root of the document. - [x] D. The descendant-or-self axis (selecting nodes anywhere below the current context).
    
309. **Question 9: What limitation of XPath does the NEXI query language attempt to address?** - [ ] A. XPath cannot select attributes. - [x] B. XPath does not support selecting elements based on content (ranked retrieval). - [ ] C. XPath syntax is too complex. - [ ] D. XPath cannot handle recursive structures.
    
310. **Question 10: In NEXI, the `about()` function replaces XPath's `contains()` function to allow for:** - [ ] A. Exact phrase matching only. - [ ] B. Boolean operations between path segments. - [x] C. Content-based searching and ranking, rather than just exact string matching. - [ ] D. Selection based on element depth.
    
311. **Question 11: XQuery extends XPath primarily by adding facilities for:** - [ ] A. Defining document structure (like DTD). - [ ] B. Specifying stricter type checking. - [x] C. Manipulating and dynamically constructing XML output. - [ ] D. Handling non-XML data sources.
    
312. **Question 12: What does FLWOR stand for in XQuery?** - [ ] A. Find, List, Order, Wrap, Return - [x] B. For, Let, Where, Order by, Return - [ ] C. Follow, Link, Orient, Weight, Rank - [ ] D. Filter, Locate, Organize, Write, Report
    
313. **Question 13: To handle XML's recursive structure and parent/child relationships, the inverted index ADT is extended so postings include:** - [x] A. Start position, end position, and depth. - [ ] B. Term frequency and document frequency. - [ ] C. Relevance score and document ID. - [ ] D. Language and encoding information.
    
314. **Question 14: What is a "CO" (Content-Only) task in INEX?** - [x] A. Ranking XML elements based solely on their content, ignoring structure specified in the query. - [ ] B. Ranking XML elements based only on their structure, ignoring content. - [ ] C. Compressing only the content of XML documents. - [ ] D. Checking XML documents for conformance to a DTD.
    
315. **Question 15: What is a "CAS" (Content-And-Structure) task in INEX?** - [ ] A. Ranking XML elements based only on content. - [x] B. Ranking XML elements considering both the content relevance and the structural constraints specified in the query. - [ ] C. Casting XML elements to a different schema. - [ ] D. Compressing both content and structure.
    
316. **Question 16: A simple way to handle CAS queries involves:** - [ ] A. Ignoring the structure completely. - [x] B. Using the path expression as a filter first, then ranking the resulting elements based on content terms. - [ ] C. Building a completely different type of index (not inverted). - [ ] D. Ranking only based on structure.
    
317. **Question 17: What is the "overlap" problem in XML retrieval evaluation?** - [ ] A. Queries overlapping in their term content. - [ ] B. Index partitions overlapping on disk. - [x] C. The fact that a single piece of text can belong to multiple nested XML elements (e.g., paragraph within section within article). - [ ] D. Assessors having overlapping judgments.
    
318. **Question 18: Why are standard document ranking methods (like BM25) sometimes applied directly to XML elements?** - [x] A. It's often a simple and reasonably effective baseline approach. - [ ] B. XML elements are guaranteed to be independent. - [ ] C. This method explicitly handles overlap. - [ ] D. Specific XML ranking functions are too complex.
    
319. **Question 19: Why might global statistics like IDF need careful handling in XML retrieval when ranking elements?** - [ ] A. XML elements do not contain terms. - [x] B. Simply counting each element containing a term as a "document" inflates frequencies based on structure, not content distribution across base documents. - [ ] C. IDF is not applicable to XML data. - [ ] D. Global statistics cannot be pre-calculated.
    
320. **Question 20: What does INEX stand for?** - [ ] A. INdexing EXperiments - [ ] B. INternet EXploration - [x] C. Initiative for the Evaluation of XML Retrieval - [ ] D. INteractive EXamination
    

### Appendix A: Computer Performance

321. **Question 1: Why is understanding data locality (sequential vs. random access) important for IR system performance?** - [ ] A. It affects the choice of programming language. - [x] B. Accessing data sequentially is often vastly faster than random access, especially on disk. - [ ] C. Random access allows for better compression. - [ ] D. Sequential access uses less RAM.
    
322. **Question 2: What are the two main components of latency when accessing a random location on a hard disk drive?** - [ ] A. Read time and write time - [x] B. Seek latency and rotational latency - [ ] C. Transfer rate and cache latency - [ ] D. CPU time and I/O time
    
323. **Question 3: Seek latency on a hard drive refers to the time taken to:** - [ ] A. Spin the disk to the correct sector. - [ ] B. Transfer the data to memory. - [x] C. Position the read/write head over the correct track. - [ ] D. Check the disk for errors.
    
324. **Question 4: Rotational latency on a hard drive refers to the time taken to:** - [ ] A. Spin the disk up from a stopped state. - [x] B. Wait for the desired data sector to rotate under the read/write head. - [ ] C. Move the read/write head across tracks. - [ ] D. Cache the data being read.
    
325. **Question 5: Compared to disk, random access latency in main memory (RAM) is:** - [ ] A. Significantly higher (slower). - [ ] B. Roughly the same. - [x] C. Significantly lower (faster), by orders of magnitude. - [ ] D. Dependent on the size of the data block.
    
326. **Question 6: Even in RAM, why is sequential access generally faster than random access?** - [ ] A. RAM chips are physically arranged for sequential reads. - [ ] B. Random access requires error checking. - [x] C. Caching mechanisms (data cache, TLB) benefit greatly from spatial and temporal locality found in sequential access patterns. - [ ] D. Sequential access uses less power.
    
327. **Question 7: What is the purpose of a data cache (L1, L2, etc.)?** - [ ] A. To store the entire operating system. - [x] B. To hold frequently or recently used data closer to the CPU for faster access than main memory. - [ ] C. To translate virtual addresses to physical addresses. - [ ] D. To store data permanently when the power is off.
    
328. **Question 8: What does a Translation Lookaside Buffer (TLB) cache?** - [ ] A. Recently executed instructions. - [ ] B. Data read from disk. - [x] C. Recently used virtual-to-physical address translations from the page table. - [ ] D. Frequently accessed dictionary terms.
    
329. **Question 9: A cache miss (data or TLB) results in:** - [ ] A. Faster execution speed. - [x] B. A significant performance penalty due to fetching data from a slower level of memory. - [ ] C. Data corruption. - [ ] D. Automatic compression of the requested data.
    
330. **Question 10: Pipelined execution in a CPU allows:** - [ ] A. Multiple cores to work on the same instruction. - [x] B. Different stages of multiple instructions to execute concurrently, increasing throughput. - [ ] C. Instructions to be executed out of order always. - [ ] D. The CPU clock speed to be dynamically increased.
    
331. **Question 11: What is a major challenge for pipelined execution?** - [ ] A. Lack of sufficient registers. - [x] B. Handling branch instructions, where the next instruction's address isn't known immediately. - [ ] C. Power consumption. - [ ] D. Cooling the CPU.
    
332. **Question 12: What is branch prediction?** - [x] A. A technique to predict the outcome (taken/not taken) of a branch instruction to keep the pipeline full. - [ ] B. A compiler optimization to remove branches. - [ ] C. A way to execute both paths of a branch simultaneously. - [ ] D. A method for debugging branch instructions.
    
333. **Question 13: What happens on a branch misprediction?** - [ ] A. The CPU executes the wrong instruction, causing a program crash. - [x] B. The work done on speculatively executed instructions must be discarded, and the pipeline refilled, causing a stall. - [ ] C. The branch instruction is skipped entirely. - [ ] D. The CPU automatically corrects the prediction for future use.
    
334. **Question 14: Why might bit-by-bit decoding of variable-length codes (like gamma codes) be inefficient on modern CPUs?** - [ ] A. CPUs cannot perform bitwise operations. - [ ] B. Variable-length codes are too complex. - [x] C. The frequent conditional checks involved can lead to high branch misprediction rates. - [ ] D. The codes require floating-point arithmetic.
    
335. **Question 15: Table-driven decoding improves performance primarily by:** - [ ] A. Using better compression algorithms. - [x] B. Reducing the number of conditional branches and potential mispredictions. - [ ] C. Accessing disk more efficiently. - [ ] D. Requiring less RAM.
    
336. **Question 16: According to Table A.1, random access on the sample system's disk is roughly how much slower than random access in RAM?** - [ ] A. 2 times slower - [ ] B. 100 times slower - [ ] C. 1,000 times slower - [x] D. 500,000 times slower (12.8 ms vs 75 ns)
    
337. **Question 17: According to Table A.1, sequential throughput in RAM is roughly how much faster than sequential throughput on disk (RAID-0)?** - [ ] A. 2 times faster - [ ] B. 10 times faster - [x] C. 40 times faster (3700 MB/s vs 87.4 MB/s) - [ ] D. 500 times faster
    
338. **Question 18: The difference between sequential and random disk access is primarily due to:** - [ ] A. CPU speed - [ ] B. RAM speed - [x] C. Seek and rotational latency - [ ] D. Network bandwidth
    
339. **Question 19: Why is optimizing for cache performance (data and TLB) important for in-memory IR operations?** - [ ] A. Cache is the largest component of memory. - [x] B. Cache misses are extremely costly compared to CPU cycle times. - [ ] C. Disk access speed depends on cache hits. - [ ] D. Cache is used for permanent storage.
    
340. **Question 20: Which IR operation discussed in the book heavily relies on random memory access and benefits from cache-aware data structures?** - [ ] A. Sequential scanning of postings lists. - [ ] B. Merge phase of index construction. - [x] C. Binary search in a large in-memory dictionary. - [ ] D. Applying stopword lists










## TMG301
1. What is the primary goal of Text Classification?
    - [ ] A. To summarize long text documents into shorter versions.
    - [ ] B. To translate text from one language to another.
    - [x] C. To categorize or assign predefined labels to text documents based on their content.
    - [ ] D. To generate new text based on a given prompt.
2. What core assumption does Naive Bayes make in the context of text classification?
    - [ ] A. That the presence of all words in a document is dependent on each other.
    - [x] B. That the presence of a particular word in a document is independent of the presence of other words.
    - [ ] C. That documents must be converted into images before classification.
    - [ ] D. That only the first and last words of a document are important for classification.
3. Which of the following is mentioned as a direct application (relevance) of Text Classification?
    - [ ] A. Image generation
    - [ ] B. Speech synthesis
    - [x] C. Spam Detection
    - [ ] D. Database optimization
4. According to the slides, what does 'Precision' quantify in evaluation metrics?
    - [ ] A. The ratio of correctly predicted positive instances to all actual positive instances.
    - [ ] B. The proportion of correctly classified instances out of the total instances.
    - [ ] C. The harmonic mean of precision and recall.
    - [x] D. The ratio of correctly predicted positive instances to all instances predicted as positive.
5. What is the F1-Score defined as in the evaluation metrics?
    - [ ] A. The average of precision and recall.
    - [ ] B. The geometric mean of precision and recall.
    - [x] C. The harmonic mean of precision and recall.
    - [ ] D. The total number of correct predictions divided by the total instances.
6. For which type of classification problem is Logistic Regression particularly suited?
    - [ ] A. Multi-class classification with many categories.
    - [ ] B. Regression problems predicting continuous values.
    - [x] C. Binary classification problems where the dependent variable has two possible outcomes.
    - [ ] D. Clustering problems with unstructured data.
7. What is the primary role of the Sigmoid function in Logistic Regression?
    - [ ] A. To perform feature scaling between 0 and 1.
    - [ ] B. To calculate the linear equation's coefficients.
    - [x] C. To transform the linear equation's output into a probability between 0 and 1.
    - [ ] D. To measure the accuracy of the classification.
8. What is the main purpose of using Regularization in Logistic Regression?
    - [ ] A. To increase the complexity of the model.
    - [ ] B. To speed up the training process significantly.
    - [x] C. To prevent overfitting by penalizing large coefficient values.
    - [ ] D. To ensure the output is always exactly 0 or 1.
9. What is a key characteristic of L1 Regularization (Lasso)?
    - [ ] A. It adds the squared values of coefficients as a penalty.
    - [x] B. It encourages some coefficients to become exactly zero, performing feature selection.
    - [ ] C. It always results in better accuracy than L2 regularization.
    - [ ] D. It makes the model less sensitive to the learning rate.
10. What does Vector Semantics aim to represent?
    - [ ] A. The grammatical structure of sentences using trees.
    - [x] B. Words or phrases as numerical vectors capturing semantic relationships.
    - [ ] C. The frequency of words in a document.
    - [ ] D. The rules for combining words into valid sentences.
11. What are Word Embeddings derived from, according to the slides?
    - [ ] A. Context-Free Grammars
    - [ ] B. Rule-based systems
    - [x] C. Vector semantics
    - [ ] D. Decision trees
12. The analogy "king - man + woman = queen" is used as an example of what capability of word embeddings?
    - [ ] A. Capturing only syntactic relationships.
    - [ ] B. Identifying spelling errors.
    - [x] C. Excelling at grasping intricate word connections and analogies through vector manipulation.
    - [ ] D. Performing image recognition based on text descriptions.
13. What is the central idea behind Distributed Representation in word embeddings?
    - [ ] A. Each word is represented by a single, unique number.
    - [x] B. Words are represented as vectors where each dimension encodes a unique semantic trait.
    - [ ] C. Words are stored in a distributed database system.
    - [ ] D. Only the most frequent words get a vector representation.
14. Which technique learns embeddings by predicting context words from a target word (Skip-gram) or vice versa (CBOW)?
    - [ ] A. GloVe
    - [ ] B. FastText
    - [x] C. Word2Vec
    - [ ] D. TF-IDF
15. What is the fundamental goal of clustering?
    - [ ] A. To classify data points into predefined labeled categories.
    - [x] B. To find natural groupings or patterns within a dataset based on similarity.
    - [ ] C. To predict a continuous value for each data point.
    - [ ] D. To reduce the dimensionality of the data.
16. Which method is commonly used to represent text documents as numerical vectors for clustering?
    - [ ] A. One-Hot Encoding
    - [x] B. Term Frequency-Inverse Document Frequency (TF-IDF) or Word Embeddings
    - [ ] C. Bag of Characters
    - [ ] D. Principal Component Analysis (PCA) directly on text
17. What does Cosine Similarity measure in the context of text similarity?
    - [ ] A. The Euclidean distance between two vectors.
    - [ ] B. The number of common words between two documents.
    - [x] C. The cosine of the angle between two vectors, indicating orientation similarity.
    - [ ] D. The difference in length between two document vectors.
18. What is the first step in the basic K-Means algorithm?
    - [ ] A. Assign data points to the nearest centroid.
    - [ ] B. Update the centroids based on assigned points.
    - [x] C. Choose the number of clusters (K).
    - [ ] D. Calculate the pairwise distance between all data points.
19. Agglomerative Hierarchical Clustering follows which approach?
    - [ ] A. Top-Down: Starts with one cluster and recursively splits it.
    - [x] B. Bottom-Up: Starts with individual points as clusters and iteratively merges them.
    - [ ] C. Centroid-Based: Finds K centroids and assigns points.
    - [ ] D. Density-Based: Groups points based on density reachability.
20. What is a key advantage of DBSCAN clustering?
    - [ ] A. It requires the number of clusters to be specified beforehand.
    - [x] B. It can discover clusters of arbitrary shapes and handle noise.
    - [ ] C. It assumes clusters are spherical and equally sized.
    - [ ] D. It is computationally faster than K-Means for all datasets.
21. What is the purpose of Stop Word Removal in text pre-processing?
    - [ ] A. To remove misspelled words.
    - [ ] B. To remove rare words.
    - [x] C. To remove common words (like "the", "is", "and") that don't carry much specific meaning.
    - [ ] D. To convert words to their base or root form.
22. What mechanism allows Transformers to handle sequential data without relying on recurrence like RNNs?
    - [ ] A. Convolutional layers
    - [ ] B. Max-pooling layers
    - [x] C. Self-attention mechanism
    - [ ] D. Explicit state-passing cells
23. Which component in the Transformer architecture allows a word to consider the importance of other words in the same sequence, regardless of distance?
    - [ ] A. Feedforward Neural Network
    - [ ] B. Positional Encoding
    - [x] C. Self-Attention Mechanism
    - [ ] D. Encoder-Decoder Stacking
24. Why are Positional Encodings added to the input embeddings in Transformers?
    - [ ] A. To increase the dimensionality of the embeddings.
    - [ ] B. To normalize the embedding values.
    - [x] C. To provide the model with information about the position of words, as it lacks inherent sequence processing.
    - [ ] D. To add semantic information from a lexicon.
25. What defines a Pre-Trained Language Model?
    - [ ] A. Models trained only on task-specific data.
    - [x] B. Neural network models trained on massive text data before being fine-tuned for specific tasks.
    - [ ] C. Rule-based systems derived from linguistic expertise.
    - [ ] D. Simple lexicon lookup tables.
26. Which model, introduced by Google, was a breakthrough pre-trained model known for its bidirectional contextual understanding?
    - [ ] A. GPT-3
    - [ ] B. Word2Vec
    - [x] C. BERT
    - [ ] D. ELMo
27. What are Chatbots, according to the definition provided?
    - [ ] A. Hardware devices for communication.
    - [ ] B. Database management systems.
    - [x] C. Computer programs designed to simulate human conversation.
    - [ ] D. Graphical user interface design tools.
28. Which type of dialogue system is designed to assist users in achieving specific objectives or tasks, like booking flights?
    - [ ] A. Open-Domain Dialogue Systems
    - [x] B. Task-Oriented Dialogue Systems
    - [ ] C. Hybrid Dialogue Systems
    - [ ] D. Generative Dialogue Systems
29. Which component of a dialogue system is responsible for interpreting and extracting meaning from user inputs (text or speech)?
    - [ ] A. Natural Language Generation (NLG)
    - [ ] B. Dialogue Management (DM)
    - [ ] C. Backend Knowledge Provider
    - [x] D. Natural Language Understanding (NLU)
30. What is the role of Natural Language Generation (NLG) in a dialogue system?
    - [ ] A. To understand the user's intent.
    - [ ] B. To track the conversation state.
    - [x] C. To generate human-like responses in natural language.
    - [ ] D. To connect to external databases.
31. What are Context-Free Grammars (CFG) used for?
    - [ ] A. To describe the semantics (meaning) of words.
    - [x] B. To provide a formal framework for describing the syntax (structure) of languages.
    - [ ] C. To perform sentiment analysis on text.
    - [ ] D. To translate text between languages.
32. In a CFG, what are 'Terminals'?
    - [ ] A. Symbols representing categories like NounPhrase or VerbPhrase.
    - [ ] B. The rules used for generating strings.
    - [x] C. The actual words or symbols that make up the language (the leaves of a parse tree).
    - [ ] D. The start symbol of the grammar.
33. What does Constituency Parsing aim to determine?
    - [ ] A. The sentiment polarity of a sentence.
    - [ ] B. The dependencies between individual words.
    - [x] C. The hierarchical syntactic structure of a sentence into phrases (constituents).
    - [ ] D. The topic of a document.
34. What does ambiguity in the context of CFGs and parse trees refer to?
    - [ ] A. A sentence having spelling errors.
    - [ ] B. A sentence that cannot be parsed by the grammar.
    - [x] C. A situation where a single sentence can be parsed into multiple valid syntactic structures.
    - [ ] D. A grammar that uses too many non-terminal symbols.
35. How does Top-Down Parsing typically start?
    - [ ] A. From the input tokens (words) of the sentence.
    - [ ] B. From the middle of the sentence.
    - [x] C. From the root of the parse tree (the start symbol of the CFG).
    - [ ] D. By building a chart of all possible constituents.
36. What are the two main actions performed by a Shift-Reduce (Bottom-Up) parser?
    - [ ] A. Start and End
    - [ ] B. Read and Write
    - [x] C. Shift and Reduce
    - [ ] D. Expand and Match
37. What is the core process involved in Dependency Parsing?
    - [ ] A. Grouping sentences into paragraphs based on topic.
    - [ ] B. Identifying the hierarchical constituent structure (phrases).
    - [x] C. Analyzing grammatical structure by identifying relationships (dependencies) between words.
    - [ ] D. Converting text into speech.
38. How are sentence structures typically represented in Dependency Parsing?
    - [ ] A. As a flat list of words.
    - [ ] B. As a constituency-based parse tree.
    - [x] C. As a directed graph called a dependency tree, showing head-dependent relations.
    - [ ] D. As a sequence of POS tags only.
39. What distinguishes Non-Projective Dependency Parsing from Projective Parsing?
    - [ ] A. Non-projective parsing only works for short sentences.
    - [ ] B. Non-projective parsing does not use dependency labels.
    - [x] C. Non-projective parsing allows dependency edges to cross, capturing more complex structures.
    - [ ] D. Projective parsing is always more accurate.
40. Transition-based dependency parsing treats the parsing process as:
    - [ ] A. A graph optimization problem.
    - [x] B. A sequence of actions (transitions) applied to a parsing state.
    - [ ] C. A rule-matching process based on CFG.
    - [ ] D. A statistical calculation of word co-occurrence.
41. Graph-based dependency parsing views the task as:
    - [ ] A. Applying a sequence of shift/reduce actions.
    - [ ] B. Building a constituency tree layer by layer.
    - [x] C. Finding the best possible graph structure via an optimization process.
    - [ ] D. Translating the sentence into a logical form.
42. What does the Unlabeled Attachment Score (UAS) measure in dependency parsing evaluation?
    - [ ] A. The percentage of correctly labeled dependency relations.
    - [ ] B. The percentage of correctly identified root words.
    - [ ] C. The overall F1-score of the parsing task.
    - [x] D. The percentage of words that are correctly attached to their predicted head, ignoring the label.
43. What is the primary purpose of using Logical Representations for sentence meaning?
    - [ ] A. To make sentences sound more natural when spoken by a machine.
    - [x] B. To capture the meaning of sentences in a precise, structured, and unambiguous formal way.
    - [ ] C. To count the number of words and characters in a sentence.
    - [ ] D. To generate visually appealing diagrams of sentences.
44. What key element does First-Order Logic add compared to Propositional Logic, enhancing its expressive power?
    - [ ] A. Logical connectives like AND, OR, NOT.
    - [ ] B. Truth values (True/False).
    - [x] C. Quantifiers (like "for all", "there exists") and predicate symbols for objects and relations.
    - [ ] D. The ability to represent only simple, atomic statements.
45. What does the lambda (λ) notation in Lambda Calculus typically represent?
    - [ ] A. A variable constant.
    - [ ] B. A logical connective.
    - [x] C. A function abstraction (defining a function).
    - [ ] D. A quantified statement.
46. What is the main goal of Montague Grammar?
    - [ ] A. To simplify natural language into basic components.
    - [x] B. To provide a framework connecting the syntax of natural language directly to formal logic representations.
    - [ ] C. To create faster algorithms for parsing.
    - [ ] D. To develop new programming languages based on logic.
47. The principle that the meaning of a complex expression (like a sentence) is derived from the meanings of its parts and how they are combined is known as:
    - [ ] A. Ambiguity Resolution
    - [ ] B. Syntactic Parsing
    - [x] C. Compositional Semantics
    - [ ] D. Lexical Analysis
48. What is Semantic Parsing?
    - [ ] A. Parsing based only on the grammatical structure (syntax).
    - [x] B. The task of converting natural language sentences into formal meaning representations (like logical forms).
    - [ ] C. Identifying the parts of speech for each word.
    - [ ] D. Grouping sentences into topics.
49. Temporal reasoning in text mining primarily involves:
    - [ ] A. Analyzing the sentiment expressed over time.
    - [x] B. Identifying and reasoning about temporal information like dates, durations, and event sequences.
    - [ ] C. Correcting grammatical errors related to tense.
    - [ ] D. Translating time expressions into different languages.
50. What is Temporal Entity Recognition focused on?
    - [ ] A. Recognizing named entities like people and organizations.
    - [x] B. Identifying temporal expressions such as dates, times, durations, and specific events in text.
    - [ ] C. Understanding the coreference between different temporal phrases.
    - [ ] D. Normalizing different calendar systems.
51. Temporal Expression Normalization is the process of:
    - [ ] A. Identifying all temporal words in a text.
    - [x] B. Converting diverse date and time formats into a single, standardized representation.
    - [ ] C. Ordering events chronologically.
    - [ ] D. Calculating the duration between two time points.
52. How does temporal reasoning primarily contribute to Trend Analysis?
    - [ ] A. By improving the grammar of the analysis report.
    - [x] B. By identifying patterns, cycles, and changes in data over time.
    - [ ] C. By summarizing the key findings concisely.
    - [ ] D. By translating the trends into different languages.
53. In text summarization, what does temporal reasoning help maintain?
    - [ ] A. The exact word count of the original text.
    - [ ] B. The thematic consistency of the summary.
    - [x] C. Contextual relevance and correct chronological order of events.
    - [ ] D. The reading difficulty level of the summary.
54. What are 'word senses'?
    - [ ] A. The emotional connotation of a word.
    - [x] B. The different meanings a single word can have depending on the context.
    - [ ] C. The grammatical category (part of speech) of a word.
    - [ ] D. The frequency of a word in a corpus.
55. What is WordNet?
    - [ ] A. A spell-checking tool.
    - [ ] B. A machine translation service.
    - [x] C. A large lexical database organizing words into synonym sets (synsets) based on meanings.
    - [ ] D. A type of neural network architecture.
56. The groups of synonymous words in WordNet that share a common meaning are called:
    - [ ] A. Hyponyms
    - [ ] B. Meronyms
    - [ ] C. Antonyms
    - [x] D. Synsets
57. In WordNet, if "rose" is a specific type of "flower", what is the relationship term for "rose" relative to "flower"?
    - [ ] A. Hypernym
    - [x] B. Hyponym
    - [ ] C. Meronym
    - [ ] D. Holonym
58. What is the goal of Word Sense Disambiguation (WSD)?
    - [ ] A. To correct spelling errors in text.
    - [x] B. To determine the correct meaning (sense) of a word in its specific context.
    - [ ] C. To translate words into different languages.
    - [ ] D. To identify the part of speech of a word.
59. Sentiment Lexicons primarily assign what kind of label or score to words/phrases?
    - [ ] A. A score based on word frequency.
    - [ ] B. A label indicating grammatical function.
    - [x] C. A polarity label/score (positive, negative, neutral).
    - [ ] D. A score indicating the complexity of the word.
60. How do Connotation Lexicons differ from basic Sentiment Lexicons?
    - [ ] A. They only contain positive words.
    - [ ] B. They are smaller and less comprehensive.
    - [x] C. They capture more nuanced emotional, associative, or cultural meanings beyond simple positive/negative polarity.
    - [ ] D. They are only used for non-English languages.
61. Which of the following is presented as a sentiment lexicon specifically designed to handle social media text, including rules for intensifiers and emoticons?
    - [ ] A. AFINN
    - [ ] B. SentiWordNet
    - [ ] C. WordNet
    - [x] D. VADER
62. Which lexicon aims to capture emotional dimensions like valence, arousal, and dominance associated with words?
    - [ ] A. VADER
    - [ ] B. NRC Emotion Lexicon
    - [x] C. ANEW (Affective Norms for English Words)
    - [ ] D. SentiWordNet
63. What is a common characteristic of 'Hybrid Approaches' in sentiment analysis involving lexicons?
    - [ ] A. They rely solely on lexicon lookups without machine learning.
    - [x] B. They combine lexicon-based features with other features in a machine learning model.
    - [ ] C. They use machine learning only to create the lexicons.
    - [ ] D. They ignore sentiment lexicons entirely.
64. Sentiment Analysis is often considered a specific type of which broader task?
    - [ ] A. Machine Translation
    - [ ] B. Text Summarization
    - [x] C. Text Classification
    - [ ] D. Information Retrieval
65. In the context of Naive Bayes for text, what does the "Bag-of-Words" model representation typically ignore?
    - [ ] A. The frequency of words
    - [x] B. The order of words in the document
    - [ ] C. The presence of specific keywords
    - [ ] D. The overall length of the document
66. When is accuracy potentially a misleading evaluation metric for classification?
    - [ ] A. When the dataset is very large.
    - [ ] B. When the dataset has many features.
    - [x] C. When the dataset is imbalanced (one class dominates).
    - [ ] D. When the model is very complex.
67. What does a Confusion Matrix provide insight into?
    - [ ] A. The computational complexity of the model.
    - [ ] B. The optimal hyperparameters for the model.
    - [x] C. True positives, true negatives, false positives, and false negatives.
    - [ ] D. The correlation between different features.
68. The core equation in Logistic Regression involves applying the sigmoid function to what?
    - [ ] A. The raw input features directly.
    - [x] B. A linear combination of the input features and coefficients (log-odds).
    - [ ] C. The F1-score of the previous iteration.
    - [ ] D. The class labels.
69. The process of finding the optimal coefficients in Logistic Regression often involves minimizing a loss function (like binary cross-entropy) using techniques such as:
    - [ ] A. Random guessing
    - [ ] B. K-Means clustering
    - [ ] C. Principal Component Analysis (PCA)
    - [x] D. Gradient Descent
70. What determines the Decision Boundary in Logistic Regression?
    - [ ] A. The number of data points in the training set.
    - [x] B. The model's learned coefficients and intercept.
    - [ ] C. The learning rate used during training.
    - [ ] D. The type of regularization applied (L1 or L2).
71. While L1 regularization can drive coefficients to zero, what is the primary effect of L2 Regularization (Ridge)?
    - [ ] A. It forces all coefficients to be positive.
    - [x] B. It significantly reduces the magnitude of coefficients, shrinking them towards zero but not necessarily making them exactly zero.
    - [ ] C. It increases the number of features used by the model.
    - [ ] D. It has no effect on the coefficients.
72. How are semantic relationships typically captured in vector space models (Vector Semantics)?
    - [ ] A. By the alphabetical order of the words.
    - [ ] B. By the length of the vectors.
    - [x] C. By the proximity (distance) and orientation (angle) between word vectors.
    - [ ] D. By assigning prime numbers to each word.
73. One significant limitation of traditional word embeddings (like Word2Vec, GloVe) mentioned is their difficulty handling:
    - [ ] A. Very short words.
    - [x] B. Words with multiple meanings depending on context (Polysemy).
    - [ ] C. Only nouns and verbs.
    - [ ] D. Sentences written in all capital letters.
74. Which word embedding technique explicitly uses global corpus statistics (word co-occurrence matrix)?
    - [ ] A. Word2Vec (CBOW)
    - [ ] B. Word2Vec (Skip-gram)
    - [x] C. GloVe
    - [ ] D. FastText
75. FastText represents words based on what, allowing it to generate embeddings for out-of-vocabulary words?
    - [ ] A. Their position in the sentence.
    - [ ] B. Their sentiment score.
    - [x] C. Character n-grams.
    - [ ] D. Their frequency rank in the corpus.
76. What is the role of 'linkage methods' (e.g., Ward, average, complete) in Hierarchical Clustering?
    - [ ] A. To determine the number of clusters (K).
    - [ ] B. To initialize the cluster centroids.
    - [x] C. To define how the distance between clusters (not just points) is calculated during merging/splitting.
    - [ ] D. To represent the final clusters as a graph.
77. In DBSCAN, what defines a 'core point'?
    - [ ] A. A point that is far away from all other points.
    - [x] B. A point with at least 'minPts' neighbors within the 'eps' radius.
    - [ ] C. A point that belongs to exactly two clusters.
    - [ ] D. The point closest to the geometric center of the dataset.
78. Stemming and Lemmatization are pre-processing techniques aimed at:
    - [ ] A. Correcting spelling errors.
    - [x] B. Reducing words to their base or root form to treat variations as the same token.
    - [ ] C. Removing punctuation marks.
    - [ ] D. Calculating TF-IDF scores.
79. What is the purpose of the 'Multi-Head Attention' mechanism in Transformers?
    - [ ] A. To process multiple sentences simultaneously.
    - [x] B. To allow the model to jointly attend to information from different representation subspaces at different positions.
    - [ ] C. To handle multiple languages within one model.
    - [ ] D. To reduce the number of parameters in the model.
80. What is the key difference between the Encoder and Decoder stacks in the standard Transformer architecture?
    - [ ] A. The Encoder uses self-attention, while the Decoder does not.
    - [x] B. The Decoder has an additional attention mechanism that attends to the Encoder's output.
    - [ ] C. The Encoder processes text, while the Decoder processes images.
    - [ ] D. The Decoder uses RNN cells, while the Encoder uses feedforward networks.
81. What does 'fine-tuning' typically involve in the context of pre-trained language models?
    - [ ] A. Training the model from scratch on a large dataset.
    - [x] B. Further training a pre-trained model on a smaller, task-specific dataset.
    - [ ] C. Manually adjusting the model's weights.
    - [ ] D. Removing layers from the pre-trained model.
82. Open-Domain Dialogue Systems are characterized by their ability to:
    - [ ] A. Only perform specific, predefined tasks.
    - [x] B. Engage in general, open-ended conversations on a wide range of topics.
    - [ ] C. Understand only numerical inputs.
    - [ ] D. Operate without needing Natural Language Understanding.
83. Intent Recognition and Entity Extraction are key sub-tasks within which component of a dialogue system?
    - [ ] A. Natural Language Generation (NLG)
    - [ ] B. Dialogue Management (DM)
    - [x] C. Natural Language Understanding (NLU)
    - [ ] D. Speech Synthesis
84. Tracking the dialogue state (what has been said, what the user wants, etc.) is the primary responsibility of which component?
    - [ ] A. Natural Language Understanding (NLU)
    - [ ] B. Natural Language Generation (NLG)
    - [x] C. Dialogue Management (DM)
    - [ ] D. Backend Database
85. In CFG rules like NP -> Det N, what are NP, Det, and N examples of?
    - [ ] A. All are Terminals.
    - [ ] B. NP is a Terminal, Det and N are Non-Terminals.
    - [ ] C. All are Non-Terminals (representing categories).
    - [x] D. NP is a Non-Terminal, Det and N could be Non-Terminals or Terminals depending on further rules.
86. A Parse Tree visually represents:
    - [ ] A. The semantic dependencies between words.
    - [ ] B. The sequence of dialogue turns.
    - [x] C. The hierarchical constituent structure of a sentence according to a CFG.
    - [ ] D. The flow of information in a neural network.
87. The CYK (Cocke-Younger-Kasami) parsing algorithm is particularly well-suited for grammars in which form?
    - [ ] A. Regular Grammar
    - [ ] B. Unrestricted Grammar
    - [x] C. Chomsky Normal Form (CNF)
    - [ ] D. Dependency Grammar
88. What fundamental aspect of sentence structure does Dependency Parsing focus on, unlike Constituency Parsing?
    - [ ] A. Hierarchical phrase structures (NPs, VPs).
    - [ ] B. Word order and sentence length.
    - [x] C. Head-dependent relationships between individual words.
    - [ ] D. The overall sentiment of the sentence.
89. In a dependency relation like nsubj(chased, cat), which word is the 'head' (or governor)?
    - [ ] A. cat
    - [x] B. chased
    - [ ] C. nsubj
    - [ ] D. There is no head in this notation.
90. What does it mean if a dependency parse is 'projective'?
    - [ ] A. The dependency edges cross each other.
    - [x] B. The dependency edges, when drawn above the sentence, do not cross.
    - [ ] C. The parse uses probabilities.
    - [ ] D. The parse only identifies subject-verb-object relations.
91. Propositional Logic deals with propositions (statements that are true/false) and connectives, but lacks the ability to represent:
    - [ ] A. Negation (NOT).
    - [ ] B. Conjunction (AND).
    - [x] C. Relationships between objects or quantification over objects (like "all" or "some").
    - [ ] D. Disjunction (OR).
92. Semantic Parsing aims to convert natural language into:
    - [ ] A. A simplified version of the same natural language.
    - [x] B. A formal meaning representation (e.g., logical form, database query).
    - [ ] C. A dependency parse tree.
    - [ ] D. A summary of the text.
93. Understanding phrases like "next Tuesday" or "two weeks ago" involves which aspect of temporal reasoning?
    - [ ] A. Explicit date/time mentions.
    - [x] B. Relative temporal references and expression normalization.
    - [ ] C. Event duration calculation only.
    - [ ] D. Identifying seasonal trends.
94. The relationship where "car" is the whole entity containing the part "wheel" is called:
    - [ ] A. Hyponymy
    - [ ] B. Antonymy
    - [ ] C. Meronymy
    - [x] D. Holonymy
95. Identifying that "bank" refers to a financial institution in "I need to deposit this check at the bank" is an example of:
    - [ ] A. Syntactic Parsing
    - [x] B. Word Sense Disambiguation (WSD)
    - [ ] C. Part-of-Speech Tagging
    - [ ] D. Text Summarization
96. What is a key difference in the type of information provided by SentiWordNet compared to AFINN?
    - [ ] A. AFINN provides scores per sense (synset), while SentiWordNet provides one score per word.
    - [x] B. SentiWordNet provides positive, negative, and objective scores per synset (sense), while AFINN provides a single polarity score per word/phrase.
    - [ ] C. SentiWordNet only includes verbs, while AFINN includes all word types.
    - [ ] D. AFINN is rule-based, while SentiWordNet is based on human intuition only.
97. How does the fundamental approach of Graph-based Dependency Parsing differ from Transition-based Dependency Parsing in terms of decision-making?
    - [ ] A. Graph-based makes sequential decisions, while Transition-based optimizes globally.
    - [x] B. Graph-based seeks the best overall tree structure using global optimization, while Transition-based makes a sequence of locally optimal decisions (actions).
    - [ ] C. Both methods rely solely on predefined grammatical rules without optimization.
    - [ ] D. Transition-based focuses on edge labels, while Graph-based focuses only on attachments.
98. Why is Non-Projective Dependency Parsing particularly important for analyzing certain types of sentences or languages, which Projective Parsing might fail to capture accurately?
    - [ ] A. Because non-projective parsing is computationally faster.
    - [x] B. Because it can handle crossing dependencies often found in languages with more flexible word order or constructions like center embedding.
    - [ ] C. Because non-projective parsing requires less training data.
    - [ ] D. Because projective parsing cannot identify the root of the sentence.
99. What limitation of Propositional Logic necessitates the use of First-Order Logic (FOL) for representing the meaning of sentences like "All humans are mortal"?
    - [ ] A. Propositional Logic cannot use logical connectives like AND or OR.
    - [x] B. Propositional Logic cannot represent the concepts of "all" (universal quantification) or properties/relationships of objects (predicates like `human(x)` or `mortal(x)`).
    - [ ] C. Propositional Logic can only represent false statements.
    - [ ] D. First-Order Logic is simply a different notation for Propositional Logic.
100. How does the concept of 'Compositional Semantics' form a foundational principle for frameworks like Montague Grammar?

- [ ] A. It states that sentence meaning is independent of the meaning of its words.
- [x] B. It provides the basis for Montague Grammar's approach, where the meaning of a sentence is derived systematically (e.g., via function application) from the meanings of its parts and their syntactic structure.
- [ ] C. It focuses only on the order of words, ignoring their individual meanings.
- [ ] D. It suggests that logical representations are unnecessary for understanding language.

101. Semantic Parsing aims to convert natural language to a formal representation. Why is this task inherently challenging due to the nature of natural language itself?

- [ ] A. Because formal representations are always shorter than natural language.
- [ ] B. Because natural language lacks any grammatical structure.
- [x] C. Because natural language exhibits significant ambiguity (word sense, syntax) and variability (different phrasings for the same meaning), which formal representations aim to eliminate.
- [ ] D. Because computers cannot process symbols used in formal logic.

102. Considering Temporal Reasoning, how do 'Implicit Temporal Relationships' (e.g., "She graduated before her brother") differ from 'Temporal Conjunctions' (e.g., "She left _after_ breakfast") in how they signal event order?

- [ ] A. Implicit relationships require explicit date mentions, while conjunctions do not.
- [x] B. Implicit relationships rely on contextual understanding and world knowledge to infer order, whereas temporal conjunctions provide explicit linguistic markers for the relationship (like 'before', 'after').
- [ ] C. Temporal conjunctions only relate events happening simultaneously.
- [ ] D. Implicit relationships can only express durations, not sequences.

103. Why is Temporal Expression Normalization a crucial _prerequisite_ for many Temporal Reasoning tasks, such as trend analysis or comparing event timelines?

- [ ] A. Because it converts all times to the local time zone.
- [ ] B. Because it eliminates the need for Temporal Entity Recognition.
- [x] C. Because it provides a consistent, standardized format for diverse temporal expressions (e.g., "Jan 1", "1/1", "First of Jan"), allowing for reliable comparison, aggregation, and analysis.
- [ ] D. Because normalization assigns a sentiment score to each temporal expression.

104. In the context of Text Summarization, what specific problem does maintaining 'Chronological Order' via temporal reasoning solve for the reader?

- [ ] A. It ensures the summary uses complex vocabulary.
- [ ] B. It prevents the summary from being too long.
- [x] C. It ensures the reader can understand the progression of events or actions as they occurred in time, making the narrative coherent and logical.
- [ ] D. It guarantees that only the most recent event is included in the summary.

105. While both Syntactic Dependency Parsing and Temporal Dependency Parsing analyze relationships between words/events, what is the primary _focus_ that distinguishes Temporal Dependency Parsing?

- [ ] A. Temporal DP focuses only on grammatical correctness, ignoring meaning.
- [x] B. Temporal DP specifically prioritizes identifying and representing the _temporal_ order and relationships between events, actions, and time expressions, often overlaying or extending syntactic structure.
- [ ] C. Syntactic DP is only used for spoken language, while Temporal DP is only for written text.
- [ ] D. Temporal DP aims to translate sentences into First-Order Logic.




## SEG-TMG
1. What is the main function of a search engine?
    
    - [ ] A. Storing users' personal data.
        
    - [x] B. Selecting relevant documents from large collections of information based on a user's query.
        
    - [ ] C. Creating data encryption algorithms.
        
    - [ ] D. Managing social networks.
        
2. Which component is primarily responsible for identifying and collecting documents for a search engine?
    
    - [ ] A. Text Transformation component.
        
    - [ ] B. Index Creation component.
        
    - [x] C. Text Acquisition component.
        
    - [ ] D. Query Process component.
        
3. What is another name for a "crawler" in the context of search?
    
    - [x] A. Bots, spiders, robots, worms, walkers.
        
    - [ ] B. Developers, engineers, analysts.
        
    - [ ] C. Servers, databases, networks.
        
    - [ ] D. Users, clients, browsers.
        
4. What is the main purpose of "web crawling"?
    
    - [ ] A. Analyzing website traffic.
        
    - [x] B. Discovering and indexing new or updated web pages for a search engine.
        
    - [ ] C. Creating advertising content.
        
    - [ ] D. Securing user data.
        
5. What is one of the significant challenges in designing a web crawler?
    
    - [ ] A. Ensuring image quality.
        
    - [x] B. Efficiently handling the large volume of new pages and keeping updated pages "fresh".
        
    - [ ] C. Optimizing the user interface.
        
    - [ ] D. Developing complex encryption algorithms.
        
6. What is an "inverted index" architecture primarily used for in a search engine?
    
    - [ ] A. Storing images and videos.
        
    - [x] B. Building a page with display results for the user after receiving a query.
        
    - [ ] C. Managing user accounts.
        
    - [ ] D. Analyzing non-textual data.
        
7. What are the main steps in building an inverted index?
    
    - [ ] A. Collect documents, parse, compress.
        
    - [ ] B. Collect documents, encrypt text, create index, search.
        
    - [x] C. Collect documents, tokenize text, perform linguistic preprocessing, index documents.
        
    - [ ] D. Collect documents, classify, tag, cluster.
        
8. What are "index terms" or "features" in the text transformation process?
    
    - [ ] A. The entire content of the document.
        
    - [x] B. The parts of a document that are stored in the index and used for searching.
        
    - [ ] C. The keywords entered by the user.
        
    - [ ] D. Links to other documents.
        
9. What is the "index vocabulary"?
    
    - [ ] A. The set of all keywords users have searched for.
        
    - [x] B. The set of all indexed terms for a document collection.
        
    - [ ] C. A dictionary of synonyms.
        
    - [ ] D. A list of stopwords.
        
10. What are the three basic building blocks of the indexing process?
    
    - [x] A. Text acquisition, text transformation, and index creation.
        
    - [ ] B. Text acquisition, querying, and ranking.
        
    - [ ] C. Text analysis, classification, and clustering.
        
    - [ ] D. Preprocessing, machine learning, and prediction.
        
11. What is "metadata" in the context of a search document?
    
    - [ ] A. The main content of the document.
        
    - [x] B. Information about a document that is not part of the text content (e.g., document type, structure).
        
    - [ ] C. Keywords tagged for optimization.
        
    - [ ] D. Internal links within the document.
        
12. What is the role of the text transformation component?
    
    - [ ] A. To identify and acquire documents.
        
    - [x] B. To transform documents into index terms or features.
        
    - [ ] C. To store documents.
        
    - [ ] D. To rank documents.
        
13. What is important for compression techniques for inverted indexes?
    
    - [ ] A. Reducing the size of the original documents.
        
    - [x] B. Reducing the response time of the search engine.
        
    - [ ] C. Increasing the number of documents that can be indexed.
        
    - [ ] D. Improving the accuracy of the results.
        
14. How can the MapReduce framework be used for building indexes for very large document collections?
    
    - [ ] A. By minimizing the amount of data to be processed.
        
    - [x] B. By performing parallel computations on large amounts of data.
        
    - [ ] C. By fully automating the indexing process.
        
    - [ ] D. By compressing data before processing.
        
15. What is the main goal of information retrieval research related to relevance?
    
    - [x] A. To understand and formalize the processes by which people make decisions about the relevance of a document.
        
    - [ ] B. To optimize search speed.
        
    - [ ] C. To develop user-friendly interfaces.
        
    - [ ] D. To reduce data storage costs.
        
16. What will a good retrieval model produce?
    
    - [ ] A. Faster algorithms.
        
    - [x] B. Output that correlates well with human relevance decisions.
        
    - [ ] C. Less training data.
        
    - [ ] D. Fewer duplicate documents.
        
17. What is the most commonly used framework for measuring text similarity in search engines?
    
    - [ ] A. Boolean model.
        
    - [x] B. Vector space model.
        
    - [ ] C. Probabilistic model.
        
    - [ ] D. Inference network model.
        
18. How does the vector space model represent each document?
    
    - [ ] A. As a string of keywords.
        
    - [ ] B. As a hierarchical tree.
        
    - [x] C. As a vector in a high-dimensional space, where each dimension is a term.
        
    - [ ] D. As a set of rules.
        
19. How is "relevance" typically defined in information retrieval?
    
    - [ ] A. An objective measure of keyword matching.
        
    - [x] B. A user's subjective assessment of the value or utility of a document in meeting a specific information need.
        
    - [ ] C. The click-through rate of a document.
        
    - [ ] D. The number of links to a document.
        
20. On what criteria does Google's PageRank algorithm rank web pages?
    
    - [ ] A. The length of the page.
        
    - [x] B. The number of HTML links to it and other "reputation-based" metrics.
        
    - [ ] C. The frequency of keyword appearance.
        
    - [ ] D. The page load time.
        
21. What is the most common form of vector space weighting?
    
    - [ ] A. Boolean weighting.
        
    - [x] B. TF-IDF weighting.
        
    - [ ] C. Position-based weighting.
        
    - [ ] D. Context-based weighting.
        
22. The Retrieval-Augmented Generation (RAG) architecture is designed to mitigate what problem?
    
    - [ ] A. Lack of training data.
        
    - [ ] B. Language model latency.
        
    - [x] C. The factual unreliability of standalone language models.
        
    - [ ] D. Computational cost.
        
23. An intelligent chatbot system for Vietnamese tourists combines the response generation capabilities of the DeepSeek R1 large language model with which retrieval algorithm to select personalized responses?
    
    - [ ] A. k-means clustering algorithm.
        
    - [x] B. k-Nearest Neighbors (k-NN) algorithm.
        
    - [ ] C. Decision tree algorithm.
        
    - [ ] D. Naive Bayes algorithm.
        
24. Which two main criteria does the k-NN algorithm in the Vietnam travel chatbot use to select the optimal answer?
    
    - [ ] A. Language and location.
        
    - [x] B. Cost and user preferences (adventure, relaxation, culture, food).
        
    - [ ] C. Time and weather.
        
    - [ ] D. User ratings and popularity.
        
25. What does "Learning to Rank" in machine learning and information retrieval involve?
    
    - [x] A. Learning how to rank documents based on user feedback.
        
    - [ ] B. Learning how to generate better queries.
        
    - [ ] C. Learning how to optimize web pages.
        
    - [ ] D. Learning how to collect data more efficiently.
        
26. Which classification technique is the most well-known approach to learning a ranking function for search?
    
    - [ ] A. Logistic Regression.
        
    - [x] B. Ranking Support Vector Machine (SVM).
        
    - [ ] C. Decision Tree.
        
    - [ ] D. Autoencoder Neural Network.
        
27. What information do Ranking SVMs and RankNet learn from?
    
    - [ ] A. Manual document labels.
        
    - [ ] B. The difference between document scores.
        
    - [x] C. Partial ranking information (e.g., preference pairs).
        
    - [ ] D. Data from a semantic dictionary.
        
28. What is a disadvantage of the vector space model compared to the Boolean model?
    
    - [x] A. It cannot make "exact" queries because it does not support operators.
        
    - [ ] B. It is slower in practice.
        
    - [ ] C. The results are difficult to interpret.
        
    - [ ] D. It requires a large amount of training data.
        
29. What steps does the data preprocessing for the Vietnam travel chatbot include?
    
    - [ ] A. One-hot encoding and data compression.
        
    - [x] B. Text normalization, deduplication, and context labeling.
        
    - [ ] C. Parsing and language translation.
        
    - [ ] D. Graph creation and network analysis.
        
30. How does the intelligent chatbot system enhance the travel experience?
    
    - [ ] A. By providing only general information.
        
    - [x] B. By providing highly personalized recommendations and accurate answers, with 24/7 support.
        
    - [ ] C. By automatically booking tickets and hotel rooms.
        
    - [ ] D. By providing real-time translation.
        

### II. Search Engine Optimization (CLO2 - SEO)

31. What is the content-focused approach in SEO?
    
    - [ ] A. Using as many keywords as possible.
        
    - [x] B. Telling a story thoroughly and accurately, hoping the content will align with the search engine's indexing algorithms.
        
    - [ ] C. Increasing the number of internal links.
        
    - [ ] D. Using hidden text techniques.
        
32. What do experienced SEO specialists typically do before a website is built, expanded, or redesigned?
    
    - [ ] A. Competitor analysis.
        
    - [x] B. Keyword analysis.
        
    - [ ] C. User interface redesign.
        
    - [ ] D. Page speed optimization.
        
33. What are "meta keyword tags" considered in modern SEO?
    
    - [ ] A. An important ranking factor.
        
    - [x] B. A major "illusion" in SEO, no longer holding much value.
        
    - [ ] C. a way to specify the main content.
        
    - [ ] D. A useful tool for keyword analysis.
        
34. According to the source, who are the search engineers who "design or optimize content for search engines"?
    
    - [x] A. Those primarily trained in computer science with a systems or database background.
        
    - [ ] B. Those working in the marketing industry.
        
    - [ ] C. Those who develop hardware.
        
    - [ ] D. Those who are project managers.
        
35. What is most important for specializing a general-purpose large language model (LLM) for a specific domain, ensuring the chatbot's responses are not only fluent but also highly relevant and accurate?
    
    - [ ] A. The size of the model.
        
    - [x] B. The meticulousness of data preparation and the fine-tuning process.
        
    - [ ] C. The training speed.
        
    - [ ] D. The model's translation capabilities.
        
36. The modern approach applied by chatbots, using NLP and ML, has overcome which limitations of traditional rule-based systems (like ELIZA or PARRY)?
    
    - [ ] A. High operational costs.
        
    - [x] B. Lack of robustness to varied input, lack of state about conversational history, and scalability challenges.
        
    - [ ] C. Difficulty in data collection.
        
    - [ ] D. Support for only a single language.
        
37. The intelligent travel chatbot fine-tuned the DeepSeek R1 model on a carefully selected dataset of how many question-answer pairs?
    
    - [ ] A. 100 pairs.
        
    - [ ] B. 1,000 pairs.
        
    - [x] C. 3,000 pairs.
        
    - [ ] D. 10,000 pairs.
        
38. What is the purpose of fine-tuning the DeepSeek R1 large language model on a specific Vietnamese tourism dataset?
    
    - [ ] A. To reduce the chatbot's response time.
        
    - [x] B. To enhance its ability to generate fluent and contextually appropriate dialogue.
        
    - [ ] C. To improve its image processing capabilities.
        
    - [ ] D. To completely replace the retrieval algorithm.
        
39. How is a "virtuous cycle" created by NLP and search described?
    
    - [ ] A. Training data automatically increases.
        
    - [x] B. Improved search engines lead to faster development of NLP algorithms, which in turn improves search technology.
        
    - [ ] C. Users provide direct feedback to developers.
        
    - [ ] D. NLP applications become more popular.
        
40. In applied text analysis, what general process is typically followed to find an optimal model?
    
    - [ ] A. Data collection, feature analysis, deployment.
        
    - [x] B. Create a corpus, select a vectorization technique, train a model, and evaluate with cross-validation.
        
    - [ ] C. Design an interface, collect feedback, continuously improve.
        
    - [ ] D. Define the problem, select an algorithm, compare performance.
        

### III. Keyword Research (CLO3 - Keywords)

41. What does keyword research help determine?
    
    - [ ] A. Competitor websites.
        
    - [x] B. The most relevant and profitable keywords.
        
    - [ ] C. Web design trends.
        
    - [ ] D. The technical issues of a website.
        
42. What is the average number of keywords in a web search query?
    
    - [ ] A. One word.
        
    - [x] B. Two to three words.
        
    - [ ] C. Five to seven words.
        
    - [ ] D. Ten or more words.
        
43. In the context of a query, what is a "keyword"?
    
    - [ ] A. Any word that appears in the query.
        
    - [x] B. An important word to specify the topic of a query.
        
    - [ ] C. A word used for advertising purposes.
        
    - [ ] D. A word identified by the search engine.
        
44. What is the syntax for a phrase query in popular search engines today?
    
    - [ ] A. Using parentheses ().
        
    - [x] B. Using double quotes "".
        
    - [ ] C. Using a hyphen -.
        
    - [ ] D. Using an asterisk *.
        
45. What is "term proximity weighting"?
    
    - [x] A. A technique where documents are preferred if the query terms appear close to each other in the text.
        
    - [ ] B. A way to calculate word frequency.
        
    - [ ] C. A method to remove irrelevant words.
        
    - [ ] D. A technique for query expansion.
        
46. What is the main advantage of search engines for finding linguistic examples?
    
    - [ ] A. Fast search capabilities.
        
    - [ ] B. The ability to handle different languages.
        
    - [x] C. Their large size, which increases the likelihood of finding language patterns.
        
    - [ ] D. Providing personalized results.
        
47. What are "stopwords"?
    
    - [ ] A. The most important words in a document.
        
    - [x] B. High-frequency words that are often removed in text preprocessing.
        
    - [ ] C. Keywords used in advertising.
        
    - [ ] D. New words added to the dictionary.
        
48. What is "stemming" in text processing?
    
    - [ ] A. The process of splitting text into sentences.
        
    - [x] B. A heuristic process that chops off the ends of words in the hope of achieving a goal correctly most of the time.
        
    - [ ] C. The process of determining the meaning of a word.
        
    - [ ] D. The process of converting words to numbers.
        
49. What is "lemmatization" in text processing?
    
    - [x] A. A process of converting a word to its base or dictionary form, grouping together grammatically different forms.
        
    - [ ] B. A method of counting word frequency.
        
    - [ ] C. A technique for removing stopwords.
        
    - [ ] D. A way to find spelling errors.
        
50. In the text preprocessing stage, why might terms be "weighted" differently?
    
    - [ ] A. To make the text more readable.
        
    - [x] B. To account for their importance within a document and/or a document collection.
        
    - [ ] C. To reduce the size of the index.
        
    - [ ] D. To speed up retrieval.
        

### IV. Analytics and Monitoring (CLO4 - Analytics)

51. What can data from user search sessions, such as clickthroughs and other interactions, be used for?
    
    - [ ] A. To create new advertisements.
        
    - [x] B. To enhance the relevance of search results.
        
    - [ ] C. To analyze system errors.
        
    - [ ] D. To estimate search costs.
        
52. Analyzing clickthrough data and other implicit feedback collected in search engine logs helps to evaluate and improve what?
    
    - [ ] A. Search speed.
        
    - [x] B. The performance of the search engine.
        
    - [ ] C. The complexity of the algorithm.
        
    - [ ] D. The diversity of the results.
        
53. What interesting relationships can be inferred by considering users, queries, and pages?
    
    - [ ] A. Users often use the same keywords.
        
    - [x] B. Similar users tend to issue similar queries, and similar pages appear as results for related queries.
        
    - [ ] C. All users have the same information needs.
        
    - [ ] D. The most popular website is always relevant to every query.
        
54. What are analytics tools primarily used to track?
    
    - [ ] A. Website domain names.
        
    - [x] B. Website traffic, user behavior, and campaign performance.
        
    - [ ] C. Source code errors.
        
    - [ ] D. Website development time.
        
55. How can user behavior features be effectively integrated into RankNet-based ranking?
    
    - [ ] A. By using a Boolean model.
        
    - [x] B. By using a machine learning algorithm.
        
    - [ ] C. By removing stopwords.
        
    - [ ] D. By relying only on explicit training data.
        

### V. Problem Solving (CLO5)

56. What are "language-aware data products"?
    
    - [ ] A. Applications that only process numerical data.
        
    - [x] B. Applications that interact with humans in natural language.
        
    - [ ] C. Applications that collect data from multiple sources.
        
    - [ ] D. Applications that only display search results.
        
57. What is the main task of data scientists when building language-aware data products?
    
    - [ ] A. Developing hardware.
        
    - [x] B. Creating a model that describes language and can make inferences based on that description.
        
    - [ ] C. Managing databases.
        
    - [ ] D. Designing user interfaces.
        
58. Machine learning (ML) has been very successful with which tasks involving complex patterns?
    
    - [ ] A. Only tasks involving numerical processing.
        
    - [x] B. Object detection and speech recognition.
        
    - [ ] C. Simple rule-based tasks.
        
    - [ ] D. Tasks requiring strict logical reasoning.
        
59. In applied text analysis, what is the "hardest part"?
    
    - [ ] A. Deploying the model.
        
    - [x] B. Distilling and collecting a domain-specific dataset to build the model.
        
    - [ ] C. Evaluating performance.
        
    - [ ] D. Choosing a programming language.
        
60. What is the "second hardest part" in applied text analysis?
    
    - [ ] A. Finding optimal algorithms.
        
    - [x] B. Composing an analytical solution for a specific application problem.
        
    - [ ] C. Ensuring data security.
        
    - [ ] D. Integrating with existing systems.
        

### VI. Fundamental Concepts and Principles of Text Mining

61. What does NLP stand for?
    
    - [ ] A. Neural Language Programming.
        
    - [ ] B. Natural Logic Processing.
        
    - [ ] C. Natural Language Programming.
        
    - [x] D. Natural Language Processing.
        
62. What is another name for text mining?
    
    - [ ] A. Big data analysis.
        
    - [x] B. Text analytics.
        
    - [ ] C. Information mining.
        
    - [ ] D. Raw data processing.
        
63. Text mining involves the use of which techniques?
    
    - [ ] A. Only statistics-based.
        
    - [x] B. Natural language processing, information retrieval, and machine learning.
        
    - [ ] C. Only language rule-based.
        
    - [ ] D. Manual programming.
        
64. What is Machine Learning (ML) defined as?
    
    - [ ] A. A branch of AI focusing on rigid rules.
        
    - [x] B. The art and science of leveraging techniques that allow machines to learn hidden patterns and relationships from underlying data and improve themselves over time without being explicitly programmed.
        
    - [ ] C. A method of manual data processing.
        
    - [ ] D. A tool used only for classification.
        
65. Deep Learning (DL) is a subfield of machine learning specializing in what type of model?
    
    - [ ] A. Simple linear models.
        
    - [x] B. Deep neural network models with many hidden layers.
        
    - [ ] C. Traditional statistical models.
        
    - [ ] D. Rule-based models.
        
66. How is natural language classified as data?
    
    - [ ] A. Structured data.
        
    - [ ] B. Semi-structured data.
        
    - [x] C. Unstructured data.
        
    - [ ] D. Relational data.
        
67. What is a "corpus" in the context of NLP?
    
    - [ ] A. A programming language.
        
    - [x] B. A large collection of language data.
        
    - [ ] C. A text processing algorithm.
        
    - [ ] D. A keyword analysis tool.
        
68. What is the process of "tokenization"?
    
    - [ ] A. Removing special characters.
        
    - [ ] B. Parsing the syntax of a sentence.
        
    - [x] C. Breaking down sentences into individual tokens (e.g., words, punctuation).
        
    - [ ] D. Converting text to a numerical format.
        
69. What makes natural language difficult to parse with deterministic rules?
    
    - [ ] A. Lack of vocabulary.
        
    - [x] B. The flexibility that humans use in interpretation.
        
    - [ ] C. Processing speed.
        
    - [ ] D. The size of the data.
        
70. What is the current state-of-the-art for text analysis?
    
    - [ ] A. Rigid rule-based systems.
        
    - [x] B. Statistical machine learning techniques.
        
    - [ ] C. Dictionary search algorithms.
        
    - [ ] D. Grammar-only based systems.
        
71. What is the main challenge in any machine learning application?
    
    - [ ] A. Designing the user interface.
        
    - [x] B. Identifying where the signal is hiding in the noise.
        
    - [ ] C. Finding large datasets.
        
    - [ ] D. Optimizing performance.
        
72. What is "feature analysis"?
    
    - [ ] A. The process of calculating statistical metrics.
        
    - [x] B. The process of identifying the best features, attributes, or dimensions to encode the underlying meaning and structure of the text.
        
    - [ ] C. The process of generating word vectors.
        
    - [ ] D. The process of classifying documents.
        
73. In data preprocessing, what steps does "text normalization" include to ensure consistency and quality?
    
    - [ ] A. Only converting text to lowercase.
        
    - [x] B. Removing unnecessary punctuation, converting text to lowercase, removing duplicates, and labeling context.
        
    - [ ] C. Translating text to another language.
        
    - [ ] D. Adding keywords to the text.
        
74. What is "context" in language understanding?
    
    - [ ] A. Only the text surrounding a word.
        
    - [x] B. It extends beyond the surrounding text to include the time period.
        
    - [ ] C. Only the grammatical relationship between words.
        
    - [ ] D. Only the dictionary meaning of a word.
        
75. What is a "language model"?
    
    - [x] A. A model that can assign a probability to a sequence of words or a sentence.
        
    - [ ] B. A model that only translates sentences.
        
    - [ ] C. A model that only recognizes speech.
        
    - [ ] D. A model that only classifies text.
        
76. What does "perplexity" measure in the context of a language model?
    
    - [ ] A. The length of a sentence.
        
    - [ ] B. The level of incomprehensibility of the text.
        
    - [x] C. The predictability of the text by evaluating the entropy of the language model's probability distribution.
        
    - [ ] D. The frequency of words.
        
77. What are "tokens"?
    
    - [ ] A. Complete sentences.
        
    - [x] B. UTF-8 encoded strings of data that listeners and readers identify as meaningful words.
        
    - [ ] C. Special characters.
        
    - [ ] D. Numbers.
        
78. Which Python libraries are described as a "powerful toolkit" for machine learning on text?
    
    - [ ] A. Pandas, Matplotlib.
        
    - [x] B. Scikit-Learn, NLTK, Gensim, spaCy, NetworkX, Yellowbrick.
        
    - [ ] C. Django, Flask.
        
    - [ ] D. NumPy, SciPy.
        
79. What is Scikit-Learn?
    
    - [ ] A. A library specialized for natural language processing.
        
    - [x] B. An extension of SciPy that provides an API for general-purpose machine learning.
        
    - [ ] C. A tool for creating search indexes.
        
    - [ ] D. A web development framework.
        
80. What is the reason deep learning has become a new trend in AI?
    
    - [x] A. The data explosion and hardware development.
        
    - [ ] B. It is easier to implement than traditional ML methods.
        
    - [ ] C. It requires less data.
        
    - [ ] D. The ability to automate all tasks.
        

### VII. Machine Learning/Deep Learning for Text Mining Applications

81. What are some of the biggest challenges in NLP currently being addressed by neural networks?
    
    - [ ] A. Only numerical computation.
        
    - [x] B. Machine translation, summarization, interpretation, question answering, and conversation.
        
    - [ ] C. Image classification.
        
    - [ ] D. Object recognition.
        
82. What is the typical size of "dense vector models"?
    
    - [ ] A. 10-20.
        
    - [x] B. 50-1000.
        
    - [ ] C. Over 10,000.
        
    - [ ] D. Unlimited.
        
83. What does the "skip-gram" algorithm in Word2vec do?
    
    - [ ] A. Predicts the target word from neighboring words.
        
    - [x] B. Predicts the context of a word (output words) from a word of interest (input word).
        
    - [ ] C. Generates complete sentences.
        
    - [ ] D. Classifies documents.
        
84. What does the "Continuous Bag-of-Words" (CBOW) approach do?
    
    - [x] A. Predicts the target word (output word) from neighboring words (input words).
        
    - [ ] B. Predicts context words from a target word.
        
    - [ ] C. Calculates word frequency.
        
    - [ ] D. Builds a syntax tree.
        
85. What did Bengio et al. show that neural language models could be used for?
    
    - [ ] A. Spam detection.
        
    - [x] B. Developing embeddings as part of a word prediction task.
        
    - [ ] C. Image classification.
        
    - [ ] D. Music generation.
        
86. What is a "neural network"?
    
    - [ ] A. A rule-based system.
        
    - [x] B. A computational model inspired by the structure of the brain.
        
    - [ ] C. A type of database.
        
    - [ ] D. A programming language.
        
87. What is the "backpropagation" algorithm?
    
    - [ ] A. An algorithm to calculate the output value of a neural network.
        
    - [x] B. An algorithm to find the weights and biases in a neural network.
        
    - [ ] C. An algorithm to randomly initialize weights.
        
    - [ ] D. An algorithm for data compression.
        
88. What is the function of the "fully connected" layer in a CNN?
    
    - [ ] A. To perform convolution operations.
        
    - [x] B. To aggregate the features learned from the convolutional and pooling layers to produce the model's output.
        
    - [ ] C. To reduce data dimensionality.
        
    - [ ] D. To increase the depth of the network.
        
89. What software did Thomas Mikolov and his team at Google release in 2013 for creating word vectors?
    
    - [ ] A. Doc2Vec.
        
    - [x] B. Word2vec.
        
    - [ ] C. GloVe.
        
    - [ ] D. FastText.
        
90. What are the two most popular models for vector semantics?
    
    - [ ] A. BoW and TF-IDF.
        
    - [x] B. tf-idf and word2vec.
        
    - [ ] C. N-gram and LDA.
        
    - [ ] D. CNN and RNN.
        
91. What is "cosine similarity" used for with embeddings?
    
    - [ ] A. To calculate the distance between words.
        
    - [x] B. To calculate the semantic similarity between two words, two sentences, or two documents.
        
    - [ ] C. To classify text.
        
    - [ ] D. To encode words into vectors.
        
92. What type of data is a "Recurrent Neural Network" (RNN) specialized for?
    
    - [ ] A. Image data.
        
    - [ ] B. Tabular data.
        
    - [x] C. Sequence data.
        
    - [ ] D. Audio data.
        
93. What are some applications of RNNs?
    
    - [ ] A. Only image classification.
        
    - [x] B. Speech-to-text, sentiment classification, machine translation.
        
    - [ ] C. Generating new images.
        
    - [ ] D. Object detection.
        
94. What is the main problem with basic RNNs that LSTMs solve?
    
    - [ ] A. Lack of parallel processing capability.
        
    - [x] B. Limited ability to look into the past and the vanishing/exploding gradient problem.
        
    - [ ] C. Only works with structured data.
        
    - [ ] D. Slow training speed.
        
95. What is an LSTM (Long Short-Term Memory) capable of?
    
    - [ ] A. Only remembering short-term information.
        
    - [x] B. Selectively retaining/discarding information during forward propagation, and avoiding vanishing/exploding gradients during backpropagation.
        
    - [ ] C. Generating animated images.
        
    - [ ] D. Performing complex numerical calculations.
        
96. What components does a "sequence-to-sequence" (seq2seq) model consist of?
    
    - [ ] A. Only an encoder.
        
    - [ ] B. Only a decoder.
        
    - [x] C. An encoder and a decoder.
        
    - [ ] D. An encoder, a decoder, and an external memory.
        
97. What are the main applications of seq2seq models?
    
    - [ ] A. Only text classification.
        
    - [x] B. Chatbot conversation, question answering, machine translation, image captioning, document summarization.
        
    - [ ] C. Fraud detection.
        
    - [ ] D. Financial data analysis.
        
98. What does the "attention mechanism" in a seq2seq model do?
    
    - [ ] A. Reduces the number of model parameters.
        
    - [x] B. Allows the model to focus on relevant parts of the input when generating the output.
        
    - [ ] C. Speeds up training.
        
    - [ ] D. Limits the length of the output sequence.
        
99. What is "transfer learning"?
    
    - [ ] A. Training a new model from scratch with new data.
        
    - [x] B. The process of using a pre-trained model on a large dataset to solve a similar problem.
        
    - [ ] C. Converting data from one format to another.
        
    - [ ] D. Collecting data from various sources.
        
100. What are the two main types of "transfer learning"? - [ ] A. Supervised learning and unsupervised learning. - [x] B. Feature extraction and fine-tuning. - [ ] C. Machine translation and text generation. - [ ] D. Classification and clustering.
    
101. What are the two most important factors for using transfer learning? - [ ] A. Network speed and storage capacity. - [x] B. The amount of data you have and the similarity of the data between the model you need to train and the pre-trained model. - [ ] C. The programming language and framework used. - [ ] D. The number of CPUs/GPUs.
    
102. How has deep learning helped in the field of Computer Vision? - [ ] A. It only improved image resolution. - [x] B. It has helped computers perform seemingly impossible tasks like classifying thousands of different objects in photos and automatically generating captions for images. - [ ] C. It reduced image size. - [ ] D. It optimized image display.
    
103. What does "fine-tuning" in transfer learning mean? - [ ] A. Using only the ConvNet part of the pre-trained model. - [x] B. Adding new fully connected layers and retraining some layers in the ConvNet of the pre-trained model. - [ ] C. Removing unnecessary layers. - [ ] D. Reducing the complexity of the model.
    
104. Which activation function is generally recommended as the default in Deep Learning? - [ ] A. Sigmoid. - [ ] B. Tanh. - [x] C. ReLU. - [ ] D. Softmax.
    
105. What is "Batch Normalization"? - [ ] A. A technique to increase the amount of training data. - [x] B. A technique that helps regulate and normalize the output of layers in a neural network. - [ ] C. A method to reduce overfitting. - [ ] D. An optimization algorithm.
    
106. When is "mini-batch gradient descent" typically used? - [ ] A. When the amount of training data is very small. - [x] B. With large amounts of data, it helps solve the problem of batch gradient descent and allows for vectorization. - [ ] C. When an absolutely exact derivative calculation is needed. - [ ] D. When there are not enough GPU resources.
    
107. According to the source, what is the "most interesting idea in the last 10 years in Machine Learning"? - [ ] A. Recurrent Neural Network (RNN) models. - [x] B. Generative Adversarial Networks (GANs). - [ ] C. Transformers. - [ ] D. Reinforcement Learning.
    
108. Which Deep Learning model was proposed by K. Simonyan and A. Zisserman of the University of Oxford? - [ ] A. ResNet. - [ ] B. GoogLeNet. - [x] C. VGG16. - [ ] D. AlexNet.
    
109. What is the purpose of initializing word vectors with an unsupervised neural language model, especially when a large labeled dataset is not available? - [ ] A. To reduce training time. - [x] B. To improve performance. - [ ] C. To increase the interpretability of the model. - [ ] D. To ensure data privacy.
    
110. Which model in Word2vec is said to have a disadvantage when averaging the contexts of a word? - [ ] A. Skip-gram. - [x] B. CBOW. - [ ] C. GloVe. - [ ] D. FastText.
    

### VIII. Text Classification and Clustering Methods and Algorithms

111. What is "text classification"? - [ ] A. Just the act of labeling text. - [x] B. The task of assigning a suitable label or category from a predefined set of labels or categories to a piece of text. - [ ] C. Summarizing the content of a text. - [ ] D. Translating text into another language.
    
112. What is "sentiment analysis"? - [ ] A. Identifying specific words in a text. - [x] B. Analyzing and evaluating a person's opinion or emotion about an object through speech or text. - [ ] C. Counting word frequency. - [ ] D. Generating new texts.
    
113. What are the two main types of machine learning techniques involved in solving the text classification problem? - [ ] A. Reinforcement learning and semi-supervised learning. - [x] B. Supervised learning and unsupervised learning. - [ ] C. Deep learning and traditional machine learning. - [ ] D. Online learning and offline learning.
    
114. The Naive Bayes algorithm belongs to which type of classification? - [ ] A. Tree-based classification. - [x] B. Statistical classification, specifically a probabilistic model. - [ ] C. Distance-based classification. - [ ] D. Neural network classification.
    
115. In sentiment classification, machine learning techniques have demonstrated significantly more accurate results than which baseline model? - [ ] A. Rule-based models. - [x] B. Models using human-created word lists. - [ ] C. Syntax-based models. - [ ] D. N-gram based models.
    
116. What is a Support Vector Machine (SVM)? - [ ] A. A clustering algorithm. - [x] B. A machine learning method based on vector spaces, with the goal of finding a decision boundary between two classes that is maximally far from any point in the training data. - [ ] C. A language model. - [ ] D. A text preprocessing tool.
    
117. What is one of the key characteristics of SVMs? - [ ] A. Easy interpretation of results. - [x] B. The ability to find a decision boundary between classes. - [ ] C. Requires little training data. - [ ] D. Fast training speed.
    
118. What is "K-means clustering"? - [ ] A. A supervised classification algorithm. - [x] B. A popular, simple, and effective flat clustering algorithm. - [ ] C. A feature extraction technique. - [ ] D. A method for dimensionality reduction.
    
119. What is "search result clustering"? - [ ] A. Sorting search results by relevance. - [x] B. Grouping similar documents in search results together to create coherent groups. - [ ] C. Filtering out irrelevant results. - [ ] D. Aggregating results from multiple search engines.
    
120. What is a requirement for search result clustering? - [ ] A. High accuracy. - [x] B. Efficiency (often based on document snippets). - [ ] C. Scalability. - [ ] D. Ability to handle multiple languages.
    
121. What is "topic modeling"? - [ ] A. A supervised machine learning technique for topic classification. - [x] B. An unsupervised machine learning technique for abstracting topics from document collections. - [ ] C. A method for keyword research. - [ ] D. A way to summarize text.
    
122. Which statistical techniques does topic modeling use? - [ ] A. Only linear regression. - [x] B. Singular Value Decomposition (SVD) and Latent Dirichlet Allocation (LDA). - [ ] C. Optimization algorithms. - [ ] D. Convolutional neural networks.
    
123. What is the basic workflow for applied text analysis involving classification? - [ ] A. Data collection, feature processing, model building, evaluation. - [x] B. Create a corpus, select a vectorization technique, train a model, and evaluate with cross-validation. - [ ] C. Design an interface, get feedback, improve. - [ ] D. Define requirements, select tools, deploy.
    
124. What metrics does classification provide to guide algorithm selection? - [ ] A. Speed, memory, and complexity. - [x] B. Accuracy, precision, recall, and F1-score. - [ ] C. Number of parameters and convergence time. - [ ] D. Data size and number of classes.
    
125. What is an unsupervised machine learning algorithm? - [ ] A. A technique that requires labeled data. - [x] B. A technique where the model learns patterns from data without explicit output labels. - [ ] C. A method for predicting numerical values. - [ ] D. A way to generate new data.
    
126. What is the relationship between the effectiveness of SVM, kNN, and Naive Bayes classifiers? - [ ] A. SVM is always better than kNN, and kNN is always better than Naive Bayes. - [x] B. The ranking of the classifiers ultimately depends on the class, the document collection, and the experimental setup. - [ ] C. Naive Bayes is always the most effective. - [ ] D. All classifiers are equally effective.
    
127. What is important when conducting evaluations for classifiers (e.g., as in Table 13.9)? - [ ] A. Using as much training data as possible. - [x] B. Maintaining a strict separation between the training and test sets. - [ ] C. Optimizing parameters on the test set. - [ ] D. Comparing with existing models.
    
128. What problem can arise with Naive Bayes and SVM if there are too many classes? - [ ] A. The training speed becomes too fast. - [x] B. The problem of data sparsity. - [ ] C. The accuracy increases significantly. - [ ] D. Difficulty in feature finding.
    
129. What method did Ntoulas et al. (2006) propose to detect web spam by analyzing content? - [ ] A. Relying only on the word count. - [x] B. Extracting a large number of features from each webpage and using these features in a classifier. - [ ] C. Analyzing the links to the page. - [ ] D. Using general artificial intelligence.
    
130. What is one of the features used to detect web spam? - [ ] A. The color of the page. - [x] B. The compressibility of the page, which measures how much the page size can be reduced. - [ ] C. The page load speed. - [ ] D. The font size.
    

### IX. Text Data Representation Methods

131. What is the "Bag of Words" (BoW) approach? - [ ] A. Representing a document as a sequence of words. - [x] B. Representing every document from the corpus as a vector of the length of the corpus's vocabulary, counting word frequency or presence without regard to order. - [ ] C. Representing the relationship between words. - [ ] D. Using only important keywords.
    
132. What information does a BoW vector ignore? - [ ] A. Word frequency. - [x] B. Word order in a sentence. - [ ] C. Vocabulary. - [ ] D. The number of documents.
    
133. What does TF-IDF stand for? - [ ] A. Text Frequency - Information Document Feature. - [ ] B. Term Feature - Inverse Document Feature. - [x] C. Term Frequency - Inverse Document Frequency. - [ ] D. Text Flow - Important Document Factor.
    
134. What is the purpose of TF-IDF? - [ ] A. To reduce the size of the text. - [x] B. To represent the importance of a word in a document relative to a collection of documents. - [ ] C. To translate text. - [ ] D. To determine grammar.
    
135. What has TF-IDF improved in information retrieval systems? - [ ] A. Speed. - [x] B. Information retrieval results. - [ ] C. The user interface. - [ ] D. The ability to understand natural language.
    
136. What does "word embedding" mean? - [x] A. Encoding words into dense numerical vectors. - [ ] B. Only counting word frequency. - [ ] C. Removing irrelevant words. - [ ] D. Parsing sentences.
    
137. What are the two requirements for a word embedding algorithm? - [ ] A. Speed and efficiency. - [x] B. There exists one and only one representation for a word, and two semantically similar words have a close distance. - [ ] C. Support for multiple languages. - [ ] D. Interpretability.
    
138. Which models are available for pre-trained word embeddings? - [ ] A. Only Word2vec. - [x] B. Word2vec, GloVe, FastText. - [ ] C. LDA and SVD. - [ ] D. TF-IDF and BoW.
    
139. Why are embeddings important for ML/DL models? - [ ] A. Because they reduce data size. - [x] B. Because they are key to encoding text data so these models can use it. - [ ] C. Because they help speed up processing. - [ ] D. Because they allow the model to learn rigid rules.
    
140. What are "universal embeddings"? - [ ] A. Embeddings that only work for one language. - [x] B. Embeddings that can be used for many different downstream NLP tasks. - [ ] C. Embeddings that are only trained on small datasets. - [ ] D. Embeddings that are based only on keywords.
    

### X. Common Applications in Text Mining

141. What are some common applications of NLP? - [ ] A. Animal classification. - [x] B. Question answering systems, machine translation, and chatbots. - [ ] C. Weather forecasting. - [ ] D. Graphic design.
    
142. What is "machine translation"? - [x] A. The process of translating one language to another using a computer. - [ ] B. Just copying text. - [ ] C. Converting speech to text. - [ ] D. Summarizing document content.
    
143. What is a "Question Answering" (QA) system? - [ ] A. A system that only searches for information on the web. - [x] B. A system that can answer questions in natural language. - [ ] C. A system that automatically generates questions. - [ ] D. A language translation system.
    
144. What do customer service chatbots primarily rely on to generate responses? - [ ] A. Complex deep learning algorithms. - [x] B. Knowledge bases or relational databases. - [ ] C. Direct feedback from users. - [ ] D. Generative language models.
    
145. What is a "chatbot"? - [ ] A. A system that only records conversations. - [x] B. A conversational agent designed to simulate human conversation through text or speech. - [ ] C. A text editing application. - [ ] D. A data analysis tool.
    
146. What makes seq2seq (sequence-to-sequence) models very suitable for chatbot conversational systems? - [ ] A. Their ability to handle short sequences. - [x] B. They are generative models. - [ ] C. They have long-term memory. - [ ] D. They are very fast.
    
147. How do seq2seq chatbots compare to knowledge-based conversational systems in terms of generalization? - [ ] A. They are worse because they don't have a knowledge base. - [x] B. They can generalize from limited corpora and still respond reasonably on topics not present in the training set. - [ ] C. They are better only in a single domain. - [ ] D. They are limited to talking about topics outside the training domain.
    
148. What is "automatic summarization"? - [ ] A. The process of translating text. - [x] B. The task of condensing a piece of text into a shorter version while preserving the key informational elements and meaning of the content. - [ ] C. Classifying text by topic. - [ ] D. Extracting keywords.
    
149. What is "information extraction"? - [x] A. A technology language focused on extracting structure from text. - [ ] B. A method for generating new text. - [ ] C. A way to analyze sentiment. - [ ] D. A web search tool.
    
150. "Sentiment detection" is an application of which field? - [ ] A. Computer Vision. - [x] B. Information Extraction. - [ ] C. Speech Recognition. - [ ] D. Machine Translation.
    
