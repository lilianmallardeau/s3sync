# S3 sync

Little command line tool to sync a local folder to an S3 bucket. The bucket is created if it does not exist.

## Usage
First, create a Python virtual environment and install the required dependencies:
```shell
python3 -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
```

### Testing with a local MinIO instance
Start the MinIO container:
```shell
docker compose up -d
```

Then:
```shell
s3sync <folder_path> <bucket_name>
```

### Using with another backend
Change the values of the `API_ENDPOINT`, `API_KEY` and `API_SECRET` variables in the `.env` file to reflect your configuration, and use like previously:

```shell
s3sync <folder_path> <bucket_name>
```
