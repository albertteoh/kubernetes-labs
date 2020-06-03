# Getting Started

This demo is based on the Docker example-voting-app. The following link details the example including architecture diagram: https://github.com/dockersamples/example-voting-app.

You can run this example by setting up a free GCP account: https://cloud.google.com/.

## Setting up a K8s Cluster in GCP

1. On the main menu, under "Compute", select "Kubernetes Engine"->"Clusters".
2. Create a new Cluster accepting the defaults. This will take a few minutes to spin up.
3. Once you see the green tick, click on "Connect".
4. Copy the kubectl command then click the "Run in Cloud Shell" button, which brings up a terminal.
5. In the terminal, paste the command (if not already pasted) then Enter.

# Deploying on K8s Cluster
```
$ git clone https://github.com/albertteoh/kubernetes-labs.git
$ cd kubernetes-labs/dockersample-votingapp
$ kubectl create -f .

# Wait for everything to be in a RUNNING state
$ kubectl get pods
```

# Validating the Deployment

1. Once all pods are up and running, click on the "Services & Ingress" menu item on the left panel.
2. Look for the "voting-service" then click on the IP address under the "Endpoints" column. It should open up a new tab containing a voting interface for Cats and Dogs.
3. Look for the "result-service" then click on the IP address under the "Endpoints" column. It should open up a new tab containing a result interface showing the voting results.
4. Click on the Cats and Dogs buttons from the "vooting-service" web page then switch over to the "result-service" page to view the results, which should be changing.
