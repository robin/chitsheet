--- 
lotus_domino_url: |-
  Domino URL cheat sheet
  
  http://www-128.ibm.com/developerworks/lotus/library/ls-Domino_URL_cheat_sheet/
  
  Level: Advanced
  
  Tara Hall, Content Developer, Lotus
  
  01 Oct 2002
  
  This article, updated for Domino 6, explains the URLs Domino uses to access servers, databases, and other Web site pieces. Use these URL commands to design links or enter commands directly into a browser to navigate a site or reach components quickly. 
  	
  
  Editor's note: This article has been updated for Domino 6 with information that also appears in Domino Designer 6 Help. Many of these commands and arguments are supported by the latest maintenance release of Domino 5, except where indicated.
  
  Domino uses URLs to access servers, databases, and other components of a Web site. Knowing the URL commands lets you design links or enter commands directly into a browser to navigate a site or reach components quickly. You can use the URL commands to:
  
      * Open databases and views
      * Open framesets
      * Open forms, navigators, and agents
      * Open, edit, create, save, and delete documents
      * Open documents by key name from a view
      * Open pages
      * Open resources
      * Open attachments, image files, and OLE objects
      * Open Web preferences
      * Create search queries
      * Require authentication
      * Process SSL certificates
      * Specify a character encoding
  
  Quick review of URL syntax for Domino
  
  Domino URL commands have the following syntax:
  http://Host/Database/DominoObject?Action&Arguments
  
  Where:
  
      * Host is the DNS entry or IP address.
      * DominoObject is a Domino construct (such as a database, view, document, form, navigator, agent, and so on).
  
  URL commands for accessing DominoObjects use the following syntax:
  http://Host/Database/DominoObject?Action&Arguments
  
  Where:
  
      * Database is the database in which the DominoObject resides.
      * Action is the action you want on the specified DominoObject (for example, ?OpenDocument).
      * Arguments are the qualifiers for the action (for example, Count=10 combined with ?OpenView limits the number of rows displayed in a view to 10).
  
  For additional information on URL syntax, see the Syntax guidelines sidebar.
  
  Note: The URL examples in this article are not intended to point to actual Domino-based Web sites, unless specifically stated.
  
  Opening databases and views
  
  The following commands access databases, views, About and Using documents, and database icons.
  
  Redirect
  Syntax:
  http://Host/Database.nsf?Redirect&Name=Notesserver&Id=To=Encodedurl
  
  Where:
  
      * http: //Host refers to the Web server that is generating the URL.
      * Name= Notesserver specifies a Domino server name in its common or abbreviated form. This is optional when the "By Database" setting on the server is on.
      * Id= indicates the replica ID of the database to be located. This is an optional argument.
      * To= Encodedurl specifies the rest of the URL.
  
  Example:
  http://www.acme.com/database.nsf?Redirect&Name=Mail&Id=0525666D0060ABBF& To=%FAView%3FOpenView
  
  OpenDatabase
  
  Syntax:
  http://Host/DatabaseFileName?OpenDatabase http://Host/_DatabaseReplicaID?OpenDatabase
  
  Examples:
  http://www.acme.com/leads.nsf?OpenDatabase
  http://www.acme.com/sales/discussion.nsf?OpenDatabase
  http://www.acme.com/_852562F3007ABFD6?OpenDatabase
  
  OpenView
  
  Syntax:
  http://Host/Database/ViewName?OpenView
  http://Host/Database/ViewUniversalID?OpenView
  http://Host/Database/$defaultview?OpenView
  
  Examples:
  http://www.acme.com/leads.nsf/By+Salesperson?Open/View
  http://www.acme.com/leads.nsf/DDC087A8ACE170F8852562F300702264?OpenView
  http://www.acme.com/leads.nsf/$defaultview?OpenView
  
  Optional arguments for OpenView
  
  Append these optional arguments to refine the OpenView URL. Combine any of the following arguments for the desired result.
  
  Start= n
  
  Where n is the row number to start with when displaying the view. The row number in a hierarchical view can include sub indexes (for example, Start=3.5.1 means the view will start at the third main topic, subtopic 5, document 1).
  
  Count= n
  
  Where n is the number of rows to display.
  
  ExpandView displays the view in expanded format.
  
  CollapseView displays the view in collapsed format.
  
  Expand= n
  
  Where n is the row number to display in expanded format in a hierarchical view. Do not combine this argument with the ExpandView or CollapseView arguments.
  
  Collapse= n
  
  Where n is the row number to display in collapsed format in a hierarchical view. Do not combine this argument with the ExpandView or CollapseView arguments.
  
  RestrictToCategory= category
  
  Sets the category for "Show Single Category" object, where category is the category to be displayed in the view.
  
  StartKey= string
  
  Where string is a key to a document in the view. The view displays at that document.
  
  Examples:
  http://www.acme.com/leads.nsf/By+Category?OpenView&CollapseView
  http://www.acme.com/leads.nsf/By+Category?OpenView&ExpandndView
  http://www.acme.com/leads.nsf/By+Category?OpenView&RestrictToCategory=pricing
  http://www.acme.com/leads.nsf/By+Category?OpenView&Start=3&Count=15
  http://www.acme.com/leads.nsf/By+Category?OpenView&StartKey=F
  
  OpenAbout
  
  Use the $about?OpenAbout command to access the About This Database document.
  
  Syntax:
  http://Host/Database/$about?OpenAbout
  
  Example:
  http://www.acme.com/leads.nsf/$about?OpenAbout
  
  OpenHelp
  
  Use the $help?OpenHelp command to access the Using This Database document.
  
  Syntax:
  http://Host/Database/$help?OpenHelp
  
  Example:
  http://www.acme.com/leads.nsf/$help?Open/Help
  
  OpenIcon
  
  Use the $icon?OpenIcon command to access the database icon.
  
  Syntax:
  http://Host/Database/$icon?OpenIcon
  
  Example:
  http://www.acme.com/leads.nsf/$icon?OpenIcon
  
  ReadViewEntries
  
  Use this command to access view data in XML form without appearance attributes such as fonts, list separators, date formats, HTML settings, view templates and frame redirections.
  
  Syntax:
  http://Host/Database/ViewName?ReadViewEntries
  http://Host/Database/ViewUniversalID?ReadViewEntries
  http://Host/Database/$defaultview?ReadViewEntries
  
  Examples:
  http://www.acme.com/leads.nsf/By+Salesperson?ReadViewEntries
  http://www.acme.com/leads.nsf/DDC087A8ACE170F8852562F300702264?ReadViewEntries
  http://www.acme.com/leads.nsf/$defaultview?ReadViewEntries
  
  Optional arguments for ReadViewEntries
  
  Append optional arguments to refine the URL. Combine any of the following arguments for the desired result.
  Collapse= n
  
  Where n is the row number to display in collapsed format in a hierarchical view. Do not combine this argument with the ExpandView or CollapseView arguments. CollapseView displays the view in collapsed format
  Count= n
  
  Where n is the number of rows to display
  Expand= n
  
  Where n is the row number to display in expanded format in a hierarchical view. Do not combine this argument with the ExpandView or CollapseView arguments. ExpandView displays the view in expanded format
  KeyType= text or time
  
  Specifies the StartKey type of either text or time. If no argument is specified, the default is text. When you specify &KeyType=time, you can specify a time value, like ISO date time value, for both the &StartKey and &UntilKey arguments.
  
  PreFormat causes all data types to be converted to text on the server. Text lists, numbers, dates and lists of numbers are converted to text before being sent. The server's locale is used for all formatting. Without this argument, the XML output stream contains information in structured, locale-neutral formats.
  ResortAscending= column number
  ResortDescending= column number
  
  Where column number is a 0-based number of a column in a view that you want to resort either ascending or descending in alphanumeric order.
  RestrictToCategory= category
  
  Sets the category for the "Show Single Category" object, where category is the category to be displayed in the view
  Start= n
  
  Where n is the row number to start with when displaying the view. The row number in a hierarchical view can include sub indexes (for example, Start=3.5.1 means the view will start at the third main topic, sub-topic 5, document 1).
  StartKey= string
  
  Where string is a key to a document in the view. The view displays at that document.
  UntilKey= string
  
  Displays a range of view entries that begin with the document specified by the StartKey and end with the document specified by the UntilKey. The &UntilKey argument is only valid with the &StartKey argument. You can use the &Count argument to limit the number of entries returned by the range.
  
  Example:
  http://www.acme.com/leads.nsf/By+Category?ReadViewEntries&CollapseView
  http://www.acme.com/leads.nsf/By+Category?ReadViewEntries&ExpandView
  http://www.acme.com/leads.nsf/By+Category?ReadViewEntries&KeyType=time&StartKey=20020715&UntilKey=20020714
  http://www.acme.com/leads.nsf/By+Category?ReadViewEntries&KeyType=text&StartKey=Aa&UntilKey=Ab
  http://www.acme.com/leads.nsf/By+Category?ReadViewEntries&PreFormat
  http://www.acme.com/leads.nsf/By+Category?ReadViewEntries&ResortAscending=3
  http://www.acme.com/leads.nsf/By+Category?ReadViewEntries&ResortDescending=3
  http://www.acme.com/leads.nsf/By+Category?ReadViewEntries&RestrictToCategory=pricing
  http://www.acme.com/leads.nsf/By+Category?ReadViewEntries&Start=3&Count=15
  http://www.acme.com/leads.nsf/By+Category?ReadViewEntries&StartKey=F
  
  
  
  	Back to top
  
  
  Opening framesets
  
  This command opens framesets.
  
  OpenFrameset
  
  Syntax:
  http://Host/Database/FramesetName?OpenFrameset
  http://Host/Database/FramesetUNID?OpenFrameset
  
  Examples:
  http://www.acme.com/discussion.nsf/main?OpenFrameset
  http://www.acme.com/discussion.nsf/35AE8FBFA573336A852563D100741784?OpenFrameset
  
  
  
  	Back to top
  
  
  Opening forms, navigators, and agents
  
  The following commands open forms, navigators, and agents in a database.
  
  OpenForm
  
  Syntax:
  http://Host/Database/FormName?OpenForm
  http://Host/Database/FormUniversalID?OpenForm
  http://Host/Database/$defaultform?OpenForm
  
  Examples:
  http://www.acme.com/products.nsf/Product?Openform
  http://www.acme.com/products.nsf/625E6111C597A11B852563DD00724CC2?OpenForm
  http://www.acme.com/products.nsf/$defaultform?OpenForm
  
  Optional arguments for OpenForm
  ParentUNID = UniqueIDNumber
  
  Where UniqueIDNumber is the document ID of the parent document, which is used in response forms or when the form property "Formulas inherit values from selected document" is selected.
  
  Syntax:
  http://Host/Database/FormUniversalID?OpenForm&ParentUNID=UniqueIDNumber
  
  Example:
  http://www.acme.com/products.nsf/40aa91d55cle4c8285256363004dc9e0?OpenForm &ParentUNID=6bc72a92613fd6bf852563de001f1a25
  
  OpenNavigator
  Syntax:
  http://Host/Database/NavigatorName?OpenNavigator
  http://Host/Database/NavigatorUniversallID?OpenNavigator
  http://Host/Database/$defaultNav?OpenNavigator
  
  Examples:
  http://www.acme.com/products.nsf/Main+Navigator?OpenNavigator
  http://www.acme.com/products.nsf/7B5BC17C7DC9EB7E85256207005F8862?OpenNavigator
  http://www.acme.com/products.nsf/$defaultnav?OpenNavigator
  
  Note: $defaultnav opens the folders pane in a database
  
  OpenAgent
  Syntax:
  http://Host/Database/AgentName?OpenAgent
  
  Example:
  http://www.acme.com/sales/leads.nsf/Process+New+Leads?OpenAgent
  
  Note: Agents may only be referred to by name. The use of UNID is not supported when referring to an agent.
  
  ReadForm
  Use the ReadForm command to display a form without showing its editable fields. ReadForm is useful for displaying a form as a simple Web page.
  
  Syntax:
  http://Host/Database/FormName?ReadForm
  http://Host/Database/FormUniversalID?ReadForm
  http://Host/Database/$defaultform?ReadForm
  
  Examples:
  http://www.acme.com/home.nsf/Welcome?ReadForm
  http://www.acme.com/products.nsf/625E6111C597A11B852563DD00724CC2?ReadForm
  http://www.acme.com/products.nsf/$defaultform?ReadForm
  
  
  
  	Back to top
  
  
  Creating, opening, editing, saving, and deleting documents
  
  The following commands manipulate documents in a database. Hidden design elements are hidden from the server; you can't use Domino URL commands to access documents in hidden views.
  
  CreateDocument
  The CreateDocument command is used as the POST action of an HTML form. When the user submits a form, Domino obtains the data entered in the form and creates a document.
  
  Syntax:
  http://Host/Database/Form?CreateDocument
  http://Host/Database/FormID?CreateDocument
  
  Examples:
  http://www.acme.com/products.nsf/basketballs?CreateDocument
  http://www.acme.com/products.nsf/b9815a87b36a85d9852563df004a9533?CreateDocument
  
  OpenDocument
  Syntax:
  http://Host/Database/View/DocumentKey?OpenDocument
  http://Host/Database/View/DocumentUniversalID?OpenDocument
  http://Host/Database/View/$First?OpenDocument
  
  Note: DocumentKey is the contents of the first sorted column in the specified view.
  
  Examples:
  http://www.acme.com/products.nsf/By+Part+Number/PC156?OpenDocument
  http://www.acme.com/leads.nsf/By+Rep/35AE8FBFA573336A852563D100741784?OpenDocument
  http://www.acme.com/leads.nsf/$First?OpenDocument
  
  Optional arguments for OpenDocument
  See the Optional outline arguments sidebar for outline arguments that apply to both OpenDocument and OpenPage.
  
  EditDocument
  Syntax:
  http://Host/Database/View/Document/?EditDocument
  
  Example:
  http://www.acme.com/products.nsf/By+Part+Number/PC156?EditDocument
  
  Note: Rich text fields containing hidden text will be visible to Web users with editor access to documents.
  
  SaveDocument
  The SaveDocument command is used as the POST action of a document being edited. Domino updates the document with the new data entered in the form.
  
  Syntax:
  http://Host/Database/View/Document?SaveDocument
  
  Example:
  http://www.acme.com/products.nsf/a0cefa69d38ad9ed8525631b006582d0/4c95c7c6700160e2852563df0078cfeb?SaveDocument
  
  DeleteDocument
  Syntax:
  http://Host/Database/View/Document?DeleteDocument
  
  Example:
  http://www.acme.com/products.nsf/By+Part+Number/PC156?DeleteDocument
  
  
  
  	Back to top
  
  
  Opening documents by key
  
  The following commands allow you to open a document by key, or to generate a URL to link to a document by key.
  
  Using Domino URLs to access a document
  To open a document by key, create a sorted view with the sort on the first key column. Then you can use a URL to open the document:
  
  Syntax:
  http://Host/DatabaseName/View/DocumentName?OpenDocument
  
  Where View is the name of the view, and DocumentName is the string, or key, that appears in the first sorted or categorized column of the view. Use this syntax to open, edit, or delete documents, and to open attached files. Domino returns the first document in the view whose column key exactly matches the DocumentName.
  
  There may be more than one matching document; Domino always returns the first match. The key must match completely for Domino to return the document. However, the match is not case-sensitive or accent-sensitive.
  
  Note that View can be a view UNID or view name. In addition, the implicit form of any of these commands will work when appropriate. (EditDocument and DeleteDocument must be explicit commands.)
  
  Examples:
  http://www.acme.com/register.nsf/Registered+Users/Jay+Street?OpenDocument
  
  LDD Today uses a document key view called Lookup. For example, the URL for this article is:
  http://www.lotus.com/ldd/today.nsf/lookup/Domino_URL_cheat_sheet?OpenDocument
  
  To get a closer look at the Lookup view, you can download the LDD Today design template from the Sandbox here on LDD.
  
  Using Domino URLs to access attachments
  To access a file attachment using a Domino URL, you must know the view name, the document name, and the file attachment name. Domino generates an URL for file attachments when it saves the documents to which the files are attached. These URLs end with the file name of the attachment.
  
  Syntax:
  http://Host/DatabaseName/View/DocumentName/$File/fileattachmentname
  
  Where View is either the view name or the view ID, and DocumentName is the document name or ID. $File is a special identifier that indicates an attachment on a document. Fileattachmentname is the file name of the attachment.
  
  Examples:
  http://www.acme.com/products.nsf/Documents/$File/Spec_sheet.pdf
  
  	Back to top
  
  
  Opening pages
  
  The following command will open a page element using its name, UNID, or Note ID.
  
  OpenPage
  Syntax:
  http://Host/Database/PageName?OpenPage
  http://Host/Database/PageUNID?OpenPage
  
  Examples:
  http://www.acme.com/discussion.nsf/products?OpenPage
  http://www.acme.com/discussion.nsf/35AE8FBFA573336A852563D100741784?OpenPage
  
  Optional arguments for OpenPage
  See the Optional outline arguments sidebar for outline arguments that apply to both OpenDocument and OpenPage.
  
  Opening resources
  
  The following commands open image and file resources stored in an database.
  
  OpenImageResource
  Opens graphics stored as image resources in a database.
  
  Syntax:
  http://Host/Database/ImageResourceName?OpenImageResource
  
  Where ImageResourceName is the file name of the image resource that you want to open.
  
  Example:
  http://www.acme.com/discussion.nsf/banner.gif?OpenImageResource
  
  OpenFileResource
  Opens a file resource stored in a database.
  
  Syntax:
  http://Host/Database/FileResourceName?OpenFileResource
  
  Where FileResourceName is the name of the file that you want to open.
  
  Example:
  http://www.acme.com/discussion.nsf/index.js?OpenFileResource
  
  Opening attachments, image files, and OLE objects
  
  The ?OpenElement command opens attachments, image files, and OLE objects within a document.
  
  Using ?OpenElement with file attachments
  Syntax:
  http://Host/Database/View/Document/$File/Filename?OpenElement
  
  Example:
  http://www.acme.com/lproducts.nsf/By+Part+Number/SN156/$File/spec.txt?OpenElement
  
  Note that if more than one attached file has the same name, the URL includes both the "internal" file name as well as the external name. Since the internal file name is not easily determined, make sure all attached files have unique names.
  
  Domino treats all file attachment OpenElement commands as implicit commands, because some browsers require that the URL end with the attached file name. For example:
  http://Host/Database/View?Document/$File/FileName
  
  Using ?OpenElement with image files
  Syntax:
  http://Host/Database/View/Document/FieldName/FieldOffset?OpenElement&FieldElemFormat=ImageFormat
  
  FieldOffset is the field number and the byte offset into the field. ImageFormat is either GIF or JPG. If the FileElemFormat is not entered, Domino assumes the image file format is GIF.
  
  Example:
  http://www.acme.com/leads.nsf/bbe63a6b9d895dc6852567d600658601/fe5138bef254cf3a852569fc00724b69/Body/0.18AA?OpenElement&FieldElemFormat=jpg
  
  Using Open Element with OLE Objects
  Syntax:
  http://Host/Database/View/Document/FieldName/FieldOffset/$OLEOBJINFO/FieldOffset/obj.ods?OpenElement
  
  Note that the current URL syntax for referencing images and objects in Notes documents-specifically the FieldOffset-makes it impractical to create these URLs manually. As an alternative, you may paste the actual bitmap or object in place of the reference, create URL references to files stored in the file system, or attach the files to the documents.
  
  Opening user Web preferences
  
  The following command opens Web preferences, a Domino 6 feature that lets users set time zone and regional preferences. For more information about Web preferences, see the LDD Today article, "Making Web browsers look smarter with Domino 6."
  
  This URL command is not supported by Domino 5 servers.
  
  OpenPreferences
  Syntax:
  http://Host/$Preferences.nsf?OpenPreferences&Argument
  
  Where:
  
      * Host indicates a server or a domain
      * $Preferences.nsf is a virtual database that "resides" on the Domino 6 server
      * ?OpenPreferences displays the default frameset of the virtual database
      * &Argument is an optional argument that you can specify to open a page instead of the frameset
  
  The $Preferences.nsf database resides at the root of each server.
  
  Example:
  http://www.acme.com/$Preferences?OpenPreferences
  
  Optional argument for OpenPreferences
  You can append the following optional arguments to the ?OpenPreferences command to open a specfiied page rather than the Web preferences default frameset.
  PreferenceType= value
  
  Where value can be one of the following values described in the table:
  Value 	Description
  Menu	Displays the Menu page which provides links to the Time Zone and Regional preferences page.
  TimeZone	Displays the Time Zone preferences page.
  Regional	Displays the Regional preferences page.
  
  Examples:
  http://www.acme.com/$Preferences?OpenPreferences&PreferenceType=Menu
  http://www.acme.com/$Preferences?OpenPreferences&PreferenceType=TimeZone
  http://www.acme.com/$Preferences?OpenPreferences&PreferenceType=Regional
  
  Creating search queries
  
  Search-related URLs are available for performing view, multiple-database, and domain searches. Typically you define a URL that displays an input form-either a customized search form or the default search form-to let users define their own searches, but you may also define a URL that performs text searches without user input. Both input and results forms may be customized.
  
  SearchDomain
  Use SearchDomain URLs for text searches across a domain. The search input form is opened with the OpenForm command by name or universal ID. For search results, the results template is specified as part of the URL. If no template is found, then the default template form, $$SearchDomainTemplate, is substituted. If $$SearchDomainTemplate is not found, an error will be returned. If no results are returned, the value of the $$ViewBody field remains the same.
  
  Syntax:
  http://Host/Database/TemplateForm?SearchDomain&ArgumentList
  
  Where:
  
      * TemplateForm is an optional argument that calls the search results form.
      * ArgumentList is a list of optional arguments.
  
  Example:
  http://www.acme.com/domainsearch.nsf/SearchForm?SearchDomain
  
  SearchSite
  Use SearchSite URLs for text searches in multiple databases. Because the URL requires the name of a search site database, be sure to create one before using a SearchSite URL.
  
  Syntax:
  http://Host/Database/$SearchForm?SearchSite&ArgumentList
  
  Where $SearchForm and ArgumentList are optional arguments.
  
  Example:
  http://www.acme.com/searchsite.nsf/$SearchForm?SearchSite
  
  SearchView
  Use SearchView URLs to limit a search to documents displayed in one database view. This URL is useful for views that display all documents (so you can have a full-database search) or for views in which you can predict what users need to see, such as all documents whose status is "Completed."
  
  Syntax:
  http://Host/Database/View/$SearchForm?SearchView&ArgumentList
  
  Where $SearchForm and ArgumentList are optional arguments. The special identifier $SearchForm indicates that Domino will present a search view form for search input. If this identifier is provided, the ArgumentList is ignored. If this identifier is absent, a default form will be generated on the fly based on the contents of the search.htm file located on the server. The default form generated by the server does not support paged results.
  
  Example:
  http://www.acme.com/products.nsf/By+Product+Number/$SearchForm?SearchView
  
  Optional arguments for SearchSite, SearchView, and SearchDomain
  
  $SearchForm
  $SearchForm is a special identifier indicating a custom search form that Domino displays. When this argument is specified, Domino ignores all arguments that follow it. If this argument is not specified, Domino displays a default search form based on the search.htm file on the server.
  Query= string
  
  Where string is the search string.
  Count= n
  
  Where n is the number of results to display on each page until the SearchMax has been reached. For example Count=10 will display 10 results per page.
  Scope=[0,1,2]
  
  Where 1=Notes databases only, 2=file system only, 0=both. The default value is 0. This argument should only be used with the SearchDomain command.
  SearchEntry= formName
  
  Where formName is the name of the form to use for the results of a domain search. The default argument is "ResultEntry," which supports all of the pre-defined results fields specified in the ArgumentList. This argument is valid for SearchDomain only and should not be used for SearchSite or SearchView.
  SearchFuzzy=[TRUE,FALSE]
  
  Indicate TRUE for fuzzy search. The default is FALSE.
  SearchOrder=[1,2,3,4]
  
  Indicate 1 to "Sort by relevance", 2 to "Sort by date ascending", 3 to "Sort by date descending." The default is 1. SearchView also supports a SearchOrder value of 4 to "Keep current order", which sorts the resulting set of documents in the order in which they appear in the view.
  SearchMax= n
  
  Where n is the maximum number of entries returned. The default value is determined by the server.
  SearchWV=[TRUE, FALSE]
  
  Where TRUE = include word variants in the search. The default value is FALSE.
  Start= n
  
  Where n is the number corresponding to the document that appears first in your list of results. For example, Start=10 begins your list of results with the 10th document found in the search. Start=0 means that paged results will not be returned.
  
  You can use the Start and Count arguments with the SearchView or SearchSite URLs as well as with the search results page to display search results page-by-page. The Start argument specifies which result appears first in the search results list. The Count argument determines the number of results displayed on the screen. For instance, if you specify Start=1 and Count=10, the search results begin with the first result and displays the next ten results on the screen. If results extend beyond ten, you can use button or hotpsots to navigate the search results pages.
  
  For more information about creating buttons or hotspots for the Start and Count arguments, see the Domino Designer 6 Help.
  
  Examples:
  http://www.acme.com/welcome.nsf/?SearchSite&Query=product+info+requests&SearchOrder=2 &SearchMax=30&SearchWV=TRUE&SearchEntry="myResultsForm"
  
  http://www.acme.com/products.nsf/By+Product+Number/?SearchView&Query=PC156&SearchOrder=3&SearchMax=1&SearchFuzzy=TRUE&SearchWV=FALSE
  
  Requiring authentication
  
  Append the following command to any Domino URL to force user authentication regardless of the database access control list. This ensures that anonymous Web users who weren't initially prompted for a name and password when they entered the site are required to supply a name and password to complete tasks that require user identity.
  
  Login
  Syntax:
  http://Host/Directory/Database?OpenDatabase&Login
  
  Examples:
  http://www.acme.com/sales/leads.nsf?OpenDatabase&Login
  
  Process SSL certificates
  
  The following commands automate the request and receipt of Secure Sockets Layer (SSL) certificates stored in a database.
  
  OpenForm with SpecialAction argument
  Syntax:
  http://Host/Database/FormName?OpenForm&SpecialAction=specialActionField
  
  Where specialActionField is the name of an editable text field on the form whose value contains a predefined command. To use the field with SSL certificates, use one of the following certificate request commands:
  
      * "SubmitCert"
      * "ServerRequest"
      * "ServerPickup"
  
  Examples:
  http://www.acme.com/certs.nsf/UserCertificateRequest?OpenForm&SpecialAction=SubmitCert
  http://www.acme.com/certs.nsf/ServerCertificateRequest?OpenForm&SpecialAction=ServerRequest
  http://www.acme.com/certs.nsf/Certificate?OpenForm&SpecialAction=ServerPickup
  
  SubmitCert
  The SubmitCert command creates a User Certificate document in the specified database, using the form specified in the TranslateForm argument.
  
  Syntax:
  http://Host/Database/ResultForm?RequestCert&Command=SubmitCert&TranslateForm=TranslationFormName
  
  Where:
  
      * ResultForm is a form in the specified database that displays information about the processed request.
      * TranslationFormName represents a form in the database that contains fields to hold certificate information.
  
  Example:
  http://www.acme.com/certs.nsf/CertificateProcessed?RequestCert&Command=SubmitCert&TranslateForm=Certificate&TranslateForm=Certificate
  
  Optional and required fields
  The SubmitCert command requires a translation form with a field named Certificate. Domino saves information about the certificate subject and issuer in the document if the form contains fields with these names:
  
      * CommonName
      * Org
      * OrgUnit
      * Locality
      * State
      * Country
      * IssuerCommonName
      * IssuerOrg
      * IssuerOrgUnit
      * IssuerLocality
      * IssuerState
      * IssuerCountry
  
  ServerRequest
  The ServerRequest command creates a Server Certificate Request document in the specified database, using the form specified in the TranslateForm argument.
  
  Syntax:
  http://Host/Database/MessageForm?RequestCert&Command=ServerRequest&TranslateForm=TranslationFormName
  
  Where ResultForm is a form in the specified database that displays information about the processed request in the user's browser after a successful submission. TranslationFormName represents a form in the database that contains fields to hold certificate information.
  
  Example:
  http://www.acme.com/certs.nsf/CertificateProcessed?RequestCert&Command=ServerRequest&TranslateForm=Certificate&TranslateForm=Certificate
  
  Optional and required fields
  The ServerRequest command requires a translation form with a field named Certificate. Domino saves information about the server request in the document if the form contains fields with these names:
  
      * CommonName
      * Org
      * OrgUnit
      * Locality
      * State
      * Country
  
  Specify a character encoding
  
  To specify a character encoding for a design element, append the charset= MIME charset argument to the end of any URL command. You can use this argument with any design element or Notes object, including agents, folders, views, databases, and so on. This argument returns a form or page in the specified language or character set overriding the Web browser's preferred language setting as well as the $$HTMLContentLang field of a form. To use the charset=MIME charset argument, you must include it in your application. The Domino server does not generate this argument automatically.
  
  Syntax:
  http://Host/Form?OpenForm&charset= MIME charset
  
  Where Form is either the form name or ID to open and MIME charset indicates the character encoding applied to the form.
  
  Domino recognizes a limited number of character set names. If Domino does not recognize a specified character set, it defaults to the character set specified in the Server document.
  
  Example:
  http://www.acme.com/products.nsf/Product?Openform&charset=ISO-2022-JP
  
  The previous example opens the Product form with a Japanese character encoding.
  
  
  Resources
  
      * Syntax Guidelines sidebar
  
      * Optional outline arguments sidebar
  
      * An alternative to the OpenServer URL command
  
      * Making Web browsers look smarter with Domino 6
  
  
  
  About the author
  
  		
  
  Tara joined the Lotus Developer Domain as a Content Developer for LDD Today in April 2002. Prior to joining us, she was a senior user assistance writer for the Notes User Assistance Group. She documented a number of products for the web applications, streaming media, and other development teams. She also worked on the Documentation Library and occasionally freelanced for Iris Today. Tara holds a B.A. and an M.A. in English.
