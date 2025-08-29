---
title: Arksuite
layout: home
parent: Synthesis
---
# ArkSuite – Data-Centric Experiment Management  

**ArkSuite** is a data-driven software environment.  
Unlike AutoSuite, which mainly focuses on **instrument control and task execution**, ArkSuite emphasizes **data organization, experiment design and management**.  
**Available on Platforms**: CatScreen, Swing SP. 


---

## Advantages of ArkSuite compared to AutoSuite  

- **Data-centric architecture**  
  ArkSuite stores all experimental information in a structured way. This ensures **traceability and reproducibility** of data. Experiments are not only executed but also archived as reusable **digital records**.  

- **Advanced experiment design**  
  ArkSuite allows scientists to **configure, compare, and optimize experiments** faster and more efficiently than the task-based logic of AutoSuite.  

- **Integration with AI & predictive modeling**  
  Structured data from ArkSuite can be directly used in **machine learning models** to support decision-making.  

<!-- Image: ArkSuite vs AutoSuite comparison -->
![ArkSuite vs AutoSuite](./../../../assets/images/arksuite_vs_autosuite.png)

---

## Core Concepts in ArkSuite  

### Article  
- Represents a **general entity or material** used in experiments;
- Articles serve as template to generate products;
- Example: Article = “Solvent”; 


### Product  
- A **specific instance** of an Article;
- Products carry detailed information such as CAS, concentration or purity;
- Example: Product = “Toluene”, “THF”. 



### Attribute  
- **Descriptors** attached to Articles or Products.  
- Provide measurable or categorical properties (e.g., boiling point, density, SMILES code).  
- Attributes allow **data filtering, searching, and modeling**.  



---

## Digital Twin  

 
The **Digital Twin** in ArkSuite is a **virtual replica of the laboratory environment** that mirrors the configuration of the physical platform.  

**Purpose:**  
- Allows experiments to be **designed, tested, and validated virtually** before execution.  
- Ensures that parameters defined in ArkSuite align with the **capabilities and limits** of the real instruments.  
- Reduces risk of errors and improves **efficiency in workflow setup**.  

**Advantages:**  
- Enhances **reproducibility** and consistency.  
- Facilitates **scale-up transfer** of workflows.  
- Provides a **safe test environment** for new protocols.  

<!-- Image: ArkSuite Digital Twin -->
![ArkSuite Digital Twin](./../../../assets/images/arksuite_digital_twin.png)

---

## Workflow Diagram  

 
The **Workflow Diagram** in ArkSuite is a **graphical representation of an experiment**.  
It allows the user to visualize the **sequence of operations**, the **flow of materials**, and the **relationships between tasks**.

**Advantages:**  
- Clear overview of complex workflows;
- Displays experiments as **interactive diagrams** rather than simple task lists.

<!-- Image: ArkSuite Workflow Diagram -->
![ArkSuite Workflow Diagram](./../../../assets/images/arksuite_workflow_diagram.png)

---

## Export of Data  

 
ArkSuite provides robust options for **data export**, ensuring that experimental results are accessible and usable outside the software environment.  

**Export Formats:**  
- **Excel / CSV** for tabular results and simple reporting.  
- **JSON / XML** for structured data integration into databases or AI pipelines. 
- **PDF reports** for documentation and compliance purposes.  


**Advantages:** 
 
- Maintains **metadata** (e.g., date, operator, platform, conditions);
- Enables direct transfer into **predictive modeling environments**;   
- Facilitates **data-driven research**;  
- Guarantees **traceability** for collaborative projects.  
