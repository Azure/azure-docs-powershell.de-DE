---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/powershell/module/az.privatedns/Set-AzPrivateDnsZone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Set-AzPrivateDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Set-AzPrivateDnsZone.md
ms.openlocfilehash: b28153176fdc591bc7298b45f75e8befa59e8554
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101936667"
---
# Set-AzPrivateDnsZone

## SYNOPSIS
Aktualisiert eine private DNS-Zone aus einer Ressourcengruppe.

## SYNTAX

### Felder (Standard)
```
Set-AzPrivateDnsZone -ResourceGroupName <String> -Name <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ResourceId
```
Set-AzPrivateDnsZone -ResourceId <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Objekt
```
Set-AzPrivateDnsZone -PrivateZone <PSPrivateDnsZone> [-Tag <Hashtable>] [-Overwrite]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## BESCHREIBUNG
Das **Cmdlet Set-AzPrivateDnsZone** aktualisiert dauerhaft eine Zone des privaten Domain Name System (DNS) aus einer angegebenen Ressourcengruppe.
Sie können ein **PrivateDnsZone-Objekt** mithilfe des *Parameters PrivateZone* oder mithilfe des Pipelineoperators übergeben oder alternativ die Parameter *Name* und *ResourceGroupName* angeben.
Sie können den Parameter Bestätigen und die $ConfirmPreference Windows PowerShell verwenden, um zu steuern, ob das Cmdlet Sie zur Bestätigung aufgefordert.
Wenn Sie die Zone mit einem **PrivateDnsZone-Objekt** angeben (über die Pipeline oder den Parameter Zone übergeben), wird die Zone nicht aktualisiert, wenn sie in Azure DNS geändert wurde, seit das lokale **PrivateDnsZone-Objekt** abgerufen wurde (nur Vorgänge direkt auf der DNS-Zonenressourcenanzahl als Änderungen, Vorgänge für Datensatzsätze innerhalb der Zone nicht). 
Dies bietet Schutz für gleichzeitige Zonenänderungen.
Dies kann mit dem Parameter *Überschreiben* unterdrückt werden, der die Zone unabhängig von gleichzeitigen Änderungen aktualisiert.

## BEISPIELE

### Beispiel 1: Aktualisiert eine private Zone
```
PS C:\>Set-AzPrivateDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup" -Tag @{tag1="value1";tag2="value2"}


This command updates the zone named myzone.com from the resource group named MyResourceGroup with the tags provided. Use Get-AzPrivateDnsZone to retrieve the updated zone. Updated zone would look something like this:

Name                          : myzone.com
ResourceId                    : "/subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/PrivateZones/myzone.com"
ResourceGroupName             : MyResourceGroup
Location                      : 
Etag                          : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Tags                          : {tag1="value1";tag2="value2"}
NumberOfRecordSets            : 1
MaxNumberOfRecordSets         : 5000
```

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

### -Name
Gibt den Namen der privaten DNS-Zone an, die von diesem Cmdlet aktualisiert wird.
Sie müssen auch den *Parameter ResourceGroupName* angeben.
Alternativ können Sie die private DNS-Zone mit dem Parameter *Zone* angeben.

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Overwrite
Wenn Sie die Zone mithilfe eines **PrivateDnsZone-Objekts** angeben (über die Pipeline oder den Parameter Zone übergeben), wird die Zone nicht aktualisiert, wenn sie seit dem Abrufen des lokalen **DnsZone-Objekts** in Azure DNS geändert wurde (nur Vorgänge direkt auf der DNS-Zone werden als Änderungen gezählt, Vorgänge für Datensatzsätze innerhalb der Zone nicht). 
Dies bietet Schutz für gleichzeitige Zonenänderungen.
Dies kann mit dem Parameter *Überschreiben* unterdrückt werden, der die Zone unabhängig von gleichzeitigen Änderungen aktualisiert.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Object
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PrivateZone
Das zu setzende Zonenobjekt.

```yaml
Type: Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone
Parameter Sets: Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ResourceGroupName
Gibt den Namen der Ressourcengruppe an, die die zu aktualisierende Zone enthält.
Sie müssen auch den *Parameter ZoneName* angeben.
Alternativ können Sie die private DNS-Zone mit einem **DnsZone-Objekt** angeben, das entweder über die Pipeline oder den Parameter *Zone übergeben* wird.

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
Private DNS Zone ResourceID.

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Tag
Eine Hashtabelle, die Ressourcentags darstellt.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
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
Default value: False
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
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## EINGABEN

### System.String

### Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone

## AUSGABEN

### Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone

## NOTIZEN

## VERWANDTE LINKS

[Get-AzPrivateDnsZone](./Get-AzPrivateDnsZone.md)

[New-AzPrivateDnsZone](./New-AzPrivateDnsZone.md)

[Set-AzPrivateDnsZone](./Set-AzPrivateDnsZone.md)
