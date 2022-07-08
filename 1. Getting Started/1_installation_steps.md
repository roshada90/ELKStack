Go to the following location to install elastic search and kibana


Kibana
https://www.elastic.co/downloads/kibana


Elastic search
https://www.elastic.co/downloads/elasticsearch


Extract above downloads with the following commands

1. cd /path/to/archive/directory
2. tar -zxf archive.tar.gz

To start elastic search
1. Go to the directory where elastic search is installed
2. go to bin/elasticsearch


✅ Elasticsearch security features have been automatically configured!
✅ Authentication is enabled and cluster connections are encrypted.

ℹ️  Password for the elastic user (reset with `bin/elasticsearch-reset-password -u elastic`):
  4FLI=tvC0aL=ryTbvI1H

ℹ️  HTTP CA certificate SHA-256 fingerprint:
  ab1f09070fd8ef0b99b7b0da4fd1b5e1b87852c31fce74a90f24f37dcf34275c

ℹ️  Configure Kibana to use this cluster:
• Run Kibana and click the configuration link in the terminal when Kibana starts.
• Copy the following enrollment token and paste it into Kibana in your browser (valid for the next 30 minutes):
  eyJ2ZXIiOiI4LjMuMiIsImFkciI6WyIxOTIuMTY4LjEuMTAzOjkyMDAiXSwiZmdyIjoiYWIxZjA5MDcwZmQ4ZWYwYjk5YjdiMGRhNGZkMWI1ZTFiODc4NTJjMzFmY2U3NGE5MGYyNGYzN2RjZjM0Mjc1YyIsImtleSI6ImQwTW0zNEVCa2RZQTlPN0daaEV5OmRJSldqQi00U3dhX2E3LUFJUGhlSVEifQ==

ℹ️  Configure other nodes to join this cluster:
• On this node:
  ⁃ Create an enrollment token with `bin/elasticsearch-create-enrollment-token -s node`.
  ⁃ Uncomment the transport.host setting at the end of config/elasticsearch.yml.
  ⁃ Restart Elasticsearch.
• On other nodes:
  ⁃ Start Elasticsearch with `bin/elasticsearch --enrollment-token <token>`, using the enrollment token that you generated.


Disabling gatekeeper for the kibana directory

xattr -dr com.apple.quarantine /path/to/kibana

now in kibana directory, run 
1. bin/kibana


now go to kibana url on the terminal and add enrollment token and username and password

