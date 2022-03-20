Git utils commands :

Check modified files :
        git status
Undo local modification on a file :
       git restore <file>
Cancel all local changes :
       git restore .
Stash of modifications
       git stash
       git stash pop (to get the changes)
Delete commit but keep the changes:
       git reset HEAD^
Rename commit :
       git commit --amend -m "<My new commit message>"
Rename branch :
 For current branch :
          git branch -m <newname>
 For any branch :
          git branch -m <oldname> <newname>
Delete local branch :
          git branch -D [branch_name]
Delete remote branch :
          git push origin --delete [branch_name]
Reset Branch from an other branch example develop :
         git checkout <myBranch>
         git reset --hard origin/develop
To undo the last commit:
        git reset --hard HEAD~1
        push force will be proposed.
To revert a commit:
        git revert <sha1>
To cherrypick a commit:
        git cherry-pick <sha1>
Combine commits :
        git checkout [my_branch]
        git rebase --interactive HEAD~2
        a vim file will then be opened with two “pick” lines which correspond to our two commits. For example, replace the “pick” of the second line by
        “s” to say squash.
        After saving, second vim will then be opened for commits messages, it suffices to comment out one of the commit message to keep the other, for that we add  “#” at the beginning of the commit message that we do not want not keep it and we save.
To commit changes into last commit :
        git commit --amend --no-edit
