---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/remove-azprivatednsrecordconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsRecordConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsRecordConfig.md
ms.openlocfilehash: 9e5daaac0807f84da73d0701c82cf7542b5182fa
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93824491"
---
# Remove-AzPrivateDnsRecordConfig

## Synopsis
Entfernt einen privaten DNS-Eintrag aus einem lokalen Datensatzobjekt.

## Syntax

### A (Standard)
```
Remove-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Ipv4Address <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### AAAA
```
Remove-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Ipv6Address <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### MX
```
Remove-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Exchange <String> -Preference <UInt16>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### PTR
```
Remove-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Ptrdname <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### TXT
```
Remove-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Value <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SRV
```
Remove-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Priority <UInt16> -Target <String>
 -Port <UInt16> -Weight <UInt16> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### CNAME
```
Remove-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Cname <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Remove-AzPrivateDnsRecordConfig-Cmdlet entfernt einen privaten DNS-Eintrag (Domain Name System) aus einem Daten Satz Satz. Das Recordset-Objekt ist ein Offlineobjekt, und Änderungen daran ändern die privaten DNS-Antworten erst, nachdem Sie das Set-AzPrivateDnsRecordSet-Cmdlet ausgeführt haben, um die Änderung am Microsoft Azure private DNS-Dienst beizubehalten. Zum Entfernen eines Datensatzes müssen alle Felder für diesen Datensatztyp genau übereinstimmen. Sie können keine SOA-Einträge hinzufügen oder entfernen. SOA-Einträge werden automatisch erstellt, wenn eine private DNS-Zone erstellt und automatisch gelöscht wird, wenn die private DNS-Zone gelöscht wird. Sie können das Recordset-Objekt als Parameter oder mithilfe des Pipelineoperators an dieses Cmdlet übergeben.

## Beispiele

### Beispiel 1: Entfernen eines a-Eintrags aus einem Daten Satz Satz
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzPrivateDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 1.2.3.4
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzPrivateDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzPrivateDnsRecordConfig -Ipv4Address 1.2.3.4 | Set-AzPrivateDnsRecordSet

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/A/www
Name              : www
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : A
Records           : {}
Metadata          :
IsAutoRegistered  :
```

In diesem Beispiel wird ein A-Eintrag aus einem vorhandenen Daten Satz Satz entfernt. Wenn es sich um den einzigen Datensatz in der Datensatzgruppe handelt, handelt es sich bei dem Ergebnis um einen leeren Daten Satz Satz. Informationen zum vollständigen Entfernen eines Daten Satz Satzes finden Sie unter Remove-AzPrivateDnsRecordSet.

### Beispiel 2: Entfernen eines AAAA-Eintrags aus einem Daten Satz Satz
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzPrivateDnsRecordConfig -RecordSet $RecordSet -Ipv6Address 2001:DB80:4009:1803::1005
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzPrivateDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzPrivateDnsRecordConfig -Ipv6Address 2001:DB80:4009:1803::1005 | Set-AzPrivateDnsRecordSet

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/AAAA/www
Name              : www
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : AAAA
Records           : {}
Metadata          :
IsAutoRegistered  :
```

In diesem Beispiel wird ein AAAA-Eintrag aus einem vorhandenen Daten Satz Satz entfernt. Wenn es sich um den einzigen Datensatz in der Datensatzgruppe handelt, handelt es sich bei dem Ergebnis um einen leeren Daten Satz Satz. Informationen zum vollständigen Entfernen eines Daten Satz Satzes finden Sie unter Remove-AzPrivateDnsRecordSet.

### Beispiel 3: Entfernen eines CNAME-Eintrags aus einem Daten Satz Satz
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name "www" -RecordType CNAME -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzPrivateDnsRecordConfig -RecordSet $RecordSet -Cname contoso.com
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzPrivateDnsRecordSet -Name "www" -RecordType CNAME -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzPrivateDnsRecordConfig -Cname contoso.com | Set-AzPrivateDnsRecordSet

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/CNAME/www
Name              : www
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : CNAME
Records           : {}
Metadata          :
IsAutoRegistered  :
```

In diesem Beispiel wird ein CNAME-Eintrag aus einem vorhandenen Daten Satz Satz entfernt. Da ein CNAME-Eintragssatz höchstens einen Datensatz enthalten kann, ist das Ergebnis ein leerer Datensatz.

### Beispiel 4: Entfernen eines MX-Eintrags aus einem Daten Satz Satz
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name "@" -RecordType MX -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzPrivateDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 -RecordSet $RecordSet
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzPrivateDnsRecordSet -Name "@" -RecordType MX -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzPrivateDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 | Set-AzPrivateDnsRecordSet

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/MX/www
Name              : www
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : MX
Records           : {}
Metadata          :
IsAutoRegistered  :
```

In diesem Beispiel wird ein MX-Eintrag aus einem vorhandenen Daten Satz Satz entfernt. Der Datensatzname "@" steht für einen Datensatz, der in der Zone Apex festgesetzt wurde. Wenn dies der einzige Datensatz in der Datensatzgruppe ist, ist das Ergebnis eine leere Datensatzgruppe. Informationen zum vollständigen Entfernen eines Daten Satz Satzes finden Sie unter Remove-AzPrivateDnsRecordSet.

### Beispiel 5: Entfernen eines PTR-Eintrags aus einem Daten Satz Satz
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name "4" -RecordType PTR -ResourceGroupName "MyResourceGroup" -ZoneName 3.2.1.in-addr.arpa
PS C:\> Remove-AzPrivateDnsRecordConfig -Ptrdname www.contoso.com -RecordSet $RecordSet
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzPrivateDnsRecordSet -Name "4" -RecordType PTR -ResourceGroupName "MyResourceGroup" -ZoneName "3.2.1.in-addr.arpa" | Remove-AzPrivateDnsRecordConfig -Ptrdname www.contoso.com | Set-AzPrivateDnsRecordSet

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/3.2.1.in-addr.arpa/PTR/4
Name              : 4
ZoneName          : 3.2.1.in-addr.arpa
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : PTR
Records           : {}
Metadata          :
IsAutoRegistered  :
```

In diesem Beispiel wird ein PTR-Eintrag aus einem vorhandenen Daten Satz Satz entfernt. Wenn dies der einzige Datensatz in der Datensatzgruppe ist, ist das Ergebnis eine leere Datensatzgruppe. Informationen zum vollständigen Entfernen eines Daten Satz Satzes finden Sie unter Remove-AzPrivateDnsRecordSet.

### Beispiel 6: Entfernen eines SRV-Eintrags aus einem Daten Satz Satz
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzPrivateDnsRecordConfig -RecordSet $RecordSet -Priority 0 -Weight 5 -Port 8080 -Target target.example.com
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzPrivateDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzPrivateDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target target.example.com  | Set-AzPrivateDnsRecordSet

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/SRV/_sip._tcp
Name              : _sip._tcp
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : SRV
Records           : {}
Metadata          :
IsAutoRegistered  :
```

In diesem Beispiel wird ein SRV-Eintrag aus einem vorhandenen Daten Satz Satz entfernt. Wenn dies der einzige Datensatz in der Datensatzgruppe ist, ist das Ergebnis eine leere Datensatzgruppe. Informationen zum vollständigen Entfernen eines Daten Satz Satzes finden Sie unter Remove-AzPrivateDnsRecordSet.

### Beispiel 7: Entfernen eines txt-Eintrags aus einem Daten Satz Satz
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name "text" -RecordType TXT -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzPrivateDnsRecordConfig -RecordSet $RecordSet -Value "This is a TXT Record"
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzPrivateDnsRecordSet -Name "text" -RecordType TXT -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzPrivateDnsRecordConfig -Value "This is a TXT Record"  | Set-AzPrivateDnsRecordSet

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/TXT/text
Name              : text
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : TXT
Records           : {}
Metadata          :
IsAutoRegistered  :
```

In diesem Beispiel wird ein TXT-Eintrag aus einem vorhandenen Daten Satz Satz entfernt. Wenn dies der einzige Datensatz in der Datensatzgruppe ist, ist das Ergebnis eine leere Datensatzgruppe. Informationen zum vollständigen Entfernen eines Daten Satz Satzes finden Sie unter Remove-AzPrivateDnsRecordSet.

## Parameter

### -CNAME
Der kanonische Name des zu entfernenden CNAME-Eintrags.
Darf nicht relativ zum Namen der Zone sein.
Darf keinen Endpunkt haben

```yaml
Type: System.String
Parameter Sets: CNAME
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### -Exchange
Der e-Mail-Exchange-Host des zu entfernenden MX-Eintrags.
Darf nicht relativ zum Namen der Zone sein.
Darf keinen Endpunkt haben

```yaml
Type: System.String
Parameter Sets: MX
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Ipv4Address
Die IPv4-Adresse des zu entfernenden A-Eintrags.

```yaml
Type: System.String
Parameter Sets: A
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IPv6
Die IPv6-Adresse des zu entfernenden AAAA-Eintrags.

```yaml
Type: System.String
Parameter Sets: AAAA
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Port
Die Portnummer des zu entfernenden SRV-Eintrags.

```yaml
Type: System.UInt16
Parameter Sets: SRV
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Präferenz
Der Einstellungswert des zu entfernenden MX-Eintrags.

```yaml
Type: System.UInt16
Parameter Sets: MX
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Priorität
Der Prioritätswert des zu entfernenden SRV-Eintrags.

```yaml
Type: System.UInt16
Parameter Sets: SRV
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Ptrdname
Der Ziel Host des zu entfernenden PTR-Eintrags.
Darf nicht relativ zum Namen der Zone sein.
Darf keinen Endpunkt haben

```yaml
Type: System.String
Parameter Sets: PTR
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Recordset
Die Datensatzgruppe, aus der der Datensatz entfernt werden soll.

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

### -Target
Der Ziel Host des zu entfernenden SRV-Eintrags.
Darf nicht relativ zum Namen der Zone sein.
Darf keinen Endpunkt haben

```yaml
Type: System.String
Parameter Sets: SRV
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Wert
Der Textwert des zu entfernenden txt-Eintrags.

```yaml
Type: System.String
Parameter Sets: TXT
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Gewicht
Der Gewichtungswert des zu entfernenden SRV-Eintrags.

```yaml
Type: System.UInt16
Parameter Sets: SRV
Aliases:

Required: True
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
