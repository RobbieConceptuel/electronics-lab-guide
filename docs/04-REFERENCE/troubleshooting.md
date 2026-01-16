# Troubleshooting

Common problems and how to fix them.

---

## Soldering Problems

| Problem | Cause | Solution |
|---------|-------|----------|
| Solder will not melt | Temperature too low | Increase by 20-30C |
| Solder will not stick | Dirty or oxidized surface | Clean with IPA, add flux |
| Dull/grainy joint | Cold joint (not enough heat) | Reheat with flux |
| Solder balls up | No flux on surface | Add flux |
| Bridge between pins | Too much solder | Use solder wick, try again with less |
| Tip will not tin | Oxidized tip | Clean with brass, apply tip tinner |
| Burn marks | Temperature too high | Reduce temperature |
| Lifted pad | Too much heat or force | Work faster, be gentler |

---

## Circuit Not Working

### Before You Power On

1. Visual check - Look for obvious problems
2. Check for shorts - Continuity test between power and ground (should NOT beep)
3. Check component orientation - ICs, diodes, electrolytic capacitors
4. Check all joints - Look for cold joints or bridges

### After Power On

1. Check voltage at power pins - Is the IC getting power?
2. Check for heat - Anything getting hot means a problem
3. Check voltage at outputs - Is anything happening?

---

## Power Issues

| Symptom | Possible Cause | Check |
|---------|----------------|-------|
| Nothing powers on | No power | Voltage at power input |
| Immediate short | Reversed polarity | Check orientation of polarized parts |
| Power but nothing works | Voltage at wrong level | Measure actual voltage |
| Gets hot immediately | Short circuit | Look for bridges, wrong components |

---

## Communication Problems

### I2C Not Working

- Check pull-up resistors (usually need 4.7k on SDA and SCL)
- Check wiring (SDA to SDA, SCL to SCL)
- Verify correct I2C address
- Try scanning for devices

### SPI Not Working

- Check wiring (MOSI, MISO, CLK, CS)
- Verify chip select is going low
- Check SPI mode setting

### UART Not Working

- TX connects to RX, RX connects to TX (cross-connect)
- Check baud rate matches on both ends
- Check voltage levels (3.3V vs 5V)

---

## Common Component Failures

### Capacitors

- Bulging top = failed, replace
- Leaking = failed, replace
- Shorted (reads 0 ohms) = failed, replace

### Diodes/LEDs

- No forward voltage in diode test = shorted or open
- Check polarity first

### Voltage Regulators

- Output wrong = check input voltage (needs to be higher than output)
- Getting hot = too much current or insufficient heatsink

---

## When to Start Over

Sometimes a board is too damaged to fix:

- Multiple lifted pads
- Burnt traces
- Components not available
- Time spent exceeds cost of new board

Document what went wrong so you do not repeat it.

---

## Debug Mindset

1. **Observe** - What exactly is not working?
2. **Hypothesize** - What could cause this?
3. **Test** - Check your hypothesis with measurement
4. **Fix** - Address what you found
5. **Verify** - Did the fix work?

Work systematically. Change one thing at a time.

---

[Back to Pinouts](pinouts.md) | [Back to main page](../../README.md)
