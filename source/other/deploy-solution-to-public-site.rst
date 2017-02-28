How to install sandbox solution to an Office 365 public site
============================================================

You need to use direct link to upload sandbox solution to solutions gallery on your Office 365 public site, because public sites are very limited and there are not link in site settings.
To get access to solution gallery just add */_catalogs/solutions* to your public site URL. The full link look like this::
	https://yousite-public.sharepoint.com/_catalogs/solutions

hen you need to activate the feature of Workflow Actions Pack on current site. Unfortunately feature management page doesn’t exist on public sites, but you can use JavaScript to do this. Just press F12 in your browser, navigate to console tab and paste the following code::

	(function(featureId, enable) {
	    var clientContext = new SP.ClientContext.get_current();
	    var featureGuid   = new SP.Guid('{' + featureId + '}');
	    var webFeatures   = clientContext.get_web().get_features();

	    if (enable) {
	        webFeatures.add(featureGuid, true, SP.FeatureDefinitionScope.site);
	    } else {
	        webFeatures.remove(featureGuid, false);
	    }

	    clientContext.executeQueryAsync(
	        function() { alert('Success!'); }
	      , function(sender, args) {
	          alert('Fail: ' + args.get_message() + '\n' + args.get_stackTrace());
	    });
	})('d7891031-e7f5-4734-8077-9189dd35551c', true);

After a few seconds you must see success message. Now you can open SharePoint Designer and use new workflow actions.

