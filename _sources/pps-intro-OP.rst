Introduction to the Help Feature
================================

💻 Pop-up a mixed-up code problem to help you finish the write-code problem
----------------------------------------------------------------------------

:Help:
    Click the **"Help"** button below the problem description to pop up **a mixed-up code problem** for this write-code problem. 

:Close Help:
    By clicking the **"Close Help"** button, you can close the provided help.
    
:Check Help Again:
    By clicking the **"View Help Again"** button, you can open to see the generated help again.

:🔁 Regenerate Help:
    By using the **🔁 Regenerate Help** button, you can generate different correct code for this write-code problem. 
    
    You need to CHANGE your code to activate this Feature.

:Copy Answer to Clipboard:
    You can use the **Copy Answer to Clipboard** button to copy the generated correct code to the clipboard and paste it in the write-code box.

:Mixed-up Code Problem - Movable Blocks:
    Move the correct blocks from the left box to the right box and put them into the correct order.

:Mixed-up Code Problem - Static Blocks: 
    The Static blocks are the blocks that are already in position in the right box. You can not move them.

:Mixed-up Code Problem - Paired Block Sets: 
    - Sets of correct blocks with incorrect blocks that are unnecessary in a correct solution.
    - These incorrect blocks may contain syntactic or semantic errors.
    - Purple edges are used to pair the correct block and the incorrect block. 
    - The correct code is randomly shown above or below the incorrect block.


🤗 Feel free to use it to help you solve the write-code practice problems!


.. activecode::  str-mixed-example-op
    :autograde: unittest
    :nocodelens:

    Finish a function, ``phrase(person, thing)``:
        - It has ``person`` and ``thing`` as input.
        - First verify whether ``person`` and ``thing`` are strings. If not, return ``False``.
        - If ``person`` and ``thing`` are two strings, return one string with the characters in ``person``, followed by an empty space, and then followed by ``thing``
        - Make sure the first letter in ``person`` is capitalized and all the characters in ``thing`` are lowercase.

        
        .. table::
            :name: phrase_table_op
            :align: left
            :width: 50


            +-------------------------------------+---------------------------------------+
            | Example Input                       | Expected Output                       |
            +=====================================+=======================================+
            |``phrase("Sam", "Likes to code")``   | ``"Sam likes to code"``               |
            +-------------------------------------+---------------------------------------+
            |``phrase("ANN", "Likes to CODE")``   | ``"Ann likes to code"``               |
            +-------------------------------------+---------------------------------------+
            |``phrase(1, "Python")``              | ``False``                             |
            +-------------------------------------+---------------------------------------+


    ~~~~
    # Here is a student's buggy code
    # You can click the "Help" button above to see what the "Mixed-up Code Help" provides.
    
    def phrase(person, thing):
        if type(person) = str or type(thing) == str:
            person = person.capitalize()
            thing = thing.lowercase
            return person + thing
        else: 
            return ""


    ====
    from unittest.gui import TestCaseGui

    class myTests(TestCaseGui):
        def testOne(self):
            self.assertEqual(phrase("sam", "Likes to code"), "Sam likes to code", 'phrase("sam", " Likes to code")')
            self.assertEqual(phrase("mary-anne", "likes to sing"), "Mary-anne likes to sing", 'phrase("mary-anne", " likes to sing")')
            self.assertEqual(phrase("ANNA", "likes to dance"), "Anna likes to dance", 'phrase("ANNA", " likes to dance")')
            self.assertEqual(phrase(1111, "likes programming"), False, 'phrase(1111, " likes programming")')



    myTests().main()



What to do next
^^^^^^^^^^^^^^^

.. raw:: html

    <p>Click on the following link to finish the skill assessment : <b><a id="pps-practice_OP"> <font size="+1">Practice Problem</font></a></b></p>

.. raw:: html

    <script type="text/javascript" >

      window.onload = function() {

        a = document.getElementById("pps-practice_OP")
        a.href = "pps-OP.html"
      };

    </script>