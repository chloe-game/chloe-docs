# Gameplay Features

## In-Game Assistant (CHLOE)

The in-game assistant, CHLOE, acts as a source of information, hints,
instructional material, and resource generation. Within the simulation, CHLOE is
rendered as a wireframe cat. As a post-release effort, CHLOE will support
redeemable codes to unlock additional CHLOE wireframes (other animals, fantasy
creatures, and so on). When the user interacts with CHLOE, several options are
available.

Yes, the player can pet the cat.

One of the most popular examples of a similar character is
[Cortana](<https://en.wikipedia.org/wiki/Cortana_(Halo)>) from the _Halo: Combat
Evolved_ series. A "ride-along" character can be critical in guiding and
teaching players, as well as establishing a sense of identity through their
relationship and dialogue.

Humans regularly anthropomorphize inanimate and non-human entities so that they
can identify with and relate to them
([source](https://psychcentral.com/news/2018/03/01/why-do-we-anthropomorphize)).
This occurs often in media and entertainment, but equally often in peoples'
every-day lives. Examples include
[house cleaning devices](https://www.wired.com/story/roomba-robot-consciousness-enlightenment/),
[plants](https://www.wired.com/story/roomba-robot-consciousness-enlightenment/),
[cars](https://www.wdsu.com/article/more-than-40-percent-of-people-name-their-vehicle-do-you/23567311),
and more.

The full acronym, Cloud Hosting and Learning Optimization Environment,
emphasizes itself as a solution to the challenge players experience trying to
achieve specific, targeted learning objectives that prevent them from moving
forward with a specific problem. CHLOE enables players to achieve their learning
objectives quickly so that they can grow and build in the cloud.

CHLOE acts as a guide. She is responsible for guiding and developing players
through their experience, and provides additional context throughout the game
story. Translated literally, the name refers to new spring growth. In this vein,
CHLOE helps grow and develop players throughout their cloud journey.

When working in the game and interacting with CHLOE, the player has the option
of performing the following actions.

### _What is this for?_

When holding a resource entity, the user can choose this option to see and/or
hear an explanation of what the resource is, what purpose it serves, and how
players are using it on AWS. This can be presented in a number of ways,
including streaming video, text, or audio. The initial effort will focus on
streaming a related video from AWS' YouTube channel. Should this introduce
problems, learning content can be packaged as part of the application
installation.

### _How do I?_

When selecting this option, the player can choose from a list of available
scenarios (such as _How do I...create a static website with CloudFront
integration?_). These tasks are simple in nature (examples below). The purpose
of this feature is to quickly explain to a user how to create some resource type
with a predefined configuration.

- _How do I... → Create a static website bucket with redirects and CORS?_
- _How do I... → Add an Availability Zone to a load balancer?_

When a _How do I_ task is chosen, an on-screen animation will begin. The
animation will show CHLOE launching the needed resources and configuration to
create the proposed architecture. The resources will not be instantiated in any
linked account(s).

After the demonstration completes, the player has the option to modify the
configuration of each involved resource and launch them. From the game engine
perspective, the AWS resources are created with some default configuration as
specified by the workload, but they are not launched yet. The player must choose
to launch them after viewing the configuration.

### Resource Launch, Update, and Terminate Actions

After the user launches, updates, or terminates an AWS resource, CHLOE acts as
the driver for the action by performing an animation relevant to the action and
resource type.

## Visual Parameters

A common feedback item from players learning AWS has been that the myriad
configuration options and data available to them in the AWS Management Console
has been overwhelming at best. Specifically, the UI of CHLOE must be simple, but
convey important data in a clear and meaningful way.

One way to accomplish this is to reduce text usage wherever possible, opting
instead for visual representation of different configurations and states. Using
position, scale, color, animation, sound, and other characteristics (with
accessibility still in mind), information currently conveyed as text can be
represented in other ways that can be more intuitively viewed and modified by
the player.

As an example, [VRHuman.com](http://vrhuman.com/) (owner: Vladimir Ilic),
demonstrates a collection of VR assets such as buttons, sliders, and knobs for
use in VR applications. This can be viewed
[here](http://www.vrhuman.com/portfolio/vr-asset-essentials-switches-levers-buttons/).

For example, Amazon S3 bucket properties explain some of the potential for
creating "visual parameters"

- `AccelerateConfiguration` is represented as a switch (on or off).
- `AccessControl` is represented as a dial with the supported options.
- `ObjectLockEnabled` is represented as a lock object that can be closed
  (`true`) or opened (`false`).
- `PublicAccessBlockConfiguration` is represented as several buttons that can be
  pressed to enable different access settings.

## Simulation Mode

The heart of the visualization component of CHLOE is Simulation Mode. The user
is free to create and configure live AWS resources in real-time. In a sense,
Simulation Mode turns AWS infrastructure engineering into a first-person/VR
experience. Ultimately, CHLOE would allow builders to do their day to day job
within a 3D world.

Simulation mode can be used both for building live AWS resources as well as
visualization and construction of 3D architecture diagrams. Players will have
the option to disable linking to AWS accounts, which disables the corresponding
AWS API actions.

## Resource State Data Collection

When a user first starts CHLOE, they will be prompted to connect to one or more
AWS accounts. If not done so already, the player must deploy an instance of the
backend data aggregation infrastructure. This infrastructure is responsible for
collecting resource state information and aggregating it into a format that
CHLOE can query regularly to perform in-game state updates (adding newly created
resources, updating resource info, deleting old resources, etc.).

AWS account linking will be supported for individual accounts or accounts that
are part of an organization in AWS Organizations.

This has to be as close to free for the player as possible, while still being
reasonably fast. Players will not want to wait 30 minutes for CHLOE to know what
is in their account.

## First-Person Camera/Controls

Users will navigate via first-person. Movement/navigation/flight will follow
common conventions for first-person games.

## VR Camera/Controls

Users will navigate via a head-mounted display (HMD).

- Movement/navigation/flight will be supported using hand controls.
- Movement/navigation/flight will also support using full-body VR platforms
  (example: [Omni by Virtuix](https://www.virtuix.com/)).

## AWS Credentials Integration

When playing game levels, AWS integration is disabled. This is to remove the
need for players to pay for running AWS resources while learning.

When playing in Simulation Mode, AWS credentials can be optionally included to
sync the local environment with one or more AWS accounts.

Direct entry of access key ID/secret access key pairs will not be supported for
security concerns.

## AWS Service Support

The initial supported AWS services are listed below.

- Amazon Simple Storage Service (Amazon S3)
- AWS Identity and Access Management (IAM)
- Amazon Virtual Private Cloud (Amazon VPC)
- Amazon Elastic Compute Cloud (Amazon EC2)
- AWS Auto Scaling
- AWS Lambda
- Amazon DynamoDB
- Amazon Relational Database Service (Amazon RDS)
- Amazon Simple Notification Service (Amazon SNS)
- Amazon Simple Queue Service (Amazon SQS)
- Amazon CloudWatch

The remaining AWS products and services will be posted in a public-facing
roadmap where players can add support for specific services/resources.

## Ongoing/Patch Support

Due to the rapid pace of AWS service and feature releases, CHLOE will support
end-user client patching. Due to the potential increased cost and complexity of
building a standalone client, initial preference will be given to using existing
clients like Steam.

## Resource Creation

Resources will be instantiated within CHLOE by the user through the user
interface.

1. The user opens the resource selection menu.
2. The user navigates a list of supported AWS services and selects a resource to
   create.
3. The resource entity is placed in the player's control and enabled for
   interaction.
4. The user selects the resource configuration menu.
5. The user selects the desired configuration for the resource.
6. The user moves the resource to their preferred location.
7. The user confirms creation of the resource.
8. The resource creation request is sent to the configured AWS account.
9. CHLOE performs a creation animation.
10. Success/failure response is monitored by CHLOE.

## Resource Updates

Resources can be updated by the user. Live resources are updated in the linked
AWS account.

1. The user selects an existing resource in the environment.
2. An information pane appears in the UI listing existing resource configuration
   details.
3. The information pane fields are editable for service properties that support
   in-place updates.
4. The user edits one or more fields.
5. The user selects the **Update** option.
6. CHLOE performs an update animation.
7. The resource update request is sent to the configured AWS account.

## Resource Deletion

Resources can be deleted by the user. This triggers deletion of the resource in
the linked AWS account.

1. The user selects an existing resource.
2. An information pane appears in the UI listing existing resource configuration
   details.
3. The user selects the **Terminate** option.
4. The user reviews any warnings and confirms deletion.
5. CHLOE performs a termination animation.
6. The resource delete request is sent to the configured AWS account.
7. On resource deletion success, the entity is removed from the scene.
8. On resource deletion failure, the entity enters a corrupt state.
9. CHLOE notifies the user of the failed resource deletion.

## AWS Resource Errors

On create, update, delete requests, the corresponding AWS API action may succeed
or fail. The user should be notified in an appropriate manner when action must
be taken.

- On resource creation success, a success animation is invoked on the entity.
- On resource creation failure, a failure animation is invoked on the entity.
  - CHLOE notifies the user of resource creation failure.
  - On selecting the failed resource, the user is provided failure information
    from the AWS API response.
  - The player is given an option to update resource parameters and retry
    creation.
  - This follows the same workflow as **Resource Updates**.
- On resource update success, a success animation is invoked on the entity.
- On resource update failure, a failure animation is invoked on the entity.
  - CHLOE notifies the user of resource update failure.
  - If the resource is successfully rolled back by AWS to a known good state, a
    warning animation is invoked on the entity.
  - If the resource is not successfully rolled back by AWS to a known good state
    (or cannot be), a failure animation is invoked on the entity.
  - On selecting the failed resource, the user is provided failure information
    from the AWS API response.
  - The player is given an option to update resource parameters and retry the
    update.
  - This follows the same workflow as Resource Updates.
- On resource delete success, a delete animation is invoked on the entity and it
  is removed from the scene.
- On resource delete failure, a failure animation is invoked on the entity.
  - CHLOE notifies the user of resource delete failure.
  - On selecting the failed resource, the user is provided failure information
    from the AWS API response.
  - The user is given an option to retry the deletion.
  - If the resource has been deleted by another principal (such as another user
    in the console), deletion is treated as a success.

## Resource Links

Some AWS resources are inherently linked based on their properties (for example,
an Amazon EC2 instance profile and an IAM role). In these cases, the resource
link can be displayed for the user through the UI.

1. The user has two or more resources in their environment.
2. If two resources are dependent on one another, a **View Link** option is
   available in the UI. The visual representation is defined by the type of
   link.
3. Example: Amazon EC2 instance profile and IAM role are linked via line.
4. Example: Amazon VPC and subnet linked via nesting.

Users can also specify their own links for the purpose of logically organizing
resources. User-created links are persistent until one or more linked resources
are terminated.

## Resource Grouping and Movement

The player is able to select and move resources after they have been created
either by the player or by the resource synchronization process. The positioning
data is stored locally as part of the user's save information.

The player is able to group resources based on freeform data (example: grouping
all the frontend web servers for a web application). This information is stored
as [tags](https://docs.aws.amazon.com/general/latest/gr/aws_tagging.html) on the
corresponding AWS resource.

## Resource Synchronization

When playing CHLOE in simulation mode with synchronization enabled, CHLOE will
regularly query the resource inventory backend for updated resource state
information. This information is processed and used to perform the following
tasks.

1. Creation of new game entities corresponding to resources in the information
   feed that did not exist in the last feed.
2. Deletion of game entities not in the information feed that did exist in the
   previous feed.
3. Update of game entities in the information feed that also existed in the
   previous feed.
4. Updating resource property values, grouping tags, etc.

The interval for performing synchronization requests can be configured by the
user (in minutes and seconds).

## Resource Positioning

As resource synchronization takes place, CHLOE will automatically position and
reposition resources in a logical manner. Some positioning criteria are as
follows:

- Resources in the same region will be positioned more closely together.
  - A clear delineation will exist between AWS regions.
- Resources in the same AWS account will be positioned more closely together.
  - A clear delineation will exist between AWS accounts.
- Resources that are associated with a "container type" resource will be
  positioned within the container.
  - Example: Amazon EC2 instances are deployed into subnets. Thus, the EC2
    instance resource must exist within a subnet container.
- Container type resources can be nested within one another, as well as cross
  boundaries into other containers.
  - Example: EC2 instances are deployed into subnets, which exist in Amazon
    VPCs. EC2 instances are associated with security groups. Security groups are
    specific to a VPC, but not to a subnet. Thus, the EC2 instance must exist in
    a subnet container, which exists in a VPC container. The security group
    container also must exist in the VPC container, but can encompass EC2
    instances in multiple subnets.

Users will also have the ability to move resources within their environment to
represent their desired architecture flow. **A resource cannot be manually moved
outside of any container.** This may only occur when the resource properties
have changed to reflect the new container hierarchy.

1. The user interacts with a resource within their environment.
2. The resource becomes movable, and is "placed" in the user's hand.
3. The user navigates to a new location and activates the resource.
4. The resource is placed in the specified location.
5. Metadata defining the resource layout is saved in the user's save data.

## Architecture Map

To support easier navigation of large-scale infrastructure, a level map will
display the overall architecture from an overhead point of view. The map will be
divided into the following sections.

- Region
- AWS Account

As the number of resources and their position change, the scale of the map will
adjust accordingly.

## Heat Map Visualization

Heat map options will be available to display the following. This will be
rendered in first-person mode by changing the presentation of the world through
camera post-processing effects.

- Service-specific highlighting (Amazon EC2, Amazon S3, etc.)
- Cost
- [AWS Well-Architected](https://aws.amazon.com/architecture/well-architected/)
  rating (one for each pillar)
- AWS Config rule violations
- Amazon CloudWatch alarm status
  - The resources being monitored by the metric/alarm will be highlighted.

## Achievements

CHLOE will support an achievement system using a modular framework to define
achievement progress and validation.
