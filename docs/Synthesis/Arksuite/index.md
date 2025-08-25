---
title: Arksuite
layout: home
parent: Synthesis
---
# ArkSuite – Data-Centric Experiment Management  

**ArkSuite** is a data-driven software environment.  
Unlike AutoSuite, which mainly focuses on **instrument control and task execution**, ArkSuite emphasizes **data organization, experiment design and management**.  
**Platforms**: CatScreen, Swing SP. 

<!-- Image: ArkSuite overview -->
![ArkSuite Overview](assets/img/INSERT_arksuite_overview.png)

---

## Advantages of ArkSuite compared to AutoSuite  

- **Data-centric architecture**  
  ArkSuite stores all experimental information in a structured, relational way. This ensures **traceability, reproducibility, and reusability** of data.  

- **Knowledge retention**  
  Experiments are not only executed but also archived as reusable **digital records**.  

- **Advanced experiment design**  
  ArkSuite allows scientists to **configure, compare, and optimize experiments** more efficiently than the task-based logic of AutoSuite.  

- **Integration with AI & predictive modeling**  
  Structured data from ArkSuite (**JSON files**) can be directly used in **machine learning models** to support decision-making.  

<!-- Image: ArkSuite vs AutoSuite comparison -->
![ArkSuite vs AutoSuite](assets/img/INSERT_arksuite_vs_autosuite.png)

---

## Core Concepts in ArkSuite  

### Article  
- Represents a **general entity or material** used in experiments.  
- Acts as the **top-level definition** (e.g., “Solvent”, “Ligand”, “Substrate”).  
- Articles serve as categories under which products are grouped.  



### Product  
- A **specific instance** of an Article.  
- Example: Article = “Solvent”; Product = “Toluene” or “THF”.  
- Products carry detailed information such as supplier, batch, and purity.  



### Attribute  
- **Descriptors** attached to Articles or Products.  
- Provide measurable or categorical properties (e.g., boiling point, density, SMILES code).  
- Attributes allow **data filtering, searching, and modeling**.  



---

## Digital Twin  

**Definition:**  
The **Digital Twin** in ArkSuite is a **virtual replica of the laboratory environment** that mirrors the configuration of the physical platform.  

**Purpose:**  
- Allows experiments to be **designed, tested, and validated virtually** before execution.  
- Ensures that parameters defined in ArkSuite align with the **capabilities and limits** of the real instruments.  
- Reduces risk of errors and improves **efficiency in workflow setup**.  

**Key Benefits:**  
- Enhances **reproducibility** and consistency.  
- Facilitates **scale-up transfer** of workflows.  
- Provides a **safe test environment** for new protocols.  

<!-- Image: ArkSuite Digital Twin -->
![ArkSuite Digital Twin](assets/img/INSERT_arksuite_digital_twin.png)

---