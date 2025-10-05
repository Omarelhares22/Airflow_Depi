# Airflow_Depi DAG

## Overview

`Airflow_Depi` is a simple Airflow DAG with three tasks:

1. **print_date**: Shows the current date (BashOperator).
2. **print_welcome**: Prints a welcome message with a name (PythonOperator).
3. **generate_random**: Saves a random number to `/tmp/random.txt` (PythonOperator).

Tasks run in order: `print_date` → `print_welcome` → `generate_random`.

## Requirements

- Docker and Docker Compose
- Write access to `/tmp` in the container

## Setup


1. Put `Airflow_Depi.py` in the `dags` folder of your Docker Compose setup.
2. Start Airflow:

   ```bash
   docker-compose up -d
   ```

## Usage

- Open Airflow UI (usually `http://localhost:8080`), log in (default: `airflow`/`airflow`).
- Turn on `Airflow_Depi` and click "Trigger DAG".
- Check logs in the UI and verify `/tmp/random.txt` has a random number.

## Troubleshooting

- **DAG missing**: Check `Airflow_Depi.py` is in the `dags` folder and error-free.
- **File issues**: Ensure `/tmp` is writable in the container.
- **Docker problems**: View logs with `docker-compose logs`.




<div>
<img width= "300"alt="Image" src="https://github.com/user-attachments/assets/49585790-cc6d-4abc-8a25-1087ce550f8d" />
<img width="300" alt="Image" src="https://github.com/user-attachments/assets/34b524c1-6a63-4650-bc8d-a2d29aac1eb5" />
<img width="300" alt="Image" src="https://github.com/user-attachments/assets/87ec40a8-34e0-4b8c-a128-90702c5190c5" />
<img width="300" alt="Image" src="https://github.com/user-attachments/assets/b08cc719-b5ef-44a2-8cc7-08d82a67928e" />
</div>
