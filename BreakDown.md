# Lyrically
Small music player application  with lyrics fetch function

The first step is to request authorization from the user, so our app can access to the Spotify resources in behalf that user. To do so, our application must build and send a GET request to the /authorize endpoint with the following parameters:

QUERY PARAMETER	VALUE
client_id-	Required
            The Client ID generated after registering your application.
response_type-	Required Set to code.
redirect_uri-	Required
    The URI to redirect to after the user grants or denies permission. This URI needs to have been entered in the Redirect URI allowlist that you specified when you         registered your application (See the app settings guide). The value of redirect_uri here must exactly match one of the values you entered when you registered your       application, including upper or lowercase, terminating slashes, and such.
state -	Optional, but strongly recommended
        This provides protection against attacks such as cross-site request forgery. See RFC-6749.
scope- 	Optional
        A space-separated list of scopes.If no scopes are specified, authorization will be granted only to access publicly available information: that is, only                   information normally visible in the Spotify desktop, web, and mobile players.
show_dialog-	Optional
        Whether or not to force the user to approve the app again if they’ve already done so. If false (default), a user who has already approved the application may be         automatically redirected to the URI specified by redirect_uri. If true, the user will not be automatically redirected and will have to approve the app again.
