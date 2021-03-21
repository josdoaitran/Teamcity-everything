# Teamcity-everything

## Get list of agent pool
curl --request GET https://{url}/app/rest/agentPools --header 'Authorization: Basic {baiscToken}'

## Get list of agent (Authorized)
curl --request GET https://{url}/app/rest/agents --header 'Authorization: Basic {baiscToken}'

## Get list of agent (Unauthorized)
curl --request GET https://{url}/app/rest/agents?locator=authorized:false --header 'Authorization: Basic {baiscToken}'


## Assign Agent to a Pool
curl --request POST --header 'Authorization: Basic {baiscToken}' \
--header  'Content-Type:application/xml' --data "<agent id='{agent_id}'/>" 'https://{url}/app/rest/agentPools/id:{pool_id}/agents' -v -k'

## Authorize an agent to Pool
curl --request POST https://{url}/app/rest/agents/id:{agent_id}/authorized --data true --header \
'Content-Type: text/plain' --header 'Authorization: Basic {baiscToken}'

## Unauthorize an agent to Pool
curl --request POST https://{url}/app/rest/agents/id:{agent_id}/authorized --data false --header \
'Content-Type: text/plain' --header 'Authorization: Basic {baiscToken}'


