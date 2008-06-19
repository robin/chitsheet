--- 
selenium: |-
  Verify number of rows in a table:
    Use the SEL:storeassertXpath extension to count columns
      assertXpath | count(//table[@id='mytable']/tr) | 10
    Or assert count & count+1
      assertElementPresent | //table[@id='mytable']/tr[10] | |
      assertElementNotPresent | //table[@id='mytable']/tr[11] | |
