---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: DFE8C373-2BBA-4A4E-B4B1-926373E68FC4
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestoreitemaclentry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItemAclEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItemAclEntry.md
ms.openlocfilehash: 02ff6856cf61664c1bd00e7d88fc7f8de999f2a2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98458086"
---
# Get-AzDataLakeStoreItemAclEntry

## SYNOPSIS
Ruft einen Eintrag im ACL einer Datei oder eines Ordners im Data Lake Store ab.

## SYNTAX

```
Get-AzDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESCHREIBUNG
Das **Cmdlet "Get-AzDataLakeStoreItemAclEntry"** ruft einen Eintrag (ACE) in der Zugriffssteuerungsliste (Access Control List, ACL) einer Datei oder eines Ordners im Data Lake Store ab.

## BEISPIELE

### Beispiel 1: Erhalten der ACL für einen Ordner
```
PS C:\> Get-AzDataLakeStoreItemAclEntry -AccountName 'ContosoADL' -Path '/'
```

Dieser Befehl ruft die ACL für das Stammverzeichnis des angegebenen Data Lake Store-Kontos ab.

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

### -Path
Gibt den Data Lake Store-Pfad des Elements an, für das dieses Cmdlet ein ACE erhält, beginnend mit dem Stammverzeichnis (/).

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

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## EINGABEN

### System.String

### Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance

## AUSGABEN

### Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce

## HINWEISE

## LINKS ZU VERWANDTEN THEMEN

[Remove-AzDataLakeStoreItemAclEntry](./Remove-AzDataLakeStoreItemAclEntry.md)

[Set-AzDataLakeStoreItemAclEntry](./Set-AzDataLakeStoreItemAclEntry.md)


