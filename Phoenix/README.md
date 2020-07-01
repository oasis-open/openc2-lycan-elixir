# Phoenix Webserver as OpenC2 API
see BlinkyHaha for more as this gets developed

API/lib/router.ex controls what url parts map to what software where.

The following code says /openc2 on the url maps to the OC2Controller command function
```
scope "/openc2", UiWeb do
  pipe_through :api
  post "/", OC2Controller, :command
end
```

API/lib/ox2_controller.ex is the OC2Controller module with the
command function which parses the json and executes the OpenC2 command.

