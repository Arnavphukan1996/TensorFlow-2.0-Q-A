## About TensorFlow

TensorFlow is an open source platform for machine learning. With TensorFlow 2.0, tf.keras is the preferred high-level API for TensorFlow, to make model building easier and more intuitive. You may use the tf.keras built-in compile()/fit() methods, or write your own custom training loops. See the Effective TensorFlow 2.0 guide and the tf.keras guide for more details.
TensorFlow 2.0 was recently released and this competition is to challenge Kagglers to use TensorFlow 2.0’s APIs focused on usability, and easier, more intuitive development, to make advancements on Question Answering.

## Getting Started

Here are some resources to help you get started:

* Starter notebook using BERT on the dataset. Note: This baseline uses code that was migrated from TF1.x. Be aware that it contains use of tf.compat.v1, which is not permitted to be eligible for TF2.0 prizes in this competition. It is intended to be used as a starting point, but we're excited to see how much better you can using TF2.0!
* Some additional TensorFlow 2.0 resources:
  * Effective TensorFlow 2.0 Guide
  * Migrating code from TF1.x to TF2.0 as well as an upgrade script
  * tf.keras Guide
  * Kaggle's announcement about TF2.0 released in notebooks
* Information on the TF2.0 prizes you an earn in this competition
* The Natural Questions site for more information about their dataset or to download directly from them. Note that this competition's private test set is completely different from any of the datasets used by Natural Questions.
* Google Cloud Platform (GCP) Credits: For entrants in this competition, we are distributing $300 Coupons for GCP Credit.Requests can be made by submitting this form by November 18, 2019. We'll distribute the coupons by November 25th.
You must have made a submission to this competition, or your request will be rejected.
Only one person per team will be issued a Coupon. This will be verified and multiple requests from the same team will be de-duplicated.

## Data Description

### What should I expect the data format to be?
Each sample contains a Wikipedia article, a related question, and the candidate long form answers. The training examples also provide the correct long and short form answer or answers for the sample, if any exist.

### What am I predicting?
For each article + question pair, you must predict / select long and short form answers to the question drawn directly from the article. - A long answer would be a longer section of text that answers the question - several sentences or a paragraph. - A short answer might be a sentence or phrase, or even in some cases a YES/NO. The short answers are always contained within / a subset of one of the plausible long answers. - A given article can (and very often will) allow for both long and short answers, depending on the question.

There is more detail about the data and what you're predicting on the Github page for the Natural Questions dataset. This page also contains helpful utilities and scripts. Note that we are using the simplified text version of the data - most of the HTML tags have been removed, and only those necessary to break up paragraphs / sections are included.

## File descriptions
* simplified-nq-train.jsonl - the training data, in newline-delimited JSON format.
* simplified-nq-kaggle-test.jsonl - the test data, in newline-delimited JSON format.
* sample_submission.csv - a sample submission file in the correct format.

## Data fields
* document_text - the text of the article in question (with some HTML tags to provide document structure). The text can be tokenized by splitting on whitespace.
* question_text - the question to be answered
* long_answer_candidates - a JSON array containing all of the plausible long answers.
* annotations - a JSON array containing all of the correct long + short answers. Only provided for train.
* document_url - the URL for the full article. Provided for informational purposes only. This is NOT the simplified version of the article so indices from this cannot be used directly. The content may also no longer match the html used to generate document_text. Only provided for train.
* example_id - unique ID for the sample.
