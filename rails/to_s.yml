--- 
rails_to_s: |-
  >> 3.days.ago.to_s(:db)
  
  Formats:
    :db
      "%Y-%m-%d %H:%M:%S" (ie: "2006-12-04 19:00:26")
    :long
      "%B %d, %Y %H:%M" (ie: "December 04, 2006 19:00")
    :rfc822
      "%a, %d %b %Y %H:%M:%S %z" (ie: "Mon, 04 Dec 2006 19:00:26 -0700")
    :short
      "%d %b %H:%M" (ie: "04 Dec 19:00")
    :time
      "%H:%M" (ie: "19:00")
  
  Add your own:
    Time::DATE_FORMATS[:mine] = '%Y%m%d%M%S'
     >> Time.new.to_s(:mine)
     => "200612040026"
