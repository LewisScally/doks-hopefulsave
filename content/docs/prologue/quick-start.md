---
title: Specifications
description: One page summary of how to start a new Doks project.
lead: One page summary of how to start a new Doks project.
date: '2020-11-16T13:59:39+01:00'
lastmod: '2020-11-16T13:59:39+01:00'
draft: false
images: []
menu:
  docs:
    parent: prologue
weight: 110
toc: true
---
## Specifications

Initial connections are normally p2p, with Lunar Chat we can ensure Hop 2 Hop, meaning that when you connect to a call, you do not connect to that user but instead the server which hosts Lunar chat. Or in the case of purchasing a custom license, your own server instance, or even local server. L chat can be setup on a local network, or deployed to the cloud and accessible globally. Hop 2 hop ensures that, only the security of the server/host, and those maintaining it are in question regards to who may view calls and potential info. By enabling End to End encryption, even if the host server or local network were to be compromised, any information pertaining calls would be undecipherable.

## Feature Outline

*   Two-Way Audio & Video

*   Audio Calls

*   Muting

*   Video Conferencing

*   Screenshare

*   Page embed*, Youtube sharing*, Session recording*

*   Slideshow, and presentation media embed*

*   Attendee Management - Set Password, enable lobby, pay gate*, and  Set Usernames*

*   Meeting Initiation, share and join management

*   Private Text Chat

*   Instant Messaging

**\*Available at additional cost to business users, included in certain customisation packages, see pricing.lchat.co.uk**

## Security

All meeting rooms are ephemeral: they only exist while the meeting is actually taking place.

```bash
P2P mode is only used for 1-to-1 meetings. In this case, audio and video are encrypted using DTLS-SRTP all the way from the sender to the receiver, even if they traverse network components like TURN servers.
```

In the case of \*\*multiparty meetings, all audio and video traffic is still encrypted on the network (again, using DTLS-SRTP). Packets are decrypted while traversing Jitsi Videobridge; \*\*however, they are never stored in any persistent storage and only live in memory while being routed to othe participants in the meeting.

## In-Depth Specifications

*   Comprehensive meetings features in every plan

*   Video Experiences

*   Audio sharing	Users can share system audio in a meeting from a device or browser tab

*   Bandwidth controls	Users can monitor their connectivity quality and adjust their video bandwidth

*   Configure, enable and disable features	Configure, enable, and disable features to build the experience you want end users to have

*   Controller mode	The ability for any participant (not just the host) to mute, control volume or remove other participants in meeting

*   Dominant speaker indication	Indicates who is the dominant speaker at any given point in time

*   Group chat	Send messages to every video meeting participant

*   HD Audio	Opus Codec

*   HD Video	Ability to support 720p video

*   In-meeting connection indications	Show information about connections status, such as bitrate, packet loss, resolution, frame rate and estimated bandwidth

*   Phone access to meetings *

*   Private chat	Send private messages to individuals in a video meeting

*   Push to talk mode	Mode in which all speakers stay muted unless they press the spacebar key to speak

*   Raise your hand	Participants can discreetly indicate they have something to say without interrupting the current speaker

*   Remote desktop control through electron integrations	Control the mouse and keyboard movements of another user remotely through electron integrations

*   Screen sharing	Share your computer screen and choose which applications or monitors to display	✓

*   Smart layout	Dynamically control app layout and display based on audio activity. Automatically or manually switch between tile and stage view, automatically focus on any participant and manage screen sharing

*   Your brand experience	Brand the experience with your company information. No 3rd party branding, Ondevs, L Chat or otherwise.

*   YouTube Video Sharing	Users can share a YouTube video for everyone in the conference to see

*   Meetings as a Service Platform

*   End-to-End Encryption for video meetings	True end to end encryption even with videobridge for desktop video meetings

*   GDPR requirements for data processors	GDPR compliant for data processors	✓

*   Highly available massively scaled global infrastructure	Real-time automatic scaling of compute capacity to ensure the right capacity is always available

*   HIPAA Compatible. HIPAA compatible and can provide a BAA. It is incumbent upon users to operate the technology in a HIPAA compliant manner.

*   Industry-leading Service Levels	99.99% Platform Uptime SLAs

*   Localization of interfaces	Record the audio, video, and screen share from a meeting. Save it to reference later or to send to those who could not attend.

*   Open and industry standard encryption	Encryption using DTLS-SRTP to secure video

*   Secure passcodes	The ability to set a passcodes to provide an additional layer of security

*   Webhooks	Configure, enable, and disable features to build the experience you want end users to have

## Technical Limits

###### 256 concurrent connection. Unlike Zoom it is possible to manage 256 video and audio guests to a conference. There will however be technical limits on the individual users hardware. For services where interaction of all participants is necessary, we can configure this as a custom solution to hand 1000 users to occupy the same room. If it is then desired to share the conference to viewers who have no audio or video input. We can configure this with modern day streaming providers to stream to more than 100 million users at one time.

## Test Results - Security

*Best in class for security, British based, secure technology, more secure than competitors*

***The Most secure way to operate our service is too disable streaming and recording, this is done by default on public access Lchat.co.uk then selecting in the settings 'Enable End to End encryption'***

## Comparison with zoom

Zoom currently offer no means of End to End encryption. **- *it might be considered military grade, but we believe security is important***

Available on your own secure server unlike zoom

No 40 min call limit unlike zoom

British unlike zoom

Actively utilises, and contributes to opensource

15% profit goes to opensource plus voluntary staff hours

## **Unbeatable Analytics**

Safe statistical reporting. Get in depth business info on your calls, without compromising any personal information. Through innovative analytical reporting.

Reports for the following statistics (and more):

*   Number of threads used by the JVM.

*   Current bitrate, packet rate, and packet loss rate.

*   Current number of audio and video channels, and conferences.

*   Current estimated number of video streams.

*   The size of the largest conference in progress.

*   The distribution of the sizes of the conferences currently in progress.

*   Aggregates of RTT and jitter across all users.

*   The total number of created, completed, failed and partially failed conferences.

*   The total number of messages sent and received through WebRTC data channels and COLIBRI web sockets.

*   The total duration of all completed conferences.

*   The number of ICE sessions established over UDP or TCP.

## In Depth Look at stat reporting

*   current_timestamp - The value is the date and time when the statistics are generated (in UTC).

*   threads - The number of Java threads that the video bridge is using.

*   bit_rate_download / bit_rate_upload - the total incoming and outgoing (respectively) bitrate for the video bridge in kilobits per second.

*   packet_rate_download / packet_rate_upload - the total incoming and outgoing (respectively) packet rate for the video bridge in packets per second.

*   loss_rate_download - The fraction of lost incoming RTP packets. This is based on RTP sequence numbers and is relatively accurate.

*   loss_rate_upload - The fraction of lost outgoing RTP packets. This is based on incoming RTCP Receiver Reports, and an attempt to subtract the fraction of packets that were not sent (i.e. were lost before they reached the bridge). Further, this is averaged over all streams of all users as opposed to all packets, so it is not correctly weighted. This is not accurate, but may be a useful metric nonetheless.

*   rtp_loss - Deprecated. The sum of loss_rate_download and loss_rate_upload.

*   jitter_aggregate - Experimental. An average value (in milliseconds) of the jitter calculated for incoming and outgoing streams. This hasn't been tested and it is currently not known whether the values are correct or not.

*   rtt_aggregate - An average value (in milliseconds) of the RTT across all streams.

*   largest_conference - The number of participants in the largest conference currently hosted on the bridge.

*   conference_sizes - The distribution of conference sizes hosted on the bridge. It is an array of integers of size 15, and the value at (zero-based) index i is the number of conferences with i participants. The last element (index 14) also includes conferences with more than 14 participants.

*   audiochannels - The current number of audio channels.

*   videochannels - The current number of video channels.

*   conferences - The current number of conferences.

*   participants - The current number of participants.

*   videostreams - An estimation of the number of current video streams forwarded by the bridge.

*   total_loss_controlled_participant_seconds -- The total number of participant-seconds that are loss-controlled.

*   total_loss_limited_participant_seconds -- The total number of participant-seconds that are loss-limited.

*   total_loss_degraded_participant_seconds -- The total number of participant-seconds that are loss-degraded.

*   total_conference_seconds - The sum of the lengths of all completed conferences, in seconds.

*   total_conferences_created - The total number of conferences created on the bridge.

*   total_failed_conferences - The total number of failed conferences on the bridge. A conference is marked as failed when all of its channels have failed. A channel is marked as failed if it had no payload activity.

*   total_partially_failed_conferences - The total number of partially failed conferences on the bridge. A conference is marked as partially failed when some of its channels has failed. A channel is marked as failed if it had no payload activity.

*   total_data_channel_messages_received / total_data_channel_messages_sent - The total number messages received and sent through data channels.

*   total_colibri_web_socket_messages_received / total_colibri_web_socket_messages_sent - The total number messages received and sent through COLIBRI web sockets.
