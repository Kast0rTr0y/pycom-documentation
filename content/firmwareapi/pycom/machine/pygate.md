---
title: "Pygate"
aliases:
    - firmwareapi/pycom/machine/pygate.html
    - firmwareapi/pycom/machine/pygate.md
    - chapter/firmwareapi/pycom/machine/pygate
---

The Pygate is an 8-channel LoRaWAN gateway. You connect a WiPy or Gpy board to the Pygate and flash a firmware build where the Pygate functionality is enabled. See the [Pygate tutorial](/tutorials/all/pygate) to get started.

## Methods

#### machine.pygate\_init(buff)

This function is used to initialize the Pygate

- `buff`: the data contents of the gateway global config json file

#### machine.pygate\_deinit()

This shuts down the concentrator.

#### machine.callback(trigger, handler=None, arg=None)

- `trigger`: A trigger event(s) for invoking the callback function `handler`, the triggers/events are:

	`machine.PYGATE_START_EVT`

	`machine.PYGATE_STOP_EVT`

	`machine.MP_QSTR_PYGATE_ERROR_EVT`

- `handler`: The callback function to be called.  When not passed to function, any pre-registered callback will be disabled/removed.

- `arg`: Optional argument to be passed to the callback function.

#### machine.events()

Get the Pygate events
