---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusQueueKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusQueueKey.md
ms.openlocfilehash: 4faca15a0c348ee1011789db5acd227c06ee1b85
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501606"
---
# Get-AzureRmServiceBusQueueKey

## Synopsis
Ruft die primären und sekundären Verbindungszeichenfolgen für die angegebene ServiceBus-Warteschlange ab.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

```
Get-AzureRmServiceBusQueueKey [-ResourceGroup] <String> -Namespace <String> -Queue <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzureRmServiceBusQueueKey** " gibt die primären und sekundären Verbindungszeichenfolgen für die angegebene ServiceBus-Warteschlange zurück. 

## Beispiele

### Beispiel 1
```
PS C:\> Get-AzureRmServiceBusQueueKey -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_exampl1 -AuthorizationRuleName SBAuthoRule1
```

Gibt die primären und sekundären Verbindungszeichenfolgen für die angegebene ServiceBus-Warteschlange zurück.

## Parameter

### -ResourceGroup
Der Name der Ressourcengruppe.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
AuthorizationRule-Name der ServiceBus-Warteschlange.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Namespace
Name des ServiceBus-Namespaces.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Queue
Name der ServiceBus-Warteschlange.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: QueueName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### -ResourceGroup
 System. String
 

### -Namespacename
 System. String
 

### -Warteschlangen
 System. String
 

### -Authorizationrulename
 System. String

## Ausgaben

### Microsoft. Azure. Commands. ServiceBus. Models. ListKeysAttributes
PrimaryConnectionString: Endpunkt = SB://SB-example1.ServiceBus.Windows.net/; SharedAccessKeyName = SBAuthoRule1; SharedAccessKey = {SharedAccessKey-Wert}; EntityPath = SB-Queue_e xampl1 SecondaryConnectionString: Endpunkt = SB://SB-example1.ServiceBus.Windows.net/; SharedAccessKeyName = SBAuthoRule1; SharedAccessKey = {SharedAccessKey-Wert}; EntityPath = SB-Queue_e xampl1 Primary: {Primärwert} SecondaryKey: {SecondaryKey Wert} keyName: SBAuthoRule1

## Notizen

## Verwandte Links

