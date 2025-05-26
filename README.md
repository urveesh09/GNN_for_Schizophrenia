## GNN-based Schizophrenia Link Prediction Implementation

This repository encapsulates the source code accompanying a research paper on Graph Neural Network (GNN) applications for schizophrenia ncRNA Link Prediction.

### Key Technical Considerations:

1.  **Data Ingestion:** All requisite datasets are co-located within the `source` directory. This design decision simplifies data referencing, allowing all data access paths to be resolved relative to `BASE_DIR`. This implies that `BASE_DIR` is the root directory containing the `source` directory, and relative paths will be constructed accordingly within the codebase.

2.  **Codebase Evolution and Path Dependency:** The codebase reflects an iterative development process, incorporating multiple optimization and refinement cycles. Consequently, **absolute or hardcoded file paths within the scripts may not universally align with the current directory structure or the assumed `BASE_DIR` context.** Developers should be prepared to verify and potentially adjust file system paths to ensure correct data loading and script execution. This suggests a potential for `FileNotFoundError` or similar I/O exceptions if the execution environment's directory structure deviates from the development environment's implicitly assumed paths.