.. _page01:

Part 01 Title
########################################################################

Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vivamus suscipit scelerisque sodales. Integer tempus malesuada orci, at vulputate magna iaculis sit amet. Nulla vel mauris sollicitudin elit placerat condimentum et eu eros.

This file covers the following topics.

.. contents::


Chapter 2
************************************************************************

Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec malesuada ultricies sapien quis egestas. Aliquam fringilla a tortor at semper.

If you work with edX documentation source files, you might find this file
helpful as a reference. This file contains examples of .rst formatting.

Explanations and more context for each type of element are provided in index

Section to cross-reference
========================================================================

This is the text of the section.

It refers to the section itself, see :ref:`page01`


.. _heading_anchor:

Heading levels
========================================================================

::

 Heading 1
 ########################################################################

 Heading 2
 ************************************************************************

 Heading 3
 ========================================================================

 Heading 4
 ------------------------------------------------------------------------


Paragraph Text and Commented Text
------------------------------------------------------------------------

This is an example of regular text in paragraph form. There are no
indents. As a best practice, break lines at about 80 characters, so that
each line has its own line number for commenting in reviews.

.. warning:: Throughout text and code examples, make sure double quotation
   marks and apostrophes are straight (") or ('), not curly quotatation marks
   and apostrophes, which might be introduced when text is cut and pasted from
   other sources or editors.

Sample text: **bold** or *italics*.

Monospace text is used for ``code examples``. Text surrounded by double grave
accent characters is rendered in monospace font.

``.. comments can be added in a file by starting a line with 2 periods and a space.``

In English source files, look for comments addressed to translators from writers.

``.. Translators:  In this code example, do not translate such and such.``


Ordered and Unordered Lists
========================================================================

Use hash symbols for ordered lists.

::

#. Select **Advanced Settings**.
#. Find the **Course Advertised Start Date** policy key.
#. Enter the value you want to display.


#. Select **Advanced Settings**.
#. Find the **Course Advertised Start Date** policy key.
    #. Enter the value you want to display.

.. note::
 Ordered lists usually use numerals. Nested ordered lists (ordered lists inside
 other ordered lists) use letters.

Use asterisks for unordered (bulleted) lists.

::

* Who is teaching the course?

* Who is teaching the course?
* What university or college is the course affiliated with?
* What topics and concepts are covered in your course?
* Why should a learner enroll in your course?


Nested Lists or Content
########################################################################

You can include content including additional lists and code examples inside
lists.

Lists
************************************************************************

To include an unordered list inside an ordered list, indent the unordered list
three spaces. The first bullet in the unordered list must be flush with the
text in the ordered list.

#. Do this
    * detail 01
    * detail 02
#. Finish like this

.. image:: /static/img/Lists_UL_inside_UL.png
 :width: 500
 :alt: An ordered (numbered) list inside an unordered (bulleted) list.


Code, Images, and Other Content inside Lists
************************************************************************

To include content such as code or an image inside a list, position the code or
image directive flush with the text in the list. That is, indent three spaces
for ordered lists and two spaces for unordered lists.


  #. In the ``lms.env.json`` and ``cms.env.json`` files, set the value of
     ``CERTIFICATES_HTML_VIEW`` within the ``FEATURES`` object  to ``true``.

     .. code-block:: bash

       "FEATURES": {
           ...
           'CERTIFICATES_HTML_VIEW': true,
           ...
       }

  #. Save the ``lms.env.json`` and ``cms.env.json`` files.


Notes and Warnings
************************************************************************

.. note::
   This is note text. If note text runs over a line, make sure the lines wrap
   and are indented to the same level as the note tag. If formatting is
   incorrect, part of the note might not render in the HTML output.

   Notes can have more than one paragraph. Successive paragraphs must indent
   to the same level as the rest of the note.

.. warning::
   Warnings are formatted in the same way as notes. In the same way, lines must
   be broken and indented under the warning tag.


Cross-References
************************************************************************

Create references

Self reference :ref:`page01`
Reference to another file :ref:`page2_label` or :ref:`page3`


Cross-References to Locations in the Same Document
========================================================================

Cross-references to locations in the same document use anchors that are located
above the heading for each topic or section. Anchors can contain numbers,
letters, spaces, underscores, and hyphens, but cannot include punctuation.
Anchors use the following syntax.

Reference using anchor
:ref:`heading_anchor`


Image References
************************************************************************

Image references look like this.

::

  .. image:: /Images/Course_Outline_LMS.png
     :width: 100
     :alt: A screen capture showing the elements of the course outline in the LMS.


Image links can include optional specifications such as height, width, or
scale. Alternative text for screen readers is required for each image. Provide
text that is useful to someone who might not be able to see the image.


.. _Examples of Tables:

Tables
************************************************************************

Each example in this section shows the raw formatting for the table followed
by the table as it would render (if you are viewing this file as part of the
Style Guide).


Example of a table with an empty cell
========================================================================

The empty cell is the second column in the first row of this table.

.. list-table::
   :widths: 25 25 50

   * - Annotation Problem
     -
     - Annotation problems ask students to respond to questions about a
       specific block of text. The question appears above the text when the
       student hovers the mouse over the highlighted text so that students can
       think about the question as they read.
   * - Example Poll
     - Conditional Module
     -  You can create a conditional module to control versions of content that
        groups of students see. For example, students who answer "Yes" to a
        poll question then see a different block of text from the students who
        answer "No" to that question.
   * - Exampel JavaScript Problem
     - Custom JavaScript
     - Custom JavaScript display and grading problems (also called *custom
       JavaScript problems* or *JS input problems*) allow you to create a
       custom problem or tool that uses JavaScript and then add the problem or
       tool directly into Studio.


Example of a table with a header row
========================================================================

.. list-table::
   :widths: 15 15 70
   :header-rows: 1

   * - First Name
     - Last Name
     - Residence
   * - Elizabeth
     - Bennett
     - Longbourne
   * - Fitzwilliam
     - Darcy
     - Pemberley


Example of a table with a boldface first column
========================================================================

.. list-table::
   :widths: 15 15 70
   :stub-columns: 1

   * - First Name
     - Elizabeth
     - Fitzwilliam
   * - Last Name
     - Bennett
     - Darcy
   * - Residence
     - Longboure
     - Pemberley


Example of a table with a cell that includes an unordered list
========================================================================

The blank lines before and after the unordered list are critical for the list
to render correctly.

.. list-table::
   :widths: 15 15 60
   :header-rows: 1

   * - Field
     - Type
     - Details
   * - ``correct_map``
     - dict
     - For each problem ID value listed by ``answers``, provides:

       * ``correctness``: string; 'correct', 'incorrect'
       * ``hint``: string; Gives optional hint. Nulls allowed.
       * ``hintmode``: string; None, 'on_request', 'always'. Nulls allowed.
       * ``msg``: string; Gives extra message response.
       * ``npoints``: integer; Points awarded for this ``answer_id``. Nulls allowed.
       * ``queuestate``: dict; None when not queued, else ``{key:'', time:''}``
         where ``key`` is a secret string dump of a DateTime object in the form
         '%Y%m%d%H%M%S'. Nulls allowed.

   * - ``grade``
     - integer
     - Current grade value.
   * - ``max_grade``
     - integer
     - Maximum possible grade value.


Code Formatting
************************************************************************

Inline code
========================================================================

you can simply use ``monospace font``



Code blocks
========================================================================


To set text in a code block, end the previous paragaph with 2 colons, leave
one line before the intended code block, and make sure the code block is
indented beyond the first colon.

For example, this is the introductory paragraph

::

    <p>and this is the code block following.</p>


Using code-block directive with specific language

.. code-block:: xml

        <problem>
            <annotationresponse>
                <annotationinput>
                <text>PLACEHOLDER: Text of annotation</text>
                    <comment>PLACEHOLDER: Text of question</comment>
                    <comment_prompt>PLACEHOLDER: Type your response below:</comment_prompt>
                    <tag_prompt>PLACEHOLDER: In your response to this question, which tag below
                    do you choose?</tag_prompt>
                <options>
                    <option choice="incorrect">PLACEHOLDER: Incorrect answer (to make this
                    option a correct or partially correct answer, change choice="incorrect"
                    to choice="correct" or choice="partially-correct")</option>
                    <option choice="correct">PLACEHOLDER: Correct answer (to make this option
                    an incorrect or partially correct answer, change choice="correct" to
                    choice="incorrect" or choice="partially-correct")</option>
                    <option choice="partially-correct">PLACEHOLDER: Partially correct answer
                    (to make this option a correct or partially correct answer,
                    change choice="partially-correct" to choice="correct" or choice="incorrect")
                    </option>
                </options>
                </annotationinput>
            </annotationresponse>
            <solution>
            <p>PLACEHOLDER: Detailed explanation of solution</p>
            </solution>
        </problem>
