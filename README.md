# Koronotyfikacja

## Workflow
Rules how to deploy changes are must while developing a project in a bigger group. Scrum master has a better feedback what is going on for example - which features are still missing or what has been done already. Also good planning prevents from regression commits and pushing unreadable/uncertain code.

Here is example of how to solve isse - representation of task. Imagine that feature as a FB post, that tell us what should be implemented in our application.

1. Pick issue
Every issue has unique ID. Its value is important and it will be used in next steps as {ISSUE_ID} that is equal to the number after #.

2. Commit local changes

```
git pull
git checkout -b fix/{ISSUE_ID}
git add .
git commit -m "Closed #{ISSUE_ID}
git push -u origin fix/{ISSUE_ID}
```
This commit message must follow this pattern, cause it is automated form of closing issue after merging PR into master branch. If You will not follow this naming convenction, you will have to close it manualy. 

3. Create Pull Request

Pull Request is a form of notifing other colabolators that You request to make changes to master branch. Approvers will decide if changes are valid. In this case you will need only two approves. Also your changes must not contain conflicts with current master branch. If conflict occurs, pull master onto your fix/{ISSUE_ID} branch and manualy solve coflicts.

4. Wait for review
Wait calm for approval of you code

5. Merge 
Voila! Your code is now included in master branch
