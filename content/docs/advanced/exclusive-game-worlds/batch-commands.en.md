---
title: "Batch Commands"
weight: 2
---

# Batch Commands

There are certain reoccurring tasks specific to exclusive game worlds, like adding funds to an airline or generating a
new batch of used aircraft. Individually, these are easy to manage. But once there are a lot of them to execute at once,
like after game world setup or when handing out fresh funds to all players in a world, these quickly become tedious.

This is where _batch commands_ come in: As the name suggests, these allow to execute many commands in a single batch.
This decreases the chance for errors and the workload both for game world owners and AirlineSim support staff.

## Working principle

Batch commands are simply a list of commands followed by one or more parameters. Command and parameters are separated by
tabs or semicolons. As such, batch commands are best prepared in a regular spreadsheet. Ideally, this is a Google
Sheet so you can just share the respective link with support.

Here's an example:

```
remove_funds	Batch Airlines  1000000
add_user    BatchUse
```

As you'd expect, this batch will remove 1,000,000 ASD from `Batch Airlines` and activate the user `BatchUser` in the
respective game world.

**Important:** All values referencing a particular resource, like usernames or aircraft types, need to be **exact**. AirlineSim cannot and will not "guess" what the closest match might be.

## Available commands

Below you can find a reference of all currently implemented commands. Values wrapped in curly braces (like `{THIS}`)
need to be replaced with the respective value.

### Add User

```
add_user    {DISPLAY_NAME}
```

`{DISPLAY_NAME}` is the user's account display name. Make sure to copy that name _exactly_.

### Remove User

```
remove_user    {DISPLAY_NAME}
```
`{DISPLAY_NAME}` is the user's account display name. Make sure to copy that name _exactly_.

### Add Funds

```
add_funds    {COMPANY_NAME} {AMOUNT}
```

- `{COMPANY_NAME}` is the _exact_ name of the company to receive the fund.
- `{AMOUNT}` is the amount to add in ASD without decimals. `.` or `,` as thousands separator are supported, but not recommended. 

### Remove Funds

```
remove_funds    {COMPANY_NAME} {AMOUNT}
```

- `{COMPANY_NAME}` is the _exact_ name of the company to remove the funds from.
- `{AMOUNT}` is the amount to remove in ASD without decimals. `.` or `,` as thousands separator are supported, but not recommended. 

### Generate Aircraft

This command generates the given amount of aircraft for the given type.

Note that for initial setup or reset of game worlds, it is easier to generate the (initial) set of used aircraft using a custom aircraft availabilities sheet. Support will help you with setting this up.

```
generate_aircraft    {AIRCRAFT_TYPE} {AMOUNT}
```

- `{AIRCRAFT_TYPE}` is the _exact_ name of the aircraft type to create aircraft of.
- `{AMOUNT}` is the amount of aircraft to generate. 