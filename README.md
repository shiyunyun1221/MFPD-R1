# MFPD-R1

Official supplementary materials and datasets for **Motif-FPD: Towards Free-Form Natural Language-Driven Functional Protein Design via Motif-Centric LLM**.

Motif-FPD is a motif-centric large-language-model framework for functional protein design from free-form natural-language instructions. This repository provides the benchmark data, supplementary material, generated scaffolds, and case-study outputs used in the work.

## Repository contents

- `Supplementary_Material.pdf` — supplementary document with additional experimental details, ablations, and extended discussion.
- `data/MFPD-Bench.jsonl` — the MFPD-Bench evaluation dataset; each line is one evaluation sample.
- `supp/data/` — supplementary task datasets:
  - `Fill-Blank.jsonl`
  - `Multiple-Choice.jsonl`
  - `Sequence-Generation.jsonl`
  - `MFPD-Bench.jsonl`
- `case_study/` — three case studies containing generated protein structures (`.pdb`) and figures (`.png`).
- `MFPD_dplm2_esmfold/` — MFPD-R1 scaffold sequences, DPLM2-completed sequences, and ESMFold structure-prediction outputs.
- `supp/` — additional supplementary artifacts corresponding to the materials above.

## Data format

The benchmark and task datasets are stored as JSON Lines (`.jsonl`): one JSON record per line. This format can be read incrementally in Python, for example:

```python
import json

with open("data/MFPD-Bench.jsonl", encoding="utf-8") as handle:
    for line in handle:
        sample = json.loads(line)
        # Process one evaluation sample.
```

## Large files

Files larger than GitHub's normal per-file limit are stored with [Git LFS](https://git-lfs.com/). To clone the complete repository, install Git LFS before cloning:

```bash
git lfs install
git clone https://github.com/shiyunyun1221/MFPD-R1.git
```

## License and citation

Please use these materials for research purposes and cite the associated Motif-FPD paper when using the datasets, benchmark, or generated results. License and citation metadata will be added with the manuscript release.
