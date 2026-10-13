### CI/CD Assessment

**Name:** Jeyashree Muthukumaran  
**Class:** IoT A  
**Registration Number:** 23011102033

## 1. GitHub

Hosted the starter project in my local repository and created a branch named `course_withdrawal` to work on the assigned tasks.

### Commands Used

- `git add`
- `git status`
- `git remote add origin`
- `git commit`
- `git push origin main`
- `git checkout -b course_withdrawal`

## 2. Maven

Reconfigured the project structure to include a parent POM and a child POM. Wrote JUnit tests for the required feature and fix.

### Commands Used

- `mvn clean test`
- `mvn package`

## 3. Jenkins Pipeline

Created a `Jenkinsfile` to automate the Maven build process and fetch the project from the remote repository.

### Pipeline Stages

`Checkout SCM` → `Tool Installation` → `Checkout` → `Clean and Test` → `Package` → `Archive Artifacts` → `Post Actions`

## 4. Kubernetes Deployment

Demonstrated the deployment of a containerized application on Kubernetes using Minikube and managed its availability through Kubernetes resources.

### Configuration Files

- `deployment.yaml`
- `service.yaml`

### Commands Used

- `minikube start`
- `kubectl get pods --show-labels`
- `kubectl get service nginx-service`
- `kubectl get endpoints nginx-service`
- `kubectl scale deployment/nginx-deployment --replicas=3`
- `kubectl get pods -w`

## 5. Change Summary

As part of Part E, I implemented the course withdrawal functionality using the existing functions and unit tests as references. I reconstructed a simple withdrawal function and wrote three unit tests to verify its behavior.

### Unit Tests Implemented

1. **`SuccessfulWithdrawal()`**
   - Verifies whether a student can successfully withdraw from a course they have registered for.

2. **`WithdrawalofNonRegisteredCourse()`**
   - Checks how the application handles a withdrawal attempt for a course in which the student is not registered.

3. **`ApplyingtoVacantSeatsAfterWithdrawal()`**
   - Checks how vacant seats are handled after a student withdraws from a particular course registration.

These tests validate the withdrawal functionality, handle invalid withdrawal attempts, and verify the handling of available seats after a withdrawal.
