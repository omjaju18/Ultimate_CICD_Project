# Jenkins Pipeline for Java based application using Maven, SonarQube, Argo CD, Helm and Kubernetes

![Screenshot 2023-03-28 at 9 38 09 PM](https://user-images.githubusercontent.com/43399466/228301952-abc02ca2-9942-4a67-8293-f76647b6f9d8.png)


Here are the step-by-step details to set up an end-to-end Jenkins pipeline for a Java application using SonarQube, Argo CD, Helm, and Kubernetes:

Prerequisites:

   -  Java application code hosted on a Git repository
   -   Jenkins server
   -  Kubernetes cluster
   -  Helm package manager
   -  Argo CD

Steps:

    1. Install the necessary Jenkins plugins:
       1.1 Git plugin
       1.2 Maven Integration plugin
       1.3 Pipeline plugin
       1.4 Kubernetes Continuous Deploy plugin

    2. Create a new Jenkins pipeline:
       2.1 In Jenkins, create a new pipeline job and configure it with the Git repository URL for the Java application.
       2.2 Add a Jenkinsfile to the Git repository to define the pipeline stages.

    3. Define the pipeline stages:
        Stage 1: Checkout the source code from Git.
        Stage 2: Build the Java application using Maven.
        Stage 3: Run unit tests using JUnit and Mockito.
        Stage 4: Run SonarQube analysis to check the code quality.
        Stage 5: Package the application into a JAR file.
        Stage 6: Deploy the application to a test environment using Helm.
        Stage 7: Run user acceptance tests on the deployed application.
        Stage 8: Promote the application to a production environment using Argo CD.

    4. Configure Jenkins pipeline stages:
        Stage 1: Use the Git plugin to check out the source code from the Git repository.
        Stage 2: Use the Maven Integration plugin to build the Java application.
        Stage 3: Use the JUnit and Mockito plugins to run unit tests.
        Stage 4: Use the SonarQube plugin to analyze the code quality of the Java application.
        Stage 5: Use the Maven Integration plugin to package the application into a JAR file.
        Stage 6: Use the Kubernetes Continuous Deploy plugin to deploy the application to a test environment using Helm.
        Stage 7: Use a testing framework like Selenium to run user acceptance tests on the deployed application.
        Stage 8: Use Argo CD to promote the application to a production environment.

    5. Set up Argo CD:
        Install Argo CD on the Kubernetes cluster.
        Set up a Git repository for Argo CD to track the changes in the Helm charts and Kubernetes manifests.
        Create a Helm chart for the Java application that includes the Kubernetes manifests and Helm values.
        Add the Helm chart to the Git repository that Argo CD is tracking.

    6. Configure Jenkins pipeline to integrate with Argo CD:
       6.1 Add the Argo CD API token to Jenkins credentials.
       6.2 Update the Jenkins pipeline to include the Argo CD deployment stage.

    7. Run the Jenkins pipeline:
       7.1 Trigger the Jenkins pipeline to start the CI/CD process for the Java application.
       7.2 Monitor the pipeline stages and fix any issues that arise.

This end-to-end Jenkins pipeline will automate the entire CI/CD process for a Java application, from code checkout to production deployment, using popular tools like SonarQube, Argo CD, Helm, and Kubernetes.

## Output:
1. Jenkins Success CI

<img width="959" alt="Jenkins Success CI" src="https://github.com/user-attachments/assets/cc0198b5-842e-4fca-be31-e97e27beb301" />

<img width="959" alt="Success CI jenkins" src="https://github.com/user-attachments/assets/3e2a1eaa-59d9-49ec-b516-ebf2c58b67ab" />


2. Image pushed through jenkins pipeline

   <img width="959" alt="Image pushed through jenkins pipeline" src="https://github.com/user-attachments/assets/c8e0f691-0e9b-4f59-9f27-0e4320da7fa1" />

3. Github update image code and Image Updation In the Github Directly through pipeline

  <img width="959" alt="Github update image code " src="https://github.com/user-attachments/assets/146751e5-8260-4ca9-9d99-5a8e84bad202" />

  <img width="874" alt="Updating the image" src="https://github.com/user-attachments/assets/c478a954-57f1-42d4-9bc6-bf0702861f55" />

  <img width="943" alt="Image gets updated in the github " src="https://github.com/user-attachments/assets/49e26497-bf1b-4893-823b-02bdd00718c4" />


4. Sonarqube Passed test

  <img width="959" alt="Sonarqube Passed test" src="https://github.com/user-attachments/assets/bd13b498-e28a-4dbe-9a38-8ffbeaddb70d" />

5. Successfully Deployed on argocd

<img width="950" alt="Successfully Deployed on argocd" src="https://github.com/user-attachments/assets/f0132ad5-a94e-4c16-9dc1-5d42d15ca827" />

