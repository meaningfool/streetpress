The goal of the project was to do data extraction using LLMs to build a graph from news articles. 

I used Streetpress, an outlet devoting a lot of effort to investigate and report about radical right networks and activities, as a source. 

I broke down the project into 3 Jupyter Notebook files to run in the following order:
1. streetpress_extract_entities.ipynb performs the entities and relationship extraction from the articles, and stores the results on disk.
2. streetpress_build_graph.ipynb reads from the disk, formats entities and relationship, performs entity resolution in order to produce a graph that is stored in a local SQLite instance.
3. streetpress_graph_viz.ipynb loads the data from SQLite and puts it into Neo4j Aura in order to visualize it