ATTINY_pwm_script
=================

pwm for a servo motor, LED and speaker, interactivity: LDR

hacked the script together using:
http://avrbasiccode.wikispaces.com/home

for the servo to run properly the only change was:

TCCR0A |= (1 << COM0A1)  // COM0A1 - COM0A0 (Set OC0A on Compare Match, clear OC0A at TOP)

instead of

TCCR0A |= (1 << COM0A1)|(1 << COM0A0)  // COM0A1 - COM0A0 (Set OC0A on Compare Match, clear OC0A at TOP)

added bit bang sound using the assembler command "nop":
http://playground.arduino.cc/Main/AVR

