# email-matic
Software for Semantic and Network Analysis of a Corpus of Emails

These scripts have been developed for the extrapolation and analysis of a corpus of emails.  They include, among other things:

 - corpuser: This script takes a path to a folder containing an archive of emails as input.  It applies some basic data cleaning, including the removal of some stop-words and punctuation and the detection of sentence boundaries, and writes a text file in which each line is the content of an email.

 - ldaer: This script builds a latent dirichlet allocation topic model from the type of file output by the corpuser script.

 - mailer: This script takes a path to a folder containing an archive of emails as input.  It outputs text files listing the probabilities of correspondce from and two a set of correspondents.

 - hister: This script will take a path to emails as well as a path to a topic model model and will print probabilities for a range of topics defined in the "topics" variable.  (These topics should have been previously established based on an analysis of the email corpus.)

 - topper: This script takes paths to emails, the email content file, and LDA and word2vec models as input, and actually outputs latex code for drawing lines between correspondents based on the probability of them corresponding about a given topic.  Note that the list of topics has been defined using the "topicker" function, which is not called in the script as written.  This list either needs to be established or incorporated into the code.  The word2vec model used should be generated on a large-scale corpus, probably not just an email corpus.
