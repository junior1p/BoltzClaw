# BoltzClaw - Natural Language-Driven Protein Design Skill

## Skill Overview
**BoltzClaw** is a natural language-driven skill designed to streamline protein design workflows using Boltz Lab, PDB, UniProt, and Biopython. It enables dynamic prediction job creation, execution, and monitoring with minimal user input, including scenarios with or without explicit sequence data.

---

## Key Features

### 1. PDB Template Retrieval
- Queries PDB using sequence data or functional descriptions.
- Selects optimal structural templates for tasks like protein-ligand docking.
- Downloads and parses structural files (PDB/mmCIF) for further analysis.

### 2. UniProt Sequence Annotation
- Fetches sequences, functional domains, and mutation data from UniProt.
- Dynamically integrates functional insights into prediction workflows.

### 3. Biopython Sequence Processing
- Supports transcription, translation, and sequence validation.
- Processes structures or sequences for seamless integration into prediction pipelines.

### 4. Boltz Prediction Pipeline
- Generates Boltz-compatible YAML files dynamically, including:
  - Sequence definitions.
  - Structural constraints.
  - Functional annotations.
- Submits tasks to Boltz Lab CLI and monitors progress in real-time.
- Retrieves results and supports downstream analysis.

---

## How to Use

You can interact with BoltzClaw using natural language queries:

### Example Queries
1. **Provide Sequence:**
   - Query: *"Predict the binding affinity of this sequence with Ligand X."*
   - Action: Retrieves UniProt and PDB data as needed, integrates with Boltz YAML generation.

2. **Without Sequence:**
   - Query: *"Design an insulin-like protein for metabolic studies."*
   - Action: Searches UniProt and PDB for relevant structures and annotations, generates prediction input dynamically.

3. **Monitor Tasks:**
   - Query: *"Check the status of my recent jobs."*
   - Action: Queries Boltz Lab CLI for active tasks, retrieves logs, and formats results as readable outputs.

4. **Retrieve Results:**
   - Query: *"Give me the results of job #12345."*
   - Action: Fetches prediction data, parses output, and prepares downloadable files or visualizations.

---

## Installation
Ensure the following prerequisites are met before deploying BoltzClaw:
1. **Boltz Lab CLI** installed and configured.
2. **Access to UniProt and PDB APIs** for data retrieval.
3. **Python with Biopython** installed for sequence processing.

---

## Skill API Reference

### YAML File Generation
**Function:** `generate_yaml_for_boltz`
- Creates Boltz-compatible prediction input files.

### PDB Retrieval
**Function:** `retrieve_pdb_template`
- Queries PDB database with sequence or keywords.

### UniProt Integration
**Function:** `get_uniprot_annotation`
- Fetches sequence annotations, GO terms, and metadata.

### Biopython Processing
**Function:** `process_sequence_with_biopython`
- Handles transcription, translation, and validation.

---

## Future Enhancements
1. Support for additional databases (e.g., AlphaFold DB).
2. Expanded task orchestration for multi-step workflows.
3. Improved NLP-driven workflows to handle ambiguous queries more effectively.

---

**Let BoltzClaw automate your protein design and prediction tasks with ease!** 🚀