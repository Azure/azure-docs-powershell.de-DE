---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
Module Name: AzureRM.Dns
ms.assetid: E37ADC54-A37B-41BF-BE94-9E4052C234BB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Set-AzureRmDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Set-AzureRmDnsZone.md
ms.openlocfilehash: 9d4e0e376e611e1373d30ab6b3aeafb51f363c31
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664268"
---
# Set-AzureRmDnsZone

## Synopsis
Aktualisiert die Eigenschaften einer DNS-Zone.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

### Felder
```
Set-AzureRmDnsZone -Name <String> -ResourceGroupName <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Objekt
```
Set-AzureRmDnsZone -Zone <DnsZone> [-Overwrite] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Satz-AzureRmDnsZone** " aktualisiert die angegebene DNS-Zone im Azure DNS-Dienst.
Mit diesem Cmdlet werden die Daten Satz Sätze in der Zone nicht aktualisiert.

Sie können ein **dnsZone** -Objekt als Parameter oder mithilfe des Pipelineoperators übergeben, oder Sie können auch die Parameter *zonename* und *ResourceGroupName* angeben.

Sie können den Parameter *Confirm* und $ConfirmPreference Windows PowerShell-Variable verwenden, um zu steuern, ob das Cmdlet Sie zur Bestätigung auffordert.

Wenn Sie eine DNS-Zone als Objekt (mithilfe des Zone-Objekts oder über die Pipeline) übergeben, wird Sie nicht aktualisiert, wenn Sie in Azure DNS geändert wurde, seit das lokale dnsZone-Objekt abgerufen wurde. Dadurch wird der Schutz für gleichzeitige Änderungen bereitgestellt. Sie können dieses Verhalten mit dem Parameter *overwrite* unterdrücken, wodurch die Zone unabhängig von gleichzeitigen Änderungen aktualisiert wird.

## Beispiele

### Beispiel 1: Aktualisieren einer DNS-Zone
```
PS C:\>$Zone = Get-AzureRmDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> $Zone.Tags = @(@{"Name"="Dept"; "Value"="Electrical"})
PS C:\> Set-AzureRmDnsZone -Zone $Zone
```

Der erste Befehl ruft die Zone mit dem Namen MyZone.com aus der angegebenen Ressourcengruppe ab und speichert Sie dann in der $Zone Variablen.

Mit dem zweiten Befehl werden die Tags für $Zone aktualisiert.

Der endgültige Befehl übernimmt die Änderung.

### Beispiel 2: Aktualisieren von Tags für eine Zone
```
PS C:\>Set-AzureRmDNSZone -ResourceGroupName "MyResourceGroup" -Name "myzone.com" -Tag @(@{"Name"="Dept"; "Value"="Electrical"})
```

Dieser Befehl aktualisiert die Tags für die Zone mit dem Namen MyZone.com, ohne die Zone zuvor explizit zu erhalten.

## Parameter

### -Name
Gibt den Namen der zu aktualisierende DNS-Zone an.

```yaml
Type: System.String
Parameter Sets: Fields
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Overwrite
Wenn Sie eine DNS-Zone als Objekt (mithilfe des Zone-Objekts oder über die Pipeline) übergeben, wird Sie nicht aktualisiert, wenn Sie in Azure DNS geändert wurde, seit das lokale dnsZone-Objekt abgerufen wurde. Dadurch wird der Schutz für gleichzeitige Änderungen bereitgestellt. Sie können dieses Verhalten mit dem Parameter *overwrite* unterdrücken, wodurch die Zone unabhängig von gleichzeitigen Änderungen aktualisiert wird.

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

### -ResourceGroupName
Gibt den Namen der Ressourcengruppe an, die die zu aktualisierende Zone enthält.
Außerdem müssen Sie den Parameter zonename angeben.

Alternativ können Sie die Zone mithilfe eines dnsZone-Objekts mit dem *Zone* -Parameter oder der Pipeline angeben.

```yaml
Type: System.String
Parameter Sets: Fields
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Tag
Schlüssel-Wert-Paare in Form einer Hashtabelle Zum Beispiel:

@ {KEY0 = "value0"; key1 = $NULL; key2 = "Value2"}

```yaml
Type: System.Collections.Hashtable
Parameter Sets: Fields
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Zone
Gibt die zu aktualisierende DNS-Zone an.

Alternativ können Sie die Zone mithilfe der Parameter *zonename* und *ResourceGroupName* angeben.

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
Zeigt, was passiert, wenn das Cmdlet ausgeführt wird. Das Cmdlet wird nicht ausgeführt. Zeigt, was passiert, wenn das Cmdlet ausgeführt wird. Das Cmdlet wird nicht ausgeführt.

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

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### Microsoft. Azure. Commands. DNS. dnsZone
Sie können ein dnsZone-Objekt an dieses Cmdlet übergeben.

## Ausgaben

### Microsoft. Azure. Commands. DNS. dnsZone
Dieses Cmdlet gibt ein dnsZone-Objekt zurück, das die aktualisierte DNS-Zone mit einem neuen ETag darstellt.

## Notizen
Sie können den Parameter *Confirm* verwenden, um zu steuern, ob dieses Cmdlet Sie zur Bestätigung auffordert.
Standardmäßig werden Sie vom Cmdlet zur Bestätigung aufgefordert, wenn die $ConfirmPreference Windows PowerShell-Variable einen Wert von Mittel oder niedriger aufweist.

Wenn Sie *bestätigen* oder *bestätigen: $true* angeben, werden Sie von diesem Cmdlet zur Bestätigung aufgefordert, bevor es ausgeführt wird.
Wenn Sie *Confirm: $false* angeben, werden Sie vom Cmdlet nicht zur Bestätigung aufgefordert.

## Verwandte Links

[Get-AzureRmDnsZone](./Get-AzureRmDnsZone.md)

[Neu – AzureRmDnsZone](./New-AzureRmDnsZone.md)

[Remove-AzureRmDnsZone](./Remove-AzureRmDnsZone.md)
