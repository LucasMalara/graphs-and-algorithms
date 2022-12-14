
# GRAPHS AND ALGORITHMS

<p align="justify">
The present repository you browse contains <b>GRAPHS_AND_ALGORITHMS</b> project. The project is built using 
<code>Maven</code> software for project management and the code is written in <code>Java 14</code>.
</p>

Project versions:
- `1.0-beta` - For diploma thesis (unshared to this repository)
- `1.0` - Current release

## Purpose

The project was focused on:

- implementation of unweighted undirected graphs that cannot have multiple edges nor loops.
- implementation of chosen algorithms involved with graph structures.

<p align="justify">
At first, this project has been created to the needs of my diploma thesis 
<b>"Algorithmic aspects of domination problem in graphs"</b>, where I inserted code fragments of implementation of 
discussed <code>approximation algorithm</code> for computing <code>maximum connected dominating set</code> of given graph. 
The implementation of the algorithm required defining specific data structure. Despite possibility to use already accessible 
data structures in <code>Java</code>, I decided to implement the structure myself in case of possible improvements and changes 
I could be willing to deploy - hence I defined <code>Graph class</code>. The next case was to decide about vertex implementation. 
And simply, because of idea: <code>what if there would be a need for each or some vertex to store several values?</code>, I decided to 
create a <code>Vertex class</code> as well. However, it was important to me to keep it simple for a potential user.
Thus, I decided <code>Vertex</code> should be an <code>inner non-static class</code> of <code>Graph</code>, so the user 
do not have to worry about having an object instance of <code>Vertex class</code> and use only a number as a reference. 
To make it accessible, I implemented methods that maps numbers and <code>Vertex</code> objects to the other.
<br>
<br>
After graduation, I decided to improve the quality of written code and add new features, but my goal was to keep
the assumption about the implementation I determined in <code>1.0-beta</code> project version. Therefore, I didn't 
implement palpable representation of edges, since implementation of <b>vertex neighbourhood</b> was satisfactory in such case. 
The outcome of my work has been committed on this repository.
</p>

## Changes in `1.0`

Below list corresponds to the changes provided into project after thesis defence:
- Prepared advanced tests of Graph implementation;
- Refactored code (cleaner code, improved functionality and efficiency of implementation);
- Replaced some methods with `lombok annotations`;
- Changed order of vertices in sets that user can see to `ascending`;
- Changed sets of vertices that user can see to `unmodifiable`;
- Changed return type of some methods from `void` to `boolean`;
- Added new files to resources,;
- Added `javadoc`;
- Added `dependencies`;
- Added `JetBrains annotations`;
- Added `unit tests`;
- Added `GraphRunner` class;
- Added `NegativeVertexIndexException` class;
- Added `NoSuchVertexIndexException` class;
- Added new features:
  - Disconnect vertices,
  - Get neighbours of given vertex,
  - Remove multiple vertices from graph(before: only singular vertex),
  - Create complete graph of given size,
  - Check if graph contains given vertices(before: only singular vertex),
  - Check if graph is bipartite,
  - Check if given subgraph is bipartite,
  - Check if graph is complete,
  - Check if given subgraph is complete,
  - Check if given subset of vertices is an independent set of graph,
  - Compute maximal independent set in graph,
  - Modified implementation of breadth first search algorithm,
  - Map given graph(`this`) to a complete graph of a same size,
  - Map vertices to their indexes;

## Features

Main features:
- Create empty graph (_order-zero graph / null graph_);
- Create graph from given file;
- Create complete graph (including empty);
- Print graph (all vertices and for each its [open] neighbourhood);
- Get all vertices of graph;
- Get neighbours of given vertex;
- Add singular vertex to graph;
- Add multiple vertices to graph;
- Remove singular vertex from graph;
- Remove multiple vertices from graph;
- Connect vertices;
- Disconnect vertices;
- Check if graph contains given vertex;
- Check if graph contains given vertices;
- Check if graph is connected;
- Check if given subgraph is connected;
- Check if graph is bipartite;
- Check if given subgraph is bipartite;
- Check if graph is complete;
- Check if subgraph is complete;
- Check if given subset of vertices is a connected dominating set of graph;
- Check if given subset of vertices is an independent set of graph;
- Modified implementation of breadth first search algorithm;
- Modified implementation of depth first search algorithm;
- Compute minimal dominating set in graph;
- Compute minimal connected dominating set in graph;
- Compute maximal independent set in graph;
- Map given graph(`this`) to a complete graph of a same size;

Others:
<br>
Other features are responsible for communication between user requests and defined Graph implementation logic.

## Environment Variables

To run this project it is recommended to add an **environment variable** to the **run configuration**:

`ALLOW`
and set its value to `true` or `false` depending on wanted behaviour.

```
if(ALLOW) -> runs basic and exceptions test of Graph implementation
else -> runs only basic test of Graph implementation
```

_Note that if you do not add environment variable to run configuration of a project you can expect to run the basic test only._

## Used Dependencies

Dependencies were managed using _Maven_ dependency mechanism. They were kept up to date during the work on project.

[Lombok](https://projectlombok.org/) (1.18.24)

[JetBrains Annotations](https://www.jetbrains.com/help/idea/annotating-source-code.html) (23.0.0)

[JUnit Jupiter API](https://junit.org/junit5/docs/5.9.0/api/org.junit.jupiter.api/module-summary.html) (5.9.0)

[JUnit Jupiter Params](https://junit.org/junit5/docs/5.9.0/api/org.junit.jupiter.params/module-summary.html) (5.9.0)

## Java Documentation

[Read documentation online](https://lucasmalara.github.io/graphs-and-algorithms/ "Java documentation")

## Author

[@??ukasz Malara](https://github.com/LucasMalara "author")