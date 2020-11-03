## Tools 

#### Name two dependency managers, can you name three ?

<details> 
  <summary>Solution</summary> 

Swift Package Manager, Cocoa Pods and Carthage.

</details> 

#### What's the difference between `git` and `Github`? 


<details> 
  <summary>Solution</summary> 

`git` is an open source versioning system. `Github` is an online versioning platform for project collaboration now owned by Mr. Softie. Other competitors to `Github` are: `BitBucket` and `GitLab`. 

</details> 



#### What is Continuous Integration (CI) / Continuous Deployment (CD) ? 

<details> 
  <summary>Solution</summary> 

Continuous Integration (CI) / Continuous Deployment (CD) is the automation process of connecting your software stack along with testing to ease versioning and deploying software, in our case automatically creating TestFlight builds or App Store builds.

</details> 

#### What is the terminal command for creating a local `git` repository ? 


<details> 
  <summary>Solution</summary> 
  
`git init`

</details> 

#### What is the terminal command for creating a Podfile in an Xcode project? 


<details> 
  <summary>Solution</summary> 

`pod init`

</details> 

#### What is the `Podfile.lock`? 


<details> 
  <summary>Solution</summary> 

This `Podfile.lock` tracks the versions of installed `pods` in your project.

</details> 

#### What is Postman? 

<details> 
  <summary>Solution</summary> 

Postman is an API development platform, as iOS developers this is our go to for testing JSON payload data from Web APIs. 

Example endpoint
`GET https://itunes.apple.com/search?media=podcast&limit=200&term=swift`

Example JSON

```json 
{
	"resultCount": 171,
	"results": [{
		"wrapperType": "track",
		"kind": "podcast",
		"artistId": 1019380766,
		"collectionId": 1209817203,
		"trackId": 1209817203,
		"artistName": "Spec, JP Simard, Jesse Squires",
		"collectionName": "Swift Unwrapped",
		"trackName": "Swift Unwrapped",
		"collectionCensoredName": "Swift Unwrapped",
		"trackCensoredName": "Swift Unwrapped",
		"artistViewUrl": "https://podcasts.apple.com/us/artist/spec/1019380766?uo=4",
		"collectionViewUrl": "https://podcasts.apple.com/us/podcast/swift-unwrapped/id1209817203?uo=4",
		"feedUrl": "https://feeds.simplecast.com/3pGv88mm",
		"trackViewUrl": "https://podcasts.apple.com/us/podcast/swift-unwrapped/id1209817203?uo=4",
		"artworkUrl30": "https://is1-ssl.mzstatic.com/image/thumb/Podcasts123/v4/4f/33/5c/4f335ccf-a9b8-672b-9c79-635925a70787/mza_3481066685613843705.jpg/30x30bb.jpg",
		"artworkUrl60": "https://is1-ssl.mzstatic.com/image/thumb/Podcasts123/v4/4f/33/5c/4f335ccf-a9b8-672b-9c79-635925a70787/mza_3481066685613843705.jpg/60x60bb.jpg",
		"artworkUrl100": "https://is1-ssl.mzstatic.com/image/thumb/Podcasts123/v4/4f/33/5c/4f335ccf-a9b8-672b-9c79-635925a70787/mza_3481066685613843705.jpg/100x100bb.jpg",
		"collectionPrice": 0.00,
		"trackPrice": 0.00,
		"trackRentalPrice": 0,
		"collectionHdPrice": 0,
		"trackHdPrice": 0,
		"trackHdRentalPrice": 0,
		"releaseDate": "2020-09-14T17:26:00Z",
		"collectionExplicitness": "cleaned",
		"trackExplicitness": "cleaned",
		"trackCount": 89,
		"country": "USA",
		"currency": "USD",
		"primaryGenreName": "Technology",
		"contentAdvisoryRating": "Clean",
		"artworkUrl600": "https://is1-ssl.mzstatic.com/image/thumb/Podcasts123/v4/4f/33/5c/4f335ccf-a9b8-672b-9c79-635925a70787/mza_3481066685613843705.jpg/600x600bb.jpg",
		"genreIds": [
			"1318",
			"26"
		],
		"genres": [
			"Technology",
			"Podcasts"
		]
	}]
}
```

</details> 

