# Book of Mormon JSON

An Open-Source Scripture Project


## Table of Contents

- [About](#about)
- [Getting Started](#getting-started)
  - [JSON Data Structure](#json-data-structure)
  - [JavaScript Fetch Example](#javascript-fetch-example)
  - [Verse Type Definition](#verse-type-definition)
- [Contributing](#contributing)
- [License](#license)
- [Acknowledgments](#acknowledgments)

## About

This open-source project contains a handful of json files that contain all the verses from the standard works of the Church of Jesus Christ of Latter-Day Saints.

## Getting Started

### JSON Data Structure
The files are each structured as an array containing JSON objects of each scripture verse.

```json
[
    {
        "volume_title": "Book of Mormon",
        "book_title": "1 Nephi",
        "book_short_title": "1 Ne.",
        "chapter_number": 1,
        "verse_number": 1,
        "verse_title": "1 Nephi 1:1",
        "verse_short_title": "1 Ne. 1:1",
        "scripture_text": "I, Nephi, having been born of goodly parents..."
    },
    ...
]
```

### JavaScript Fetch Example

Here's a simple way to access this json data in a web app using the JavaScript Fetch API and console log the returned data.

```javascript
const getScriptures = async () => {
    await fetch("./book-of-mormon.json")
    .then(resp => resp.json())
    .then(json => console.log(json))
}


// Replace './book-of-mormon.json' with the file path to your json file
```

### Verse Type Definition
You can find a basic TypeScript type definition of the verse JSON object in the verse.d.ts file contained within this repo.

## Contributing
My hope is that over time I will be able to include other translations in different languages. If you have a specific language request open an issue and I'll try my best to get that language! As well, create pull requests for any changes or additions that you want to make for this project.


## License

This project is licensed under the [MIT License](LICENSE) - see the [LICENSE](LICENSE) file for details.

## Acknowledgments

Credit given to the [LDS Documentation Project](https://scriptures.nephi.org/) for providing English exports of the Book of Mormon and the Standard Works.

