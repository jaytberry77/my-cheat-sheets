# GOOGLE CLOUD PUB SUB CHEAT SHEET

`google cloud pub sub` _is a fully-managed real-time messaging
service that allows you to send and receive messages between
independent applications._

Documentation and reference,

* [Google Cloud Pub/Sub Documentation](https://cloud.google.com/pubsub/docs/)
* [Quickstart using console](https://cloud.google.com/pubsub/docs/quickstart-console)
* [Quickstart using gcloud pubsub](https://cloud.google.com/pubsub/docs/quickstart-cli)
* [Google Cloud Pub/Sub SDK Reference (gcloud pubsub)](https://cloud.google.com/sdk/gcloud/reference/pubsub/)

View my entire list of cheat sheets on
[my GitHub Webpage](https://jeffdecola.github.io/my-cheat-sheets/).

## PUB/SUB FREE TIER

The pub/sub free tier is,

* 10GB of messages per month.

Full list of [free gcp services](https://cloud.google.com/free/docs/gcp-free-tier).

## LOCAL PUB/SUB INSTALL

[Local Pub/Sub Install](https://cloud.google.com/pubsub/docs/emulator)

Must install Java JRE

```bash
sudo apt-get update
sudo apt-get install default-jre
```

## STEP 1 - START

```bash
gcloud beta emulators pubsub start \
    --data-dir="/home/jeff/.config/gcloud/emulators/pubsub"
```

## STEP 2 - CALL evn-init

Make your code call the API running in the local
instance instead of the production API, hence
run the env-init command in another terminal,

$(gcloud beta emulators pubsub env-init)

To see command line arguments,

```bash
gcloud beta emulators pubsub --help
```

## GCLOUD BETA - PUB/SUB

Beta versions of gcloud commands such as ones for pubsub.

List whats available

```bash
gcloud help beta
```

List pubsub topics,

```bash
gcloud beta pubsub topics list
```

List pubsub subscriptions,
This lists everything, so it can be a long list.

```bash
gcloud beta pubsub subscriptions list
```
