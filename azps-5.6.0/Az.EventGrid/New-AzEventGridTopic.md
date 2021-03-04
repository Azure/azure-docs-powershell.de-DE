---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/powershell/module/az.eventgrid/new-azeventgridtopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridTopic.md
ms.openlocfilehash: df81f976f571a59f68d51ef734f1bc3ea5536015
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101938731"
---
# New-AzEventGridTopic

## SYNOPSIS
Erstellt ein neues Azure Event Grid Topic.

## SYNTAX

```
New-AzEventGridTopic [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-Tag <Hashtable>]
 [-InputSchema <String>] [-InputMappingField <Hashtable>] [-InputMappingDefaultValue <Hashtable>]
 [-InboundIpRule <Hashtable>] [-PublicNetworkAccess <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## BESCHREIBUNG
Erstellt ein neues Azure Event Grid Topic. Nachdem das Thema erstellt wurde, kann eine Anwendung Ereignisse auf dem Themenendpunkt veröffentlichen.

## BEISPIELE

### Beispiel 1
```powershell
PS C:\> New-AzEventGridTopic -ResourceGroupName MyResourceGroupName -Name Topic1 -Location westus2
```

Erstellt ein Ereignisrasterthema Topic1 am angegebenen geografischen Standort \` \` \` westus2 \` in der Ressourcengruppe \` MyResourceGroupName \` .

### Beispiel 2
```powershell
PS C:\> New-AzEventGridTopic -ResourceGroupName MyResourceGroupName -Name Topic1 -Location westus2 -Tag @{ Department="Finance"; Environment="Test" }
```

Erstellt ein Ereignisrasterthema Topic1 am angegebenen geografischen Standort westus2 in der Ressourcengruppe MyResourceGroupName mit den angegebenen Tags \` \` \` \` \` \` "Department" und "Environment".

## PARAMETER

### -DefaultProfile
Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden

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

### -InboundIpRule
Hashtable, die eine Liste der eingehenden #A0 darstellt. Jede Regel gibt die IP-Adresse in der CIDR-Notation an, z. B. 10.0.0.0/8 zusammen mit der entsprechenden Aktion, die basierend auf der Übereinstimmung oder keiner Übereinstimmung der IpMask ausgeführt werden soll. Mögliche Aktionswerte umfassen Nur zulassen

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -InputMappingDefaultValue
Hashtable, die die Eingabezuordnungsfelder mit dem Standardwert im Leerzeichen getrennten Schlüssel = Wertformat darstellt. Zulässige Schlüsselnamen sind: Betreff, Ereignistyp und Datenversion. Dies wird verwendet, wenn InputSchemaHelp nur customeventschema ist.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -InputMappingField
Hashtable, die die Eingabezuordnungsfelder im Leerzeichen getrennten Schlüssel = Wertformat darstellt. Zulässige Schlüsselnamen sind: ID, Thema, Ereigniszeit, Betreff, Ereignistyp und Datenversion. Dies wird verwendet, wenn InputSchemaHelp nur customeventschema ist.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -InputSchema
Das Schema der Eingabeereignisse für das Thema. Zulässige Werte sind: eventgridschema, customeventschema oder cloudeventv01Schema. Standardwert ist eventgridschema. Beachten Sie, dass bei Angabe von customeventschema auch die Parameter InputMappingField oder/und InputMappingDefaultValue angegeben werden müssen.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: EventGridSchema, CustomEventSchema, CloudEventSchemaV1_0

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Location
Der Speicherort des Themas

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name
Der Name des Themas.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PublicNetworkAccess
Dadurch wird bestimmt, ob Datenverkehr über das öffentliche Netzwerk zulässig ist. Standardmäßig ist es aktiviert. Sie können weitere Beschränkungen auf bestimmte IPs durch Konfigurieren von InboundIpRule-Parametern festlegen. Zulässige Werte sind deaktiviert und aktiviert.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: enabled, disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Die Ressourcengruppe, in der das Thema erstellt werden soll.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Tag
Hashtables, die Ressourcentags darstellt.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Bestätigen
Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.
Das Cmdlet wird nicht ausgeführt.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## EINGABEN

### System.String

### System.Collections.Hashtable

## AUSGABEN

### Microsoft.Azure.Commands.EventGrid.Models.PSTopic

## NOTIZEN

## VERWANDTE LINKS
