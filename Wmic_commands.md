## See windows updates  ##

wmic qfe get hotfixid

## See cpu info ##

wmic cpu list brief
wmic cpu list full

## See bios info ##

wmic bios list brief
wmic bios list full

## See memory info ##

wmic memorychip list full

## See disk drive info ##

wmic diskdrive list full

## See motherboard info ##

wmic baseboard list full

## See graphics card info ##

wmic path win32_videocontroller

## See windows info

wmic os list brief
wmic os list full