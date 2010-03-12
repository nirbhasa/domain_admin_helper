
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


4. Additional Functionality
-----------------------------

There is some additional functionality which depends on the following 2 patched modules in our github repp. However if you don't install these modules, the above functionality will work fine without it. We hope to submit patches to integrate these with drupal.org soon.

4.1 Domain Blocks: There is additional functionality contained within the module which facilitates the management of domain blocks, but it relies on a heavily modified version of the domain_block module that right now exists only in our github repo at http://github.com/vasudeva-server/domain_blocks

Enabling the module and enabling the 'administer domain blocks' permission will create 'Configure regions' and 'Add region content' links to the sidebar.

4.2 Book page access: The patched version exists at http://github.com/vasudeva-server/book_page_access and extends the module to delegate access to individual users.


5. Credits
-----------

Module developed by Vasudeva Server (http://www.vasudevaserver.org). First used on the Sri Chinmoy Marathon Team website (http://www.srichinmoyraces.org)

Thank you to the Override Node Options and View Unpublished Nodes modules for showing us how to do some things.



