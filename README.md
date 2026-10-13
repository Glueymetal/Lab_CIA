CI_CD_ASSESSMENT
Name: Jeyashree Muthukumaran
Class: IoT A
Registration Number: 23011102033

1. GitHub: Hosted the Starter project on my local repository and created branch "course_withdrawal" to work on the Tasks given.
Commands used:
git add
git status
git remote add origin
git commit
git push origin main
git checkout -b <branch-name>

2. Maven: Reconfigure the project structure to have Parent and Child Pom and wrote JUnit tests for the feature asked to be implemented and fix to be made
Commands used:
mvn clean test
mvn package

3. Jenkins pipeline:
Wrote a Jenkinsfile to drive the Maven process and to fetch the project from the remote repository I have created
Pipeline Stages: Checkout SCM -> Tool Install -> Checkout -> Clean and Test -> Package -> Archive Artifacts -> Post Actions

4. Kubernetes deployment:
Demonstrated the ability to deploy a containerized application on Kubernetes using
Minikube and manage its availability through Kubernetes resources with the help of the following commands and also by creating deployment.yaml and service.yaml
Commands used:
minikube start
kubectl get pods --show-labels
kubectl get service nginx-service
kubectl get endpoints nginx-service
kubectl scale deployment/nginx-deployment --replicas=3
kubectl get pods -w

5. Change summary:
According to the Part E, I had to implement the Withdrawal Function, with the help of the existing functions and unit tests, I was able to reconstruct a simple Withdrawal Function and Unit-tests
I have written three unit-tests:
- SuccessfulWithdrawal() - to check whether the Withdrawal was succesful.
- WithdrawalofNonRegisteredCourse() - How does it handle withdrawal of course where the student haven't registered yet.
- ApplyingtoVacantSeatsAfterWithdrawal() - How vacant seats are handled after withdrawal of a student from a particular registration.
