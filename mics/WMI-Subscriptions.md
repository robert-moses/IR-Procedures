# Manually check WMI Subscriptions
```
wmic/namespace:\\root\subscription PATH __EventConsumer get/format:list
wmic/namespace:\\root\subscription PATH __EventFilter get/format:list
wmic/namespace:\\root\subscription PATH __FilterToConsumerBinding get/ format:list
wmic/namespace:\\root\subscription PATH __TimerInstruction get/format:list.
```
