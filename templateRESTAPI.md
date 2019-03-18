# API_name

  <_Give a brief, preferably one-line, description of your API call. Try to use verbs that match both request type (get vs delete) and plurality (one vs multiple)._>

## Syntax/HTTP request
  
  <_State the HTTP request type followed by the path only (no URL)._>
  
  `GET /jobs/`_`job_identifier`_`/results`
  
## Example request

  <_Provide sample call to endpoint, broken into the URL and the path itself._>  
     
   `GET https://10.3.57.4:8078/v4/jobs/3fc911e0-a553-11e7-ba87-41ed1518f774/results`
  
## Request parameters

   <_If URL params exist, specify them in accordance with name mentioned in URL section. Separate into optional and required, or use a table. Document data constraints._> 

   **Required:**
 
   `id=[integer]`

   **Optional:**
 
   `photo_id=[alphanumeric]`

## Request body

  <_If making a (often POST) request that requires a body payload, show how it should look and describe parameters as required._>  

## Response
  
  <_Detail returned data for a successful response. Provide example(s) and describe as required. Create Example sections if more than one example is required._>

  **Content:** `{ id : 12 }`
 
## Errors

  <_List errors that can be returned if specific to the API call, with level of error and any workarounds to offer. For generic/common errors, instead put in a separate reference topic._>

  * **Code:** 401 UNAUTHORIZED <br />
    **Content:** `{ error : "Log in" }`

  * **Code:** 422 UNPROCESSABLE ENTRY <br />
    **Content:** `{ error : "Email Invalid" }`

## <_Notes_> 

  <_This is where all uncertainties, commentary, etc. can go. Use appropriate heading(s)._> 
  
## Related links

  <_List related topics._> 
