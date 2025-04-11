---
title: "LaTeX Workshop for Research Students at IoBM"
author: "Dr. M. Ali Faisal"
format: html
editor: visual
---

This workshop is designed for early career researchers that are starting to explore the dynamics of academic writing. This is usually a two session workshop that covers the introduction to a LaTeX structure, how to write a scientific paper using LaTeX, and writing thesis using LaTeX.

You can follow along during the lesson and if we don't manage to get through everything today you can finish off at home. Happy Typesetting!

Key Workshop Objectives

Understand the basic structure of a Latex document

Learn how to write a scientific paper using LaTeX

Understand the typical Latex workflow

Learn how a thesis can be written in LaTeX

To get you to a point where you feel confident using and experimenting with LaTeX on your own!

Why use Latex? What's wrong with Word?

Prevalence in academic literature

Working with large documents

Creating professional looking documents!

Equations can be created easily in the math mode

Tables, graphs and figures using TikZ, PGF-Plots vector graphics

Can even automatically populate graphs and figures using your existing research data (e.g. with csv files)

Working with non-Latin scripts (Arabic, Sanskrit etc.)

Not just used for academic literature

Books, CVs, presentations, posters

Check out the gallery here for all sorts of examples

…And most importantly, impress your peers who think you have to be some crazy tech-wizard to actually want to write your documents in Latex.

Typical Workflow

Do your writing in a LaTeX .tex file + Bibliography .bib file (optional) → Run the files through a LaTeX distribution (sometimes called a compiler) → LaTeX outputs a PDF

This is a different way of working to wysiwyg editors like Microsoft Word. Some people claim this allows you to focus more on your content, instead of its appearance. On the other hand your writing now has LaTeX specific commands intermingled with it.

LaTeX Editors

These are what you actually do your writing in. Because LaTeX is written in plain text, if you wanted to (and plenty of people do) you could use a simple text editor like Notepad to do your writing, and then run the LaTeX distribution (the software that takes all your Latex files and outputs a PDF) yourself.

However, this is unnecessarily complicated and newer LaTeX editors provide lots of nice features like spell checking, code highlighting, and autocompletion.

You must have a LaTeX distribution installed on your computer to be able to build your Latex files. MikTeX and TeX Live are by far the most popular. On most Linux distributions and Mac OS, LaTeX comes pre-installed. Once you've got a distribution, go ahead and download the editor of your choosing.

For this workshop you don't need to install anything!

My personal recommendations for desktop Latex editors:

TeXstudio

TeXmaker

Texworks

However a more recent development in the LaTeX world is web based LaTeX editors. This is what we will be using today.

Overleaf

<a href="http://overleaf.com" title="Overleaf" target="_blank">Overleaf</a> is a modern web based LaTeX editor that allows you to work on Latex documents anywhere in the world without needing to install any software, all you need is your browser (and an active Internet connection).

Because it is a web based tool, it also has some other helpful features that you typically don't get from desktop-based editors, the most useful of which are:

Live recompiling: Your changes are automatically reflected in the PDF preview as you're working on them

Collaboration: Overleaf allows you to share your Latex projects with other users. This is especially useful for working with co-authors and/or sharing your papers with your supervisors as you're working on them

Overleaf has a free plan. However, for full features they charge a monthly fee. Half price plans are available for students. In my opinion, the only major limiting feature to the free plan is that it only allows you to share your document with a single collaborator. Provided this isn't a deal breaker, the free plan still provides heaps of features and allows you to create unlimited private projects.

Basic LaTeX

Every LaTeX document is comprised of a mixture of Latex commands and your actual content. Almost all Latex commands follow the exact same structure:

\command[optional arguments]{arguments}

Note the backslash (\) that precedes commands. This is what lets Latex know that everything following the backslash (up until the next space) should be interpreted as being a Latex command, rather than just ordinary content.

Almost all Latex commands take arguments. This is the information that you 'pass' to the command to tell it what to do. For example:

This text would appear formatted normally, but \textbf{this text would appear bold}.

The above command would appear in your PDF as:

This text would appear formatted normally, but <b>this text would appear bold</b>.

In the example above, the command \textbf{} tells Latex to bold anything that appears between the two curly-braces {}.

Latex Document Structure

Every Latex document follows the same structure:

Preamble Commands
 - This is where you do things like specify:
    - The document type: e.g. whether it's a book or a journal article, and one or two columns
    - The document title and author(s)
    - List any packages you want to use (more on this later)
----
Document Content
- This is where you actually put the content of your document, and is generally divided into different chapters and/or sections, or in Latex terms 'environments'

In actual Latex, this is what it looks like:

\documentclass[twocolumn]{article}
\title{My first LaTeX document}
\author{Ali Faisal}

\begin{document}
\maketitle
This is the actual body of the document, this text would appear in the PDF.
\end{document}

That above code is a complete and valid Latex document. That is all you need! Latex will take care of sorting out all the default margins for you. It even generates a nice title, author, and date section for you based on the information you provided in the document preamble (i.e. the stuff that came before the begin{document} command).

If you were to paste the above code into Overleaf, you would see the following output PDF:

 The text only goes halfway across the page because we specified that this was a twocolumn document in the Latex command:

\documentclass[twocolumn]{article}

This is an example of an optional argument, why is why it appears in []. You could have instead simply written:

\documentclass{article}

and your document would have defaulted to a single column article.


\documentclass{article}
\title{My first Latex document}
\author{Author 1
\and
Author 2
\and
Author 3
}
\date{}

\begin{document}
\maketitle
This is the actual body of the document, this text would appear in the PDF.
\end{document}

Latex Environments

Some commands have both opening and closing commands. These are generally referred to as environments, and you have already seen an example above.

\begin{document}
\end{document}

All content within the opening and closing command will have some sort of styling applied to them. For example, the environment below centers text:

\begin{center}
This text would be center-aligned!
\end{center}

You can nest environments within one another, however they must \begin{} and \end{} in the correct order. For example, the Latex code below would generate an error:

\begin{document}
\begin{center}
This text would be center-aligned!
\end{document}
\end{center}

Sections, Abstracts, and Chapters

\documentclass[twocolumn]{article}
\title{My first LaTeX document}
\author{Ali Faisal}

\begin{document}
\maketitle

\begin{abstract}
    In this article Ali tries his best to teach some Latex. Hopefully you find it useful.
\end{abstract}

\section{Introduction}
This is the actual body of the document, this text would appear in the PDF.

\section{Background}
Ali used Latex in his own PhD, and he thinks it's pretty cool.

\subsection{Research Questions}
This research hopes to answer two primary research questions:

\begin{enumerate}
    \item Is Latex as cool as Ali thinks it is?
    \item Is it worth the effort?
\end{enumerate}

\end{document}

Usually we don't write our articles as one big block of content, instead we divide it into different chapters, sections, and subsections. Although it seems logical to use environments for sectioning, we don't do this because when you're potentially dealing with sections, subsections, and even subsubsections you can end up with chaotic looking code like this:

\begin{document}
\begin{section}{Section One}
...
\begin{subsection}{Subsection One}
...
\begin{subsubsection}{Subsubsection One}
...
\end{subsubsection}
\end{subsection}
\end{section}
\end{document}

Instead Latex has dedicated commands such as \section{} and \chapter{} to indicate the beginning of a new section, and these have no \end{} tag. For example:

\begin{document}
\section{Introduction}
This appears in the introduction section.
\subsection{Research Questions}
This text would appear in a subsection named '1.1 Research Questions'.
\end{document}

::: note <b>Exception: Abstracts</b>. The abstract section is an exception to the rule, because some Latex class files (which are basically just a list of commands that act as a style template for your documents, more on this soon) apply special formatting to the abstract section.

Writing an article using Overleaf

Create a new blank project on Overleaf and name it 'My First LaTeX Article'

Create five sections (in first four sections, create two subsections) in your document.

Create the bibliography file

There are many advanced and complex bibliography management systems. We will stick to a simple one.

On the left column, create a new file and call it my_bibliography.bib.

Populate the bibliography

The bibliography file is populated with the references to the articles, books, papers, and other resources, that you want to cite.

The file is a collection of entries that look like this:

@article{label_name,
    author = "Author name",
    title = "Article title",
    journal = "Journal where article was published",
    year = 2023,
    volume = "73",
    number = "2",
    pages = "103--110"
}

The @article says it is an article item (it could be a @book, etc). The label_name is a label name that you will use to cite the work from your document. The things that follow are pairs that contain more information about the item you want to cite. You can read more about the BibTeX format here.

Many article and book repositories have functionality to automatically generate the BibTeX entry for a given article, report, book, etc.

For example, I went to Google Scholar and searched for "house". Then, I clicked the button "Cite" and then "BibTeX". It generated this for me:

@article{hauser1988house,
  title={The house of quality},
  author={Hauser, John R and Clausing, Don and others},
  year={1988},
  publisher={Harvard Business Review Vol. 66, May-June 1988}
}

Put that in your my_bibliography.bib file.

Inserting the bibliography

To insert the bibliography in your document, use the command \bibliography and use as argument the name of your file (without the .bib extension).

Like so:

% ...

\subsection{Problem Statement}

The dining room is where people have their meals together.

\bibliography{my_bibliography}  % Insert the bibliography here.

% The body ends here.
\end{document}

Recompile your document, and behold! Nothing happens! That is because the bibliography will only show the items that you \textbf{actively} cited in your document.

Citing an item with \cite

To cite an item from your bibliography, just use the command \cite with the citation key as the argument. The citation key is the label name of that bibliographic item, and it should be the first thing inside the curly braces {} in your item.

For example, in

@article{hauser1988house,
  title={The house of quality},
  author={Hauser, John R and Clausing, Don and others},
  year={1988},
  publisher={Harvard Business Review Vol. 66, May-June 1988}
}

the citation key is hauser1988house.

To cite this work in the document, write \cite{hauser1988house}. For example, like so:

% ...
\subsection{Problem Statement}

% Add a citation to the bibliography.
We base our work on the contributions of \cite{hauser1988house}.
% ...

Recompile, and behold! Still, nothing happens!

Setting the style of the bibliography

To display a bibliography, you also have to set its style. There are many styles available, but we will go with the plain one for this article:

% ...

\bibliographystyle{plain}  % Set the style of the bibliography.
\bibliography{my_bibliography}  % Insert the bibliography here.

% The body ends here.
\end{document}

Now, the bibliography should show its only item.

Learn more about managing a bibliography here

Creating LaTeX tables

You can create tables using multiple methods such as manual typesetting, an online service like this one, or through your compiler's in-built option (TeXShop and Overleaf).

\begin{table}[h]
    \centering
    \begin{tabular}{ccccc}
        \toprule
        Column 1 & Column 2 & Column 3 & Column 4 & Column 5 \\
        \midrule
        Row 1    & Data     & Data     & Data     & Data     \\
        Row 2    & Data     & Data     & Data     & Data     \\
        Row 3    & Data     & Data     & Data     & Data     \\
        Row 4    & Data     & Data     & Data     & Data     \\
        Row 5    & Data     & Data     & Data     & Data     \\
        Row 6    & Data     & Data     & Data     & Data     \\
        \bottomrule
    \end{tabular}
    \caption{My Table}
    \label{tab:1}
\end{table}

Awesome tables with booktabs

Once you are comfortable with creating a couple of tables I suggest that you look up the package booktabs. With very little effort you can create professional-looking tables. In particular, I am a big fan of this quick guide

Inserting images into your document

Uploading the image

The first thing you need to do if you want to insert an image into your LaTeX document is to tell Overleaf about it. This means you need to upload the image into Overleaf.

On the left, Overleaf has an "Upload" button that you can use. You can upload Fig1 provided in the material to upload.

The next thing you need is to use the package that is appropriate for images: graphicx.

\documentclass{article}
\usepackage{graphicx}  % Allows inserting images into the PDF.

Next, go to where you want to add your image and create the environment figure.

\begin{figure}  % <- start the environment to add a figure.

\end{figure}

There is a command, called includegraphics, that is responsible for inserting the image into the document. We can use that command inside the environment figure.

\begin{figure}[h]
    \includegraphics[scale=0.1]{fig1.jpg}
    \caption{My Figure}
    \label{fig:1}
\end{figure}

Equations

One area where LaTeX clearly surpasses WYSIWYG editors is its ability to display equations. Up until recently, the only way to write equations in LaTeX was though manual typesetting.

To create a full equation that is displayed in the centre of the text, use the environment equation:

\begin{equation}
    \frac{dy}{dx} = \lim_{\Delta x \to 0} \frac{f(x + \Delta x) - f(x)}{\Delta x} 
    \label{eq:1}
\end{equation}

However, now Overleaf can generate the same equation through a one line command.

Adding automatic links to references with hyperref

To add automatic links to your document, you can use the package hyperref. To "use a package" means going into the header of your document and using the command \usepackage to load the package.

Just by loading the package hyperref, your references become clickable.

\documentclass{article}
\usepackage{hyperref}  % This makes references clickable!

The links will be surrounded by a red box. This is customisable, but you can also easily turn it off with:

\documentclass{article}
\usepackage[hidelinks]{hyperref}

To reference a table, figure, or an equation you can use the following:

This is my reference to Table \ref{tab:1}, Figure \ref{fig:1}, and Equation \eqref{eq:1}

We'll take a look at working with larger documents now instead of articles. Go ahead and create a new blank project named 'thesis' and delete the automatically generated contents.

Organizing Bigger Documents

Let's create a basic outline for our new thesis project and build on it from here.

Code:

\documentclass{report}
\title{My Latex Thesis}
\author{Your Name}

\begin{document}
\maketitle

\chapter{Introduction}
Welcome to my professional looking Latex thesis.

\chapter{Background}
Look, Latex puts this on a new page for me!

\end{document}

One of the nice things about working with Latex is that you can easily split your content into different files (for example a different file for each chapter), and then have a single 'main' thesis file which combines all these files and outputs a single PDF. This makes life a lot easier when you start dealing with big documents like theses.

Let's do that now. Create a new folder in your Latex project named chapters, and within the folder create 2 new files, introduction.tex and background.tex. Next we'll take the content corresponding to each of the chapters from our existing main.tex file, and place it in the appropriate file. For example, the file background.tex should now look like this:

\chapter{Background}
Look, Latex puts this on a new page for me!

The \input{} Command

In order to tell our main.tex file to grab the content from our new files, we simply use the \input{} command, and pass it the path to our new files. This path is relative to the location of the file that the command is in. For example, if we had a file named methodology.tex within the same folder as our main.tex file we would use the command \input{"methodology"}.

However, because we're nice and tidy Latex users, we put our chapters into the separate chapters folder, so we instead use the command input{"chapters/introduction"} and input{"chapters/background"}.

The double quotes " are optional in this case, but are recommended because otherwise Latex doesn't play nice if you have spaces in your file names.

You don't need to duplicate all of the preamble in your chapter files. The \input{} command takes all of the content from individual files and uses it to create one big .tex file. So from Latex's point of view nothing has changed even though our commands are now split over 3 files.

Our main.tex file should now look like this:

Code:

\documentclass{report}
\title{My Latex Thesis}
\author{My Name}

\begin{document}
\maketitle

\input{"chapters/introduction"}
\input{"chapters/background"}

\end{document}

Table of Contents and Figure List

Although it doesn't make much sense for a document of this size, most thesis include both a Table of Contents and a List of Figures.

Setting all this up in Latex is so simple that I'm not even going to explain the commands!

Update our main.tex file with 2 new commands:

Code:

...
\begin{document}
\maketitle
\tableofcontents % <- Creates a table of contents
\listoffigures % <- Creates a list of figures
...

Easy peasy! These lists will continue to update automatically as we add to our document.

Next Steps

Feel free to explore the recently added in-built functions in overleaf to generate tables, titles, abstracts, equations, etc.

Use templates of publishers to write your articles.

That's it, Well done!

Hopefully you've seen the light, and realize the potential power of LaTeX once you get the hang of it.

If not… Well, I tried.
