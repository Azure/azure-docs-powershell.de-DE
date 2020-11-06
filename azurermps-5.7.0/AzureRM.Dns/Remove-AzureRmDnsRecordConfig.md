---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
Module Name: AzureRM.Dns
ms.assetid: D1A2326C-CD41-45A6-B37A-FC6176193B01
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.dns/remove-azurermdnsrecordconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Remove-AzureRmDnsRecordConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Remove-AzureRmDnsRecordConfig.md
ms.openlocfilehash: 1e0a7de22b459f5d87c4a79bb91ef4c36f88ad77
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499865"
---
# Remove-AzureRmDnsRecordConfig

## Synopsis
Entfernt einen DNS-Eintrag aus einem lokalen Datensatzobjekt.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

### Eine
```
Remove-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Ipv4Address <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### AAAA
```
Remove-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Ipv6Address <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### NS
```
Remove-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Nsdname <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### MX
```
Remove-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Exchange <String> -Preference <UInt16>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### PTR
```
Remove-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Ptrdname <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### TXT
```
Remove-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Value <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SRV
```
Remove-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Priority <UInt16> -Target <String> -Port <UInt16>
 -Weight <UInt16> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### CNAME
```
Remove-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Cname <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### CAA
```
Remove-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -CaaFlags <Byte> -CaaTag <String> -CaaValue <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Mit dem Cmdlet **Remove-AzureRmDnsRecordConfig** wird ein DNS-Eintrag (Domain Name System) aus einem Daten Satz Satz entfernt.
Das **Recordset** -Objekt ist ein Offlineobjekt, und Änderungen daran ändern die DNS-Antworten erst, nachdem Sie das Set-AzureRmDnsRecordSet-Cmdlet ausgeführt haben, um die Änderung am Microsoft Azure-DNS-Dienst beizubehalten.

Zum Entfernen eines Datensatzes müssen alle Felder für diesen Datensatztyp genau übereinstimmen.
Sie können keine SOA-Einträge hinzufügen oder entfernen.
SOA-Einträge werden automatisch erstellt, wenn eine DNS-Zone erstellt und automatisch gelöscht wird, wenn die DNS-Zone gelöscht wird.

Sie können das **Recordset** -Objekt als Parameter oder mithilfe des Pipelineoperators an dieses Cmdlet übergeben.

## Beispiele

### Beispiel 1: Entfernen eines a-Eintrags aus einem Daten Satz Satz
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name "www" -RecordType A -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzureRmDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 1.2.3.4
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzureRmDnsRecordSet -Name "www" -RecordType A -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzureRmDnsRecordConfig -Ipv4Address 1.2.3.4 | Set-AzureRmDnsRecordSet
```

In diesem Beispiel wird ein A-Eintrag aus einem vorhandenen Daten Satz Satz entfernt.
Wenn es sich um den einzigen Datensatz in der Datensatzgruppe handelt, handelt es sich bei dem Ergebnis um einen leeren Daten Satz Satz.
Informationen zum vollständigen Entfernen eines Daten Satz Satzes finden Sie unter Remove-AzureRmDnsRecordSet.

### Beispiel 2: Entfernen eines AAAA-Eintrags aus einem Daten Satz Satz
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name "www" -RecordType AAAA -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzureRmDnsRecordConfig -RecordSet $RecordSet -Ipv6Address 2001:DB80:4009:1803::1005
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzureRmDnsRecordSet -Name "www" -RecordType AAAA -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzureRmDnsRecordConfig -Ipv6Address 2001:DB80:4009:1803::1005 | Set-AzureRmDnsRecordSet
```

In diesem Beispiel wird ein AAAA-Eintrag aus einem vorhandenen Daten Satz Satz entfernt.
Wenn es sich um den einzigen Datensatz in der Datensatzgruppe handelt, handelt es sich bei dem Ergebnis um einen leeren Daten Satz Satz.
Informationen zum vollständigen Entfernen eines Daten Satz Satzes finden Sie unter Remove-AzureRmDnsRecordSet.

### Beispiel 3: Entfernen eines CNAME-Eintrags aus einem Daten Satz Satz
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name "www" -RecordType CNAME -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzureRmDnsRecordConfig -RecordSet $RecordSet -Cname contoso.com
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzureRmDnsRecordSet -Name "www" -RecordType CNAME -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzureRmDnsRecordConfig -Cname contoso.com | Set-AzureRmDnsRecordSet
```

In diesem Beispiel wird ein CNAME-Eintrag aus einem vorhandenen Daten Satz Satz entfernt.
Da ein CNAME-Eintragssatz höchstens einen Datensatz enthalten kann, ist das Ergebnis ein leerer Datensatz.

### Beispiel 4: Entfernen eines MX-Eintrags aus einem Daten Satz Satz
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name "@" -RecordType MX -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzureRmDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 -RecordSet $RecordSet
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzureRmDnsRecordSet -Name "@" -RecordType MX -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzureRmDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 | Set-AzureRmDnsRecordSet
```

In diesem Beispiel wird ein MX-Eintrag aus einem vorhandenen Daten Satz Satz entfernt.
Der Datensatzname "@" steht für einen Datensatz, der in der Zone Apex festgesetzt wurde.
Wenn dies der einzige Datensatz in der Datensatzgruppe ist, ist das Ergebnis eine leere Datensatzgruppe.
Informationen zum vollständigen Entfernen eines Daten Satz Satzes finden Sie unter Remove-AzureRmDnsRecordSet.

### Beispiel 5: Entfernen eines NS-Eintrags aus einem Daten Satz Satz
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name "abc" -RecordType NS -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzureRmDnsRecordConfig -Nsdname ns1.myzone.com -RecordSet $RecordSet
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzureRmDnsRecordSet -Name "abc" -RecordType NS -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzureRmDnsRecordConfig -Nsdname "ns1.myzone.com" | Set-AzureRmDnsRecordSet
```

In diesem Beispiel wird ein NS-Eintrag aus einem vorhandenen Daten Satz Satz entfernt.
Wenn dies der einzige Datensatz in der Datensatzgruppe ist, ist das Ergebnis eine leere Datensatzgruppe.
Informationen zum vollständigen Entfernen eines Daten Satz Satzes finden Sie unter Remove-AzureRmDnsRecordSet.

### Beispiel 6: Entfernen eines PTR-Eintrags aus einem Daten Satz Satz
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name "4" -RecordType PTR -ResouceGroupName "MyResourceGroup" -ZoneName 3.2.1.in-addr.arpa
PS C:\> Remove-AzureRmDnsRecordConfig -Ptrdname www.contoso.com -RecordSet $RecordSet
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzureRmDnsRecordSet -Name "4" -RecordType PTR -ResouceGroupName "MyResourceGroup" -ZoneName "3.2.1.in-addr.arpa" | Remove-AzureRmDnsRecordConfig -Ptrdname www.contoso.com | Set-AzureRmDnsRecordSet
```

In diesem Beispiel wird ein PTR-Eintrag aus einem vorhandenen Daten Satz Satz entfernt.
Wenn dies der einzige Datensatz in der Datensatzgruppe ist, ist das Ergebnis eine leere Datensatzgruppe.
Informationen zum vollständigen Entfernen eines Daten Satz Satzes finden Sie unter Remove-AzureRmDnsRecordSet.

### Beispiel 7: Entfernen eines SRV-Eintrags aus einem Daten Satz Satz
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzureRmDnsRecordConfig -RecordSet $RecordSet -Priority 0 -Weight 5 -Port 8080 -Target target.example.com
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzureRmDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzureRmDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target target.example.com  | Set-AzureRmDnsRecordSet
```

In diesem Beispiel wird ein SRV-Eintrag aus einem vorhandenen Daten Satz Satz entfernt.
Wenn dies der einzige Datensatz in der Datensatzgruppe ist, ist das Ergebnis eine leere Datensatzgruppe.
Informationen zum vollständigen Entfernen eines Daten Satz Satzes finden Sie unter Remove-AzureRmDnsRecordSet.

### Beispiel 8: Entfernen eines txt-Eintrags aus einem Daten Satz Satz
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name "text" -RecordType TXT -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzureRmDnsRecordConfig -RecordSet $RecordSet -Value "This is a TXT Record"
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzureRmDnsRecordSet -Name "text" -RecordType TXT -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzureRmDnsRecordConfig -Value "This is a TXT Record"  | Set-AzureRmDnsRecordSet
```

In diesem Beispiel wird ein TXT-Eintrag aus einem vorhandenen Daten Satz Satz entfernt.
Wenn dies der einzige Datensatz in der Datensatzgruppe ist, ist das Ergebnis eine leere Datensatzgruppe.
Informationen zum vollständigen Entfernen eines Daten Satz Satzes finden Sie unter Remove-AzureRmDnsRecordSet.

## Parameter

### -CaaFlags
Die Flags für den hinzuzufügenden CAA-Eintrag. Muss eine Zahl zwischen 0 und 255 sein.

```yaml
Type: Byte
Parameter Sets: Caa
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -CaaTag
Das Tag-Feld des hinzuzufügenden CAA-Eintrags.

```yaml
Type: String
Parameter Sets: Caa
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -CaaValue
Das Feld "Wert" für den hinzuzufügenden CAA-Eintrag.

```yaml
Type: String
Parameter Sets: Caa
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -CNAME
Gibt den Domänennamen für einen CNAME-Eintrag (Kanonischer Name) an.

```yaml
Type: String
Parameter Sets: CNAME
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

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

### -Exchange
Gibt den e-Mail-Exchange-Servernamen für einen MX-Eintrag (Mail Exchange) an.

```yaml
Type: String
Parameter Sets: MX
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Ipv4Address
Gibt eine IPv4-Adresse für einen A-Eintrag an.

```yaml
Type: String
Parameter Sets: A
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -IPv6
Gibt eine IPv6-Adresse für einen AAAA-Eintrag an.

```yaml
Type: String
Parameter Sets: AAAA
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Nsdname
Gibt den Namenserver für einen Namenserver (NS)-Eintrag an.

```yaml
Type: String
Parameter Sets: NS
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Port
Gibt den Port für einen Dienst (SRV)-Eintrag an.

```yaml
Type: UInt16
Parameter Sets: SRV
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Präferenz
Gibt die Einstellung für einen MX-Eintrag an.

```yaml
Type: UInt16
Parameter Sets: MX
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Priorität
Gibt die Priorität für einen SRV-Eintrag an.

```yaml
Type: UInt16
Parameter Sets: SRV
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Ptrdname
Gibt den Zieldomänen Namen eines Zeiger (PTR)-Eintrags an.

```yaml
Type: String
Parameter Sets: PTR
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Recordset
Gibt das **Recordset** -Objekt an, das den zu entfernenden Datensatz enthält.

```yaml
Type: DnsRecordSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Target
Gibt das Ziel für einen SRV-Eintrag an.

```yaml
Type: String
Parameter Sets: SRV
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Wert
Gibt den Wert für einen TXT-Eintrag an.

```yaml
Type: String
Parameter Sets: TXT
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Gewicht
Gibt die Gewichtung für einen SRV-Eintrag an.

```yaml
Type: UInt16
Parameter Sets: SRV
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### Microsoft. Azure. Commands. DNS. DnsRecordSet
Sie können ein **DnsRecordSet** -Objekt an dieses Cmdlet übergeben.
Hierbei handelt es sich um eine Offlinedarstellung des Daten Satz Satzes, und es werden keine DNS-Antworten geändert, bis Sie den Satz-AzureRmDnsRecordSet ausgeführt haben.

## Ausgaben

### Microsoft. Azure. Commands. DNS. DnsRecordSet
Dieses Cmdlet gibt das geänderte **Recordset** -Objekt zurück.

## Notizen

## Verwandte Links

[Add-AzureRmDnsRecordConfig](./Add-AzureRmDnsRecordConfig.md)

[Get-AzureRmDnsRecordSet](./Get-AzureRmDnsRecordSet.md)

[Satz-AzureRmDnsRecordSet](./Set-AzureRmDnsRecordSet.md)
