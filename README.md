# A-JMS-Consumer-and-Producer-client
A maven based JMS queue Consumer and Producer java client which uses Jboss-Eap 7.2.0. ( Please go through Readme file to configure JMS queues/topics in JBOSS EAP 7.2.0)

1. First thing first to able to consume/produce jboss jms queue/topic, an application user must needs to be created with "guest" user-role.
(Otherwise SSL handshake error will be thrown).


2. Rename the standalone-full.xml to standalone.xml and standalone.xml to standalone-old.xml as standalone-full.xml consists of all the J2EE subsystems (for JMS JBOSS-EAP uses activemq server.).


3. Though creating new queues/topics is easy from GUI but it can be created directly from standalone.xml as well. just add your queue details as follows (here test queue ):
                <jms-queue name="TestQueue" entries="java:jboss/exported/jms/queue/test queue/test" durable="true"/>
   
   Pay attention : entries="java:jboss/exported/jms...    part  is important to add in entries from GUI/standalone.xml.
