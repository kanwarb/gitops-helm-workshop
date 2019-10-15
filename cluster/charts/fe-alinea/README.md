##  Nuxeo Helm Chart


##  This chart has been customized for use internally .


### Nuxeo Frontend 

####  How to Install the first Time 
      
      - Before installing please use helm list to verify if chart is installed

      - Run helm command from the chart root directory above nuxeo folder

      $ helm install nuxeo --namespace < Install Namespace > --n <Name of Install> --set nuxeo.packages="nuxeo-web-ui nuxeo-drive nuxeo-vision"
 
      EXAMPLE
      $ helm install nuxeo --namespace nuxeo --n nuxeo-fe --set nuxeo.packages="nuxeo-web-ui nuxeo-drive nuxeo-vision"


####  How to list 

      From anywhere on your desktop

      $ helm list

####  How to Upgrade using this chart

      - cd <Directory of the Chart where the values.yaml is> eg  $HOME/nuxeo/     
      - $ helm upgrade --install <Name of Install during Create> .  --recreate-pods --set nuxeo.packages="nuxeo-web-ui nuxeo-liveconnect nuxeo-drive"

      EXAMPLE
      - $ helm upgrade --install nuxtest .  --recreate-pods --set nuxeo.packages="nuxeo-web-ui nuxeo-liveconnect nuxeo-drive"


#### How to delete the installed chart
   
     - From any location on machine where helm is present eg desktop / bastion host

     - $ helm delete <Name of Install> --purge

#### Additional References for more Details

Inherited from Chart :  https://github.com/nuxeo/nuxeo-helm-charts

