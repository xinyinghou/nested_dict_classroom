Skill Assessment
================

Self-efficacy Survey
^^^^^^^^^^^^^^^^^^^^

.. poll:: CS-self-efficacy-1
    :option_1: Strongly disagree
    :option_2: Disagree
    :option_3: Neither agree nor disagree
    :option_4: Agree
    :option_5: Strongly agree
    :results: instructor

    Generally I have felt secure about attempting computer programming problems.

.. poll:: CS-self-efficacy-2
    :option_1: Strongly disagree
    :option_2: Disagree
    :option_3: Neither agree nor disagree
    :option_4: Agree
    :option_5: Strongly agree
    :results: instructor

    I am sure I could do advanced work in computer science.

.. poll:: CS-self-efficacy-3
    :option_1: Strongly disagree
    :option_2: Disagree
    :option_3: Neither agree nor disagree
    :option_4: Agree
    :option_5: Strongly agree
    :results: instructor

    I am sure that I can learn programming.

.. poll:: CS-self-efficacy-4
    :option_1: Strongly disagree
    :option_2: Disagree
    :option_3: Neither agree nor disagree
    :option_4: Agree
    :option_5: Strongly agree
    :results: instructor

    I think I could handle more difficult programming problems.

.. poll:: CS-self-efficacy-5
    :option_1: Strongly disagree
    :option_2: Disagree
    :option_3: Neither agree nor disagree
    :option_4: Agree
    :option_5: Strongly agree
    :results: instructor

    I can get good grades in computer science.

.. poll:: CS-self-efficacy-6
    :option_1: Strongly disagree
    :option_2: Disagree
    :option_3: Neither agree nor disagree
    :option_4: Agree
    :option_5: Strongly agree
    :results: instructor

    I have a lot of self-confidence when it comes to programming.


For the next three questions, please select the answer that best matches your familiarity and confidence about the specified concept(s).


.. poll:: nested-dict-1
    :option_1: I am unfamiliar with this concept
    :option_2: I know what it means, but have not used it in a program
    :option_3: I have used this concept in a program, but am not confident about my ability to use it
    :option_4: I am confident in my ability to use this concept in simple programs
    :option_5: I am confident in my ability to use this concept in complex programs
    :results: instructor

    Access values in inner dictionary like <code>value_for_inner_key1 = nested_dict['outer_key']['inner_key1']</code>

.. poll:: nested-dict-2
    :option_1: I am unfamiliar with this concept
    :option_2: I know what it means, but have not used it in a program
    :option_3: I have used this concept in a program, but am not confident about my ability to use it
    :option_4: I am confident in my ability to use this concept in simple programs
    :option_5: I am confident in my ability to use this concept in complex programs
    :results: instructor

    Add a new key-value pair to the inner dictionary of the given nested dictionary like <code>nested_dict['outer_key']['new_key'] = 'new_value'</code>

.. poll:: nested-dict-3
    :option_1: I am unfamiliar with this concept
    :option_2: I know what it means, but have not used it in a program
    :option_3: I have used this concept in a program, but am not confident about my ability to use it
    :option_4: I am confident in my ability to use this concept in simple programs
    :option_5: I am confident in my ability to use this concept in complex programs
    :results: instructor

    Loop through the outer items (key-value pairs) of a nested dictionary like <code>for outer_key, outer_value in nested_dict.items():</code>


Skill Assessment
^^^^^^^^^^^^^^^^
.. timed:: skill-assessment-1
    :timelimit: 5

    Please choose the option you think is the best answer for the following two questions.

    .. poll:: pretest-mcq-1
        :option_1: {'f': {'g': '456'}}
        :option_2: {'c': {'f': {'g': '456'}}}
        :option_3: '123'
        :option_4: {'g': '456'}
        :option_5: '456'
        :option_6: {'e': '123'}
        :results: instructor
        
        <code> nested_dict = {'a': {'b': {'e': '123'}, 'c': {'f': {'g': '456'}}}} </code> 
        <br><br>
        What does <code>nested_dict['a']['c']['f']</code> return?


    .. poll:: pretest-mcq-2
        :option_1: <code>my_dict['first_level']['B']['d']['f']</code>
        :option_2: <code>my_dict['first_level']['B']['f']</code>
        :option_3: <code>my_dict['first_level']['B']['d'][1]</code>
        :option_4: <code>my_dict['second_level']['D']['i']['f']</code>
        :option_5: <code>my_dict['second_level']['D']['h']['f']</code>
        :option_6: <code>my_dict['second_level']['D']['f']['j']</code>
        :results: instructor
        
            <code> 
                my_dict = {'first_level': {'A': {'a': 1, 'b': 2},'B': {'c': 3, 'd': {'e': 4, 'f': 5}}},
                        'second_level': {'C': {'g': 6},'D': {'h': 7, 'i': {'j': 8}}}}
            </code> 
        <br><br>
        What is the correct way to access the value associated with the key <code>'f'<code> inside the nested dictionary?


    .. activecode:: pretest-ac_3
        :nocodelens:
        
        How to correctly print each employee's name along with their skills, using a nested loop?
        ~~~~
        employees = {'John': {'age': 28, 'position': 'Designer', 'skills': ['Figma']}, 
                        'Alice': {'age': 34, 'position': 'Developer','skills': ['Python', 'AWS']}}
        # Write your code here:
        



        """ Expected Output:
        John Figma
        Alice Python
        Alice AWS
        """
    

What to do next
^^^^^^^^^^^^^^^^
.. raw:: html

    <p>Click on the following link to learn how to solve different types of problems in this ebook : <b><a id="p3pps-intro"><font size="+2">Introduction to Problem Types</font></a></b></p>

.. raw:: html

   <script type="text/javascript">

     function getCookie(cookieName) {
        let name = cookieName + "=";
        let decodedCookie = decodeURIComponent(document.cookie);
        let ca = decodedCookie.split(';');
        for(let i = 0; i < ca.length; i++) {
           let c = ca[i];
           while (c.charAt(0) == ' ') {
              c = c.substring(1);
           }
           if (c.indexOf(name) == 0) {
              return c.substring(name.length, c.length);
           }
        }
        return "";
     }

     function setCookie(cookieName, cvalue) {
        document.cookie = cookieName + "=" + cvalue + ";";
     }

     window.onload = function() {

        a = document.getElementById("p3pps-intro")

        // get prev set cookie
        var EXP_COOKIE = 'p3pps-exp'
        var cond = getCookie(EXP_COOKIE);

        // if no prev set cookie: generate random condition and set cookie
        if (cond != 'acoc' && cond != 'acop') {
           var v = Math.floor(Math.random() * 2);
           if (v < 1) {
               cond = 'acoc';
           } else {
               cond = 'acop';
           }
           setCookie(EXP_COOKIE, cond);
        }

        if (cond == 'acop') {
           a.href = "pps-intro-OP.html"
        } else if (cond == 'acoc') {
           a.href = "pps-intro-OC.html"
        }
     };
   </script>


