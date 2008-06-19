--- 
regex_lib: |-
  Leerzeichen zwischen String und Zuweisung entfernen
  ---------------------------------------------------
    Pattern: /"(\s*)=/
    Replacement: " =
  
  
  YAML to Ruby-Hash
  -----------------
    Pattern: /^(\s+)(\w+):\s+(.*)\s*$/
    Replacement: $1:$2 => $3,
  
  
  MySQL SELECT * Ergebnis in INSERTS
  ----------------------------------
    Pattern: /^\s*\|\s+\d+\s+\|\s+([\d\w\s\/\,\(\)\-\.\*]+\w)\s+\|\s+(\d+).*$/
    Replacement: INSERT INTO lookups (original_type, text, original_id) VALUES('Bodytype', '$1', $2);
  
  
  MySQL SHOW TABLES Ergebnis in DROP TABLES umwandeln
  ---------------------------------------------------
    Pattern: ^\s*\|\s+(\w+).*$
    Replacement: DROP TABLE $1;
