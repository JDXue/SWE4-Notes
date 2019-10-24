# 22 Oct
## Morning

#### Tip: Naming Conventions
Make sure that function names that return a boolean can always be answered by a yes/no question

### Testing with Chai :tea:

#### Test Driven Development (TDD)

**Steps to using TDD:**

1. Decide on what you want the program to achieve
2. Write Test
3. Test Fails
4. Write code
5. Test passes
6. Refactor

*and repeat!*

**General Notation for writing tests**
``` js
describe("functionName", () => {
    it("What function will do", () =>{
        const args
        expect(function(args)).to.equal(expectedReturn)
    })
})
```
**Unit Tests** Testing very small parts of a program (base level)

### Git

#### Using git commands in Terminal

1. **git init /RepoName**
2. **make changes to files**
3. **git add .**
4. **git status**
5. **git commit -m "describe changes made"**
6. **make GitHub remote file**
7. **git push -u origin /URL of GitHub Repo**

## Creating a version history through git
* Make some local changes
* Save the changes to your files
* Good habit: check which changes are and aren't staged, git status
* Stage the changes: git add filename.extension; git add . to stage all files
* Commit the changes, git commit -m 'Some helpful commit message (click for guidance)'
* Now, when you run git log, you will see that your commit message is appearing in history

Not completed: Creating a version history through gitMake some lo.... Select to mark as complete.

Git workflow with GitHub
1. Make sure that your local master is up-to-date with the remote master: git checkout master && git pull
2. Branch off master onto a local well-named branch, git checkout -b my-new-feature
3. Make changes, git add ., git commit -m 'Made a change to...', etc.
4. When you want to create an upstream version of your branch, git remote push -u origin my-new-feature
5. If an upstream version of the branch exists already, to push changes to the remote version, git push
6. Once you are happy, open a Pull Request through GitHub for that remote branch (e.g. onto the remote master)
7. Somebody else will probably review your code, make suggestions and then ultimately merge the pull request
8. To pull down changes from an upstream version of a branch, git checkout branch-name && git pull