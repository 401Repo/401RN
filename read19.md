[Home](https://401repo.github.io/401RN/README)

# Readings: Event Driven Applications   

![Source](https://i1.wp.com/garywoodfine.com/wp-content/uploads/2017/06/EventLoop.jpg)

### Why is access control important?

Access contro denones what a user in the system can do with the data accesible to them: by defining the role of a user within a hirachy we can define their ability to modify the data according to their roles. 

### Describe an application that would need access control.


Most any app: do you have a blog that would save post and treieve the infor from a db? then youd like some users to be able to be guest but not delete the post, but maybe grant them the ability to comment.


### What is a role used for?

Without roles anyone would be able to anything with all the information available: it would be chaos.

### Why is role based access control more scalable than discretionary or mandatory access control?

Discresionary allows an automatic - non involved utilitarian designation of many users without an admin having to grant it unless the new user needs that aditional scruitiny (i.e. a new moderator of a forum is brought on unlike a new user).

>DAC allows for a lot of flexibility and decreases the load on system administrators as users can manage access on their own. On the other hand, it doesn’t provide a high level of security for several reasons:

If user 1 shares access rights with user 2, there’s no guarantee that user 2 needs this access to work or won’t steal or corrupt data or grant access to a malicious user.
It’s impossible to control information flows inside the network.
It’s impossible to enforce the principles of least privilege, need to know, and separation of duties.
 

Because of these limitations, DAC can’t be used by organizations that work with extremely sensitive data (medical, financial, military, etc.). 

 
At the same time, DAC is a good choice for small businesses with limited IT staff and cybersecurity budgets. It allows for sharing information and ensures the smooth operation of the business. This approach, when applied in an organization with 10 to 20 employees, lacks the complexity and oversight challenges associated with the use of DAC in organizations with hundreds or thousands

[source](https://www.ekransystem.com/en/blog/mac-vs-dac)

*Authorization*

the ability of a user to crud in a system.

*Role Based Access Control*

roles of users have associated crud opperations allowed to them

*Capabilities*

can a sure perform crud operations? if yes then they are assigned capabilities if not all of them.

[Home](https://401repo.github.io/401RN/README)