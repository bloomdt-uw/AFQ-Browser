# Browser-based graphical user interface for AFQ

AFQ-Browser will run in any standard web browser and is designed
to visualize AFQ results.

See: [http://yeatmanlab.github.io/Sarica_2017]http://yeatmanlab.github.io/Sarica_2017 for a working example

## Installation

AFQ-Browser requires the [numpy](http://www.numpy.org/),
[scipy](http://scipy.org/scipylib/index.html) and
[pandas](http://pandas.pydata.org/) libraries. These are all included in the
[Anaconda Python distribution](https://docs.continuum.io/anaconda/)

AFQ-Browser and its dependencies can also be installed using pip:

    pip install AFQ-Browser

To install AFQ-Browser from source,
[download](https://github.com/yeatmanlab/AFQ-Browser/archive/master.zip) the
source code and run `python setup.py install` in the top-level folder after
extracting it.

## Running AFQ-Browser

After installing the software, you can run the program on mat files generated by
[AFQ](https://github.com/yeatmanlab/AFQ). For an example, download this
[mat file](https://github.com/yeatmanlab/AFQ-Browser/raw/master/afqbrowser/site/client/data/afq.mat), change your working directory to the location where the
file was downloaded to, or move the file to your current working directory
and run:

    afqbrowser-assemble afq.mat
    afqbrowser-run

Open a browser pointing to http://localhost:8080, to view the visualization of
these data and to interact with it. The variables in the metadata table are
created based on the variables that are stored in the [metadata field]
(https://github.com/yeatmanlab/AFQ/wiki#including-subject-metadata-in-the-afq-structure) of the afq.mat file.

## Publishing your website

There is a command line function that allows you to publish your website to
Github. If you don't already have one, start by [creating a Github account](https://github.com/join). Then run the following sequence:

    afqbrowser-assemble   # Run this if you haven't before
    afqbrowser-publish -t ./AFQ-Browser -r myresults

Where `./AFQ-Browser` is the folder that was created by `afqbrowser-assemble`,
and the URL of the website is: `https://username.github.io/myresults` (with
`username` replaced with your Github username, and `myresults` replaced with the
input to the `-r` flag).
