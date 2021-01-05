# Install Node.js on IBM cloud

## Pre-requisites
You must have an account created in IBM cloud, the account must be *Pay-As-You-Go* or *Subscription*. You can read more, [here](https://cloud.ibm.com/docs/account?topic=account-accounts "here").
If you have a Lite account, you can upgrade it, see [this](https://cloud.ibm.com/docs/account?topic=account-account-getting-started#account-gs-upgrade "this").

## Step 1: Provision Kubernetes Cluster

* Click on the search section at the top of the main page, type Kubernetes and choose Kurbenetes cluster

![Screenshot](Kubernetes1.PNG)

* A new window opens, in "Pricing plan", you can choose between the free and standard type, in this example we choose the free plan, and click on create.

![Screenshot](Kubernetes2.PNG)

* We wait a few minutes, when the cluster is ready the following ad appears.

![Screenshot](Kubernetes3.PNG)

## Step 2:  Deploy IBM Cloud Block Storage plug-in

* Click on the search section at the top of the main page, IBM cloud block storage and click it.

![Screenshot](Storage1.PNG)

* A new window opens,select the cluster and put the name you want to the workspace in this case it will be called storage-example, we click on install and wait a few minutes.

![Screenshot](Storage2.PNG)


## Step 3: Install Node.js

* Click on the search section at the top of the main page, type Node.js and choose it.

![Screenshot](node1.PNG)

* A new window opens, select the cluster and put the name you want to the workspace, in this case it will be called _node-example_, accept the terms and click on install. You can modify the different installation parameters at the bottom, in our example we will leave them default, you can read more about the parameters [here](https://cloud.ibm.com/catalog/content/node-Qml0bmFtaS1ub2Rl-global "here").

![Screenshot](node2.PNG)


## Step 4: Verify Installation

* Go to the *Resources List* in the Left Navigation Menu and click on *Kubernetes*

![Screenshot](test1.PNG)


* Click the *Actions* button and select *Web terminal*.

![Screenshot](test2.PNG)


* A window opens to install the web terminal, click install and wait a few minutes.

![Screenshot](test3.PNG)


* When the terminal is installed, click on the action button again and click on web terminal and type the following command. It will show you the workspaces of your cluster, you can see *node-example* active.

`$ kubectl get ns`

![Screenshot](test4.PNG)


`$ kubectl get pod -n node-example -o wide`

![Screenshot](test5.PNG)

`kubectl get service -n node-example`

![Screenshot](test6.PNG)

Installation is complete, enjoy!
