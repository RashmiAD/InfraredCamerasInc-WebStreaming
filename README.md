#Video Streaming

* OSI layers -
    1. Physical Layer
    2. Data Link Layer
    3. Network Layer
    4. Transport Layer
    5. Session Layer
    6. Presentation Layer
    7. Application Layer

* RTP - Real Time protocol
    1. RTP is a Network protocol for delivering audio and video over IP networks.
    2. RTP carries real time content like timestamp and control mechanisms for synchronizing different streams with timing            properties.
    3. RTP runs over User Datagram Protocol (UDP in transport layer) .
    4. RTP is a combination of two parts - 
    
        a. Real Time Protocol (RTP) - It carries real-time data.
        
        b. Real Time Control Protocol (RTCP) - It monitors quality-of-service (QoS) and conveys information about participants.            It is periodic transmission of control packets to all participants in the session. It carries persistent transport-            level identifier for an RTP source called the canonical name or CNAME
    5. Structure of RTP packet -
        
        | IP Header | UDP Header | RTP Header |    RTP Payload    |
    6. There is sequence number for each RTP data packet in order to synchronize at the receiver end, but only the sequence            number isn't sufficient to synchronize we need timestamp as well. Many RTP packets may have same timestamp but                  definitely different sequence number. Best use of timestamp is synchronizing audio and video RTP packets since audio and        video are always transmitted seperately.
    7. Application Level Framing -
        RTP is intended to be malleable (capable of being easily changed) to provide adequate functionality.
        
* Real Time Streaming Protocol (RTSP) -
    RTSP is a network control protocol which uses RTP but has additional control functionalities like setup, play, pause and       teardown the stream. 
