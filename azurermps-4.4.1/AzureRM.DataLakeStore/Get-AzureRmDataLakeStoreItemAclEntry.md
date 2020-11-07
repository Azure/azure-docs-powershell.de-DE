---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: DFE8C373-2BBA-4A4E-B4B1-926373E68FC4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreItemAclEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreItemAclEntry.md
ms.openlocfilehash: 2532b8fb63fb864cf2c70b9e2bfd1d5ef1a5365e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663959"
---
# Get-AzureRmDataLakeStoreItemAclEntry

## Synopsis
Ruft einen Eintrag in der ACL einer Datei oder eines Ordners im Data Lake Store ab.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

```
Get-AzureRmDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzureRmDataLakeStoreItemAclEntry** " ruft in der Zugriffssteuerungsliste (ACL) einer Datei oder eines Ordners im Data Lake Store einen Eintrag (ACE) ab.

## Beispiele

### Beispiel 1: Abrufen der ACL für einen Ordner
```
PS C:\> Get-AzureRmDataLakeStoreItemAclEntry -AccountName 'ContosoADL' -Path '/'
```

Mit diesem Befehl wird die ACL für das Stammverzeichnis des angegebenen Data Lake Store-Kontos abgerufen.

## Parameter

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

### -Path
Gibt den Daten See-Speicherpfad des Elements an, für das dieses Cmdlet ab dem Stammverzeichnis (/) ein Ass erhält.

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

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.

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

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

## Ausgaben

### IEnumerable<DataLakeStoreItemAce>
Die Liste der ACL-Einträge für den angegebenen Ordner oder die angegebene Datei.

## Notizen

## Verwandte Links

[Remove-AzureRmDataLakeStoreItemAclEntry](./Remove-AzureRmDataLakeStoreItemAclEntry.md)

[Satz-AzureRmDataLakeStoreItemAclEntry](./Set-AzureRmDataLakeStoreItemAclEntry.md)


