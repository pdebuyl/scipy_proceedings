:author: Pierre de Buyl
:email: pdebuyl@ulb.ac.be
:institution: Université libre de Bruxelles

-------------------------------------------------------------
Re-Re-Submitting a contribution to EuroSciPy 2013 proceedings
-------------------------------------------------------------

.. class:: abstract

   EuroSciPy 2013 has decided to steal (shamelessly, by the way) the
   proceedings system of SciPy 2013. This paper reviews the process.

   In a desperate attempt to be participant-friendly, this is written
   as the author is using the system for the first time.

   This paper is a duplicate of a previous paper by the same author.

.. class:: keywords

   scipy, proceedings

Introduction
------------

Handling conference proceedings consists in many steps. We consider
here the technical part of submitting, reviewing and publishing
conference proceedings.

It is indeed mandatory that such a document contains mathematics. A
common assumption is that

.. math::

   N_{papers} \leq N_{contributions}

where :math:`N_{papers}` is the number of papers in the proceedings
and :math:`N_{contributions}` is the number of contributions (talks
and posters) at the conference.

We may test the assumption, if needed, in Python:

.. code-block:: python

   def assumption_number(n_papers, n_contrib):
       """Test the numbers."""

       return n_papers <= n_contrib

Filling
-------

An short (few paragraphs) paper compiles fines but then all floating
elements (figures and tables) collapse at the top and this leads to
very ugly papers.

To fill the void, here are the steps to create your own paper. The
instructions refer to the SciPy version and will change.

.. code-block:: sh

   # fork the scipy/scipy_proceedings on github
   git clone git@github.com:mygithublogin/scipy_proceedings
   cd scipy_proceedings
   git checkout 2013
   cd papers
   mkdir name
   cp 00_vanderwalt/00_vanderwalt.rst name/name.rst
   cd name
   vi name.rst
   cd ../..
   ./make_paper.sh papers/name
   git add papers/name
   git commit -m "Adding contribution by name."
   git push -u origin 2013

Indeed, replace name and so on with your own data.


Some perspective
----------------

The EuroSciPy conference has a logo.

.. figure:: euroscipy_logo.png
   :scale: 80%

   The EuroSciPy logo. :label:`logo`

And there is a lot to know about the conference.

.. table:: Conference statistics. :label:`mtable`

   +------------+-------------------------+
   | Year       | Number of participants  |
   +------------+-------------------------+
   | 2011       | 200                     |
   +------------+-------------------------+
   | 2012       | 400                     |
   +------------+-------------------------+
   | 2013       | 1000?                   |
   +------------+-------------------------+


