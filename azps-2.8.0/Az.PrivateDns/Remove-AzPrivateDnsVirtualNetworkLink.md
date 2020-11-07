---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
ms.assetid: A8E230A0-5057-40BC-81CD-6D397A503A84
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/remove-azprivatednsvirtualnetworklink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsVirtualNetworkLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsVirtualNetworkLink.md
ms.openlocfilehash: 21e02077e7c2644c622a3f290a82fa26d7d6fc64
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93824487"
---
# Remove-AzPrivateDnsVirtualNetworkLink

## Synopsis
Entfernt einen virtuellen Netzwerk Link aus einer Ressourcengruppe.

## Syntax

### Felder (Standard)
```
Remove-AzPrivateDnsVirtualNetworkLink -ResourceGroupName <String> -ZoneName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Objekt
```
Remove-AzPrivateDnsVirtualNetworkLink -InputObject <PSPrivateDnsVirtualNetworkLink> [-Overwrite] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ResourceId
```
Remove-AzPrivateDnsVirtualNetworkLink -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Beschreibung
Mit dem Cmdlet **Remove-AzPrivateDnsVirtualNetworkLink** wird dauerhaft ein privater DNS-Link (Domain Name System) aus einer angegebenen Ressourcengruppe gelöscht.
Sie können ein **PSPrivateDnsVirtualNetworkLink** -Objekt mithilfe des *Link* -Parameters oder mithilfe des Pipelineoperators übergeben, oder Sie können auch die Parameter *Name* *zonename* und *ResourceGroupName* angeben.
Sie können den Parameter Confirm und $ConfirmPreference Windows PowerShell-Variable verwenden, um zu steuern, ob das Cmdlet Sie zur Bestätigung auffordert.
Wenn Sie die Verknüpfung mit einem **PSPrivateDnsVirtualNetworkLink** -Objekt angeben (das über den Pipeline-oder *Link* -Parameter übergeben wird), wird der Link nicht gelöscht, wenn er in Azure private DNS geändert wurde, nachdem das lokale **PSPrivateDnsVirtualNetworkLink** -Objekt abgerufen wurde. Dadurch wird der Schutz für gleichzeitige Zonenänderungen bereitgestellt. Dies kann mithilfe des *overwrite* -Parameters unterdrückt werden, wodurch die Zone unabhängig von gleichzeitigen Änderungen gelöscht wird.

## Beispiele

### Beispiel 1: Entfernen eines Links
```
PS C:\>Remove-AzPrivateDnsVirtualNetworkLink -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" -Name "mylink"
```

Mit diesem Befehl wird der Link MyLink mit Zone myzone.com aus der Ressourcengruppe myresourcegroup entfernt.

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

### -Inputobject
Das zu entfernende virtuelle Netzwerk Link-Objekt.

```yaml
Type: Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsVirtualNetworkLink
Parameter Sets: Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Gibt den Namen des Links an, der gelöscht werden soll.
Außerdem müssen Sie den Parameter *ResourceGroupName* und *zonename* angeben.
Sie können den Link auch über den *Link* -Parameter angeben.

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
Wenn Sie die Zone mithilfe eines **PSPrivateDnsVirtualNetworkLink** -Objekts angeben (das über den Pipeline-oder *Link* -Parameter übergeben wird), wird die Zone nicht gelöscht, wenn Sie in Azure DNS geändert wurde, nachdem das lokale **PSPrivateDnsVirtualNetworkLink** -Objekt abgerufen wurde.
Dadurch wird der Schutz für gleichzeitige Zonenänderungen bereitgestellt.
Dies kann mithilfe des *overwrite* -Parameters unterdrückt werden, wodurch die Zone unabhängig von gleichzeitigen Änderungen gelöscht wird.

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

### -PassThru
Wird verwendet, um das Ergebnis (boolescher Wert) des Vorgangs "virtuellen Netzwerk löschen" weiter unten in der Pipeline zu übergeben.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Gibt den Namen der Ressourcengruppe an, die den zu entfernenden Link enthält.
Außerdem müssen Sie den Parameter *zonename* und *Name* angeben.
Alternativ können Sie die DNS-Zone mithilfe eines **PSPrivateDnsVirtualNetworkLink** -Objekts angeben, das entweder über die Pipeline oder den *Link* -Parameter übergeben wird.

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

### -Resourcen-Nr
Gibt die Arm-Ressourcen-ID des Links an.

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

### -ZoneName
Gibt den Namen der privaten DNS-Zone an, der der Link zugeordnet ist.
Außerdem müssen Sie den Parameter *ResourceGroupName* und *Name* angeben.
Sie können den Link auch über den *Link* -Parameter angeben.

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

### -Bestätigen
Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.

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
Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.
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
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### Microsoft. Azure. Commands. PrivateDns. Models. PSPrivateDnsVirtualNetworkLink

### System. String

## Ausgaben

### System. Boolean

## Notizen

## Verwandte Links

[Get-AzPrivateDnsVirtualNetworkLink](./Get-AzPrivateDnsVirtualNetworkLink.md)

[Neu – AzPrivateDnsVirtualNetworkLink](./New-AzPrivateDnsVirtualNetworkLink.md)

[Satz-AzPrivateDnsVirtualNetworkLink](./Set-AzPrivateDnsVirtualNetworkLink.md)
