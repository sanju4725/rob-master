##########################################TASKS########################################################

def spin:
  make it spin?
  set speeds(a,-a,-a,a)

def stop:
  set speeds(0,0,0,0)

def turn:
  set rotation with degrees (45degree)

def forward:
  sets speed as same for all to go into the direction

def reverse:
  sets same speed just negative

set behaviour:
  Random walk/ wander ():
    just turn randomly
    with every 4/5 sec turn a random degree then go on
    while on walk turn the gimbal every 4/5 sec to check for a person
  look around
    just spin the gimbal if you find person lock ont him
    uses. camera& gimbal

check conditions:
  find_person:
    whenever look around happens look for a person
    vision_ctrl.enable_detection(rm_define.vision_detection_people)
    and reset timer!
    

set behaviour:
  follow person:
    once a person is found by the findperson
    you just go behind him like 
    def vision_recognized_people(msg):
      make sure they stay in frame!


check conditions:
  collision(hit detection):
    while wandering if you get Hit
    if this is triggered reverse out of the spot and reset the timer
    

set behaviour:
  light up:
    set led on all 4 sides to flash if you find people
    set led only on the side that was hit if collision is detected
  lasers:
    set the laser on then spin the gimbal 
    so it puts up a show


check conditions:
  lost(timer):
    if timer hits a certain limit simply accept defeat and o the spin with the leds flashing on all 4 skip_doctest

  
