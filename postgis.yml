--- 
postgis: |-
  PostGIS
  ----
  
  Installation
  ----
  
    $ su - postgres
    $ psql
  
    # create database template_postgis with template = template1;
    # UPDATE pg_database SET datistemplate = TRUE where datname = 'template_postgis';
  
    # \c template_postgis
    # CREATE LANGUAGE plpgsql;
    # \i /path/to/share/postgis/lwpostgis.sql;
    # \i /path/to/share/postgis/spatial_ref_sys.sql;
    # GRANT ALL ON geometry_columns TO PUBLIC;
    # GRANT ALL ON spatial_ref_sys TO PUBLIC;
  
    # VACUUM FREEZE;
  
  Create a table
  ----
  
    $ createdb -O <owner> -T template_postgis <new_table_name>
