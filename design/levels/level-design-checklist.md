# Level Design Questions

These questions should be reviewed and answered before each level is considered
"complete".

1. How does the environment react to the player's actions?
   - As the player completes levels for various departments, the world becomes
     more "alive", representing the successful migration of workloads to AWS.
   - I.E. The player helps the Legal team set up an Amazon VPC and some
     resources, which then instantiates as "live" workloads running in the
     world.
2. What makes the environment "alive"?
   - The environment should grow as the player completes levels.
   - The environment should be organic...things should go wrong occasionally.
   - Break up the monotony of the core gameplay loop.
3. How is the environment useful/interesting to the user?
   - Use resources like AWS Answers to provide contextual information to the
     user about components running in the environment.
   - Send user messages.
     - _"Hey thanks for the help setting up the site-to-site VPN. We added
       monitoring features. You should check it out!"_
   - Have a kiosk/environment element that shows them info from the
     corresponding AWS best practices.
     - Example:
       [VPN Monitoring Overview](https://docs.aws.amazon.com/vpn/latest/s2svpn/monitoring-overview-vpn.html)
4. Does the level provide a realistic introduction to the problem the player is
   solving?
   - _We need to implement a highly available web application to store an
     employee wiki._
   - _We are going through legal discovery, how can we perform structured
     queries on massive data lakes?_
5. How does the story of the level tie into the main story?
6. Can we identify what the player wants?
7. Can we identify what the player actually needs?
8. Does the player fix something that leads them closer to migration completion?
9. Is it leading the player towards solving the main problem (getting out of the
   game)?
10. Does the level show the practical application of the work being performed?

    - Example: If the player creates an S3 bucket, what are they going to use it
      for?

11. Does the level show the practical solution using the technologies the player
    created?
12. Does the level limit what services are available to the player?

    - This is a must, otherwise its overwhelming.

13. Does the level limit what service properties are available to the player?

    - Example: EC2 instance types.
    - Cost/fraud reduction scenarios.

14. Does the level include humor to draw the player in?
15. What is the risk vs. reward?

    - Failure should have consequences.
      - Example: "Negative Achievements" with tongue-in-cheek descriptions.
      - Example: CHLOE responses (_I wasn't programmed to try that
        approach...because it's bad._).
    - Success should have rewards.
      - Example: Achievements for timely completion, not using hints from CHLOE.

16. How will the level react to the uniqueness of the player's AWS account?

    - If the player has linked their AWS account while in Game Mode, it **can
      and will** have configurations in place that prevent the normal level
      actions from working properly.
    - Example: S3 bucket public access policies, EC2 instance restrictions, IAM
      user policies, and more.
    - Each API call should have an appropriate handler should that specific
      action not work properly because of the player's account configuration.
