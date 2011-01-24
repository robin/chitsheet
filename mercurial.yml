--- 
mercurial: |-
  Quick Start
  ===========
  
  Create a new repository:
  hg init
  
  Add new files and delete all old files to repository:
  hg addremove
  
  Commit with message
  hg commit -m "the commit message"
  
  Push your changes to the repo
  hg push <repo url>
  
  
  Using the Built-in Help
  -----------------------
  
  Mercurial has excellent built-in documentation that can keep this cheat short:
  
      hg help
      hg help <command>
      hg help <extension>
  
  Don't miss the 'additional topics' sections, as many of them are quite useful,
  like 'patterns' and 'revisions.'
  
  
  Mercurial Queues
  ================
  
  Mercurial Queues ('mq') is an advanced extension, packaged with the core Hg
  distribution, that provides a system for managing patch queues with the
  benefits of version control. It was inspired by Quilt and is similar to
  Stacked Git, if you're coming from the Other Side of the DVCS world.
  
  One of the most common uses for mq is flexible rebasing, allowing you to work
  on features in sets of 'floating' patches that can be continually refreshed
  and rebased atop mainline changes that occur while your work is ongoing. This
  also provides a means for 'rewriting history' to clean it up before pushing
  to permanent record on a shared repository. If you're accustomed to git's
  interactive rebasing, this is what you're looking for.
  
  To work with it, you must first enable it in your .hgrc:
  
      [extensions]
      hgext.mq =
  
  And you should probably also use git-style extended diffs:
  
      [diff]
      git = True
  
  `hg help` will now show a number of new commands beginning with 'q'.
  There are a number of other uses for mq and you're encouraged to check out
  the wiki for more on what you can do with it:
  
      http://mercurial.selenic.com/wiki/MqExtension
  
  
  Rewriting History
  -----------------
  
  By nature of Mercurial's Revlog format for storing history, it is not really
  practical to 'rewrite' it once changes have been pushed publicly. That being
  said, mq is here to help with work you haven't yet pushed upstream (and can
  help for sharing in-progress patch queues too!).
  
  Following is a rundown of using mq to change history (say you need to change
  a commit message or forgot to add a file needed for a build). First you
  rewind to the first revision that you need to change:
  
      hg qinit
      hg qimport -r BADREV:tip
      hg qpop -a
      hg qseries
  
  `qseries` shows the list of patches you're now managing, numbered by local
  revision. Your next step depends on what your goal is: if you just want to
  delete this one revision,
  
      hg qdelete BADREV.diff
  
  Otherwise, you can revise it:
  
      hg qpush BADREV.diff
      # Edit, add a file you forgot, revert one you didn't mean to add
      hg qrefresh
  
  Now you're ready to move on and finish:
  
      hg qpush -a
      hg qfinish -a
  
  If you need to edit multiple commits, use `qpush` without the `-a` (all)
  option to step through revisions one-at-a-time. If you introduce any
  conflicts along the way, you'll need to fix them and `qrefresh` before
  moving on. You can also squash multiple patches into one with `qfold`.
  
  At this point you have rewritten your revisions and can push them publicly
  if you're ready. See the hg wiki for more on history rewriting with mq:
  
      http://mercurial.selenic.com/wiki/EditingHistory
