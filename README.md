# bluehound
Tool for parsing and analyzing sharphound data in Neo4J... and making it pretty


# install
```
pip3 install ansicolors
pip3 install neo4j
Edit database.config for password and host
```

# running
Run `python3 bluefox.py -h` for options to choose password and single domain

This may take some time depending on how large the dataset is. 10K node network takes about 10 minutes.

After it completes, a new file is created called `out.json`, you can view it if you'd like

Next, run `python pretty_bluefox.py`

This takes the out.json data and populates it into the HTML template located at templates/black_dashboard/dashboard.html

Once complete, cd into the directory 'cd templates/black_dashboard'

Now run, `python -m SimpleHTTPServer` and your cwd will be available to browse to on port 8000 in your browser (go to: http://<ip>:8000

Click on the report link to view the generated HTML report
