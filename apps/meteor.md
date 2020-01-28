# Meteor

<!-- TOC -->

- [METEOR_SETTINGS](#meteor_settings)
- [METEOR_PACKAGE_DIRS](#meteor_package_dirs)
- [ROOT_URL](#root_url)
- [MONGO_OPLOG_URL](#mongo_oplog_url)
- [MONGO_URL](#mongo_url)
- [BIND_IP](#bind_ip)
- [PORT](#port)
- [DISABLE_WEBSOCKETS](#disable_websockets)
- [HTTP_FORWARDED_COUNT](#http_forwarded_count)
- [MAIL_URL](#mail_url)

<!-- /TOC -->

List of environment variables settable by Meteor.

## METEOR_SETTINGS
- (production)
- In production, when running the bundled app, pass a string of JSON containing your settings
- e.g. `METEOR_SETTINGS='{ "server_only_setting": "foo","public": { "client_and_server_setting": "bar"} }'`
- In development, pass the settings on command line, to enjoy full-reactivity when changing settings, e.g. `meteor --settings [file.json]`
- see docs for `Meteor.settings`

## METEOR_PACKAGE_DIRS
- (development, production)
- Colon-delimited list of local package directories to look in, outside your normal app structure
- for example: `METEOR_PACKAGE_DIRS="/usr/local/my_packages/"`
- Note that this used to be PACKAGE_DIRS but was changed in Meteor 1.4.2.

## ROOT_URL
- (development, production)
- Used to generate URLs to your app by, among others, the accounts package. Provide a full URL to your app
- e.g. `ROOT_URL="https://www.myapp.com"`

## MONGO_OPLOG_URL
- (development, production)
- MongoDB server oplog URL
- If you’re using a replica set (which you should), construct this url like so: `MONGO_URL="mongodb://user@password:myserver.com:10139/local?replicaSet=(your replica set)&authSource=(your auth source)"`

## MONGO_URL
- (development, production)
- MongoDB server URL
- Give a fully qualified URL (or comma-separated list of URLs) like `MONGO_URL="mongodb://user@password:myserver.com:10139"`
- For more information see the MongoDB docs.

## BIND_IP
- scope: production
- Bind the app server to a specific network interface by IP address
- e.g. `BIND_IP=192.168.0.2`
- see also: `PORT`
- In development, this can be done with `meteor run --port a.b.c.d:port`

## PORT
- (production)
- Which port the app should listen on
- for example: PORT=3030
- See also: BIND_IP
- In development, this can be accomplished with `meteor run --port <port>`

## DISABLE_WEBSOCKETS
- scope: development, production
- Explicitly disable WebSockets and forcibly resort to the fallback polling mechanism, instead of trying to detect this automatically.
- e.g. `DISABLE_WEBSOCKETS=1`

## HTTP_FORWARDED_COUNT
- production
- Set this to however many number of proxies you have running before your Meteor app.
- For example, if have an NGINX server acting as a proxy before your Meteor app, you would set HTTP_FORWARDED_COUNT=1. If you have a load balancer in front of that NGINX server, the count is 2.

## MAIL_URL
- (development, production)
- If you’re using an external mail service like Postmark, Mandrill, MailGun or 
SendGrid, you can provide a SMTP URL for your Meteor app to use to send e-mail.
- For example: MAIL_URL="smtp://user@pass:yourservice.com:587".
