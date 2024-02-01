Introduction to the Help Feature
================================

💻  Pop-up a correct code to help you finish the write-code problem
---------------------------------------------------------------------

:Help:
    You may see a problem that allows you to pop-up completed corret code for this write-code problem. 
    
    To see the completed code for this write-code problem, click the **"Help"** button below the problem description.

:Close Help:
    By clicking the **"Close Help"** button, you can close the provided help.
    
:Check Help Again:
    By clicking the **"View Help Again"** button, you can open to see the generated help again.

:🔁 Regenerate Help:
    By using the **🔁 Regenerate Help** button, you can generate different correct code for this write-code problem. 
    You need to CHANGE your code to activate this Feature.

:Copy Answer to Clipboard:
    You can use the **Copy Answer to Clipboard** button to copy the generated correct code to the clipboard and paste it in the write-code box.

🤗 Feel free to use it to help you solve the write-code practice problems!



.. activecode::  str-mixed-example-oc
    :autograde: unittest
    :nocodelens:
    :openaicode:

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
    # You can click the "Help" button above to see what the "Completed Code Help" provides.
    
    def phrase(person, thing):
        if type(person) = str or type(thing) = str:
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

    <p>Click on the following link to finish the skill assessment : <b><a id="pps-practice_OC"> <font size="+1">Practice Problem</font></a></b></p>

.. raw:: html

    <script type="text/javascript" >

      window.onload = function() {

        a = document.getElementById("pps-practice_OC")
        a.href = "pps-OC.html"
      };

    </script>