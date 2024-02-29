# Rill Demo for ClickHouse

### Prerequisite 

- Install Clickhouse
```bash
curl https://clickhouse.com/ | sh
sudo mv clickhouse /usr/local/bin
```
- Install Rill
```base
curl https://rill.sh | sh
```
- Running clickhouse local server
```bash
clickhouse server
```

## Steps to run Rill Demo
Note: Run below steps from root directory of this repo. 

Step 1: Import data for your github repo 
```bash
scripts/data-import.sh <path_to_repo>
```
Step 2: Start rill 
```bash
rill start --db-driver clickhouse --db "clickhouse://localhost:9000" .
```