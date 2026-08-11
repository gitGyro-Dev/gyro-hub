# Gyro Publication Checklist

This checklist standardizes the publication lifecycle for Gyro Project research outputs.

Use one copy of this checklist for each paper, preprint, release, translation, or major research artifact.

---

## 1. Publication Identity

- [ ] Project identified: Gyro Logic / GyroOS / GyroAuth / Gyro Hub / Other
- [ ] Official title confirmed
- [ ] English and Japanese titles aligned where applicable
- [ ] Authors and contributor names confirmed
- [ ] ORCID identifiers confirmed
- [ ] Version or release number confirmed
- [ ] Publication language identified
- [ ] Publication type identified: preprint / paper / software release / dataset / research note / other

---

## 2. Source and Repository

- [ ] Source Markdown or manuscript finalized
- [ ] Figures, tables, and equations finalized
- [ ] References validated
- [ ] AI-use disclosure included where required
- [ ] License confirmed
- [ ] `CITATION.cff` validated where applicable
- [ ] Repository README updated
- [ ] Japanese README updated where applicable
- [ ] Relevant documentation index updated
- [ ] Final source committed to GitHub
- [ ] Commit SHA recorded

---

## 3. Pre-publication Multi-AI Critical Review

For major manuscripts, releases, or theory-bearing research artifacts, complete the Multi-AI Critical Review Gate before publication.

- [ ] ChatGPT internal consistency and revision pass completed
- [ ] Claude Code / Claude independent critical review completed
- [ ] Gemini independent critical review completed
- [ ] Claude and Gemini reviews were performed independently before synthesis where practical
- [ ] Review artifacts recorded in `reviews/` or the project-equivalent review location
- [ ] Claude/Gemini did not edit the reviewed source note or publication material directly
- [ ] Review disagreements preserved rather than averaged away
- [ ] Existing review records checked for duplicate or substantially overlapping criticisms
- [ ] Each material criticism classified by ChatGPT before revision as one of:
  - [ ] `valid`
  - [ ] `partially valid`
  - [ ] `misunderstanding`
  - [ ] `needs verification`
  - [ ] `future work`
- [ ] `needs verification` items independently checked before acceptance or rejection
- [ ] Review content was not adopted automatically merely because an AI reviewer proposed it
- [ ] Disposition record committed before the corresponding source revision
- [ ] Accepted current-scope criticisms reflected in the revised source
- [ ] `future work` items preserved outside the current revision scope where appropriate
- [ ] Follow-up review completed when substantial issues remained open
- [ ] Operational sequence followed where applicable: `classification record → revised note → re-review`
- [ ] Project owner reviewed the resulting criticism/revision record before publication

Reference operating model: [`../research_cycle.md`](../research_cycle.md).

---

## 4. PDF and Artifact Validation

- [ ] Publication PDF generated
- [ ] PDF title, author, abstract, and references verified
- [ ] Figures and fonts rendered correctly
- [ ] Page layout reviewed
- [ ] Embedded links verified
- [ ] DOI placeholders removed or explicitly marked as pending
- [ ] Final PDF committed to GitHub
- [ ] Supplementary files included where applicable

---

## 5. GitHub Release

- [ ] Release scope confirmed
- [ ] Release candidate review completed
- [ ] Release notes prepared in English
- [ ] Release notes prepared in Japanese where applicable
- [ ] Git tag created
- [ ] GitHub Release published
- [ ] Release assets attached
- [ ] Release URL recorded

---

## 6. Zenodo

- [ ] GitHub–Zenodo integration confirmed
- [ ] Zenodo deposition created from the intended release
- [ ] Metadata reviewed
- [ ] Title and abstract match the publication language
- [ ] Authors and ORCID identifiers verified
- [ ] Related identifiers added where applicable
- [ ] License verified
- [ ] Zenodo record published
- [ ] Version DOI recorded
- [ ] Concept DOI recorded where applicable
- [ ] Zenodo DOI added to the manuscript or repository where appropriate

---

## 7. Jxiv

### English edition

- [ ] English manuscript finalized
- [ ] English PDF validated
- [ ] Jxiv submission completed
- [ ] Metadata language verified
- [ ] Title and abstract verified
- [ ] Author name and ORCID verified
- [ ] Publication status confirmed
- [ ] Jxiv DOI resolves correctly
- [ ] Jxiv DOI recorded

### Japanese edition

- [ ] Japanese translation finalized
- [ ] Technical terminology aligned with the English edition
- [ ] Japanese PDF validated
- [ ] Jxiv submission completed
- [ ] Metadata language verified
- [ ] Title and abstract verified
- [ ] Author name and ORCID verified
- [ ] Publication status confirmed
- [ ] Jxiv DOI resolves correctly
- [ ] Jxiv DOI recorded

### Cross-edition consistency

- [ ] English and Japanese editions reference each other where appropriate
- [ ] Titles, versions, and publication dates are consistent
- [ ] DOI links point to the intended language edition
- [ ] PDF language matches metadata language

---

## 8. ORCID

- [ ] Work imported automatically or added manually
- [ ] Correct DOI attached
- [ ] Title language verified
- [ ] Publication type verified
- [ ] Author role verified
- [ ] Visibility set to `Everyone`
- [ ] Duplicate or similar works reviewed
- [ ] English edition featured where appropriate
- [ ] Featured Works order reviewed
- [ ] Gyro Hub, GitHub Organization, and X links remain current

---

## 9. ResearchHub

- [ ] ResearchHub profile is complete
- [ ] ORCID is connected
- [ ] X profile is connected where appropriate
- [ ] Publication found by title or DOI
- [ ] Imported metadata reviewed
- [ ] Title and abstract language verified
- [ ] Research Note prepared
- [ ] Discussion question prepared
- [ ] DOI link included
- [ ] GitHub repository or Gyro Hub link included
- [ ] Zenodo or demo link included where useful
- [ ] Research Note published
- [ ] Discussion published
- [ ] Comments and questions monitored
- [ ] Relevant feedback recorded for the Gyro Project Cycle

Templates:

- [`../templates/researchhub/research_note_template.md`](../templates/researchhub/research_note_template.md)
- [`../templates/researchhub/discussion_template.md`](../templates/researchhub/discussion_template.md)
- [`../templates/researchhub/initial_posts.md`](../templates/researchhub/initial_posts.md)

---

## 10. Gyro Hub

- [ ] `papers.md` updated
- [ ] `projects.md` updated where applicable
- [ ] `dashboard.md` updated
- [ ] Dashboard data updated
- [ ] `artifacts.md` or artifact data updated
- [ ] `links.md` updated
- [ ] Roadmap updated where publication changes project status
- [ ] Current weekly report updated
- [ ] Project Cycle Reflection received and applied

---

## 11. Communication

- [ ] X announcement prepared
- [ ] English announcement published where appropriate
- [ ] Japanese announcement published where appropriate
- [ ] DOI link verified before posting
- [ ] GitHub or Gyro Hub link included
- [ ] ResearchHub discussion linked after publication
- [ ] Follow-up communication planned if external feedback arrives

---

## 12. Feedback and Continuation

- [ ] ResearchHub feedback reviewed
- [ ] GitHub issues or discussions created for actionable feedback
- [ ] Corrections distinguished from future research extensions
- [ ] Required repository updates identified
- [ ] Required manuscript updates identified
- [ ] Toolkit improvements identified
- [ ] Roadmap implications identified
- [ ] Next publication or revision candidate recorded
- [ ] Significant external feedback routed back through the Multi-AI Critical Review process where appropriate

---

## 13. Completion Record

- **Project:**
- **Publication:**
- **Version:**
- **GitHub repository:**
- **Commit SHA:**
- **GitHub Release:**
- **Zenodo DOI:**
- **Jxiv DOI (English):**
- **Jxiv DOI (Japanese):**
- **ORCID record:**
- **ResearchHub post:**
- **ResearchHub discussion:**
- **X announcement:**
- **Completion date:**
- **Remaining issues:**

---

## Publication Flow

```text
Research and implementation
        ↓
GitHub source and documentation
        ↓
Multi-AI Critical Review
        ↓
Disposition classification and duplicate check
        ↓
Revision and human judgment
        ↓
Independent re-review
        ↓
GitHub release
        ↓
Zenodo archive and DOI
        ↓
Jxiv preprint publication
        ↓
ORCID research record
        ↓
ResearchHub discussion and review
        ↓
X communication
        ↓
Feedback returned to GitHub and Gyro Project Cycle
```
