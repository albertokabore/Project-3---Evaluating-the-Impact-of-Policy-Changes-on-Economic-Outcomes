# Notebook and VS Code accuracy review

Review date: October 1, 2026.

## Verified local facts

The supplied CSV contains 588,101 rows, seven columns, 14,843 recorded conversions, no missing values, and no duplicate user IDs. The ad group contains 564,577 records and 14,423 conversions; the PSA group contains 23,524 records and 420 conversions. The observed difference is approximately 0.769 percentage points, or 43.1% relative to the PSA rate. These are descriptive file statistics.

CSV SHA-256: `de6ce8def1a6559e9e5ab364fce07cfe2e84f02dd407c3586eea55743c7e17f2`.

No input records were synthesized or changed. The Kaggle source listing was located, but original empirical authenticity and exact hosted-file identity were not verified. The notebook therefore cannot be certified as using verified real-world experimental data. Primary collection documentation is still needed to satisfy that requirement.

## Corrections

- Added introduction, observations, final insight, recommendations, conclusion, and source references.
- Removed unsupported causal, calibration, statistical-significance, and model-equivalence claims.
- Explained that correlated raw/log exposure terms must be interpreted jointly, and full one-hot category contrasts require scale adjustment.
- Distinguished average precision from trapezoidal precision-recall area; retained `pr_auc` as a documented historical field name.
- Removed the constant baseline's duplicate, misleading F1-optimal row. Its ranking capture is now the expectation under random tie-breaking; lift uses the actual selected fraction.
- Disclosed full-data EDA, non-nested threshold selection, uncertain feature timing, and missing external validation.
- Clarified that the notebook analyzes marketing conversion, not economic-policy impacts.
- Removed blanket FutureWarning suppression and added package versions and the dataset hash to the analysis.

## VS Code

Read the available user settings and confirmed Python, Pylance, and Jupyter extensions are installed. Added workspace settings for the verified Python executable and repository-root notebook working directory. Added extension recommendations. No global settings were changed.

The notebook's live kernel selection cannot be established from its generic `python3` metadata. The workspace default interpreter does not force an existing notebook's kernel. Select the matching interpreter using VS Code's kernel picker and compare the executable printed in the setup cell. See [Microsoft's notebook documentation](https://code.visualstudio.com/docs/datascience/jupyter-notebooks).

## Outstanding information and scope

The author identified himself as Albert Kabore, PhD student in AI. This supplied name and status now appear in the notebook and Word report.

The Word report has now been rebuilt using the revised notebook narrative and saved numerical results. The older PDF is explicitly labeled LEGACY_UNREVIEWED and is not the current deliverable.

The supplied assignment concerns marketing prediction. Its requirement for demographics and purchase history is not fully met by the campaign-exposure dataset. The separate grading rubric and source collection documentation have not been supplied. Recommendations describe future work, not completed experiments or demonstrated business returns.

## Execution and verification

Executed all 27 code cells from a fresh Python kernel with nbconvert; process exit code 0 and no notebook error outputs. Checked notebook schema, compiled cell source, matched metrics JSON to CSV, checked coefficient selection counts and the 11-value CV grid, and rechecked the unchanged dataset hash. Figures and result files were regenerated.

Tuned L1 test ROC-AUC: 0.860087; average precision: 0.142006; F1: 0.240192. The 1-SE L1 fit retains 22 encoded coefficients and has AP 0.137810.

The Windows run emitted event-loop/IPython permission warnings and joblib resource-tracker cleanup KeyErrors. These did not prevent cell completion or artifact writing; the environment should not be described as warning-free. No convergence warning was observed in saved outputs unless listed below.

Saved cell warning summaries: []

## Assignment-specific report revision

Revised the notebook narrative to explain the analysis in a natural academic voice, preserving the previously executed code and outputs. Retained bullet formatting for observations, final insight, and recommendations. Rebuilt the Word report with Introduction, Data Collection, Data Preprocessing, Model Selection & Regularization, Training & Hyperparameter Tuning, Evaluation, Interpretation, Conclusion, and References. Added an explicit requirements appendix. Checked the report structure, embedded figures, saved-result consistency, and author metadata. Word pagination was not visually rendered in this environment.

The numerical workflow was not rerun for this prose-only revision: all 27 code cells and saved outputs were preserved from the earlier successful execution.

## Expanded report and APA references

Created report/Project3_Regularization_Report_APA_Expanded.docx because the previous Word file was locked with a Word lock file present. Added detailed model formulation, preprocessing order, solver settings, CV fit counts, classification errors, model-score differences, worked coefficient contrasts, and sparse-term interpretation. These details use the existing model outputs and the unchanged input file; no fitted models or observations were fabricated.

References now use APA author-date citations, alphabetization, italicized titles/journal volumes, hanging indents, and live external URL relationships. Verified 12 references, all nine required sections, and five embedded figures. Source metadata for the peer-reviewed papers was checked against JMLR and PLOS; software references point to official documentation. The dataset listing remains distinct from verified empirical provenance. Visual Word pagination was not rendered.

## Author-confirmed dataset source

Albert Kabore confirmed that marketing_AB.csv was obtained from https://www.kaggle.com/datasets/faviovaz/marketing-ab-testing. Updated the notebook and report to state this explicitly, separating the confirmed download source from independently unverified original collection details. This supersedes earlier wording suggesting the download source was unconfirmed. The expanded Word file was locked, so the corrected deliverable is report/Project3_Regularization_Report_APA_Corrected.docx.

## Impersonal academic wording

Revised narrative passages to remove first-person language while retaining Albert Kabore as author. Rebuilt report/Project3_Regularization_Report_APA_Revised.docx and verified its paragraphs and tables contain no first-person pronouns. All nine required sections, 12 reference links, five figures, and numerical results are retained. Notebook code and executed outputs are unchanged; no observations or model results were fabricated.

## Assignment example and analytical emphasis

The latest assignment text explicitly identifies the Marketing A/B Testing Kaggle dataset as its example. This supersedes earlier conclusions that the selected dataset required separate instructor approval. Rebalanced the notebook and report around descriptive analysis, preprocessing, regularization, tuning, evaluation, and coefficient interpretation. Added data-derived exposure summaries and day-level counts to the Word report, and included timing and cumulative-gains figures. Consolidated the main inference qualifications into one short concluding paragraph. The current deliverable is report/Project3_Marketing_Analytics_Report.docx. Verified nine required sections, seven embedded figures, 12 reference hyperlinks, unchanged input hash, and preserved notebook code/outputs.

## Report cleanup

Verified and retained Project3_Marketing_Analytics_Report.docx as the sole report document. Removed all superseded Word reports and the legacy PDF after their locks were released. The build script, formatting helper, and reference metadata remain available for reproduction. Earlier entries describing preserved report copies are historical and superseded by this cleanup.
