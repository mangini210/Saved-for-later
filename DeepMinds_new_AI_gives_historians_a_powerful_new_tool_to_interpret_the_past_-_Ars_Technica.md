# DeepMind’s new AI gives historians a powerful new tool to interpret the past - Ars Technica

**Source URL:** https://arstechnica.com/?p=1839561

## Summary
Here is a summary of the article:

*   **Advanced AI for History:** Google DeepMind has developed "Ithaca," a deep neural network designed to assist historians in restoring, dating, and geolocating damaged ancient Greek inscriptions.
*   **Superior Accuracy:** When working in tandem, human historians and the Ithaca AI achieve a 72% accuracy rate in text restoration, significantly outperforming human-only analysis (25%) and AI-only analysis (62%).
*   **Solving Historical Debates:** The system has already proven its practical value by providing evidence to help resolve a long-standing scholarly dispute regarding the dating of ancient Athenian decrees.
*   **Accessibility and Expansion:** The researchers have made the Ithaca code open source and created a free interactive version; they now plan to adapt the tool to support other ancient languages like Hebrew, Akkadian, and Mayan.

--- 

## Full Content
# DeepMind’s new AI gives historians a powerful new tool to interpret the past

Ithaca system restores text, can also ID location and date of damaged inscriptions.

![](https://cdn.arstechnica.net/wp-content/uploads/2022/03/ithaca2CROP.jpg)

Google DeepMind has collaborated with classical scholars [to create](https://deepmind.com/blog/article/Predicting-the-past-with-Ithaca) a new AI tool that uses deep neural networks to help historians decipher the text of damaged inscriptions from ancient Greece. The new system, dubbed Ithaca, builds on an earlier text restoration system called Pythia.

Ithaca doesn’t just assist historians in restoring text—it can also identify a text’s location of origin and the date of creation, according to [a new paper](https://www.nature.com/articles/s41586-022-04448-z) the research team published in the journal Nature. In fact, Ithaca has already been used to help resolve an ongoing debate among historians about the correct dates for a group of ancient Athenian decrees. An interactive version of Ithaca is [freely available](https://ithaca.deepmind.com), and the team is making its [code open source](https://github.com/deepmind/ithaca).

Many ancient sources—whether they be written on scrolls, papyri, stone, metal, or pottery—are so damaged that large chunks of text are often illegible. Determining where the texts originated can also be a challenge, since they have likely been moved multiple times. As for accurately determining when they were produced, radiocarbon dating and similar methods can’t be used since they can damage the priceless artifacts. So the daunting and time-consuming task of interpreting these incomplete texts falls to so-called epigraphists who specialize in those skills.

As the folks at DeepMind [wrote in 2019](https://deepmind.com/research/publications/2019/Restoring-ancient-text-using-deep-learning-a-case-study-on-Greek-epigraphy):

One of the issues with discerning meaning from incomplete fragments of text is that there are often multiple possible solutions. In many word games and puzzles, players guess letters to complete a word or phrase—the more letters that are specified, the more constrained the possible solutions become. But unlike these games, where players have to guess a phrase in isolation, historians restoring a text can estimate the likelihood of different possible solutions based on other context clues in the inscription—such as grammatical and linguistic considerations, layout and shape, textual parallels, and historical context.

To help speed up the process, DeepMind’s Yannis Assael, Thea Sommerschield, and Jonathan Prag collaborated with researchers at the University of Oxford to develop Pythia, an ancient-text restoration system named after the [high priestess](https://en.wikipedia.org/wiki/Pythia) who served as the Oracle of Delphi by delivering the pronouncements of the god Apollo.

![Detail from the Chalcis decree](https://cdn.arstechnica.net/wp-content/uploads/2022/03/ithaca5CROP.jpg)

The researchers’ first step was converting the Packard Humanities Institute (PHI) database—the largest digital collection of ancient Greek inscriptions—into machine-actionable text they called PHI-ML. That amounted to about 35,000 inscriptions and more than 3 million words from the 7th century BCE through the 5th century CE. Next, the researchers trained Pythia (with both words and the individual characters as inputs) to predict the missing letters of words in those inscriptions. Pythia was trained to use the pattern-recognition capabilities of deep neural networks.

When faced with an incomplete inscription, Pythia produced as many as 20 different possible letters or words that might fill in the gaps, as well as the confidence level for each possibility. It was up to the historians (i.e., the “domain experts”) to sift through those possibilities and make a final determination based on their subject matter expertise.

The team tested the system by comparing Pythia’s results on completing 2,949 inscriptions with those of Oxford graduate students in epigraphy. Pythia’s output had a 30.1 percent error rate, compared to 57.3 percent error rate for the students. Pythia was also able to complete the task much more quickly, requiring just a few seconds to decipher 50 inscriptions, compared to two hours for the students.

And now Assael and his cohorts are back with Ithaca. In addition to the text restoration capability, Ithaca makes predictions about the geographical attribution of incomplete inscriptions. The probability distribution over all possible predictions is helpfully visualized on a map, “to shed light on possible underlying geographical connections across the ancient world,” the team wrote in [an accompanying blog post](https://deepmind.com/blog/article/Predicting-the-past-with-Ithaca). For chronological attribution, Ithaca produces a distribution of its predicted dates between 800 BCE to 800 CE.

![Restored inscription filling in missing text](https://cdn.arstechnica.net/wp-content/uploads/2022/03/ithaca4.jpg)

Testing revealed that Ithaca on its own is able to achieve 62 percent accuracy in the restoration of damaged text, compared to 25 percent accuracy for human historians. But the combination of man and machine boosts the overall accuracy to 72 percent, which Assael *et al*. believe demonstrates “the potential for human-machine cooperation” in the field. As for attributing inscriptions to their original location, Ithaca can do so with 71 percent accuracy and date the inscriptions to within 30 years.

Ithaca has already had the chance to demonstrate its usefulness to historians in a test case involving a set of Athenian decrees that have been at the center of [a dating controversy](https://www.jstor.org/stable/27564180). Historians had previously pegged the dates of the decrees to no later than 446 BCE. That assessment [was based](https://www.amazon.com/Athenian-Empire-Restored-Epigraphic-Historical/dp/0472106562) on certain letterforms (known as the Attic three-bar sigma) that the Athenian bureaucracy used during this period. After 446 BCE, the Athenians switched to an Ionic four-bar sigma for its decrees.

This was the standard dating methodology for Athenian inscriptions until other historians began to question its assumptions, particularly since several decrees dated this way seemed to conflict with the historical accounts of [Thucydides](https://en.wikipedia.org/wiki/Thucydides). These historians uncovered evidence that the Attic letterform had continued to be used in official documents long after 446 BCE. They concluded that the dates of many of these decrees should be earlier—around 420 BCE. Ithaca predicted a date of 421 BCE, very much in keeping with that conclusion.

![Schematic showing samples of Ithaca's output](https://cdn.arstechnica.net/wp-content/uploads/2022/03/ithaca3.jpg)

“Although it might seem like a small difference, this date shift has significant implications for our understanding of the political history of Classical Athens,” Sommerschield said in a statement. The next step is to develop additional versions of Ithaca that can restore text in other ancient languages, including Akkadian, Demotic, Hebrew, and Mayan.

“This paper represents a very important development in the collaborative use of AI to enhance the restoration, dating, and attribution of inscriptions written in Greek from the ancient world over a period of several centuries,” said Alison Cooley, president of the International Digital Epigraphy Association at the University of Warwick, who is not affiliated with the project. “The innovative design of Ithaca promises to transform the potential contribution of inscribed evidence to our understanding of key moments in world history.”

Roger Bagnall, emeritus professor at New York University (also not affiliated with the project), is enthusiastic about what he terms an extraordinary advance in performance since Pythia, particularly because Ithaca can be extended to other languages. “I can hardly wait to see it applied to the documentary papyri where we have far more precise dating but far more unprovenanced texts, because of the operations of the antiquities market,” he said in a statement. “It should be possible with Ithaca’s help to reconstruct the workings of that market and the original historical context of many more of the thousands of papyrus documents.”

DOI: Nature, 2022. [10.1038/s41586-022-04448-z](http://dx.doi.org/10.1038/s41586-022-04448-z)  ([About DOIs](http://arstechnica.com/science/news/2010/03/dois-and-their-discontents-1.ars)).

Listing image:
Wikimedia/CC BY-SA 3.0

![Photo of Jennifer Ouellette](https://cdn.arstechnica.net/wp-content/uploads/2018/08/arspic300.jpg)
![Loading](https://cdn.arstechnica.net/wp-content/themes/ars-v9/public/images/firework-loader.75ab30.gif)
Loading comments...
![Listing image for first story in Most Read: Amazon stuck with months of repairs after drone strikes on data centers](https://cdn.arstechnica.net/wp-content/uploads/2026/05/GettyImages-2264958756-768x432.jpg)

Ars Technica has been separating the signal from
the noise for over 25 years. With our unique combination of
technical savvy and wide-ranging interest in the technological arts
and sciences, Ars is the trusted source in a sea of information. After
all, you don’t need to know everything, only what’s important.
