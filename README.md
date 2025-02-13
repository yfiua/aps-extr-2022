# aps-extr-2022
This repository contains the instruction and code to get and extract the American Physical Society (APS) publication and citation data. We use the 2022 version as example here. For other versions of the data you might need to adapt the code a bit.

## Request data

With a reasonable request to <https://journals.aps.org/datasets-announcement>, you will get the links to download two zip files,
`aps-dataset-citations-2022.zip` and `aps-dataset-metadata-2022.zip`.

## Extract zipped data

```sh
unzip aps-dataset-citations-2022.zip
unzip aps-dataset-metadata-2022.zip 2> unzip-errors.log
```

Check the error log for any issues.
Fix a possibly corrupted filename.

```sh
cat unzip-errors.log
mv aps-dataset-metadata-2022/PRD/85/PhysRevD.\(5.023532.json aps-dataset-metadata-2022/PRD/85/PhysRevD.85.023532.json
```
