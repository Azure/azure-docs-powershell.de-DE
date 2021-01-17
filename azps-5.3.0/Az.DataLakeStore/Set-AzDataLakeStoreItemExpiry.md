---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/set-azdatalakestoreitemexpiry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemExpiry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemExpiry.md
ms.openlocfilehash: ff769801c7a3496ab094e5c9877e0b53fb64fbfd
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98458035"
---
# Set-AzDataLakeStoreItemExpiry

## SYNOPSIS
Legt die Ablaufzeit für eine Datei in einem Azure Data Lake Store-Konto fest oder entfernt sie.

## SYNTAX

### SetAbsoluteNeverExpireExpiry (Standard)
```
Set-AzDataLakeStoreItemExpiry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [[-Expiration] <DateTimeOffset>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SetRelativeExpiry
```
Set-AzDataLakeStoreItemExpiry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-RelativeFileExpiryOption] <PathRelativeExpiryOptions> [[-RelativeTime] <Int64>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## BESCHREIBUNG
Das **Cmdlet "Set-AzDataLakeStoreItemExpiry"** legt die Ablaufzeit für eine Datei in einem Azure Data Lake Store-Konto fest oder entfernt sie.

## BEISPIELE

### Beispiel 1: Festlegen der Ablaufzeit für eine Datei
```
PS C:\> Set-AzDataLakeStoreItemExpiry -AccountName "ContosoADL" -Path /myfile.txt -Expiration [DateTimeOffset]::Now.AddHours(2)
```

Legt den Ablauf für die myfile.txt im Konto ContosoADL auf zwei Stunden fest.
Dadurch läuft die Datei in zwei Stunden ab (wird zum Löschen markiert).

### Beispiel 2: Entfernen des Ablaufs einer Datei
```
PS C:\> Set-AzDataLakeStoreItemExpiry -AccountName "ContosoADL" -Path /myfile.txt
```

Entfernt alle Ablaufzeiten, die zuvor für die Datei "myfile.txt" im Konto "ContosoADL" festgelegt wurden.
Dies bedeutet, dass die Datei nicht automatisch abläuft (zum Löschen markiert) und manuell gelöscht werden muss oder festgelegt ist, dass sie erneut abläuft.

### Beispiel 3: Festlegen der Ablaufzeit für eine Datei relativ zu "Jetzt"
```
PS C:\> Set-AdlStoreItemExpiry -Account "ContosoADL" -path /myfile.txt -RelativeFileExpiryOption RelativeToNow -RelativeTime 240000
PS C:\> Set-AdlStoreItemExpiry -Account "ContosoADL" -path /myfile.txt -RelativeFileExpiryOption RelativeToCreationDate -RelativeTime 240000
```

Der erste Befehl legt die Ablaufzeit der Datei /myfile.txt 240 Sekunden relativ zur aktuellen Serverzeit fest.
Der zweite Befehl legt die Ablaufzeit der Datei /myfile.txt 240 Sekunden relativ zur Erstellungszeit beim Server fest.

## PARAMETERS

### -Konto
Gibt den Namen des Data Lake Store-Kontos an.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.

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

### -Expiration
Die absolute Ablaufzeit für die angegebene Datei.
Wenn kein Wert oder wert auf "MaxValue" festgelegt ist, läuft die Datei nie ab.

```yaml
Type: System.DateTimeOffset
Parameter Sets: SetAbsoluteNeverExpireExpiry
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Path
Gibt den Data Lake Store-Pfad des Dateielements an, dessen Ablaufdatum festgelegt oder entfernt werden soll.

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RelativeFileExpiryOption
Relative Ablaufoptionen. RelativeToNow oder RelativeToCreationDate sind aktuelle Optionen.

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+PathRelativeExpiryOptions
Parameter Sets: SetRelativeExpiry
Aliases:
Accepted values: RelativeToNow, RelativeToCreationDate

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RelativeTime
Die relative Zeit in Millisekunden in Bezug auf die Jetzt- oder Erstellungszeit

```yaml
Type: System.Int64
Parameter Sets: SetRelativeExpiry
Aliases:

Required: False
Position: 3
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
Default value: None
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
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## EINGABEN

### System.String

### Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance

### System.DateTimeOffset

### Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+PathRelativeExpiryOptions

### System.Int64

## AUSGABEN

### Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItem

## HINWEISE
Alias: Set-AdlStoreItemExpiry

## LINKS ZU VERWANDTEN THEMEN

[Get-AzDataLakeStoreItem](./Get-AzDataLakeStoreItem.md)

