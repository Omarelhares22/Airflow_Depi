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

## License

MIT License
<div>
<img src "https://github.com/user-attachments/assets/3fea71e4-64c4-4c26-b27d-a50eb2ea729e" width="300">
<img src "https://github.com/user-attachments/assets/3b5432a5-fbe5-4591-88ec-ce2930e1905e" width="300">
<img src "https://github.com/user-attachments/assets/b05078cf-06df-420b-bad6-9bf1e2275123" width="300">
<img width="1920" height="1080" alt="Image" src="https://github.com/user-attachments/assets/0ede2d7b-3e35- />4d44-be9a-ed81bc81a372"
</div>

