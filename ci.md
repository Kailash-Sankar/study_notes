
# CI/CD Notes

### setup jfrog artifactory npm repo for local project
      # login in to jfrog
      # create an api key
      # go to you project folder
      # add jfrog repo url
      echo "_registry=<registry_url>" >> .npmrc
      
      # add auth info
      curl -u<username> <jrgo_repo>/api/npm/auth >> .npmrc
      
      
