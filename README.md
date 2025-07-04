# CME: ChatGPT Material Explorer 1.0  

**CME 1.0** is a domain-specific custom GPT on the GPT-4o architecture. CME is developed with several key objectives in mind: (1) lowering the barrier to entry for AI-assisted materials research, (2) integrating experimental and computational data pipelines, and (3) reducing the risk of hallucination by interfacing with real-time databases and using physics-aware modeling approaches with many more potential additions in the future.




# Comparison between GPT-4o and ChatGPT Material Explorer

This table compares responses from different AI models to various materials science queries. **Bold** entries indicate correct or reasonably accurate responses.

| Question | GPT-4o Response | ChemCrow | ChatGPT Material Explorer Response |
|----------|-----------------|----------|-----------------------------------|
| 1. Get IUPAC name for `CC(=O)OC1=CC=CC=C1C(=O)O` | **2-(4-acetylphenyl)acetic acid However, this molecule is more commonly known as acetylsalicylic acid, which is the chemical name for aspirin** | **Aspirin** | **This is the official IUPAC name for acetylsalicylic acid (aspirin)** |
| 2. Get me the molecular formula for aspirin | **C9H8O4** | **C9H8O4** | **C9H8O4** |
| 3. Look up the SMILES notation for ibuprofen | **CC(C)CC1=CC=C(C=C1)C(C)C(=O)O** | **CC(C)Cc1ccc(C(C)C(=O)O)cc1** | **CC(C)Cc1ccc(cc1)C(C)C(O)=O** |
| 4. Find all materials containing chemical formula MgB2 in the JARVIS-DFT database and their total number. Present in table format. | The JARVIS-DFT database includes materials containing the chemical formula MgB2, notably the well-known superconductor magnesium diboride (MgB2) and related compounds. The primary entry for MgB2 in the database is identified by the JARVIS-ID JVASP-1151. Additionally, the database features related materials such as Mg2B4N2, which ... | I'm sorry, but I don't have access to JARVIS-DFT database. I recommend using the JARVIS-DFT... | **A total of 4 MgB2 materials were found in the JARVIS-DFT database JVASP-1151, JVASP-19821, JVASP-135405.... The table above summarizes their key properties...** |
| 5. Predict properties of this Poscar using ALIGNN: MoSe2 1.0 1.661759 -2.878250 0.000000 1.661759 2.878250 0.000000 0.000000 0.000000 35.451423 Mo Se 1 2 direct 0.666667 0.333333 0.326886 Mo 0.333333 0.666667 0.374080 Se 0.333333 0.666667 0.279691 Se | Running ALIGNN Predictions Locally To predict properties using ALIGNN: Install JARVIS-Tools: Ensure you have Python installed, then run: pip install jarvis-tools Prepare Your POSCAR File: Save your structure in a file named POSCAR. Run ALIGNN Prediction: Use the following Python script: ... | I'm sorry, but I don't have the capability to analyze Poscar file or use ALIGNN to predict properties. Please use a tool or service that supports these features. | **Here are the ALIGNN-predicted properties for the given MoSe2 POSCAR structure (from JARVIS-DFT), Formation energy per atom: -0.634 eV, Total energy per atom: -4.52 eV, Bandgap (OptB88vdW functional): 0.359 eV. These values suggest a moderately stable material with a small bandgap, consistent with known semiconducting behavior of MoSe2...** |
| 6. Find papers on MgB2 in arXiv. State how many results did you find and show top 10 recent papers only. | I found several papers on MgB2 (magnesium diboride) in arXiv. Here are the top 10 most recent ones: Kinetic Inductance and Nonlinearity of MgB2 Films at 4K Authors: J. Greenfield, C. Bell... | Note: This tool can take some time to complete execution!! Tool encountered an error... RuntimeError: Failed to avoid a service limit across 5 retries. | **I found 905 results on arXiv related to MgB2. Here are the 10 most recent papers: High-pressure high-temperature solution growth, structural, and superconducting properties of Fe-substituted MgB2 single crystals...** |
| 7. How do I interpret a phase diagram? | **Interpreting a phase diagram-especially a binary phase diagram-is crucial in materials science, metallurgy, and chemistry for understanding material stability, melting, solidification, and transformation. Here's a step-by-step guide:...** | **A phase diagram is a type of chart used in fields such as physical chemistry, engineering, mineralogy, and materials science. It shows the conditions, such as pressure and temperature, at which thermodynamically distinct phases (like solid, liquid, or gaseous states) ...** | **Interpreting a phase diagram involves understanding the stability and transitions of different phases (solid, liquid, gas, or multiple solid phases) of a material as a function of variables like temperature, pressure, or composition...** |
| 8. Can you explain the band structure of silicon? | **Yes, the band structure of silicon is fundamental to understanding its role as a semiconductor. Here's a detailed explanation:1. What is a Band Structure? The band structure of a solid describes the allowed energy levels (bands) that electrons can occupy, as a function of momentum (k-vector)...** | **The band structure of silicon refers to the ranges of energy that an electron within the silicon may have (called energy bands, energy levels, or simply bands) and ranges of energy that it may not have (called band gaps or simply gaps)...** | **Crystal Structure and Brillouin Zone Crystal structure: Silicon crystallizes in the diamond cubic structure.Brillouin zone: The symmetry points typically discussed in the band structure of silicon include: Γ (Gamma): center of Brillouin zone X, L, and K: high-symmetry points...** |

## Key Observations

- **ChatGPT Material Explorer** consistently provides the most accurate and detailed responses for materials science queries
- **GPT-4o** performs well on general chemistry questions but struggles with specialized database queries
- **ChemCrow** shows mixed performance, with some technical limitations for database access and complex file analysis
- Material Explorer excels particularly in database queries (JARVIS-DFT), property predictions (ALIGNN), and literature searches (arXiv)


# ChatGPT Material Exlorer Example Prompts:

There are no limits to the types of questions you can ask Material Explorer. Below are just a few examples. You can also engage in an iterative conversation, asking follow-up questions or requesting explanations of the results.

1. Find all materials containing Carbon (C) and Silicon (Si) in the JARVIS-DFT database and their total number. Present in table format.
2. Find all materials containing Carbon (C) and Silicon (Si) in the C2DB database and their total number. Present in table format.
3. Find all materials containing chemical formula MoS2 in the JARVIS-DFT database and their total number. Present in table format. (Note chemical formula should be alphabetically ordered, so O2Si not SiO2)
4. Predict properties of this Poscar file using ALIGNN for atomic structure: MySytem
1.0
1.549892767326361 -2.684493224977372 0.0
1.549892767326361 2.684493224977372 0.0
0.0 0.0 10.151391815821647
Si C
4 4
Cartesian
1.54989 -0.8948317896599827 9.52045238045808
1.54989 0.8948317896599827 4.444757380458079
0.0 0.0 6.982616849916004
0.0 0.0 1.9069218499160046
1.54989 -0.8948317896599827 7.6117778219678485
1.54989 0.8948317896599827 2.536082821967849
0.0 0.0 5.080550587658042
0.0 0.0 0.0048555876580418525
5. How do I interpret a phase diagram?
6. Can you explain the band structure of silicon?
7. Retrieve materials with the chemical formula Al2O3 from the JARVIS-DFT database and summarize their properties.
8. Find all materials containing chemical formula MoS2 in the JARVIS-DFT, Materials Project, COD and C2DB databases and their total number. Present them all in individual table format.
9. Get IUPAC name for CC(=O)OC1=CC=CC=C1C(=O)O
10. Get me the molecular formula for aspirin

(If you good prompts worth sharing with others, make a pull request to this README file)


# 📺 Related YouTube Playlist

[🎥 Watch the Playlist on YouTube](https://www.youtube.com/playlist?list=PLjf6vHVv7AoK22-cHlApfBpSKBf6oBg4A)



# Disclaimer: 

While we strive for accuracy, the information retrieved and analyzed by this tool is dependent on third-party sources and computational models, which may have inherent limitations or uncertainties.

This tool is intended for research and informational purposes only. It should not be used as a substitute for experimental validation or professional engineering judgment. Users are encouraged to verify critical data through independent sources before making any scientific, industrial, or commercial decisions.

By using Material Explorer 1.0, you acknowledge that:

The tool and its developers do not guarantee the accuracy, completeness, or reliability of the provided data.
We are not liable for any direct or indirect damages resulting from the use of this tool or its outputs.
Users are responsible for ensuring compliance with intellectual property laws, licensing agreements, and ethical guidelines when utilizing external datasets.

