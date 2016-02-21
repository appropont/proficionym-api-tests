FORMAT: 1A
HOST: http://api.proficionym.dev:3000

# Group Index

An endpoint that fetches synonyms for a word.
It currently uses the dictionaryapi.com Thesaurus API.

## 200 - Index [/]

Successful request.
    
### Get a successful set of synonyms [GET]

+ Response 200 (application/json)
        
        {
            "name":"Proficionym API",
            "version":"0.0.1"
        }