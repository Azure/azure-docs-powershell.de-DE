---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/remove-azprivatednszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsZone.md
ms.openlocfilehash: d381af8de23b5eb781882f10670e6ba69afbc571
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100160332"
---
# Remove-AzPrivateDnsZone

## SYNOPSIS
Entfernt eine private DNS-Zone aus einer Ressourcengruppe.

## SYNTAX

### Felder (Standard)
```
Remove-AzPrivateDnsZone -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Objekt
```
Remove-AzPrivateDnsZone -PrivateZone <PSPrivateDnsZone> [-Overwrite] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ResourceId
```
Remove-AzPrivateDnsZone -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## BESCHREIBUNG
Das **Cmdlet "Remove-AzPrivateDnsZone"** löscht eine Private Domain Name System (DNS)-Zone dauerhaft aus einer angegebenen Ressourcengruppe.
Alle in der Zone enthaltenen Datensatzsätze werden ebenfalls gelöscht.
Sie können ein **PrivateDnsZone-Objekt** mit dem *Parameter "PrivateZone"* oder mit dem Pipelineoperator übergeben, oder Sie können die Parameter *"Name"* und *"ResourceGroupName"* angeben.
Sie können den Parameter "Bestätigen" und $ConfirmPreference Windows PowerShell, um zu steuern, ob sie vom Cmdlet zur Bestätigung aufgefordert werden.
Wenn Sie die Zone mit einem **PrivateDnsZone-Objekt** angeben (das über die Pipeline oder den *Parameter "Zone"* übergeben wird), wird die Zone nicht gelöscht, wenn sie in Azure DNS geändert wurde, da das lokale **"PrivateDnsZone"-Objekt** abgerufen wurde (nur Vorgänge direkt für die DNS-Zonenressourcen zählen als Änderungen, Vorgänge für Datensatzsätze innerhalb der Zone nicht).
Dies bietet Schutz für Änderungen gleichzeitiger Zonen.
Dies kann mithilfe des Parameters *"Overwrite"* unterdrückt werden, der die Zone unabhängig von gleichzeitigen Änderungen löscht.

## BEISPIELE

### Beispiel 1: Entfernen einer privaten Zone
```
PS C:\>Remove-AzPrivateDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
```

Mit diesem Befehl wird die Zone namens "myzone.com" aus der Ressourcengruppe "MyResourceGroup" entfernt.

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

### -Name
Gibt den Namen der privaten DNS-Zone an, die von diesem Cmdlet entfernt wird.
Sie müssen auch den Parameter *"ResourceGroupName"* angeben.
Alternativ können Sie die DNS-Zone mit dem Parameter *"Zone"* angeben.

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
Wenn Sie die Zone mit einem **PrivateDnsZone-Objekt** angeben (das über die Pipeline oder den *Parameter "Zone"* übergeben wird), wird die Zone nicht gelöscht, wenn sie in Azure DNS geändert wurde, da das lokale **"PrivateDnsZone"-Objekt** abgerufen wurde (nur Vorgänge direkt für die DNS-Zonenressourcen zählen als Änderungen, Vorgänge für Datensatzsätze innerhalb der Zone nicht).
Dies bietet Schutz für Änderungen gleichzeitiger Zonen.
Dies kann mithilfe des Parameters *"Overwrite"* unterdrückt werden, der die Zone unabhängig von gleichzeitigen Änderungen löscht.

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
Wird verwendet, um das Ergebnis (boolesch) des Vorgangs weiter unten in der Pipeline zu löschen.

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

### -PrivateZone
Das zu löschende private Zonenobjekt.

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
Gibt den Namen der Ressourcengruppe an, die die zu entfernende Zone enthält.
Sie müssen auch den *Parameter "ZoneName"* angeben.
Alternativ können Sie die DNS-Zone mit einem **PrivateDnsZone-Objekt** angeben, das entweder über die Pipeline oder den Parameter *"Zone" übergeben* wird.

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

### -Confirm
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

### -Waswenn
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
Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## EINGABEN

### Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone

### System.String

## AUSGABEN

### System.Boolean

## HINWEISE

## LINKS ZU VERWANDTEN THEMEN

[Get-AzPrivateDnsZone](./Get-AzPrivateDnsZone.md)

[New-AzPrivateDnsZone](./New-AzPrivateDnsZone.md)

[Set-AzPrivateDnsZone](./Set-AzPrivateDnsZone.md)
