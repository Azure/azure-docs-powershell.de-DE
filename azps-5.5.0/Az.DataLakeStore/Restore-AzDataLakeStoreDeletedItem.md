---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: D231E9A0-DC1E-411B-A87A-56A8C767F6C5
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/restore-azdatalakestoredeleteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Restore-AzDataLakeStoreDeletedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Restore-AzDataLakeStoreDeletedItem.md
ms.openlocfilehash: 9dcc45f8f082ce59a6082ad71c2084c5df10064c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100161868"
---
# Restore-AzDataLakeStoreDeletedItem

## SYNOPSIS
Wiederherstellen einer gelöschten Datei oder eines gelöschten Ordners in Azure Data Lake.

## SYNTAX

### Standard (Standard)
```
Restore-AzDataLakeStoreDeletedItem [-Account] <String> [-Path] <String> [-Destination] <String>
 [-Type] <String> [-RestoreAction <String>] [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### InputObject
```
Restore-AzDataLakeStoreDeletedItem [-Account] <String> [-DeletedItem] <DataLakeStoreDeletedItem>
 [-RestoreAction <String>] [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## BESCHREIBUNG
Mit **dem Cmdlet "Restore-AzDataLakeStoreDeletedItem"** wird eine gelöschte Datei oder ein gelöschter Ordner im Data Lake Store wiederhergestellt. Erfordert den Pfad des gelöschten Elements im Papierkorb, der von "Get-AzDataLakeStoreDeletedItem" zurückgegeben wurde.
Vorsicht: Das Wiederherstellen von Dateien ist ein Vorgang nach bestem Aufwand. Es gibt keine Garantie dafür, dass eine Datei nach dem Löschen wiederhergestellt werden kann. Die Verwendung dieser API wird über Whitelisting aktiviert. Wenn Ihr ADL-Konto nicht in der Whiteliste aufgeführt ist, wird mit dieser API die Ausnahme "Nicht implementiert" ausgelöst. Für weitere Informationen und Unterstützung wenden Sie sich bitte an den Microsoft-Support.

## BEISPIELE

### Beispiel 1: Wiederherstellen einer Datei aus dem Data Lake Store mit der Option "-force"
```
PS > Restore-AzDataLakeStoreDeletedItem -Account ml1ptrashtest -Path 927e8fb1-a287-4353-b50e-3b4a39ae4088 -Destination adl://ml1ptrashtest.azuredatalake.com/test0/file_1230 -Type "file" -Force
PS >

### Example 2: Restore a file from Data Lake Store using user confirmation

PS > restore-azdatalakestoredeleteditem -account ml1ptrashtest -path 927e8fb1-a287-4353-b50e-3b4a39ae4088 -destination adl://ml1ptrashtest.azuredatalake.com/test4/file_1115 -type file

Restore user data ?
From - 927e8fb1-a287-4353-b50e-3b4a39ae4088
To   - adl://ml1ptrashtest.azuredatalake.com/test4/file_1115
Type - file
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
PS >
```

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

### -DeletedItem
Das gelöschte Elementobjekt.

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreDeletedItem
Parameter Sets: InputObject
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Destination
Der Zielpfad, in dem die gelöschte Datei oder der gelöschte Ordner wiederhergestellt werden soll. 

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Force
Erzwingt die Ausführung des Befehls ohne Benutzerbestätigung.

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

### -PassThru
Geben Sie boolescher Wert wahr bei Erfolg zurück.

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

### -Path
Der Pfad der gelöschten Datei oder des gelöschten Ordners im Papierkorb.

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RestoreAction
Aktion für Zielnamenskonflikte – "Kopieren" oder "Überschreiben"

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Type
Der Typ des wiederhergestellten Eintrags – "Datei" oder "Ordner"

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## EINGABEN

### System.String

## AUSGABEN

### Keine

## HINWEISE

## LINKS ZU VERWANDTEN THEMEN

[Get-AzDataLakeStoreDeletedItem](./Get-AzDataLakeStoreDeletedItem.md)