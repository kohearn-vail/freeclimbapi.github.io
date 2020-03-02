# Freeclimb::DefaultApi

All URIs are relative to *https://www.freeclimb.com/apiserver*

Method | HTTP request | Description
------------- | ------------- | -------------
[**buy_a_phone_number**](DefaultApi.md#buy_a_phone_number) | **POST** /Accounts/{accountId}/IncomingPhoneNumbers | Buy a Phone Number
[**create_a_conference**](DefaultApi.md#create_a_conference) | **POST** /Accounts/{accountId}/Conferences | Create a Conference
[**create_a_queue**](DefaultApi.md#create_a_queue) | **POST** /Accounts/{accountId}/Queues | Create a Queue
[**create_an_application**](DefaultApi.md#create_an_application) | **POST** /Accounts/{accountId}/Applications | Create an application
[**delete_a_recording**](DefaultApi.md#delete_a_recording) | **DELETE** /Accounts/{accountId}/Recordings/{recordingId} | Delete a Recording
[**delete_an_application**](DefaultApi.md#delete_an_application) | **DELETE** /Accounts/{accountId}/Applications/{applicationId} | Delete an application
[**delete_an_incoming_number**](DefaultApi.md#delete_an_incoming_number) | **DELETE** /Accounts/{accountId}/IncomingPhoneNumbers/{phoneNumberId} | Delete an Incoming Number
[**dequeue_a_member**](DefaultApi.md#dequeue_a_member) | **POST** /Accounts/{accountId}/Queues/{queueId}/Members/{callId} | Dequeue a Member
[**dequeue_head_member**](DefaultApi.md#dequeue_head_member) | **POST** /Accounts/{accountId}/Queues/{queueId}/Members/Front | Dequeue Head Member
[**download_a_recording_file**](DefaultApi.md#download_a_recording_file) | **GET** /Accounts/{accountId}/Recordings/{recordingId}/Download | Download a Recording File
[**filter_logs**](DefaultApi.md#filter_logs) | **POST** /Accounts/{accountId}/Logs | Filter Logs
[**get_a_call**](DefaultApi.md#get_a_call) | **GET** /Accounts/{accountId}/Calls/{callId} | Get a Call
[**get_a_conference**](DefaultApi.md#get_a_conference) | **GET** /Accounts/{accountId}/Conferences/{conferenceId} | Get a Conference
[**get_a_member**](DefaultApi.md#get_a_member) | **GET** /Accounts/{accountId}/Queues/{queueId}/Members/{callId} | Get a Member
[**get_a_participant**](DefaultApi.md#get_a_participant) | **GET** /Accounts/{accountId}/Conferences/{conferenceId}/Participants/{callId} | Get a Participant
[**get_a_queue**](DefaultApi.md#get_a_queue) | **GET** /Accounts/{accountId}/Queues/{queueId} | Get a Queue
[**get_a_recording**](DefaultApi.md#get_a_recording) | **GET** /Accounts/{accountId}/Recordings/{recordingId} | Get a Recording
[**get_an_account**](DefaultApi.md#get_an_account) | **GET** /Accounts/{accountId} | Get an Account
[**get_an_application**](DefaultApi.md#get_an_application) | **GET** /Accounts/{accountId}/Applications/{applicationId} | Get an Application
[**get_an_incoming_number**](DefaultApi.md#get_an_incoming_number) | **GET** /Accounts/{accountId}/IncomingPhoneNumbers/{phoneNumberId} | Get an Incoming Number
[**get_an_sms_message**](DefaultApi.md#get_an_sms_message) | **GET** /Accounts/{accountId}/Messages/{messageId} | Get an SMS Message
[**get_head_member**](DefaultApi.md#get_head_member) | **GET** /Accounts/{accountId}/Queues/{queueId}/Members/Front | Get Head Member
[**list_active_queues**](DefaultApi.md#list_active_queues) | **GET** /Accounts/{accountId}/Queues | List Active Queues
[**list_all_account_logs**](DefaultApi.md#list_all_account_logs) | **GET** /Accounts/{accountId}/Logs | List All Account Logs
[**list_an_application**](DefaultApi.md#list_an_application) | **GET** /Accounts/{accountId}/Applications | List applications
[**list_available_numbers**](DefaultApi.md#list_available_numbers) | **GET** /AvailablePhoneNumbers | List available numbers
[**list_call_logs**](DefaultApi.md#list_call_logs) | **GET** /Accounts/{accountId}/Calls/{callId}/Logs | List Call Logs
[**list_call_recordings**](DefaultApi.md#list_call_recordings) | **GET** /Accounts/{accountId}/Calls/{callId}/Recordings | List Call Recordings
[**list_calls**](DefaultApi.md#list_calls) | **GET** /Accounts/{accountId}/Calls | List Calls
[**list_conferences**](DefaultApi.md#list_conferences) | **GET** /Accounts/{accountId}/Conferences | List Conferences
[**list_incoming_numbers**](DefaultApi.md#list_incoming_numbers) | **GET** /Accounts/{accountId}/IncomingPhoneNumbers | List Incoming Numbers
[**list_members**](DefaultApi.md#list_members) | **GET** /Accounts/{accountId}/Queues/{queueId}/Members | List Members
[**list_participants**](DefaultApi.md#list_participants) | **GET** /Accounts/{accountId}/Conferences/{conferenceId}/Participants | List Participants
[**list_recordings**](DefaultApi.md#list_recordings) | **GET** /Accounts/{accountId}/Recordings | List Recordings
[**list_sms_messages**](DefaultApi.md#list_sms_messages) | **GET** /Accounts/{accountId}/Messages | List SMS Messages
[**make_a_call**](DefaultApi.md#make_a_call) | **POST** /Accounts/{accountId}/Calls | Make a Call
[**remove_a_participant**](DefaultApi.md#remove_a_participant) | **DELETE** /Accounts/{accountId}/Conferences/{conferenceId}/Participants/{callId} | Remove a Participant
[**send_an_sms_message**](DefaultApi.md#send_an_sms_message) | **POST** /Accounts/{accountId}/Messages | Send an SMS Message
[**stream_a_recording_file**](DefaultApi.md#stream_a_recording_file) | **GET** /Accounts/{accountId}/Recordings/{recordingId}/Stream | Stream a Recording File
[**update_a_conference**](DefaultApi.md#update_a_conference) | **POST** /Accounts/{accountId}/Conferences/{conferenceId} | Update a Conference
[**update_a_live_call**](DefaultApi.md#update_a_live_call) | **POST** /Accounts/{accountId}/Calls/{callId} | Update a Live Call
[**update_a_participant**](DefaultApi.md#update_a_participant) | **POST** /Accounts/{accountId}/Conferences/{conferenceId}/Participants/{callId} | Update a Participant
[**update_a_queue**](DefaultApi.md#update_a_queue) | **POST** /Accounts/{accountId}/Queues/{queueId} | Update a Queue
[**update_an_account**](DefaultApi.md#update_an_account) | **POST** /Accounts/{accountId} | Manage an account
[**update_an_application**](DefaultApi.md#update_an_application) | **POST** /Accounts/{accountId}/Applications/{applicationId} | Update an application
[**update_an_incoming_number**](DefaultApi.md#update_an_incoming_number) | **POST** /Accounts/{accountId}/IncomingPhoneNumbers/{phoneNumberId} | Update an Incoming Number



## buy_a_phone_number

> IncomingNumberResult buy_a_phone_number(opts)

Buy a Phone Number

### Example

```ruby
# load the gem
require 'freeclimb'
# setup authorization
Freeclimb.configure do |config|
  # Configure HTTP basic authorization: fc
  config.username = 'ACCOUNT ID'
  config.password = 'AUTH TOKEN'
end

api_instance = Freeclimb::DefaultApi.new
opts = {
  buy_incoming_number_request: Freeclimb::BuyIncomingNumberRequest.new # BuyIncomingNumberRequest | Incoming Number transaction details
}

begin
  #Buy a Phone Number
  result = api_instance.buy_a_phone_number(opts)
  p result
rescue Freeclimb::ApiError => e
  puts "Exception when calling DefaultApi->buy_a_phone_number: #{e}"
end
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **buy_incoming_number_request** | [**BuyIncomingNumberRequest**](BuyIncomingNumberRequest.md)| Incoming Number transaction details | [optional] 

### Return type

[**IncomingNumberResult**](IncomingNumberResult.md)

### Authorization

[fc](../README.md#fc)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## create_a_conference

> ConferenceResult create_a_conference(opts)

Create a Conference

### Example

```ruby
# load the gem
require 'freeclimb'
# setup authorization
Freeclimb.configure do |config|
  # Configure HTTP basic authorization: fc
  config.username = 'ACCOUNT ID'
  config.password = 'AUTH TOKEN'
end

api_instance = Freeclimb::DefaultApi.new
opts = {
  create_conference_request: Freeclimb::CreateConferenceRequest.new # CreateConferenceRequest | Conference to create
}

begin
  #Create a Conference
  result = api_instance.create_a_conference(opts)
  p result
rescue Freeclimb::ApiError => e
  puts "Exception when calling DefaultApi->create_a_conference: #{e}"
end
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **create_conference_request** | [**CreateConferenceRequest**](CreateConferenceRequest.md)| Conference to create | [optional] 

### Return type

[**ConferenceResult**](ConferenceResult.md)

### Authorization

[fc](../README.md#fc)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## create_a_queue

> QueueResult create_a_queue(opts)

Create a Queue

### Example

```ruby
# load the gem
require 'freeclimb'
# setup authorization
Freeclimb.configure do |config|
  # Configure HTTP basic authorization: fc
  config.username = 'ACCOUNT ID'
  config.password = 'AUTH TOKEN'
end

api_instance = Freeclimb::DefaultApi.new
opts = {
  queue_request: Freeclimb::QueueRequest.new # QueueRequest | Queue details used to create a queue
}

begin
  #Create a Queue
  result = api_instance.create_a_queue(opts)
  p result
rescue Freeclimb::ApiError => e
  puts "Exception when calling DefaultApi->create_a_queue: #{e}"
end
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **queue_request** | [**QueueRequest**](QueueRequest.md)| Queue details used to create a queue | [optional] 

### Return type

[**QueueResult**](QueueResult.md)

### Authorization

[fc](../README.md#fc)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## create_an_application

> ApplicationResult create_an_application(opts)

Create an application

### Example

```ruby
# load the gem
require 'freeclimb'
# setup authorization
Freeclimb.configure do |config|
  # Configure HTTP basic authorization: fc
  config.username = 'ACCOUNT ID'
  config.password = 'AUTH TOKEN'
end

api_instance = Freeclimb::DefaultApi.new
opts = {
  application_request: Freeclimb::ApplicationRequest.new # ApplicationRequest | Application Details
}

begin
  #Create an application
  result = api_instance.create_an_application(opts)
  p result
rescue Freeclimb::ApiError => e
  puts "Exception when calling DefaultApi->create_an_application: #{e}"
end
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **application_request** | [**ApplicationRequest**](ApplicationRequest.md)| Application Details | [optional] 

### Return type

[**ApplicationResult**](ApplicationResult.md)

### Authorization

[fc](../README.md#fc)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## delete_a_recording

> delete_a_recording(recording_id)

Delete a Recording

### Example

```ruby
# load the gem
require 'freeclimb'
# setup authorization
Freeclimb.configure do |config|
  # Configure HTTP basic authorization: fc
  config.username = 'ACCOUNT ID'
  config.password = 'AUTH TOKEN'
end

api_instance = Freeclimb::DefaultApi.new
recording_id = 'recording_id_example' # String | String that uniquely identifies this recording resource.

begin
  #Delete a Recording
  api_instance.delete_a_recording(recording_id)
rescue Freeclimb::ApiError => e
  puts "Exception when calling DefaultApi->delete_a_recording: #{e}"
end
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **recording_id** | **String**| String that uniquely identifies this recording resource. | 

### Return type

nil (empty response body)

### Authorization

[fc](../README.md#fc)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: Not defined


## delete_an_application

> delete_an_application(application_id)

Delete an application

### Example

```ruby
# load the gem
require 'freeclimb'
# setup authorization
Freeclimb.configure do |config|
  # Configure HTTP basic authorization: fc
  config.username = 'ACCOUNT ID'
  config.password = 'AUTH TOKEN'
end

api_instance = Freeclimb::DefaultApi.new
application_id = 'application_id_example' # String | String that uniquely identifies this application resource.

begin
  #Delete an application
  api_instance.delete_an_application(application_id)
rescue Freeclimb::ApiError => e
  puts "Exception when calling DefaultApi->delete_an_application: #{e}"
end
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **application_id** | **String**| String that uniquely identifies this application resource. | 

### Return type

nil (empty response body)

### Authorization

[fc](../README.md#fc)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: Not defined


## delete_an_incoming_number

> delete_an_incoming_number(phone_number_id)

Delete an Incoming Number

### Example

```ruby
# load the gem
require 'freeclimb'
# setup authorization
Freeclimb.configure do |config|
  # Configure HTTP basic authorization: fc
  config.username = 'ACCOUNT ID'
  config.password = 'AUTH TOKEN'
end

api_instance = Freeclimb::DefaultApi.new
phone_number_id = 'phone_number_id_example' # String | String that uniquely identifies this phone number resource.

begin
  #Delete an Incoming Number
  api_instance.delete_an_incoming_number(phone_number_id)
rescue Freeclimb::ApiError => e
  puts "Exception when calling DefaultApi->delete_an_incoming_number: #{e}"
end
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **phone_number_id** | **String**| String that uniquely identifies this phone number resource. | 

### Return type

nil (empty response body)

### Authorization

[fc](../README.md#fc)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: Not defined


## dequeue_a_member

> QueueMember dequeue_a_member(queue_id, call_id, opts)

Dequeue a Member

### Example

```ruby
# load the gem
require 'freeclimb'
# setup authorization
Freeclimb.configure do |config|
  # Configure HTTP basic authorization: fc
  config.username = 'ACCOUNT ID'
  config.password = 'AUTH TOKEN'
end

api_instance = Freeclimb::DefaultApi.new
queue_id = 'queue_id_example' # String | String that uniquely identifies the Queue that the Member belongs to.
call_id = 'call_id_example' # String | ID if the Call that the Member belongs to
opts = {
  dequeue_member_request: Freeclimb::DequeueMemberRequest.new # DequeueMemberRequest | Dequeue member request details
}

begin
  #Dequeue a Member
  result = api_instance.dequeue_a_member(queue_id, call_id, opts)
  p result
rescue Freeclimb::ApiError => e
  puts "Exception when calling DefaultApi->dequeue_a_member: #{e}"
end
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **queue_id** | **String**| String that uniquely identifies the Queue that the Member belongs to. | 
 **call_id** | **String**| ID if the Call that the Member belongs to | 
 **dequeue_member_request** | [**DequeueMemberRequest**](DequeueMemberRequest.md)| Dequeue member request details | [optional] 

### Return type

[**QueueMember**](QueueMember.md)

### Authorization

[fc](../README.md#fc)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## dequeue_head_member

> QueueMember dequeue_head_member(queue_id, opts)

Dequeue Head Member

### Example

```ruby
# load the gem
require 'freeclimb'
# setup authorization
Freeclimb.configure do |config|
  # Configure HTTP basic authorization: fc
  config.username = 'ACCOUNT ID'
  config.password = 'AUTH TOKEN'
end

api_instance = Freeclimb::DefaultApi.new
queue_id = 'queue_id_example' # String | String that uniquely identifies this queue resource.
opts = {
  dequeue_member_request: Freeclimb::DequeueMemberRequest.new # DequeueMemberRequest | Dequeue head member request details
}

begin
  #Dequeue Head Member
  result = api_instance.dequeue_head_member(queue_id, opts)
  p result
rescue Freeclimb::ApiError => e
  puts "Exception when calling DefaultApi->dequeue_head_member: #{e}"
end
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **queue_id** | **String**| String that uniquely identifies this queue resource. | 
 **dequeue_member_request** | [**DequeueMemberRequest**](DequeueMemberRequest.md)| Dequeue head member request details | [optional] 

### Return type

[**QueueMember**](QueueMember.md)

### Authorization

[fc](../README.md#fc)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## download_a_recording_file

> File download_a_recording_file(recording_id)

Download a Recording File

### Example

```ruby
# load the gem
require 'freeclimb'
# setup authorization
Freeclimb.configure do |config|
  # Configure HTTP basic authorization: fc
  config.username = 'ACCOUNT ID'
  config.password = 'AUTH TOKEN'
end

api_instance = Freeclimb::DefaultApi.new
recording_id = 'recording_id_example' # String | String that uniquely identifies this recording resource.

begin
  #Download a Recording File
  result = api_instance.download_a_recording_file(recording_id)
  p result
rescue Freeclimb::ApiError => e
  puts "Exception when calling DefaultApi->download_a_recording_file: #{e}"
end
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **recording_id** | **String**| String that uniquely identifies this recording resource. | 

### Return type

**File**

### Authorization

[fc](../README.md#fc)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: audio/x-wav


## filter_logs

> LogList filter_logs(opts)

Filter Logs

### Example

```ruby
# load the gem
require 'freeclimb'
# setup authorization
Freeclimb.configure do |config|
  # Configure HTTP basic authorization: fc
  config.username = 'ACCOUNT ID'
  config.password = 'AUTH TOKEN'
end

api_instance = Freeclimb::DefaultApi.new
opts = {
  filter_logs_request: Freeclimb::FilterLogsRequest.new # FilterLogsRequest | Filter logs request paramters
}

begin
  #Filter Logs
  result = api_instance.filter_logs(opts)
  p result
rescue Freeclimb::ApiError => e
  puts "Exception when calling DefaultApi->filter_logs: #{e}"
end
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **filter_logs_request** | [**FilterLogsRequest**](FilterLogsRequest.md)| Filter logs request paramters | [optional] 

### Return type

[**LogList**](LogList.md)

### Authorization

[fc](../README.md#fc)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## get_a_call

> CallResult get_a_call(call_id)

Get a Call

### Example

```ruby
# load the gem
require 'freeclimb'
# setup authorization
Freeclimb.configure do |config|
  # Configure HTTP basic authorization: fc
  config.username = 'ACCOUNT ID'
  config.password = 'AUTH TOKEN'
end

api_instance = Freeclimb::DefaultApi.new
call_id = 'call_id_example' # String | String that uniquely identifies this call resource.

begin
  #Get a Call
  result = api_instance.get_a_call(call_id)
  p result
rescue Freeclimb::ApiError => e
  puts "Exception when calling DefaultApi->get_a_call: #{e}"
end
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **call_id** | **String**| String that uniquely identifies this call resource. | 

### Return type

[**CallResult**](CallResult.md)

### Authorization

[fc](../README.md#fc)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_a_conference

> ConferenceResult get_a_conference(conference_id)

Get a Conference

### Example

```ruby
# load the gem
require 'freeclimb'
# setup authorization
Freeclimb.configure do |config|
  # Configure HTTP basic authorization: fc
  config.username = 'ACCOUNT ID'
  config.password = 'AUTH TOKEN'
end

api_instance = Freeclimb::DefaultApi.new
conference_id = 'conference_id_example' # String | A string that uniquely identifies this conference resource.

begin
  #Get a Conference
  result = api_instance.get_a_conference(conference_id)
  p result
rescue Freeclimb::ApiError => e
  puts "Exception when calling DefaultApi->get_a_conference: #{e}"
end
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **conference_id** | **String**| A string that uniquely identifies this conference resource. | 

### Return type

[**ConferenceResult**](ConferenceResult.md)

### Authorization

[fc](../README.md#fc)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_a_member

> QueueMember get_a_member(queue_id, call_id)

Get a Member

### Example

```ruby
# load the gem
require 'freeclimb'
# setup authorization
Freeclimb.configure do |config|
  # Configure HTTP basic authorization: fc
  config.username = 'ACCOUNT ID'
  config.password = 'AUTH TOKEN'
end

api_instance = Freeclimb::DefaultApi.new
queue_id = 'queue_id_example' # String | String that uniquely identifies the Queue that the Member belongs to.
call_id = 'call_id_example' # String | ID of the Call that the Member belongs to

begin
  #Get a Member
  result = api_instance.get_a_member(queue_id, call_id)
  p result
rescue Freeclimb::ApiError => e
  puts "Exception when calling DefaultApi->get_a_member: #{e}"
end
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **queue_id** | **String**| String that uniquely identifies the Queue that the Member belongs to. | 
 **call_id** | **String**| ID of the Call that the Member belongs to | 

### Return type

[**QueueMember**](QueueMember.md)

### Authorization

[fc](../README.md#fc)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_a_participant

> ConferenceParticipantResult get_a_participant(conference_id, call_id)

Get a Participant

### Example

```ruby
# load the gem
require 'freeclimb'
# setup authorization
Freeclimb.configure do |config|
  # Configure HTTP basic authorization: fc
  config.username = 'ACCOUNT ID'
  config.password = 'AUTH TOKEN'
end

api_instance = Freeclimb::DefaultApi.new
conference_id = 'conference_id_example' # String | ID of the conference this participant is in.
call_id = 'call_id_example' # String | ID of the Call associated with this participant.

begin
  #Get a Participant
  result = api_instance.get_a_participant(conference_id, call_id)
  p result
rescue Freeclimb::ApiError => e
  puts "Exception when calling DefaultApi->get_a_participant: #{e}"
end
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **conference_id** | **String**| ID of the conference this participant is in. | 
 **call_id** | **String**| ID of the Call associated with this participant. | 

### Return type

[**ConferenceParticipantResult**](ConferenceParticipantResult.md)

### Authorization

[fc](../README.md#fc)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_a_queue

> QueueResult get_a_queue(queue_id)

Get a Queue

### Example

```ruby
# load the gem
require 'freeclimb'
# setup authorization
Freeclimb.configure do |config|
  # Configure HTTP basic authorization: fc
  config.username = 'ACCOUNT ID'
  config.password = 'AUTH TOKEN'
end

api_instance = Freeclimb::DefaultApi.new
queue_id = 'queue_id_example' # String | A string that uniquely identifies this queue resource.

begin
  #Get a Queue
  result = api_instance.get_a_queue(queue_id)
  p result
rescue Freeclimb::ApiError => e
  puts "Exception when calling DefaultApi->get_a_queue: #{e}"
end
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **queue_id** | **String**| A string that uniquely identifies this queue resource. | 

### Return type

[**QueueResult**](QueueResult.md)

### Authorization

[fc](../README.md#fc)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_a_recording

> RecordingResult get_a_recording(recording_id)

Get a Recording

### Example

```ruby
# load the gem
require 'freeclimb'
# setup authorization
Freeclimb.configure do |config|
  # Configure HTTP basic authorization: fc
  config.username = 'ACCOUNT ID'
  config.password = 'AUTH TOKEN'
end

api_instance = Freeclimb::DefaultApi.new
recording_id = 'recording_id_example' # String | String that uniquely identifies this recording resource.

begin
  #Get a Recording
  result = api_instance.get_a_recording(recording_id)
  p result
rescue Freeclimb::ApiError => e
  puts "Exception when calling DefaultApi->get_a_recording: #{e}"
end
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **recording_id** | **String**| String that uniquely identifies this recording resource. | 

### Return type

[**RecordingResult**](RecordingResult.md)

### Authorization

[fc](../README.md#fc)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_an_account

> AccountResult get_an_account

Get an Account

### Example

```ruby
# load the gem
require 'freeclimb'
# setup authorization
Freeclimb.configure do |config|
  # Configure HTTP basic authorization: fc
  config.username = 'ACCOUNT ID'
  config.password = 'AUTH TOKEN'
end

api_instance = Freeclimb::DefaultApi.new

begin
  #Get an Account
  result = api_instance.get_an_account
  p result
rescue Freeclimb::ApiError => e
  puts "Exception when calling DefaultApi->get_an_account: #{e}"
end
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**AccountResult**](AccountResult.md)

### Authorization

[fc](../README.md#fc)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_an_application

> ApplicationResult get_an_application(application_id)

Get an Application

### Example

```ruby
# load the gem
require 'freeclimb'
# setup authorization
Freeclimb.configure do |config|
  # Configure HTTP basic authorization: fc
  config.username = 'ACCOUNT ID'
  config.password = 'AUTH TOKEN'
end

api_instance = Freeclimb::DefaultApi.new
application_id = 'application_id_example' # String | A string that uniquely identifies this application resource.

begin
  #Get an Application
  result = api_instance.get_an_application(application_id)
  p result
rescue Freeclimb::ApiError => e
  puts "Exception when calling DefaultApi->get_an_application: #{e}"
end
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **application_id** | **String**| A string that uniquely identifies this application resource. | 

### Return type

[**ApplicationResult**](ApplicationResult.md)

### Authorization

[fc](../README.md#fc)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_an_incoming_number

> IncomingNumberResult get_an_incoming_number(phone_number_id)

Get an Incoming Number

### Example

```ruby
# load the gem
require 'freeclimb'
# setup authorization
Freeclimb.configure do |config|
  # Configure HTTP basic authorization: fc
  config.username = 'ACCOUNT ID'
  config.password = 'AUTH TOKEN'
end

api_instance = Freeclimb::DefaultApi.new
phone_number_id = 'phone_number_id_example' # String | String that uniquely identifies this phone number resource.

begin
  #Get an Incoming Number
  result = api_instance.get_an_incoming_number(phone_number_id)
  p result
rescue Freeclimb::ApiError => e
  puts "Exception when calling DefaultApi->get_an_incoming_number: #{e}"
end
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **phone_number_id** | **String**| String that uniquely identifies this phone number resource. | 

### Return type

[**IncomingNumberResult**](IncomingNumberResult.md)

### Authorization

[fc](../README.md#fc)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_an_sms_message

> MessageResult get_an_sms_message(message_id)

Get an SMS Message

### Example

```ruby
# load the gem
require 'freeclimb'
# setup authorization
Freeclimb.configure do |config|
  # Configure HTTP basic authorization: fc
  config.username = 'ACCOUNT ID'
  config.password = 'AUTH TOKEN'
end

api_instance = Freeclimb::DefaultApi.new
message_id = 'message_id_example' # String | String that uniquely identifies this Message resource.

begin
  #Get an SMS Message
  result = api_instance.get_an_sms_message(message_id)
  p result
rescue Freeclimb::ApiError => e
  puts "Exception when calling DefaultApi->get_an_sms_message: #{e}"
end
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **message_id** | **String**| String that uniquely identifies this Message resource. | 

### Return type

[**MessageResult**](MessageResult.md)

### Authorization

[fc](../README.md#fc)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_head_member

> QueueMember get_head_member(queue_id)

Get Head Member

### Example

```ruby
# load the gem
require 'freeclimb'
# setup authorization
Freeclimb.configure do |config|
  # Configure HTTP basic authorization: fc
  config.username = 'ACCOUNT ID'
  config.password = 'AUTH TOKEN'
end

api_instance = Freeclimb::DefaultApi.new
queue_id = 'queue_id_example' # String | String that uniquely identifies the Queue that the Member belongs to.

begin
  #Get Head Member
  result = api_instance.get_head_member(queue_id)
  p result
rescue Freeclimb::ApiError => e
  puts "Exception when calling DefaultApi->get_head_member: #{e}"
end
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **queue_id** | **String**| String that uniquely identifies the Queue that the Member belongs to. | 

### Return type

[**QueueMember**](QueueMember.md)

### Authorization

[fc](../README.md#fc)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_active_queues

> QueueList list_active_queues(opts)

List Active Queues

### Example

```ruby
# load the gem
require 'freeclimb'
# setup authorization
Freeclimb.configure do |config|
  # Configure HTTP basic authorization: fc
  config.username = 'ACCOUNT ID'
  config.password = 'AUTH TOKEN'
end

api_instance = Freeclimb::DefaultApi.new
opts = {
  _alias: '_alias_example' # String | Return only the Queue resources with aliases that exactly match this name.
}

begin
  #List Active Queues
  result = api_instance.list_active_queues(opts)
  p result
rescue Freeclimb::ApiError => e
  puts "Exception when calling DefaultApi->list_active_queues: #{e}"
end
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **_alias** | **String**| Return only the Queue resources with aliases that exactly match this name. | [optional] 

### Return type

[**QueueList**](QueueList.md)

### Authorization

[fc](../README.md#fc)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_all_account_logs

> LogList list_all_account_logs

List All Account Logs

### Example

```ruby
# load the gem
require 'freeclimb'
# setup authorization
Freeclimb.configure do |config|
  # Configure HTTP basic authorization: fc
  config.username = 'ACCOUNT ID'
  config.password = 'AUTH TOKEN'
end

api_instance = Freeclimb::DefaultApi.new

begin
  #List All Account Logs
  result = api_instance.list_all_account_logs
  p result
rescue Freeclimb::ApiError => e
  puts "Exception when calling DefaultApi->list_all_account_logs: #{e}"
end
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**LogList**](LogList.md)

### Authorization

[fc](../README.md#fc)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_an_application

> ApplicationList list_an_application(opts)

List applications

### Example

```ruby
# load the gem
require 'freeclimb'
# setup authorization
Freeclimb.configure do |config|
  # Configure HTTP basic authorization: fc
  config.username = 'ACCOUNT ID'
  config.password = 'AUTH TOKEN'
end

api_instance = Freeclimb::DefaultApi.new
opts = {
  _alias: '_alias_example' # String | Return only applications with aliases that exactly match this value.
}

begin
  #List applications
  result = api_instance.list_an_application(opts)
  p result
rescue Freeclimb::ApiError => e
  puts "Exception when calling DefaultApi->list_an_application: #{e}"
end
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **_alias** | **String**| Return only applications with aliases that exactly match this value. | [optional] 

### Return type

[**ApplicationList**](ApplicationList.md)

### Authorization

[fc](../README.md#fc)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_available_numbers

> AvailableNumberList list_available_numbers(opts)

List available numbers

### Example

```ruby
# load the gem
require 'freeclimb'
# setup authorization
Freeclimb.configure do |config|
  # Configure HTTP basic authorization: fc
  config.username = 'ACCOUNT ID'
  config.password = 'AUTH TOKEN'
end

api_instance = Freeclimb::DefaultApi.new
opts = {
  _alias: '_alias_example', # String | Filter on numbers based on the formatted string of the phone number.
  phone_number: 'phone_number_example' # String | PCRE-compatible regular expression to filter against `phoneNumber` field, which is in E.164 format.
}

begin
  #List available numbers
  result = api_instance.list_available_numbers(opts)
  p result
rescue Freeclimb::ApiError => e
  puts "Exception when calling DefaultApi->list_available_numbers: #{e}"
end
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **_alias** | **String**| Filter on numbers based on the formatted string of the phone number. | [optional] 
 **phone_number** | **String**| PCRE-compatible regular expression to filter against &#x60;phoneNumber&#x60; field, which is in E.164 format. | [optional] 

### Return type

[**AvailableNumberList**](AvailableNumberList.md)

### Authorization

[fc](../README.md#fc)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_call_logs

> LogList list_call_logs(call_id)

List Call Logs

### Example

```ruby
# load the gem
require 'freeclimb'
# setup authorization
Freeclimb.configure do |config|
  # Configure HTTP basic authorization: fc
  config.username = 'ACCOUNT ID'
  config.password = 'AUTH TOKEN'
end

api_instance = Freeclimb::DefaultApi.new
call_id = 'call_id_example' # String | String that uniquely identifies this call resource.

begin
  #List Call Logs
  result = api_instance.list_call_logs(call_id)
  p result
rescue Freeclimb::ApiError => e
  puts "Exception when calling DefaultApi->list_call_logs: #{e}"
end
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **call_id** | **String**| String that uniquely identifies this call resource. | 

### Return type

[**LogList**](LogList.md)

### Authorization

[fc](../README.md#fc)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_call_recordings

> RecordingList list_call_recordings(call_id, opts)

List Call Recordings

### Example

```ruby
# load the gem
require 'freeclimb'
# setup authorization
Freeclimb.configure do |config|
  # Configure HTTP basic authorization: fc
  config.username = 'ACCOUNT ID'
  config.password = 'AUTH TOKEN'
end

api_instance = Freeclimb::DefaultApi.new
call_id = 'call_id_example' # String | String that uniquely identifies this call resource.
opts = {
  date_created: 'date_created_example' # String | Only show recordings created on the specified date, in the form *YYYY-MM-DD*.
}

begin
  #List Call Recordings
  result = api_instance.list_call_recordings(call_id, opts)
  p result
rescue Freeclimb::ApiError => e
  puts "Exception when calling DefaultApi->list_call_recordings: #{e}"
end
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **call_id** | **String**| String that uniquely identifies this call resource. | 
 **date_created** | **String**| Only show recordings created on the specified date, in the form *YYYY-MM-DD*. | [optional] 

### Return type

[**RecordingList**](RecordingList.md)

### Authorization

[fc](../README.md#fc)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_calls

> CallList list_calls(opts)

List Calls

### Example

```ruby
# load the gem
require 'freeclimb'
# setup authorization
Freeclimb.configure do |config|
  # Configure HTTP basic authorization: fc
  config.username = 'ACCOUNT ID'
  config.password = 'AUTH TOKEN'
end

api_instance = Freeclimb::DefaultApi.new
opts = {
  to: 'to_example', # String | Only show Calls to this phone number.
  from: 'from_example', # String | Only show Calls from this phone number.
  status: 'status_example', # String | Only show Calls currently in this status. May be `queued`, `ringing`, `inProgress`, `canceled`, `completed`, `failed`, `busy`, or `noAnswer`.
  start_time: 'start_time_example', # String | Only show Calls that started at or after this time, given as YYYY-MM-DD hh:mm:ss.
  end_time: 'end_time_example', # String | Only show Calls that ended at or before this time, given as YYYY-MM- DD hh:mm:ss.
  parent_call_id: 'parent_call_id_example' # String | Only show Calls spawned by the call with this ID.
}

begin
  #List Calls
  result = api_instance.list_calls(opts)
  p result
rescue Freeclimb::ApiError => e
  puts "Exception when calling DefaultApi->list_calls: #{e}"
end
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **to** | **String**| Only show Calls to this phone number. | [optional] 
 **from** | **String**| Only show Calls from this phone number. | [optional] 
 **status** | **String**| Only show Calls currently in this status. May be &#x60;queued&#x60;, &#x60;ringing&#x60;, &#x60;inProgress&#x60;, &#x60;canceled&#x60;, &#x60;completed&#x60;, &#x60;failed&#x60;, &#x60;busy&#x60;, or &#x60;noAnswer&#x60;. | [optional] 
 **start_time** | **String**| Only show Calls that started at or after this time, given as YYYY-MM-DD hh:mm:ss. | [optional] 
 **end_time** | **String**| Only show Calls that ended at or before this time, given as YYYY-MM- DD hh:mm:ss. | [optional] 
 **parent_call_id** | **String**| Only show Calls spawned by the call with this ID. | [optional] 

### Return type

[**CallList**](CallList.md)

### Authorization

[fc](../README.md#fc)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_conferences

> ConferenceList list_conferences(opts)

List Conferences

### Example

```ruby
# load the gem
require 'freeclimb'
# setup authorization
Freeclimb.configure do |config|
  # Configure HTTP basic authorization: fc
  config.username = 'ACCOUNT ID'
  config.password = 'AUTH TOKEN'
end

api_instance = Freeclimb::DefaultApi.new
opts = {
  status: 'status_example', # String | Only show conferences that currently have the specified status. Valid values: `empty`, `populated`, `inProgress`, or `terminated`.
  _alias: '_alias_example', # String | List Conferences whose alias exactly matches this string.
  date_created: 'date_created_example', # String | Only show Conferences that were created on the specified date, in the form *YYYY-MM-DD*.
  date_updated: 'date_updated_example' # String | Only show Conferences that were last updated on the specified date, in the form *YYYY-MM-DD*.
}

begin
  #List Conferences
  result = api_instance.list_conferences(opts)
  p result
rescue Freeclimb::ApiError => e
  puts "Exception when calling DefaultApi->list_conferences: #{e}"
end
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **status** | **String**| Only show conferences that currently have the specified status. Valid values: &#x60;empty&#x60;, &#x60;populated&#x60;, &#x60;inProgress&#x60;, or &#x60;terminated&#x60;. | [optional] 
 **_alias** | **String**| List Conferences whose alias exactly matches this string. | [optional] 
 **date_created** | **String**| Only show Conferences that were created on the specified date, in the form *YYYY-MM-DD*. | [optional] 
 **date_updated** | **String**| Only show Conferences that were last updated on the specified date, in the form *YYYY-MM-DD*. | [optional] 

### Return type

[**ConferenceList**](ConferenceList.md)

### Authorization

[fc](../README.md#fc)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_incoming_numbers

> IncomingNumberList list_incoming_numbers(opts)

List Incoming Numbers

### Example

```ruby
# load the gem
require 'freeclimb'
# setup authorization
Freeclimb.configure do |config|
  # Configure HTTP basic authorization: fc
  config.username = 'ACCOUNT ID'
  config.password = 'AUTH TOKEN'
end

api_instance = Freeclimb::DefaultApi.new
opts = {
  phone_number: 'phone_number_example', # String | Only show incoming phone number resources that match this PCRE-compatible regular expression.
  _alias: '_alias_example' # String | Only show incoming phone numbers with aliases that exactly match this value.
}

begin
  #List Incoming Numbers
  result = api_instance.list_incoming_numbers(opts)
  p result
rescue Freeclimb::ApiError => e
  puts "Exception when calling DefaultApi->list_incoming_numbers: #{e}"
end
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **phone_number** | **String**| Only show incoming phone number resources that match this PCRE-compatible regular expression. | [optional] 
 **_alias** | **String**| Only show incoming phone numbers with aliases that exactly match this value. | [optional] 

### Return type

[**IncomingNumberList**](IncomingNumberList.md)

### Authorization

[fc](../README.md#fc)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_members

> QueueMemberList list_members(queue_id)

List Members

### Example

```ruby
# load the gem
require 'freeclimb'
# setup authorization
Freeclimb.configure do |config|
  # Configure HTTP basic authorization: fc
  config.username = 'ACCOUNT ID'
  config.password = 'AUTH TOKEN'
end

api_instance = Freeclimb::DefaultApi.new
queue_id = 'queue_id_example' # String | String that uniquely identifies the Queue that the Member belongs to.

begin
  #List Members
  result = api_instance.list_members(queue_id)
  p result
rescue Freeclimb::ApiError => e
  puts "Exception when calling DefaultApi->list_members: #{e}"
end
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **queue_id** | **String**| String that uniquely identifies the Queue that the Member belongs to. | 

### Return type

[**QueueMemberList**](QueueMemberList.md)

### Authorization

[fc](../README.md#fc)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_participants

> ConferenceParticipantList list_participants(conference_id, opts)

List Participants

### Example

```ruby
# load the gem
require 'freeclimb'
# setup authorization
Freeclimb.configure do |config|
  # Configure HTTP basic authorization: fc
  config.username = 'ACCOUNT ID'
  config.password = 'AUTH TOKEN'
end

api_instance = Freeclimb::DefaultApi.new
conference_id = 'conference_id_example' # String | ID of the conference this participant is in.
opts = {
  talk: true, # Boolean | Only show Participants with the talk privilege.
  listen: true # Boolean | Only show Participants with the listen privilege.
}

begin
  #List Participants
  result = api_instance.list_participants(conference_id, opts)
  p result
rescue Freeclimb::ApiError => e
  puts "Exception when calling DefaultApi->list_participants: #{e}"
end
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **conference_id** | **String**| ID of the conference this participant is in. | 
 **talk** | **Boolean**| Only show Participants with the talk privilege. | [optional] 
 **listen** | **Boolean**| Only show Participants with the listen privilege. | [optional] 

### Return type

[**ConferenceParticipantList**](ConferenceParticipantList.md)

### Authorization

[fc](../README.md#fc)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_recordings

> RecordingList list_recordings(opts)

List Recordings

### Example

```ruby
# load the gem
require 'freeclimb'
# setup authorization
Freeclimb.configure do |config|
  # Configure HTTP basic authorization: fc
  config.username = 'ACCOUNT ID'
  config.password = 'AUTH TOKEN'
end

api_instance = Freeclimb::DefaultApi.new
opts = {
  call_id: 'call_id_example', # String | Show only Recordings made during the Call with this ID.
  conference_id: 'conference_id_example', # String | Show only Recordings made during the conference with this ID.
  date_created: 'date_created_example' # String | Only show Recordings created on this date, formatted as *YYYY-MM-DD*.
}

begin
  #List Recordings
  result = api_instance.list_recordings(opts)
  p result
rescue Freeclimb::ApiError => e
  puts "Exception when calling DefaultApi->list_recordings: #{e}"
end
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **call_id** | **String**| Show only Recordings made during the Call with this ID. | [optional] 
 **conference_id** | **String**| Show only Recordings made during the conference with this ID. | [optional] 
 **date_created** | **String**| Only show Recordings created on this date, formatted as *YYYY-MM-DD*. | [optional] 

### Return type

[**RecordingList**](RecordingList.md)

### Authorization

[fc](../README.md#fc)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_sms_messages

> MessagesList list_sms_messages(opts)

List SMS Messages

### Example

```ruby
# load the gem
require 'freeclimb'
# setup authorization
Freeclimb.configure do |config|
  # Configure HTTP basic authorization: fc
  config.username = 'ACCOUNT ID'
  config.password = 'AUTH TOKEN'
end

api_instance = Freeclimb::DefaultApi.new
opts = {
  to: 'to_example', # String | Only show Messages to this phone number.
  from: 'from_example', # String | Only show Messages from this phone number.
  begin_time: 'begin_time_example', # String | Only show Messages sent at or after this time (GMT), given as *YYYY-MM-DD hh:mm:ss*.
  end_time: 'end_time_example', # String | Only show messages sent at or before this time (GMT), given as *YYYY-MM-DD hh:mm*..
  direction: 'direction_example', # String | Either `inbound` or `outbound`. Only show Messages that were either *sent from* or *received by* FreeClimb.
  account_id: 'account_id_example' # String | String that uniquely identifies this account resource.
}

begin
  #List SMS Messages
  result = api_instance.list_sms_messages(opts)
  p result
rescue Freeclimb::ApiError => e
  puts "Exception when calling DefaultApi->list_sms_messages: #{e}"
end
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **to** | **String**| Only show Messages to this phone number. | [optional] 
 **from** | **String**| Only show Messages from this phone number. | [optional] 
 **begin_time** | **String**| Only show Messages sent at or after this time (GMT), given as *YYYY-MM-DD hh:mm:ss*. | [optional] 
 **end_time** | **String**| Only show messages sent at or before this time (GMT), given as *YYYY-MM-DD hh:mm*.. | [optional] 
 **direction** | **String**| Either &#x60;inbound&#x60; or &#x60;outbound&#x60;. Only show Messages that were either *sent from* or *received by* FreeClimb. | [optional] 
 **account_id** | **String**| String that uniquely identifies this account resource. | [optional] 

### Return type

[**MessagesList**](MessagesList.md)

### Authorization

[fc](../README.md#fc)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## make_a_call

> CallResult make_a_call(opts)

Make a Call

### Example

```ruby
# load the gem
require 'freeclimb'
# setup authorization
Freeclimb.configure do |config|
  # Configure HTTP basic authorization: fc
  config.username = 'ACCOUNT ID'
  config.password = 'AUTH TOKEN'
end

api_instance = Freeclimb::DefaultApi.new
opts = {
  make_call_request: Freeclimb::MakeCallRequest.new # MakeCallRequest | Call details for making a call
}

begin
  #Make a Call
  result = api_instance.make_a_call(opts)
  p result
rescue Freeclimb::ApiError => e
  puts "Exception when calling DefaultApi->make_a_call: #{e}"
end
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **make_call_request** | [**MakeCallRequest**](MakeCallRequest.md)| Call details for making a call | [optional] 

### Return type

[**CallResult**](CallResult.md)

### Authorization

[fc](../README.md#fc)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## remove_a_participant

> remove_a_participant(conference_id, call_id)

Remove a Participant

### Example

```ruby
# load the gem
require 'freeclimb'
# setup authorization
Freeclimb.configure do |config|
  # Configure HTTP basic authorization: fc
  config.username = 'ACCOUNT ID'
  config.password = 'AUTH TOKEN'
end

api_instance = Freeclimb::DefaultApi.new
conference_id = 'conference_id_example' # String | ID of the conference this participant is in.
call_id = 'call_id_example' # String | ID of the Call associated with this participant.

begin
  #Remove a Participant
  api_instance.remove_a_participant(conference_id, call_id)
rescue Freeclimb::ApiError => e
  puts "Exception when calling DefaultApi->remove_a_participant: #{e}"
end
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **conference_id** | **String**| ID of the conference this participant is in. | 
 **call_id** | **String**| ID of the Call associated with this participant. | 

### Return type

nil (empty response body)

### Authorization

[fc](../README.md#fc)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: Not defined


## send_an_sms_message

> MessageResult send_an_sms_message(opts)

Send an SMS Message

### Example

```ruby
# load the gem
require 'freeclimb'
# setup authorization
Freeclimb.configure do |config|
  # Configure HTTP basic authorization: fc
  config.username = 'ACCOUNT ID'
  config.password = 'AUTH TOKEN'
end

api_instance = Freeclimb::DefaultApi.new
opts = {
  message_request: Freeclimb::MessageRequest.new # MessageRequest | Details to create a message
}

begin
  #Send an SMS Message
  result = api_instance.send_an_sms_message(opts)
  p result
rescue Freeclimb::ApiError => e
  puts "Exception when calling DefaultApi->send_an_sms_message: #{e}"
end
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **message_request** | [**MessageRequest**](MessageRequest.md)| Details to create a message | [optional] 

### Return type

[**MessageResult**](MessageResult.md)

### Authorization

[fc](../README.md#fc)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## stream_a_recording_file

> File stream_a_recording_file(recording_id)

Stream a Recording File

### Example

```ruby
# load the gem
require 'freeclimb'
# setup authorization
Freeclimb.configure do |config|
  # Configure HTTP basic authorization: fc
  config.username = 'ACCOUNT ID'
  config.password = 'AUTH TOKEN'
end

api_instance = Freeclimb::DefaultApi.new
recording_id = 'recording_id_example' # String | String that uniquely identifies this recording resource.

begin
  #Stream a Recording File
  result = api_instance.stream_a_recording_file(recording_id)
  p result
rescue Freeclimb::ApiError => e
  puts "Exception when calling DefaultApi->stream_a_recording_file: #{e}"
end
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **recording_id** | **String**| String that uniquely identifies this recording resource. | 

### Return type

**File**

### Authorization

[fc](../README.md#fc)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: audio/x-wav


## update_a_conference

> ConferenceResult update_a_conference(conference_id, opts)

Update a Conference

### Example

```ruby
# load the gem
require 'freeclimb'
# setup authorization
Freeclimb.configure do |config|
  # Configure HTTP basic authorization: fc
  config.username = 'ACCOUNT ID'
  config.password = 'AUTH TOKEN'
end

api_instance = Freeclimb::DefaultApi.new
conference_id = 'conference_id_example' # String | String that uniquely identifies this conference resource.
opts = {
  update_conference_request: Freeclimb::UpdateConferenceRequest.new # UpdateConferenceRequest | Conference Details to update
}

begin
  #Update a Conference
  result = api_instance.update_a_conference(conference_id, opts)
  p result
rescue Freeclimb::ApiError => e
  puts "Exception when calling DefaultApi->update_a_conference: #{e}"
end
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **conference_id** | **String**| String that uniquely identifies this conference resource. | 
 **update_conference_request** | [**UpdateConferenceRequest**](UpdateConferenceRequest.md)| Conference Details to update | [optional] 

### Return type

[**ConferenceResult**](ConferenceResult.md)

### Authorization

[fc](../README.md#fc)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## update_a_live_call

> update_a_live_call(call_id, opts)

Update a Live Call

### Example

```ruby
# load the gem
require 'freeclimb'
# setup authorization
Freeclimb.configure do |config|
  # Configure HTTP basic authorization: fc
  config.username = 'ACCOUNT ID'
  config.password = 'AUTH TOKEN'
end

api_instance = Freeclimb::DefaultApi.new
call_id = 'call_id_example' # String | String that uniquely identifies this call resource.
opts = {
  update_call_request: Freeclimb::UpdateCallRequest.new # UpdateCallRequest | Call details to update
}

begin
  #Update a Live Call
  api_instance.update_a_live_call(call_id, opts)
rescue Freeclimb::ApiError => e
  puts "Exception when calling DefaultApi->update_a_live_call: #{e}"
end
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **call_id** | **String**| String that uniquely identifies this call resource. | 
 **update_call_request** | [**UpdateCallRequest**](UpdateCallRequest.md)| Call details to update | [optional] 

### Return type

nil (empty response body)

### Authorization

[fc](../README.md#fc)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined


## update_a_participant

> ConferenceParticipantResult update_a_participant(conference_id, call_id, opts)

Update a Participant

### Example

```ruby
# load the gem
require 'freeclimb'
# setup authorization
Freeclimb.configure do |config|
  # Configure HTTP basic authorization: fc
  config.username = 'ACCOUNT ID'
  config.password = 'AUTH TOKEN'
end

api_instance = Freeclimb::DefaultApi.new
conference_id = 'conference_id_example' # String | ID of the conference this participant is in.
call_id = 'call_id_example' # String | ID of the Call associated with this participant.
opts = {
  update_conference_participant_request: Freeclimb::UpdateConferenceParticipantRequest.new # UpdateConferenceParticipantRequest | Conference participant details to update
}

begin
  #Update a Participant
  result = api_instance.update_a_participant(conference_id, call_id, opts)
  p result
rescue Freeclimb::ApiError => e
  puts "Exception when calling DefaultApi->update_a_participant: #{e}"
end
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **conference_id** | **String**| ID of the conference this participant is in. | 
 **call_id** | **String**| ID of the Call associated with this participant. | 
 **update_conference_participant_request** | [**UpdateConferenceParticipantRequest**](UpdateConferenceParticipantRequest.md)| Conference participant details to update | [optional] 

### Return type

[**ConferenceParticipantResult**](ConferenceParticipantResult.md)

### Authorization

[fc](../README.md#fc)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## update_a_queue

> QueueResult update_a_queue(queue_id, opts)

Update a Queue

### Example

```ruby
# load the gem
require 'freeclimb'
# setup authorization
Freeclimb.configure do |config|
  # Configure HTTP basic authorization: fc
  config.username = 'ACCOUNT ID'
  config.password = 'AUTH TOKEN'
end

api_instance = Freeclimb::DefaultApi.new
queue_id = 'queue_id_example' # String | A string that uniquely identifies this Queue resource.
opts = {
  queue_request: Freeclimb::QueueRequest.new # QueueRequest | Queue Details to update
}

begin
  #Update a Queue
  result = api_instance.update_a_queue(queue_id, opts)
  p result
rescue Freeclimb::ApiError => e
  puts "Exception when calling DefaultApi->update_a_queue: #{e}"
end
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **queue_id** | **String**| A string that uniquely identifies this Queue resource. | 
 **queue_request** | [**QueueRequest**](QueueRequest.md)| Queue Details to update | [optional] 

### Return type

[**QueueResult**](QueueResult.md)

### Authorization

[fc](../README.md#fc)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## update_an_account

> update_an_account(opts)

Manage an account

### Example

```ruby
# load the gem
require 'freeclimb'
# setup authorization
Freeclimb.configure do |config|
  # Configure HTTP basic authorization: fc
  config.username = 'ACCOUNT ID'
  config.password = 'AUTH TOKEN'
end

api_instance = Freeclimb::DefaultApi.new
opts = {
  account_request: Freeclimb::AccountRequest.new # AccountRequest | Account details to update
}

begin
  #Manage an account
  api_instance.update_an_account(opts)
rescue Freeclimb::ApiError => e
  puts "Exception when calling DefaultApi->update_an_account: #{e}"
end
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **account_request** | [**AccountRequest**](AccountRequest.md)| Account details to update | [optional] 

### Return type

nil (empty response body)

### Authorization

[fc](../README.md#fc)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined


## update_an_application

> ApplicationResult update_an_application(application_id, opts)

Update an application

### Example

```ruby
# load the gem
require 'freeclimb'
# setup authorization
Freeclimb.configure do |config|
  # Configure HTTP basic authorization: fc
  config.username = 'ACCOUNT ID'
  config.password = 'AUTH TOKEN'
end

api_instance = Freeclimb::DefaultApi.new
application_id = 'application_id_example' # String | A string that uniquely identifies this application resource.
opts = {
  application_request: Freeclimb::ApplicationRequest.new # ApplicationRequest | Application details to update.
}

begin
  #Update an application
  result = api_instance.update_an_application(application_id, opts)
  p result
rescue Freeclimb::ApiError => e
  puts "Exception when calling DefaultApi->update_an_application: #{e}"
end
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **application_id** | **String**| A string that uniquely identifies this application resource. | 
 **application_request** | [**ApplicationRequest**](ApplicationRequest.md)| Application details to update. | [optional] 

### Return type

[**ApplicationResult**](ApplicationResult.md)

### Authorization

[fc](../README.md#fc)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## update_an_incoming_number

> IncomingNumberResult update_an_incoming_number(phone_number_id, opts)

Update an Incoming Number

### Example

```ruby
# load the gem
require 'freeclimb'
# setup authorization
Freeclimb.configure do |config|
  # Configure HTTP basic authorization: fc
  config.username = 'ACCOUNT ID'
  config.password = 'AUTH TOKEN'
end

api_instance = Freeclimb::DefaultApi.new
phone_number_id = 'phone_number_id_example' # String | String that uniquely identifies this phone number resource.
opts = {
  incoming_number_request: Freeclimb::IncomingNumberRequest.new # IncomingNumberRequest | Incoming Number details to update
}

begin
  #Update an Incoming Number
  result = api_instance.update_an_incoming_number(phone_number_id, opts)
  p result
rescue Freeclimb::ApiError => e
  puts "Exception when calling DefaultApi->update_an_incoming_number: #{e}"
end
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **phone_number_id** | **String**| String that uniquely identifies this phone number resource. | 
 **incoming_number_request** | [**IncomingNumberRequest**](IncomingNumberRequest.md)| Incoming Number details to update | [optional] 

### Return type

[**IncomingNumberResult**](IncomingNumberResult.md)

### Authorization

[fc](../README.md#fc)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

