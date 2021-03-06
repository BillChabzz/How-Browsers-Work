## What's a browser?

Before we know how a browser works, let's describe a browser. It can be described as a **software application** that retreives data from a server and presents or 
renders a page  from the world wide web. The world wide web is a resource of documents that can be accessed via the internet. The documents' location is specified
by the URL(Uniform Resource Locator).

## The browser's main function
The core function of a browser is to present the web resources by requesting a server and displaying it in the browser window. The resources are mainly HTML documents.
They can also be videos , images or any other content. As stated under "What's a browser" topic, the resources are specified by a user using a URL/URI.
Examples of browsers include:
* Chrome
* Firefox
* Edge
* Safari

The browsers have common user interface like the:
* Address bar for typing the URL
* Menu icon 
* Home, refresh, forward and backward buttons

There are many more similarities.

##A brief description of how a browser works

The URL typed in address bar maps to an IP address. This is called DNS(Domain Name Service) lookup. The DNS maps numeric computer addresses to human readable names.

Once the browser has the IP address, it sends a HTTP request to the web server at the specified address. Hyper Text Transfer Protocol is used to facilitate requests from your client(the browser) and responses from a server. As this HTML response is being sent to the browser, the browser's rendering engine is displaying the request content on your screen. To accomplish this the rendering engine parses the HTML and creates the DOM tree.

The browser then parses style data(CSS) and together with the html ,it constructs a render tree. The render tree displays rectangles (i.e divs,paragraphs, headlines, etc) with a few visual attributes such as color and size dimensions. The rectangles are displayed in order on the page. The browser lays out the contents in the position they will appear in the browser. Finaly is "painting" where the elements are drawn on the screen.

### Let's get to understand the browser and its structure.
The browser is made up of components as follows:

1.Browser engine- this marshals between the UI and rendering engine

2.UI(user interface)- these are the interactive parts such as the address bar,bookmarking menu,forward/backward button but does not include the the browser window.

3.Rendering engine-this displays requested content to the browser screen. This can also include other types of data using plug-ins e.g. PDFs

##### Rendering engines and flow

Different browsers use different rendering engines. The rendering engine gets the content of requested documents from the network layer usually in 8kb chucks.The main flow of the engine can be described as follows:

-- Parsing html to construct DOM tree- this parses the html document and converts the style data, both external CSS and in style elements. The styling of visual instructions will be used to create the render tree.

--Render tree construction-the render tree contains rectangles with visual attributes. These rectangles are displayed in order on the page.

--Layout of render tree-Each node is given the exact coordinates where it should appear on the screen.

--Painting the render tree-The render tree is traversed and each node painted using UI backend layer.

4.Networking- for handling the http requests using different implementations for different platforms

5.UI backend- this draws the basic widgets like combo boxes and windows.It exposes the generic interface that isn't platform specific.

6.Js interpreter- used to parse and execute Js code.

7.Data storage-a persistence layer where the browser stores data locally eg cookies

