# Electrical System Knowledge Graph for the Porsche 718

An independent, interactive knowledge graph modeling the electrical architecture of the Porsche 718 (982).

**[Open the interactive 718 Electrical System Model](https://rcx-engineering.github.io/718-system-model/Electrical_System_for_Porsche_718.html)**

> This model may contain errors and omissions. It is provided as a reference to fellow enthusiasts, but use at your own risk. Please consider contributing improvements.

The project converts available electrical-system technical information into a structured, machine-readable knowledge graph that can be explored interactively in a web browser. Rather than reproducing conventional wiring diagrams, it represents electrical components and their relationships as structured factual data and generates original visualizations dynamically.

The repository is intentionally minimal:

```text
README.md
Electrical_System_for_Porsche_718.html
SKILL-wiring_diagram.md
```

## What the Knowledge Graph Contains

The model represents the electrical system as interconnected entities and relationships rather than as a collection of individual wiring sheets.

Depending on the modeled subsystem, information may include:

- Electronic control units and other electrical components
- Connectors and connector relationships
- Pins and terminal assignments
- Wiring and electrical connectivity
- Power distribution
- Grounds
- Fuses and protection devices
- Sensors and actuators
- Communication networks and buses
- Component-to-component signal paths
- Functional and architectural relationships

The resulting graph allows the vehicle electrical system to be examined at multiple levels, from individual connections to larger subsystem and network relationships.

## Interactive Visualization

[`Electrical_System_for_Porsche_718.html`](https://rcx-engineering.github.io/718-system-model/Electrical_System_for_Porsche_718.html) is a self-contained browser application.

The visualization is generated dynamically from the underlying knowledge graph rather than being copied from or rendered from conventional wiring diagrams. The graph can therefore be explored according to relationships in the data instead of being limited to the organization and presentation of traditional schematic documentation.

No server-side software is required. The file can be opened directly in a modern browser or hosted as a static web page using a service such as GitHub Pages.

## Knowledge Graph and openCypher Representation

The electrical-system model is conceptually a **knowledge graph**: a structured representation of engineering entities, their properties, and the relationships between them.

The implementation contained in the HTML file uses **openCypher to express a labeled property graph**. A labeled property graph is a particular graph data model in which nodes and relationships may have labels and associated properties. This provides a convenient machine-readable representation for the electrical topology while retaining the broader semantics of a knowledge graph.

The HTML file contains this openCypher graph as **plain text**.

Its nodes, relationships, labels, properties, and topology can therefore be inspected, extracted, searched, transformed, or imported into compatible graph-database and analysis tools.

This also makes the model particularly useful to **AI agents and large-language-model-based engineering tools**. Because the graph is stored directly in structured plain text, an AI agent can easily reference and use it without first interpreting graphical wiring diagrams or reverse-engineering the visualization.

AI-assisted applications can use the model to:

- Trace electrical paths and relationships
- Identify components connected directly or indirectly to another component
- Analyze power, ground, signal, and network dependencies
- Construct graph queries
- Navigate across subsystem boundaries
- Compare related components or circuits
- Reason about electrical-system topology
- Assist with troubleshooting and engineering analysis
- Translate the graph into other structured engineering representations

openCypher is the representation used by this implementation, but the underlying methodology is not dependent on openCypher or on the labeled property graph model. The same knowledge could be represented using other graph, ontology, or systems-engineering formats such as SysML v2, RDF-based models, Brick, or other structured schemas.

Conversion between graph representations is generally straightforward because the important information is contained in the entities, properties, and relationships rather than in a particular visualization or serialization format. Modern AI tools can also assist substantially with translating between these representations.

The standalone HTML file therefore contains both:

1. A **human-oriented interactive electrical-system viewer**
2. A **machine-oriented structured representation of the electrical system**

## Reusable Knowledge-Graph Creation Skill

[`SKILL-wiring_diagram.zip`](SKILL-wiring_diagram.zip) contains the reusable AI-agent skill and engineering workflow used to create this type of electrical-system knowledge graph.

The skill is provided so that others can apply the same approach to additional vehicles, machinery, equipment, or other complex engineered systems.

It describes a methodology for converting available technical information into structured entities and relationships, including the extraction and normalization of components, connectors, pins, circuits, networks, and other electrical relationships; construction of a machine-readable graph representation; and generation of an interactive knowledge-graph visualization.

The skill is intentionally separate from the Porsche-specific electrical data. It is intended to demonstrate and propagate the **method of converting conventional engineering information into machine-readable knowledge models**, rather than simply distributing one completed model.

## Engineering Approach

The project demonstrates a workflow for converting heterogeneous engineering information into a structured, machine-readable knowledge model.

Potential source information can include:

- Technical documentation
- Photographs
- Component markings
- Connector and harness observations
- Measurements
- Diagnostic information
- Vehicle observations
- Engineering notes
- Existing structured data
- Other available technical information

The general workflow is:

```text
Technical information
        │
        ▼
Fact extraction and observation
        │
        ▼
Normalization and entity identification
        │
        ▼
Engineering ontology / information model
        │
        ▼
Knowledge graph
        │
        ├──────────────► AI / machine reasoning
        │
        ├──────────────► Graph queries and analysis
        │
        ├──────────────► Other engineering data models
        │
        └──────────────► Dynamic visualization
```

The objective is not simply to redraw electrical schematics.

A knowledge graph separates the **engineering information** from any particular graphical presentation of that information. Once represented as entities and relationships, the same model can support interactive visualization, automated analysis, graph traversal, search, troubleshooting, AI-assisted reasoning, and translation into other engineering information models.

This approach is potentially applicable well beyond automotive electrical systems to other large, highly interconnected engineered systems whose technical information is distributed across drawings, photographs, observations, tables, manuals, databases, and other sources.

## Why a Knowledge Graph?

Traditional wiring diagrams are optimized primarily for human viewing. They are extremely useful engineering documents, but information is often distributed across many sheets and requires the reader to manually follow references between connectors, components, circuits, and subsystems.

A graph representation makes those relationships explicit.

Instead of asking only:

> What is shown on this wiring diagram?

the model can support questions such as:

- What components are electrically connected to this control unit?
- What path connects two components?
- Which systems share a particular power source, ground, connector, or network?
- What components participate in a particular communication bus?
- What signals cross subsystem boundaries?
- What other elements are affected by a particular connection or component?
- What electrical relationships exist several connections away from the starting point?

These are naturally graph problems and are well suited to graph-query tools, systems-engineering models, and AI-assisted engineering analysis.

## Copyright, Factual Information, Database Rights, and DMCA

This project distinguishes between **engineering facts** and the particular expressive form in which those facts may be documented.

Under U.S. copyright law, facts themselves are not copyrightable. The U.S. Supreme Court held in *Feist Publications, Inc. v. Rural Telephone Service Co.*, 499 U.S. 340 (1991), that facts remain available for others to use even when they appear within a copyrighted compilation. Copyright may protect sufficiently original expression, selection, coordination, or arrangement, but it does not give ownership of the underlying facts themselves.

Similarly, 17 U.S.C. § 102(b) provides that copyright protection does not extend to an idea, procedure, process, system, method of operation, concept, principle, or discovery, regardless of the form in which it is described, explained, illustrated, or embodied.

European Union law similarly distinguishes underlying data from protected expression, but additionally provides a separate **sui generis database right** under Directive 96/9/EC on the legal protection of databases. That right may protect a database where there has been substantial qualitative or quantitative investment in obtaining, verifying, or presenting its contents and may restrict extraction or re-utilization of all or a substantial part of a protected database.

This database right is distinct from copyright in the underlying information. Directive 96/9/EC expressly states that the sui generis right does not extend copyright protection to mere facts or data and does not create a new exclusive right in the individual works, data, or materials contained in a database.

Accordingly, an engineering fact or physical relationship does not become protected expression merely because it appears in a database. Rights may nevertheless exist in an original database structure or compilation, and EU database rights may separately apply to substantial extraction or re-utilization from a qualifying database.

This project is intended to construct an independent engineering model from heterogeneous available technical information, observations, measurements, photographs, notes, and other sources rather than reproduce the expressive presentation or database structure of a particular source.

The Digital Millennium Copyright Act (DMCA), including the notice-and-takedown process in 17 U.S.C. § 512, is a U.S. statutory framework providing procedures for claims involving allegedly infringing copyrighted material. It does **not** expand the subject matter protected by copyright or convert otherwise uncopyrightable facts, systems, methods, or engineering relationships into copyrighted expression.

Accordingly, this project represents electrical connectivity and system relationships as independently structured factual data and original visualizations. It does not reproduce third-party wiring drawings, page layouts, illustrations, or substantial textual descriptions.

Nothing in this section should be interpreted as claiming ownership of underlying engineering facts that are not subject to copyright protection, nor as suggesting that copyright, database rights, trademark rights, or other applicable intellectual-property rights cannot exist in particular source materials or compilations.

And an additional note: We licensed this project to make it freely available to fellow enthusiasts and for Porsche's own internal use, and we have shared our methods so they can be applied to future engineering designs. We hope this knowledge graph serves as more than a direct technical reference—it also demonstrates to technicians and engineers how model-based engineering and model-based systems analysis can improve methods, accelerate development, and reduce the costs of design, maintenance, and repair.

We also implore Porsche, and all manufacturers, to respect individuals' right to repair. Please make more technical information and tools like this freely available, and stop making basic maintenance and repair unnecessarily difficult.

## Independent Project

This is an independent, community-developed engineering project.

It is **not affiliated with, sponsored by, approved by, or endorsed by Dr. Ing. h.c. F. Porsche AG or any of its subsidiaries or affiliates**.

The repository does **not** contain Porsche workshop manuals, Porsche wiring-diagram PDFs, scanned technical documentation, or reproductions of Porsche wiring drawings.

The knowledge graph consists of structured factual electrical-system information, independently organized into a graph model, together with original software and visualizations used to explore that information.

Porsche and 718 are trademarks of Dr. Ing. h.c. F. Porsche AG. Their names are used solely to identify the vehicle to which this independent technical model applies.

## Accuracy and Contributions

Complex vehicle electrical systems vary by model year, equipment configuration, market, installed options, hardware revision, and software configuration.

Corrections, validation, additional relationships, observations, and improvements to the modeling methodology are welcome.

When proposing changes, contribute structured factual information, independently developed analysis, observations, measurements, photographs for factual reference where appropriate, or improvements to the knowledge-graph methodology. Do not submit copyrighted wiring diagrams, workshop-manual pages, scans, screenshots, or substantial copied text from third-party technical publications.

## Licensing

Different portions of the project are licensed according to the type of material involved.

### Software — Apache License 2.0

The software contained in `Electrical_System_for_Porsche_718.html`, including the visualization, user interface, graph-processing logic, and supporting code, is licensed under the **Apache License 2.0**.

The Apache License permits use, modification, redistribution, and commercial use subject to its terms, including preservation of applicable notices.

### Documentation and Skill — Creative Commons Attribution 4.0

Original project documentation, including this `README.md`, `SKILL-wiring_diagram.md`, and other original explanatory or instructional material, is licensed under the **Creative Commons Attribution 4.0 International License (CC BY 4.0)**.

You may share and adapt this material for any purpose provided appropriate attribution is given.

### Knowledge Graph — Open Data Commons Attribution License 1.0

The independently compiled factual electrical-system knowledge graph, including its structured organization, graph representation, annotations, and database contents to the extent that applicable rights exist, is made available under the **Open Data Commons Attribution License 1.0 (ODC-By 1.0)**.

This permits use, modification, redistribution, and commercial use of the database subject to the attribution requirements of the license.

These licenses apply only to rights actually held by the contributors to this project. They do not assert ownership of otherwise uncopyrightable facts and do not grant rights in third-party trademarks, copyrighted works, databases, or other third-party intellectual property.

## Repository Contents

### [Electrical System Model — Interactive Viewer](https://rcx-engineering.github.io/718-system-model/Electrical_System_for_Porsche_718.html)

Standalone interactive electrical-system knowledge graph containing:

- The browser-based visualization and user interface
- Graph-processing and navigation software
- The electrical-system model
- The embedded plain-text openCypher labeled property graph

### [`SKILL-wiring_diagram.zip`](SKILL-wiring_diagram.zip)

Reusable AI-agent skill and engineering methodology for creating similar electrical-system knowledge graphs from available technical information.

It is intended to allow the technique demonstrated by this project to be applied to other vehicles and engineered systems.

### `README.md`

Project description, methodology, limitations, attribution, legal context, and licensing information.

## Disclaimer

This model may contain omissions, transcription errors, incorrect relationships, or other inaccuracies.

The project and its contents are provided **as-is**, without warranties or representations of accuracy, completeness, reliability, fitness for a particular purpose, or suitability for diagnosis, repair, modification, or other use.

Users are responsible for independently verifying critical information before relying upon it. The authors and contributors assume no responsibility for damage, injury, diagnostic errors, repair errors, or other consequences resulting from use of this project or its contents.
