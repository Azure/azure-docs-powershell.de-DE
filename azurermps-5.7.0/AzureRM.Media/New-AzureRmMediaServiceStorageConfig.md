---
external help file: Microsoft.Azure.Commands.Media.dll-Help.xml
Module Name: AzureRM.Media
ms.assetid: 4D64CA4D-1066-4D3E-9317-60D37D9DE2BB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.media/new-azurermmediaservicestorageconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/New-AzureRmMediaServiceStorageConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/New-AzureRmMediaServiceStorageConfig.md
ms.openlocfilehash: 7296d744749dd037c10d0d4d5ee2b0461a55b794
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663246"
---
# New-AzureRmMediaServiceStorageConfig

## Synopsis
Erstellen Sie eine Speicherkonto Konfiguration für die Media Service-Cmdlets.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

```
New-AzureRmMediaServiceStorageConfig [-DefaultProfile <IAzureContextContainer>] [-StorageAccountId] <String>
 [-IsPrimary] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **New-AzureRmMediaServiceStorageConfig** erstellt eine Speicherkonto Konfiguration für die Mediendienst-Cmdlets.

## Beispiele

### Beispiel 1: Erstellen einer Speicherkonto Konfiguration für die Media Service-Cmdlets
```
PS C:\>
$StorageAccount = New-AzureRmStorageAccount -ResourceGroupName $ResourceGroupName -Name "Storage1" -Location "East US" -Type "Standard_GRS"

PS C:\> New-AzureRmMediaServiceStorageConfig -StorageAccountId $StorageAccount.Id -IsPrimary
```

Der erste Befehl erstellt ein Speicherkonto Objekt mithilfe des Cmdlets **New-AzureRmStorageAccount** .
Der Befehl benennt dieses Speicherkonto Storage1 und der Typ hat den Namen Standard_GRS und speichert das Ergebnis in der Variablen mit dem Namen $StorageAccount.

Mit dem zweiten Befehl wird ein Speicher Konfigurationsobjekt als das primäre Speicherkonto erstellt, das dem Mediendienst unter Verwendung der Speicherkonto-ID-Informationen zugeordnet ist, die in der $StorageAccount Variablen gespeichert sind.

## Parameter

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

### -IsPrimary
Gibt an, dass das Cmdlet das Speicherkonto als primären Speicher für den Mediendienst erstellt.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StorageAccountId
Gibt die ID des speicherkontos an.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
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
Default value: False
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
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### Keine
Dieses Cmdlet akzeptiert keine Eingaben.

## Ausgaben

### Microsoft. Azure. Commands. Media. Models. PSStorageAccount

## Notizen

## Verwandte Links

[Synchronisieren-AzureRmMediaServiceStorageKeys](./Sync-AzureRmMediaServiceStorageKeys.md)


