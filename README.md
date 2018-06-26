# Global Witness DataCorps
## Building a Network Graph of UK corporate ownership

The content of this repository illustrates the concepts and execution of the DataKind UK team in mapping the network graph of UK corporate ownership. These notebooks are provided as examples of how the work was done but should be taken as an illustration of concept and cannot be guaranteed to work with future Companies House data releases.

## How to use these notebooks
These notebooks are anticipated to be run in a specific order to rebuild the Global Witness UK benefical ownership graph database. 

**NOTE** They rely on a number of data sets being downloaded and available:
- The list of active companies from Companies House; available here http://download.companieshouse.gov.uk/en_output.html
- The Beneficial Ownership data, also known as Persons of Signficant Control (PSC data) from Companies House; available here http://download.companieshouse.gov.uk/en_pscdata.html
- Officers data used in this project was supplied by Open Corporates (see notebooks 09 & 10); this data requires an API key from Open Corporates and so the notebooks are only for illustration. The data could also be collected using an API key from Companies House but would be in a different format.
- The Financial Secrecy Index is available from https://www.financialsecrecyindex.com/introduction/fsi-2018-results . **N.B.** We used our own version and so some modifications to the relevant section of code need to be made.

The notebooks should be read (and run) in the following order:

- 00.Demo connection to Neo4j
- 01.Setting-up-fresh-neo4j-database
- 02.Country-Node-creation
- 03.Inserting-active-companies-into-neo4j
- 04.Inserting-human-PSCs
- 05.Inserting-Corporate-PSCs
- 06.Inserting-Legal-Entity-PSCs
- 07.Inserting-PSC-Super-Secure-Persons
- 08.Inserting-missing-PSC-statements
- 09.Inserting-Officers-People
- 10.Inserting-Officers-Companies - **NOTE** it was discovered that both company ids are not available in the working dataset and hence this notebook is actually incomplete and needs additional data to build the connections between companies that are officers
- 11.Tidying-up-the-database

MIT License

Copyright (c) [2018] [DataKind UK]

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
