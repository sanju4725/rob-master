###################################TASKS#############################################

1)def spin:
  make it spin?
  set speeds(a,-a,-a,a)

2)def stop:
  set speeds(0,0,0,0)

3)def turn:
  set rotation with degrees (adegree)

4)def forward:
  sets speed as same for all to go into the direction

5)def reverse:
  sets same speed just negative

set behaviour:
  6)Random walk/ wander ():
    just turn randomly
    with every 4/5 sec turn a random degree then go on
    while on walk turn the gimbal every 4/5 sec to check for a person

set behaviour:
  7)look around
    just spin the gimbal if you find person lock ont him
    uses. camera& gimbal

check conditions:
  8)find_person:
    whenever look around happens look for a person
    vision_ctrl.enable_detection(rm_define.vision_detection_people)
    and reset timer!
    

set behaviour:
  9)follow person:
    once a person is found by the findperson
    you just go behind him like 
    def vision_recognized_people(msg):
      make sure they stay in frame!


check conditions:
  10)collision(hit detection):
    while wandering if you get Hit
    if this is triggered reverse out of the spot and reset the timer
    

set behaviour:
  11)light up:
    set led on all 4 sides to flash if you find people
    set led only on the side that was hit if collision is detected
    
set behaviour:
  12)lasers:
    set the laser on then spin the gimbal 
    so it puts up a show


check conditions:
  13)lost(timer):
    if timer hits a certain limit simply accept defeat and o the spin with the leds flashing on all 4 skip_doctest


https://github.com/sanju4725/rob-master/assets/92858165/7d8676e6-7d3c-419a-a851-74ff8c439bd0


  
