---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: B78F3E8B-C7D2-458C-AB23-06F584FE97E0
online version: https://docs.microsoft.com/powershell/module/az.dns/new-azdnszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/New-AzDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/New-AzDnsZone.md
ms.openlocfilehash: 40f1b40bbb5546e1d38b9c2916ea635aab80c144
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101935040"
---
# New-AzDnsZone

## SYNOPSIS
Erstellt eine neue DNS-Zone.

## SYNTAX

### Ids (Standard)
```
New-AzDnsZone -Name <String> -ResourceGroupName <String> [-ZoneType <ZoneType>] [-ParentZoneId <String>]
 [-Tag <Hashtable>] [-RegistrationVirtualNetworkId <System.Collections.Generic.List`1[System.String]>]
 [-ResolutionVirtualNetworkId <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Namen
```
New-AzDnsZone -Name <String> -ResourceGroupName <String> [-ZoneType <ZoneType>] [-ParentZoneName <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Objekte
```
New-AzDnsZone -Name <String> -ResourceGroupName <String> [-ZoneType <ZoneType>] [-ParentZone <DnsZone>]
 [-Tag <Hashtable>]
 [-RegistrationVirtualNetwork <System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]>]
 [-ResolutionVirtualNetwork <System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## BESCHREIBUNG
Das **Cmdlet New-AzDnsZone** erstellt eine neue Zone des Domain Name System (DNS) in der angegebenen Ressourcengruppe. Sie müssen einen eindeutigen DNS-Zonennamen für den *Parameter Name* angeben, oder das Cmdlet gibt einen Fehler zurück. Nachdem die Zone erstellt wurde, verwenden Sie das cmdlet New-AzDnsRecordSet, um Datensatzsätze in der Zone zu erstellen.
Sie können den Parameter *Bestätigen* und die $ConfirmPreference Windows PowerShell verwenden, um zu steuern, ob das Cmdlet Sie zur Bestätigung aufgefordert.

## BEISPIELE

### Beispiel 1: Erstellen einer DNS-Zone
```
PS C:\>$Zone = New-AzDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
```

Mit diesem Befehl wird eine neue DNS-Zone myzone.com in der angegebenen Ressourcengruppe erstellt und dann in der $Zone gespeichert.

### Beispiel 2: Erstellen einer privaten DNS-Zone durch Angeben virtueller Netzwerk-IDs
```
PS C:\>$ResVirtualNetworkId = "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/testresgroup/providers/Microsoft.Network/virtualNetworks/resvnet"
PS C:\>$Zone = New-AzDnsZone -Name "myprivatezone.com" -ResourceGroupName "MyResourceGroup" -ZoneType Private -ResolutionVirtualNetworkId @($ResVirtualNetworkId)
```

Mit diesem Befehl wird eine neue private DNS-Zone mit dem Namen myprivatezone.com in der angegebenen Ressourcengruppe mit einem zugeordneten virtuellen Auflösungsnetzwerk erstellt (mit der zugehörigen ID) und dann in der $Zone gespeichert.

### Beispiel 3: Erstellen einer privaten DNS-Zone durch Angeben virtueller Netzwerkobjekte
```
PS C:\>$ResVirtualNetwork = Get-AzVirtualNetwork -Name "resvnet" -ResourceGroupName "testresgroup"
PS C:\>$Zone = New-AzDnsZone -Name "myprivatezone.com" -ResourceGroupName "MyResourceGroup" -ZoneType Private -ResolutionVirtualNetwork @($ResVirtualNetwork)
```

Mit diesem Befehl wird eine neue private DNS-Zone mit dem Namen myprivatezone.com in der angegebenen Ressourcengruppe mit einem zugeordneten virtuellen Auflösungsnetzwerk (auf das von der $ResVirtualNetwork-Variable verwiesen wird) erstellt und dann in der variablen $Zone gespeichert.

### Beispiel 4: Erstellen einer DNS-Zone mit Delegierung durch Angeben des übergeordneten Zonennamens
```
PS C:\>$Zone = New-AzDnsZone -Name "mychild.zone.com" -ResourceGroupName "MyResourceGroup" -ParentZoneName "zone.com"
```

Mit diesem Befehl wird eine neue untergeordnete DNS-Zone mychild.zone.com in der angegebenen Ressourcengruppe erstellt und in der $Zone gespeichert.
Außerdem wird die Delegierung in der übergeordneten DNS-Zone zone.com, die sich in derselben Abonnement- und Ressourcengruppe wie die untergeordnete Zone befindet.

### Beispiel 5: Erstellen einer DNS-Zone mit Delegierung durch Angeben der übergeordneten Zonen-ID
```
PS C:\>$Zone = New-AzDnsZone -Name "mychild.zone.com" -ResourceGroupName "MyResourceGroup" -ParentZoneId "/subscriptions/**67e2/resourceGroups/other-rg/providers/Microsoft.Network/dnszones/zone.com"
```

Mit diesem Befehl wird eine neue untergeordnete DNS-Zone mychild.zone.com in der angegebenen Ressourcengruppe erstellt und in der $Zone gespeichert.
Außerdem wird die Delegierung in der übergeordneten DNS-Zone mit dem Namen zone.com in der Ressourcengruppe andere rg hinzu, vorausgesetzt, das Abonnement ist identisch mit der der erstellten untergeordneten Zone.

### Beispiel 6: Erstellen einer DNS-Zone mit Delegierung durch Angeben des übergeordneten Zonenobjekts
```
PS C:\>$PZone = New-AzDnsZone -Name "zone.com" -ResourceGroupName "MyResourceGroup" 
PS C:\>$Zone = New-AzDnsZone -Name "mychild.zone.com" -ResourceGroupName "MyResourceGroup" -ParentZone @($PZone)
```

Mit diesem Befehl wird eine neue untergeordnete DNS-Zone mychild.zone.com in der angegebenen Ressourcengruppe erstellt und in der $Zone gespeichert.
Außerdem wird eine Delegierung in der übergeordneten DNS-Zone zone.com die im ParentZone-Objekt übergeben wird.

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
Gibt den Namen der zu erstellenden DNS-Zone an.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ParentZone
Der vollständige Name der übergeordneten Zone, die delegierung hinzugefügt werden soll (ohne einen endenden Punkt).

```yaml
Type: Microsoft.Azure.Commands.Dns.DnsZone
Parameter Sets: Objects
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ParentZoneId
Die Ressourcen-ID der übergeordneten Zone, die delegierung hinzugefügt werden soll (ohne einen endenden Punkt).

```yaml
Type: System.String
Parameter Sets: Ids
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ParentZoneName
Der vollständige Name der übergeordneten Zone, die delegierung hinzugefügt werden soll (ohne einen endenden Punkt).

```yaml
Type: System.String
Parameter Sets: Names
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RegistrationVirtualNetwork
Die Liste der virtuellen Netzwerke, in der Hostnamen für virtuelle Computer registriert werden, enthält Einträge in dieser DNS-Zone, die nur für private Zonen verfügbar sind.

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]
Parameter Sets: Objects
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
Parameter Sets: Ids
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
Parameter Sets: Objects
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
Parameter Sets: Ids
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Gibt die Ressourcengruppe an, in der die Zone erstellt werden soll.

```yaml
Type: System.String
Parameter Sets: (All)
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
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ZoneType
Der Typ der Zone( Öffentlich oder Privat). Zonen ohne Typ oder mit einem öffentlichen Typ werden auf dem öffentlichen DNS-Dienstebenen zur Verwendung in der DNS-Hierarchie verfügbar gemacht. Zonen mit einem Typ "Privat" sind nur mit der Gruppe der zugeordneten virtuellen Netzwerke sichtbar (dieses Feature befindet sich in der Vorschau). Diese Eigenschaft kann für eine Zone nicht geändert werden.

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Dns.Models.ZoneType]
Parameter Sets: (All)
Aliases:
Accepted values: Public, Private

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

### System.Nullable'1[[Microsoft.Azure.Management.Dns.Models.ZoneType, Microsoft.Azure.Management.Dns, Version=3.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]

### System.Collections.Hashtable

### System.Collections.Generic.List'1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]

### System.Collections.Generic.List'1[[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference, Microsoft.Azure.PowerShell.Clients.Network, Version=1.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]

## AUSGABEN

### Microsoft.Azure.Commands.Dns.DnsZone

## NOTIZEN
Sie können den Parameter *Bestätigen* verwenden, um zu steuern, ob Sie von diesem Cmdlet zur Bestätigung aufgefordert werden.
Standardmäßig werden Sie vom Cmdlet zur Bestätigung aufgefordert, wenn die $ConfirmPreference Windows PowerShell den Wert Mittel oder niedriger hat.
Wenn Sie *Bestätigen* oder *Bestätigen:$True,* werden Sie von diesem Cmdlet zur Bestätigung aufgefordert, bevor es ausgeführt wird.
Wenn Sie *Confirm:$False* angeben, werden Sie vom Cmdlet nicht zur Bestätigung aufgefordert.

## VERWANDTE LINKS

[Get-AzDnsZone](./Get-AzDnsZone.md)

[New-AzDnsRecordSet](./New-AzDnsRecordSet.md)

[Remove-AzDnsZone](./Remove-AzDnsZone.md)
