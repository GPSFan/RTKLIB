This is a fork of two forks. Does that make it a spoon?

No, "There is no spoon".

The original being Windoze centric for the GUI, I took the best of Jens Reimann's Qt port
and the best of Tim Everett's RTKExplorer Demo5 enhancements to Tomoji Takasu's 2.4.3 b27 branch
and combined them into this repo. 
As I have neither capability nor desire to rebuild the Windoze GUI code, don't rely on this repo for that, use
RTKExplorer. There is nothing in the RTKLIB part of this repo that isn't in RtkExplorer.
If you need a pure Qt port of Tomoji Takasu's original, use Jens's repo.
Other repo's like emlid's, drotek's and some 400 others,... you are on your own, good luck.

If you need a Qt port of RTKExplorer, you have come to the right place.
You do not need any sort of propritary compiler to build the Qt stuff. Just Qt Creator.
But, it won't build the original's Windoze Gui .exe files. I've tried to maintain their
integrity (RTKExplorer wise that is), but no guarantees, and for that you will need the
Embarcadero C++ Builder that you have to pay for.

Many of my commit messages attribute to me. That's because of the way I updated the code. I also
cherry picked a lot of commits which did retain their attributions. Most of what I committed
should be attributable to either Tim or Jens.

I've also removed the building of rtkvideo_qt and rtkvplayer_qt as I was never able to get my Qt install
to have the right multimedia stuff. The code is still there and maintained as is Jens', I just
don't build them.

#
#  RTKLIB 2.4.3 Betas
#

DESCRIPTION

The development branch for RTKLIB 2.4.3.



UPDATE HISTORY

2014/09/07  2.4.3 b1  add 3-panel and veritical-panel modes for RTKNAVI
                      add sky image overlay to skyplot for RTKPLOT
                      fix invalid identification of obs type "C2" (#113)
                      fix invalid format of saved image by RTKPLOT (#114)
2014/10/21  2.4.3 b2  add pos2-bdsarmode for beidou amb-res option
                      add beidou amb-res option for rtknavi and rtkpost
                      support stdin/stdout if -in/-out omitted in str2str
                      strtok() -> strtok_r() in expath() for thread-safe
                      fix problem on week rollover in rtcm 2 type 14
                      fix problem on reading "C2" in rinex 2.12
                      fix bug on clock error variance in peph2pos()
                      fix bug on P0(a[3]) computation in tide_oload()
                      fix bug on m2 computation in tide_pole()
                      fix bug on receiver option -GL*,-RL*,-JL* for javad
                      fix bug on receiver option -GL*,-RL*,-EL* for novatel
2014/10/24  2.4.3 b3  fix bug on beidou amb-res with pos2-bdsarmode=0
                      fix bug on return of var_uraeph() if ura<0||15<ura
2014/11/08  2.4.3 b4  fix getconfig error (87) with bluetooth device
                      fix bug on ar-degradation by unhealthy satellites
                      support qzss navigation subframes by decode_frame()
                      add receiver option -RT_INP for rtcm3
                      support message RXM-RAWX and RXM-SFRBX for u-blox
                      add option -a, -i and -o for str2str
                      merge updates of src/rcv/rt17.c (pull-req #45)
2014/11/09  2.4.3 b5  support glonass, qzss and beidou for skytraq
2016/01/23  2.4.3 b6  merge 2.4.2 p11 bug fixes
                      update ppp/ppp-ar features
                      support septentrio
2016/01/26  2.4.3 b7  fix bugs #126,#127,#128,#129,#130,#131
2016/01/28  2.4.3 b8  support galileo navigation data in u-blox RXM-SFRBX
2016/05/10  2.4.3 b9  unsupport ppp-ar features
2016/05/25  2.4.3 b10 fix several bugs
                      update data/TLE_GNSS_SATNO.txt
                      repository for RTKLIB/bin is moved to new RTKLIB_bin to
                      reduce repository size.
                      septentrio.c is updated by Apr 6 ver by JensReimann.
2016/06/12  2.4.3 b11 fix several bugs
                      support solution ground track pane in rtknavi
                      support gpx conversion function to rtkpost and pos2kml
                      support shapefile in rtkplot
                      add data/ubx_m8p_ref_glo/bds_1hz.cmd
2016/06/21  2.4.3 b12 support GPX format as waypoints of RTKPLOT
                      add menu Map Layer of RTKPLOT
                      support solution status format as input of RTKPLOT
                      support solution status format as output of RTKNAVI
2016/07/19  2.4.3 b13 support IRNSS
                      support RINEX 3.03
                      add src/rcv/cmr.c
                      add half-cycle vaild check for ublox ubx-trk-meas
                      add leap second before 2017/1/1 00:00:00
                      support averaging single pos as base position
2016/07/22  2.4.3 b14 fix a fatal bug for baseline analysis
2016/07/29  2.4.3 b15 merge Qt port by JensReimann
                      add output of received stream to tcp port for serial
                      nename api compress() -> rtk_uncompress()
                      nename api crc16()    -> rtk_crc16()
                      nename api crc24q()   -> rtk_crc24q()
                      nename api crc32()    -> rtk_crc32()
2016/07/31  2.4.3 b16 fix several bugs
                      improve draw speed of gis data in rtkplot
                      add tcp output option of input stream from serial output
                      add command of serial output
                      add out-outsingle, out-maxsolstd options
                      add commands for u-blox M8P
2016/08/20  2.4.3 b17 fix several bugs
                      merge pull request #180
                      merge pull request #199
                      merge pull request #206
                      binary ap compiled by C++ builder 10.1 Berlin
                      add ap rtkpost_win64, rtknavi_win64, rnx2rtkp_win64
                      add ap rtkpost_win64, rtknavi_win64, rnx2rtkp_win64
2016/08/20  2.4.3 b18 fix #134 (loss-of-lock not recognized in RTCM MSM 6 or 7)
2016/08/29  2.4.3 b19 add option -STD_SLIP for u-blox receiver driver
                      fix on half-cyc valid for sbas in u-blox trkmeas
                      update kelper terminate condition for alm2pos(),eph2pos()
                      fix bug on week overflow in time2gpst(),gpst2time()
                      fix bug on starting serial thread for windows
                      fix bug on mark and path in Google Earth view of RTKPLOT
                      add protocol analysis in input stream monitor of STRSVR
                      add window size extension of RTKPOST and RTKCONV
2016/09/03  2.4.3 b20 add ntrip caster functions
2016/09/05  2.4.3 b21 fix several bugs
2016/09/06  2.4.3 b22 fix several bugs
                      add app/str2str/run_cast.sh for ntrip caster control 
2016/09/06  2.4.3 b23 fix several bugs
                      add -sys option for rnx2rtkp
                      add 4- and 5-panel modes for rtknavi
2016/09/19  2.4.3 b24 fix several bugs
                      change api rtksvrstart()
                      add minimized panel mode of rtklaunch
                      add relay back message of output streams to strsvr
                      add option -b to str2str
                      support multiple remote console connections by rtkrcv
                      add option -w to rtkrcv
2016/09/25  2.4.3 b25 fix several bugs
                      add ap rtkvideo
                      add ap rtkvplayer
                      change build environment to C++ builder 10.1 Berlin
2016/10/01  2.4.3 b26 fix several bugs
                      change api rtksvrstart(), strsvrstart()
                      support udp server and client for stream types
                      support periodic receiver commands by rtknavi, strsvr
2017/04/25  2.4.3 b27 fix several bugs
