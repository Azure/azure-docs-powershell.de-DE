---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 9D4A68A8-0A39-4C9A-8EA6-391A5E7A0E25
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/add-azurermapimanagementregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Add-AzureRmApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Add-AzureRmApiManagementRegion.md
ms.openlocfilehash: 9ea4b734eba1ed1a37a72e756c32acc3d6ad2a32
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498558"
---
# Add-AzureRmApiManagementRegion

## Synopsis
Fügt neue Bereitstellungsbereiche zu einer PsApiManagement-Instanz hinzu.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

```
Add-AzureRmApiManagementRegion -ApiManagement <PsApiManagement> -Location <String> [-Sku <PsApiManagementSku>]
 [-Capacity <Int32>] [-VirtualNetwork <PsApiManagementVirtualNetwork>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das **Add-AzureRmApiManagementRegion-** Cmdlet fügt der Sammlung von **AdditionalRegions** der bereitgestellten Instanz des Typs **Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement** eine neue Instanz des Typs **PsApiManagementRegion** hinzu.
Dieses Cmdlet stellt nichts für sich bereit, sondern aktualisiert die Instanz von **PsApiManagement** im Arbeitsspeicher.
Um eine Bereitstellung einer API-Verwaltung zu aktualisieren, übergeben Sie die geänderte **PsApiManagement** -Instanz an Update-AzureRmApiManagementDeployment.

## Beispiele

### Beispiel 1: Hinzufügen neuer Bereitstellungsbereiche zu einer PsApiManagement-Instanz
```
PS C:\>Add-AzureRmApiManagementRegion -ApiManagement $ApiManagement -Location "East US" -Sku "Premium" -Capacity 2
```

Dieser Befehl addiert zwei Premium-SKU-Einheiten und die Region "East US" zur **PsApiManagement** -Instanz.

### Beispiel 2: Hinzufügen neuer Bereitstellungsbereiche zu einer PsApiManagement-Instanz und anschließendes Aktualisieren der Bereitstellung
```
PS C:\>Get-AzureRmApiManagement -ResourceGroupName "Contoso" -Name "ContosoApi" | Add-AzureRmApiManagementRegion -Location "East US" -Sku "Premium" -Capacity 2 | Update-AzureRmApiManagementDeployment
```

Dieser Befehl ruft ein **PsApiManagement** -Objekt ab, addiert zwei Premium-SKU-Einheiten für die Region mit dem Namen East US und aktualisiert dann die Bereitstellung.

## Parameter

### -ApiManagement
Gibt die **PsApiManagement** -Instanz an, der dieses Cmdlet zusätzliche Bereitstellungsbereiche hinzufügt.

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

### -Kapazität
Gibt die SKU-Kapazität des Bereitstellungsbereichs an.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
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

### -Standort
Gibt den Speicherort des neuen Bereitstellungsbereichs zwischen dem unterstützten Bereich für den API-Verwaltungsdienst an.
Verwenden Sie zum Abrufen gültiger Speicherorte das Cmdlet Get-AzureRmResourceProvider-ProviderNamespace "Microsoft. ApiManagement" | wobei {$ _. Hilfswerte [0]. "-EQ"-Dienst "} | Select-Object Standorte

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SKU
Gibt die Ebene des Bereitstellungsbereichs an.
Gültige Werte sind: 
- Entwickler
- Standard
- Premium

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku]
Parameter Sets: (All)
Aliases:
Accepted values: Developer, Standard, Premium, Basic

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VirtualNetwork
Gibt eine virtuelle Netzwerkkonfiguration an.

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement
Parameter: ApiManagement (ByValue)

## Ausgaben

### Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement

## Notizen
* Das Cmdlet schreibt eine aktualisierte **PsApiManagement** -Instanz in Pipeline.

## Verwandte Links

[Remove-AzureRmApiManagementRegion](./Remove-AzureRmApiManagementRegion.md)

[Update-AzureRmApiManagementRegion](./Update-AzureRmApiManagementRegion.md)

[Update-AzureRmApiManagementDeployment](./Update-AzureRmApiManagementDeployment.md)


