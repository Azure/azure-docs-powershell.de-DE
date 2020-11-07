---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusQueueKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusQueueKey.md
ms.openlocfilehash: 0a2bfe70e986b3ed92cef215cc23245216c0e961
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664978"
---
# New-AzureRmServiceBusQueueKey

## Synopsis
Generiert die primären oder sekundären Verbindungszeichenfolgen für die ServiceBus-Warteschlange erneut.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

```
New-AzureRmServiceBusQueueKey [-ResourceGroup] <String> [-NamespaceName] <String> [-QueueName] <String>
 [-AuthorizationRuleName] <String> [-RegenerateKeys] <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **New-AzureRmServiceBusQueueKey** generiert die primären oder sekundären Verbindungszeichenfolgen für die angegebene ServiceBus-Warteschlange und Autorisierungsregel erneut.

## Beispiele

### Beispiel 1
```
PS C:\> New-AzureRmServiceBusQueueKey -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_exampl1 -AuthorizationRuleName SBAuthoRule1 -RegenerateKeys PrimaryKey
```

Generiert die primäre Verbindungszeichenfolge für den Namespace erneut.

### Beispiel 2
```
PS C:\> New-AzureRmServiceBusQueueKey -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_exampl1 -AuthorizationRuleName SBAuthoRule1 -RegenerateKeys SecondaryKey
```

Generiert die sekundäre Verbindungszeichenfolge für den Namespace erneut.

## Parameter

### -Authorizationrulename
Der Name der Autorisierungsregel.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Namespacename
Der Name des ServiceBus-Namespaces.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Warteschlangen
Der Name der ServiceBus-Warteschlange.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RegenerateKeys
Gibt an, ob die primären oder sekundären Schlüssel neu generiert werden sollen.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: PrimaryKey, SecondaryKey

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroup
Der Name der Ressourcengruppe.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Bestätigen
Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.
Das Cmdlet wird nicht ausgeführt.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### -ResourceGroup
 System. String
 

### -Namespacename
 System. String
 

### -Authorizationrulename
 System. String
 

### -Warteschlangen
 System. String
 

### -RegenerateKeys
 System. String

## Ausgaben

### Microsoft. Azure. Management. ServiceBus. Models. ResourceListKeys
PrimaryConnectionString: Endpunkt = SB://SB-example1.ServiceBus.Windows.net/; SharedAccessKeyName = SBAuthoRule1; SharedAccessKey = {SharedAccessKey-Wert}; EntityPath = SB-Queue_exa mpl1 SecondaryConnectionString: Endpunkt = SB://SB-example1.ServiceBus.Windows.net/; SharedAccessKeyName = SBAuthoRule1; SharedAccessKey = {SharedAccessKey-Wert}; EntityPath = SB-Queue_exa mpl1 Primary: {Primärwert} SecondaryKey: {SecondaryKey Wert} keyName: SBAuthoRule1

## Notizen

## Verwandte Links

