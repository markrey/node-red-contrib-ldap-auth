Node-red-contrib-ldap-auth
--------------------------

This is a Node-RED authentication plugin that uses LDAP as the backend user store.

It can be installed with:

    npm install -g node-red-contrib-ldap-auth

And then to enable it add the following to your settings.js file:

    adminAuth: require('node-red-contrib-ldap-auth').setup({
		uri:'ldap://url.to.server', 
		base: 'ou=group,o=company.com', 
		filterTemplate: 'mail={{username}}'
	}),