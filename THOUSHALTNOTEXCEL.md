THOU SHALT NOT EXCEL
Marta Bartnicka, triggered by Agenor Hofmann-Delbor


Image from www.kindpng.com
Why it is usually a bad idea to copy localization resources or xml/html fragments to Excel?

1) Because CAT tools like them as they are. The most of
industry-standard CAT tools can handle the most of industry-standard
content that you might use for UI resources, web pages or documentation.
Moreover, if you use any kind of $variables, CAT can protect them from
translation – Excel cannot.


CAT can!

Excel cannot
2) Because translators need as much context as possible to translate the
resources properly. In a JSON or YAML file, a lot of useful information
is hidden as comments, key IDs, or can be derived from the sequence of
strings in file (e.g. when button labels are grouped together). Moving
strings to Excel is a good (baad!) chance to strip the translatable
content out of all that context.


CAT with context preview

Excel with no context
3) Because copy/paste to Excel tempts you to take another two steps: sort
the strings alphabetically and remove duplicates. Short advice: don’t.
Long advice: don’t, because this leads to further stripping the strings
off their natural context (see above). Also, removing duplicates erases
the good redundancy which would allow different translation of the same
word in different contexts.


Once upon a time, this file had three fields called „Name”: one for document name, one for person’s name and one for the action of naming a document…

…but bad people decided that one „Name” should be enough. Which meaning? Oh well.
4) Because migration to another format, CSV or XSL(X) in this case, is
always a good opportunity for an error to occur: incomplete export or
import, code page issues, mixing up Polish with Portuguese or Chinese
Simplified with Traditional – let’s not go through it.


CAT maintains language pair in a translated file

In Excel, things can go bad much easier
OK. So what should you do to get the resources translated?

First, try to export them from your CMS / programming tool „as they are”. Send a sample export to an experienced Translator or LSP and ask them if the format is CAT-friendly. It probably is!
In the not so frequent case it’s not, check the possibilities of other export formats available from your tool: JSON, PO, XLIFF?
Consider Excel (or CSV) as exchange format with Translators only if none of the above works. In that situation you still can do it pro:
Include keys and comments along with translatable text (as separate columns and rows of course);
Do not sort – keep the content structure as it is;
Do not exclude duplicates – if you need same string n times in your resources, Translators need it too!
Check that Excel has not scattered your strings into multiple rows or converted currency to date, etc.
