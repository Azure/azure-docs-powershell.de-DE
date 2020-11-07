---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/remove-azprivatednszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsZone.md
ms.openlocfilehash: d54dac2689fd751663ebf0046288c4d4ceeae928
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93824484"
---
# Remove-AzPrivateDnsZone

## Synopsis
Entfernt eine private DNS-Zone aus einer Ressourcengruppe.

## Syntax

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

## Beschreibung
Das Cmdlet **Remove-AzPrivateDnsZone** löscht endgültig eine Private Domain Name System (DNS)-Zone aus einer angegebenen Ressourcengruppe.
Alle in der Zone enthaltenen Daten Satz Sätze werden ebenfalls gelöscht.
Sie können ein **PrivateDnsZone** -Objekt mithilfe des *PrivateZone* -Parameters oder mithilfe des Pipelineoperators übergeben, oder Sie können auch den *Namen* und die *ResourceGroupName* -Parameter angeben.
Sie können den Parameter Confirm und $ConfirmPreference Windows PowerShell-Variable verwenden, um zu steuern, ob das Cmdlet Sie zur Bestätigung auffordert.
Wenn Sie die Zone mithilfe eines **PrivateDnsZone** -Objekts angeben (das über den Pipeline-oder *Zone* -Parameter übergeben wird), wird die Zone nicht gelöscht, wenn Sie in Azure DNS geändert wurde, da das lokale **PrivateDnsZone** -Objekt abgerufen wurde (nur Vorgänge, die direkt in der DNS-Zonen Ressource ausgeführt werden, als Änderungen, Operationen für Daten Satz Sätze innerhalb der Zone nicht).
Dadurch wird der Schutz für gleichzeitige Zonenänderungen bereitgestellt.
Dies kann mithilfe des *overwrite* -Parameters unterdrückt werden, wodurch die Zone unabhängig von gleichzeitigen Änderungen gelöscht wird.

## Beispiele

### Beispiel 1: Entfernen einer privaten Zone
```
PS C:\>Remove-AzPrivateDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
```

Mit diesem Befehl wird die Zone mit dem Namen MyZone.com aus der Ressourcengruppe myresourcegroup entfernt.

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
Gibt den Namen der privaten DNS-Zone an, die vom Cmdlet entfernt wird.
Sie müssen auch den *ResourceGroupName* -Parameter angeben.
Alternativ können Sie die DNS-Zone mithilfe des *Zone* -Parameters angeben.

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
Wenn Sie die Zone mithilfe eines **PrivateDnsZone** -Objekts angeben (das über den Pipeline-oder *Zone* -Parameter übergeben wird), wird die Zone nicht gelöscht, wenn Sie in Azure DNS geändert wurde, da das lokale **PrivateDnsZone** -Objekt abgerufen wurde (nur Vorgänge, die direkt in der DNS-Zonen Ressource ausgeführt werden, als Änderungen, Operationen für Daten Satz Sätze innerhalb der Zone nicht).
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
Wird verwendet, um das Ergebnis (boolescher Wert) des Vorgangs Delete private Zone weiter unten in der Pipeline zu übergeben.

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
Das Private Zone-Objekt, das gelöscht werden soll.

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
Außerdem müssen Sie den Parameter *zonename* angeben.
Alternativ können Sie die DNS-Zone mithilfe eines **PrivateDnsZone** -Objekts angeben, das entweder über die Pipeline oder den *Zone* -Parameter übergeben wird.

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
Private DNS Zone-Quell Code.

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

### Microsoft. Azure. Commands. PrivateDns. Models. PSPrivateDnsZone

### System. String

## Ausgaben

### System. Boolean

## Notizen

## Verwandte Links

[Get-AzPrivateDnsZone](./Get-AzPrivateDnsZone.md)

[Neu – AzPrivateDnsZone](./New-AzPrivateDnsZone.md)

[Satz-AzPrivateDnsZone](./Set-AzPrivateDnsZone.md)
