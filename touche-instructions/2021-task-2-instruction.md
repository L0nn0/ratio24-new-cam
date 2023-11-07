# Touché Task 2: Argument Retrieval for Comparative Questions

The goal of Task 2 is to support users facing some choice problem from "everyday life". Given a comparative question, the task is to retrieve and rank documents from the [ClueWeb12](https://lemurproject.org/clueweb12/) that help to answer the comparative question.

Each comparison search task is represented as a topic, where the *title* is a comparative question. The topic *description* represents a detailed search scenario, and the *narrative* describes what documents would be considered (highly) relevant.

## 1. Read topic
For each topic, please read its title, description, and narrative carefully. In particular, the narrative specifies what a (highly) relevant document would be for a given topic.
Note that narratives may not describe _all_ possible relevance options. This instruction should be considered as an extension to all topics.

## 2. Read document
Open the document by copy-pasting the URL, read the document.

## 3. Annotate relevance
Annotate the document's relevance for the topic:
   
| Label | Title | Rule of thumb |
| --- | --- | --- |
| R-2 | highly relevant | Compares the options mentioned in the question with respect to the aspects from the question and the description. Ideally, also includes a conclusion on which option is preferable, though that is not a must. Can contain a list of "good" / "best" options. |
| R-1 | relevant | Contain information about at least one of the compared options mentioned in the questions. At least, the user may learn something important about one of the options. |
| R-0 | not relevant | Does not compare the options. Also does not provide information on one of the options. |

## 4. Annotate quality
###### Description
Annotate the rhetorical quality, i.e. "well-writtenness" of the document (regardless of its relevance).
   - Does the text have a good style of speech? Informal is regared inferior to formal language.
   - Does it have proper sentence structure, and is easy to read?
   - Does it include informal speech, profanity, has typos, and makes use of other detrimental style choices?

###### Examples
> "Cats are the best!!! Don't even try to argue with me. Yeah, yeah, yeah (Grrrr) I have always had cats, they are so cool, and dogs just suck." (Question: Which is a better pet, a cat or a dog?)

The above argument, while factually sound, is of *low* rhetorical quality, as it lacks proper sentence structure, uses informal speech, has typos, and its use of ellipsis makes it hard to follow.

> "While a cat's independent nature generally helps them deal better than dogs with being left alone, it's important to remember that all cats are different. Some breeds are more sociable than others. Cats also tend to live longer than dogs, which is sometimes a consideration when searching for a lifelong furry companion." (Question: Which is a better pet, a cat or a dog?)

The above argument is an example of *high* rhetorical quality, as it is presented in formal language, well-structured and written in a way that is easily understandable, and orthographically correct.

###### Labels

| Label | Title | Rule of thumb |
| --- | --- | --- |
| Q-2 | high quality | The text fulfills all the above criteria sufficiently, i.e., proper language, well-structured, little grammar issues, easy to follow |
| Q-1 | medium quality | The text fulfills only some of the above criteria, or only to a limited degree, e.g., proper language but broken logic / hard to follow |
| Q-0 | low quality | The text does not fulfill the above criteria or is not argumentative at all, e.g., profanity, hard to follow, hard to read |
