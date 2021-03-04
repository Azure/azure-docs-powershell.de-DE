---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: E37ADC54-A37B-41BF-BE94-9E4052C234BB
online version: https://docs.microsoft.com/powershell/module/az.dns/set-azdnszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Set-AzDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Set-AzDnsZone.md
ms.openlocfilehash: d1b5fb606262b680d4e83f9c8e0a9ea166070ed4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101934987"
---
# Set-AzDnsZone

## SYNOPSIS
Aktualisiert die Eigenschaften einer DNS-Zone.

## SYNTAX

### Felder (Standard)
```
Set-AzDnsZone -Name <String> -ResourceGroupName <String> [-Tag <Hashtable>]
 [-RegistrationVirtualNetworkId <System.Collections.Generic.List`1[System.String]>]
 [-ResolutionVirtualNetworkId <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### FieldsObjects
```
Set-AzDnsZone -Name <String> -ResourceGroupName <String> [-Tag <Hashtable>]
 [-RegistrationVirtualNetwork <System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]>]
 [-ResolutionVirtualNetwork <System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Objekt
```
Set-AzDnsZone -Zone <DnsZone> [-Overwrite] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## BESCHREIBUNG
Das **Cmdlet Set-AzDnsZone** aktualisiert die angegebene DNS-Zone im Azure DNS-Dienst.
Dieses Cmdlet aktualisiert die Datensatzsätze in der Zone nicht.
Sie können ein **DnsZone-Objekt** als Parameter oder mithilfe des Pipelineoperators übergeben oder alternativ die *Parameter ZoneName* und *ResourceGroupName* angeben.
Sie können den Parameter *Bestätigen* und die $ConfirmPreference Windows PowerShell verwenden, um zu steuern, ob das Cmdlet Sie zur Bestätigung aufgefordert.
Wenn Sie eine DNS-Zone als -Objekt übergeben (mithilfe des Zone-Objekts oder über die Pipeline), wird sie nicht aktualisiert, wenn sie in Azure DNS seit dem Abrufen des lokalen DnsZone-Objekts geändert wurde. Dies bietet Schutz für gleichzeitige Änderungen. Sie können dieses Verhalten mit dem Parameter *Überschreiben* unterdrücken, der die Zone unabhängig von gleichzeitigen Änderungen aktualisiert.

## BEISPIELE

### Beispiel 1: Aktualisieren einer DNS-Zone
```
PS C:\>$Zone = Get-AzDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> $Zone.Tags = @(@{"Name"="Dept"; "Value"="Electrical"})
PS C:\> Set-AzDnsZone -Zone $Zone
```

Der erste Befehl ruft die Zone mit dem Namen myzone.com aus der angegebenen Ressourcengruppe ab und speichert sie dann in der $Zone Variablen.
Der zweite Befehl aktualisiert die Tags für $Zone.
Der letzte Befehl übergeht die Änderung.

### Beispiel 2: Aktualisieren von Tags für eine Zone
```
PS C:\>Set-AzDNSZone -ResourceGroupName "MyResourceGroup" -Name "myzone.com" -Tag @(@{"Name"="Dept"; "Value"="Electrical"})
```

Mit diesem Befehl werden die Tags für die Zone namens myzone.com aktualisiert, ohne zuerst die Zone explizit zu erhalten.

### Beispiel 3: Zuordnen einer privaten Zone zu einem virtuellen Netzwerk durch Angeben der ID
```
PS C:\>$vnet = Get-AzVirtualNetwork -ResourceGroupName "MyResourceGroup" -Name "myvnet"
PS C:\>Set-AzDNSZone -ResourceGroupName "MyResourceGroup" -Name "myprivatezone.com" -RegistrationVirtualNetworkId @($vnet.Id)
```

Dieser Befehl ordnet die Private DNS-Zone myprivatezone.com dem virtuellen Netzwerk myvnet als Registrierungsnetzwerk zu, indem die ID angegeben wird.

### Beispiel 4: Zuordnen einer privaten Zone zu einem virtuellen Netzwerk durch Angeben des Netzwerkobjekts
```
PS C:\>$vnet = Get-AzVirtualNetwork -ResourceGroupName "MyResourceGroup" -Name "myvnet"
PS C:\>Set-AzDNSZone -ResourceGroupName "MyResourceGroup" -Name "myprivatezone.com" -RegistrationVirtualNetwork @($vnet)
```

Dieser Befehl ordnet die private DNS-Zone myprivatezone.com dem virtuellen Netzwerk myvnet als Registrierungsnetzwerk zu, indem das virtuelle Netzwerkobjekt, das durch die Variable $vnet dargestellt wird, an das cmdlet Set-AzDnsZone übergeben.

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
Gibt den Namen der zu aktualisierenden DNS-Zone an.

```yaml
Type: System.String
Parameter Sets: Fields, FieldsObjects
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Overwrite
Wenn Sie eine DNS-Zone als -Objekt übergeben (mithilfe des Zone-Objekts oder über die Pipeline), wird sie nicht aktualisiert, wenn sie in Azure DNS seit dem Abrufen des lokalen DnsZone-Objekts geändert wurde. Dies bietet Schutz für gleichzeitige Änderungen. Sie können dieses Verhalten mit dem Parameter *Überschreiben* unterdrücken, der die Zone unabhängig von gleichzeitigen Änderungen aktualisiert.

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

### -RegistrationVirtualNetwork
Die Liste der virtuellen Netzwerke, in der Hostnamen für virtuelle Computer registriert werden, enthält Einträge in dieser DNS-Zone, die nur für private Zonen verfügbar sind.

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]
Parameter Sets: FieldsObjects
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RegistrationVirtualNetworkId
Die Liste der virtuellen Netzwerk-IDs, die Hostnamen für virtuelle Computer in dieser DNS-Zone registrieren, ist nur für private Zonen verfügbar.

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: Fields
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResolutionVirtualNetwork
Die Liste der virtuellen Netzwerke, die Datensätze in dieser DNS-Zone auflösen können, die nur für private Zonen verfügbar sind.

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]
Parameter Sets: FieldsObjects
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResolutionVirtualNetworkId
Die Liste der virtuellen Netzwerk-IDs, die Datensätze in dieser DNS-Zone auflösen können, die nur für private Zonen verfügbar sind.

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: Fields
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Gibt den Namen der Ressourcengruppe an, die die zu aktualisierende Zone enthält.
Sie müssen auch den Parameter ZoneName angeben.
Alternativ können Sie die Zone mithilfe eines DnsZone-Objekts mit dem *Parameter Zone* oder der Pipeline angeben.

```yaml
Type: System.String
Parameter Sets: Fields, FieldsObjects
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Tag
Schlüssel-Wert-Paare in Form einer Hashtabelle. Beispiel: @{key0="value0";key1=$null;key2="value2"}

```yaml
Type: System.Collections.Hashtable
Parameter Sets: Fields, FieldsObjects
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Zone
Gibt die zu aktualisierende DNS-Zone an.
Alternativ können Sie die Zone mithilfe der *Parameter ZoneName* und *ResourceGroupName* angeben.

```yaml
Type: Microsoft.Azure.Commands.Dns.DnsZone
Parameter Sets: Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
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
Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird. Das Cmdlet wird nicht ausgeführt. Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird. Das Cmdlet wird nicht ausgeführt.

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

### System.Collections.Hashtable

### System.Collections.Generic.List'1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]

### System.Collections.Generic.List'1[[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference, Microsoft.Azure.PowerShell.Clients.Network, Version=1.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]

### Microsoft.Azure.Commands.Dns.DnsZone

## AUSGABEN

### Microsoft.Azure.Commands.Dns.DnsZone

## NOTIZEN
Sie können den Parameter *Bestätigen* verwenden, um zu steuern, ob Sie von diesem Cmdlet zur Bestätigung aufgefordert werden.
Standardmäßig werden Sie vom Cmdlet zur Bestätigung aufgefordert, wenn die $ConfirmPreference Windows PowerShell den Wert Mittel oder niedriger hat.
Wenn Sie *Bestätigen* oder *Bestätigen:$True,* werden Sie von diesem Cmdlet zur Bestätigung aufgefordert, bevor es ausgeführt wird.
Wenn Sie *Confirm:$False* angeben, werden Sie vom Cmdlet nicht zur Bestätigung aufgefordert.

## VERWANDTE LINKS

[Get-AzDnsZone](./Get-AzDnsZone.md)

[New-AzDnsZone](./New-AzDnsZone.md)

[Remove-AzDnsZone](./Remove-AzDnsZone.md)
