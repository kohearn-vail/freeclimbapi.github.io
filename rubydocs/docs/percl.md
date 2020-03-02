# Percl

The Performance Command Language (PerCL) defines a set of instructions, written in JSON format, that express telephony actions to be performed in response to an event on the FreeClimb platform. FreeClimb communicates with the application server when events associated with the application occur, so the webserver can instruct FreeClimb how to handle such events using PerCL scripts.

When creating a Percl object, required parameters must be used in the constructer while optional parameters must be set direclty on the given Percl object. Example:
```ruby
digits = '630'
send_digits = Percl::SendDigits.new(digits)
send_digits.pauseMs = '500'
```

## Documentation for PerCL Responses
Class | Description
------------ | -------------
[*Percl::OutDial*](percl.md#percl::outdial) | The `OutDial` command is used to call a phone number 
[*Percl::Hangup*](percl.md#percl::hangup) | The `Hangup` command terminates a Call
[*Percl::Pause*](percl.md#percl::pause) | The `Pause` command halts execution of the current PerCL script for a specified number of millisecond
[*Percl::Redirect*](percl.md#percl::redirect) | The `Redirect` command transfers control of a Call to the PerCL at a different URL
[*Percl::SendDigits*](percl.md#percl::senddigits) | The `SendDigits` command plays DTMF tones on a live Call. This is useful for navigating through IVR menus or dialing extensions
[*Percl::Reject*](percl.md#percl::reject) | The `Reject` command blocks an incoming Call.
[*Percl::CreateConference*](percl.md#percl::createConference) | The `CreateConference` command does exactly what its name implies — it creates an unpopulated Conference (one without any Participants).
[*Percl::TerminateConference*](percl.md#percl::terminateConference) | The `TerminateConference` command terminates an existing Conference.
[*Percl::AddToConference*](percl.md#percl::addToConference) | The `AddToConference` command adds a Participant to a Conference.
[*Percl::RemoveFromConference*](percl.md#percl::removeFromConference) | The `RemoveFromConference` command removes a Participant from a Conference but does not hang up.
[*Percl::SetListen*](percl.md#percl::setListen) | The `SetListen` command enables or disables the listen privilege for a Conference Participant provided both calls are in the same conference. 
[*Percl::SetTalk*](percl.md#percl::setTalk) | The `SetTalk` command enables or disables the talk privilege for a Participant in a Conference provided both calls are in the same conference.
[*Percl::Enqueue*](percl.md#percl::enqueue) | The `Enqueue` command adds the current Call to a call Queue.
[*Percl::Dequeue*](percl.md#percl::dequeue) | The `Dequeue` command transfers control of a Call that is in a Queue so that the waiting caller exits the Queue.
[*Percl::RecordUtterance*](percl.md#percl::recordUtterance) | The `RecordUtterance` command records the caller's voice and returns the URL of a file containing the audio recording.
[*Percl::StartRecordCall*](percl.md#percl::startRecordCall) | The `StartRecordCall` command records the current call and returns the URL of a file containing the audio recording when recording completes.
[*Percl::PlayEarlyMedia*](percl.md#percl::playEarlyMedia) | The `PlayEarlyMedia` command plays A media file before attempting to connect a call
[*Percl::Play*](percl.md#percl::play) | the `Play` command plays an audio file back to the caller.
[*Percl::Say*](percl.md#percl::say) | The `Say` command provides Text-To-Speech (TTS) support. It converts text to speech and then renders it in a female voice back to the caller.
[*Percl::GetDigits*](percl.md#percl::getDigits) | The `GetDigits` command collects DTMF inputs from the caller.
[*Percl::GetSpeech*](percl.md#percl::getSpeech) | The `GetSpeech` command enables the Caller to respond to the application using a supported language.
[*Percl::Sms*](percl.md#percl::Sms) | The `Sms` command can be used to send an SMS message to a phone number during a phone call.



## Percl::OutDial

The OutDial command is used to call a phone number

### Example

```ruby
# load the gems
require 'sinatra'
require 'freeclimb'
require 'json'

post '/voice' do 
  out_dial = Percl::OutDial.new('MOCK_ACTION_URL', 'MOCK_CALL_CONNECT_URL', 'MOCK_CALLING_NUMBER', 'MOCK_DESTINATION')
  script = Percl::Script.new
  script.add(out_dial)
  script.to_json
end
```

### Parameters
Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **actionUrl** | **String**| URL to which FreeClimb sends an HTTP POST request. 
 **callConnectUrl** | **String**| URL to which FreeClimb makes an HTTP POST request informing the result of the OutDial.
 **callingNumber** | **String** | The caller ID to show to the called party when FreeClimb calls. This can be one of the following: The To or From number provided in the first Webhook to your webserver. Any phone number you have purchased from FreeClimb.
 **destination** | **String** | E.164 representation of the phone number to Call. 
 **ifMachine** | **String** | Specifies how FreeClimb should handle this OutDial if an answering machine answers the Call. Valid values: `redirect` invokes the ifMachineUrl for instructions. `hangup` hangs up the Call. The ifMachineUrl will not be invoked. | [optional]
 **ifMachineUrl** | **String** | When the `ifMachine` flag is set to `redirect`, this attribute specifies a URL to which FreeClimb makes a POST request when an answering machine or a fax machine is detected. This URL is required if the `ifMachine` flag is set to `redirect`. Otherwise, it should not be included. | [required if `ifMachine` is set to `redirect`]
 **sendDigits** | **String** | DTMF tones to play to the outdialed Call. This is typically used to dial a number and then dial an extension. | [optional]
 **statusCallBackUrl** | **String** | When the outdialed Call leg terminates, FreeClimb sends a `callStatus` Webhook to the `statusCallbackUrl`. This is a notification only; any PerCL command returned is ignored. | [optional]
 **timeout** | **String** | Maximum time in seconds the `OutDial` command waits for the called party to answer the Call. When a timeout occurs, FreeClimb invokes the `callConnectUrl` Webhook to report that the out-dialed Call has ended with a status of `noAnswer`. | [optional]


## Percl::Hangup

The Hangup command terminates a Call

### Example

```ruby
# load the gems
require 'sinatra'
require 'freeclimb'
require 'json'

post '/voice' do 
  hangup = Percl::Hangup.new
  script = Percl::Script.new
  script.add(out_dial)
  script.to_json
end
```

### Parameters
Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**callId** | **String** | The ID of the Call leg to hang up. If not specified, the Call leg corresponding to the current PerCL execution context hangs up. | [optional]
**reason** | **String** | The user defined reason for the hangup. In general, applications should use a set of enumerated values that are predefined to cover all exit points of the Call flows for the given application. | [optional]

## Percl::Pause

The `Pause` command halts execution of the current PerCL script for a specified number of milliseconds. If `Pause` is the first command in a PerCL document, FreeClimb will wait for the specified time to elapse before picking up the call.

### Example

```ruby
# load the gems
require 'sinatra'
require 'freeclimb'
require 'json'

post '/voice' do 
  pause = Percl::Pause.new(2000)
  script = Percl::Script.new
  script.add(out_dial)
  script.to_json
end
```

### Parameters
Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**length** | **Integer** | Length in milliseconds. FreeClimb will wait silently before continuing on. 


## Percl::Redirect

The `Redirect` command transfers control of a Call to the PerCL at a different URL. `Redirect` is a terminal command, so any actions following it are never executed.

### Example

```ruby
# load the gems
require 'sinatra'
require 'freeclimb'
require 'json'

post '/voice' do 
  redirect = Percl::Redirect.new('MOCK_REDIRECT_URL')
  script = Percl::Script.new
  script.add(redirect)
  script.to_json
end
```

### Parameters
Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**actionUrl** | **String** | URL to request a new PerCL script to continue with the current Call's processing. When `Redirect` invokes the `actionUrl`, an `inbound` Webhook is sent.


## Percl::SendDigits

The `SendDigits` command plays DTMF tones on a live Call. This is useful for navigating through IVR menus or dialing extensions.

### Example

```ruby
# load the gems
require 'sinatra'
require 'freeclimb'
require 'json'

post '/voice' do 
  send = Percl::SendDigits.new('12367#')
  script = Percl::Script.new
  script.add(send)
  script.to_json
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**digits** | **String** | String containing the digits to be played. The string cannot be empty and can include any digit, plus `#`, or `*`, and allows embedding specification for delay or pause between the output of individual digits.
**pauseMs** | **Integer** | Pause between digits in milliseconds. Valid values are 100-1000 milliseconds and will be adjusted by FreeClimb to satisfy the constraint. | [optional]


## Percl::Reject

The `Reject` command blocks an incoming Call. Using `Reject` is the only way to prevent FreeClimb from answering a Call. Any other response will result in an answered Call and your account will be billed.

### Example

```ruby
# load the gems
require 'sinatra'
require 'freeclimb'
require 'json'

post '/voice' do 
  reject = Percl::Reject.new
  script = Percl::Script.new
  script.add(reject)
  script.to_json
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**reason** | **String** | Reason for the rejection. This can be any string value. In general, applications should use a set of enumerated values that are predefined to cover all exit points of the call flows for the given application. | [optional]


## Percl::CreateConference

The `CreateConference` command does exactly what its name implies — it creates an unpopulated Conference (one without any Participants). Once created, a Conference remains in FreeClimb until explicitly terminated by a customer. Once a Conference has been terminated, it can no longer be used.

### Example

```ruby
# load the gems
require 'sinatra'
require 'freeclimb'
require 'json'

post '/voice' do 
  create_conference = Percl::CreateConference.new('MOCK_ACTION_URL')
  script = Percl::Script.new
  script.add(create_conference)
  script.to_json
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**actionUrl** | **String** | This URL is invoked once the Conference is successfully created. Actions on the Conference, such as adding Participants, can be performed via the PerCL script returned in the response. 
**alias** | **String** | Descriptive name for the Conference. | [optional]
**playBeep** | **String** | Indicates whether to play a beep when a Participant enters or leaves the Conference. either `always`, `never`, `entryOnly`, or `exitOnly`. Leaving this unset will make conference default to `always` | [optional]
**record** | **String** | When set to `true`, the entire Conference is recorded. The `statusCallbackUrl` of the Conference will receive a `conferenceRecordingEnded` Webhook when the Conference transitions from the `inProgress` to empty state. | [optional]
**waitUrl** | **String** | If specified, this URL provides the custom hold music for the Conference when it is in the populated state. This attribute is always fetched using HTTP GET and is fetched just once – when the Conference is created. The URL must be an audio file that is reachable and readable by FreeClimb. | [optional]
**statusCallbackUrl** | **String** | This URL is invoked when the status of the Conference changes or when a recording of the Conference has become available. | [optional]


## Percl::TerminateConference

The `TerminateConference` command terminates an existing Conference. Any active participants are hung up on by FreeClimb. If this is not the desired behavior, use the `RemoveFromConference` command to unbridge Calls that should not be hung up.

Note: The Call requesting TerminateConference must be on the same Conference for this command to execute.

### Example

```ruby
# load the gems
require 'sinatra'
require 'freeclimb'
require 'json'

post '/voice' do 
  terminate = Percl::TerminateConference.new('MOCK_CONFERENCE_ID')
  script = Percl::Script.new
  script.add(terminate)
  script.to_json
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**conferenceId** | **String** | ID of the conference to terminate.


## Percl::AddToConference

The `AddToConference` command adds a Participant to a Conference. If this Participant currently is in another Conference, the Participant is first removed from that Conference. Two Call legs can be bridged together by creating a Conference and adding both Call legs to it via `AddToConference`.

### Example

```ruby
# load the gems
require 'sinatra'
require 'freeclimb'
require 'json'

post '/voice' do 
  # Assuming Conference is already created
  add = Percl::AddToConference.new('MOCK_CONF_ID', 'MOCK_CALL_ID')
  script = Percl::Script.new
  script.add(add)
  script.to_json
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**conferenceId** | **String** | ID of the Conference to which to add the Participant (Call leg). Conference must exist or an error will result.
**callId** | **String** | ID of the Call that will be added to the specified Conference. The Call must be in progress or an error will result. If the Call is part of an existing Conference, it is first removed from that Conference and is then moved to the new one.
**startConfOnEnter** | **Boolean** | Flag that indicates whether a Conference starts upon entry of this particular Participant. This is usually set to `true` for moderators and `false` for all other Participants. | [optional]
**talk** | **Boolean** | If `true`, the Participant joins the Conference with talk privileges. This may be modified later via the REST API or `SetTalk` PerCL command. | [optional]
**listen** | **Boolean** | If `true`, the Participant joins the Conference with listen privileges. This may be modified later via the REST API or `SetListen` PerCL command. | [optional]
**allowCallControl** | **Boolean** | If `true`, Call control will be enabled for this Participant's Call leg. | [optional]
**callControlSequence** | **String** | Defines a sequence of digits that, when entered by this caller, invokes the `callControlUrl`. Only digits plus '*', and '#' may be used. | [`required` if allowCallControl is `true`]
**callControlUrl** | **String** | URL to be invoked when this Participant enters the digit sequence defined in the `callControlSequence` attribute. |  [`required` if allowCallControl is `true`]
**leaveConferenceUrl** | **String** | URL to be invoked when the Participant leaves the Conference. | [optional]
**notificationUrl** | **String** | When the Participant enters the Conference, this URL will be invoked using an HTTP POST request with the standard request parameters. | [optional]


## Percl::RemoveFromConference

The `RemoveFromConference` command removes a Participant from a Conference but does not hang up. Instead, the Call is simply unbridged and what happens next with the Call is determined by the PerCL returned in response to the `leaveConferenceUrl` attribute.

### Example

```ruby
# load the gems
require 'sinatra'
require 'freeclimb'
require 'json'

post '/voice' do 
  # Assuming Conference is already created and participant is in conference
  remove = Percl::RemoveFromConference.new('MOCK_CALL_ID')
  script = Percl::Script.new
  script.add(remove)
  script.to_json
end
```

### Parameters
Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**callId** | **String** | ID of the Call leg to be removed from the Conference. The Call must be in a Conference or an error will be triggered.



## Percl::SetListen

The `SetListen` command enables or disables the listen privilege for a Conference Participant provided both calls are in the same conference. The Participant can hear what the other participants are saying only if this privilege is enabled.

### Example


```ruby
# load the gems
require 'sinatra'
require 'freeclimb'
require 'json'

post '/voice' do 
  # Assuming Conference is already created and participant is in conference
  listen = Percl::SetListen.new('MOCK_CALL_ID')
  script = Percl::Script.new
  script.add(listen)
  script.to_json
end
```

### Parameters
Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**callId** | **String** | ID of the call leg that is to be assigned the listen privilege. The Call must be in a Conference or an error will be triggered.
**listen** | **Boolean** | Specifying `false` will silence the Conference for this Participant. | [optional]


## Percl::SetTalk

The `SetTalk` command enables or disables the talk privilege for a Participant in a Conference provided both calls are in the same conference. If 'true', no audio from that Participant is shared with the other Participants of the Conference.

### Example

```ruby
# load the gems
require 'sinatra'
require 'freeclimb'
require 'json'

post '/voice' do 
  # Assuming Conference is already created and participant is in conference
  talk = Percl::SetTalk.new('MOCK_CALL_ID')
  script = Percl::Script.new
  script.add(talk)
  script.to_json
end
```

### Parameters
Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**callId** | **String** | ID of the call leg that is to be muted or unmuted. The Call must be in a Conference or an error will be triggered.
**talk** | **Boolean** | Specifying `false` mutes the Participant. | [optional]

## Percl::Enqueue

The `Enqueue` command adds the current Call to a call Queue. If the specified Queue does not exist, it is created and then the Call is added to it. The default maximum length of the queue is 100. This can be modified using the REST API.

### Example

```ruby
# load the gems
require 'sinatra'
require 'freeclimb'
require 'json'

post '/voice' do 
  # Assuming Queue is already created
  enqueue = Percl::Enqueue.new('MOCK_QUEUE_ID', 'MOCK_WAIT_URL', 'MOCK_ACTION_URL')
  script = Percl::Script.new
  script.add(enqueue)
  script.to_json
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**queueId** | **String** | ID of the Queue to which to add the Call. If the Queue does not exist, it will be created. The ID must start with QU followed by 40 hex characters.
**waitUrl** | **String** | Specifies a URL pointing to a PerCL script containing actions to be executed while the caller is waiting in the Queue. Once the script returned by the `waitUrl` runs out of commands to execute, FreeClimb will re-request the `waitUrl` and start over, essentially looping the script indefinitely.
**actionUrl** | **String** | A request is made to this URL when the Call leaves the Queue, which can occur if enqueue of the Call fails or when the call is dequeued via the `Dequeue` command, the REST API (POST to Queue Member resource), or the caller hangs up.
**notificationUrl** | **String** | URL to be invoked when the call enters the queue. The request to the URL contains the standard request parameters.This is a notification only; any PerCL returned will be ignored. | [optional]


## Percl::Dequeue

The `Dequeue` command transfers control of a Call that is in a Queue so that the waiting caller exits the Queue. Execution continues with the first command in the PerCL script returned by the `actionUrl` specified in the `Enqueue` command.


### Example

```ruby
# load the gems
require 'sinatra'
require 'freeclimb'
require 'json'

post '/voice' do 
  # Assuming call is in queue
  dequeue = Percl::Dequeue.new
  script = Percl::Script.new
  script.add(dequeue)
  script.to_json
end
```

### Parameters
none


## Percl::RecordUtterance

The `RecordUtterance` command records the caller's voice and returns the URL of a file containing the audio recording.

`RecordUtterance` is blocking and is a terminal command. As such, the `actionUrl` property is required, and control of the Call picks up using the PerCL returned in response to the `actionUrl`. Recording information is returned in the `actionUrl` request.

### Example

```ruby
# load the gems
require 'sinatra'
require 'freeclimb'
require 'json'

post '/voice' do 
  record = Percl::RecordUtterance.new('MOCK_ACTION_URL')
  script = Percl::Script.new
  script.add(record)
  script.to_json
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**actionUrl** | **String** | URL to which information on the completed recording is submitted. The PerCL received in response is then used to continue with Call processing.
**silenceTimeoutMs** | **Integer** | Interval of silence that should elapse before ending the recording. | [optional]
**finishOnKey** | **String** | Key that triggers the end of the recording. any digit, '#', or '*' | [optional]
**maxLengthSec** | **Integer** | Maximum length for the command execution in seconds. | [optional]
**playBeep** | **Boolean** | Indicates whether to play a beep sound before the start of the recording. If set to `false`, no beep is played. | [optional]
**autoStart** | **Boolean** | If `false`, recording begins immediately after the RecordUtterance command is processed. If `true`, recording begins when audio is present and if audio begins before the `maxLengthSec` timeout. If no audio begins before `maxLengthSec`, no recording is generated. | [optional]


## Percl::StartRecordCall

The `StartRecordCall` command records the current call and returns the URL of a file containing the audio recording when recording completes.

`StartRecordCall` is non-blocking. After recording of the current call begins, control of the call moves to the PerCL command that follows `StartRecordCall` in the current PerCL script.

### Example

```ruby
# load the gems
require 'sinatra'
require 'freeclimb'
require 'json'

post '/voice' do 
  record = Percl::StartRecordCall.new
  script = Percl::Script.new
  script.add(record)
  script.to_json
end
```

### Parameters
none


## Percl::PlayEarlyMedia

`PlayEarlyMedia` is relevant only when present as the very first command in the PerCL script returned for an incoming Call. In such cases, the command is executed before FreeClimb attempts to connect the call. The audio file it uses can be stored in any location that is accessible via URL.

### Example

```ruby
# load the gems
require 'sinatra'
require 'freeclimb'
require 'json'

post '/voice' do 
  media = Percl::PlayEarlyMedia.new('MOCK_FILE_URL')
  script = Percl::Script.new
  script.add(media)
  script.to_json
end
```

### Parameters
Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**file** | **String** | URL of the audio file to be played to the caller. The URL can be the `recordingUrl` generated from the `RecordUtterance` or `StartRecordCall` PerCL commands or any accessible URL. FreeClimb will respect Cache-Control headers for this file. Use these to limit repeated requests for unchanged audio. If no Cache-Control header is provided, the file will be cached for seven days by default.


## Percl::Play

The `Play` command plays an audio file back to the caller. The audio file may be located at any location accessible via a URL. `Play` can exist as a stand-alone command or as a nested command. It does not allow barge-in unless nested within a `GetSpeech` command. The file will always be played to completion unless nested.


### Example

```ruby
# load the gems
require 'sinatra'
require 'freeclimb'
require 'json'

post '/voice' do 
  play = Percl::Play.new('MOCK_FILE_URL')
  script = Percl::Script.new
  script.add(play)
  script.to_json
end
```

### Parameters
Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**file** | **String** | URL of the audio file to be played to the caller. The URL can be the `recordingUrl` generated from the `RecordUtterance` or `StartRecordCall` PerCL commands. 
**loop** | **Integer** | Number of times the audio file is played. Specifying '0' causes the Play action to loop until the Call is hung up. | [optional]
**conferenceId** | **String** | ID of the Conference the audio should be rendered to. If this is not specified, the audio is by default rendered to the caller associated with the call leg that corresponds to the current PerCL execution context. The call leg associated with this command must be in the specified Conference or the command will return an error. | [optional]


## Percl::Say

The `Say` command provides Text-To-Speech (TTS) support. It converts text to speech and then renders it in a female voice back to the caller. `Say` is useful in cases where it's difficult to pre-record a prompt for any reason. `Say` does not allow barge-in unless nested within a `GetSpeech` command. The file will always be played to completion unless nested.

When translating text to speech, the `Say` action will make assumptions about how to pronounce numbers, dates, times, amounts of money and other abbreviations.

### Example

```ruby
# load the gems
require 'sinatra'
require 'freeclimb'
require 'json'

post '/voice' do 
  say = Percl::Say.new('Hello, World!')
  script = Percl::Script.new
  script.add(say)
  script.to_json
end
```

### Parameters
Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**text** | **String** | The message to be played to the caller using TTS. The size of the string is limited to 4 KB (or 4,096 bytes). An empty string will cause the command to be skipped.
**loop** | **Integer** | Number of times the text is said. Specifying '0' causes the `Say` action to loop until the Call is hung up. | [optional]
**language** | **String** | Language and (by implication) the locale to use. This implies the accent and pronunciations to be usde for the TTS. The complete list of valid values for the language attribute is shown below. | [optional]
**conferenceId** | **String** | ID of the Conference the speech should be rendered to. If this is not specified, the speech is by default rendered to the Caller associated with the call leg that corresponds to the current PerCL execution context. The call leg associated with this command must be in the specified Conference or the command will return an error. | [optional]
**enforcePCI** | **Boolean** | Parameter `enforcePCI` will not log the 'text' as required by PCI compliance.


## Percl::GetDigits

The `GetDigits` command collects DTMF inputs from the caller. It is only supported only when there is a single party on the Call.

`GetDigits` is a Terminal Command — any actions following it are never executed. When the Caller is done entering the digits, FreeClimb submits that data to the provided `actionUrl` using an HTTP POST request. Your server will be required to respond to the FreeClimb Webhook with PerCL to continue handling the call.

### Example

```ruby
# load the gems
require 'sinatra'
require 'freeclimb'
require 'json'

post '/voice' do 
  digits = Percl::GetDigits.new('MOCK_ACTION_URL')
  script = Percl::Script.new
  script.add(digits)
  script.to_json
end
```

### Parameters
Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**actionUrl** | **String** | When the Caller has finished entering digits, FreeClimb will make an HTTP POST request to this URL. A PerCL response is expected to continue handling the Call. Make sure to keep “http://“ in the URL.
**initialTimeoutMs** | **Integer** | Maximum time in milliseconds that FreeClimb will wait for the Caller to press the first digit before making a determination that a `timeout` has occurred and moving on to make the request to the `actionUrl` to submit the results of the `GetDigits` command. This timeout interval begins when all nested commands have been fully executed. | [optional]
**digitTimeoutMs** | **Integer** | Maximum time in milliseconds that FreeClimb will wait for the Caller to press any digit after the last digit entered, before making a determination that a `timeout` has occurred and moving on to make the request to the actionUrl to submit the results of the `GetDigits` command. This timeout interval begins and resets after each digit entered. | [optional]
**finishOnKey** | **String** | Digit that causes the input sequence to be deemed complete. This attribute defers to the `timeout` attribute – so, if a `timeout` occurs, then the command terminates regardless of the value of `finishOnKey`. | [optional]
**minDigits** | **Integer** | Minimum number of digits expected in the input. If specified, FreeClimb will return the collected digits only if the Caller has entered at least that many digits. | [optional]
**maxDigits** | **Integer** | Maximum number of digits expected in the input. If the terminating digit is not entered and the caller has entered the maximum number of digits allowed, the `GetDigits` command terminates regardless of the value of `finishOnKey`. | [optional]
**prompts** | **String** | JSON array of PerCL commands to nest within the `GetDigits` command. The `Say`, `Play`, and `Pause` commands can be used. The nested actions are executed while FreeClimb is waiting for input from the Caller. | [optional]
**enforcePCI** | **Boolean** | Parameter `enforcePCI` obscures the result as required by PCI compliance.


## Percl::GetSpeech

The `GetSpeech` command enables the Caller to respond to the application using a supported language. Unlike DTMF entry, which implicitly restricts the user to using the available buttons on the phone key pad, speech input allows for flexible audio inputs based on grammar. FreeClimb supports grammars written using GRXML compatible with the Microsoft Speech Platform.

`GetSpeech` is only supported on a single call leg. It is not supported when there are two or more call legs connected (as in within a Conference).

### Example

```ruby
# load the gems
require 'sinatra'
require 'freeclimb'
require 'json'

post '/voice' do 
  speech = Percl::GetSpeech.new('MOCK_ACTION_URL', 'MOCK_GRAMMAR_FILE')
  script = Percl::Script.new
  script.add(speech)
  script.to_json
end
```

### Parameters
Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**actionUrl** | **String** | When the caller has finished speaking or the command has timed out, FreeClimb will make a POST request to this URL. A PerCL response is expected to continue handling the call.
**grammarFile** | **String** | The grammar file to use for speech recognition. If grammarType is set to URL, this attribute is specified as a download URL.
**grammarType** | **String** | The grammar file type to use for speech recognition. A value of 'URL' indicates the grammarFile attribute specifies a URL that points to the grammar file. A value of 'BUILTIN' indicates the grammarFile attribute specifies the name of one of the platform built-in grammar files. | [optional]
**grammarRule** | **String** | The grammar rule within the specified grammar file to use for speech recognition. This attribute is optional if `grammarType` is `URL` and ignored if `grammarType` is `BUILTIN`. | [optional if `grammarType` is `URL`]
**playBeep** | **Boolean** | Indicates whether a beep should be played just before speech recognition is initiated so that the speaker can start to speak. | [optional]
**prompts** | **Percl Commands Array** | The JSON array of PerCL commands to nest within the `GetSpeech` command. The `Say`, `Play`, and `Pause` commands can be used. The nested actions are executed while FreeClimb is waiting for input from the caller. This allows for playing menu options to the caller and to prompt for the expected input. These commands stop executing when the caller begins to input speech. | [optional]
**noInputTimeoutMs** | **Integer** | When recognition is started and there is no speech detected for `noInputTimeoutMs` milliseconds, the recognizer will terminate the recognition operation. | [optional]
**recognitionTimeoutMs** | **Integer** | When playback of prompts ends and there is no match for `recognitionTimeoutMs` milliseconds, the recognizer will terminate the recognition operation. | [optional]
**confidenceThreshold** | **Float** | When a recognition resource recognizes a spoken phrase, it associates a confidence level with that match. Parameter `confidenceThreshold` specifies what confidence level is considered a successful match. Values are between 0.0 and 1.0. | [optional]
**sensitivityLevel** | **Float** | The speech recognizer supports a variable level of sound sensitivity. The sensitivityLevel attribute allows for filtering out background noise, so it is not mistaken for speech. Values are between 0.0 and 1.0 | [optional]
**speechCompleteTimeoutMs** | **Integer** | Parameter `speechCompleteTimeoutMs` specifies the length of silence required following user speech before the speech recognizer finalizes a result. This timeout applies when the recognizer currently has a complete match against an active grammar. Reasonable speech complete timeout values are typically in the range of 0.3 seconds to 1.0 seconds. | [optional]
**speechIncompleteTimeoutMs** | **Integer** | Parameter `speechIncompleteTimeoutMs` specifies the length of silence following user speech after which a recognizer finalizes a result. This timeout applies when the speech prior to the silence is an incomplete match of all active grammars. Timeout `speechIncompleteTimeoutMs` is usually longer than `speechCompleteTimeoutMs` to allow users to pause mid-utterance. | [optional]
**enforcePCI** | **Boolean** | Parameter enforcePCI will not log the 'text' as required by PCI compliance. | [optional]


## Percl::Sms

The `Sms` command can be used to send an SMS message to a phone number during a phone call.

International SMS is disabled by default.

### Example

```ruby
# load the gems
require 'sinatra'
require 'freeclimb'
require 'json'

post '/voice' do 
  sms = Percl::Sms.new('MOCK_TO_NUMBER', 'MOCK_FROM_NUMBER', 'MOCK_TEXT')
  script = Percl::Script.new
  script.add(sms)
  script.to_json
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**to** | **String** | E.164 representation of the phone number to which the message will be sent. Must be within FreeClimb's service area and E.164 formatting (e.g., +18003608245).
**from** | **String** | E.164 representation of the phone number to use as the sender. This must be an incoming phone number you have purchased from FreeClimb.
**text** | **String** | Text contained in the message (maximum 160 characters).
**notificationUrl** | **String** | When the message changes status, this URL will be invoked using HTTP POST with the messageStatus parameters. This is a notification only; any PerCL returned will be ignored.
