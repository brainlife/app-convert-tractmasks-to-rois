<h1 align="center">Convert tract masks to ROIs</h1>

<p align="center">
  A rois dataset from a tractmasks dataset, with the mask images left unchanged.
</p>

<p align="center">
  <a href="https://github.com/brainlife/abcd-spec"><img src="https://img.shields.io/badge/ABCD_Spec-v1.1-green.svg" alt="ABCD Spec v1.1"></a>
  <a href="https://doi.org/10.25663/brainlife.app.707"><img src="https://img.shields.io/badge/Brainlife-brainlife.app.707-blue.svg" alt="Run on brainlife.io"></a>
  <a href="LICENSE"><img src="https://img.shields.io/badge/License-MIT-lightgrey.svg" alt="MIT license"></a>
</p>

> 📍 **This branch, `1.0`, is the brainlife.io App Convert tractmasks to rois** ([doi:10.25663/brainlife.app.707](https://doi.org/10.25663/brainlife.app.707)).

## 🧠 At a glance

<!-- brainlife-app:begin (generated from the App manifest; edit the manifest, not this block) -->

> **Converts a tractmasks datatype into a rois datatype by moving the mask files unchanged; a format-conversion utility.**

Moves every file at the top level of the tract masks directory into a rois directory, without changing the images. Use it to feed tract masks to Apps that expect ROIs.

| | |
|---|---|
| 📥 **Inputs** | `neuro/tractmasks` |
| 📤 **Outputs** | `neuro/rois` |
| ⚙️ **Resources** | 0.25 h walltime |
| 🔗 **Run it** | [doi.org/10.25663/brainlife.app.707](https://doi.org/10.25663/brainlife.app.707) |

#### 📥 Inputs

| Input | Datatype | Required | Description |
|---|---|---|---|
| `masks` | `neuro/tractmasks` | yes | Tract masks (one NIfTI per tract). |

#### 📤 Outputs

| Output | Datatype | Description |
|---|---|---|
| `output` | `neuro/rois` | The same masks as a rois datatype. |

<!-- brainlife-app:end -->

## 🚀 Running the App

### ☁️ On brainlife.io

Open the App at [doi.org/10.25663/brainlife.app.707](https://doi.org/10.25663/brainlife.app.707), choose a `neuro/tractmasks` dataset (one NIfTI per tract) and press **Execute**. The App moves every file at the top level of the masks directory into a `rois` directory without changing the images, and archives the result to your project as a `neuro/rois` dataset. Use it to feed tract masks to Apps that expect ROIs.

### 💻 Locally

You need [`jq`](https://jqlang.github.io/jq/) and GNU `find`/`xargs`/`mv`; no container is used.

1. Clone this repository.
2. Create `config.json` with the path to your tract masks directory:

   ```json
   {
       "masks": "/input/tractmasks/masks"
   }
   ```

3. Run the App:

   ```bash
   ./main
   ```

   The mask files are **moved**, not copied, so work on a copy of your data.

## 📦 Outputs

```text
output/
└── rois/   the tract mask files, unchanged, as a rois dataset
```

## 📚 Citing

> [!TIP]
> If you use this App in your work, please cite the App, the software it builds on and brainlife.io (below). GitHub's **Cite this repository** button gives the App citation in APA and BibTeX.

- Convert tractmasks to rois. brainlife.io App. [doi:10.25663/brainlife.app.707](https://doi.org/10.25663/brainlife.app.707)
- Avesani P, McPherson B, Hayashi S, et al. The open diffusion data derivatives, brain data upcycling via integrated publishing of derivatives and reproducible open cloud services. Sci Data 6, 69 (2019). [doi:10.1038/s41597-019-0073-y](https://doi.org/10.1038/s41597-019-0073-y)
- Hayashi S, Caron BA, Heinsfeld AS, et al. brainlife.io: a decentralized and open-source cloud platform to support neuroscience research. *Nature Methods* 21:809–813 (2024). [doi:10.1038/s41592-024-02237-2](https://doi.org/10.1038/s41592-024-02237-2)

## 👥 Authors

- Giulia Bertò
- Antonio Fernandez

## 💰 Funding

[![Wellcome-226486/Z/22/Z](https://img.shields.io/badge/Wellcome-226486%2FZ%2F22%2FZ-purple.svg)](https://wellcome.org/)
[![NIH-NINDS-U24NS140384](https://img.shields.io/badge/NIH_NINDS-U24NS140384-green.svg)](https://reporter.nih.gov/project-details/11261037)
[![NIH-NINDS-UM1NS132207](https://img.shields.io/badge/NIH_NINDS-UM1NS132207-green.svg)](https://reporter.nih.gov/project-details/11411328)
[![NIH-NIBIB-R01EB029272](https://img.shields.io/badge/NIH_NIBIB-R01EB029272-green.svg)](https://reporter.nih.gov/project-details/10262925)
[![NIH-NIBIB-R01EB030896](https://img.shields.io/badge/NIH_NIBIB-R01EB030896-green.svg)](https://reporter.nih.gov/project-details/10428625)
[![NIH-NIMH-R01MH126699](https://img.shields.io/badge/NIH_NIMH-R01MH126699-green.svg)](https://reporter.nih.gov/project-details/10460628)
[![NIH-NIDCD-R01DC020088](https://img.shields.io/badge/NIH_NIDCD-R01DC020088-green.svg)](https://reporter.nih.gov/project-details/11140284)
[![NSF-BCS-1734853](https://img.shields.io/badge/NSF_BCS-1734853-blue.svg)](https://www.nsf.gov/awardsearch/showAward?AWD_ID=1734853)
[![NSF-BCS-2203524](https://img.shields.io/badge/NSF_BCS-2203524-blue.svg)](https://www.nsf.gov/awardsearch/showAward?AWD_ID=2203524)
[![NSF-IIS-1636893](https://img.shields.io/badge/NSF_IIS-1636893-blue.svg)](https://www.nsf.gov/awardsearch/showAward?AWD_ID=1636893)
[![NSF-OAC-2148729](https://img.shields.io/badge/NSF_OAC-2148729-blue.svg)](https://www.nsf.gov/awardsearch/showAward?AWD_ID=2148729)
[![NSF-IIS-1912270](https://img.shields.io/badge/NSF_IIS-1912270-blue.svg)](https://www.nsf.gov/awardsearch/showAward?AWD_ID=1912270)
[![NSF-IIS-2148700](https://img.shields.io/badge/NSF_IIS-2148700-blue.svg)](https://www.nsf.gov/awardsearch/showAward?AWD_ID=2148700)
[![NSF-OAC-1916518](https://img.shields.io/badge/NSF_OAC-1916518-blue.svg)](https://www.nsf.gov/awardsearch/showAward?AWD_ID=1916518)

<sub>brainlife.io is publicly funded, and acknowledging that support helps keep it running. This App was developed with support from Wellcome, the U.S. National Institutes of Health (including the BRAIN Initiative BRAIN CONNECTS program: The Axonal Projectome EXchange, U24NS140384, and the Center for Mesoscale Connectomics, UM1NS132207) and the U.S. National Science Foundation.</sub>

## ⚖️ License

[MIT](LICENSE).
