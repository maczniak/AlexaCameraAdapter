# AlexaCameraAdapter

camera (or RTSP media source) integration with Echo Show

## Requirement

* `DiscoverAppliancesRequest` and OAuth 2.0 handling because camera skills
  belong to Smart Home Skill API
* camera-specific `RetrieveCameraStreamUriRequest` handling
* RTP and RTPS on TCP port 443 with TLS 1.0
* SSL certificate for a valid domain
* H.264 and AAC/G711 codecs
* HTTP Digest authentication

## Reference

[Building Smart Home Camera Skills](https://developer.amazon.com/public/solutions/alexa/alexa-skills-kit/docs/building-smart-home-camera-skills)
> ### Local and Remote Execution Recommendations
> There are no requirements regarding whether you should return a URI that is on
> the same local network as the device with Alexa or a remote URI accessible
> from anywhere with an Internet connection. You should return what makes the
> most sense for your device cloud configuration. Regardless of your URI choice,
> all technical requirements must still be met including TLS 1.0 support.<br>
> In general, a URI is not reachable both locally and remotely by default. You
> can make the URI accessible locally and remotely through domain purchasing or
> port forwarding. These solutions are technically challenging and so you should
> provide this kind of solution only if your customers need both local and
> remote URI access.

[Smart Home Skill API Reference](https://developer.amazon.com/public/solutions/alexa/alexa-skills-kit/docs/smart-home-skill-api-reference)
> The URI to the feed for the camera specified in the request. The hostname of
> this URI must be a valid domain that can be verified as a Common Name or
> Subject Alternative Name in your SSL certificate. Hostnames that contain IP
> addresses will be rejected.

