# optimizely-time-to-conversion

Allows you to automatically measure the time from visitor-bucketing to conversion 

### How to install
* Install the `Project JavaScript` code found in [projectjs.js](https://github.com/cpreid/optimizely-time-to-conversion/blob/master/projectjs.js)
* Create an Analytics Extension from JSON [(Optimizely docs)](https://help.optimizely.com/Integrate_Other_Platforms/Custom_analytics_integrations_in_Optimizely_X#Create_as_JSON)
  * Copy the JSON contents from [analytics-integration-config.json](https://github.com/cpreid/optimizely-time-to-conversion/blob/master/analytics-integration-config.json)
* Enable the extension you created [(Optimizely docs)](https://help.optimizely.com/Integrate_Other_Platforms/Custom_analytics_integrations_in_Optimizely_X#Enable_an_integration)

### How to use
* Create a Numeric Metric [(Optimizely docs)](https://help.optimizely.com/Measure_success%3A_Track_visitor_behaviors/Create_a_metric_in_Optimizely_X) 
  * This metric's _api name_ will be used when configuring the integration within an experiment
* Navigate to the experiment to which you'd like to track the conversion
* Visit the 'Metrics' tab and add the Numeric Metric you created in the first step
* Visit the 'Integrations' tab and you will see a _Time To Conversion integration_ module 
![Integrations Screen](https://github.com/cpreid/optimizely-time-to-conversion/blob/master/docs/integration.png)
* Check the 'tracked' checkbox in the upper right
  * Set the `Listen for Event (api name)` field to the _api name_ of the event you want to time
  * Set the `Time To Conversion Event (api name)` field to the _api name_ of the numeric metric you created above
  * Select the appropriate _Reset timer on re-bucket_ setting. If you want to reset the timer on each re-bucket in the experiment, choose 'yes' otherwise choose 'no'.
* Save your changes, Publish the experiment
