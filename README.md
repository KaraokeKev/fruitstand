ansible-playbook tmp.yml -t apple

ansible-playbook tmp.yml -t 1_2_3





For tags, if it starts with a number it must be in quotes. e.g.

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

