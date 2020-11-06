---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/set-azurermdatalakestoreitemexpiry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreItemExpiry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreItemExpiry.md
ms.openlocfilehash: 6908bc4d474d0dbe9df045332f3820b5f7536dac
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500622"
---
# Set-AzureRmDataLakeStoreItemExpiry

## Synopsis
Legt die Ablaufzeit für eine Datei in einem Azure Data Lake Store-Konto fest oder entfernt Sie.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

### SetAbsoluteNeverExpireExpiry (Standard)
```
Set-AzureRmDataLakeStoreItemExpiry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [[-Expiration] <DateTimeOffset>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SetRelativeExpiry
```
Set-AzureRmDataLakeStoreItemExpiry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [[-RelativeFileExpiryOption] <PathRelativeExpiryOptions>] [[-RelativeTime] <Int64>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Set-AzureRmDataLakeStoreItemExpiry** " legt die Ablaufzeit für eine Datei in einem Azure Data Lake Store-Konto fest oder entfernt Sie.

## Beispiele

### Beispiel 1: Einrichten der Ablaufzeit für eine Datei
```
PS C:\> Set-AzureRmDataLakeStoreItemExpiry -AccountName "ContosoADL" -Path /myfile.txt -Expiration [DateTimeOffset]::Now.AddHours(2)
```

Legt das Ablaufdatum für die Datei myfile.txt in Konto ContosoADL auf zwei Stunden fest.
Dies führt dazu, dass die Datei in zwei Stunden abläuft (für DELETE markiert ist).

### Beispiel 2: Entfernen des Ablaufs für eine Datei
```
PS C:\> Set-AzureRmDataLakeStoreItemExpiry -AccountName "ContosoADL" -Path /myfile.txt
```

Entfernt alle Ablaufdaten, die zuvor für die Datei "myfile.txt" im Konto "ContosoADL" festgesetzt wurden.
Dies bedeutet, dass die Datei nicht automatisch abläuft (für DELETE markiert ist) und manuell gelöscht oder wieder ablaufen muss.


### Beispiel 3: Legen Sie die Ablaufzeit für eine Datei relativ zu jetzt
```
PS C:\> Set-AdlStoreItemExpiry -Account "ContosoADL" -path /myfile.txt -RelativeFileExpiryOption RelativeToNow -RelativeTime 240000
PS C:\> Set-AdlStoreItemExpiry -Account "ContosoADL" -path /myfile.txt -RelativeFileExpiryOption RelativeToCreationDate -RelativeTime 240000
```

Der erste Befehl legt die Ablaufzeit der Datei/myfile.txt 240 Sekunden relativ zur aktuellen Uhrzeit auf dem Server fest.

Der zweite Befehl legt die Ablaufzeit für die Datei/myfile.txt 240 Sekunden relativ zum Erstellungszeitpunkt auf dem Server fest.

## Parameter

### -Konto
Gibt den Namen des Daten Lake Store-Kontos an.

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.

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

### -Ablauf
Die absolute Ablaufzeit für die angegebene Datei.
Wenn kein Wert oder auf MaxValue gesetzt wird, läuft die Datei nie ab.

```yaml
Type: DateTimeOffset
Parameter Sets: Set expiry as Absolute or NeverExpire
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RelativeFileExpiryOption
Relative Ablauf Optionen. RelativeToNow oder RelativeToCreationDate sind aktuelle Optionen
```yaml
Type: PathRelativeExpiryOptions
Parameter Sets: Set expiry as relative to creation or now
Aliases: 
Accepted values: RelativeToNow, RelativeToCreationDate

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Path
Gibt den Daten See-Speicherpfad für das Dateielement an, für das das Ablaufdatum festgelegt oder entfernt werden soll.

```yaml
Type: DataLakeStorePathInstance
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Relativzeit
Relative Zeit in Millisekunden in Bezug auf "jetzt" oder "Erstellungszeit"
```yaml
Type: Int64
Parameter Sets: Set expiry as relative to creation or now
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
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
Default value: None
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
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### Keine
Dieses Cmdlet akzeptiert keine Eingaben.

## Ausgaben

### DataLakeStoreItem
Die aktualisierte Datei mit einer neuen Ablaufzeit.

## Notizen
Alias: Set-AdlStoreItemExpiry

## Verwandte Links

[Get-AzureRmDataLakeStoreItem](./Get-AzureRmDataLakeStoreItem.md)

