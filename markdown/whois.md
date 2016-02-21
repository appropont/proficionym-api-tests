FORMAT: 1A
HOST: http://api.proficionym.dev

# Whois

An endpoint that checks whether a domain name is registered. Currently supported TLDs are: .com, .net, .org, .io

## 200 - Whois [/whois/{domain}]

Successful lookup of an unregistered .com

+ Parameters
	+ domain: "testing123abcd321.com" (required, string) - Synonyms will be looked up for this word. It must not have punctuation or numbers.
	
### Look up an unregistered .com

+ Response 200 (application/json)
		
		{
			"domain":"testing123abcd321.com",
			"status":"available"
		}
		

## 200 - Whois [/whois/{domain}]

Successful lookup of a registered .com

+ Parameters
	+ word: "google.com" (required, string) - Synonyms will be looked up for this word. It must not have punctuation or numbers.

### Look up a registered .com

+ Response 200 (application/json)

		{
			"domain": "google.com",
			"status": "registered"
		}
	
## 200 - Whois [/whois/{domain}]

Failed request due to no synonyms being found for otherwise valid string.

+ Parameters
	+ word: "no-tld" (required, string) - Synonyms will be looked up for this word. It must not have punctuation or numbers.

### Get an error for an invalid domain

+ Response 200 (application/json)

		{
			"domain": "no-tld",
			"status": "error"
		}
