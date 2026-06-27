
## Project Report Template

> This repository serves as a template for your project reports as part of the Document Analysis lecture. To set up your project report as a webpage using GitHub Pages, simply follow the steps outlined in the next chapter.
>
>**Some Organizational Details:** Get creative with your project ideas! Just make sure they relate to Natural Language Processing and incorporate this specified dataset: [Link to data](https://huggingface.co/datasets/webis/tldr-17), [Link to paper](https://aclanthology.org/W17-4508.pdf). Submissions should be made in teams of 2-3 students. Each team is expected to create a blog-style project website, using GitHub Pages, to present their findings. Additionally, teams will deliver a lightning talk during the final lecture to discuss their project. Add all your code, such as Python scripts and Jupyter notebooks, to the `code` folder. Use markdown files for your project report. [Here](https://docs.gitlab.com/ee/user/markdown.html) you can read about how to format Markdown documents. 
>
>Have fun working on your project! 🥳

## Setup The Report Template

Follow this steps to set up your project report:

1. **Fork the Repository:** Begin by creating a copy of this repository for your own use. Click the `Fork` button at the top right corner of this page to do this.

2. **Configure GitHub Pages:** Navigate to `Settings` -> `Pages` in your newly forked repository. Under the `Branch` section, change from `None` to `master` and then click `Save`.

3. **Customize Configuration:** Modify the `_config.yml` file within your repository to personalize your site. Update the `title:` to reflect the title of your project and adjust the `description:` to provide a brief summary.

4. **Start Writing:** Start writing your report by modifying the `README.md`. You can also add new Markdown files for additional pages by modifying the `_config.yml` file. Use the standard [GitHub Markdown syntax](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax) for formatting. 

5. **Access Your Site:** Return to `Settings` -> `Pages` in your repository to find the URL to your live site. It typically takes a few minutes for GitHub Pages to build and publish your site after updates. The URL to access your live site follows this schema: `https://<<username>>.github.io/<<repository_name>>/`

***

# Expressive Punctuation Patterns

_Group members: Oksana Melnyk, Deanne Julia Luis
## Introduction

In everyday life our communication is filled with emotions which are expressed not only verbally through words but also through prosodic cues such as intonation and pitch as well as non-verbally through facial expressions, gestures or posture. However, with the spread of technologies, an increasing amount of everyday communication has moved into online space as informal written interaction. Between late 1990s and 2026 online communication changed drastically from a specialised channel of communications used by technologically privileged groups into a mass means of communication accessible to a larger part (75%) of the world’s population (Statistics, n.d.). 
![Individul using the Internet, 2006-2026](InternetUse2006-2025.png)

The need to express your emotions in written digital communication has not disappeared so new means for it have been developed, such es emoticons or existing means have acquired a new pragmatic function such as punctuation marks. Punctuation has become “a device for organizing written interactions sequentially and establishing shared meanings between participants” (Busch, 2021, p. 2).

While traditionally punctuation is removed during preprocessing in natural language processing tasks to simplify textual data, this can discard important information necessary for deep language understanding. In addition to its grammatical and communicative functions, punctuation may provide insight into stylistic features associated with particular authors and genres. It is considered as a ‘supra-linguistic’ representational system which is not fully and may never be standardised (Darmon et al., 2021, p. 1072). From this perspective, the detection of characteristic punctuation patterns through quantitative analysis may reveal information about emotional context, authorship, or communicative style. Such an approach belongs to stylometry, as it treats punctuation as a measurable feature of textual style (Darmon et al., 2021, p. 1070).

Punctuation patterns in Reddit topics are the focus of this project. In our project we want to investigate *how reddit topics differ in their use of expressive punctuation*. In order to answer this question we *first* identify punctuation patterns across subreddits. We consider subreddits as proxies for Reddit topics, assuming that each subreddit broadly represents a specific thematic community or area of discussion. *Secondly,* we analyse what expressive functions these punctuation patters may indicate. *Finally,* examine whether punctuation features can predict community specific topics or subreddit categories.

## Theoretical Framework

Punctuation marks can serve as graphic cues that contribute to the emotional expressiveness of a written digital message and to positioning in digital discourse. These cues are constantly developing and changing, enabling users to express complex interpersonal meanings in digital interaction (Androutsopoulos, 2023; Busch, 2021). They can also influence the valence, that is, the emotional direction, of a message (Glauch, 2025).

## Key Expressive Punctuation Marks and Their Meanings
### Period / Full Stop (.)

Apart from its formal function of ending a sentence or message, the full stop can convey a range of meanings in digital communication. A message ending with a full stop may signal a lower level of excitement or emphasis. It may also make a message appear more serious or thoughtful (Albritton, 2022). For the reader, such a message may also seem less sincere or more abrupt compared with the same message without a period (Gunraj et al., 2016; Reynolds et al., 2017). This is especially relevant for very short messages, such as “yes.” Although the lexical meaning of yes expresses agreement, the final period may change the perceived valence of the message and suggest annoyance, seriousness, or, in some contexts, anger. However, in longer messages of more than six words, the negative effect of the period disappears (Kemp et al., 2025).

### Exclamation Mark (!) and Repetition (!!!)

Unlike the period, which originally had a predominantly syntactic function, the exclamation mark is considered a communicative sign oriented toward participants’ stances. However, it has also undergone functional shifts, the most obvious of which is intentional repetition (Busch, 2021, p. 6).

The exclamation mark functions as an intensifier of emotion expressed in a message, whether positive or negative. It is assumed that a single exclamation mark does not usually change the valence of a message (Glauch, 2025, p. 185). For example, “It’s funny!” does not convey an emotion different from the one already expressed by the semantic content of the message; rather, it strengthens it.

Repeatability is a typical characteristic of expressive meaning. The repeated use of exclamation marks (!!!) is not redundant; instead, it increases the expressive function that the exclamation mark already has. However, repetition can potentially change the emotional force or perceived direction of a message (Busch, 2021; Glauch, 2025). One variation of repeated exclamation marks is the indignation mark, a combination of the exclamation mark <!> and the digit <1>, such as <!1!!>, <!!11!>, or <!!1!11>. The pragmatic meaning of this graphic cue is often associated with mockery and sarcasm (Androutsopoulos, 2023).

### Ellipsis (...)

Traditionally, ellipsis marks express omission or an unfinished thought, but in digital communication they may also express hesitation, continuation, or emotional distance. They can create a feeling of pause or delayed response (Albritton, 2017). It is considered as a neutral mark (Reynolds et al., 2017), not changing the emotional direction of a message. However, its pragmatic function depends strongly on context and position.

Ong’s findings (2011) indicate that stand-alone ellipsis marks can signal confusion, lack of understanding, or disagreement with a previous utterance, especially when they occur after an earlier sequence of explicit disagreement. The position of the ellipsis can also change its pragmatic function. Ellipses occur most often in the middle of contributions, where they function as general-purpose segmenters, often replacing commas or periods. Message-final ellipses, by contrast, often indicate openness, continuation, or shared background knowledge. Stand-alone ellipses can express speechlessness, disappointment, silent agreement, or interpersonal alignment (Androutsopoulos, 2020).

### Repeated Question Marks (???)

Repeated question marks almost never convey only the interrogative character of a message. Instead, they often signal that the writer perceives the issue as urgent, emotionally loaded, or important. In this context, multiple question marks can express impatience, surprise, concern, or heightened involvement (Sidi et al., 2021).

Repeated question marks do not necessarily change the emotional direction of the message itself, but they can influence how the message and the writer are evaluated. Depending on the perspective of the writer or receiver, they may be interpreted as neutral expressive markers or as negative cues, indicating writer's impatience, disbelief, shock, anger, or even reduced competence (Kruger, 2023; Sidi et al., 2021).


## Dataset

Provide a short description of the dataset used in your project. Focus on highlighting the aspects that are particularly relevant to your work.

## Methods

### Setup 


Outline the tools, software, and hardware environment, along with configurations used for conducting your experiments. Be sure to document the Python version and other dependencies clearly. Provide step-by-step instructions on how to recreate your environment, ensuring anyone can replicate your setup with ease:

```bash
conda create --name myenv python=<version>
conda activate myenv
```

Include a `requirements.txt` file in your project repository. This file should list all the Python libraries and their versions needed to run the project. Provide instructions on how to install these dependencies using pip, for example:

```bash
pip install -r requirements.txt
```

### Experiments

Report how you conducted the experiments. We suggest including detailed explanations of the preprocessing steps and model training in your project. For the preprocessing, describe  data cleaning, normalization, or transformation steps you applied to prepare the dataset, along with the reasons for choosing these methods. In the section on model training, explain the methodologies and algorithms you used, detail the parameter settings and training protocols, and describe any measures taken to ensure the validity of the models.

## Results and Discussion

Present the findings from your experiments, supported by visual or statistical evidence. Discuss how these results address your main research question.

## Conclusion

Summarize the major outcomes of your project, reflect on the research findings, and clearly state the conclusions you've drawn from the study.

## Contributions

| Team Member        | Contributions                                             |
|--------------------|-----------------------------------------------------------|
| Oksana Melnyk      |                                                           |
| Deanne Julia Luis  | ...                                                       |

## References
- Albritton, A. (2017). A Rhetorical Model of Punctuation Mark Function in Computer-Mediated Communication. International Journal of Linguistics, Literature and     Culture, 4(1), 17–29.
- Albritton, A. (2021). What’s the Point? A Study of Full-Stop Use in Text Messages in Varying Emotional Contexts. Online Journal of Communication and Media   Technologies, 12(1), e202203. https://doi.org/10.30935/ojcmt/11431
- Androutsopoulos, J. (2020). Auslassungspunkte in der schriftbasierten Interaktion. In J. Androutsopoulos & F. Busch (Eds), Register des Graphischen (pp. 133–158). De Gruyter. https://doi.org/10.1515/9783110673241-006
- Androutsopoulos, J. (2023). Punctuating the other: Graphic cues, voice, and positioning in digital discourse. Language & Communication, 88, 141–152. https://doi.org/10.1016/j.langcom.2022.11.004
- Busch, F. (2021). The interactional principle in digital punctuation. Discourse, Context & Media, 40, 100481. https://doi.org/10.1016/j.dcm.2021.100481
- Darmon, A. N. M., Bazzi, M., Howison, S. D., & Porter, M. A. (2021). Pull out all the stops: Textual analysis via punctuation sequences. European Journal of Applied Mathematics, 32(6), 1069–1105. https://doi.org/10.1017/S0956792520000157
- Glauch, K. (2025). Expressive punctuation: How punctuation changes the perceived valence of discourse referents in computer-mediated communication. Linguistische Berichte (LB), 2025(282), 47–81. https://doi.org/10.46771/9783967699470_2
- Gunraj, D. N., Drumm-Hewitt, A. M., Dashow, E. M., Upadhyay, S. S. N., & Klin, C. M. (2016). Texting insincerely: The role of the period in text messaging. Computers in Human Behavior, 55, 1067–1075. https://doi.org/10.1016/j.chb.2015.11.003
- Kemp, N., Kovacic, R., & Beyersmann, E. (2025). Is the period really “pissed”? The effect of punctuation and message length on perceptions in digital communication. Telematics and Informatics, 97(102241), 1–8. https://doi.org/10.1016/j.tele.2025.102241
- Kruger, L. (2023, November 30). Question marks in user-generated comments on Afrikaans websites: A corpus linguistic study - LitNet. LitNet - Die Boekehuis Met Baie Wonings. https://www.litnet.co.za/question-marks-in-user-generated-comments-on-afrikaans-websites-a-corpus-linguistic-study/
- Ong, K. (2011). Disagreement, confusion, disapproval, turn elicitation and floor holding: Actions as accomplished by ellipsis marks-only turns and blank turns in quasisynchronous chats. Discourse Studies - DISCOURSE STUD, 13, 211–234. https://doi.org/10.1177/1461445610392138
- Reynolds, K., Casarotto, B., Noviski, S., & Roche, J. M. (2017). Using punctuation as a marker of sincerity and affective convergence during texting. Proceedings of the Annual Meeting of the Cognitive Science Society, 39(0). https://escholarship.org/uc/item/6mw7v01s
- Sidi, Y., Glikson, E., & Cheshin, A. (2021). Do You Get What I Mean?!? The Undesirable Outcomes of (Ab)Using Paralinguistic Cues in Computer-Mediated Communication. Frontiers in Psychology, 12. https://doi.org/10.3389/fpsyg.2021.658844
- Statistics. (n.d.). ITU. Retrieved 21 June 2026, from https://www.itu.int:443/en/ITU-D/Statistics/pages/stat/default.aspx



Include a list of academic and professional sources you cited in your report, using an appropriate citation format to ensure clarity and proper attribution.

