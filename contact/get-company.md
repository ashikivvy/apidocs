# Get Company

{% api-method method="post" host="\[PlatformAddress\]/api/1.0/contact?action=getCompany" path="" %}
{% api-method-summary %}
Get Company
{% endapi-method-summary %}

{% api-method-description %}
Get a single company's detail
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="id" type="integer" required=true %}
The company's identifier
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```text
{
  "id": "25146",
  "businessName": "Test",
  "tradingName": "Test Trading",
  "businessNumber": "1234586",
  "email": "company@test.com",
  "phone": "0455550000",
  "fax": "0455550125",
  "website": "www.test.com",
  "address": {
    "line1": "Street Number",
    "line2": "Street Name",
    "line3": "",
    "line4": "",
    "city": "Gold Coast",
    "stateCode": "QLD",
    "countryCode": "AU",
    "postalCode": "4227"
  }
  "primaryAccountManager": "Test User",
  "secondaryAccountManager": "Test User",
  "industry": "Industry Name",
  "primaryContact": "Test User",
  "agentcommission": {
      "commissionRoomHireValue": 123,
      "commissionRoomHireType": "CHF",
      "commissionFoodValue": 222,
      "commissionFoodType": "CHF",
      "commissionBeverageValue": 333,
      "commissionBeverageType": "CHF",
      "commissionAudioVisualValue": 444,
      "commissionAudioVisualType": "CHF",
      "commissionAccommodationValue": 555,
      "commissionAccommodationType": "CHF"
  }
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

## Example Request

`Get a specific company`

```javascript
{ 
  "id":6
}
```

## Returns

| Property | Description |
| :--- | :--- |
| id | The unique identifier for the company |
| externalId | Optionally a unique identifier of the company that is managed by an external application |
| businessName | The company's business name |
| tradingName | The company's trading name |
| businessNumber | The company's registration number |
| phone | The company's phone number |
| fax | The company's fax number |
| website | The company's website |
| email | The company's email address |
| address | The company’s address. This is an an object with the [keys](get-company.md#keys) |
| modifiedDate | The modified date of the company |
| primaryAccountManager | The primary account manager of the company |
| secondaryAccountManager | The secondary account manager of the company |
| industry | The industry of the company |
| primaryContact | The primary contact of the company |
| agentcommission | The commission amount of the company. This is an an object with the [keys](get-company.md#commission) |

## Keys

| **keys** |
| :--- |
| line1 |
| line2 |
| line3 |
| line4 |
| city |
| stateCode \(e.g: QLD\) |
| countryCode \(e.g: AU\) |
| postalCode |

## commission

| **commission types** |
| :--- |
| commissionRoomHireValue |
| commissionRoomHireType |
| commissionFoodValue |
| commissionFoodType |
| commissionBeverageValue |
| commissionBeverageType |
| commissionAudioVisualValue |
| commissionAudioVisualType |
| commissionAccommodationValue |
| commissionAccommodationType |

## Throws

| Code | Description |
| :--- | :--- |
| Specific Code: 24153 | Unable to find company |

The company identifier must be provided to fetch a specific company from the system.

