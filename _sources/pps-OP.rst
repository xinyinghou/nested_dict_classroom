Practice Problems
=================

* This exercise includes four write-code problems with help that provided a **mixed-up code problem**.

* The Help can be triggered by clicking the **"Help"** button under each problem description.

* Please answer these problems without any outside help, including AI tools like ChatGPT.

* You can stop working on a problem after you worked on it for about five minutes without solving it.



.. activecode:: table_reservation_ac
        :autograde: unittest
        :nocodelens:

        Finish the function ``table_reservation(reservation_dict, guest_num)`` below:
            - It takes a nested dictionary ``reservation_dict`` representing a restaurant's current reservation situation for a day and a specific number of guests ``guest_num`` as input. 
            - ``reservation_dict`` is a nested dictionary with outer keys as time slots in a day (e.g., breakfast, lunch, dinner), and values as a list of dictionaries where the inner keys are unique researvation IDs and the values are the number of guests for that reservation. 
            - Your goal is to count and return the number of reservations in ``reservation_dict`` with the same guest number as the input ``guest_num``.
        
        .. table::
            :name: nested_merge_course_table
            :align: left
            :width: 50

            +----------------------------------------------------------------------------------------------------------------------------------------------------------------------+------------------+
            | Example Input                                                                                                                                                        | Expected Output  |
            +======================================================================================================================================================================+==================+
            |``table_reservation({"breakfast": [{"G01": 3}, {"G02": 4}], "lunch": [{"G03": 2}, {"G04": 4}], "happy_hour": [{"G05": 6}], "dinner": [{"G06": 2}, {"G07": 8}]}, 4)``  | ``2``            |                 
            +----------------------------------------------------------------------------------------------------------------------------------------------------------------------+------------------+
            |``table_reservation({"brunch": [{"G01": 2}], "lunch": [{"G02": 2}, {"G03": 4}], "happy_hour": [{"G04": 2}], "dinner": [{"G05": 2}, {"G06": 8}]}, 2)``                 | ``4``            |
            +----------------------------------------------------------------------------------------------------------------------------------------------------------------------+------------------+
            |``table_reservation({"breakfast": [{"G01": 1}], "lunch": [{"G02": 2}, {"G03": 4}], "happy_hour": [{"G04": 6}], "dinner": [{"G05": 2}, {"G06": 8}]}, 6)``              | ``1``            |
            +----------------------------------------------------------------------------------------------------------------------------------------------------------------------+------------------+     
        
        ~~~~
        def table_reservation(reservation_dict, guest_num):




                    



        ====

        from unittest.gui import TestCaseGui

        class myTests(TestCaseGui):

            def testOne(self):
                self.assertEqual(table_reservation({"breakfast": [{"G01": 3}, {"G02": 4}], "lunch": [{"G03": 2}, {"G04": 4}], "happy_hour": [{"G05": 6}], "dinner": [{"G06": 2}, {"G07": 8}]}, 4), 2)
                self.assertEqual(table_reservation({"breakfast": [{"G01": 2}, {"G02": 4}], "lunch": [{"G03": 2}, {"G04": 2}], "happy_hour": [{"G05": 6}], "dinner": [{"G06": 2}, {"G07": 8}]}, 2), 4)
                self.assertEqual(table_reservation({"breakfast": [{"G01": 2}, {"G02": 4}], "lunch": [{"G03": 2}, {"G04": 2}], "happy_hour": [{"G05": 6}], "dinner": [{"G06": 2}, {"G07": 8}]}, 10), 0)
                self.assertEqual(table_reservation({"breakfast": [{"G01": 1}, {"G02": 4}]}, 1), 1)
                self.assertEqual(table_reservation({"lunch": [{"G01": 1}, {"G02": 4}], "happy_hour": [{"G01": 1}, {"G02": 4}]}, 1), 2)
                self.assertEqual(table_reservation({"breakfast": [{"G02": 4}]}, 9), 0)
        myTests().main()



.. poll::  how_use_1_op
    :allowcomment:
    :option_1: I didn't use it.
    :option_2: I wanted to get an idea about how to start solving the problem.
    :option_3: I wasn't stuck, but I wanted to check something I wasn't sure about when writing the code.
    :option_4: I wanted to know what to do next because I was stuck.
    :option_5: I finished writing the code, but it did not pass all the unit tests, so I wanted to figure out what went wrong.
    :option_6: None of the above.
    :results: instructor

    How did you use the "Help" to solve the preceding problem? Please select the option that best describes your situation. Please explain it in detail in the comment (Option 2- 6). If you did not use the "Help", select Option 1.

    
.. poll:: mental_poll_1_op
    :allowcomment:
    :option_1: Very, very low mental effort
    :option_2: Very low mental effort
    :option_3: Low mental effort
    :option_4: Rather low mental effort
    :option_5: Neither low nor high mental effort
    :option_6: Rather high mental effort
    :option_7: High mental effort
    :option_8: Very high mental effort
    :option_9: Very, very high mental effort
    :results: instructor

    In solving the preceding problem I invested:

.. fillintheblank:: reflect_1_op

    The following statements ask you about the usefulness with the **"Help" feature**. It includes using the initial Help button, view Help again button and regenerate Help button. For each statement, please use the following scale to indicate what is most true for you.
        
    .. list-table::
       :align: center
       :header-rows: 1

       * - Strongly Disagree
         - Disagree
         - Neither agree or disagree
         - Agree
         - Strongly Agree
       * - 1
         - 2
         - 3
         - 4
         - 5

    **A.** The above "Help" was useful in helping me **identify what I did wrong**.  |blank|

    **B.** The above "Help" was useful in helping me **think through how to construct a correct solution**. |blank|

    **C.** The above "Help" was useful in improving my **problem-solving skill on this topic**, e.g. finding the strategy to solve the problem.  |blank| 

    **D.** The above "Help" was useful in improving my **understanding of this topic**, e.g. what does nested dictionary mean, etc. |blank|
    

    -   :1.0 5.0:       Saved
        :.*:            Incorrect
    -   :1.0 5.0:       Saved
        :.*:            Incorrect
    -   :1.0 5.0:       Saved
        :.*:            Incorrect
    -   :1.0 5.0:       Saved
        :.*:            Incorrect



.. activecode:: get_average_score_ac
        :autograde: unittest
        :nocodelens:
        
        Finish the function ``get_average_score(student_information)`` below:
            - It takes a dictionary ``student_information`` representing student data, where the keys are student names, and the values are dictionaries containing information about the student, including their age and a list of courses they took and the grade for each course.
            - You then need to calculate the average grade for each student.
            - Return a dictionary that stores the students whose average grade is higher than or equal to ``80`` in a dictionary. The keys are student names and the values are their average grade.

        .. table::
            :name: item_quantity_table
            :align: left
            :width: 50

            +---------------------------------------------------------------------------------------------------------------------------------------+--------------------------------+
            | Example Input                                                                                                                         | Expected Output                |
            +=======================================================================================================================================+================================+
            |``get_average_score({"Alice": {"age": 20, "courses": {"Math": 90}}, "Bob": {"age": 22, "courses": {"History": 92, "Science": 88}}})``  | ``{"Alice": 90, "Bob": 90}``   |                 
            +---------------------------------------------------------------------------------------------------------------------------------------+--------------------------------+
            |``get_average_score({"Charlie": {"age": 21, "courses": {"Math": 70, "History": 60}})``                                                 | ``{}``                         |
            +---------------------------------------------------------------------------------------------------------------------------------------+--------------------------------+
            |``get_average_score({"Bob": {"age": 22, "courses": {"Math": 92, "History", 86}})``                                                     | ``{"Bob": 89}``                |
            +---------------------------------------------------------------------------------------------------------------------------------------+--------------------------------+     
        
        ~~~~
        def get_average_score(student_information):


            





        ====

        from unittest.gui import TestCaseGui

        class myTests(TestCaseGui):

            def testOne(self):
                self.assertEqual(get_average_score({"Alice": {"age": 20, "courses": {"Math": 90}}, "Bob": {"age": 22, "courses": {"Math": 87, "History": 92, "Science": 85}}}), {"Alice": 90, "Bob": 88})
                self.assertEqual(get_average_score({"Bob": {"age": 22, "courses": {"Math": 75, "History": 85}}}), {"Bob": 80})
                self.assertEqual(get_average_score({"Bob": {"age": 22, "courses": {"Math": 75, "History": 85}}, "Charlie": {"age": 21, "courses": {"Math": 70}}}), {"Bob": 80})
                self.assertEqual(get_average_score({"Bob": {"age": 22, "courses": {"Math": 92, "History": 86}}})["Bob"], 89)
                self.assertEqual(get_average_score({"Mike": {"age": 22, "courses": {"Math": 60, "History": 60}}}), {})
        myTests().main()



.. poll::  how_use_2_op
    :allowcomment:
    :option_1: I didn't use it.
    :option_2: I wanted to get an idea about how to start solving the problem.
    :option_3: I wasn't stuck, but I wanted to check something I wasn't sure about when writing the code.
    :option_4: I wanted to know what to do next because I was stuck.
    :option_5: I finished writing the code, but it did not pass all the unit tests, so I wanted to figure out what went wrong.
    :option_6: None of the above.
    :results: instructor

    How did you use the "Help" to solve the preceding problem? Please select the option that best describes your situation. Please explain it in detail in the comment (Option 2- 6). If you did not use the "Help", select Option 1.

    
.. poll:: mental_poll_2_op
    :allowcomment:
    :option_1: Very, very low mental effort
    :option_2: Very low mental effort
    :option_3: Low mental effort
    :option_4: Rather low mental effort
    :option_5: Neither low nor high mental effort
    :option_6: Rather high mental effort
    :option_7: High mental effort
    :option_8: Very high mental effort
    :option_9: Very, very high mental effort
    :results: instructor

    In solving the preceding problem I invested:

.. fillintheblank:: reflect_2_op

    The following statements ask you about the usefulness with the **"Help" feature**. It includes using the initial Help button, view Help again button and regenerate Help button. For each statement, please use the following scale to indicate what is most true for you.
        
    .. list-table::
       :align: center
       :header-rows: 1

       * - Strongly Disagree
         - Disagree
         - Neither agree or disagree
         - Agree
         - Strongly Agree
       * - 1
         - 2
         - 3
         - 4
         - 5

    **A.** The above "Help" was useful in helping me **identify what I did wrong**.  |blank|

    **B.** The above "Help" was useful in helping me **think through how to construct a correct solution**. |blank|

    **C.** The above "Help" was useful in improving my **problem-solving skill on this topic**, e.g. finding the strategy to solve the problem.  |blank| 

    **D.** The above "Help" was useful in improving my **understanding of this topic**, e.g. what does nested dictionary mean, etc. |blank|
    


    -   :1.0 5.0:       Saved
        :.*:            Incorrect
    -   :1.0 5.0:       Saved
        :.*:            Incorrect
    -   :1.0 5.0:       Saved
        :.*:            Incorrect
    -   :1.0 5.0:       Saved
        :.*:            Incorrect



.. activecode:: get_vegetarian_menu_ac
        :autograde: unittest
        :nocodelens:

        Finish the function ``get_vegetarian_menu(menu_items):`` below:
            - It takes a list of tuples ``menu_items`` as input, each tuple contains ``(name, category, price, is_vegetarian)``.
            - It returns a new nested dictionary that only contains the items from  ``menu_items`` where ``is_vegetarian`` is ``True``.
                - The outer dictionary keys are ``category`` such as "Soup", "Pizza", "Pasta", "Salad". 
                - The inner dictionary keys are ``name`` and values are ``price`` for each vegetarian item of that ``category``.


        .. table::
            :name: get_vegetarian_menu_table
            :align: left
            :width: 40

            +--------------------------------------------------------------------------------------------------------------------------------------------------------------------+-------------------------------------------------------------------------------------------+
            | Example Input                                                                                                                                                      | Expected Output                                                                           |
            +====================================================================================================================================================================+===========================================================================================+
            |``get_vegetarian_menu([("Margherita", "Pizza", 15, True), ("Pepperoni", "Pizza", 22, False), ("Hawaiian", "Pizza", 10, True), ("Caesar", "Salad", 10, True)])``     | ``{"Pizza": {"Margherita": 15, "Hawaiian": 10}, "Salad": {"Caesar": 10}}``                |                 
            +--------------------------------------------------------------------------------------------------------------------------------------------------------------------+-------------------------------------------------------------------------------------------+
            |``get_vegetarian_menu([("Margherita", "Pizza", 15, True), ("Pepperoni", "Pizza", 22, False), ("Olive-Walnut", "Pasta", 20, True), ("Caesar", "Salad", 10, True)])`` | ``{"Pizza": {"Margherita": 15}, "Pasta": {"Olive-Walnut": 20}, "Salad": {"Caesar": 10}}`` |                                                       
            +--------------------------------------------------------------------------------------------------------------------------------------------------------------------+-------------------------------------------------------------------------------------------+
            |``get_vegetarian_menu([("Lentil", "Soup", 15, True), ("Salmorejo", "Soup", 18, True), ("Harvest", "Salad", 18, False), ("Tuna Poke", "Salad", 20, False)])``        | ``{"Soup": {"Lentil": 15, "Salmorejo": 18}``                                              |
            +--------------------------------------------------------------------------------------------------------------------------------------------------------------------+-------------------------------------------------------------------------------------------+     

        ~~~~
        def get_vegetarian_menu(menu_items):








        ====
        from unittest.gui import TestCaseGui

        class myTests(TestCaseGui):

            def testOne(self):
                self.assertEqual(get_vegetarian_menu([("Margherita", "Pizza", 15, True), ("Pepperoni", "Pizza", 22, False), ("Hawaiian", "Pizza", 10, True), ("Caesar", "Salad", 10, True)]), {"Pizza": {"Margherita": 15, "Hawaiian": 10}, "Salad": {"Caesar": 10}})
                self.assertEqual(get_vegetarian_menu([("Lentil", "Soup", 15, True), ("Salmorejo", "Soup", 18, True), ("Harvest", "Salad", 18, False), ("Tuna Poke", "Salad", 20, False)]), {"Soup": {"Lentil": 15, "Salmorejo": 18}})
                self.assertEqual(get_vegetarian_menu([("Margherita", "Pizza", 15, True), ("Pepperoni", "Pizza", 22, False), ("Olive-Walnut", "Pasta", 20, True), ("Caesar", "Salad", 10, True)]), {"Pizza": {"Margherita": 15}, "Pasta": {"Olive-Walnut": 20}, "Salad": {"Caesar": 10}})
                self.assertEqual(get_vegetarian_menu([("Margherita", "Pizza", 15, False)]), {})
                self.assertEqual(get_vegetarian_menu([("Lentils", "Side", 5, True), ("Potatoes", "Side", 5, False), ("Peas", "Side", 5, True)]), {"Side": {"Lentils": 5, "Peas": 5}})
        myTests().main()





.. poll::  how_use_3_op
    :allowcomment:
    :option_1: I didn't use it.
    :option_2: I wanted to get an idea about how to start solving the problem.
    :option_3: I wasn't stuck, but I wanted to check something I wasn't sure about when writing the code.
    :option_4: I wanted to know what to do next because I was stuck.
    :option_5: I finished writing the code, but it did not pass all the unit tests, so I wanted to figure out what went wrong.
    :option_6: None of the above.
    :results: instructor

    How did you use the "Help" to solve the preceding problem? Please select the option that best describes your situation. Please explain it in detail in the comment (Option 2- 6). If you did not use the "Help", select Option 1.

    
.. poll:: mental_poll_3_op
    :allowcomment:
    :option_1: Very, very low mental effort
    :option_2: Very low mental effort
    :option_3: Low mental effort
    :option_4: Rather low mental effort
    :option_5: Neither low nor high mental effort
    :option_6: Rather high mental effort
    :option_7: High mental effort
    :option_8: Very high mental effort
    :option_9: Very, very high mental effort
    :results: instructor

    In solving the preceding problem I invested:

.. fillintheblank:: reflect_3_op

    The following statements ask you about the usefulness with the **"Help" feature**. It includes using the initial Help button, view Help again button and regenerate Help button. For each statement, please use the following scale to indicate what is most true for you.
        
    .. list-table::
       :align: center
       :header-rows: 1

       * - Strongly Disagree
         - Disagree
         - Neither agree or disagree
         - Agree
         - Strongly Agree
       * - 1
         - 2
         - 3
         - 4
         - 5

    **A.** The above "Help" was useful in helping me **identify what I did wrong**.  |blank|

    **B.** The above "Help" was useful in helping me **think through how to construct a correct solution**. |blank|

    **C.** The above "Help" was useful in improving my **problem-solving skill on this topic**, e.g. finding the strategy to solve the problem.  |blank| 

    **D.** The above "Help" was useful in improving my **understanding of this topic**, e.g. what does nested dictionary mean, etc. |blank|
    


    -   :1.0 5.0:       Saved
        :.*:            Incorrect
    -   :1.0 5.0:       Saved
        :.*:            Incorrect
    -   :1.0 5.0:       Saved
        :.*:            Incorrect
    -   :1.0 5.0:       Saved
        :.*:            Incorrect



.. activecode:: get_order_totals_ac
        :autograde: unittest
        :nocodelens:



        Write a function, ``get_order_totals()``, that takes a list of tuples and returns a nested dictionary with the same information. Each tuple includes 3 values; the first is the person's name, the second is item name, and the third is the quantity. 
        Note that there may be more than one tuple for the same person and item - your dictionary should total all the quantities for the same person and item.
     
        .. table::
            :name: get_order_table
            :align: left
            :width: 40

            +----------------------------------------------------------------------------------------------------+-------------------------------------------------------+
            | Example Input                                                                                      | Expected Output                                       |
            +====================================================================================================+=======================================================+
            |``get_order_totals([('Holden', 'pizza', 1), ('Cristina', 'taco', 2), ('Holden', 'pizza', 1)])``     | ``{'Holden': {'pizza': 2}, 'Cristina': {'taco': 2}}`` |                 
            +----------------------------------------------------------------------------------------------------+-------------------------------------------------------+
            |``get_order_totals([('Holden', 'pizza', 1), ('Cristina', 'taco', 2)])``                             | ``{'Holden': {'pizza': 1}, 'Cristina': {'taco': 2}}`` |                                                       
            +----------------------------------------------------------------------------------------------------+-------------------------------------------------------+
            
        ~~~~
        def get_order_totals(orders):
        






        ====

        from unittest.gui import TestCaseGui

        class myTests(TestCaseGui):

            def testOne(self):
                self.assertEqual(get_order_totals([('Holden', 'pizza', 1), ('Cristina', 'taco', 2), ('Holden', 'pizza', 1)]), {'Holden': {'pizza': 2}, 'Cristina': {'taco': 2}})
                self.assertEqual(get_order_totals([('person1', 'food1', 2), ('person2', 'food2', 2)]), {'person1': {'food1': 2}, 'person2': {'food2': 2}})
                self.assertEqual(get_order_totals([('person1', 'food1', 1)]), {'person1': {'food1': 1}})
                self.assertEqual(get_order_totals([('p1', 'f1', 2), ('p1', 'f1', 3), ('p2', 'f1', 4), ('p1', 'f2', 5), ('p2', 'f2', 2)])['p1']['f1'], 5)

        myTests().main()




.. poll::  how_use_4_op
    :allowcomment:
    :option_1: I didn't use it.
    :option_2: I wanted to get an idea about how to start solving the problem.
    :option_3: I wasn't stuck, but I wanted to check something I wasn't sure about when writing the code.
    :option_4: I wanted to know what to do next because I was stuck.
    :option_5: I finished writing the code, but it did not pass all the unit tests, so I wanted to figure out what went wrong.
    :option_6: None of the above.
    :results: instructor

    How did you use the "Help" to solve the preceding problem? Please select the option that best describes your situation. Please explain it in detail in the comment (Option 2- 6). If you did not use the "Help", select Option 1.

    
.. poll:: mental_poll_4_op
    :allowcomment:
    :option_1: Very, very low mental effort
    :option_2: Very low mental effort
    :option_3: Low mental effort
    :option_4: Rather low mental effort
    :option_5: Neither low nor high mental effort
    :option_6: Rather high mental effort
    :option_7: High mental effort
    :option_8: Very high mental effort
    :option_9: Very, very high mental effort
    :results: instructor

    In solving the preceding problem I invested:

.. fillintheblank:: reflect_4_op

    The following statements ask you about the usefulness with the **"Help" feature**. It includes using the initial Help button, view Help again button and regenerate Help button. For each statement, please use the following scale to indicate what is most true for you.
        
    .. list-table::
       :align: center
       :header-rows: 1

       * - Strongly Disagree
         - Disagree
         - Neither agree or disagree
         - Agree
         - Strongly Agree
       * - 1
         - 2
         - 3
         - 4
         - 5

    **A.** The above "Help" was useful in helping me **identify what I did wrong**.  |blank|

    **B.** The above "Help" was useful in helping me **think through how to construct a correct solution**. |blank|

    **C.** The above "Help" was useful in improving my **problem-solving skill on this topic**, e.g. finding the strategy to solve the problem.  |blank| 

    **D.** The above "Help" was useful in improving my **understanding of this topic**, e.g. what does nested dictionary mean, etc. |blank|
    

    -   :1.0 5.0:       Saved
        :.*:            Incorrect
    -   :1.0 5.0:       Saved
        :.*:            Incorrect
    -   :1.0 5.0:       Saved
        :.*:            Incorrect
    -   :1.0 5.0:       Saved
        :.*:            Incorrect


.. poll::  satisfication_op
    :allowcomment:
    :option_1: Very, very low satisfaction
    :option_2: Very low satisfaction
    :option_3: Low satisfaction
    :option_4: Rather low satisfaction
    :option_5: Neither low nor high satisfaction
    :option_6: Rather high satisfaction
    :option_7: High satisfaction
    :option_8: Very high satisfaction
    :option_9: Very, very high satisfaction
    :results: instructor

    From 1-lowest to 9-highest, rate your level of **satisfaction** with the "Help" feature. Explain the reason for your choice in the comment box.


.. poll::  confidence_op
    :allowcomment:
    :option_1: Very, very low confidence
    :option_2: Very low confidence
    :option_3: Low confidence
    :option_4: Rather low confidence
    :option_5: Neither low nor high confidence
    :option_6: Rather high confidence
    :option_7: High confidence
    :option_8: Very high confidence
    :option_9: Very, very high confidence
    :results: instructor

    From 1-lowest to 9-highest, rate your level of **confidence** in your ability to solve a similar problem from scratch after the practice. Explain the reason for your choice in the comment box.


.. poll::  closeness_op
    :allowcomment:
    :option_1: Very, very low alignment
    :option_2: Very low alignment
    :option_3: Low alignment
    :option_4: Rather low alignment
    :option_5: Neither low nor high alignment
    :option_6: Rather high alignment
    :option_7: High alignment
    :option_8: Very high alignment
    :option_9: Very, very high alignment
    :results: instructor


    From 1-lowest to 9-highest, how closely do the solutions provided in the "Help" **align with** your initial idea for a solutions? Explain the reason for your choice in the comment box.


.. shortanswer:: end_explain_op
   
    If you did not use the “Help ” at all when solving the above practice problems, please explain why. Please skip this question if you used the "Help" at least once.




What to do next
^^^^^^^^^^^^^^^^
.. raw:: html

    <p>Click on the following link to work on the post test: <a id="pps-end-survey" href="pps-end-survey.html"><font size="+1"><b>End of Practice Survey</b></font></a></p>
