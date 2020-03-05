# GASP! Generating Abstracts of Scientific Papers from Abstracts of Cited Papers
This repository contains the GASP dataset.

GASP is a dataset composed by list of cited abstracts associated with the corresponding source abstract.

The goal is to generete a paper abstract give cited paper's abstracts and model the human creativity behind the process.

## GASP! Motivation

Creativity is one of the driving forces of human kind as it allows to break current understanding to envision new ideas, which may revolutionize entire fields of knowledge. Scientific research offers a challenging environment where to learn creativity. In fact, scientific research is a creative act in the formal settings of the scientific method and this creative act is describe in articles.

Here, we dare to introduce the novel as well as scientifically and philosophically challenging task of Generating Abstracts of Scientific Papers from the abstracts of their citations (GASP) as a text-to-text rewriting task to investigate scientific creativity. To foster research about this original challenge, we set up an annotated dataset by using services that solved the copyrighht problems. As a result, the dataset is publicly available and offers examples of real papers and a reference training-test split. Finally, three vanilla summarization systems have been already applied to the dataset whose outcomes allowed to early measure the GASP task complexity.


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

More information in the <a href="http://doi.org/10.13140/RG.2.2.20755.22562">paper</a> 

## GASP! Download

The corpus is available to download from the <a href="http://art.uniroma2.it/zanzotto/datasets/GASP_corpus_v1.0.zip">ART Site</a>

## GASP! Cite

Please, if you use the GASP dataset cite:

```
@article{Zanzotto_Bono_Vocca_Santilli_Croce_Gambosi_Basili_2020, 
	title={GASP! Generating Abstracts of Scientific Papers from Abstracts of Cited Papers}, 
	url={http://rgdoi.net/10.13140/RG.2.2.20755.22562}, 
	DOI={10.13140/RG.2.2.20755.22562}, 
	author={Zanzotto, Fabio Massimo and Bono, Viviana and Vocca, Paola and 
	        Santilli, Andrea and Croce, Danilo and Gambosi, Giorgio and Basili, Roberto}, 
	year={2020} }
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
    <td><code itemprop="description">The dataset consists of list of cited abstracts associated with the corresponding source abstract. The goal is to generete the abstract of a target paper given the abstracts of cited papers.</code></td>
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
    <td><code itemprop="citation">http://doi.org/10.13140/RG.2.2.20755.22562</code></td>
  </tr>
</table>
</div>

## GASP! contacts 
If you have comments, suggestions or you want to communicate results, please contact:

<a href="mailto:fabio.massimo.zanzotto@uniroma2.it">fabio.massimo.zanzotto@uniroma2.it</a>


## GASP! underlying project(s)

GASP! is a result of research in this project: <a href="http://HitAI.org"><b>HitAI.org</b>Human-in-the-loop Artificial Intelligence</a> 
