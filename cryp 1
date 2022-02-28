#!/usr/bin/env python3

import sys
import json
import binascii
import secrets


inputs = json.load(sys.stdin)
outputs = {}

#Problem One
input_string = inputs["problem 1"]
for i in range(len(input_string)):
    input_string[i] = input_string[i].upper()
outputs["problem 1"] = input_string

#Problem Two
input_hextwo = inputs["problem 2"]
output_string2 = []
for i in range(len(input_hextwo)):
    input_hextwo[i] = (input_hextwo[i])
    output_bytes = bytes.fromhex(input_hextwo[i])
    output_ascii = output_bytes.decode()
    output_string2.append(output_ascii)
outputs["problem 2"] = output_string2

#Problem Three
input_hexthree = inputs["problem 3"]
output_string3 = []
initialhex = {}
split_hexthree = []
concat_hex = ""
#preoutput_string3 = ""
newstr = ""

for positionone in range(len(input_hexthree)):
    input_hexthree[positionone] = (input_hexthree[positionone])
    initialhex = input_hexthree[positionone]
  

    split_hexthree = [initialhex[positiontwo: positiontwo + 2] for positiontwo in range(0, len(initialhex), 2)]
 
    outpass = split_hexthree

    for positionthree in range(len(outpass)):
      outpass[positionthree] = (hex((int((outpass[positionthree]),16) + 32 + positionthree) % 256).lstrip("0x"))
     
      concat_hex += outpass[positionthree]
    


    output_string3.append(concat_hex)
    concat_hex = ""

     
outputs["problem 3"] = output_string3









#Problem Four
input_strings_four = inputs["problem 4"]
output_string_four = []

for positionfour in range(len(input_strings_four)):
    input_strings_four[positionfour] = (input_strings_four[positionfour])
    input_strings_four[positionfour] = secrets.randbelow(input_strings_four[positionfour]-1)
    output_string_four.append(input_strings_four[positionfour])

outputs["problem 4"] = output_string_four



print(json.dumps(outputs, indent="  "))
print()
