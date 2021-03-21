# Teamcity-everything

## Get list of agent pool
curl --request GET https://{url}/app/rest/agentPools --header 'Authorization: Basic {baiscToken}'

## Get list of agent (Authorized)
curl --request GET https://{url}/app/rest/agents --header 'Authorization: Basic {baiscToken}'

## Get list of agent (Unauthorized)
curl --request GET https://{url}/app/rest/agents?locator=authorized:false --header 'Authorization: Basic {baiscToken}'
