# Git Developer-Organization workflow

1. External organization project: https://github.com/georgi-team/project

2. Fork the external organization project: https://github.com/georgi-team/project into your github account. Result after the fork: https://github.com/berchev/project

3. Clone forked project locally: 

```
$ git clone git@github.com:berchev/project.git
```

4. Adding upstream to be the external organization project

```
$ git remote
origin
$ git remote add upstream https://github.com/georgi-team/project.git 
$ git remote
origin
upstream
$ git remote -v
origin  git@github.com:berchev/project.git (fetch)
origin  git@github.com:berchev/project.git (push)
upstream        https://github.com/georgi-team/project.git (fetch)
upstream        https://github.com/georgi-team/project.git (push)
$ 
```

5. Pull changes from the upstream (external project) in order to make sure everything is up to date!

```
$ git pull upstream main
```

6. Create branch in the forked project:

```
$ git checkout -b patch
```

7. Do changes

8. See the changes:

```
$ git status
```

9. Add the changes:

```
$ git add -A
```

10. Verify the changes:

```
$ git status
```

11. Commit the changes:

```
$ git commit -m "Update main.tf"
```

12. Push your feature branch in your remote fork:

```
$ git push origin patch
```

13. Open a PR from the pushed commit
