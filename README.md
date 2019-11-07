# bluehound
Tool for parsing and analyzing sharphound data in Neo4J... and making it pretty

# prereq
```
1.) Run on linux host (pref ubuntu)
2.) You need Sharphound data and neo4j installed (neo4j database doesnt need to be on the same host as bluehound. You will specifiy that config in database.config file. (Recommended: best to place on same host for speed and security - communicates over unencrypted channel to the neo4j database) 
3.) Clone the repo for the same folder structure
4.) Import data from Sharphound into neo4j
5.) Now we can continue
```

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

Now run, `python -m SimpleHTTPServer` and your cwd will be available to browse to on port 8000 in your browser (go to: http://yourip:8000

Click on the report link to view the generated HTML report
