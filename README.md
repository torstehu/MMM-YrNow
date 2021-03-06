# MagicMirror² Module: YrNow

This is a module for [MagicMirror²](https://github.com/MichMich/MagicMirror) which displays data from Yr's Nowcast.
Nowcast data is only available for some Norwegian locations covered by the weather radar. See [Explanation (in Norwegian)](https://yrkundesenter.zendesk.com/hc/no/articles/209295525-N%C3%A5varsel-Pr%C3%B8v-v%C3%A5rt-nye-nedb%C3%B8rvarsel-)
![Screenshot](/images/screenshot.png?raw=true)

## How to install

Remote into your Magic Mirror box using a terminal software and go to the modules folder:

    cd ~/MagicMirror/modules

Clone the repository:

	git clone https://github.com/nrkno/MMM-YrNow

Add the module to the modules array in the config/config.js file by adding the following section. You can change this configuration later when you see this works:

	{
		module: 'MMM-YrNow',
		position: 'top_right',
		config: {
			locationId: '1-73738',
            showWeatherForecast: true
		}
	},

## Configuration options

<table style="width:100%">
	<tr>
		<th>Option</th>
		<th>Comment</th>
		<th>Default</th>
	</tr>
	<tr>
		<td>locationId</td>
		<td>The unique Id found in the Url of any location on <a href="https://www.yr.no/nb/liste/dag/1-73738/Norge/Oslo/Oslo/Blindern">Yr</a> I.e. Blindern (Oslo)</td>
		<td>1-73738</td>
	</tr>
    <tr>
        <td>showWeatherForecast</td>
        <td>If there's no precipitation in the nowcast, the weather forecast for the next period is shown.</td>
        <td>true</td>
    </tr>
</table>
