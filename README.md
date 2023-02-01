# Applied AI Student Project with metaphacts
## Folder description
### Embeddings for Concepts only
<p> In this folder are: </p>
<ol>
  <li> Samples (The CSV files for the entities and also the number of publications)</li>
  <li> Outcomes (The Turtle file with the embeddings)</li>
  <li> Jupyter-Notebook (Created code for the calculation of the embeddings and for the preparation of the visualisation)</li>
</ol>

### Embeddings for Publications & related Publications
<p> In this folder are: </p>
<ol>
  <li> Samples (The CSV files for the entities and also the number of publications)</li>
  <li> Outcomes (The Turtle file with the embeddings)</li>
  <li> Jupyter-Notebook (Created code for the calculation of the embeddings and for the preparation of the visualisation)</li>
</ol>

### Embeddings for Publications only
<p> In this folder are: </p>
<ol>
  <li> Samples (The CSV files for the entities and also the number of publications)</li>
  <li> Outcomes (The Turtle file with the embeddings)</li>
  <li> Jupyter-Notebook (Created code for the calculation of the embeddings and for the preparation of the visualisation)</li>
</ol>

### Visualization
<p>In this folder an html file is stored that contains the template of the visualisation in the metaphactory</p>

### pyRDF2Vec modified

<p>For the calculation of the embeddings we used pyRDF2Vec. <br>
For the calculation itself, you have to define the Knowledge Graph, for which there are 3 variants (see: <a href="https://github.com/IBCNServices/pyRDF2Vec#use-a-knowledge-graph">Knowledge Graph Definition </a>). We use the variant via the endpoint.</p>
<b>The problem is that some of the code in the library is out of date.</b>
<p>To fix the problem, replace the obsolete code in the <a href="https://github.com/Cress8/aki_student_project_metaphacts/blob/main/pyRDF2Vec%20modified/pyrdf2vec/connectors.py">Connectors file</a> as follows:</p>
<p>In code line 117, the <b>"/query?query"</b>:</p>

```python
url = f"{self.endpoint}/query?query={parse.quote(query)}"
```

<p> must be changed to <b>"?query"</b>:</p>

```python
url = f"{self.endpoint}?query={parse.quote(query)}"
```

<p> The same in line 132 and press <b>CTRL + S </b> to save the file</p>


