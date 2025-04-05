# novartis-moabox-vs-bioactivity
A comparative analysis of Novartis MoA Box compound–target annotations against our internal bioactivity database
## Novartis MoA Box vs Bioactivity Database

This project flattens the **Novartis MoA Box** compound–target annotations and compares them to our existing bioactivity database. The provided Excel data is first mapped to gene IDs, from which UniProt IDs are retrieved using ChEMBL.

---

### Folder Structure

#### `novartis_data_flattened/`
- Contains all flattened data from the MoA Box.
- Data is stored in individual CSV files.
- Each file is named using the corresponding UniProt ID and gene symbol (e.g., `P12345_TP53.csv`).

#### `novartis_only_uniprot_smiles/`
- Contains compound–target pairs that are **present in the Novartis MoA Box** but **not found in our bioactivity database**.
- Matching is done using **InChIKey**.

#### `novartis_only_smiles/`
- Contains compound–target pairs where the **target exists in our database**, but the **specific compound–target pair is missing**.

---

### Disclaimer

> ⚠️ This comparison is **not fully accurate yet**.  
> Some targets have not been mapped to UniProt primary accessions.  
> The results of this comparison may change as target annotations are finalized.

---

### To-Do

- [ ] Update all targets in the bioactivity database with UniProt primary accessions.
- [ ] Re-run the comparison for more complete and accurate results.

