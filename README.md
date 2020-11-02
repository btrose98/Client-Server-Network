# Client-Server-Network
Chat server that allows users to create and join group chats to exchange messages

This was completed for the purposes of Assignment 1 for CEG 4188 - Higher Layer Network Protocols at the University of Ottawa.
Assignment partner: Jason Smith, https://github.com/JasonSmith03

The purpose of this assignment was to introduce us to socket programming API. The assignment was implemented using Python2 and tested in a Linux terminal.
Client-Server Network is a simple application that connects users over a network: a chat server. The chat server allows users to converse in different channels. Users can create and join channels; once a user is in a particular channel, all messages that he/she sends will be relayed to all other users in that channel. If a user joins or leaves a channel, all users in that existing channel are notified of the action. A user is only allowed to be in one channel at a time.

Testing Notes:

  client.py should be started using the following command line arguments: $python2 client.py name ipAddress portNumber 
                                                                           
                                                                           For example:   $python2 client.py Bradley 127.0.0.1 55555
  
  /create <channel name> : User is attempting to create a new channel.
  
    Checks to see if there is an already existing channel with that name. If the channel already exists, then the user is informed that the channel cannot be created and is         asked to perform a new action. If the channel does not exist, the new channel is created and the user is then placed in that channel.
  
  /join <channel name>: User is attempting to join an already existing channel.
  
     Checks to see if there is an existing channel with that name. If the channel exists, then the user is removed from their current channel and moved into the new specified        channel. Everyone in the original channel is notified that the user has left the channel, while everyone in the new channel is notified that the user has joined the            channel. If the channel does not exist, then the user is notified that the channel does not exist and prompts them to create the specified channel or select a new action.
  
  /list:  Displays all current available channels that the user can join.
    
