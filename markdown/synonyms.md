FORMAT: 1A
HOST: http://api.proficionym.dev

# Synonyms

An endpoint that fetches synonyms for a word.
It currently uses the dictionaryapi.com Thesaurus API.

## 200 - Synonyms [/synonyms/{word}]

Successful request.

+ Parameters
	+ word: "test" (required, string) - Synonyms will be looked up for this word. It must not have punctuation or numbers.
	
### Get a successful set of synonyms

+ Response 200 (application/json)

		{
		    "synonyms":[
		        "essay",
		        "experimentation",
		        "test",
		        "trial",
		        "trialanderror",
		        "dryrun",
		        "shakedown",
		        "exercise",
		        "practice",
		        "rehearsal",
		        "tryout",
		        "workout",
		        "crucible",
		        "ordeal",
		        "attempt",
		        "effort",
		        "try",
		        "exam",
		        "quiz",
		        "aptitudetest",
		        "intelligencetest",
		        "placementtest",
		        "pretest",
		        "retest",
		        "board",
		        "midterm",
		        "midyear",
		        "catechism",
		        "audition",
		        "final",
		        "checkup",
		        "inspection",
		        "review",
		        "inquiry",
		        "interrogation",
		        "investigation",
		        "probe",
		        "research",
		        "sample",
		        "check",
		        "investigate",
		        "study",
		        "resample",
		        "strain",
		        "stretch",
		        "tax",
		        "demand",
		        "exact",
		        "importune",
		        "press",
		        "pressure",
		        "push",
		        "aggravate",
		        "agitate",
		        "annoy",
		        "bother",
		        "exasperate",
		        "gall",
		        "get",
		        "grate",
		        "harass",
		        "harry",
		        "hassle",
		        "irk",
		        "irritate",
		        "nettle",
		        "pain",
		        "peeve",
		        "pester",
		        "rile",
		        "spite",
		        "vex"
		    ]
		}

## 400 - Synonyms [/synonyms/{word}]

Failed request due to invalid string.

+ Parameters
	+ word: "test123" (required, string) - Synonyms will be looked up for this word. It must not have punctuation or numbers.

### Get an error for an invalid string

+ Response 400 (application/json)

		{
			"error": "Invalid Parameter",
			"description": "The word you look up must be a single word with no numbers or punctuation"
		}
	
## 400 - Synonyms [/synonyms/{word}]

Failed request due to no synonyms being found for otherwise valid string.

+ Parameters
	+ word: "ierghefvibei" (required, string) - Synonyms will be looked up for this word. It must not have punctuation or numbers.

### Get an error for an invalid string

+ Response 400 (application/json)

		{
			"error": "No Synonyms",
			"description": "_mapRawSynonyms: rawSynonyms fails validation"
		}