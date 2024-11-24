+++
title = "Autosaving in Xcode"
date = "2015-12-24T10:02:09-08:00"

#
# description is optional
#
# description = "An optional description for SEO. If not provided, an automatically created summary will be used."

tags = ["coding"]
+++

While working on a Swift Project recently, I spent ~ 4 hours adjusting a few pop-ups and fine tuning design for a screen. As it so happens, while working in the zone, I missed any committing and committed the code after my entire sprint.

Now, the other day, I was helping out a colleague with git and explaining git checkout. As it turns out, my brain decided to remind myself of the command exactly while committing and I ended up typing

```
git checkout . (instead of git add .)
git commit -m "My Commit Message" 
git push origin feature-branch
```

I didn’t realize my mistake until I came back to XCode and notice all the 4+ hours of work totally undone. Panicked, my first reaction was to find out how to undo files from an accidental checkout. Turns out, you cannot. Unless you have ever used git add or git stash on the files, there’s nothing that can be done.

I was about to lose hope when I saw an answer on SO on looking through the IDE’s auto save files. A bit more searches later - turns out OS X does auto-save files.

Gladly, I was able to get back the entire code in an auto-saved version 2-3 hours back and the day was saved thanks to auto-save.

However this is a lesson on reinforcing strict programming / source control habits. Always think once before you use . operator - And twice before using git checkout . Make sure you add / stash your code in smaller task increments. finished a small task - add to the index. Going to work later?, stash it

