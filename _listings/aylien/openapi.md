swagger: "2.0"
x-collection-name: Aylien
x-complete: 1
info:
  title: AYLIEN News API
  description: the-aylien-news-api-is-the-most-powerful-way-of-sourcing-searching-and-syndicating-analyzed-and-enriched-news-content--it-is-accessed-by-sending-http-requests-to-our-server-which-returns-information-to-your-client-
  termsOfService: https://newsapi.aylien.com/tos
  contact:
    name: API support
    url: https://newsapi.aylien.com/
    email: support@aylien.com
  version: 1.0.0
host: api.newsapi.aylien.com
basePath: /api/v1
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /stories:
    get:
      summary: List Stories
      description: The stories endpoint is used to return stories based on parameters
        you set in your query. The News API crawler gathers articles in near real-time
        and stores information about them, or metadata. Below you can see all of the
        query parameters, which you can use to narrow down your query.
      operationId: listStories
      x-api-path-slug: stories-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - News
      - List
      - Stories
  /related_stories:
    get:
      summary: List related stories
      description: This endpoint is used for finding semantically similar stories
        based on the parameters you provide as inputs. For example, if you want to
        find stories similar to a Tweet or any text extract you input, the related
        stories endpoint will analyze the entities present and the meaning of the
        text, and find stories with a similar meaning. The maximum number of related
        stories returned is 100.
      operationId: listRelatedStories
      x-api-path-slug: related-stories-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - News
      - List
      - Related
      - Stories
    post:
      summary: List related stories
      description: This endpoint is used for finding semantically similar stories
        based on the parameters you provide as inputs. For example, if you want to
        find stories similar to a Tweet or any text extract you input, the related
        stories endpoint will analyze the entities present and the meaning of the
        text, and find stories with a similar meaning. The maximum number of related
        stories returned is 100.
      operationId: listRelatedStoriesAsPost
      x-api-path-slug: related-stories-post
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - News
      - List
      - Related
      - Stories
  /coverages:
    get:
      summary: List coverages
      description: The coverages endpoint allows you to understand the reach a document
        has had. For example, you can track the coverage of a press release or a Tweet
        based on how many times it has been mentioned in stories.
      operationId: listCoverages
      x-api-path-slug: coverages-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - News
      - List
      - Coverages
    post:
      summary: List coverages
      description: The coverages endpoint allows you to understand the reach a document
        has had. For example, you can track the coverage of a press release or a Tweet
        based on how many times it has been mentioned in stories.
      operationId: listCoveragesAsPost
      x-api-path-slug: coverages-post
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - News
      - List
      - Coverages
  /autocompletes:
    get:
      summary: List autocompletes
      description: The autocompletes endpoint a string of characters provided to it,
        and then returns suggested terms that are the most likely full words or strings.
        The terms returned by the News API are based on parameters the type parameters
        you can see below. For example, if you provide the autocompletes endpoint
        with the term `New York C` and select the type `dbpedia_resources`, the API
        will return links to the DBpedia resources `New_York_City`, `New_York_City_Subway`,
        `New_York_City_Police_Department`, and so on.
      operationId: listAutocompletes
      x-api-path-slug: autocompletes-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - News
      - List
      - Autocompletes
  /time_series:
    get:
      summary: List time series
      description: The time series endpoint allows you to track information contained
        in stories over time. This information can be anything from mentions of a
        topic or entities, sentiment about a topic, or the volume of stories published
        by a source, to name but a few. The full list of parameters is given below.
        Using the [Date Math Syntax](https://newsapi.aylien.com/docs/working-with-dates),
        you can easily set your query to return information from any time period,
        from the current point in time to when the News API started collecting stories.
        The returned information can be rounded to a time also specified by you, for
        example by setting the results into hourly, daily, or weekly data points.
      operationId: listTimeSeries
      x-api-path-slug: time-series-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - News
      - List
      - Time
      - Series
  /trends:
    get:
      summary: List trends
      description: The trends endpoint allows you to identify the most-mentioned entities,
        concepts and keywords relevant to your query. For example, this endpoint allows
        you to set parameters like a time period, a subject category, or an entity,
        and your request will return the most mentioned entities or keywords that
        are mentioned in relation to your query.
      operationId: listTrends
      x-api-path-slug: trends-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - News
      - List
      - Trends
  /histograms:
    get:
      summary: List histograms
      description: For the numerical metadata that the News API gathers (such as word
        counts or social shares for example), you can use the histograms endpoint
        to access and display this information. As this endpoint does not return actual
        stories, the results you are given will not count towards your story allowance
        provided by your subscription, so you can effectively query this endpoint
        free of charge.
      operationId: listHistograms
      x-api-path-slug: histograms-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - News
      - List
      - Histograms