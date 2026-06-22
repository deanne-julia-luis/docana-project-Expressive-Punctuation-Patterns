
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

The need to express your emotions in written digital communication has not disappeared so new means for it have been developed, such es emoticons or existing means have acquired new meanings such as punctuation marks. Punctuation has acquired a new function - communicative, it has become “a device for organizing written interactions sequentially and establishing shared meanings between participants” (Busch, 2021, p. 2).

While traditionally punctuation is removed during preprocessing in natural language processing tasks to simplify textual data, this can discard important information necessary for deep language understanding. In addition to its grammatical and communicative functions, punctuation may provide insight into stylistic features associated with particular authors and genres. It is considered as a ‘supra-linguistic’ representational system which is not fully and may never be standardised (Darmon et al., 2021, p. 1072). From this perspective, the detection of characteristic punctuation patterns through quantitative analysis may reveal information about emotional context, authorship, or communicative style. Such an approach belongs to stylometry, as it treats punctuation as a measurable feature of textual style (Darmon et al., 2021, p. 1070).

Punctuation patterns in Reddit topics are the focus of this project. In our project we want to investigate *how reddit topics differ in their use of expressive punctuation*. In order to answer this question we *first* identify punctuation patterns across subreddits. We consider subreddits as proxies for Reddit topics, assuming that each subreddit broadly represents a specific thematic community or area of discussion. *Secondly,* we analyse what expressive functions these punctuation patters may indicate. *Finally,* examine whether punctuation features can predict community specific topics or subreddit categories.


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

Include a list of academic and professional sources you cited in your report, using an appropriate citation format to ensure clarity and proper attribution.

