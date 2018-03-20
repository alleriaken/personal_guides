# Install gcloud sdk
	```https://cloud.google.com/sdk/docs/quickstart-windows```

# Login and set default application
	```gcloud auth login```
	```gcloud auth application-default login```

# Download cloud sql proxy 
	```https://cloud.google.com/sql/docs/mysql/connect-admin-proxy```
	
# Start the proxy
	cloud_sql_proxy_x64 -instances=<INSTANCE_CONNECTION_NAME>=tcp:<port>