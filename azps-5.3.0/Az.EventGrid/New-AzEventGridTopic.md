---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/new-azeventgridtopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridTopic.md
ms.openlocfilehash: 402d781c32b98362d504dd5167024932d82e64fb
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98458715"
---
# New-AzEventGridTopic

## SYNOPSIS
Erstellt ein neues Azure-Veranstaltungsrasterthema.

## SYNTAX

```
New-AzEventGridTopic [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-Tag <Hashtable>]
 [-InputSchema <String>] [-InputMappingField <Hashtable>] [-InputMappingDefaultValue <Hashtable>]
 [-InboundIpRule <Hashtable>] [-PublicNetworkAccess <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## BESCHREIBUNG
Erstellt ein neues Azure-Veranstaltungsrasterthema. Nachdem das Thema erstellt wurde, kann eine Anwendung Ereignisse am Themenendpunkt veröffentlichen.

## BEISPIELE

### Beispiel 1
```powershell
PS C:\> New-AzEventGridTopic -ResourceGroupName MyResourceGroupName -Name Topic1 -Location westus2
```

Erstellt ein Ereignisrasterthema "Topic1" am angegebenen geografischen Standort \` \` \` "westus2" \` in der Ressourcengruppe \` "MyResourceGroupName". \`

### Beispiel 2
```powershell
PS C:\> New-AzEventGridTopic -ResourceGroupName MyResourceGroupName -Name Topic1 -Location westus2 -Tag @{ Department="Finance"; Environment="Test" }
```

Erstellt ein Ereignisrasterthema "Topic1" am angegebenen geografischen Standort "westus2" in der Ressourcengruppe \` \` \` \` "MyResourceGroupName" mit den angegebenen Tags \` \` "Department" und "Environment".

## PARAMETERS

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
Hashtable, die eine Liste der eingehenden #A0 darstellt. Jede Regel gibt die IP-Adresse in der CIDR-Notation an, z. B. 10.0.0.0/8, zusammen mit der entsprechenden Aktion, die basierend auf der Übereinstimmung oder keiner Übereinstimmung des "IpMask" ausgeführt werden soll. Mögliche Aktionswerte umfassen "Nur zulassen"

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
Hashtable, die die Eingabezuordnungsfelder mit einem Standardwert im #A0 = Wertformat darstellt. Zulässige Schlüsselnamen sind: Betreff, Ereignistyp und Datenversion. Dies wird verwendet, wenn InputSchemaHelp nur "customeventschema" ist.

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
Hashtable, die die Eingabezuordnungsfelder im Format "Leertaste = Wert" darstellt. Zulässige Schlüsselnamen sind: id, topic, eventtime, subject, eventtype und dataversion. Dies wird verwendet, wenn InputSchemaHelp nur "customeventschema" ist.

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
Das Schema der Eingabeereignisse für das Thema. Zulässige Werte sind: eventgridschema, customeventschema oder cloudeventv01Schema. Der Standardwert ist "eventgridschema". Beachten Sie, dass bei Angabe von "customeventschema" auch die Parameter "InputMappingField" oder/und "InputMappingDefaultValue" angegeben werden müssen.

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
Dies bestimmt, ob Datenverkehr über ein öffentliches Netzwerk zulässig ist. Standardmäßig ist sie aktiviert. Sie können weiter auf bestimmte IPs beschränken, indem Sie die Parameter für "InboundIpRule" konfigurieren. Zulässige Werte sind deaktiviert und aktiviert.

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

### -Confirm
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

### -Waswenn
Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.
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
Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## EINGABEN

### System.String

### System.Collections.Hashtable

## AUSGABEN

### Microsoft.Azure.Commands.EventGrid.Models.PSTopic

## HINWEISE

## LINKS ZU VERWANDTEN THEMEN
