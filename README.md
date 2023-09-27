# GroupBy Retail Bash client

## Overview

This is a Bash client script for accessing GroupBy Retail service.

The script uses cURL underneath for making all REST calls.

## Usage

```shell
# Make sure the script has executable rights
$ chmod u+x gb-retailapi-client

# Print the list of operations available on the service
$ ./gb-retailapi-client -h

# Print the service description
$ ./gb-retailapi-client --about

# Print detailed information about specific operation
$ ./gb-retailapi-client <operationId> -h

# Make GET request
./gb-retailapi-client --host http://<hostname>:<port> --accept xml <operationId> <queryParam1>=<value1> <header_key1>:<header_value2>

# Make GET request using arbitrary curl options (must be passed before <operationId>) to an SSL service using username:password
gb-retailapi-client -k -sS --tlsv1.2 --host https://<hostname> -u <user>:<password> --accept xml <operationId> <queryParam1>=<value1> <header_key1>:<header_value2>

# Make POST request
$ echo '<body_content>' | gb-retailapi-client --host <hostname> --content-type json <operationId> -

# Make POST request with simple JSON content, e.g.:
# {
#   "key1": "value1",
#   "key2": "value2",
#   "key3": 23
# }
$ echo '<body_content>' | gb-retailapi-client --host <hostname> --content-type json <operationId> key1==value1 key2=value2 key3:=23 -

# Make POST request with form data
$ gb-retailapi-client --host <hostname> <operationId> key1:=value1 key2:=value2 key3:=23

# Preview the cURL command without actually executing it
$ gb-retailapi-client --host http://<hostname>:<port> --dry-run <operationid>

```

## Docker image

You can easily create a Docker image containing a preconfigured environment
for using the REST Bash client including working autocompletion and short
welcome message with basic instructions, using the generated Dockerfile:

```shell
docker build -t my-rest-client .
docker run -it my-rest-client
```

By default you will be logged into a Zsh environment which has much more
advanced auto completion, but you can switch to Bash, where basic autocompletion
is also available.

## Shell completion

### Bash

The generated bash-completion script can be either directly loaded to the current Bash session using:

```shell
source gb-retailapi-client.bash-completion
```

Alternatively, the script can be copied to the `/etc/bash-completion.d` (or on OSX with Homebrew to `/usr/local/etc/bash-completion.d`):

```shell
sudo cp gb-retailapi-client.bash-completion /etc/bash-completion.d/gb-retailapi-client
```

#### OS X

On OSX you might need to install bash-completion using Homebrew:

```shell
brew install bash-completion
```

and add the following to the `~/.bashrc`:

```shell
if [ -f $(brew --prefix)/etc/bash_completion ]; then
  . $(brew --prefix)/etc/bash_completion
fi
```

### Zsh

In Zsh, the generated `_gb-retailapi-client` Zsh completion file must be copied to one of the folders under `$FPATH` variable.

## Documentation for API Endpoints

All URIs are relative to **

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*AutocompleteApi* | [**autocompletesearch**](docs/AutocompleteApi.md#autocompletesearch) | **GET** /api/request | 
*ProductApi* | [**getByProductIds**](docs/ProductApi.md#getbyproductids) | **GET** /api/search/product | Provided product search functionality
*RecommendationsAPIApi* | [**predict**](docs/RecommendationsAPIApi.md#predict) | **POST** /api/predict | Provide Recommendations AI functionality.
*RecommendationsAPIApi* | [**predictV2**](docs/RecommendationsAPIApi.md#predictv2) | **POST** /api/recommendation | Provide Recommendations AI functionality.
*SearchApi* | [**facetSearch**](docs/SearchApi.md#facetsearch) | **POST** /api/search/facet | Provided search functionality
*SearchApi* | [**search**](docs/SearchApi.md#search) | **POST** /api/search | Provided search functionality


## Documentation For Models

 - [AdditionalInfo](docs/AdditionalInfo.md)
 - [AttributeSuggestion](docs/AttributeSuggestion.md)
 - [Audience](docs/Audience.md)
 - [BiasDto](docs/BiasDto.md)
 - [BiasDtoStrengthDto](docs/BiasDtoStrengthDto.md)
 - [BiasingProfileDto](docs/BiasingProfileDto.md)
 - [BoostedProductBucket](docs/BoostedProductBucket.md)
 - [ColorInfo](docs/ColorInfo.md)
 - [CustomParameterDto](docs/CustomParameterDto.md)
 - [CustomParameterTrigger](docs/CustomParameterTrigger.md)
 - [DebugDto](docs/DebugDto.md)
 - [ErrorDto](docs/ErrorDto.md)
 - [ErrorResponse](docs/ErrorResponse.md)
 - [Experiment](docs/Experiment.md)
 - [ExperimentVariant](docs/ExperimentVariant.md)
 - [Facet](docs/Facet.md)
 - [FacetSearchRequestDto](docs/FacetSearchRequestDto.md)
 - [FacetSearchResponseDto](docs/FacetSearchResponseDto.md)
 - [FieldMask](docs/FieldMask.md)
 - [Filter](docs/Filter.md)
 - [FilterParameter](docs/FilterParameter.md)
 - [FulfillmentInfo](docs/FulfillmentInfo.md)
 - [Identity](docs/Identity.md)
 - [Image](docs/Image.md)
 - [Interval](docs/Interval.md)
 - [Merchandiser](docs/Merchandiser.md)
 - [MessageType](docs/MessageType.md)
 - [Metadata](docs/Metadata.md)
 - [NavigationDto](docs/NavigationDto.md)
 - [NavigationType](docs/NavigationType.md)
 - [NavigationTypeDto](docs/NavigationTypeDto.md)
 - [Order](docs/Order.md)
 - [Overwrites](docs/Overwrites.md)
 - [PageInfoDto](docs/PageInfoDto.md)
 - [PinnedRefinement](docs/PinnedRefinement.md)
 - [PredictResults](docs/PredictResults.md)
 - [PriceInfo](docs/PriceInfo.md)
 - [PriceInfoPriceEffectiveTime](docs/PriceInfoPriceEffectiveTime.md)
 - [PriceInfoPriceExpireTime](docs/PriceInfoPriceExpireTime.md)
 - [PriceInfoPriceRange](docs/PriceInfoPriceRange.md)
 - [PriceInfoPriceRangeOriginalPrice](docs/PriceInfoPriceRangeOriginalPrice.md)
 - [PriceInfoPriceRangePrice](docs/PriceInfoPriceRangePrice.md)
 - [ProductCustomAttribute](docs/ProductCustomAttribute.md)
 - [ProductDto](docs/ProductDto.md)
 - [ProductDtoAudience](docs/ProductDtoAudience.md)
 - [ProductDtoAvailableTime](docs/ProductDtoAvailableTime.md)
 - [ProductDtoColorInfo](docs/ProductDtoColorInfo.md)
 - [ProductDtoPriceInfo](docs/ProductDtoPriceInfo.md)
 - [ProductDtoPublishTime](docs/ProductDtoPublishTime.md)
 - [ProductDtoRating](docs/ProductDtoRating.md)
 - [ProductDtoRetrievableFields](docs/ProductDtoRetrievableFields.md)
 - [Promotion](docs/Promotion.md)
 - [QueryPatternTrigger](docs/QueryPatternTrigger.md)
 - [QueryPatternTriggerType](docs/QueryPatternTriggerType.md)
 - [Range](docs/Range.md)
 - [RangeFilter](docs/RangeFilter.md)
 - [Rating](docs/Rating.md)
 - [RecommendationsErrorResponse](docs/RecommendationsErrorResponse.md)
 - [RecommendationsRequest](docs/RecommendationsRequest.md)
 - [RecordDto](docs/RecordDto.md)
 - [Refinement](docs/Refinement.md)
 - [RefinementDto](docs/RefinementDto.md)
 - [Request](docs/Request.md)
 - [Role](docs/Role.md)
 - [RuleConfiguration](docs/RuleConfiguration.md)
 - [RuleTemplate](docs/RuleTemplate.md)
 - [RuleTemplateSection](docs/RuleTemplateSection.md)
 - [RuleType](docs/RuleType.md)
 - [RuleVariant](docs/RuleVariant.md)
 - [SearchFilter](docs/SearchFilter.md)
 - [SearchMetadataDto](docs/SearchMetadataDto.md)
 - [SearchRequestDto](docs/SearchRequestDto.md)
 - [SearchRequestDtoOverwrites](docs/SearchRequestDtoOverwrites.md)
 - [SearchResponseDto](docs/SearchResponseDto.md)
 - [SearchResults](docs/SearchResults.md)
 - [SearchResultsStats](docs/SearchResultsStats.md)
 - [SearchTerms](docs/SearchTerms.md)
 - [SelectedRefinementDto](docs/SelectedRefinementDto.md)
 - [SelectedRefinementTrigger](docs/SelectedRefinementTrigger.md)
 - [SelectedRefinementTriggerType](docs/SelectedRefinementTriggerType.md)
 - [Sort](docs/Sort.md)
 - [SortDto](docs/SortDto.md)
 - [SortDtoOrderDto](docs/SortDtoOrderDto.md)
 - [SpellCorrectionMode](docs/SpellCorrectionMode.md)
 - [Stats](docs/Stats.md)
 - [TemplateDto](docs/TemplateDto.md)
 - [TemplateDtoTriggerSet](docs/TemplateDtoTriggerSet.md)
 - [Timestamp](docs/Timestamp.md)
 - [TriggerSet](docs/TriggerSet.md)
 - [ValueFilter](docs/ValueFilter.md)
 - [ValueFilterValueFilterType](docs/ValueFilterValueFilterType.md)
 - [ZoneDto](docs/ZoneDto.md)
 - [ZoneDtoType](docs/ZoneDtoType.md)
 - [ZoneType](docs/ZoneType.md)


## Documentation For Authorization


## ClientKey


- **Type**: API key
- **API key parameter name**: Authorization
- **Location**: HTTP header

## GroupByIncEmployee


- **Type**: HTTP basic authentication

