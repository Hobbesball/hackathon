# InnoAir and Europeana hackathon datasets

This repository provides direct downloads to datasets from Europeana that can be used during the [InnoAir hackathon](https://innoair-sofia.eu/en/challenges/97-challenges/407-hackathon-%E2%80%9Cinnoair-europeana-the-challenge-of-sustainability-and-social-justice%E2%80%9D.html), organised by the Sofia Development Association and the Sofia Municipality. The hackathon runs from June 1st to June 8th 2023, and features around **7.500 EUR in prizes**. You can sign up for the hackathon [here](https://docs.google.com/forms/d/e/1FAIpQLScecHLEodmsXKpVRK1mYk0MNsLEaI8B3-N0Pn6rBXQvBo1pcQ/viewform). 

**for any questions, mentoring or guidance on how to use these datasets or Europeana's APIs, please get in contact with Jolan at jolan[dot)wuyts(at]Europeana[dot)eu**

The datasets in this repo correspond to the following two hackathon challenges: 

### Use historical photographic data to re-imagine urban mobility
Using the historical photographs of Bulgaria from the [NALIS foundation](https://www.europeana.eu/en/collections/organisation/1482250000004510583-national-academic-library-and-information-system-foundation?page=6&view=grid&query=), showcase and analyse historical urban planning and urban mobility to propose solutions for the future. This challenge allows teams to focus on more qualitative low-tech products that connect historical knowledge embedded in cultural heritage objects with the current trends towards degrowth and a solarpunk future. You can use this dataset and any other connected data you'd like in your end product. All 15K images from the NALIS foundation are in the public domain. 

### Connect cultural heritage libraries with current biodiversity databases
Europeana's largest aggregator of data is [OpenUp!](https://open-up.myspecies.info/en), which collects, enriches and standardises Natural History heritage from all over Europe. [More than 10 million objects](https://www.europeana.eu/en/search?page=1&qf=PROVIDER%3A%22OpenUp%5C%21%22&query=&view=grid) showcasing the biodiversity and natural history heritage of Europe are available on Europeana through OpenUp. These collections are very well described and metadated and are largely free for re-use. Create a product that uses this rich trove of biodiversity heritage to (re)imagine a more green, sustainable future that preserves biodiversity knowledge and/or operationalises that historical wealth for future ecological decision-making. You can use this dataset in conjunction with other current databases and APIs on biodiversity like [Genesys](https://www.genesys-pgr.org/) for your end product.

## General useful links
- [tips on how to search Europeana](https://www.europeana.eu/en/help/search-tips)
- [interesting info for devs on europeana.eu](https://www.europeana.eu/en/for-developers)
- [Europeana API documentation homepage](https://pro.europeana.eu/page/apis)
- [get an API key here](https://pro.europeana.eu/pages/get-api) 
- [Search API documentation](https://pro.europeana.eu/page/search)
- [Search and Record API Swagger console](https://pro.europeana.eu/page/api-rest-console)
- [Record API documentation](https://pro.europeana.eu/page/record)
- [Harvesting and Downloads API documentation](https://pro.europeana.eu/page/harvesting-and-downloads)
- [pyEuropeana](https://rd-europeana-python-api.readthedocs.io/en/stable/index.html) python library for Europeana's APIs
- [information about our data model, EDM](https://pro.europeana.eu/page/intro#edm)


## NALIS
The NALIS foundation has one dataset provided to Europeana that you can re-use in the hackathon. The 'NALIS' folder contains:
- one zipped dataset in XML format, where every object on Europeana from this dataset corresponds to 1 XML file. You can read more about the structure of this dataset in the ['Downloads' section of this page](https://pro.europeana.eu/page/harvesting-and-downloads#downloads). 
- an md5 checksum file that you can use to ensure that the dataset you've downloaded is complete and uncorrupted
- a JSON file called 'dataset description NALIS.json' that lists the single dataset name and the amount of objects in that dataset. This file was created using [this API call](https://api.europeana.eu/record/v2/search.json?wskey=api2demo&query=DATA_PROVIDER%3A%22National%20Academic%20Library%20and%20Information%20System%20Foundation%22&rows=0&profile=facets&facet=edm_datasetName). 
- a JSON file called 'facet information for NALIS foundation data.json' that collects information from the indexed facets Europeana has about this dataset. This file was created using [this API call](https://api.europeana.eu/record/v2/search.json?wskey=api2demo&query=DATA_PROVIDER%3A%22National%20Academic%20Library%20and%20Information%20System%20Foundation%22&rows=0&profile=facets).
- If you want to access the full NALIS dataset in a Search API result, you can use this API call: `https://api.europeana.eu/record/v2/search.json?wskey=api2demo&query=DATA_PROVIDER:%22National%20Academic%20Library%20and%20Information%20System%20Foundation%22`

## OpenUp!
The OpenUp! aggregator has 74 datasets provided to Europeana. These datasets contain about 55Gb of metadata if you count all the sets together, so we can't provide the full datasets on GitHub. To get access to a full download of these datasets, you'll need to download them from the [FTP server or from the OAI-PMH server](https://pro.europeana.eu/page/harvesting-and-downloads).

The openup folder contains:
- a JSON file called 'dataset description openup.json' that lists every single dataset name and the amount of objects in that dataset. This file was created using [this API call](https://api.europeana.eu/record/v2/search.json?wskey=api2demo&query=PROVIDER%3A%22OpenUp!%22&rows=0&profile=facets&facet=edm_datasetName&f.edm_datasetName.facet.limit=10000). 

If you want to look at the contents of a single OpenUp dataset you can search europeana.eu for the following query: `edm_datasetName:(DATASETLABELHERE)` or do the same through a Europeana Search API query. [Here's a query example](https://api.europeana.eu/record/v2/search.json?wskey=api2demo&query=edm_datasetName:(%22179_OpenUp_NBGB_Part3%22)) looking for the dataset `"179_OpenUp_NBGB_Part3"`

- If you want to access the full OpenUp! dataset in a Search API result, you can use this API call: `https://api.europeana.eu/record/v2/search.json?wskey=api2demo&query=PROVIDER:%22OpenUp!%22`
