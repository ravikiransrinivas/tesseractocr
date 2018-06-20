Text Extraction using OCR(Optical Character Recognition) from PDF

Motivation
----------

-   OCR is a machine-learning technique used to transform images that contain text (e.g. a scan of a document) into actual text content and helps us to edit data extracted from an uneditable source.

Tech/framework used
-------------------

-   Python 3.5.2
-   tesseract 3.04.01
-   leptonica-1.73
-   ImageMagick

Features
--------

-   This project was created to identify text in a pdf and allows us to copy the pdf’s data where selectable text is not allowed in the pdf.
-   If the text is embedded then it will automatically extract the text without the need of an OCR reader.

Installation
------------

sudo apt-get install tesseract-ocr to install TESSERACT

sudo apt-get install imagemagick (to install IMAGEMAGICK)

How to use?
-----------

In the terminal, go to the directory where you saved extract\_text.sh. For example:

-   -   cd /Users/me/myscripts
-   Make the script executable with the following command:

    -   chmod +x extract\_text.sh
-   Put all of your PDFs in a single directory.
-   Assuming that you put all of your PDFs in /Users/me/mypdfs, and you want to write text output to the directory /Users/me/myplaintext,

     =&gt; change the SUBPROCESS function variables in the python wrapper as follows:

    -   ./extract\_text.sh /Users/me/mypdfs/ /Users/me/myplaintext/
-   If you are working with German-language texts, you can add a language code at the end. For example:

    -   ./extract\_text.sh /Users/me/mypdfs/ /Users/me/myplaintext/ deu

NOTE: For convinience the bash shell script is wrapped under a python script so it is enough if permission is given and run through a python compiler.

Test Cases:
-----------

The project works well under certain conditions and fails in certain conditions.

The detailed test cases can be found in another documentation. As an overview the test cases in which the script the works the best is when there is embedded text in the the pdf. The code directly extracts that information and is processed for further usage.

I most real world conditions a pdf would often include scanned non-embedded images such as scanned images in many formats. This is pretty accurately identified by the script and quite accurately the data is retrievable.

The test cases in which the code is usually fails is the one where the data is embedded in an image. In this case the output usually tries to predict it but would usually give only partial outputs especially if the image is not clear.

\[explained in detail in test cases documentation\]
