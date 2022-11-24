# DynamoDB migration script

Simple Python script to migrate the content of an AWS DynamoDB table to another.

It consists of two main fucntions that can be used independently:
- `export_ddb` to export data from a DynamoDB database
- `import_ddb_from_ddb_json` (or `import_ddb_from_dict_json` if it's not in DynamoDB format) to import data to a DynamoDB database

The import functions use the AWS CLI command `aws dynamodb batch-write-item`, so it will NOT overwrite the existing data in the import table.

## Requirements

- Python >= 3.9
- AWS CLI >= 2.7

It doesn't need any Python virtual environement to be run in as it doesn't require any external Python module.

## How to

- Set up your AWS credentials and region

- Edit at your convenience and run the main script:
```bash
python3 main.py
```

- Input the DynamoDB table name to export as and the DynamoDB table name to import as, as prompted.
