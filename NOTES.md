#Notes techniques

##Tentative Description for creating elements:

  In each list Element goes a div. This Div is the Interface Element which can be dragged to the canvas.
  Each element has the class "newMockElement". This is changed to "mockElement" when it is added to the cavas.
  Also each element can have other classes.

  In the Div there can be other nested elements.

  One of these elements *can* hold text that can be edited.  This is done by adding the attribute "data-editablearea" to this element.

  The way the text is edited can be customized, by adding the attribute `data-editable-mode=` to it. The attribute can have the following values: "markdown", "uielements", "plain". If you set nothing, markdown is assumed.

*  markdown: Is markdown with a table extension and the possibility to create radiobuttons via `(x)` and checkboxes via `[x]`
*  uielements: for creating lists where the items are seperated by a `;`. List items can highlighted (item-highlighted class is added to the <li> element) by adding a `*` in front: "normal; normal; *I am Active; normal item again; …"
*  plain: plain text

###DO:
  
  * give your element an additional (aside the newMockupElement) class: "newMockupElement fooBarClass".

* Use ">" (direct child) instead of the " " (descendant operator); If elements are nested it can have strange side effects since the nested element will have styles that it did not have before.

###DONT:
  
  * give the element an id. The id is set by the script.