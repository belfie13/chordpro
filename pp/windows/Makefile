# nmake file for MS Windows + CitrusPerl
# Based on 32-bit nmake and CitrusPerl 5.16 with wxWidgets 2.8.

chordpro.exe : chordpro.pp
	pp --output=chordpro.exe @chordpro.pp ../script/chordpro.pl

# For wxWidgets, explicit libraries are specified in wxchordpro.pp and the
# PATH must be set accordingly.
wxchordpro.exe : chordpro.pp wxchordpro.pp wxchordpro.msw.pp
	set path=C:\\CitrusPerl\\vendor\\lib\\Alien\\wxWidgets\\msw_2_8_12_uni_gcc_3_4\\lib;%path%
	pp --output=wxchordpro.exe @wxchordpro.msw.pp ../script/wxchordpro.pl

# NOTE: THIS IS FOR TESTING/DEVELOPMENT ONLY.
refresh :
	xcopy /s /y h:\ChordPro ..
	del *chordpro.exe
