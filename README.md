ansible-playbook tmp.yml -t apple

ansible-playbook tmp.yml -t 1_2_3





Tags must be strings. In Python 3.6+, underscores are considered convenience notation for numbers. Therefore 1_2_3 would be considered an integer of value 123.

    - debug:
        msg: "I am a banana"
      tags:
        - banana
        - fruit
        - "1_2_3"


Note the following will not call the "integer test" task from tmp.yml
<ul>
<li>ansible-playbook tmp.yml -t 4_5_6</li>
<li>ansible-playbook tmp.yml -t "4_5_6"</li>
</ul>

However this will:

    ansible-playbook tmp.yml -t 9_9_9

