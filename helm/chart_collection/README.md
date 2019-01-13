# Charts  
_https://docs.helm.sh/developing_charts/_  
   
> Helm uses a packaging format called charts. A chart is a collection of files that describe a related set of Kubernetes resources. A single chart might be used to deploy something simple, like a memcached pod, or something complex, like a full web app stack with HTTP servers, databases, caches, and so on.  
  
## Chart File Structure  
A chart is organized as a collection of files inside of a directory. The directory name is the name of the chart (without versioning information). Thus, a chart describing WordPress would be stored in the wordpress/ directory.  
  
Charts contain a directory with the following setup:  
```sh  
<chartname/>  
  Chart.yaml          # A YAML file containing information about the chart  
  LICENSE             # OPTIONAL: A plain text file containing the license for the chart  
  README.md           # OPTIONAL: A human-readable README file  
  requirements.yaml   # OPTIONAL: A YAML file listing dependencies for the chart  
  values.yaml         # The default configuration values for this chart  
  charts/             # A directory containing any charts upon which this chart depends.  
  templates/          # A directory of templates that, when combined with values,  
                      # will generate valid Kubernetes manifest files.  
  templates/NOTES.txt # OPTIONAL: A plain text file containing short usage notes  
```  
