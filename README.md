# WindowsPerformanceScore-Zabbix
 
1. Import `Windows Performance Score Template 64.yaml` to your Zabbix Server
2. Add the template to your ohsts

Macros:
 - {$CPUMINSCORE}
 - {$DISKMINSCORE}
 - {$GPUMINSCORE}
 - {$MEMMINSCORE}
 - {$SPRMINSCORE}

Items:
 - CPU Performance Score
 - Disk Performance Score
 - Graphics Performance Score
 - Memory Performance Score
 - SPR Performance Score
 
Trigger:
 - CPU Score is below recommended ({ITEM.VALUE} < {$CPUMINSCORE})
 - Disk Score is below recommended ({ITEM.VALUE} < {$DISKMINSCORE})
 - Graphics Score is below recommended ({ITEM.VALUE} < {$GPUMINSCORE})
 - Memory Score is below recommended ({ITEM.VALUE} < {$MEMMINSCORE})
 - SPR Score is below recommended ({ITEM.VALUE} < {$SPRMINSCORE})