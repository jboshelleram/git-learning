
Create your own branch
----------------------------

* How to

Branch naming convention
----------------------------
```
<initals>/<token>-<scope>-<description> 
```

#### Allowed `<token>`
* wip `'Works in progress; stuff I know won't be finished soon'`
* feat `'Feature I'm adding or expanding'`
* bug `'Bug fix'`
* junk `'Throwaway branch created to investigate/learn'`
* spike `'Experiment that maybe needed later'`

#### Allowed `<scope>`
A single term that represents the area of work.

#### Allowed `<description>`
This can vary. This can be used to version, or give more meaning to the branch.

### Examples  

* jb/feat-kitchensink-v2
* jb/bug-kitchensink-utensil
* jb/junk-kitchensink-demo

* Branch maintenance (how & when to delete, see whos used it etc)


Git Lifecycle
----------------------------

![Alt text](readme/images/lifecycle.png?raw=true "Git Life Cycle")

Keeping your branch up to date
----------------------------

![Alt text](readme/images/uptodate.png?raw=true "Git Life Cycle")

How often should I commit, pull, push, merge?
----------------------------

| Type             | Frequency                         | Notes              |
 ----------------- | --------------------------------- | ------------------
| Commit           | Early and Often               | `'Try to make sure its works. If not, comment it out. But don't be afraid to commit.'` |
| Pull             | Few times a day is sufficient | `'Ensure that you are merging in changes as they come from the upstream branch to prevent merge conflicts and help identify bugs early.'` |
| Push             | Never leave without pushing     | `'Use a working branch independent of the main branch which should not be touched by others. This will make life easier when restructuring your commits before merging back to master.'` |
| Merge to back master  | When Done     | `'I trust this code. It is complete. It runs. I have tested it. I have restructured my commits. I am ready for other people to see it.'` |


Git Commit Good Practice
----------------------------

## Do's

* Only one "logical change" per commit. Per type-scope?

## Dont's

* Mixing whitespace changes with functional code changes.
* Mixing two unrelated functional changes
* Sending large new features in a single giant commit.

Commit Comments
----------------------------
```
<type>(<scope>): <subject>
```

Any line of the commit message cannot be longer 100 characters! This allows the message to be easier to read on github as well as in various git tools.

### Subject line        
Subject line contains succinct description of the change.

#### Allowed `<type>`
* feat (feature)
```
feat($browser): onUrlChange event (popstate/hashchange/polling)
```
* fix (bug fix)
```
fix($compile): couple of unit tests for IE9
```
* docs (documentation)
```
docs(guide): updated fixed docs from Google Docs
```
* style (formatting, missing semi colons, …)
```
style($location): add couple of missing semi colons
```
* refactor
```
refactor: share logic between 4d3d3d3 and flarhgunnstow
```
* test (when adding missing tests)
```
test(config): adding missing tests
```
* chore
```
chore: updating grunt tasks etc; no production code change
```

#### Allowed `<scope>`
Scope could be anything specifying place of the commit change. For example $location, $browser, $compile, $rootScope, ngHref, ngClick, ngView, etc...

#### `<subject>` text
* use imperative, present tense: “change” not “changed” nor “changes”
* don't capitalize first letter
* no dot (.) at the end


```

https://hashnode.com/post/what-tips-and-guidelines-do-you-follow-while-writing-git-commit-messages-cimorctip0010oz53hibbt5a3

https://wiki.openstack.org/wiki/GitCommitMessages

