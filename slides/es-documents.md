## ES Documents

Anything goes, but JSON is easiest to manage. Logstash documents look like this:

```javascript
{
	'@timestamp': new Date(),
	'@version': 1,
	'message': "this text was input to logstash,
				and logstash wasn't configured to do any 
				processing on it. Logstash will simply pass it 
				through to elasticsearch in a JSON property 
				called message."
}
```