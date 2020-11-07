---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/Set-AzPrivateDnsRecordSet
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Set-AzPrivateDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Set-AzPrivateDnsRecordSet.md
ms.openlocfilehash: 7c4f76b9731e82bd134be7ae38461a7d74e31e6a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93824479"
---
# Set-AzPrivateDnsRecordSet

## Synopsis
Aktualisiert/legt einen Daten Satz Satz in einer privaten DNS-Zone fest.

## Syntax

```
Set-AzPrivateDnsRecordSet -RecordSet <PSPrivateDnsRecordSet> [-Overwrite]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Beschreibung
Das Set-AzPrivateDnsRecordSet-Cmdlet aktualisiert einen Daten Satz Satz im Azure private DNS-Dienst von einem lokalen Recordset-Objekt. Sie können ein Recordset-Objekt als Parameter oder mithilfe des Pipelineoperators übergeben. Sie können den Parameter Confirm und $ConfirmPreference Windows PowerShell-Variable verwenden, um zu steuern, ob das Cmdlet Sie zur Bestätigung auffordert. Der Daten Satz Satz wird nicht aktualisiert, wenn er in Azure private DNS geändert wurde, seit das lokale Recordset-Objekt abgerufen wurde. Dadurch wird der Schutz für gleichzeitige Änderungen bereitgestellt. Sie können dieses Verhalten mithilfe des overwrite-Parameters unterdrücken, wodurch der Daten Satz Satz unabhängig von gleichzeitigen Änderungen aktualisiert wird.

## Beispiele

### Beispiel 1: Aktualisieren eines Daten Satz Satzes
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -ResourceGroupName MyResourceGroup -ZoneName myzone.com -Name www -RecordType A
PS C:\> Add-AzPrivateDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 172.16.0.0
PS C:\> Add-AzPrivateDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 172.31.255.255
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

# These cmdlets can also be piped:

PS C:\> Get-AzPrivateDnsRecordSet -ResourceGroupName MyResourceGroup -ZoneName myzone.com -Name www -RecordType A | Add-AzPrivateDnsRecordConfig -Ipv4Address 172.16.0.0 | Add-AzPrivateDnsRecordConfig -Ipv4Address 172.31.255.255 | Set-AzPrivateDnsRecordSet

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Microsoft.Netwo
                    rk/privateDnsZones/myzone.com/A/www
Name              : www
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : A
Records           : {1.2.3.4, 172.16.0.0, 172.31.255.255}
Metadata          :
IsAutoRegistered  :
```

Der erste Befehl verwendet das Get-AzPrivateDnsRecordSet-Cmdlet, um den angegebenen Daten Satz Satz abzurufen, und speichert ihn dann in der Variablen $Recordset. Der zweite und der dritte Befehl sind Offlinevorgänge, um dem Daten Satz Satz zwei A-Datensätze hinzuzufügen. Der endgültige Befehl verwendet das Set-AzPrivateDnsRecordSet-Cmdlet, um das Update zu übernehmen.

### Beispiel 2: Aktualisieren eines SOA-Eintrags
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name "@" -RecordType SOA -Zone $Zone
PS C:\> $RecordSet.Records[0].Email = "admin.myzone.com"
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/SOA/@
Name              : @
ZoneName          : myzone.com
ResourceGroupName : Myresourcegroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : SOA
Records           : {[internal.cloudapp.net,admin.myzone.com,3600,300,2419200,300]}
Metadata          :
IsAutoRegistered  :
```

Der erste Befehl verwendet das Get-AzPrivateDnsRecordSet-Cmdlet, um den angegebenen Daten Satz Satz abzurufen, und speichert ihn dann in der Variablen $Recordset. Der zweite Befehl aktualisiert den angegebenen SOA-Eintrag in $Recordset. Der endgültige Befehl verwendet das Set-AzPrivateDnsRecordSet-Cmdlet, um das Update in $Recordset zu propagieren.

## Parameter

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.

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
Verwenden Sie das ETag-Feld des Recordset-Parameters nicht für Prüfungen mit vollständigen Parallelität.

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
Die Datensatzgruppe, in der der Datensatz hinzugefügt werden soll.

```yaml
Type: Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet
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
Default value: None
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
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### Microsoft. Azure. Commands. PrivateDns. Models. PSPrivateDnsRecordSet

## Ausgaben

### Microsoft. Azure. Commands. PrivateDns. Models. PSPrivateDnsRecordSet

## Notizen

## Verwandte Links
