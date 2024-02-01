Posttest Problems
^^^^^^^^^^^^^^^^^^^^^^^^^^^

* 💻 Please complete the problems below independently without any outside help, including AI tools like ChatGPT.

* Again, you can stop working on a problem after you worked on it for about five minutes without solving it. 



Please choose the option you think is the best answer for the following two questions.

.. poll:: posttest-mcq-1
    :option_1: <code>{'f': {'g': '456'}}</code>
    :option_2: <code>{'c': {'f': {'g': '456'}}}</code>
    :option_3: <code>'123'</code>
    :option_4: <code>{'g': '456'}</code>
    :option_5: <code>'456'</code>
    :results: instructor
    
    <code> nested_dict = {'a': {'b': {'e': '123'}, 'c': {'f': {'g': '456'}}}} </code> 
    <br><br>
    What does <code>nested_dict['a']['c']['f']</code> return?


.. poll:: posttest-mcq-2
    :option_1: <code>my_dict['first_level']['B']['d']['f']</code>
    :option_2: <code>my_dict['first_level']['B']['f']</code>
    :option_3: <code>my_dict['first_level']['B']['d'][1]</code>
    :option_4: <code>my_dict['second_level']['D']['i']['f']</code>
    :option_5: <code>my_dict['second_level']['D']['h']['f']</code>
    :results: instructor
    
        <code> 
            my_dict = {'first_level': {'A': {'a': 1, 'b': 2},'B': {'c': 3, 'd': {'e': 4, 'f': 5}}},
                    'second_level': {'C': {'g': 6},'D': {'h': 7, 'i': {'j': 8}}}}
        </code> 
    <br><br>
    What is the correct way to access the value associated with the key <code>'f'<code> inside the nested dictionary?


.. shortanswer:: posttest-sa_3
    :nocodelens:
    
    Please write the code line that is missing below

    .. code-block::

        employees = {
            'John': {'age': 28, 'position': 'Designer', 'skills': {'soft_skill': 'Creativity', 'technical_skill': 'Figma'}},
            'Alice': {'age': 34, 'position': 'Developer', 'skills': {'soft_skill': 'Communication', 'technical_skill': 'Python'}}
        }

        # Printing each employee's name along with their skills using a nested loop
        for name, details in employees.items():
            # Write one code line that is missing here to print the employee's name, skill_type and skill_value
                print(f"{name}'s {skill_type_key}: {skill_expertise_value}")
        
        """ The output of the code above should be:
        John's soft_skill: Creativity
        John's technical_skill: Figma
        Alice's soft_skill: Communication
        Alice's technical_skill: Python
        """



.. parsonsprob:: mixedup_customer_payment
    :numbered: left
    :practice: T

    Create a function ``customer_payment(order_list, price_dict)``: 
    - Input ``order_list`` contains a list of tuples, each tuple includes 3 values; the first is the person's name, the second is item name, and the third is the quantity. Note that there may be more than one tuple for the same person and item
    - Input ``price_dict`` contains a dictionary where the keys are the item names, and values are the prices.
    - The output dictionary should return the total price each customer needs to pay based on the ``order_list`` and ``price_list``.


    .. table::
        :name: payment_table
        :align: left
        :width: 50

        +-----------------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
        | Example Input                                                                                                                                       | Expected Output                   | Explanation                                                                                                                                          |
        +=====================================================================================================================================================+===================================+======================================================================================================================================================+
        |``customer_payment([('Holden', 'pizza', 1), ('Cristina', 'taco', 1), ('Cristina', 'pizza', 2)], {'pizza': 8, 'taco': 6})``                           | ``{'Holden': 8, 'Cristina': 22}`` | Holden ordered 1 pizza ($8 each); Cristina ordered 2 pizzas ($8 each) for a total of $16 and 1 taco at $6, so the total is $22                       |                 
        +-----------------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
        |``customer_payment([('Bob', 'pizza', 1), ('Mike', 'taco', 2), ('Bob', 'taco', 1), ('Mike', 'burger', 2)], {'pizza': 8, 'taco': 6, 'burger': 10})``   | ``{'Bob': 14, 'Mike': 32}``       | Bob ordered 1 pizza ($8 each) and 1 taco ($6 each), so the total is $14; Mike ordered 2 burgers ($10 each) and 2 tacos ($6 each), so the total is 32 | 
        +-----------------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
    
    -----
    def customer_payment(order_list, price_list):
    =====
        payment_totals = {}
    =====
        for person, item, quantity in order_list:
    =====
        for person, item, quantity in order_list.items(): #paired
    =====
            item_cost = quantity * price_list[item]
    =====
            if person not in payment_totals:
    =====
            if person not in payment_totals.values: #paired
    =====
                payment_totals[person] = item_cost
    =====
            else:
    =====
                payment_totals[person] += item_cost
    =====
        return payment_totals


.. activecode:: identify_top_employee_fix_v2
    :autograde: unittest
    :nocodelens:

    Fix the function ``top_employee(employee_dict)`` below:
        - The ``employee_dict`` is a nested dictionary. The outermost dictionary has unique employee names as keys and a dictionary as values. 
        - Each second-level dictionary has keys of age and performance. The value for the key ``age`` is a number, the value for the key ``performance`` is a dictionary.
        - The ``performance`` dictionary has keys of quarters (``Q1``, ``Q2``, ``Q3``, ``Q4``), and a performance score as the value out of 100. 
        - The goal is to return a new dictionary where the keys are the names of top employees (those whose average performance score is above or equal to ``90``), and the values are their average performance scores.
    
    .. table::
        :name: identify_top_employee_table
        :align: left
        :width: 50

        +-------------------------------------------------------------------------------------------------------------------------------------------------+--------------------------------+
        | Example Input                                                                                                                                   | Expected Output                |
        +=================================================================================================================================================+================================+
        |``top_employee({"Alice": {"age": 30, "performance": {"Q4": 95}}, "Bob": {"age": 33, "performance": {"Q1": 93, "Q2": 88, "Q3": 95, "Q4": 88}}})`` | ``{"Alice": 95, "Bob": 91}``   |                 
        +-------------------------------------------------------------------------------------------------------------------------------------------------+--------------------------------+
        |``top_employee({"Charlie": {"age": 31, "performance": {"Q3": 70, "Q4": 60}})``                                                                   | ``{}``                         |
        +-------------------------------------------------------------------------------------------------------------------------------------------------+--------------------------------+
        |``top_employee({"Bob": {"age": 33, "performance": {"Q3": 92, "Q4", 92}})``                                                                       | ``{"Bob": 92}``                |
        +-------------------------------------------------------------------------------------------------------------------------------------------------+--------------------------------+     

    ~~~~
    def top_employee(employee_dict):
        top_employees = {}
        
        for employee, employee_data in employee_dict.values:
            performance_dict = employee_data["performance"].items
            score_total = 0
            for quarter, score in performance_dict.item():
                score_total += score
            average_score = score_total / len(performance_dict)

            if average_score > 90:
                top_employees[employee] = average_score

        return top_employees

    ====
    
    from unittest.gui import TestCaseGui

    class myTests(TestCaseGui):
        def testOne(self):
            self.assertEqual(top_employee({"Bob": {"age": 22, "performance": {"Q3": 92, "Q4": 90}}})["Bob"], 91)
            self.assertEqual(top_employee({"Mike": {"age": 22, "performance": {"Q3": 60, "Q4": 60}}}), {})
            self.assertEqual(top_employee({"Alice": {"age": 20, "performance": {"Q4": 90}}, "Bob": {"age": 22, "performance": {"Q2": 87, "Q3": 92, "Q4": 60}}}), {"Alice": 90})
            self.assertEqual(top_employee({"Bob": {"age": 22, "performance": {"Q3": 92, "Q4": 92}}}), {"Bob": 92})
            self.assertEqual(top_employee({"Bob": {"age": 22, "performance": {"Q3": 92, "Q4": 92}}, "Charlie": {"age": 21, "performance": {"Q4": 70}}}), {"Bob": 92})

    myTests().main() 

    

.. activecode:: happy_hour_specials_ac
    :autograde: unittest
    :nocodelens:

    Write the function ``happy_hour_specials(menu_items)``:
        - ``menu_items`` is a list of tuples. Each tuple contains ``(name, category, is_today_special, price)``.
        - Return a nested dictionary that only includes the items marked as today's special (``is_today_special`` is ``True``) and where the prices are less than or equal to ``15``. Each outer key is the ``category`` and each value is a dictionary. The inner dictionary keys are ``name``, and the values are ``price``.

    .. table::
        :name: today_specical_table
        :align: left
        :width: 40

        +--------------------------------------------------------------------------------------------------------------------------------------------------------------------+----------------------------------------------------------------------------+
        | Example Input                                                                                                                                                      | Expected Output                                                            |
        +====================================================================================================================================================================+============================================================================+
        |``happy_hour_specials([("Margherita", "Pizza", True, 15), ("Pepperoni", "Pizza", False, 22), ("Hawaiian", "Pizza", True, 10), ("Caesar", "Salad", True, 10)])``     | ``{"Pizza": {"Margherita": 15, "Hawaiian": 10}, "Salad": {"Caesar": 10}}`` |                 
        +--------------------------------------------------------------------------------------------------------------------------------------------------------------------+----------------------------------------------------------------------------+
        |``happy_hour_specials([("Margherita", "Pizza", True, 15), ("Pepperoni", "Pizza", False, 22), ("Olive-Walnut", "Pasta", True, 20), ("Caesar", "Salad", True, 10)])`` | ``{"Pizza": {"Margherita": 15}, "Salad": {"Caesar": 10}}``                 |                                                       
        +--------------------------------------------------------------------------------------------------------------------------------------------------------------------+----------------------------------------------------------------------------+
        |``happy_hour_specials([("Lentil", "Soup", True, 15), ("Salmorejo", "Soup", False, 18), ("Harvest", "Salad", False, 18), ("Fruit", "Salad", True, 8)])``             | ``{"Soup": {"Lentil": 15}, "Salad": {"Fruit": 8}}``                        |
        +--------------------------------------------------------------------------------------------------------------------------------------------------------------------+----------------------------------------------------------------------------+     


    ~~~~
    def happy_hour_specials(new_menu_items):








    ====
        
    from unittest.gui import TestCaseGui

    class myTests(TestCaseGui):

        def testOne(self):

            self.assertEqual(happy_hour_specials([("Classic", "Burger", True, 12), ("Veggie", "Burger", True, 14), ("Fish", "Burger", True, 16), ("Cheese", "Pizza", False, 20)]), {"Burger": {"Classic": 12, "Veggie": 14}})
            self.assertEqual(happy_hour_specials([("Mango", "Smoothie", True, 8), ("Green", "Smoothie", True, 12), ("Chocolate", "Milkshake", True, 15), ("Vanilla", "Milkshake", False, 18)]), {"Smoothie": {"Mango": 8, "Green": 12}})
            self.assertEqual(happy_hour_specials([("Spaghetti", "Pasta", True, 10), ("Alfredo", "Pasta", True, 12), ("Bolognese", "Pasta", True, 14), ("Seafood", "Pasta", True, 18)]), {"Pasta": {"Spaghetti": 10, "Alfredo": 12, "Bolognese": 14}})
            self.assertEqual(happy_hour_specials([("Fruit", "Salad", True, 8), ("Greek", "Salad", True, 12), ("Caesar", "Salad", True, 14), ("Chicken", "Salad", False, 18)]), {"Salad": {"Fruit": 8, "Greek": 12, "Caesar": 14}})

    myTests().main()




🙌 Thank You!
============================
Thank you for taking part in this study!  We appreciate your time on this.


