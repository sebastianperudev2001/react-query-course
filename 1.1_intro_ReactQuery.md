# Introduction to React Query

## CLient State vs Server State

| State Type | Description | Example |
|------------|-------------|---------|
| Client State | Information relevant to browser session. It's simply tracking what the user does | A user might choose a language or theme |
| Server State | Information stored on server | Blog post data from database |


## What problem does React Query solve? 
- React Query maintains cache of server data on client
- When I fetch server data, do it via React Query 

React code <---> React Query <---> Server

## React Query manages data
- Indicate when to update cache with new data from the server
- imperatively: invalidate data
- Declaratively: Configure how (window focus) & when to trigger a refetch (stale time)


Maintains Loading/Error States so that I do not have to them manually.
Fetch data when it is needed for pagination or infinite scroll.
Prefetching data for routes that are about to be visited.
Mutations -->  Updates of data in the server
De-duplication of requests: Queries are identified by a key. Can manage requests, several componentes on the page requests the same data, it can only request once. De duplicate the request
Retry on error --> If I get an error, it will retry the request
Callbacks --> onSuccess, onError, onSettled. Take actions based on the state of the query