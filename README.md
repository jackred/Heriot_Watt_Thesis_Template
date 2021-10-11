# Heriot_Watt_Thesis_Template
A template for LaTeX. Should be following the guidelines for the submission of a thesis at Heriot-Watt University.  

## Copyright/Licensing
This template is licensed under the MIT License. You can use it, modify it, distribute it, as long as the License and Copyright notice are included. You don't need to provide the copyright notice in the pdf version of your thesis. However if you provide or make public the latex version, please include it. The License limitations includes liability and warranty.  

MIT is softer than the lppl or whatever other License you can find, hence my use of it.

## Disclaimer
Any word missing or other type of error should be attributed to my lack of attention and my absence of motivation about reading everything twice.  

## Implementation
I tried to follow the guideline as much as possible, here is what I made:
- A4 sized, with 40mm left margin and 20mm other margin, with 2 spaces between sentences and 1.5 spacing between lines, with justified text.
- 12pt font, similar to Times New Roman (LaTeX don't have the exact one)
- Page Numbering 10mm above the edge, Roman numerals (possible to remove) for the preliminaries
- Titlepage with everything asked for
- Abstract/Dedication/Acknowledgements page
- Pdf inclusion code to add the Declaration form right in the Thesis
- Table of Content, List of Tables, Figures, Glossary (for acronym), List of Publications by the Candidate (using the bibliography system)
- One chapter per files, that you can compile alone to avoid long compilation on the whole Thesis
- Heading: chapter 14pt, section 12pt, subsection 12pt italicised, all bold. Chapter and section have capitalised initial in the heading (not in the toc). It can be changed in the config files as it can be annoying if you have word that should be all uppercase.
- Chapter numbering, note numbering
- Headers with chapter title (or leftmark if you change it), 10pt italicsm no bold, Footers with only page number
- Table/Figures/Equations command for referencing, propoer numbering
- Appendices letter numbering
- Published paper as pdf in appendix, referenced in toc
- List of reference and Bibliography (or further reading) using biblatex

## Modifications

There is probably some modifications to the Template itself you want to make. I'll try to list a few I thought of.

### Contributing 
If you think the one you did are worth mentionning, you can submit a Pull Request to this repository with your modifications. In the even I don't have time to maintain this repository in the future, feel free to fork it and contact me about it, I'll update the README to inform people to look at your fork instead.

### Comment
You will find some comment in the Template. It is often there to change some part. The most notable one are:
- the Table Of Content/List Of Figures/etc one, which allow you to remove the pagination from those specific pages (it is very annoying to do)
- Some part of the title page I don't think are necessary

It also works the other way, part such as the List of Figures, List of Publications, Bibliography, etc are optional and can be commented.  

### Heading
I followed the guidelines regarding the heading size, which makes them way smaller than the default LaTeX style and also less noticeable. This can be changed in the `I-config.tex` files. Line 57-59 define the constant defining the size of the headder. The baseline is automatically computed. The style itself can be changed in the next part, starting line 69.

### Glossary
I used the acronym version for the glossary, and I am not using the `\gls` command. You can have more details here: [Overleaf help](https://www.overleaf.com/learn/latex/Glossaries). This is bit annoying to work with, as without the `noidx` command, you need first to create a normal glossary, then comment it and create your acronym gloassary. The package is creating some cached files, and apparently need it this way. The way it is written in the template works however, but if you want more functionality from the package, you will have to implement them yourself.

### Bibliography
I put 3 bibliographies:
- The list of publications (yours) if you have one
- The list of references, the work you cite
- The bliography or further reading, for any works you used but don't cite

Only the references use a numbered column. The two other are sorted alphabetically. Your work should be put in the `BibMine.bib` file. It will be listed in the References and Further reading (depending if you cite it). If you want to change that, you will have to modify the `refsection` and/or create some new one. Everything was done with biblatex.

### Section/Chapter heading / Thesis title
I added some auto capitalising because I thought it was nice, but it can be pretty annoying oif you want to write full uppercase word. Most of the time, the command `\capitalisewords` need to be removed or `\MakeLowerCase` and `\makefirstuc` (both).

## How to use

### Overleaf
A template is available on Overleaf [here](https://www.overleaf.com/latex/templates/heriot-watt-thesis-template/whcchqtmfxgf)

### Github
You can download the lastest version (normally the same as on Overleaf) on [github](https://github.com/jackred/Heriot_Watt_Thesis_Template) clicking on `code` then `Download ZIP`. You can also clone or fork the repository directly to create your thesis repository.
