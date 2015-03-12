chef-handler-sumologic Cookbook
===============================
A Chef Report and Error handler that integrates with SumoLogic. 

Requirements
------------

#### Cookbook 
- chef_handler (http://community.opscode.com/cookbooks/chef_handler)

Attributes
----------
#### chef-handler-sumologic::default
<table>
  <tr>
    <th>Key</th>
    <th>Type</th>
    <th>Description</th>
    <th>Default</th>
  </tr>
  <tr>
    <td><tt>["sumologic"]["endpoint"]</tt></td>
    <td>URL</td>
    <td>SumoLogic HTTP Endpoint to receive reports and exceptions</td>
    <td><tt>true</tt></td>
  </tr>
</table>

Usage
-----
#### chef-handler-sumologic::default
1. Create an HTTP source on your SumoLogic account (https://service.sumologic.com)
2. Set the attribute default['sumologic']['endpoint'] with the URL of this HTTP source.
NOTE: if you want to save the report and exceptions to the local chef-client log, use the value "local". Your log level should be at least :info to see the report results, and at least :warn to see the exceptions.
3. Include `chef-handler-sumologic` first in your node's `run_list`:

```json
{
  "name":"my_node",
  "run_list": [
    "recipe[chef-handler-sumologic]"
  ]
}
```

Contributing
------------
1. Fork the repository on Github
2. Create a named feature branch (like `add_component_x`)
3. Write your change
4. Write tests for your change (if applicable)
5. Run the tests, ensuring they all pass
6. Submit a Pull Request using Github

License and Authors
-------------------
Authors:
Duc T. Ha (duc@sumologic.com)
 
