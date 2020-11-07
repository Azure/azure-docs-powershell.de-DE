---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: ECA70C6C-E0B0-445D-BCAD-041625FAC632
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/get-azurermdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreItem.md
ms.openlocfilehash: b1a570d2821606944d4afde21919dad8832ed380
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662472"
---
# Get-AzureRmDataLakeStoreItem

## Synopsis
Ruft die Details einer Datei oder eines Ordners im Data Lake Store ab.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

```
Get-AzureRmDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzureRmDataLakeStoreItem** " Ruft die Details einer Datei oder eines Ordners im Data Lake Store ab.

## Beispiele

### Beispiel 1: Abrufen von Details zu einer Datei aus dem Data Lake Store
```
PS C:\>Get-AzureRmDataLakeStoreItem -AccountName "ContosoADL" -Path "/MyFiles/Test.csv"
```

Dieser Befehl ruft die Details der Datei Test.csv aus dem Data Lake Store ab.

## Parameter

### -Konto
Gibt den Namen des Data Lake Store-Kontos an.

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

### -Path
Gibt den Daten See-Speicherpfad an, aus dem Details zu einem Element abgerufen werden sollen, beginnend mit dem Stammverzeichnis (/).

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

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### Keine
Dieses Cmdlet akzeptiert keine Eingaben.

## Ausgaben

### DataLakeStoreItem
Die Datei oder der Ordner im angegebenen Pfad.

## Notizen

## Verwandte Links

[Export-AzureRmDataLakeStoreItem](./Export-AzureRmDataLakeStoreItem.md)

[Get-AzureRmDataLakeStoreChildItem](./Get-AzureRmDataLakeStoreChildItem.md)

[Importieren-AzureRmDataLakeStoreItem](./Import-AzureRmDataLakeStoreItem.md)

[Teilnehmen – AzureRmDataLakeStoreItem](./Join-AzureRmDataLakeStoreItem.md)

[Verschieben-AzureRmDataLakeStoreItem](./Move-AzureRmDataLakeStoreItem.md)

[Neu – AzureRmDataLakeStoreItem](./New-AzureRmDataLakeStoreItem.md)

[Remove-AzureRmDataLakeStoreItem](./Remove-AzureRmDataLakeStoreItem.md)

[Test-AzureRmDataLakeStoreItem](./Test-AzureRmDataLakeStoreItem.md)


