# EX288 - Exam preparation

### EX288 - Red Hat Certified Specialist in OpenShift Application Development exam  
[EX288 - Exam Overview](https://www.redhat.com/en/services/training/ex288-red-hat-certified-specialist-openshift-application-development-exam?section=Overview)  
[EX288 - Exam Objectives](https://www.redhat.com/en/services/training/ex288-red-hat-certified-specialist-openshift-application-development-exam?section=Objectives)
  
### Version:  
EX288V46k  

### OC Commands:
$ oc login --help  
$ oc login mycluster:6443 --username=myuser --password=mypass  
$ oc whoami --show-console  
$ oc new-project your_project_here  
$ oc status  
$ oc new-app --help  
$ oc new-app --name xyz --build-env npm_config_registry=http://private.registry.com/nodejs http://mygit.com/xyz.git  
$ oc delete all -l app=myapp  
$ oc logs -f bc/xyz  
$ oc start-build --follow bc/xyz (start a new build e.g. if you've made code changes)  
$ oc expose --help  
$ oc expose service xyz --hostname=xyzbuild.apps.cluster.domain.example.com  
$ oc get route 
$ oc create -f ~/your_template.json
$ oc new-app --help (see template example)
$ oc new-app --template=oujfbp-common/php-mysql-ephemeral \
  -p NAME=quotesapi \
  -p APPLICATION_DOMAIN=quote-${RHT_OCP4_DEV_USER}.${RHT_OCP4_WILDCARD_DOMAIN} \
  -p SOURCE_REPOSITORY_URL=https://github.com/${RHT_OCP4_GITHUB_USER}/DO288-apps \
  -p CONTEXT_DIR=quotes \
  -p DATABASE_SERVICE_NAME=quotesdb \
  -p DATABASE_USER=user1 \
  -p DATABASE_PASSWORD=mypa55 \
  --name quotes
$ oc cp ~/your_source_file your_pod:/tmp/your_dest_file
$ oc rsh -t your_pod

### VALIDATE JSON:
$ python3 -m json.tool my.json

### GIT Commands:
$ git clone https://github.com/myrepo.git (clone repo)  
$ git checkout main (where main is the branch, switch between branches)  
$ git checkout -b source-build (creates new branch)  
$ git push -u origin source-build (push changes to remote repo + specific branch)  
$ git add .  
$ git commit -m "my changes"  
$ git push  
