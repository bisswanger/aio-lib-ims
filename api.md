# Adobe I/O Lib IMS Library API Documentation

## Modules

<dl>
<dt><a href="#module_aio-lib-ims">aio-lib-ims</a></dt>
<dd><p>The <code>@adobe/aio-lib-ims</code> module offers three kinds of elements:</p>
<ol>
<li>Managing configuration contexts for token creation and use</li>
<li>Creating and invalidating tokens</li>
<li>Providing low level access to IMS API</li>
</ol>
</dd>
</dl>

## Classes

<dl>
<dt><a href="#Ims">Ims</a></dt>
<dd><p>The <code>Ims</code> class wraps the IMS API.</p>
</dd>
<dt><a href="#ConfigCliContext">ConfigCliContext</a></dt>
<dd><p>The <code>ConfigCliContext</code> class stores IMS <code>contexts</code> for the Adobe I/O CLI in the local file
system using the Adobe I/O Core Configuration Library.</p>
</dd>
<dt><a href="#Context">Context</a></dt>
<dd><p>The <code>Context</code> abstract class provides an interface to manage the IMS configuration contexts on behalf of
the Adobe I/O Lib IMS Library.</p>
</dd>
<dt><a href="#StateActionContext">StateActionContext</a></dt>
<dd><p>The <code>StateActionContext</code> class stores IMS <code>contexts</code> for Adobe I/O Runtime Actions in the
cloud using the Adobe I/O State Library.</p>
</dd>
</dl>

## Constants

<dl>
<dt><a href="#TYPE_ACTION">TYPE_ACTION</a></dt>
<dd><p>Name of context type action</p>
</dd>
<dt><a href="#TYPE_CLI">TYPE_CLI</a></dt>
<dd><p>Name of context type cli</p>
</dd>
<dt><a href="#IMS">IMS</a></dt>
<dd><p>Name of the IMS configuration context data structure</p>
</dd>
<dt><a href="#CONTEXTS">CONTEXTS</a></dt>
<dd><p>Property holding an object with all contexts</p>
</dd>
<dt><a href="#CONFIG">CONFIG</a></dt>
<dd><p>Property holding an object with context management configuration</p>
</dd>
<dt><a href="#CLI">CLI</a></dt>
<dd><p>Property holding the cli context name</p>
</dd>
<dt><a href="#CURRENT">CURRENT</a></dt>
<dd><p>Property holding the current context name</p>
</dd>
<dt><a href="#Updater">Updater</a></dt>
<dd><p>Create an Updater for the Error wrapper</p>
</dd>
<dt><a href="#E">E</a></dt>
<dd><p>Provides a wrapper to easily create classes of a certain name, and values</p>
</dd>
<dt><a href="#ACCESS_TOKEN">ACCESS_TOKEN</a></dt>
<dd><p>The constant string <code>access_token</code>.</p>
</dd>
<dt><a href="#REFRESH_TOKEN">REFRESH_TOKEN</a></dt>
<dd><p>The constant string <code>refresh_token</code>.</p>
</dd>
<dt><a href="#AUTHORIZATION_CODE">AUTHORIZATION_CODE</a></dt>
<dd><p>The constant string <code>authorization_code</code>.</p>
</dd>
<dt><a href="#CLIENT_CREDENTIALS">CLIENT_CREDENTIALS</a></dt>
<dd><p>The constant string <code>client_credentials</code>.</p>
</dd>
<dt><a href="#CLIENT_ID">CLIENT_ID</a></dt>
<dd><p>The constant string <code>client_id</code>.</p>
</dd>
<dt><a href="#CLIENT_SECRET">CLIENT_SECRET</a></dt>
<dd><p>The constant string <code>client_secret</code>.</p>
</dd>
<dt><a href="#SCOPE">SCOPE</a></dt>
<dd><p>The constant string <code>scope</code>.</p>
</dd>
</dl>

## Functions

<dl>
<dt><a href="#_sendPost">_sendPost(postUrl, token, postData)</a> ⇒ <code>Promise</code></dt>
<dd><p>Send a request via POST.</p>
</dd>
<dt><a href="#getTokenData">getTokenData(token)</a> ⇒ <code>object</code></dt>
<dd><p>Returns the decoded token value as JavaScript object.</p>
</dd>
</dl>

<a name="module_aio-lib-ims"></a>

## aio-lib-ims
The `@adobe/aio-lib-ims` module offers three kinds of elements:1. Managing configuration contexts for token creation and use2. Creating and invalidating tokens3. Providing low level access to IMS API


* [aio-lib-ims](#module_aio-lib-ims)
    * [.getTokenData](#module_aio-lib-ims.getTokenData)
    * [.Ims](#module_aio-lib-ims.Ims)
    * [.ACCESS_TOKEN](#module_aio-lib-ims.ACCESS_TOKEN)
    * [.REFRESH_TOKEN](#module_aio-lib-ims.REFRESH_TOKEN)
    * [.AUTHORIZATION_CODE](#module_aio-lib-ims.AUTHORIZATION_CODE)
    * [.CLIENT_ID](#module_aio-lib-ims.CLIENT_ID)
    * [.CLIENT_SECRET](#module_aio-lib-ims.CLIENT_SECRET)
    * [.SCOPE](#module_aio-lib-ims.SCOPE)
    * [.context](#module_aio-lib-ims.context)
    * [.getToken(contextName, options)](#module_aio-lib-ims.getToken) ⇒ <code>Promise</code>
    * [.invalidateToken(contextName, [force])](#module_aio-lib-ims.invalidateToken) ⇒ <code>Promise</code>

<a name="module_aio-lib-ims.getTokenData"></a>

### aio-lib-ims.getTokenData
**Kind**: static property of [<code>aio-lib-ims</code>](#module_aio-lib-ims)  
**See**: [`getTokenData`](#gettokendata)  
<a name="module_aio-lib-ims.Ims"></a>

### aio-lib-ims.Ims
**Kind**: static property of [<code>aio-lib-ims</code>](#module_aio-lib-ims)  
**See**: [`Ims`](#ims)  
<a name="module_aio-lib-ims.ACCESS_TOKEN"></a>

### aio-lib-ims.ACCESS\_TOKEN
**Kind**: static property of [<code>aio-lib-ims</code>](#module_aio-lib-ims)  
**See**: [`ACCESS_TOKEN`](#access_token)  
<a name="module_aio-lib-ims.REFRESH_TOKEN"></a>

### aio-lib-ims.REFRESH\_TOKEN
**Kind**: static property of [<code>aio-lib-ims</code>](#module_aio-lib-ims)  
**See**: [`REFRESH_TOKEN`](#refresh_token)  
<a name="module_aio-lib-ims.AUTHORIZATION_CODE"></a>

### aio-lib-ims.AUTHORIZATION\_CODE
**Kind**: static property of [<code>aio-lib-ims</code>](#module_aio-lib-ims)  
**See**: [`AUTHORIZATION_CODE`](#authorization_code)  
<a name="module_aio-lib-ims.CLIENT_ID"></a>

### aio-lib-ims.CLIENT\_ID
**Kind**: static property of [<code>aio-lib-ims</code>](#module_aio-lib-ims)  
**See**: [`CLIENT_ID`](#client_id)  
<a name="module_aio-lib-ims.CLIENT_SECRET"></a>

### aio-lib-ims.CLIENT\_SECRET
**Kind**: static property of [<code>aio-lib-ims</code>](#module_aio-lib-ims)  
**See**: [`CLIENT_SECRET`](#client_secret)  
<a name="module_aio-lib-ims.SCOPE"></a>

### aio-lib-ims.SCOPE
**Kind**: static property of [<code>aio-lib-ims</code>](#module_aio-lib-ims)  
**See**: [`SCOPE`](#scope)  
<a name="module_aio-lib-ims.context"></a>

### aio-lib-ims.context
**Kind**: static property of [<code>aio-lib-ims</code>](#module_aio-lib-ims)  
**See**: [`Context`](#context)  
<a name="module_aio-lib-ims.getToken"></a>

### aio-lib-ims.getToken(contextName, options) ⇒ <code>Promise</code>
Returns an access token for the given context name. When running in Adobe I/O Runtimetokens will be persisted in the [`State SDK`](https://github.com/adobe/aio-lib-state).

**Kind**: static method of [<code>aio-lib-ims</code>](#module_aio-lib-ims)  
**Returns**: <code>Promise</code> - Resolving to an access token (string)  

| Param | Type | Description |
| --- | --- | --- |
| contextName | <code>string</code> | The name of the IMS context for which to return the              access token. If this is empty, the token(s) of the current IMS context              are invalidated. |
| options | <code>object</code> | A set of arbitrary options which will be passed to the underlying login plugin. |

<a name="module_aio-lib-ims.invalidateToken"></a>

### aio-lib-ims.invalidateToken(contextName, [force]) ⇒ <code>Promise</code>
Invalidates the access and optionally refresh of an IMS context.The name of the IMS context is given as its first parameter and defaultsto the current context if missing or empty. The force parameter indicateswhether only the access token is invalidated (force=false) or the refreshtoken (if existing) is also invalidated (force=true). If the refresh tokenexists and is validated, all access tokens which have been created withthis refresh token will automatically become invalid as well.

**Kind**: static method of [<code>aio-lib-ims</code>](#module_aio-lib-ims)  
**Returns**: <code>Promise</code> - Promise that resolves with the request data  

| Param | Type | Description |
| --- | --- | --- |
| contextName | <code>string</code> | The name of the IMS context for which to              invalidate the token(s). If this is empty, the token(s) of              the current IMS context are invalidated. |
| [force] | <code>boolean</code> | Whether to invalidate just the access token or              to also invalidate the refresh token. Defaults to `false`. |

<a name="Ims"></a>

## Ims
The `Ims` class wraps the IMS API.

**Kind**: global class  

* [Ims](#Ims)
    * [new Ims(env)](#new_Ims_new)
    * _instance_
        * [.getApiUrl(api)](#Ims+getApiUrl) ⇒ <code>string</code>
        * [.getSusiUrl(clientId, scopes, callbackUrl, state)](#Ims+getSusiUrl) ⇒ <code>string</code>
        * [.get(api, token, parameters)](#Ims+get) ⇒ <code>Promise</code>
        * [.post(api, token, parameters)](#Ims+post) ⇒ <code>Promise</code>
        * [.getAccessToken(authCode, clientId, clientSecret, scopes)](#Ims+getAccessToken) ⇒ <code>Promise</code>
        * [.getAccessTokenByClientCredentials(clientId, clientSecret, orgId, scopes)](#Ims+getAccessTokenByClientCredentials) ⇒ <code>Promise</code>
        * [.exchangeJwtToken(clientId, clientSecret, signedJwtToken)](#Ims+exchangeJwtToken) ⇒ <code>Promise</code>
        * [.invalidateToken(token, clientId, clientSecret)](#Ims+invalidateToken) ⇒ <code>Promise</code>
        * [.validateToken(token, [clientId])](#Ims+validateToken) ⇒ <code>object</code>
        * [.getOrganizations(token)](#Ims+getOrganizations) ⇒ <code>object</code>
        * [.toTokenResult(token)](#Ims+toTokenResult) ⇒ <code>Promise</code>
    * _static_
        * [.fromToken(token)](#Ims.fromToken) ⇒ <code>Promise</code>

<a name="new_Ims_new"></a>

### new Ims(env)
Creates a new IMS connector instance for the stage or prod environment


| Param | Type | Description |
| --- | --- | --- |
| env | <code>string</code> | The name of the environment. `prod` and `stage`      are the only values supported. `prod` is default and any value      other than `prod` or `stage` it is assumed to be the default      value of `prod`. If not set, it will get the global cli env value. See https://github.com/adobe/aio-lib-env      (which defaults to `prod` as well if not set) |

<a name="Ims+getApiUrl"></a>

### ims.getApiUrl(api) ⇒ <code>string</code>
Returns the absolute URL to call the indicated API.The API is expected to be the API absolute path, such as `/ims/profile`.To form the absolute URL, the scheme (`https`) and fully qualifieddomain of the IMS host for this instance's environment is prependedto the path.

**Kind**: instance method of [<code>Ims</code>](#Ims)  
**Returns**: <code>string</code> - The absolute URI for the IMS API  

| Param | Type | Description |
| --- | --- | --- |
| api | <code>string</code> | The API (path) for which to return the URL |

<a name="Ims+getSusiUrl"></a>

### ims.getSusiUrl(clientId, scopes, callbackUrl, state) ⇒ <code>string</code>
Returns the URL for the environment of this instance which allowsfor OAuth2 based three-legged authentication with a browser foran end user.

**Kind**: instance method of [<code>Ims</code>](#Ims)  
**Returns**: <code>string</code> - the OAuth2 login URL  

| Param | Type | Description |
| --- | --- | --- |
| clientId | <code>string</code> | The Client ID |
| scopes | <code>string</code> | The list of scopes to request as a blank separated list |
| callbackUrl | <code>string</code> | The callback URL after the user signed in |
| state | <code>string</code> | Any state value which is passed back from sign in |

<a name="Ims+get"></a>

### ims.get(api, token, parameters) ⇒ <code>Promise</code>
Send a `GET` request to an IMS API with the access token sendingthe `parameters` as request URL parameters.

**Kind**: instance method of [<code>Ims</code>](#Ims)  
**Returns**: <code>Promise</code> - a promise resolving to the result of the request  

| Param | Type | Description |
| --- | --- | --- |
| api | <code>string</code> | The IMS API to `GET` from, e.g. `/ims/profile/v1` |
| token | <code>string</code> | The IMS access token to call the API |
| parameters | <code>Map</code> | A map of request parameters |

<a name="Ims+post"></a>

### ims.post(api, token, parameters) ⇒ <code>Promise</code>
Send a `POST` request to an IMS API with the access token sendingthe `parameters` as form data.

**Kind**: instance method of [<code>Ims</code>](#Ims)  
**Returns**: <code>Promise</code> - a promise resolving to the result of the request  

| Param | Type | Description |
| --- | --- | --- |
| api | <code>string</code> | The IMS API to `POST` to, e.g. `/ims/profile/v1` |
| token | <code>string</code> | The IMS access token to call the API |
| parameters | <code>Map</code> | A map of request parameters |

<a name="Ims+getAccessToken"></a>

### ims.getAccessToken(authCode, clientId, clientSecret, scopes) ⇒ <code>Promise</code>
Request the access token for the given client providing the accessgrant in the `authCode`.The promise resolve to the token result JavaScript object as follows:```js{  access_token: {    token: "eyJ4NXUiOi...6ZodTesbag",    expiry: 1566242851048  },  refresh_token: {    token: "eyJ4NXUiOi...YbT1_szWZA",    expiry: 1567366051050  },  payload: {     ...full api response...  }}```

**Kind**: instance method of [<code>Ims</code>](#Ims)  
**Returns**: <code>Promise</code> - a promise resolving to a tokens object as described in the     [toTokenResult](toTokenResult) or rejects to an error message.  

| Param | Type | Description |
| --- | --- | --- |
| authCode | <code>string</code> | The authorization code received from the OAuth2      sign in page or by some other means. This may also be a refresh      token which may be traded for a new access token. |
| clientId | <code>string</code> | The Client ID |
| clientSecret | <code>string</code> | The Client Secrete proving client ID ownership |
| scopes | <code>string</code> | The list of scopes to request as a blank separated list |

<a name="Ims+getAccessTokenByClientCredentials"></a>

### ims.getAccessTokenByClientCredentials(clientId, clientSecret, orgId, scopes) ⇒ <code>Promise</code>
Request an access token of the Client Credentials Grant Type.

**Kind**: instance method of [<code>Ims</code>](#Ims)  
**Returns**: <code>Promise</code> - a promise resolving to a tokens object as described in the     [toTokenResult](toTokenResult) or rejects to an error message.  

| Param | Type | Description |
| --- | --- | --- |
| clientId | <code>string</code> | The Client ID |
| clientSecret | <code>string</code> | The Client Secret proving client ID ownership |
| orgId | <code>string</code> | the IMS org Id |
| scopes | <code>Array.&lt;string&gt;</code> | The list of scopes to request as a blank separated list |

<a name="Ims+exchangeJwtToken"></a>

### ims.exchangeJwtToken(clientId, clientSecret, signedJwtToken) ⇒ <code>Promise</code>
Asks for the signed JWT token to be exchanged for a valid accesstoken as well as a refresh token.The promise resolve to the token result JavaScript object as follows:```js{  access_token: {    token: "eyJ4NXUiOi...6ZodTesbag",    expiry: 1566242851048  },  payload: {     ...full api response...  }}```Note that there is no `refresh_token` in a JWT token exchange.

**Kind**: instance method of [<code>Ims</code>](#Ims)  
**Returns**: <code>Promise</code> - returns a Promise that resolves to the token result object  

| Param | Type | Description |
| --- | --- | --- |
| clientId | <code>string</code> | The client ID of the owning application |
| clientSecret | <code>string</code> | The client's secret |
| signedJwtToken | <code>string</code> | The properly signed JWT token for the JWT token exchange |

<a name="Ims+invalidateToken"></a>

### ims.invalidateToken(token, clientId, clientSecret) ⇒ <code>Promise</code>
Invalidates the given token. If the token is a refresh token, all theaccess tokens created with that refresh token will also be invalidatedat the same time.

**Kind**: instance method of [<code>Ims</code>](#Ims)  
**Returns**: <code>Promise</code> - Promise that resolves with the request data  

| Param | Type | Description |
| --- | --- | --- |
| token | <code>string</code> | the access token |
| clientId | <code>string</code> | the client id |
| clientSecret | <code>string</code> | the client secret |

<a name="Ims+validateToken"></a>

### ims.validateToken(token, [clientId]) ⇒ <code>object</code>
Verifies a given token.

**Kind**: instance method of [<code>Ims</code>](#Ims)  
**Returns**: <code>object</code> - the server response  

| Param | Type | Description |
| --- | --- | --- |
| token | <code>string</code> | the access token |
| [clientId] | <code>string</code> | the client id, optional |

<a name="Ims+getOrganizations"></a>

### ims.getOrganizations(token) ⇒ <code>object</code>
Gets the IMS organizations attached to the given token.

**Kind**: instance method of [<code>Ims</code>](#Ims)  
**Returns**: <code>object</code> - the server response  

| Param | Type | Description |
| --- | --- | --- |
| token | <code>string</code> | the access token |

<a name="Ims+toTokenResult"></a>

### ims.toTokenResult(token) ⇒ <code>Promise</code>
Converts the access token to a token result object as follows:```js{  access_token: {    token: "eyJ4NXUiOi...6ZodTesbag",    expiry: 1566242851048  }}```The `expiry` property is the expiry time of the token in millisecondssince the epoch.

**Kind**: instance method of [<code>Ims</code>](#Ims)  
**Returns**: <code>Promise</code> - a `Promise` resolving to an object as described.  

| Param | Type | Description |
| --- | --- | --- |
| token | <code>string</code> | The access token to wrap into a token result |

<a name="Ims.fromToken"></a>

### Ims.fromToken(token) ⇒ <code>Promise</code>
Creates an instance of the `Ims` class deriving the instance'senvironment from the `as` claim in the provided access token.

**Kind**: static method of [<code>Ims</code>](#Ims)  
**Returns**: <code>Promise</code> - A `Promise` resolving to the `Ims` instance.  

| Param | Type | Description |
| --- | --- | --- |
| token | <code>string</code> | The access token from which to extract the      environment to setup the `Ims` instancee. |

<a name="ConfigCliContext"></a>

## ConfigCliContext
The `ConfigCliContext` class stores IMS `contexts` for the Adobe I/O CLI in the local filesystem using the Adobe I/O Core Configuration Library.

**Kind**: global class  

* [ConfigCliContext](#ConfigCliContext)
    * [.getCli()](#ConfigCliContext+getCli) ⇒ <code>Promise.&lt;any&gt;</code>
    * [.setCli(contextData, [local], [merge])](#ConfigCliContext+setCli)

<a name="ConfigCliContext+getCli"></a>

### configCliContext.getCli() ⇒ <code>Promise.&lt;any&gt;</code>
Gets the cli context data

**Kind**: instance method of [<code>ConfigCliContext</code>](#ConfigCliContext)  
**Returns**: <code>Promise.&lt;any&gt;</code> - the cli context data  
<a name="ConfigCliContext+setCli"></a>

### configCliContext.setCli(contextData, [local], [merge])
Sets the cli context data

**Kind**: instance method of [<code>ConfigCliContext</code>](#ConfigCliContext)  

| Param | Type | Default | Description |
| --- | --- | --- | --- |
| contextData | <code>object</code> |  | the data to save |
| [local] | <code>boolean</code> | <code>false</code> | set to true to save to local config, false for global config |
| [merge] | <code>boolean</code> | <code>true</code> | set to true to merge existing data with the new data |

<a name="Context"></a>

## Context
The `Context` abstract class provides an interface to manage the IMS configuration contexts on behalf ofthe Adobe I/O Lib IMS Library.

**Kind**: global class  

* [Context](#Context)
    * [.getCurrent()](#Context+getCurrent) ⇒ <code>Promise.&lt;string&gt;</code>
    * [.setCurrent(contextName)](#Context+setCurrent) ⇒ <code>Promise.&lt;any&gt;</code>
    * [.get(contextName)](#Context+get) ⇒ <code>Promise.&lt;object&gt;</code>
    * [.set(contextName, contextData, local)](#Context+set)
    * [.keys()](#Context+keys) ⇒ <code>Promise.&lt;Array.&lt;string&gt;&gt;</code>

<a name="Context+getCurrent"></a>

### context.getCurrent() ⇒ <code>Promise.&lt;string&gt;</code>
Gets the current context name.

**Kind**: instance method of [<code>Context</code>](#Context)  
**Returns**: <code>Promise.&lt;string&gt;</code> - the current context name  
<a name="Context+setCurrent"></a>

### context.setCurrent(contextName) ⇒ <code>Promise.&lt;any&gt;</code>
Sets the current context name in the local configuration

**Kind**: instance method of [<code>Context</code>](#Context)  
**Returns**: <code>Promise.&lt;any&gt;</code> - returns an instance of the Config object  

| Param | Type | Description |
| --- | --- | --- |
| contextName | <code>string</code> | The name of the context to use as the current context |

<a name="Context+get"></a>

### context.get(contextName) ⇒ <code>Promise.&lt;object&gt;</code>
Returns an object representing the named context.If the contextName parameter is empty or missing, it defaults to thecurrent context name. The result is an object with two properties:  - `name`: The actual context name used  - `data`: The IMS context data

**Kind**: instance method of [<code>Context</code>](#Context)  
**Returns**: <code>Promise.&lt;object&gt;</code> - The configuration object  

| Param | Type | Description |
| --- | --- | --- |
| contextName | <code>string</code> | Name of the context information to return. |

<a name="Context+set"></a>

### context.set(contextName, contextData, local)
Updates the named configuration with new configuration data. If a configurationobject for the named context already exists it is completely replaced with this newconfiguration.

**Kind**: instance method of [<code>Context</code>](#Context)  

| Param | Type | Default | Description |
| --- | --- | --- | --- |
| contextName | <code>string</code> |  | Name of the context to update |
| contextData | <code>object</code> |  | The configuration data to store for the context |
| local | <code>boolean</code> | <code>false</code> | Persist in local or global configuration. When running in      Adobe I/O Runtime, this has no effect unless `contextData` contains an      `access_token` or `refresh_token` field, in which case setting `local=true` will      prevent the persistence of those fields in the [`State      SDK`](https://github.com/adobe/aio-lib-state). Please note that when calling      `getToken` in an I/O Runtime Action, generated tokens will always be persisted      as `getToken` internally calls `context.set` with `local=false`. |

<a name="Context+keys"></a>

### context.keys() ⇒ <code>Promise.&lt;Array.&lt;string&gt;&gt;</code>
Returns the names of the configured contexts as an array of strings.

**Kind**: instance method of [<code>Context</code>](#Context)  
**Returns**: <code>Promise.&lt;Array.&lt;string&gt;&gt;</code> - The names of the currently known configurations.  
<a name="StateActionContext"></a>

## StateActionContext
The `StateActionContext` class stores IMS `contexts` for Adobe I/O Runtime Actions in thecloud using the Adobe I/O State Library.

**Kind**: global class  
<a name="TYPE_ACTION"></a>

## TYPE\_ACTION
Name of context type action

**Kind**: global constant  
<a name="TYPE_CLI"></a>

## TYPE\_CLI
Name of context type cli

**Kind**: global constant  
<a name="IMS"></a>

## IMS
Name of the IMS configuration context data structure

**Kind**: global constant  
<a name="CONTEXTS"></a>

## CONTEXTS
Property holding an object with all contexts

**Kind**: global constant  
<a name="CONFIG"></a>

## CONFIG
Property holding an object with context management configuration

**Kind**: global constant  
<a name="CLI"></a>

## CLI
Property holding the cli context name

**Kind**: global constant  
<a name="CURRENT"></a>

## CURRENT
Property holding the current context name

**Kind**: global constant  
<a name="Updater"></a>

## Updater
Create an Updater for the Error wrapper

**Kind**: global constant  
<a name="E"></a>

## E
Provides a wrapper to easily create classes of a certain name, and values

**Kind**: global constant  
<a name="ACCESS_TOKEN"></a>

## ACCESS\_TOKEN
The constant string `access_token`.

**Kind**: global constant  
<a name="REFRESH_TOKEN"></a>

## REFRESH\_TOKEN
The constant string `refresh_token`.

**Kind**: global constant  
<a name="AUTHORIZATION_CODE"></a>

## AUTHORIZATION\_CODE
The constant string `authorization_code`.

**Kind**: global constant  
<a name="CLIENT_CREDENTIALS"></a>

## CLIENT\_CREDENTIALS
The constant string `client_credentials`.

**Kind**: global constant  
<a name="CLIENT_ID"></a>

## CLIENT\_ID
The constant string `client_id`.

**Kind**: global constant  
<a name="CLIENT_SECRET"></a>

## CLIENT\_SECRET
The constant string `client_secret`.

**Kind**: global constant  
<a name="SCOPE"></a>

## SCOPE
The constant string `scope`.

**Kind**: global constant  
<a name="_sendPost"></a>

## \_sendPost(postUrl, token, postData) ⇒ <code>Promise</code>
Send a request via POST.

**Kind**: global function  
**Returns**: <code>Promise</code> - Promise that resolves with the request data  

| Param | Type | Description |
| --- | --- | --- |
| postUrl | <code>string</code> | the url endpoint |
| token | <code>string</code> | the authorization token |
| postData | <code>object</code> | the data to send |

<a name="getTokenData"></a>

## getTokenData(token) ⇒ <code>object</code>
Returns the decoded token value as JavaScript object.

**Kind**: global function  
**Returns**: <code>object</code> - The decoded token payload data without header and signature  

| Param | Type | Description |
| --- | --- | --- |
| token | <code>string</code> | The token to decode and extract the token value from |

