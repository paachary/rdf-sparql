# rdf-sparql
Contains sample rdf graphical data representation &amp; data set and sparql queries.

### Note
This exercise uses blazegraph database to insert the graph data and execute the SPARQL queries

## Initial Steps

1. Please ensure you have Java JDK 8 installed (Java version 1.8). Please work with techworks team to get it installed if not already installed.

2. Please download blazegraph database jar using [this link](https://github.com/blazegraph/database/releases/download/BLAZEGRAPH_2_1_6_RC/blazegraph.jar)

3. Copy this jar file into a folder on your desktop:
         Example: c:/Users/<corpid>/<blazegraphdb>

4. Run the following command in the directory containing the jar file:
         java -server -Xmx4g -jar blazegraph.jar

5. If the command succeeds, you should see the endpoint of the blazegraph.

6. Navigating to that link will provide a UI to access the local blazegraph database running on your desktop
         
## Setting up the initial data
We will be using the blzegraph to insert our graph and query from it to answer some questions.
         
For this, we are using a simple graphical representation of data shown below: ![alt text](https://github.com/paachary/rdf-sparql/blob/main/RDF-Graph-Representation-Person-Example.jpg "attached jpeg file link")

### Inserting the data
Load the [person-data-graph.ttl](https://github.com/paachary/rdf-sparql/blob/main/person-data-graph.ttl) file into the blazegraph tool under the UPDATE menu. Choose file type as RDF and Turtle.

### Querying the data
You can try to answer the questions in [person-data-graph.query](https://github.com/paachary/rdf-sparql/blob/main/person-data-graph.query) using SPARQL under the QUERY menu of the tool. 

### Verify your queries
You can use the file [solutions.query](https://github.com/paachary/rdf-sparql/blob/main/solutions.query) to refer to the answers to the questions.

## Getting the endpoint for blazegraph for further development
RDF Sparql queries can be written programitcally in python, java and Jupyter notebook using the blazegraph endpoint:
```python
         endpoint:  http://localhost:9999/bigdata/sparql
```

## Visualizing graph using Jupyter Notebook and Sparqlkernel

### Install Jupyter Notebook and Sparqlkernel on your unix box
Note: These commands have been run on Ubuntu 20.04 OS

More information on Sparqlkernel can be found in [this repository](https://github.com/riccardotommasini/rsp-kernel)
This assumes python3 is already installed on your machine.
```python
       pip install sparqlkernel
       pip install notebook
       jupyter sparqlkernel install  
```

Install Graphviz library for the visulation to work on Jupyter.
```python
   ## On Ubuntu:
   sudo apt install graphviz

   ## On EC2 Linux:
   sudo yum install graphviz
```

### Open the jupyter notebook and run the Sparql kernel
```python
   jupyter notebook
```

Example can be viewed through the [online Notebook viewer](https://nbviewer.jupyter.org/github/paachary/rdf-sparql/blob/main/jupyter-notebook-graph-example.ipynb).

         
