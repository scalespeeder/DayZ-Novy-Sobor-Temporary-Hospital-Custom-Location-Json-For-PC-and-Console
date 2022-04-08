DayZ Novy Sobor Temporary Hospital For Console and PC json Mod Instructions & Terms Of Use

Spawns a Temporary Hospital inside a hanger  & related structures at  6995.96 / 8180.62 which is North of Novy Sobor on Chernarus.

Limited Testing on PC Chernarus Local Server DAYZ Version 1.16 Apr 2021.

Created by @scalespeeder. Please report bugs & errors to scalespeeder@gmail.com with screenshots.

If you'd like to edit the file, simply load "novy-sobor-temp-hospital.dze" into DayZ Editor.

Many Thanks To Inclement Dab for his amazing DayZ Editor that makes this all possible: https://steamcommunity.com/sharedfiles/filedetails/?id=2250764298

TERMS OF USE
THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND,
EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS
OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN
AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH
THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

Using these modded json files and instructions could break the functioning of your DAYZ server, requiring a reinstall that would wipe
all player progress.

Using these modded files neccessitates increased regular restarts to prevent server crashing.

It is suggested you thoroughly test your server after applying these files to ensure proper
functioning of your server.

I always recomend you validate your files at: https://www.xmlvalidation.com/ and https://jsonformatter.curiousconcept.com/

Instructions:

Click the "Code" button and "Download Zip" on the Github Repository and extract the files on your local PC for access.

Stop your server.

Ensure your DayZ Server has activated the cfggameplay.json. For console users on Nitrado Servers, go to "General Settings" on your server and tick "Enable cfggameplay.json".

On PC Servers add the following line to your serverDZ.cfg:

enableCfgGameplayFile = 1;

(On some PC servers, including Nitrado, the serverDZ.cfg is "hidden", so you need to enable "expert mode" in settings,
then go to "expert settings", which is the serverDZ.cfg. Stop the server before making changes this way.)

Upload "novy-sobor-temp-hospital.json" from the extracted files to inside the "custom" folder of the mission directory on your server.
(If you haven't got a "custom" folder, create one.)

Open the cfggameplay.json file in the correct mission file for your server and look for the "objectSpawnersArr" line.

This file tells your server to access your custom file.

Edit it to look like this: 

	"objectSpawnersArr": ["custom/novy-sobor-temp-hospital.json"]	
	
If you already are calling custom jsons to spawn items or buildings, seperate the files like this:

	"objectSpawnersArr": ["custom/novy-sobor-temp-hospital.json","custom/anotherfile.json","custom/differentfile.json"]
	
Save your changes & upload if you need to.

Next we add loot to the structures by adding the following code snippet to the top of your mapgrouppos.xml file, after <map> 

	<!--Novy Sobor Temporary Hospital Loot-->
	<group name="Land_Airfield_ServiceHangar_L" pos="6987.609863 315.570007 8188.339844" rpy="0.000000 4.000000 40.796692" a="49.2033"/>
	<group name="Land_Airfield_ServiceHangar_R" pos="7020.200195 319.131989 8226.080078" rpy="0.000000 3.999999 40.820297" a="49.1797"/>
	<group name="Land_Mil_Tent_Big1_1" pos="7034.839844 319.891998 8225.450195" rpy="0.000000 3.999999 40.795601" a="49.2044"/>
	<group name="Land_Mil_Tent_Big1_2" pos="7027.750000 319.895996 8231.820313" rpy="0.000000 3.999998 37.817287" a="52.1827"/>
	<group name="Land_Medical_Tent_Big" pos="6992.250000 316.071991 8190.839844" rpy="3.999999 0.000000 133.403976" a="-43.404"/>
	<group name="Land_Medical_Tent_Shower" pos="7003.529785 318.026001 8189.649902" rpy="0.000000 4.500000 39.288795" a="50.7112"/>
	<group name="Land_Medical_Tent_Big" pos="7001.399902 316.993988 8200.639648" rpy="-3.499999 0.000000 -48.374298" a="138.374"/>
	<group name="Land_Mil_Tent_Big1_5" pos="7019.950195 318.950989 8221.469727" rpy="0.871171 -4.004990 -143.251999" a="-126.748"/>
	<group name="Land_Mil_Tent_Big1_5" pos="7027.060059 319.029999 8215.929688" rpy="0.871171 -4.004990 -143.251999" a="-126.748"/>
	<group name="Land_Dead_MassGrave" pos="6932.665039 311.731567 8157.374512" rpy="-1.298585 3.503795 0.000000" a="90"/>
	<group name="Land_Castle_Wall1_20" pos="7026.910156 315.797028 8185.850098" rpy="178.999817 86.899841 -140.399918" a="-129.6"/>
	<group name="Land_Castle_Wall1_20" pos="7042.010254 315.907043 8172.709961" rpy="178.999817 86.899841 -140.399918" a="-129.6"/>
	<group name="Land_Mil_Fortified_Nest_Small" pos="7033.358398 319.275635 8198.630859" rpy="-3.508765 -0.111581 -49.466171" a="139.466"/>
	<group name="Land_Mil_Fortified_Nest_Small" pos="7015.872559 317.531250 8179.304199" rpy="-4.137222 -0.357403 -50.690773" a="140.691"/>
	<group name="Land_Roadblock_Table" pos="7024.550781 320.602020 8241.429688" rpy="-0.000000 -0.000000 -139.192490" a="-130.808"/>
	<group name="Land_Misc_Toilet_Mobile" pos="6987.348633 317.545532 8201.237305" rpy="-3.633319 -0.077668 -52.188656" a="142.189"/>
	<group name="Land_Misc_Toilet_Mobile" pos="6988.341797 317.648376 8202.394531" rpy="-3.633318 -0.077616 -52.188656" a="142.189"/>
	<group name="Land_Misc_Toilet_Mobile" pos="7037.240234 320.713989 8216.240234" rpy="3.603989 -0.870766 131.729004" a="-41.729"/>
	<group name="Land_Misc_Toilet_Mobile" pos="7036.029785 320.554993 8214.759766" rpy="3.603569 -0.870669 134.128998" a="-44.129"/>
	<group name="Land_Wreck_Volha_Police" pos="7044.649902 317.653992 8158.399902" rpy="-1.451190 1.772440 108.730988" a="-18.731"/>
	<group name="Land_Wreck_Ikarus" pos="7035.930176 317.461029 8151.385742" rpy="0.487210 -1.920156 -133.431488" a="-136.569"/>
	<group name="Land_Wreck_hb01_aban1_blue" pos="7029.958496 316.365448 8144.143066" rpy="-0.873905 -8.348882 -130.912979" a="-139.087"/>
	<group name="Land_Wreck_hb02_aban2_blue" pos="7026.506836 315.489166 8140.414551" rpy="-0.000000 -0.000000 -149.731720" a="-120.268"/>
	<group name="Land_Wreck_sed01_aban2_white" pos="7023.552734 315.101532 8135.335938" rpy="-0.000000 -0.000000 -177.362579" a="-92.6374"/>
	<group name="Land_Wreck_sed01_aban1_black" pos="7018.164551 314.541290 8129.186035" rpy="-1.012583 -4.311282 -126.004814" a="-143.995"/>
	<group name="Land_Wreck_Volha_Police" pos="7059.470215 319.321991 8174.669922" rpy="-1.451190 1.771880 148.231003" a="-58.231"/>
	<group name="Land_Wreck_sed02_aban2_yellow" pos="7063.129883 319.720093 8178.301270" rpy="-4.953443 4.847556 0.000000" a="90"/>
	<group name="Land_Wreck_sed02_aban2_grey" pos="7067.344727 320.360077 8182.383301" rpy="1.285743 6.682247 41.669979" a="48.33"/>
	<group name="Land_Wreck_sed01_aban1_black" pos="7070.934082 320.942200 8186.849609" rpy="-4.497976 3.038902 0.000000" a="90"/>
	<group name="Land_Wreck_Ikarus" pos="7077.009766 321.863861 8194.849609" rpy="0.792293 -4.769752 -132.838791" a="-137.161"/>
	<group name="Land_wreck_truck01_aban1_green" pos="7041.841797 318.644958 8203.900391" rpy="-3.559631 -0.296345 -54.962780" a="144.963"/>
	<group name="Land_wreck_truck01_aban1_green" pos="7045.971680 319.279022 8209.064453" rpy="-3.838578 -0.244166 -59.958820" a="149.959"/>
	<group name="Land_wreck_truck01_aban1_green" pos="7049.536133 319.654419 8213.037109" rpy="-3.589110 2.424107 -21.656052" a="111.656"/>
	<group name="Land_Farm_WaterTower_Small" pos="7058.833008 326.316772 8237.852539" rpy="-0.000000 -0.000000 133.114975" a="-43.115"/>
	<group name="Land_Misc_Well_Pump_Yellow" pos="7060.038086 321.996460 8237.753906" rpy="-0.000000 -0.000000 36.074306" a="53.9257"/>
	<group name="Land_Wreck_Uaz" pos="7026.289551 319.037231 8193.277344" rpy="-0.573994 2.864888 0.903056" a="89.0969"/>
	<group name="Land_Wreck_V3S" pos="7033.492188 319.761017 8187.041016" rpy="-3.503996 1.281064 -29.033436" a="119.033"/>
	<group name="Land_Wreck_hb01_aban1_police" pos="7037.514648 319.075623 8183.382813" rpy="-0.000000 -0.000000 23.840498" a="66.1595"/>
	<!--End Of Novy Sobor Temporary Hospital Loot-->
	
	
Save your changes & upload if you need to.

Restart your server and the new structures will appear immediatly, and then they will slowly stock with loot.

Thanks, Rob.
