### Manually check WMI Subscriptions
```
wmic/namespace:\\root\subscription PATH __EventConsumer get/format:list
wmic/namespace:\\root\subscription PATH __EventFilter get/format:list
wmic/namespace:\\root\subscription PATH __FilterToConsumerBinding get/ format:list
wmic/namespace:\\root\subscription PATH __TimerInstruction get/format:list.
```
### Remove WMI subscrption example
```
# Removing WMI Subscriptions using Remove-WMIObject
# Event Filter
Get-WMIObject -Namespace root\Subscription -Class __EventFilter -Filter “Name=’Updater’” | Remove-WmiObject -Verbose

# Event Consumer
Get-WMIObject -Namespace root\Subscription -Class CommandLineEventConsumer -Filter “Name=’Updater’” | Remove-WmiObject -Verbose

# Binding
Get-WMIObject -Namespace root\Subscription -Class __FilterToConsumerBinding -Filter “__Path LIKE ‘%Updater%’” | Remove-WmiObject -Verbose
```
