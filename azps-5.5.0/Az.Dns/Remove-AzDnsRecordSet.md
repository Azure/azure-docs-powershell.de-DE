---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: 505562A4-30BC-44E7-94EF-579763B8D794
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/remove-azdnsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Remove-AzDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Remove-AzDnsRecordSet.md
ms.openlocfilehash: f5d7075322bb2b5a4b61635400664f0e909f126d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100147980"
---
# Remove-AzDnsRecordSet

## SYNOPSIS
Löscht einen Datensatzsatz.

## SYNTAX

### Felder
```
Remove-AzDnsRecordSet -Name <String> -RecordType <RecordType> -ZoneName <String> -ResourceGroupName <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Gemischt
```
Remove-AzDnsRecordSet -Name <String> -RecordType <RecordType> -Zone <DnsZone> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Objekt
```
Remove-AzDnsRecordSet -RecordSet <DnsRecordSet> [-Overwrite] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## BESCHREIBUNG
Das **Cmdlet "Remove-AzDnsRecordSet"** löscht den angegebenen Datensatzsatz aus der angegebenen Zone.
Sie können keine SOA- oder Namenservereinträge (Name Server, NS) löschen, die automatisch an der Zonenspitze erstellt werden.
Sie können ein **"RecordSet"-Objekt** mithilfe des Pipelineoperators oder als Parameter an dieses Cmdlet übergeben.
Zum Identifizieren eines Datensatzes nach Name und Typ ohne Verwendung eines **"RecordSet"-Objekts** müssen Sie die Zone als **"DnsZone"-Objekt** mit dem Pipelineoperator oder als Parameter an dieses Cmdlet übergeben. Alternativ können Sie auch die Parameter *"ZoneName"* und *"ResourceGroupName"* angeben.
Sie können den Parameter "Bestätigen" und $ConfirmPreference Windows PowerShell, um zu steuern, ob sie vom Cmdlet zur Bestätigung aufgefordert werden.
Wenn Sie den Datensatzsatz mithilfe eines **"RecordSet"-Objekts** angeben, wird der Datensatzsatz nicht gelöscht, wenn er seit dem Abrufen des lokalen **"RecordSet"-Objekts** in Azure DNS geändert wurde.
Dies bietet Schutz für gleichzeitige Änderungen.
Sie können dies unterdrücken, indem Sie den Parameter *"Overwrite"* verwenden, der den Datensatzsatz unabhängig von gleichzeitigen Änderungen löscht.

## BEISPIELE

### Beispiel 1: Entfernen eines Datensatzes
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "www" -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordSet -RecordSet $RecordSet
```

Der erste Befehl ruft den angegebenen Datensatzsatz ab und speichert ihn dann in der $RecordSet Variable. Der zweite Befehl entfernt den Datensatzsatz in $RecordSet.

### Beispiel 2: Entfernen eines Datensatzes und Unterdrücken aller Bestätigungen
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "www" -ZoneName "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> Remove-AzDnsRecordSet -RecordSet $RecordSet -Confirm:$False -Overwrite

# Alternatively, the record set can be removed as follows.  In this case,
# because the record set is specified by name rather than by object, the
# Overwrite parameter is not applicable.

PS C:\> Remove-AzDnsRecordSet -Name "www" -ZoneName "myzone.com" -ResourceGroupName "MyResourceGroup" -Confirm:$False
```

Der erste Befehl ruft den angegebenen Datensatzsatz ab.
Mit dem zweiten Befehl wird der Datensatzsatz gelöscht, auch wenn er sich in der Zwischenzeit geändert hat.
Bestätigungsaufforderungen werden unterdrückt.

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
Gibt den Namen des zu entfernenden **Datensatzes** an.
Wenn Sie den Eintrag nach Name angeben, muss die DNS-Zone entweder mit dem Parameter *"Zone"* oder mit den Parametern *"ZoneName"* und *"ResourceGroupName" angegeben* werden.
Alternativ kann der Datensatzsatz mithilfe eines **RecordSet-Objekts** angegeben werden, das mit dem *Parameter "RecordSet" übergeben* wird.

```yaml
Type: System.String
Parameter Sets: Fields, Mixed
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Overwrite
Wenn Sie den Datensatzsatz mithilfe eines **"RecordSet"-Objekts** angeben, wird der Datensatzsatz nicht gelöscht, wenn er seit dem Abrufen des lokalen **"RecordSet"-Objekts** in Azure DNS geändert wurde.
Dies bietet Schutz für gleichzeitige Änderungen.
Dies kann mithilfe des Parameters *"Overwrite"* unterdrückt werden, wodurch der Datensatzsatz unabhängig von gleichzeitigen Änderungen gelöscht wird.

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
passthru

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
Gibt das zu **entfernende "RecordSet"-Objekt** an.
Alternativ kann der Datensatzsatz mit den *Parametern "Name"* und *"Zone"* oder mit den *Parametern "Name",* *"ZoneName"* und *"ResourceGroupName" angegeben* werden.

```yaml
Type: Microsoft.Azure.Commands.Dns.DnsRecordSet
Parameter Sets: Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -RecordType
Gibt den Typ des DNS-Eintrags an.
Gültige Werte sind:
- A
- AAAA
- CNAME
- MX
- NS
- PTR
- SRV
- TXT-SOA-Einträge werden automatisch gelöscht, wenn die Zone gelöscht wird.
Sie können keine SOA-Einträge manuell löschen.

```yaml
Type: Microsoft.Azure.Management.Dns.Models.RecordType
Parameter Sets: Fields, Mixed
Aliases:
Accepted values: A, AAAA, CAA, CNAME, MX, NS, PTR, SOA, SRV, TXT

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Gibt die Ressourcengruppe an, die die DNS-Zone enthält, die das zu **löschende RecordSet** enthält.
Dieser Parameter gilt nur, wenn der Eintragssatz und die DNS-Zone mit den *Parametern "Name"* und *"ZoneName" angegeben* werden.
Alternativ können Sie den Datensatzsatz mit dem *Parameter "RecordSet"* oder den *Parametern "Name"* und *"Zone"* angeben.

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

### -Zone
Gibt die DNS-Zone an, die das **zu löschende RecordSet** enthält.
Dieser Parameter gilt nur, wenn der Datensatzsatz mit dem Parameter *"Name" angegeben* wird.
Alternativ können Sie den Datensatzsatz mit dem *Parameter "RecordSet"* oder den *Parametern "Name",* *"ZoneName"* und *"ResourceGroupName"* angeben.

```yaml
Type: Microsoft.Azure.Commands.Dns.DnsZone
Parameter Sets: Mixed
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ZoneName
Gibt den Namen der Zone an, die das **zu löschende RecordSet** enthält.
Sie müssen auch die Parameter *"Name"* und *"ResourceGroupName"* angeben.
Alternativ kann der Datensatzsatz entweder mit dem *Parameter "RecordSet"* oder mit den *Parametern "Name"* und *"Zone" angegeben* werden.

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

### Microsoft.Azure.Management.Dns.Models.RecordType

### System.String

### Microsoft.Azure.Commands.Dns.DnsZone

### Microsoft.Azure.Commands.Dns.DnsRecordSet

## AUSGABEN

### System.Boolean

## HINWEISE
Mit dem Parameter *"Bestätigen"* können Sie steuern, ob Sie von diesem Cmdlet zur Bestätigung aufgefordert werden.
Standardmäßig werden Sie vom Cmdlet zur Bestätigung aufgefordert, wenn $ConfirmPreference Windows PowerShell Variable den Wert "Mittel" oder "Niedriger" hat.
Wenn Sie *"Bestätigen"* oder *"Bestätigen:$True"* angeben, fordert Sie dieses Cmdlet zur Bestätigung auf, bevor es ausgeführt wird.
Wenn Sie *"Confirm:$False" angeben,* werden Sie vom Cmdlet nicht zur Bestätigung aufgefordert.

## LINKS ZU VERWANDTEN THEMEN

[Get-AzDnsRecordSet](./Get-AzDnsRecordSet.md)

[New-AzDnsRecordSet](./New-AzDnsRecordSet.md)

[Set-AzDnsRecordSet](./Set-AzDnsRecordSet.md)
