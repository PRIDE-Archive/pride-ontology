# PRIDE Ontology

The PRIDE Ontology (PRIDE CV) provides controlled vocabulary terms for proteomics data representation in PRIDE and related resources.

## License

PRIDE ontology is licensed under the [Creative Commons Attribution 4.0 International License](https://creativecommons.org/licenses/by/4.0/).

## Getting Help

For questions, feedback, or support, please contact the PRIDE Helpdesk at the EBI: [pride-support@ebi.ac.uk](mailto:pride-support@ebi.ac.uk).

We welcome error reports, improvement suggestions, and new feature requests.

## Modifying the Ontology

To modify the PRIDE ontology, update the OBO file (`pride_cv.obo`) and convert it to OWL using the following protocol.

### Local Testing of OWL Generation and Validation

To test the ontology conversion and validation process locally, follow these steps:

### 1. Validate the OBO File

Ensure you have Docker installed and run the following command to validate the OBO file using `fastobo-validator`:

```sh
docker run --rm -v "$PWD:/work" -w /work obolibrary/odkfull \
    fastobo-validator --all pride_cv.obo
```

### 2. Convert OBO to OWL and Validate

Use the `robot` tool to generate the OWL file and validate it:

```sh
# Pull the ROBOT container if not already available
docker pull obolibrary/robot

# Convert OBO to OWL
docker run -v "$PWD":/work/ obolibrary/robot \
 robot convert -vvv -i /work/pride_cv.obo -o /work/pride_tmp.owl --format owl

# Validate the OWL file
docker run --rm -v "$PWD:/work" -w /work obolibrary/robot \
    robot report -vvv --input pride_cv.owl --output report.tsv
```

### 3. Review the Validation Report

After running the above commands, check `report.tsv` for validation errors.

### CI/CD Pipeline

This process is automated in the CI/CD pipeline, which runs on every push and pull request to `master` and `dev` branches:

1. **Validate OBO file** using `fastobo-validator`.
2. **Convert OBO to OWL** using `robot`.
3. **Validate OWL file** and generate a report (`report.tsv`).
4. **Upload report** as an artifact.

You can check the CI/CD logs and artifacts for additional details.

---

By following these steps, you can ensure that modifications to the PRIDE ontology maintain consistency and correctness before committing changes.
