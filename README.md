# puppet-devops
## Devops Assignment

### TODO:

Modify the manifest environments/test/manifests/site.pp to -

1. Create below directory structure using puppet.
```
/var/www/
└── test-app
    ├── current
    │   └── index.html
    ├── releases
    └── shared
```
2. Create a self signed certificate and add it to modules/nginx/files/ as example.com.crt and example.com.key

3. Fix the site.pp manifest file nginx configuration to match the nginx sample config file testapi.example.com.conf (Additional location blocks in ssl server). Refer the Readme in nginx module for syntaxes.

4. Change the number of worker_processes to 2 in nginx.conf.

5. Test the puppet code using vagrant and resolve issues if any (Vagrantfile is present in the repo).

6. Write a script for the below problem statement, and include that script file in scripts directory.

   Problem Statement : 

	Find file 'new_image.json' under the directory 'scripts'. This supplied JSON file contains an array of Images. Write a script in a language of your choice that takes 3 parameters from the user:

        1. A number of “retention_days” an Image object should be kept before it should be deleted. ie: 90 for "90 days"
        2. A prefix string for Image name to be filtered on: ie "cc-r"
        3. Path to json file: ie: ~/Downloads/images.json

	Problem - Given the above inputs, your script should output both:

        1. the total number of images which are older than the given retention_days are due for deletion.
        2. filtered Images that match the prefix string

	Note:  (todays date - image creation date ) > = retention days

  Script should be run something like this:

  ```
    $ ./images.sh 90 "cc-" ~/Downloads/images.json
  ```

