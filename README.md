# Rill Demo for ClickHouse

### Prerequisite 

- Clone this repo 
```bash 
git clone git@github.com:rilldata/git-commits-demo.git && cd git-commits-demo 
```
- Install Clickhouse
```bash
curl https://clickhouse.com/ | sh
```
- Start clickhouse local server
```bash
clickhouse server
```

- Install Rill
```base
curl https://rill.sh | sh
```


## Steps to run Rill Demo
Note: Run below steps from root directory of this repo. 

Step 1: Import data for your github repo  
```bash
scripts/data-import.sh git@github.com:ClickHouse/ClickHouse.git
```
Change the repo url to use your own repo. 
 
Step 2: Start rill (Assumes clickhouse is running on localhost:9000)
```bash
rill start --db-driver clickhouse --db "clickhouse://localhost:9000" .
```

This would open up browser with a Rill dashboard showing commits for your repo.