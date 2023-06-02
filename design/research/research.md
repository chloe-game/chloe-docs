# Research Tasks

The following items need to be researched in more depth so that we can figure
out a design that makes sense.

## Automatic Organization of Resources in 3D

There are some default rules that have to be in place, such as the below related
to containers of resources:

- A resource that exist in a container cannot be moved outside of that container
  (you can't move an EC2 instance out of it's subnet without manually changing
  something about it).
- A container cannot be moved into/out of a container (you can't move a subnet
  to another VPC).
- Containers can grow or shrink at will to fit the contained resources.

The challenge is going to be how to automatically organize resources when they
are synced from an active AWS account. There could be tens to tens of thousands
of resources, so some rules need to be defined for this to present in a way that
makes sense.

## Presenting Multiple Regions

Need to determine how to present multiple regions in relation to single and
multiple AWS accounts.

## Presenting Multiple Accounts

Need to determine how to present multiple accounts at the same time.

## Resource Links

We need to determine how we can best visualize relationships between resources,
with scalability being another major factor.

I.E. It's easy to use lines to relate resources when an account only has 20
resources within it. Lines become too much when there are 20,000 resources.

I would like to do some research about data visualization of large data sets. My
initial thought is to take advantage of LODs. We have z-depth for the
lines/connections. Essentially we create one LOD that is invisible, so players
could easily "walk" through their resources (even thousands) and the lines would
draw according to their position in the game.

Also thinking about a Portal-style approach, where the player has to actively
select a resource and choose to view things it is related to. At that point,
portals would open/close, acting as windows to see the related resources.
