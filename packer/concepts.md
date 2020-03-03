Packer has templates that are json files.  
What are the Template components?  

- builder: Is this going to be an image for AWS, or a Docker image?  
- description: Description of the machine image  
- min_packer_version: version of Packer used  
- post-processors: What actions to perform after the machine image has been created, such as tagging the image, publishing a Docker image to a repo.  
- provisioners: How we are going to provision our machine images? (ansible, chef, puppet, script)  
- variables: key-value pairs that will be used in our templates  

