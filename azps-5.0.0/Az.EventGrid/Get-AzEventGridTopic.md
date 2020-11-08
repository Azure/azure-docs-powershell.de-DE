---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/get-azeventgridtopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopic.md
ms.openlocfilehash: df3f6673729a868e7aeb349a34fba32b2033862e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94177670"
---
# Get-AzEventGridTopic

## Synopsis
Ruft die Details eines Ereignis Raster Themas ab oder ruft eine Liste aller Themen des Ereignis Rasters im aktuellen Azure-Abonnement ab.

## Syntax

### ResourceGroupNameParameterSet (Standard)
```
Get-AzEventGridTopic [[-ResourceGroupName] <String>] [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### TopicNameParameterSet
```
Get-AzEventGridTopic [-ResourceGroupName] <String> [-Name] <String> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceIdEventSubscriptionParameterSet
```
Get-AzEventGridTopic [-ResourceId] <String> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### NextLinkParameterSet
```
Get-AzEventGridTopic [-NextLink <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Get-AzEventGridTopic-Cmdlet ruft entweder die Details eines angegebenen Ereignis Raster Themas oder eine Liste aller Themen des Ereignis Rasters im aktuellen Azure-Abonnement ab.
Wenn der Name des Themas angegeben ist, werden die Details für ein einzelnes Ereignis Raster Thema zurückgegeben.
Wenn der Name des Themas nicht angegeben wird, wird eine Liste der Themen zurückgegeben. Die Anzahl der in dieser Liste zurückgegebenen Elemente wird durch den Top-Parameter gesteuert. Wenn der obere Wert nicht angegeben oder $NULL ist, enthält die Liste alle themenelemente. Andernfalls zeigt Top die maximale Anzahl von Elementen an, die in der Liste zurückgegeben werden sollen.
Wenn noch weitere Themen verfügbar sind, sollte der Wert in Nextlink beim nächsten Aufruf verwendet werden, um die nächste Seite mit Themen abzurufen.
Schließlich wird ODataQuery-Parameter verwendet, um die Filterung für die Suchergebnisse durchzuführen. Die Filterabfrage folgt der OData-Syntax, wobei nur die Name-Eigenschaft verwendet wird. Zu den unterstützten Vorgängen gehören: Contains, EQ (für EQUAL), ne (für ungleich), und, oder und nicht.

## Beispiele

### Beispiel 1
```powershell
PS C:\> Get-AzEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1
```

Ruft die Details des Ereignis Rasters Topic \` THEMA1 hat \` in Resource Group \` MyResourceGroupName \` .

### Beispiel 2
```powershell
PS C:\> Get-AzEventGridTopic -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/topics/Topic1"
```

Ruft die Details des Ereignis Rasters Topic \` THEMA1 hat \` in Resource Group \` MyResourceGroupName \` .

### Beispiel 3
```powershell
PS C:\> Get-AzEventGridTopic -ResourceGroup MyResourceGroupName
```

Listen Sie alle Themen des Ereignis Rasters in der Ressourcengruppe \` MyResourceGroupName \` ohne Paginierung auf.

### Beispiel 4
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> $result = Get-AzEventGridTopic -ResourceGroup MyResourceGroupName -Top 10 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridTopic $result.NextLink
```

Listen Sie die ersten 10 Themen des Ereignis Rasters (sofern vorhanden) in der Ressourcengruppe \` MyResourceGroupName auf \` , die die $odataFilter Abfrage erfüllt. Wenn weitere Ergebnisse zur Verfügung stehen, wird die $Result. Nextlink wird nicht $NULL. Um die nächste Seite (n) von Themen zu erhalten, wird erwartet, dass der Benutzer Get-AzEventGridTopic erneut anruft und Ergebnis verwendet. Nextlink, der aus dem vorherigen Anruf abgerufen wurde. Der Anrufer sollte beim Ergebnis beendet werden. Nextlink wird $NULL.

### Beispiel 5
```powershell
PS C:\> Get-AzEventGridTopic
```

Listen Sie alle Themen des Ereignis Rasters im Abonnement ohne Paginierung auf.

### Beispiel 6
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> $result = Get-AzEventGridTopic -Top 10 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridTopic $result.NextLink
```

Listen Sie die ersten 10 Themen des Ereignis Rasters (sofern vorhanden) im Abonnement auf, das die $odataFilter Abfrage erfüllt. Wenn weitere Ergebnisse zur Verfügung stehen, wird die $Result. Nextlink wird nicht $NULL. Um die nächste Seite (n) von Themen zu erhalten, wird erwartet, dass der Benutzer Get-AzEventGridTopic erneut anruft und Ergebnis verwendet. Nextlink, der aus dem vorherigen Anruf abgerufen wurde. Der Anrufer sollte beim Ergebnis beendet werden. Nextlink wird $NULL.

## Parameter

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
EventGrid-Themen Name

```yaml
Type: System.String
Parameter Sets: TopicNameParameterSet
Aliases: TopicName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Nextlink
Der Link für die nächste Seite der Ressourcen, die abgerufen werden sollen. Dieser Wert wird mit dem ersten Get-AzEventGrid-Cmdlet-Aufruf abgerufen, wenn noch weitere Ressourcen zur Abfrage zur Verfügung stehen.

```yaml
Type: System.String
Parameter Sets: NextLinkParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ODataQuery
Die OData-Abfrage, die zum Filtern der Listenergebnisse verwendet wird. Das Filtern ist derzeit nur für die Name-Eigenschaft zulässig. Zu den unterstützten Vorgängen gehören: Contains, EQ (für EQUAL), ne (für ungleich), und, oder und nicht.

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, TopicNameParameterSet, ResourceIdEventSubscriptionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Name der Ressourcengruppe.

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet
Aliases: ResourceGroup

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: TopicNameParameterSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Resourcen-Nr
Ressourcenbezeichner, der das Thema des Ereignis Rasters darstellt.

```yaml
Type: System.String
Parameter Sets: ResourceIdEventSubscriptionParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Top
Die maximale Anzahl von Ressourcen, die abgerufen werden sollen. Gültiger Wert ist zwischen 1 und 100. Wenn Top-Wert angegeben ist und weitere Ergebnisse weiterhin verfügbar sind, enthält das Ergebnis einen Link zur nächsten Seite, die in Nextlink abgefragt werden soll. Wenn der obere Wert nicht angegeben wird, wird die vollständige Liste der Ressourcen gleichzeitig zurückgegeben.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ResourceGroupNameParameterSet, TopicNameParameterSet, ResourceIdEventSubscriptionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## Eingaben

### System. String

### System. Nullable ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]

## Ausgaben

### Microsoft. Azure. Commands. EventGrid. Models. PSTopic

### Microsoft. Azure. Commands. EventGrid. Models. PSTopicListInstance

## Notizen

## Verwandte Links
