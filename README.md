ansible-playbook tmp.yml -t apple

ansible-playbook tmp.yml -t 1_2_3





For tags, if it starts with a number it must be in quotes. e.g.

    - debug:
        msg: "I am a banana"
      tags:
        - banana
        - fruit
        - "1_2_3" 
