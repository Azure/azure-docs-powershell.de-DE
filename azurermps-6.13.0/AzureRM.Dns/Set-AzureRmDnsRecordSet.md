---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
Module Name: AzureRM.Dns
ms.assetid: 99E6C4DD-11AF-4DC0-848B-39811240BE06
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.dns/set-azurermdnsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Set-AzureRmDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Set-AzureRmDnsRecordSet.md
ms.openlocfilehash: d0a7451db664d80240250984fcc1c0f8e1aaefe9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499526"
---
# Set-AzureRmDnsRecordSet

## Synopsis
Aktualisiert einen DNS-Eintragssatz.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

```
Set-AzureRmDnsRecordSet -RecordSet <DnsRecordSet> [-Overwrite] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Satz-AzureRmDnsRecordSet** " aktualisiert einen Daten Satz Satz im Azure DNS-Dienst von einem lokalen **Recordset** -Objekt.
Sie können ein **Recordset** -Objekt als Parameter oder mithilfe des Pipelineoperators übergeben.
Sie können den Parameter *Confirm* und $ConfirmPreference Windows PowerShell-Variable verwenden, um zu steuern, ob das Cmdlet Sie zur Bestätigung auffordert.
Der Daten Satz Satz wird nicht aktualisiert, wenn er in Azure DNS geändert wurde, seit das lokale **Recordset** -Objekt abgerufen wurde.
Dadurch wird der Schutz für gleichzeitige Änderungen bereitgestellt.
Sie können dieses Verhalten mithilfe des *overwrite* -Parameters unterdrücken, wodurch der Daten Satz Satz unabhängig von gleichzeitigen Änderungen aktualisiert wird.

## Beispiele

### Beispiel 1: Aktualisieren eines Daten Satz Satzes
```
PS C:\>$RecordSet = Get-AzureRmDnsRecordSet -ResourceGroupName MyResourceGroup -ZoneName myzone.com -Name www -RecordType A
PS C:\> Add-AzureRmDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 172.16.0.0
PS C:\> Add-AzureRmDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 172.31.255.255
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# These cmdlets can also be piped:

PS C:\> Get-AzureRmDnsRecordSet -ResourceGroupName MyResourceGroup -ZoneName myzone.com -Name www -RecordType A | Add-AzureRmDnsRecordConfig -Ipv4Address 172.16.0.0 | Add-AzureRmDnsRecordConfig -Ipv4Address 172.31.255.255 | Set-AzureRmDnsRecordSet
```

Der erste Befehl verwendet das Get-AzureRmDnsRecordSet-Cmdlet, um den angegebenen Daten Satz Satz abzurufen, und speichert ihn dann in der Variablen $Recordset.
Der zweite und der dritte Befehl sind Offlinevorgänge, um dem Daten Satz Satz zwei A-Datensätze hinzuzufügen.
Der endgültige Befehl verwendet das Cmdlet " **festlegen-AzureRmDnsRecordSet** ", um das Update zu übernehmen.

### Beispiel 2: Aktualisieren eines SOA-Eintrags
```
PS C:\>$RecordSet = Get-AzureRmDnsRecordSet -Name "@" -RecordType SOA -Zone $Zone
PS C:\> $RecordSet.Records[0].Email = "admin.myzone.com"
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet
```

Der erste Befehl verwendet das Cmdlet " **Get-AzureRmDnsRecordset** ", um den angegebenen Daten Satz Satz abzurufen, und speichert ihn dann in der $Recordset-Variablen.
Der zweite Befehl aktualisiert den angegebenen SOA-Eintrag in $Recordset.
Der endgültige Befehl verwendet das Cmdlet " **AzureRmDnsRecordSet** ", um das Update in $Recordset weiterzugeben.

## Parameter

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement

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

### -Overwrite
Gibt an, dass der Daten Satz Satz unabhängig von gleichzeitigen Änderungen aktualisiert werden soll.
Der Daten Satz Satz wird nicht aktualisiert, wenn er in Azure DNS geändert wurde, seit das lokale **Recordset** -Objekt abgerufen wurde.
Dadurch wird der Schutz für gleichzeitige Änderungen bereitgestellt.
Um dieses Verhalten zu unterdrücken, können Sie den Parameter *overwrite* verwenden, der dazu führt, dass der Daten Satz Satz unabhängig von gleichzeitigen Änderungen aktualisiert wird.

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

### -Recordset
Gibt das zu aktualisierende **Recordset** an.

```yaml
Type: Microsoft.Azure.Commands.Dns.DnsRecordSet
Parameter Sets: (All)
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

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### Microsoft. Azure. Commands. DNS. DnsRecordSet
Parameter: Recordset (ByValue)

## Ausgaben

### Microsoft. Azure. Commands. DNS. DnsRecordSet

## Notizen
Sie können den Parameter *Confirm* verwenden, um zu steuern, ob dieses Cmdlet Sie zur Bestätigung auffordert.
Standardmäßig werden Sie vom Cmdlet zur Bestätigung aufgefordert, wenn die $ConfirmPreference Windows PowerShell-Variable einen Wert von Mittel oder niedriger aufweist.
Wenn Sie *bestätigen* oder *bestätigen: $true* angeben, werden Sie von diesem Cmdlet zur Bestätigung aufgefordert, bevor es ausgeführt wird.
Wenn Sie *Confirm: $false* angeben, werden Sie vom Cmdlet nicht zur Bestätigung aufgefordert. 

## Verwandte Links

[Get-AzureRmDnsRecordSet](./Get-AzureRmDnsRecordSet.md)

[Neu – AzureRmDnsRecordSet](./New-AzureRmDnsRecordSet.md)

[Remove-AzureRmDnsRecordSet](./Remove-AzureRmDnsRecordSet.md)
