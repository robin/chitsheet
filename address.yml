--- 
address: |-
  Here's a simple ERB snippet to output an address if you don't know which components of the address will be provided.
  
  <%= record.address + content_tag(:br) if record.address %>
  <%= record.address2 + content_tag(:br) if record.address2 %>
  <%= record.city.to_s + (record.state || record.zip ? ',' : '') %>
  <%= "#{record.state} #{record.zip}" %>
  <%= content_tag(:br) + record.country if record.country %>
