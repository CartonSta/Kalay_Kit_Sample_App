# Sample App  using Kalay SDK

[![N|Solid](http://www.throughtek.com.tw/images/logo_TUTK.png)](http://www.throughtek.com.tw/kalay_overview.html)

The sample demo how to use Kalay SDK to connect a device which integrated Kalay SDK.

# Sample App! based on  TUTK_IOTC_Platform_14W08  &�@TUTK_IOTC_Platform_14W36

  - AVAPIs
  - AVAPIs_Client
  - AVAPIs_Server
  - IOT_Camera
  - IOT_Camera2
  - IOTC_Basics
  - IOTCAPIs_Client
  - IOTCAPIs_Device
  - LED_Switch
  - P2PTunnelAgent
  - P2PTunnelAPIs
  - RDTAPIs
  - TPNS_QuickStart
  
ThroughTek TPNS Quickstart :
  - Based on Google GCM quickstart and modified for ThroughTek TPNS service.
  - How to getting Started
      - You MUST activate your APPLICATION & UID first before using TPNS. (Please contact your account manager for more help.)
      - Register your UIDs to TPNS server.
      - Run the sample on your Android device.
      - Update API_KEY in GcmSender.java, with API key from your project.
      - Send/Push messages from your device via TPNS.
 
You can also:
  - Import and save files from GitHub, Dropbox, Google Drive and One Drive
  - Drag and drop markdown and HTML files into Dillinger
  - Export documents as Markdown, HTML and PDF

### IOTC Platform Release Note

(Legend: '+' means the newly added features,
         'o' means the modified or improved features
         '*' means critical bugs fix
         '-' means the removed features )'
==============================================================================================
[14W36]
  - IOTC Module <1.11.0.0>
    For both IOTC device and client:
		* Fix misjudge NAT type3.
		o Fix crash bug on Win32.
		o Fix re-connection error when do it frequently.
		o Fix choose a not workable Server on TCP mode.
		o Fix login failed when re-query Master failed.
		o Improve connection performance a little bit.
		+ Add support class A/B/C LAN search.
		+ Add IOTC_Setup_LANConnection_Timeout() for setup time to try LAN connection.
		+ Add IOTC_TCPRelayOnly_TurnOn() for setup connection only via TCP relay mode.
		- Remove include platform_config.h

  - AV Module <1.4.5.0>
	For both AV server and client:
		* Fix client connection failed when packet lost.
		o Fix crash bug on Win32.
		- Remove include platform_config.h

  - RDT Module <1.6.0.0>
	For both RDT server and client:
		o Fix re-connection error when do it frequently.
		o Improve RDT_Abort() function call will exit immediately.
		o Improve RDT connection performance.
		+ Add RDT_Create_Exit() for exit RDT_Create() process before reach timeout.
		- Remove include platform_config.h
		 
  - P2PTUNNEL Module <1.3.0.0>
	For both P2PTunnel server and agent:
		o Improve TCP relay mode performance.
		- Remove include platform_config.h

  - Sample Code
	- Remove include platform_config.h

==============================================================================================
[14W08]
  - IOTC Module <1.10.8.0>
    For both IOTC device and client:
		 o Fix big endian bug.
		 o Add memory information in uCOSII.
		 o Fix udp port error.
		 o Improve connecting machanism in uCOSII.
		 o Fix race condition bug in MAC OS.
		 o Improve NAT Type detection.
		 + Support different functional UID.
		 + Add new api IOTC_Set_Device_Name() to set Device Name.
		 + Add new api IOTC_Lan_Search2() to know Device Name in Lan.

  - AV Module <1.4.4.0>
	For AV server:
		 + Add new api avResendBufUsageRate() to know usage rate of resend buffer.

  - RDT Module <1.4.3.0>
	For both RDT server and client:
		 o Improve transmission machanism.
		 
  - P2PTUNNEL Module <1.2.9.0>
    For both P2PTunnel server and agent:
	     o Fix restart bug.
		 o Improve transmission machanism.
		 o Fix LAN search issue under LAN in P2PTunnelServer_Start().
		 o Fix re-bind error.
		 
    For P2PTunnel server:
	     Fix Server restart error.

  - Sample Code
         o Update security certificate mechanism in P2PTunnel sample code for Linux.
		 - Remove auto-disconnecting mechanism in P2PTunnel sample code for Linux.

==============================================================================================
[13W47]
  - IOTC Module <1.10.7.0>
    For both IOTC device and client:
         o Fix socket bind error.
         o Fix variables conflict error.

  - AV Module <1.4.3.0>
    For both AV server and client:
         o Fix variables conflict error.

  - RDT Module <1.4.2.0>
    For both RDT server and client:
         o Improve transmission machanism.
         o Fix variables conflict error.
         - Remove CRC machanism.

  - P2PTUNNEL Module <1.2.8.0>
    For both P2PTunnel server and agent:
         o Fix race condition and deadlock bug.
         o Fix disconnection bug.
         o Fix variables conflict error.

    For P2PTunnel server:
         + Support Lan mode environment.

  - Sample Code
         o Update P2PTunnel sample code for Linux in order to work in LAN mode without Internet.

==============================================================================================
[13W45SB1]
  - IOTC Module <1.10.6.4>
    For both IOTC device and client:
         o Fix error detection in Win32.
         o Fix critical section in uCOSII.
         o Fix Winsock issues in win32 static link.
         o Fix compiler warnings in some arm9 platform.
         + Support Lite UID.
         o Fix LAN connection timeout extends to 1.5s.
         o Fix bugs in receiving data.

  - AV Module <1.4.2.3>
    For AV server:
         o Fix avServStart2() and avServStart3() may blocks.

    For both AV server and client:
         o Fix algorithm of avSendFrameData() on uCOSII. 
         o Fix critical session in uCOSII.
         o Stop usage of AV_ER_EXCEED_MAX_ALARM (-20005).
         o Fix big endian bugs.
         o Add Lite UID support and AV_ER_NO_PERMISSION(-20023) error code.
    
  - RDT Module <1.4.1.5>
    For both RDT server and client:
         o Use call back function instead of polling when reading packets.
         o Fix RDT algorithm in LAN mode to improve performance.
         o Fix compiler warnings in Win32 platform.

  - P2PTUNNEL Module <1.2.7.3>
    For both P2PTunnel server and agent:
         o Fix flow control mechanism. 
         o Fix error detection in Win32.
         o Fix big endian bug.
         + P2PTunnel_SetBufSize() API to set tunnel buffer size to improve performance.
         o Fix buffer control for RTSP/TCP application.

    Known issues:
         1. P2PTunnel agent will not work on a big endian platform.

  - Sample Code
         o Update P2PTunnel sample code for Android to demo the P2PTunnel_SetBufSize() API.
         o Update AVAPI sample code for correct frame rate.

==============================================================================================
[13W26P2]
  - IOTC Module <1.10.6.0>
    For both IOTC device and client:
         + Add IOTC_Set_Partial_Encryption() to control encryption length.
         o Fix NAT type check error to prevent from become RELAY mode after first connection.
         o Fix TCP socket management and error code handling to increase TCP relay stability.
         o Fix variable initialize to prevent from Win32 crashes.
         o Fix network detection return -41 issue.
         * Fix crashes when checking session status.
	 o Fix IOTC_Session_Read() data handling in timeout status.
    For IOTC client:
         o Fix connecting to multi-device may return -19 error code.
         * Fix UDP socket receive buffer size to avoid loss packets.
    For IOTC device:
         * Fix IOTC_Device_Login() will occupy a session ID temporary.
    
  - RDT Module <1.4.1.0>
    For both RDT server and client:
         + Add RDT_Abort() API to close a channel with non blocking mode.
         + Add error code RDT_ER_REMOTE_ABORT for RDT_Write(), 
           RDT_Read(), RDT_Destroy() and RDT_Abort() 
         + Add error code RDT_ER_LOCAL_ABORT for RDT_Write() and RDT_Read().
         + Add error code RDT_ER_CHANNEL_OCCUPIED for RDT_Create(). 
         o Fix CRC error in a Big Endian platform. 

  - P2PTUNNEL Module <1.2.7.0>
    For both P2PTunnel server and agent:
        o Fix TCP socket error code handling to improve P2PTunnel stability.
        o Fix P2PTunnel control command may not be sent correctly to prevent channel is
          kept after disconnected.
    For P2PTunnel server:
        o Fix Big Endian platform will make P2PTunnelAgent_Connect returns -30008 error code.

    Known issues:
        1. P2PTunnel agent will not work on a Big Endian platform.

  - Sample Code
    o Update RDTAPIs sample code for Android.

==============================================================================================
[13W26P1]
  - IOTC Module <1.10.5.0>
    For IOTC client:
         o Fix IOTC_Connect may blocked.
         o Fix IOTC_Connect_ByUID may blocked.
         o Fix multiple calling of connect_byUID() return -19 error.
    For IOTC device:
         o Fix incorrect network detection when WAN port of router is disconnected.
    For both IOTC device and client:
         o Fix relay disconnected issue.
         o Fix inconsistency connection mode between device and client, and cause -42 error code.
         o Fix memory leak issue.
         o Fix IOTC_Session_Write performance and returns -16 issue.
         o Fix incorrect connection packages when connection and disconnection in a short period.
         o Fix keep alive packages transmission mechanism.

  - AV Module <1.4.2.0>
    For AV server:
        o Fix Big-endian algorithm in avSendFrameData().
    For both AV server and client
        o Fix resend mechanism sometimes halt forever and makes client can't receive video data anymore.
        o Improve performance by remove send and receive thread for server and client.
        o Fix argument type error.
        o Fix crash issue.

  - P2PTUNNEL Module <1.2.6.0>
    For both P2PTunnel server and agent:
     o Fix CPU busy issue.
     o Fix large transmission of the same packages.

  - Sample Code
    o Update P2PTunnel sample code to demo the handling method when app goes to background.

==============================================================================================
[13W26]
  - IOTC Module <1.10.3.0>
    For both IOTC device and client:
        o Fix algorithm for NAT type checking function may not called on type 1.
        o Fix error handling algorithm when receive EAGAIN in TCP connection.
        o Fix algorithm to avoid returning IOTC_ER_DEVICE_NOT_LISTENING.
        o Fix bug when data size near max buffer size.
        + Add critical section for uCOSII.
        o Fix log function blocks.
        o Fix better variable type for storing session number.
        o Fix log function cannot be disabled.
        o Fix the handle of TCP packets with header magic error.
        + Add IOTC_Set_Log_Path() to set log file name, path and maximum size.
        + Log error codes in specified file.
        o Fix incorrect returning IOTC_ER_NO_SERVER_LIST when Master is shutdown for a long time.
        o Fix relay connection unstable when use UDP and TCP in different side.
        + Add new platform Arm9_GM8181_3.4.3
        + Add Arm9_Hi3518_4.4.1
        + Arm9_Hi3520A_4.4.1
        + Arm11_SSD1937_4.3.2
        + ArmV5TE_FH8755_4.4.0
        + Mips_Realtek8196E_3.4.6

    For IOTC device
        o Fix algorithm to process P2P packet correctly when device is not listening.
        o Fix IOTC_Device_Login() blocking bug.
        o Fix IOTC_Session_Close() keeps VPG information on device side.

    For IOTC client:
        + Add IOTC_Connect_ByUID_Parallel() and IOTC_Get_SessionID() for supporting to
          connect to device concurrently.
        + Add IOTC_Connect_Stop_BySID() to stop a specific session connecting to device.
        o Fix TCP connection to IOTC server confirmation error.
        o Fix return precise TCP connection error code.

  - RDT Module <1.4.0.0>
    For both RDT server and client:
        o Modify queue process algorithm to improve performance.
        + Add CRC16 mechanism.
        o Fix file pointer leak in log function.
        + Add RDT_Set_Log_Path() to set log file name, path and maximum size.
        + Log error codes in specified file.
        o Modify RDT connection timeout from 10 to 20 seconds.
        o Modify congestion control, dynamic window size and timeout.

  - AV Module <1.4.1.0>
    For AV server
        + Add avServStart3() and avServSetResendSize() for AV re-send supporting.
        o Fix re-send mechanism sometimes halt and cause client can't receive video data anymore.

    For AV client
        + Add avClientStart2() for AV re-send supporting.
        + avClientCleanVideoBuf() to clean video buffer.
        + avClientCleanAudioBuf() to clean audio buffer. 

    For both AV server and client
        o Remove send and receive thread for server and client to improve performance.
        o Avoid avServStart(), avServStart2() and avClientStart() re-assign an
          AV channel ID for a pair of IOTC session ID and IOTC channel ID.
        o Fix avServStart(), avServStart2() and avClientStart() may return wrong channel ID.
        o Fix avDeInitialize() bug.

  - P2PTUNNEL Module <1.2.5.0>
    For both P2PTunnel server and agent:
        + Add P2PTunnel_LastIOTime() to get the last IO time of SID.
        o Fix local socket does not disconnect correctly when remotes side is disconnected.
        o Fix timer bug which causes incorrect waiting interval.
        o Fix bugs of buffer handling at low bandwidth condition.
        o Fix file pointer leak in log function.
        + Tunnel agent add SO_REUSEADDR option except win32.
        o Modify IOTC_Device_Login() stop retry if login failed.
        o Use IOTC_Initialize2() instead of IOTC_Initialize().
        o Check pointer is not NULL before access.
        + Add P2PTunnelAgent_Set_Log_Path() to set log file name, path and maximum size.
        + Log error codes in specified file.

  - Sample Code
    o Update AVAPI sample code for Linux to demo new APIs.

==============================================================================================
[13W10]
  - IOTC Module <1.9.1.0>
    For IOTC device:
        + Add error code IOTC_ER_NO_SERVER_LIST for IOTC_Device_Login().
        o Fix continue notify when login status changed.

    For IOTC client:
        + Add IOTC_Lan_Search().
        + Add error code IOTC_ER_DEVICE_MULTI_LOGIN for IOTC_Connect_ByUID() and IOTC_Connect_ByUID2().
        + Add error code IOTC_ER_NO_SERVER_LIST for IOTC_Connect_ByUID() and IOTC_Connect_ByUID2().
        + Add error code IOTC_ER_INVALID_ARG for IOTC_Lan_Search().
        - Remove IOTC_Connect_ByName and IOTC_Connect_ByName2 APIs.

    For both IOTC device and client
        + Support Arm9_Hi3531_4.4.1 platform.
        + Support Mips_RalinkRT3352_3.4.2 platform.
        o Fix bug for getting local ip address.
        o Change IOTC_ER_NO_TCP_SUPPORT to IOTC_ER_NO_PERMISSION for advance UID identification.
    
  - AV Module <1.3.1.0>
    For AV server:
        + Add avServSetDelayInterval() for setting packets delay time of video frames.
        o Fix memory leak in avServStop().
        o Fix memory leak in avSendFrameData().

    For AV client:
        + Add new mechanism for receive frame function: avRecvFrameData2().
        + Add avClientCleanBuf() to clean audio and video buffer.
        * Fix avCheckAudioBuf() may returns wrong audio frames count.
        o Fix memory leak in avClientStop().

    For both AV server and client:
        o Fix the bug of avSendIOCtrl() returns AV_ER_SENDIOCTRL_ALREADY_CALLED after avSendIOCtrlExit() called.

  - P2PTUNNEL Module <1.2.0.0>
    + All new P2PTUNNEL module, NO backward compatible
    + Support authentication
  
  - Sample Code
    o Separate device and client of IOTCAPIs Android sample code.
    + Add IOTC_Lan_Search() demo in IOTCAPIs Android sample code.
    + Add P2PTUNNEL samples for Androd, iOS, Linux, MAC and Win32
	
==============================================================================================	
[12W51]
  - IOTC Platform
    + Support TCP80 in IOTC server (Requires Server Program advanced version V0.5.2.0 and above)
    + Add blacklist and whitelist mechanism in IOTC server
    + Add user manual: AV module service type and IO control reference guide

  - IOTC Module <1.8.5.0>
    + Support TCP80
    + Support iOS6
    + Add error codes for blacklist and whitelist mechanism
    + Add a mechanism to check session status by callback: IOTC_Session_Check_ByCallBackFn
    + Add error code IOTC_ER_FAIL_CREATE_SOCKET, IOTC_ER_FAIL_SOCKET_OPT, IOTC_ER_FAIL_SOCKET_BIND,
      IOTC_ER_NOT_SUPPORT_RELAY returned by IOTC_Connect_ByUID(), IOTC_Connect_ByUID2(),
      IOTC_Connect_ByName() and IOTC_Connect_ByName2()
    + Support Mips_Realtek8196C_3.4.6
    + Support Mips_Realtek8196D_4.4.5
    + Support Mips_RalinkRTF5350_3.4.2
    + Support ARM9_GM8126_4.4.7
    + Support ARM9_N32905U1DN_4.2.1
    - Delete ARM9_GM8126_3.4.6
    - Delete MIPS_RalinkRT5350_4.3.3
    - Remove error code IOTC_ER_FAIL_CREATE_SOCKET, IOTC_ER_FAIL_SOCKET_OPT,
      IOTC_ER_FAIL_SOCKET_BIND from IOTC_Initialize() and IOTC_Initialize2()
    o Fix IOTC_Connect_ByUID() issue in multi-thread usage
    o Fix connection issue for second time IOTC_Initialize() after IOTC_DeInitialize()
    o Change the algorithm of random port generation
    o Improve LAN search successful rate
    o Improve the speed of detection whether network is reachable
    o Modify relay not to be established again with already connected UID 
    o Add const modifier for input parameters in function prototype

  - AV Module <1.2.8.1>
    o Add const modifier for input parameters in function prototype

  - RDT Module <1.3.7.0>
    o Improve RDT transfer rate
    o Add const modifier for input parameters in function prototype

  - Sample Code
    o Fix missing invocation of avServStop() and avClientStop() when using avServStart() and
      avClientStart(), respectively

==============================================================================================
[12W33]
  - IOTC Platform
    + Add watchdog mechanism in IOTC server
    o Change diagnostic mechanism in IOTC server by using native file system

  - IOTC Module <1.7.0.0>
    + Add APIs to support both non-secure and secure mode: IOTC_Listen2(), 
      IOTC_Connect_ByUID2() and IOTC_Connect_ByName2()
    + Add a mechanism to get login status by callback: IOTC_Get_Login_Info_ByCallBackFn()
    + Add error code IOTC_ER_NOT_INITIALIZED returned by IOTC_DeInitialize()
    o Improve device login and client connection time more quickly
    o Return IOTC_ER_NETWORK_UNREACHABLE in IOTC_Device_Login() when network is unavailable
    o Change the error code IOTC_ER_UNKNOWN_DEVICE returned by IOTC_Connect_ByUID()
      to IOTC_ER_SERVER_NOT_RESPONSE for clarification purpose
    o Change the error code IOTC_ER_TIMEOUT returned by IOTC_Connect_ByXXX() to
      IOTC_ER_FAIL_SETUP_RELAY for clarification purpose
    o Fix memory leak caused by IOTC_Device_Login() fails
    - Remove error codes: IOTC_ER_SENDTO_FAILED, IOTC_ER_DEVICE_NOT_LOGIN
      IOTC_ER_DEVICE_NOT_SECURE_LISTEN

  - RDT Module <1.3.5.0>
    + Add error code RDT_ER_RCV_DATA_END for RDT_Read() to indicate remote site
      has destroyed the RDT channel
    o Re-arrange error codes to distinguish from the ones defined by IOTC modules
    o Modify API name from RDT_Set_Max_Session_Number() to RDT_Set_Max_Channel_Number()
      for unifying naming rule
    - Remove error codes: RDT_ER_INVALID_ARG, RDT_ER_IOTC_SENDTO_FAILED,
      RDT_ER_IOTC_SESSION_CLOSE_BY_REMOTE, RDT_ER_IOTC_REMOTE_TIMEOUT_DISCONNECT,
      RDT_ER_IOTC_CH_NOT_ON

  - AV Module <1.2.8.0>
    + Add deinitialization function: avDeInitialize()
    + Add error code AV_ER_CLIENT_NO_AVLOGIN returned by avSendAudioData()
    o Re-arrange error codes to distinguish from the ones defined by IOTC modules
    o Change the error code AV_ER_BUFPARA_MAXSIZE_INFUFF to AV_ER_BUFPARA_MAXSIZE_INSUFF

  - Sample Code
    + Add iOS / Android application framework for easier development - Advanced only

