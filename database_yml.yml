--- 
database_yml: |-
  DRY out your database.yml
  From: http://blog.bleything.net/articles/2006/06/27/dry-out-your-database-yml
  Updated with a more universal database naming scheme, which better accomodates multiple instances of the same application.
  
  -----
  
  login: &login
    adapter: mysql
    username: username
    password: password
    # host: mysql.example.com
    encoding: utf8
    port: 3306
  
  development:
    <<: *login
    database: app_domain_com_d
  
  test:
    <<: *login
    database: app_domain_com_t
  
  production:
    <<: *login
    database: app_domain_com_p
