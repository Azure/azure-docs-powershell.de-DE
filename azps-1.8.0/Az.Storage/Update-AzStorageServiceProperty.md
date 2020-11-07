---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/update-azstorageserviceproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageServiceProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageServiceProperty.md
ms.openlocfilehash: dc7f579366956f8447ba64fc898e97f5c33b70f7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93658714"
---
# Update-AzStorageServiceProperty

## Synopsis
Ändert die Eigenschaften für den Azure-Speicherdienst.

## Syntax

```
Update-AzStorageServiceProperty [-ServiceType] <StorageServiceType> [-DefaultServiceVersion <String>]
 [-PassThru] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **Update-AzStorageServiceProperty** ändert die Eigenschaften für den Azure-Speicherdienst.

## Beispiele

### Beispiel 1: Einrichten des BLOB-Diensts DefaultServiceVersion auf 2017-04-17
```
C:\PS>Update-AzStorageServiceProperty -ServiceType Blob -DefaultServiceVersion 2017-04-17
```

Dieser Befehl legt die DefaultServiceVersion des BLOB-Diensts auf 2017-04-17

## Parameter

### -Context
Gibt einen Azure-Speicherkontext an.
Verwenden Sie das New-AzStorageContext-Cmdlet, um einen Speicherkontext zu erhalten.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultServiceVersion
DefaultServiceVersion gibt die Standard Version an, die für Anforderungen an den BLOB-Dienst verwendet werden soll, wenn die Version einer eingehenden Anforderung nicht angegeben ist. Mögliche Werte sind Version 2008-10-27 und alle neueren Versionen. Weitere Details finden Sie unter https://docs.microsoft.com/en-us/rest/api/storageservices/versioning-for-the-az-storage-services

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru
ServiceProperties anzeigen

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

### -ServiceType
Gibt den Typ des Speicher Diensts an.
Dieses Cmdlet ruft die Protokollierungseigenschaften des Diensttyps ab, den dieser Parameter angibt.
Die zulässigen Werte für diesen Parameter lauten wie folgt:
- BLOB 
- Tabelle
- Warteschlange
- Datei

```yaml
Type: Microsoft.WindowsAzure.Commands.Storage.Common.StorageServiceType
Parameter Sets: (All)
Aliases:
Accepted values: Blob, Table, Queue, File

Required: True
Position: 0
Default value: None
Accept pipeline input: False
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
Zeigt, was passiert, wenn das Cmdlet ausgeführt wird. Das Cmdlet wird nicht ausgeführt.

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

### Microsoft. Azure. Commands. Common. Authentication. Abstractions. IStorageContext

## Ausgaben

### Microsoft. WindowsAzure. Commands. Storage. Model. ResourceModel. PSSeriviceProperties

## Notizen

## Verwandte Links
