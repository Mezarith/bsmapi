# BSMAPI - _B_orealis (Game)_s_erver _M_anager API
For when you want to be even lazier.
---
## Concept
The point behind this project is to provide a backend for the client application to fetch data from on the fly, thus removing the need to push data with app updates (the app can just check this bad boy for new stuff). It'll store server configurations, and that's about it, really. There's some foundation for other concepts to be introduced at a later point (authentication, etc.)

## Installation
1. Clone this repository: `git clone https://bitbucket.org/Mezarith/bsmapi`
2. Move into the directory (I shouldn't need to tell you how to do this).
3. Run `npm install` to download dependencies.
4. Run `npm start` to start the API.  

It'll begin listening on whatever port/ip is specified in the config file (config.json).

## Endpoints
**[GET/POST] /bsmver**  
Gets the commit sha of the BGM as the version number.  

**[GET/POST] /apiver**  
Gets the commit sha of this API's repository.  

**[GET] /config/:appid:**  
Gets a predefined config file and sends it to the client via XML (eww).  

**[GET] /launch/:appid:**  
Gets the launch flags for the specified server.  

**[PUT] /submit**  
Takes data, and creates a new config template.

## TODO
- Actually implement these endpoints.
- Find enough time to work on this.
- Decide on a database (preferrably sqlite due to the low amount of requests).
- Make this TODO more impressive. :feelsbadman:
- Work on otherworld middlewares.
