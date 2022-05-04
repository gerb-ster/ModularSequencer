# Modular Sequencer

A modular sequencer consisting of a control module and 1 or more linkable io-modules. Al daisychained together.

## Notes

- All connected by a parallel SPI bus.
- contains 1 serial connected line for discovery
- a termination jumper for the last io-board
- all io-boards start up in a discovery mode
- if io board has termination jumper it sends signal
- control boards send an ID which is registered by io board
- io board goes out of discovery mode and sets discovery line high
- this triggers the same process in the ajasoned io-board module
- this goes on until control board senses a discovery line high
- play mode is then activated
- control board sends a gate active command; board_id + port + on / off
- io board scans inputs, gate on/off, cv value & gate length for all of its 4 ports and sends it to the control board.

## features

### Main Control Board

- tempo pot
- tempo external input (bpm)
- tempo CV input (?)
- start / stop button
- start / stop trigger inputs (?)
- CV output
- CV Portamento
- Gate Output

### IO Board

- 4x CV level pot
- 4x Gate length pot
- 4x Gate on/off toggle switch
- 4x Step indicator LED