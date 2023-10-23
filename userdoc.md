# PPS Catalogue

The PPS Catalogue is designed to help you efficiently manage Profinits growing workforce by identifying and connecting employees with similar skillsets and attributes. This module uses a graph-based approach to visualize relationships between individuals and provides tools for querying and refining results.

![intro picture](./userdoc-pics/intro.png)

## Key Features

### Standard Catalog User

- **Graph Visualization**: Gain insights into personnel relationships through an intuitive visual representation with nodes and edges highlighting similarities.

- **Query Customization**: Tailor your search experience by selecting a reference person, adjusting graph size, and refining similarity thresholds to find the perfect match.

- **Personnel Information**: Access comprehensive details about individual employees, helping you make informed decisions.

### Data Scientist

- **Fine-Tuning Data Harvesting**: Customize various parameters of the data harvesting algorithm, including SVD thresholds and more, to ensure precise and relevant data collection.

- **Raw Employee Data Inspection**: Dive deep into the raw employee data for debugging and fine-tuning data harvesting processes.

- **Default Metric Weight Definition**: Define default metric weights within the similarity algorithm, giving you control over how different attributes contribute to similarity calculations.

## Accessing the Catalogue

To access the PPS Catalogue module, please navigate to the Reporting module and select the Human Resources sub-module. Inside the Human Resources sub-module, you will find a link labeled PPS Catalogue. Click on this link to access the module.

*Depending on your role within the Profinit, you may have different levels of access and permissions within the module. Please consult your supervisor or system administrator for information on your user role and privileges.*

## Standart User Catalogue Interactions

In this section, we will explore various interactions with the catalog, allowing you to maximize your experience and harness its full potential.

### Graph Interpretations

There are two modes of displaying the graph within the **PPS Catalogue** module, each offering unique insights into personnel relationships:

1. **Single-Person Query Mode**:
   - When you query a single person, the module constructs a neighborhood around the inputted person. In this mode, the size of each node depends on its similarity to the queried individual. Larger nodes indicate a higher degree of similarity.
   - Edges connecting nodes reflect the similarity between two individuals. The more visible and shorter the edge, the greater the similarity it represents. This allows you not only to explore the neighborhood of the queried person but also to examine connections within the neighborhood.

   ![single center](./userdoc-pics/single-center.png)

2. **Multi-Person Query Mode**:
   - When you query multiple individuals, the module renders them in a circular arrangement. The module then identifies and displays individuals who are most similar to each of the queried persons.
   - In this mode, the size of each node expresses its cumulative similarity to all the queried individuals. However, there are no edges between the found nodes, as it was found to be confusing for interpretation.

   ![single center](./userdoc-pics/multiple-center.png)

### Query Parametrization

**PPS Catalogue** provides options for customizing your queries to meet your specific needs:

- **Select Queried User**: Use the multiselect feature to search for and select the user you want to query. If only one user is selected, the first type of graph, as described in the "Graph Interpretations" section, is constructed and displayed. If more than one user is selected, the multi-person query mode is employed.

- **Graph Size Slider**: Adjust the size of the resulting graph using the slider. This allows you to focus on a specific area of interest within the personnel network.

![query box](./userdoc-pics/query-box.png)

#### Customize Your Similarity Metric

The module allows you to fine-tune the similarity metric to align with your preferences. When you click the button to change the metric, you'll be presented with a window featuring different sliders, each representing a specific parameter. Here's a breakdown of the available sliders:

- **Knowledge Slider**: Adjust the importance of knowledge based on the knowledge matrix. Closer to 1 indicates greater prominence.

- **School Slider**: Consider the relevance of the school attended by a given person when calculating similarity.

- **Project History Slider**: Weigh the significance of shared project history within the Profinit.

- **Work Position Slider**: Evaluate individuals based on their work position, categorized into five levels from junior to senior.

- **Work Time Slider**: Factor in whether a person works part-time or full-time when determining similarity.

- **Time in Profinit Slider**: Consider the duration of time a person has worked within the Profinit.

Additionally, this feature enables you to create and save templates, allowing you to reuse your customized metric settings without the need for frequent adjustments.

![metric form](./userdoc-pics/metric-form.png)

### Information About the Person

In the last section, you can access comprehensive details about an individual user. All available data used during similarity computation is displayed here. If certain information is missing, it will not be displayed in this section.

![metric form](./userdoc-pics/empl-info.png)

## Data Scientist Catalogue Interactions

This section is dedicated to features that empower data scientists to fine-tune the similarity algorithm and data harvesting process within the **PPS Catalogue**.

### Configurations

Within the **PPS Catalogue**, data scientists have access to a comprehensive set of configuration options. These configurations encompass various aspects, including data fetching/harvesting, metric definition, graph appearance, and more. When you navigate to `Reporting > Human Resources > PPS Catalogue Configurations`, you'll find a page that accommodates all possible configuration values.

An important feature to note is that each configuration parameter is explained in detail when you hover over the 'info' icon located next to the respective parameter. For more in-depth explanations of these algorithms and configurations, please refer to the technical documentation.

It's worth mentioning that changes to these parameters do not trigger an immediate data harvest process; this ensures that adjustments can be made without affecting ongoing operations.

![configs](./userdoc-pics/configs.png)

### PPS Catalogue Data

The raw data underpinning the **PPS Catalogue** is readily accessible on the `Reporting > Human Resources > PPS Catalogue Data` page. Here, you'll find a table displaying the dataset, and you can choose to display only specific columns to inspect relevant data.

In addition to inspecting data, there is a button provided for manual data harvest. While data harvesting typically occurs periodically, this feature allows data scientists to initiate the process manually when needed, ensuring that the dataset remains up-to-date and relevant for analysis.

![catalogue data](./userdoc-pics/catalogue-data.png)
