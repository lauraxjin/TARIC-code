# TARIC-code
==========
The TARIC-code web service assists users ( primarily EU custom officials and international exporters who export goods to the EU)to identify a particular good's TARIC-code(HS international trade product code plus an additional 4 digit EU code) from the HS hierarchical rules.

Data is divided in the hierarchical structure specified in the HS handbook(21 Sections and 96 Chapters).

  - **all-rules.html** shows a list of all the rules in the handbook,listed by the hierarchical structure. It is at the upper most level of the website, and it will support GET, POST, HEAD, and OPTIONS as I speficied in the previous assignment.
  - **rule.html** shows a specific trade product's path from the upper most level of the rules in the HS handbook to identifying the product's TARIC-code. And this page support GET, POST(Authentification needed), and DELETE(Authentification needed).
  - **rule-form.html** represents a user's posting of a rule.
  - **find-rule.html** shows how the matching rule to the user's query is presented. This page supports GET.

## Attribute values: Id, Class, Name, and Rel

### Id attribute values: 
  This design relies on two unique identifiers for representation:
  
  *rules* : Applied to a div tag. The list of rules in this representation.
  
  *queries* : Applied to a div tag. The list of valid(correct format and parameter) queries in this representation (represented by the HTML anchor tag). 

### Class attribute values:
  *all* : Applied to a OL tag. A hiearchical list representation of all the sections and chapters. 
 
  *rule* :  A representation of a single rule. It should contain the following descendant elements: 
      
       SPAN.class="rule-text"
       A.rel="rule" 
  
  *rule-post* : Applied to a FORM tag. A link template to add a new rule to the system by the authorized user. The element will be set to FORM.method="post" and it should contain a descendant element:
       
       TEXTAREA.name="new-rule"
  
  *rule-search(get)* : Applied to a FORM tag. A link template to search of all the rules. The element will be set to FORM.method="get" and will contain the following descendant elements:
  
      INPUT[text].name="search"
      
  *rule-text* : Applied to a SPAN tag. The text of a rule posted by an authorized user.
  
  *search* : Applied to a OL tag. A list representation. When this element is a descendant of DIV.id="rules" it contains a list of rules and will have only one LI.class="message" descendant elements because all the rules will have the same link template.

### Name attribute values:
  *rule* : Applied to TEXTAREA element. The rule to post(for the authorized user).
  
  *search* : Applied to an INPUT[text]. The search(get) value to use when searching rules(when applied to FORM.class="rule-search").
### Rel attribute values:
  *rule* : Applied to an anchor tag. A reference to a rule representation.
 
  *rule-post* : Applied to an anchor tag. A reference to the rule-post FORM.
 
  *rule-all* : Applied to an anchor tag. A reference to a list representaiton fo all the rules in the system.
 
  *rule-search(get)* : Applied to an anchor tag. A reference to rule-search(get) FORM.
 

  
    
