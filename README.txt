
1. About
---------

The Domain Administration helper allows delegated users to do most of the administration for individual domains without needing site-wide permissions.

2. Installation and Configuration Instructions:
------------------------------------------------

2.1. Add to modules folder and Enable as per usual

2.2. Navigate to Admin->Site Building->Blocks and enable admin block (note that it won't appear for the main domain). If you have the Domain Blocks module enabled, you can assign this block to selected domains. 

2.3. Enable permissions in Users >> Permissions

By default, these permissions are available:
    'view own unpublished nodes on domain',
    'update all unpublished nodes on domain',
    'update own unpublished nodes on domain', 
    'delete all unpublished nodes on domain',
    'delete own unpublished nodes on domain', 
    'change author and creation date of nodes on domain',
    'access published checkbox on domain',

If the Book module is enabled, the 'rearrange book pages on domain' permission is available.

If the Menu and Domain Conf modules are enabled, the following permissions are enabled:
    'administer domain primary links menu';
    'administer domain secondary links menu';
    'administer domain navigation menu';

If the Webform module is enabled, the 'access webform results on domain' permission is available.

If the Locale and Domain Conf modules are enabled, the 'translate domain language content' permission is available.

2.4. In Site Building >> Domains >> Settings you can set the URL/path to help pages. If filled in, this link will appear in the domain administration block. When clicked on, it will open up in a new tab, allowing the user to remain on the site. Note: if you have no help pages, you can use the URL at http://www.vasudevaserver.org/domain-admin-help


3. Usage Notes:
-----------------

3.1. The domain admin block will add a 'Create new…' link for any node type the user has permission to edit. If the current node is part of a book structure, and the 'Create new…' link is clicked for a book-enabled content type, by default the parent will be set to the current node (this of course can be changed in the 'Book Navigation' fieldset).

3.2. For developers there is a hook_domainadminblock if other modules want to append their own content to the block. 


4. Additional functionality
-----------------------------

The domain_admin_helper module also contains some additional functionality, but it relies on enabling heavily patched versions of existing Drupal modules:

4.1. Ability to configure domain blocks and add domain block - this relies on heavily patched version of Domain Blocks module, which in turn relies on a core patch. 

4.2. Ability to delegate book pages and their children on a domain to a user who does not have full domain edit permissions - requires patched version of Book Page Access, available here. 

We hope to reintegrate the functionality of these 2 modules back into their drupal.org versions (especially in case of number 4.2, we are not sure we can get around the necessity of the core patch in number 4.1) and then we can update domain_admin_helper accordingly.

5. Credits
-----------

Module developed by Vasudeva Server (http://www.vasudevaserver.org)

Thank you to the Override Node Options and View Unpublished Nodes modules for showing us how to do some things.



