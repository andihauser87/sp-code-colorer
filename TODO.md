#Three areas
1.	Input area for the code (plain-text)
2.	Preview with colored code
3.	HTML view
How to display this areas?
- One below another (mobile friendly?)
- One "under" another, allowing to switch between views by usung tabs, for example

#Limits?
- Source code size in bytes/characters?
- Final code size?
- JS-library limits?
- SharePoint limits? (e.g. WikiContent field)

#How to open the add-in?
- From the Ribbon while editing page
? From the add-in home page (dedicated link to open dialog)

#User actions
- Insert source code (Ctrl+V, paste)
- Preview
- Copy to clipboard: rich-text
- Copy to clipboard: HTML
- Paste into the page (if possible, e.g. if the dialog was opened while editing the page's content)
- Cancel/Close

#Two ways to grab the code
- Copy from Preview as rich-text that can be pasted with OOB WYSIWYG functionality
- Copy as HTML code to paste into page's source code (advanced scenario?)

Do we need to prepare the source code somehow? For example, smart quotes, autoindent, etc. Maybe JS-library can do it already.

Frameworks & libraries: jQuery, Office UI Fabric, React, ClipboardJS, HighlightJS

! Localization

Do we need to wrap HTML-version of generated code with <code> tag?

#Add-in configuration page
- Do we need it at all? Do we have any options to configure out of main window of the add-in?
- Who can configure the add-in? Website admins?
- How to implement: dedicated page.
  BTW, Default.aspx is quite a good option: we can show help/how-to on the page for all users, adding "Configure" link for admins only.
  Of course Admin.aspx should also check if user has web administrator rights on the site.

How to update DataURL links for the icons? Gulp? On demand / automatically

#Dialog box
- Keyboard shortcut to open Code Colorer?
- How to close a dialog box by pressing Esc?
- Use CloseCustomActionDialogNoRefresh (https://dev.office.com/sharepoint/docs/sp-add-ins/sharepoint-add-ins-ux-design-guidelines)

? Use Webpack to bundle JS-file with only needed parts of UIFabric, React, etc.