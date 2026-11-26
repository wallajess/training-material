---
layout: tutorial_hands_on

title: Phonetic research with MFA, Praat, and new-FAVE
zenodo_link: https://zenodo.org/records/21371207
questions:
- Which biological questions are addressed by the tutorial?
- Which bioinformatics techniques are important to know for this type of data?
objectives:
- The learning objectives are the goals of the tutorial
- They will be informed by your audience and will communicate to them and to yourself
  what you should focus on during the course
- They are single sentences describing what a learner should be able to do once they
  have completed the tutorial
- You can use Bloom's Taxonomy to write effective learning objectives
time_estimation: 3H
key_points:
- The take-home messages
- They will appear at the end of the tutorial
contributors:
- contributor1
- contributor2

---



General introduction about the topic and then an introduction of the
tutorial (the questions and the objectives). It is nice also to have a
scheme to sum up the pipeline used during the tutorial. The idea is to
give to trainees insight into the content of the tutorial and the (theoretical
and technical) key concepts they will learn.

You may want to cite some publications; this can be done by adding citations to the
bibliography file (`tutorial.bib` file next to your `tutorial.md` file). These citations
must be in bibtex format. If you have the DOI for the paper you wish to cite, you can
get the corresponding bibtex entry using [doi2bib.org](https://doi2bib.org).

With the example you will find in the `tutorial.bib` file, you can add a citation to
this article here in your tutorial like this:
{% raw %} `{% cite Batut2018 %}`{% endraw %}.
This will be rendered like this: {% cite Batut2018 %}, and links to a
[bibliography section](#bibliography) which will automatically be created at the end of the
tutorial.

<!-- This is a comment. -->

**Please follow our
[tutorial to learn how to fill the Markdown]({{ site.baseurl }}/topics/contributing/tutorials/create-new-tutorial-content/tutorial.html)**

> <agenda-title></agenda-title>
>
> In this tutorial, we will cover:
>
> 1. TOC
> {:toc}
>
{: .agenda}

# Title for your first section

Give some background about what the trainees will be doing in the section.
Remember that many people reading your materials will likely be novices,
so make sure to explain all the relevant concepts.

## Title for a subsection
Section and subsection titles will be displayed in the tutorial index on the left side of
the page, so try to make them informative and concise!

# Hands-on Sections
Below are a series of hand-on boxes, one for each tool in your workflow file.
Often you may wish to combine several boxes into one or make other adjustments such
as breaking the tutorial into sections, we encourage you to make such changes as you
see fit, this is just a starting point :)

Anywhere you find the word "***TODO***", there is something that needs to be changed
depending on the specifics of your tutorial.

have fun!

## Get data

> <hands-on-title> Data Upload </hands-on-title>
>
> 1. Create a new history for this tutorial
> 2. Import the files from [Zenodo]({{ page.zenodo_link }}) or from
>    the shared data library (`GTN - Material` -> `{{ page.topic_name }}`
>     -> `{{ page.title }}`):
>
>    ```
>    https://zenodo.org/api/records/21371207/files/the_fox_and_the_grapes.zip/content
>    ```
>    ***TODO***: *Add the files by the ones on Zenodo here (if not added)*
>
>    ***TODO***: *Remove the useless files (if added)*
>
>    {% snippet faqs/galaxy/datasets_import_via_link.md %}
>
>    {% snippet faqs/galaxy/datasets_import_from_data_library.md %}
>
> 3. Rename the datasets
> 4. Check that the datatype
>
>    {% snippet faqs/galaxy/datasets_change_datatype.md datatype="datatypes" %}
>
> 5. Add to each database a tag corresponding to ...
>
>    {% snippet faqs/galaxy/datasets_add_tag.md %}
>
{: .hands_on}

# Title of the section usually corresponding to a big step in the analysis

It comes first a description of the step: some background and some theory.
Some image can be added there to support the theory explanation:

![Alternative text](../../images/image_name "Legend of the image")

The idea is to keep the theory description before quite simple to focus more on the practical part.

***TODO***: *Consider adding a detail box to expand the theory*

> <details-title> More details about the theory </details-title>
>
> But to describe more details, it is possible to use the detail boxes which are expandable
>
{: .details}

A big step can have several subsections or sub steps:


## Sub-step with **MFA Find OOVs**

> <hands-on-title> Task description </hands-on-title>
>
> 1. {% tool [MFA Find OOVs](toolshed.g2.bx.psu.edu/repos/bgruening/mfa_find_oovs/mfa_find_oovs/3.4.2+0) %} with the following parameters:
>    - *"Corpus Source"*: `Single Audio + Transcript Files`
>        - {% icon param-file %} *"Audio File"*: `output` (Input dataset)
>        - {% icon param-file %} *"Transcript File"*: `output` (Input dataset)
>    - *"Dictionary Source"*: `Use a built-in MFA Dictionary`
>        - *"Select Dictionary"*: `English Us (ARPA)`
>
>    ***TODO***: *Check parameter descriptions*
>
>    ***TODO***: *Consider adding a comment or tip box*
>
>    > <comment-title> short description </comment-title>
>    >
>    > A comment about the tool or something else. This box can also be in the main text
>    {: .comment}
>
{: .hands_on}

***TODO***: *Consider adding a question to test the learners understanding of the previous exercise*

> <question-title></question-title>
>
> 1. Question1?
> 2. Question2?
>
> > <solution-title></solution-title>
> >
> > 1. Answer for question1
> > 2. Answer for question2
> >
> {: .solution}
>
{: .question}

## Sub-step with **MFA G2P**

> <hands-on-title> Task description </hands-on-title>
>
> 1. {% tool [MFA G2P](toolshed.g2.bx.psu.edu/repos/bgruening/mfa_g2p/mfa_g2p/3.4.2+0) %} with the following parameters:
>    - *"Input Mode"*: `Word List (Text File)`
>        - {% icon param-file %} *"Word List"*: `oovs_found` (output of **MFA Find OOVs** {% icon tool %})
>    - *"G2P Model Source"*: `Use a built-in MFA Model`
>        - *"Select G2P Model"*: `English Us (ARPA)`
>
>    ***TODO***: *Check parameter descriptions*
>
>    ***TODO***: *Consider adding a comment or tip box*
>
>    > <comment-title> short description </comment-title>
>    >
>    > A comment about the tool or something else. This box can also be in the main text
>    {: .comment}
>
{: .hands_on}

***TODO***: *Consider adding a question to test the learners understanding of the previous exercise*

> <question-title></question-title>
>
> 1. Question1?
> 2. Question2?
>
> > <solution-title></solution-title>
> >
> > 1. Answer for question1
> > 2. Answer for question2
> >
> {: .solution}
>
{: .question}

## Sub-step with **MFA Merge**

> <hands-on-title> Task description </hands-on-title>
>
> 1. {% tool [MFA Merge](toolshed.g2.bx.psu.edu/repos/bgruening/mfa_merge/mfa_merge/3.4.2+0) %} with the following parameters:
>    - *"Dictionary Source"*: `Use a built-in MFA Dictionary`
>        - *"Select Dictionary"*: `English Us (ARPA)`
>    - In *"Dictionary to add"*:
>        - {% icon param-repeat %} *"Insert Dictionary to add"*
>            - {% icon param-file %} *"MFA dictionary"*: `output_dictionary` (output of **MFA G2P** {% icon tool %})
>
>    ***TODO***: *Check parameter descriptions*
>
>    ***TODO***: *Consider adding a comment or tip box*
>
>    > <comment-title> short description </comment-title>
>    >
>    > A comment about the tool or something else. This box can also be in the main text
>    {: .comment}
>
{: .hands_on}

***TODO***: *Consider adding a question to test the learners understanding of the previous exercise*

> <question-title></question-title>
>
> 1. Question1?
> 2. Question2?
>
> > <solution-title></solution-title>
> >
> > 1. Answer for question1
> > 2. Answer for question2
> >
> {: .solution}
>
{: .question}

## Sub-step with **MFA Align**

> <hands-on-title> Task description </hands-on-title>
>
> 1. {% tool [MFA Align](toolshed.g2.bx.psu.edu/repos/bgruening/mfa_align/mfa_align/3.4.2+0) %} with the following parameters:
>    - *"Corpus Source"*: `Single Audio + Transcript Files`
>        - {% icon param-file %} *"Audio File"*: `output` (Input dataset)
>        - {% icon param-file %} *"Transcript File"*: `output` (Input dataset)
>    - *"Dictionary Source"*: `Upload from History`
>        - {% icon param-file %} *"MFA dictionary"*: `merged_dict` (output of **MFA Merge** {% icon tool %})
>    - *"Acoustic Model Source"*: `Use a built-in MFA Model`
>        - *"Select Acoustic Model"*: `English Us (ARPA)`
>
>    ***TODO***: *Check parameter descriptions*
>
>    ***TODO***: *Consider adding a comment or tip box*
>
>    > <comment-title> short description </comment-title>
>    >
>    > A comment about the tool or something else. This box can also be in the main text
>    {: .comment}
>
{: .hands_on}

***TODO***: *Consider adding a question to test the learners understanding of the previous exercise*

> <question-title></question-title>
>
> 1. Question1?
> 2. Question2?
>
> > <solution-title></solution-title>
> >
> > 1. Answer for question1
> > 2. Answer for question2
> >
> {: .solution}
>
{: .question}

## Sub-step with **Unzip**

> <hands-on-title> Task description </hands-on-title>
>
> 1. {% tool [Unzip](toolshed.g2.bx.psu.edu/repos/imgteam/unzip/unzip/6.0+galaxy5) %} with the following parameters:
>    - {% icon param-file %} *"Input file"*: `output_archive` (output of **MFA Align** {% icon tool %})
>    - *"What to extract"*: `All files`
>
>    ***TODO***: *Check parameter descriptions*
>
>    ***TODO***: *Consider adding a comment or tip box*
>
>    > <comment-title> short description </comment-title>
>    >
>    > A comment about the tool or something else. This box can also be in the main text
>    {: .comment}
>
{: .hands_on}

***TODO***: *Consider adding a question to test the learners understanding of the previous exercise*

> <question-title></question-title>
>
> 1. Question1?
> 2. Question2?
>
> > <solution-title></solution-title>
> >
> > 1. Answer for question1
> > 2. Answer for question2
> >
> {: .solution}
>
{: .question}

## Sub-step with **Praat**

> <hands-on-title> Task description </hands-on-title>
>
> 1. {% tool [Praat](interactive_tool_praat) %} with the following parameters:
>    - {% icon param-file %} *"Audio File"*: `output` (Input dataset)
>    - {% icon param-file %} *"Transcript File"*: `unzipped` (output of **Unzip** {% icon tool %})
>
>    ***TODO***: *Check parameter descriptions*
>
>    ***TODO***: *Consider adding a comment or tip box*
>
>    > <comment-title> short description </comment-title>
>    >
>    > A comment about the tool or something else. This box can also be in the main text
>    {: .comment}
>
{: .hands_on}

***TODO***: *Consider adding a question to test the learners understanding of the previous exercise*

> <question-title></question-title>
>
> 1. Question1?
> 2. Question2?
>
> > <solution-title></solution-title>
> >
> > 1. Answer for question1
> > 2. Answer for question2
> >
> {: .solution}
>
{: .question}

## Sub-step with **Vowel formant extraction**

> <hands-on-title> Task description </hands-on-title>
>
> 1. {% tool [Vowel formant extraction](toolshed.g2.bx.psu.edu/repos/bgruening/new_fave_extract/new_fave_extract/1.3.0+galaxy0) %} with the following parameters:
>    - {% icon param-file %} *"Audio input"*: `output` (Input dataset)
>    - {% icon param-file %} *"Aligned grid of transcribed text"*: `outputs` (output of **Praat** {% icon tool %})
>
>    ***TODO***: *Check parameter descriptions*
>
>    ***TODO***: *Consider adding a comment or tip box*
>
>    > <comment-title> short description </comment-title>
>    >
>    > A comment about the tool or something else. This box can also be in the main text
>    {: .comment}
>
{: .hands_on}

***TODO***: *Consider adding a question to test the learners understanding of the previous exercise*

> <question-title></question-title>
>
> 1. Question1?
> 2. Question2?
>
> > <solution-title></solution-title>
> >
> > 1. Answer for question1
> > 2. Answer for question2
> >
> {: .solution}
>
{: .question}


## Re-arrange

To create the template, each step of the workflow had its own subsection.

***TODO***: *Re-arrange the generated subsections into sections or other subsections.
Consider merging some hands-on boxes to have a meaningful flow of the analyses*

# Conclusion

Sum up the tutorial and the key takeaways here. We encourage adding an overview image of the
pipeline used.