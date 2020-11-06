---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 17D7EBD2-FE3F-4D24-A1AA-8C45B9B1FEF5
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementRegion.md
ms.openlocfilehash: 8bacb26b4e30521ddd840d2a8081365ed9c4c6ad
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93477410"
---
# Remove-AzureRmApiManagementRegion

## Synopsis
Entfernt einen vorhandenen Bereitstellungsbereich aus der PsApiManagement-Instanz.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

```
Remove-AzureRmApiManagementRegion -ApiManagement <PsApiManagement> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **Remove-AzureRmApiManagementRegion** entfernt eine Instanz des Typs **Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagementRegion** aus einer Sammlung von **AdditionalRegions** , die die Instanz des Typs **Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement** bereitgestellt hat.
Dieses Cmdlet ändert die Bereitstellung nicht selbst, sondern aktualisiert die Instanz von **PsApiManagement** im Arbeitsspeicher.
Wenn Sie eine Bereitstellung einer API-Verwaltung aktualisieren möchten, übergeben Sie den geänderten **PsApiManagementInstance** an **Update-AzureRmApiManagement**.

## Beispiele

### Beispiel 1: Entfernen eines Bereichs aus einer PsApiManagement-Instanz
```
PS C:\>Remove-AzureRmApiManagementRegion -ApiManagement $ApiManagement -Location "East US"
```

Mit diesem Befehl wird die Region East US aus der **PsApiManagement** -Instanz entfernt.

### Beispiel 2: Entfernen eines Bereichs aus einer PsApiManagement-Instanz mithilfe einer Reihe von Befehlen
```
PS C:\>Get-AzureRmApiManagement -ResourceGroupName "Contoso" -Name ContosoApi | Remove-AzureRmApiManagementRegion -Location "East US" | Update-AzureRmApiManagementDeployment
```

Dieser erste Befehl ruft eine Instanz von **PsApiManagement** aus der Ressourcengruppe namens Contoso mit dem Namen ContosoApi ab.
Der endgültige Befehl entfernt dann die Region mit dem Namen East US aus dieser Instanz und aktualisiert dann die Bereitstellung.

## Parameter

### -ApiManagement
Gibt die **PsApiManagement** -Instanz an, aus der dieses Cmdlet den zusätzlichen Bereitstellungsbereich entfernt.

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Standort
Gibt den Speicherort des Bereichs an, den dieses Cmdlet entfernt.

Gültige Werte sind: 

- Nord-Zentral-USA
- Süd-Mittelamerika
- Zentral-US
- West Europa
- Nordeuropa
- West-US
- East US
- East US 2
- Japan (Ost)
- Japan West
- Brasilien Süd
- Südostasien
- Ostasien
- Australien (Ost)
- Australien südöstlich

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
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

### PsApiManagement
Der Parameter "ApiManagement" akzeptiert den Wert vom Typ "PsApiManagement" aus der Pipeline.

## Ausgaben

### Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement

## Notizen

## Verwandte Links

[Add-AzureRmApiManagementRegion](./Add-AzureRmApiManagementRegion.md)

[Update-AzureRmApiManagementRegion](./Update-AzureRmApiManagementRegion.md)


