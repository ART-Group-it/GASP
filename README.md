# GASP! Generating Abstracts of Scientific Papers from Abstracts of Cited Papers
This repository contains the GASP dataset.

GASP is a dataset composed by list of cited abstracts associated with the corresponding source abstract.

The goal is to generete a paper abstract give cited paper's abstracts and model the human creativity behind the process.

## GASP! Motivation

Creativity is one of the driving forces of human kind as it allows to break current understanding to envision new ideas, which may revolutionize entire fields of knowledge. Scientific research offers a challenging environment where to learn creativity. In fact, scientific research is a creative act in the formal settings of the scientific method and this creative act is describe in articles.

Here, we dare to introduce the novel, scientifically and philosophically challenging task of Generating Abstracts of Scientific Papers from abstracts of cited papers (GASP) as a text-to-text task to investigate scientific creativity, To foster research in this novel, challenging task, we prepared a dataset by using services where that solve the problem of copyright and, hence, the dataset is public available with its standard split.  Finally, we experimented with three vanilla summarization systems to start the analysis of the complexity of the GASP task.


## GASP! The dataset 


The GASP task is aimed to producing the target abstract of a paper `"output_paper"` given the abstracts of the set of referred papers `"input_papers"`. This latter is a list of abstracts, which we may assume have been inspirational for the idea in the target paper.

The dataset is composed by a training set of 100000 elements, a test set and a validation set of 10000 each.

Each set is a `.json` file composed by a list of elements following the structure below:
```
[{
	 "input_papers": [
	 		"CONTEXT Mentoring, as a partnership ...  issues, and using cross-disciplinary approaches.", 
	 		"PROBLEM AND BACKGROUND In 1998, the University of ... retention in academic medicine.", 
			"PURPOSE To determine (1) the prevalence of ... deliberate approach to the practice of mentoring.",
			 ...], 
	 "output_paper": "The purpose of this article is to ... proposed next steps for research in this area.",
	 "output_id": "363801205efb14a28dea8cbcdc86afc2eb908f53"
 },
 ...
 ]
```
Where:
- `"input_papers"` is a variable lenght list of string of papers
- `"output_paper"` is the text of the output paper (string)
- `"output_id"`is the S2 Paper ID of the output paper that can be used to look for additional information with <a href="https://api.semanticscholar.org/">Semantic Scholar API</a>


## GASP! Download

The corpus is available to download at <a href="https://bitbucket.org/fabiomassimozanzotto/gasp/raw/54d25cbc28f5da3e7233330e825bf365d065c200/Gasp%20corpus.zip"> this address </a>

## GASP! Cite

Please, if you use the GASP dataset cite:

```
@cite
```

## GASP! License

GASP dataset is licensed under <a href="https://opendatacommons.org/licenses/by/1.0/">ODC-BY</a>.

### Dataset Metadata
The following table is necessary for this dataset to be indexed by search
engines such as <a href="https://g.co/datasetsearch">Google Dataset Search</a>.
<div itemscope itemtype="http://schema.org/Dataset">
<table>
  <tr>
    <th>property</th>
    <th>value</th>
  </tr>
  <tr>
    <td>name</td>
    <td><code itemprop="name">Generating Abstracts of Scientific Papers from Abstracts of Cited Papers</code></td>
  </tr>
  <tr>
    <td>alternateName</td>
    <td><code itemprop="alternateName">GASP</code></td>
  </tr>
  <tr>
    <td>url</td>
    <td><code itemprop="url">https://github.com/ART-Group-it/GASP</code></td>
  </tr>
  <tr>
    <td>sameAs</td>
    <td><code itemprop="sameAs">https://github.com/ART-Group-it/GASP</code></td>
  </tr>
  <tr>
    <td>description</td>
    <td><code itemprop="description">The dataset consists of list of cited abstracts associated with the corresponding source abstract. The goal is to generete a paper abstract give cited paper's abstracts.</code></td>
  </tr>
  <tr>
    <td>provider</td>
    <td>
      <div itemscope itemtype="http://schema.org/Organization" itemprop="provider">
        <table>
          <tr>
            <th>property</th>
            <th>value</th>
          </tr>
          <tr>
            <td>name</td>
            <td><code itemprop="name">University of Roma Tor Vergata</code></td>
          </tr>
          <tr>
            <td>sameAs</td>
            <td><code itemprop="sameAs">https://en.wikipedia.org/wiki/University_of_Rome_Tor_Vergata</code></td>
          </tr>
        </table>
      </div>
    </td>
  </tr>
  <tr>
    <td>citation</td>
    <td><code itemprop="citation">https://identifiers.org/arxiv:1909.05855</code></td>
  </tr>
</table>
</div>
