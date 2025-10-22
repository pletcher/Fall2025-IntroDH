# Web Scraping Lab

## Statement on Gen AI

**Again, do not use generative AI for this assignment.**

Using generative AI for this lab will be considered an academic
integrity violation, which I am required to report.

## Network work: scraping Wikipedia

> [!NOTE]
> Wikipedia explicitly allows scraping, but you _must_ be careful
> to implement a rate limiter. `time.sleep(5)` should be
> sufficient.

For this lab, you will use what you've learned about Python so far
to collect data from Wikipedia. Your task is to build a network of
pages, beginning from a page of your choosing.

Networks are composed of nodes (or vertices) and edges. Each
node should contain information about a single Wikipedia page,
and the node's edges are the links that it contains to other
Wikipedia pages.

Using the [Digital Humanities](https://en.wikipedia.org/wiki/Digital_humanities)
page as an example, your network might look something like the following:

```json
{
	"title": "Digital Humanities",
	"content": "...",
	"url": "https://en.wikipedia.org/wiki/Digital_humanities",
	"links": [{
		"title": "Computing",
		"content": "...",
		"url": "https://en.wikipedia.org/wiki/Computing",
		"links": [{
			"title": "..."
		}]
	}, {
		"title": "Information technology",
		"content": "...",
		"url": "https://en.wikipedia.org/wiki/Information_technology",
		"links": [{

		}]
	}]
}
```

Notice how each node has the basic form

```json
{
	"title": "The page title",
	"content": "The text content of the page — you might want to limit how much information you try to grab here.",
	"url": "The URL for the page",
	"links": "The top n links to other Wikipedia pages, where you decide what `n` makes the most sense for your goals."
}
```

The goal here is for you to explore Python. If you have time and would like an extra challenge, you could
attempt to identify loops in your network: links that refer back to pages you have already indexed.

You'll need to keep track of how deep your network gets — you don't need to go more than four or five levels down.

We will return to the content that you have scraped for the NLP Lab, so try to choose a topic that
you find interesting.

For your submission, please turn in the script that you used to gather your network, as well
as a JSON dump of the data itself.

Please also submit a short (2-3–page) lab report, detailing your hypothesis/es about
the network that you're exploring, your methods, and a brief discussion of the tools
and techniques that you used to complete the lab.

This lab is due at 11:59 p.m. on Tuesday, October 28, 2025.
