# LeMaterial - A Standardized Dataset of Materials

<p align="center">
  <img src="images/BANNER LEMATERIAL v2.png" alt="LeMaterial"><br/>

<a href="https://github.com/example" style="text-decoration: none;">
  <button style="background-color: #333; color: white; border: none; padding: 10px 20px; border-radius: 5px; cursor: pointer;">
    🐙 Code
  </button>
</a>
<a href="https://huggingface.co/datasets/LeMaterial/leDataset" style="text-decoration: none;">
  <button style="background-color: #333; color: white; border: none; padding: 10px 20px; border-radius: 5px; cursor: pointer;">
    🤗 LeMaterial Dataset
  </button>
</a>
<a href="https://huggingface.co/spaces/LeMaterial/materials_explorer" style="text-decoration: none;">
  <button style="background-color: #333; color: white; border: none; padding: 10px 20px; border-radius: 5px; cursor: pointer;">
    🤗 Material Explorer
  </button>
</a>
<a href="https://huggingface.co/spaces/LeMaterial/phase_diagram" style="text-decoration: none;">
  <button style="background-color: #333; color: white; border: none; padding: 10px 20px; border-radius: 5px; cursor: pointer;">
    🤗 Phase Diagram
  </button>
</a>
</p>


<p align="center">
</p>


> Today, we are thrilled to announce the launch of **LeMaterial**, an open-source collaborative project led by *Entalpic* and *Hugging Face,* designed to simplify and accelerate materials research for scientists and ML practitioners. LeMaterial unifies, cleans, and standardizes the most prominent material datasets, including [Materials Project](https://next-gen.materialsproject.org/), [Alexandria](https://alexandria.icams.rub.de/), and [OQMD](https://oqmd.org/) — giving rise to a single harmonized data format with **6.7M entries** and X properties.


## Why LeMaterial?

The world of materials science at the intersection of quantum chemistry and machine learning is brimming with opportunity. However, **this field is hampered by fragmented datasets** that vary in format, parameters, and scope.

- Different datasets have incompatible calculation parameters, limiting their integration.
- Field definitions and formats vary widely, increasing complexity. Standards like Optimade exist but focus only on structure parameters, not individual material properties.
- Similar materials may appear across datasets without clear connections or identifiers.
- Existing datasets differ in scope, e.g., repositories like NOMAD focus on quantum chemistry calculations, while others like Materials Project offer rich material properties but limited quantities.

This fragmented landscape makes it difficult for researchers in AI4Science and materials informatics to fully utilize existing data. Applications like training foundational models, constructing accurate phase diagrams, or determining material novelty lack simple solutions.

**LeMaterial** bridges these gaps by offering a unified and standardized dataset combining the strengths of three major databases: Materials Project, Alexandria, and OQMD. This high-quality resource is designed for studying materials, training AI models, and exploring chemical space. We aim to expand LeMaterial over time, incorporating new datasets, properties, and structures.

---

## Achieving a Clean, Unified, and Standardized Dataset

LeMaterial is more than a merged dataset with a permissive license. It’s a carefully curated resource designed to simplify research workflows and improve data quality.

> Vizu → Insert the dataset viewer + link to the datacard @Inel Djafar  

| **Release**     | **Description & Value**                                                                                                                         | **Date**    |
|------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|-------------|
| **v1.0**        | - Data collection and merging from Materials Project, Alexandria, and OQMD.                                                                      |
|                  | - Data cleaning to remove non-conforming data.                                                                                                  |
|                  | - Standardization with Optimade.                                                                                                               |
|                  | - Material fingerprinting with a unique identifier for deduplication.                                                                          |
|                  | - Data validation and visualization tools.                                                                                                     | 10/12/2024  |
| **v1.1**        | - Charge data and band gap calculations for Materials Project.                                                                                  |
|                  | - Unified energy correction scheme.                                                                                                            | Q1 2025     |
| **Next Releases**| - R2SCAN data from Materials Project.                                                                                                          |
|                  | - Surface datasets (OC20, OC22).                                                                                                               |
|                  | - Harmonization of trajectories and relational data.                                                                                           | Q2 2025     |

### Dataset Splits

- **Compatibility**: Provides calculations compatible for mixing across 3 functionals (PBE, PBESol, SCAN).
- **Novel**: Deduplicated materials using a structure fingerprint algorithm.
- **All**: Includes all processed materials.

| **Database** | **Number of Materials** | **Number of Structures*** |
| --- | --- | --- |
| Materials Project | 153,235 | 189,403 |
| Alexandria | 4,628,422 | 5,459,260 |
| OQMD | 1,226,781 | 1,226,781 |
| **LeMaterial (All)** | 5,835,800 | 6,725,593 |

---

## Integrating a Well-Benchmarked Materials Fingerprint

One of LeMaterial’s key contributions is its **hashing function** for uniquely identifying materials. This ensures:

- Quick identification of novel materials.
- Deduplication and consistency across datasets.
- Enhanced calculations for thermodynamic properties.

> **Clarification**: This fingerprint is a benchmark, not a ground truth, aiming to foster community discussion around material identification.

### Benchmark Evaluations:

- Distinct materials yield different hashes.
- Small noise in materials retains the same hash.
- Cross-database consistency confirmed with manual and DFT checks.
- Faster and more accurate than Pymatgen’s StructureMatcher.

<p align="center">
  <img src="images/Platform Team Charts - Hash Function (2).png" alt="LeMaterial"><br/>
</p>
---

## LeMaterial in Action: Applications and Impact

LeMaterial enables diverse applications:

- **Exploring Extended Phase Diagrams**: Better stability approximations in chemical spaces.
- **Comparing Material Properties Across Databases**: Useful for benchmarking.
- **Determining Novelty of Materials**: Fingerprinting highlights duplicates and novelties.

### Example: Identifying Duplicate Entries

LeMaterial’s fingerprint algorithm identified Alexandria entries with identical hashes. Manual checks confirmed they represented the same material, improving dataset integrity.

---

<div style="text-align: center;">
  <p>Supported by:</p>
  <div style="display: flex; justify-content: center; gap: 200px; align-items: center;">
    <img src="https://mila.quebec/sites/default/files/styles/fixed_width_480/public/startup/10712/logo-purple.png.webp?itok=q_EnRbVf" alt="ServiceNow" width="200">
    <img src="https://www.bigcode-project.org/hf_logo.jpg" alt="Hugging Face" width="200">
  </div>
</div>
