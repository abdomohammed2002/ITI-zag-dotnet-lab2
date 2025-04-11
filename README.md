1 - how to remove branch localy ? 
answer: git checkout main 
        git branch -d dev
2 - how to remove branch remotly ?
answer: git checkout main
        git push origin :dev

3 - Annotated tags vs lightweit tags ? 
        annotated tags:
                syntax: git tag -a name -m "message"
                Storage: objects with metadata; lightweight tags are just refs in refs/tags/.
                Use Case: Annotated for formal releases
        lightweit tags: 
                syntax: git tag -a name 
                Storage: are just refs in refs/tags/.
                Use Case: lightweight for quick markers

4 - when to use rebase ?
        use git rebase when you want a cleaner, linear commit history or need to integrate upstream changes without a merge commit.
        Why:
        Clean History: Rebase rewrites your commits on top of another branch (e.g., git rebase main while on feature), avoiding merge commits and keeping the history linear. Ideal for feature branches before merging into main.
        Incorporate Upstream Changes: Use rebase to apply your local commits on top of updated upstream changes (e.g., after git fetch and git rebase origin/main).
        Avoid When: Don’t use rebase on shared branches, as it rewrites history and can cause conflicts for collaborators. Use merge instead in those cases.
5 - How to delete tag locally and remotly ?
        locally : git tag -d tagName
        remotely : git push origin tagName

