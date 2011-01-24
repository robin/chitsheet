--- 
xslt: |-
  Functions
  ---------
  
  Node Set Functions
  ------------------
  number last()
  
  number position()
  
  number count(node-set)
  
  node-set id(object)
  
  string local-name(node-set?)
  
  string namespace-uri(node-set?)
  
  string name(node-set?)
  
  String Functions
  ----------------
  
  
  # haystack = the string/nodeset/etc that the function is applied to
  # needle = something to be applied to the haystack (find, substring etc)
  
  string string(object?)
  
  string concat(string, string, string*)
  
  boolean starts-with(haystack, needle)
  
  boolean contains(haystack, needle)
  
  string substring-before(haystack, needle)
  
  string substring-after(haystack, needle)
  
  string substring(haystack, index, length?)
  
  number string-length(string?)
  
  string normalize-space(string?)
  
  string translate(haystack, from, to) # note: only chars, not words
  
  
  Boolean Functions
  -----------------
  
  boolean boolean(object)
  
  boolean not(object)
  
  boolean true()
  
  boolean false()
  
  boolean lang(string)
  
  
  Number Functions
  ----------------
  
  number number(object?)
  
  number sum(node-set)
  
  number floor(number)
  
  number ceiling(number)
  
  number round(number) # <0.5 -> 0 ;; >= 0.5 -> 1.0
  
  
  --------
  Elements
  --------
  
  xsl:apply-imports
  
  xsl:apply-templates select="nodeset" mode="qname"
  
  xsl:attribute name="qname" namespace="uri" # must be directly after element
  
  xsl:attribute-set name="qname" use-attribute-sets="qnames"
  
  xsl:call-template name="qname"
  
  xsl:choose
  
  xsl:comment
  
  xsl:copy use-attribute-sets="qnames"
  
  xsl:copy-of select="expression"
  
  xsl:decimal-format name="qname" decimal-separator="char" grouping-separator="char" infinity="string" minus-sign="char" NaN="string" percent="char" per-mille="char" zero-digit="char" digit="char" pattern-separator="char"
  
  xsl:document href="uri"
  
  xsl:element name="qname" namspace="uri" use-attribute-sets="qnames"
  
  xsl:fallback
  
  xsl:for-each select="nodeset"
  
  xsl:if test="boolean"
  
  xsl:include href="uri"
  
  xsl:import href="uri"
  
  xsl:key name="qname" match="pattern" use="expression"
  
  xsl:message terminate="yes|no"
  
  xsl:namespace-alias result-prefix="prefix|#default" stylesheet-prefix="prefix|#default"
  
  xsl:number level="single|multiple|any" count="pattern" from="pattern" value="number-expression" format="string" lang="nmtoken" letter-value="alphabetical|traditional" grouping-separator="char" grouping-size="number"
  
  xsl:otherwise
  
  xsl:output method="xml|html|text|qname" version="string" encoding="string" omit-xml-declaration="yes|no" doctype-public="string" doctype-system="string" standalone="yes|no" indent="yes|no" cdata-section-elements="qnames" media-type="string"
  
  xsl:param name="qname" [select="expression"]
  
  xsl:processing-instruction name="qname"
  
  xsl:preserve-space elements="tokens"
  
  xsl:sort select="string" lang="string" data-type="text|number|qname" order="ascending|descending" case-order="upper-first|lower-first"
  
  xsl:strip-space elements="tokens"
  
  xsl:stylesheet version="1.0" id="id" extension-element-prefixes="tokens" exclude-result-prefixes="tokens" xmlns:xsl="http://www.w3.org/1999/XSL/Transform
  
  xsl:template match="pattern" name="qname" priority="number" mode="qname"
  
  xsl:text disable-output-escaping="yes|no"
  
  xsl:value-of select="expression" disable-output-escaping="yes|no"
  
  xsl:variable name="qname" select="expression"
  
  xsl:when test="boolean"
  
  xsl:with-param name="qname" select="expression"
  
  
  
  
  
  ----
  
  Axis
  
  ----
  
  ancestor:: 
  ancestor-or-self:: 
  attribute:: (@)
  child:: 
  descendant:: 
  descendant-or-self:: (//)
  following::
  following-sibling::
  namespace::
  parent:: (..)
  preceding::
  preceding-sibling::
  self:: (.)
