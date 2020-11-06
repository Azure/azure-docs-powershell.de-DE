---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
Module Name: AzureRM.Dns
ms.assetid: A8E230A0-5057-40BC-81CD-6D397A503A84
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.dns/remove-azurermdnszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Remove-AzureRmDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Remove-AzureRmDnsZone.md
ms.openlocfilehash: ac3f65ed82f9b04eb49e26a8cb03a3dcd8c9bc34
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502601"
---
# Remove-AzureRmDnsZone

## Synopsis
Entfernt eine DNS-Zone aus einer Ressourcengruppe.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

### Felder
```
Remove-AzureRmDnsZone -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Objekt
```
Remove-AzureRmDnsZone -Zone <DnsZone> [-Overwrite] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **Remove-AzureRmDnsZone** löscht endgültig eine DNS-Zone (Domain Name System) aus einer angegebenen Ressourcengruppe.
Alle in der Zone enthaltenen Daten Satz Sätze werden ebenfalls gelöscht.

Sie können ein **dnsZone** -Objekt mithilfe des *Name* -Parameters oder mithilfe des Pipelineoperators übergeben, oder Sie können auch die Parameter *zonename* und *ResourceGroupName* angeben.

Sie können den Parameter Confirm und $ConfirmPreference Windows PowerShell-Variable verwenden, um zu steuern, ob das Cmdlet Sie zur Bestätigung auffordert.

Wenn Sie die Zone mithilfe eines **dnsZone** -Objekts angeben (das über den Pipeline-oder *Zone* -Parameter übergeben wird), wird die Zone nicht gelöscht, wenn Sie in Azure DNS geändert wurde, da das lokale **dnsZone** -Objekt abgerufen wurde (nur Vorgänge, die direkt in der DNS-Zonen Ressource ausgeführt werden, als Änderungen, Operationen für Daten Satz Sätze innerhalb der Zone nicht).
Dadurch wird der Schutz für gleichzeitige Zonenänderungen bereitgestellt.
Dies kann mithilfe des *overwrite* -Parameters unterdrückt werden, wodurch die Zone unabhängig von gleichzeitigen Änderungen gelöscht wird.

## Beispiele

### Beispiel 1: Entfernen einer Zone
```
PS C:\>Remove-AzureRmDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
```

Mit diesem Befehl wird die Zone mit dem Namen MyZone.com aus der Ressourcengruppe myresourcegroup entfernt.

## Parameter

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
Dieser Parameter ist für dieses Cmdlet veraltet.
Sie wird in einer zukünftigen Version entfernt.

Verwenden Sie den Parameter *Confirm* , um zu steuern, ob Sie von diesem Cmdlet zur Bestätigung aufgefordert werden.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Gibt den Namen der DNS-Zone an, die von diesem Cmdlet entfernt wird.
Sie müssen auch den *ResourceGroupName* -Parameter angeben.

Alternativ können Sie die DNS-Zone mithilfe des *Zone* -Parameters angeben.

```yaml
Type: String
Parameter Sets: Fields
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Overwrite
Wenn Sie die Zone mithilfe eines **dnsZone** -Objekts angeben (das über den Pipeline-oder *Zone* -Parameter übergeben wird), wird die Zone nicht gelöscht, wenn Sie in Azure DNS geändert wurde, da das lokale **dnsZone** -Objekt abgerufen wurde (nur Vorgänge, die direkt in der DNS-Zonen Ressource ausgeführt werden, als Änderungen, Operationen für Daten Satz Sätze innerhalb der Zone nicht).
Dadurch wird der Schutz für gleichzeitige Zonenänderungen bereitgestellt.

Dies kann mithilfe des *overwrite* -Parameters unterdrückt werden, wodurch die Zone unabhängig von gleichzeitigen Änderungen gelöscht wird.

```yaml
Type: SwitchParameter
Parameter Sets: Object
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru
passthru

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Gibt den Namen der Ressourcengruppe an, die die zu entfernende Zone enthält.
Außerdem müssen Sie den Parameter *zonename* angeben.

Alternativ können Sie die DNS-Zone mithilfe eines **dnsZone** -Objekts angeben, das entweder über die Pipeline oder den *Zone* -Parameter übergeben wird.

```yaml
Type: String
Parameter Sets: Fields
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Zone
Gibt die zu löschende DNS-Zone an.
Das übergebene **dnsZone** -Objekt kann auch über die Pipeline übergeben werden.

Alternativ können Sie die zu löschende DNS-Zone mithilfe der Parameter *zonename* und *ResourceGroupName* angeben.

```yaml
Type: DnsZone
Parameter Sets: Object
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Bestätigen
Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.

```yaml
Type: SwitchParameter
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
Type: SwitchParameter
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

### Microsoft. Azure. Commands. DNS. dnsZone
Sie können ein **dnsZone** -Objekt an dieses Cmdlet übergeben.

## Ausgaben

### Keine
Dieses Cmdlet generiert keine Ausgabe.

## Notizen
Aufgrund der potenziell großen Auswirkung des Löschens einer DNS-Zone fordert dieses Cmdlet standardmäßig eine Bestätigung an, wenn die $ConfirmPreference Windows PowerShell-Variable einen anderen Wert als None aufweist.

Wenn Sie *bestätigen* oder *bestätigen: $true* angeben, werden Sie von diesem Cmdlet zur Bestätigung aufgefordert, bevor es ausgeführt wird.
Wenn Sie *Confirm: $false* angeben, werden Sie vom Cmdlet nicht zur Bestätigung aufgefordert. 

## Verwandte Links

[Get-AzureRmDnsZone](./Get-AzureRmDnsZone.md)

[Neu – AzureRmDnsZone](./New-AzureRmDnsZone.md)

[Satz-AzureRmDnsZone](./Set-AzureRmDnsZone.md)
