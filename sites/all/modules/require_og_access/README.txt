Require OG access

Prevent access to OG private posts except to privileged users and OG 
group members.

This module serves to ensure that OG private posts remain private to the
Organic Group(s) to which they're posted, regardless of which other
modules may be trying to grant access.

Under most circumstances and for most simple Drupal installations, Organic
Groups will do a fine job of ensuring that group posts marked "private"
will only be accessible by group members. It does this by simply refusing
to grant access to those nodes.

However, it is possible for other modules to grant other users with access 
to those nodes. For example, Workflow module may be configured to grant
view, edit, and/or delete access to certain roles, for nodes in a certain 
workflow state. This grant will be enough to allow non-group-members in 
those roles to access the nodes.

This module adds an additional check to the node access system, so that
group posts marked "private" will be inaccessible (for view, edit, and
delete operations) to anyone who is not a group member, even if other modules
grant such access.

This limitation can be lifted for specific roles, operations, or content types,
using the provided permissions.

This module requires Node Access Fixer.

