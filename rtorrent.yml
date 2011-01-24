--- 
rtorrent: |-
  Adding and removing torrents
    backspace
      Add torrent using an URL or file path. Use tab to view directory content and do auto-complete.
      Also, wildcards can be used. For example: ~/torrent/*
    return
      Same as backspace, except the torrent remains inactive. (Use ^s to activate)
    ^O
      Set new download directory for selected torrent. Only works if torrent has not yet been activated.
    ^s
      Start download. Runs hash first unless already done.
    ^d
      Stop an active download, or remove a stopped download.
    ^r
      Initiate hash check of torrent. Without starting to download/upload.
  
  Throttling
    a/s/d
      Increase the upload throttle by 1/5/50 KB.
    z/x/c
      Decrease the upload throttle by 1/5/50 KB.
    A/S/D
      Increase the download throttle by 1/5/50 KB.
    Z/X/C
      Decrease the download throttle by 1/5/50 KB.
  
  Navigating
    Main View Keys
      right -- Switch to Download View.
      ^r    -- Initiate hash check of torrent.
      +/-   -- Change priority of torrent.
      l     -- View log. Exit by pressing the space-bar.
      1     -- Show all downloads
      2     -- Show all downloads, ordered by name
      3     -- Show started downloads
      4     -- Show stopped downloads
      5     -- Show complete downloads
      6     -- Show incomplete downloads
      7     -- Show hashing downloads
      8     -- Show seeding downloads
  
    Download View Keys
      right -- Switch to selected view
      left  -- Switch to view selection or back to main view
      1/2   -- Adjust max uploads.
      3/4   -- Adjust min peers.
      5/6   -- Adjust max peers.
      p     -- Display peer list
      o     -- Display torrent info
      i     -- Display file list
      u     -- Display tracker list
      t/T   -- Initiate tracker request.
               Use capital T to force the request, ignoring the "min interval" set by the tracker.
  
    Peer list View Keys
      left  -- Switch to view selection
      right -- Show file details
      space -- Change the file priority; applies recursively when done on a directory
      *     -- Change the priority of all files
      /     -- Collapse directories. While collapsed, press right to expand the selected directory.
  
    Tracker list View Keys
      left  -- Switch to view selection
      *     -- Enable/disable tracker
      space -- Rotate trackers in a group
