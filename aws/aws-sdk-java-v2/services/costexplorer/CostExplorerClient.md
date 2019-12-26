# software.amazon.awssdk.services.costexplorer.CostExplorerClient

Service client for accessing AWS Cost Explorer.

This can be created using the static **`builder()`** method.

The Cost Explorer API enables you to programmatically query your cost and usage data.

You can query for aggregated data such as total monthly costs or total daily usage.

You can also query for granular data, such as the number of daily write operations for Amazon DynamoDB database tables in your production environment.

Service Endpoint

The Cost Explorer API provides the following endpoint:

+ https://ce.us-east-1.amazonaws.com

For information about costs associated with the Cost Explorer API, see [AWS Cost Management Pricing](https://aws.amazon.com/aws-cost-management/pricing/).















SERVICE_NAME
builder()
create()
serviceMetadata()

getCostAndUsage(Consumer<Builder>)
getCostAndUsage(GetCostAndUsageRequest)

getCostForecast(Consumer<Builder>)
getCostForecast(GetCostForecastRequest)

getDimensionValues(Consumer<Builder>)
getDimensionValues(GetDimensionValuesRequest)

getReservationCoverage(Consumer<Builder>)
getReservationCoverage(GetReservationCoverageRequest)

getReservationPurchaseRecommendation(Consumer<Builder>)
getReservationPurchaseRecommendation(GetReservationPurchaseRecommendationRequest)

getReservationUtilization(Consumer<Builder>)
getReservationUtilization(GetReservationUtilizationRequest)

getTags(Consumer<Builder>)
getTags(GetTagsRequest)

getUsageForecast(Consumer<Builder>)
getUsageForecast(GetUsageForecastRequest)


## SERVICE_NAME

SERVICE_NAME = "ce"

## create()

Create a CostExplorerClient with the region loaded from the software.amazon.awssdk.regions.providers.DefaultAwsRegionProviderChain and credentials loaded from the software.amazon.awssdk.auth.credentials.DefaultCredentialsProvider.

## builder()

Create a builder that can be used to configure and create a CostExplorerClient.

## serviceMetadata()


## getCostAndUsage(Consumer<Builder>)

Retrieves cost and usage metrics for your account.

You can specify which cost and usage-related metric, such as BlendedCosts or UsageQuantity, that you want the request to return.

You can also filter and group your data by various dimensions, such as SERVICE or AZ, in a specific time range.

For a complete list of valid dimensions, see the [GetDimensionValues](http://docs.aws.amazon.com/aws-cost-management/latest/APIReference/API_GetDimensionValues.html) operation.

Master accounts in an organization in AWS Organizations have access to all member accounts.

This is a convenience which creates an instance of the [GetCostAndUsageRequest.Builder](#) avoiding the need to create one manually via [GetCostAndUsageRequest.builder()](#).


### Parameters: 

getCostAndUsageRequest

A Consumer that will call methods on GetCostAndUsageRequest.Builder to create a request.

### Returns:

Result of the GetCostAndUsage operation returned by the service.

### Throws:

LimitExceededException - You made too many calls in a short period of time. Try again later.

BillExpirationException - The requested report expired. Update the date interval and try again.

DataUnavailableException - The requested data is unavailable.

InvalidNextTokenException - The pagination token is invalid. Try again without a pagination token.

RequestChangedException - Your request parameters changed between pages. Try again with the old parameters or without a pagination token.

SdkException - Base class for all exceptions that can be thrown by the SDK (both service and client). Can be used for catch all scenarios.

SdkClientException - If any client side error occurs such as an IO related failure, failure to get credentials, etc.

CostExplorerException - Base class for all service exceptions. Unknown exceptions will be thrown as an instance of this type.

AwsServiceException

See Also:

AWS API Documentation@sampleCostExplorerClient.GetCostAndUsage

## getCostAndUsage(GetCostAndUsageRequest)



## getCostForecast(Consumer<Builder>)



## getCostForecast(GetCostForecastRequest)



## getDimensionValues(Consumer<Builder>)



## getDimensionValues(GetDimensionValuesRequest)



## getReservationCoverage(Consumer<Builder>)



## getReservationCoverage(GetReservationCoverageRequest)



## getReservationPurchaseRecommendation(Consumer<Builder>)



## getReservationPurchaseRecommendation(GetReservationPurchaseRecommendationRequest)



## getReservationUtilization(Consumer<Builder>)



## getReservationUtilization(GetReservationUtilizationRequest)



## getTags(Consumer<Builder>)



## getTags(GetTagsRequest)



## getUsageForecast(Consumer<Builder>)



## getUsageForecast(GetUsageForecastRequest)












































