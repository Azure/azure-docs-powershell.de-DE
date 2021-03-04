---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: 99E6C4DD-11AF-4DC0-848B-39811240BE06
online version: https://docs.microsoft.com/powershell/module/az.dns/set-azdnsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Set-AzDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Set-AzDnsRecordSet.md
ms.openlocfilehash: 1ab2d10800648d04c9e8dcb2cf8907d426bd2d48
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101935011"
---
# Set-AzDnsRecordSet

## SYNOPSIS
Aktualisiert einen DNS-Eintragssatz.

## SYNTAX

```
Set-AzDnsRecordSet -RecordSet <DnsRecordSet> [-Overwrite] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## BESCHREIBUNG
Das **Set-AzDnsRecordSet-Cmdlet** aktualisiert einen Datensatzsatz im Azure DNS-Dienst von einem lokalen **RecordSet-Objekt.**
Sie können ein **RecordSet-Objekt** als Parameter oder mithilfe des Pipelineoperators übergeben.
Sie können den Parameter *Bestätigen* und die $ConfirmPreference Windows PowerShell verwenden, um zu steuern, ob das Cmdlet Sie zur Bestätigung aufgefordert.
Der Datensatzsatz wird nicht aktualisiert, wenn er seit dem Abrufen des lokalen **RecordSet-Objekts** in Azure DNS geändert wurde.
Dies bietet Schutz für gleichzeitige Änderungen.
Sie können dieses Verhalten mit dem Parameter *Überschreiben* unterdrücken, der den Datensatzsatz unabhängig von gleichzeitigen Änderungen aktualisiert.

## BEISPIELE

### Beispiel 1: Aktualisieren eines Datensatzsatzs
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -ResourceGroupName MyResourceGroup -ZoneName myzone.com -Name www -RecordType A
PS C:\> Add-AzDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 172.16.0.0
PS C:\> Add-AzDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 172.31.255.255
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# These cmdlets can also be piped:

PS C:\> Get-AzDnsRecordSet -ResourceGroupName MyResourceGroup -ZoneName myzone.com -Name www -RecordType A | Add-AzDnsRecordConfig -Ipv4Address 172.16.0.0 | Add-AzDnsRecordConfig -Ipv4Address 172.31.255.255 | Set-AzDnsRecordSet
```

Der erste Befehl verwendet das Get-AzDnsRecordSet-Cmdlet, um den angegebenen Datensatzsatz zu erhalten, und speichert ihn dann in der $RecordSet Variablen.
Der zweite und dritte Befehl sind off-line-Vorgänge, um dem Datensatzsatz zwei A-Datensätze hinzuzufügen.
Der letzte Befehl verwendet das **Cmdlet Set-AzDnsRecordSet,** um das Update zu commiten.

### Beispiel 2: Aktualisieren eines SOA-Eintrags
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -Name "@" -RecordType SOA -Zone $Zone
PS C:\> $RecordSet.Records[0].Email = "admin.myzone.com"
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet
```

Der erste Befehl verwendet das **Get-AzDnsRecordset-Cmdlet,** um den angegebenen Datensatzsatz zu erhalten, und speichert ihn dann in der $RecordSet Variablen.
Der zweite Befehl aktualisiert den angegebenen SOA-Eintrag in $RecordSet.
Der letzte Befehl verwendet das **Cmdlet Set-AzDnsRecordSet,** um das Update in $RecordSet.

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

### -Overwrite
Gibt an, den Datensatzsatz unabhängig von gleichzeitigen Änderungen zu aktualisieren.
Der Datensatzsatz wird nicht aktualisiert, wenn er seit dem Abrufen des lokalen **RecordSet-Objekts** in Azure DNS geändert wurde.
Dies bietet Schutz für gleichzeitige Änderungen.
Um dieses Verhalten zu unterdrücken, können Sie den Parameter *Überschreiben* verwenden, wodurch der Datensatzsatz unabhängig von gleichzeitigen Änderungen aktualisiert wird.

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

### -RecordSet
Gibt das **zu aktualisierende RecordSet** an.

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

### Microsoft.Azure.Commands.Dns.DnsRecordSet

## AUSGABEN

### Microsoft.Azure.Commands.Dns.DnsRecordSet

## NOTIZEN
Sie können den Parameter *Bestätigen* verwenden, um zu steuern, ob Sie von diesem Cmdlet zur Bestätigung aufgefordert werden.
Standardmäßig werden Sie vom Cmdlet zur Bestätigung aufgefordert, wenn die $ConfirmPreference Windows PowerShell den Wert Mittel oder niedriger hat.
Wenn Sie *Bestätigen* oder *Bestätigen:$True,* werden Sie von diesem Cmdlet zur Bestätigung aufgefordert, bevor es ausgeführt wird.
Wenn Sie *Confirm:$False* angeben, werden Sie vom Cmdlet nicht zur Bestätigung aufgefordert. 

## VERWANDTE LINKS

[Get-AzDnsRecordSet](./Get-AzDnsRecordSet.md)

[New-AzDnsRecordSet](./New-AzDnsRecordSet.md)

[Remove-AzDnsRecordSet](./Remove-AzDnsRecordSet.md)
