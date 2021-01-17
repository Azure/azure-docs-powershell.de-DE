---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 9D4A68A8-0A39-4C9A-8EA6-391A5E7A0E25
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/add-azapimanagementregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementRegion.md
ms.openlocfilehash: 172bd1490b105b942dc706afe9440030d39d5c49
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98471525"
---
# Add-AzApiManagementRegion

## SYNOPSIS
Fügt einer "PsApiManagement"-Instanz neue Bereitstellungsregionen hinzu.

## SYNTAX

```
Add-AzApiManagementRegion -ApiManagement <PsApiManagement> -Location <String> [-Sku <PsApiManagementSku>]
 [-Capacity <Int32>] [-VirtualNetwork <PsApiManagementVirtualNetwork>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESCHREIBUNG
Das **Cmdlet "Add-AzApiManagementRegion"** fügt der Sammlung **"AdditionalRegions"** der bereitgestellten Instanz des Typs **"Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement"** eine neue Instanz des Typs **"PsApiManagementRegion"** hinzu.
Dieses Cmdlet stellt nichts allein zur Verfügung, sondern aktualisiert die Instanz **von PsApiManagement** im Arbeitsspeicher.
Um eine Bereitstellung einer API Management zu aktualisieren, übergeben Sie die geänderte **"PsApiManagement"-Instanz** an "Set-AzApiManagement".

## BEISPIELE

### Beispiel 1: Hinzufügen neuer Bereitstellungsregionen zu einer Instanz "PsApiManagement"
```
PS C:\>Add-AzApiManagementRegion -ApiManagement $ApiManagement -Location "East US" -Sku "Premium" -Capacity 2
```

Mit diesem Befehl werden der Instanz **"PsApiManagement"** zwei Premium-SKU-Einheiten und die Region "Ost US" hinzufügt.

### Beispiel 2: Hinzufügen neuer Bereitstellungsregionen zu einer Instanz "PsApiManagement" und anschließendes Aktualisieren der Bereitstellung
```powershell
PS C:\>$service = Get-AzApiManagement -ResourceGroupName "Contoso" -Name "ContosoApi"
PS C:\>$service = Add-AzApiManagementRegion -ApiManagement $service -Location $secondarylocation -VirtualNetwork $additionalRegionVirtualNetwork
PS C:\>$service = Set-AzApiManagement -InputObject $service -PassThru
```

Dieser Befehl ruft ein **"PsApiManagement"-Objekt** ab, fügt zwei Premium-SKU-Einheiten für die Region "Ost-USA" hinzu und aktualisiert dann die Bereitstellung.

## PARAMETERS

### -ApiManagement
Gibt die **Instanz "PsApiManagement"** an, der dieses Cmdlet weitere Bereitstellungsregionen hinzufügt.

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

### -Capacity
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

### -Location
Gibt den Speicherort der neuen Bereitstellungsregion unter der unterstützten Region für den Api-Verwaltungsdienst an.
Verwenden Sie zum Abrufen gültiger Speicherorte das Cmdlet Get-AzResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | dabei {$_. ResourceTypes[0]. ResourceTypeName -eq "service"} | Select-Object von Speicherorten

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
Gibt die Stufe der Bereitstellungsregion an.
Gültige Werte sind: 
- Entwickler
- Standard
- Premium

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku]
Parameter Sets: (All)
Aliases:
Accepted values: Developer, Standard, Premium, Basic, Consumption

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
Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## EINGABEN

### Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement

## AUSGABEN

### Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement

## HINWEISE
* Das Cmdlet schreibt die aktualisierte **Instanz "PsApiManagement"** in die Pipeline.

## LINKS ZU VERWANDTEN THEMEN

[Remove-AzApiManagementRegion](./Remove-AzApiManagementRegion.md)

[Update-AzApiManagementRegion](./Update-AzApiManagementRegion.md)

[Set-AzApiManagement](./Set-AzApiManagement.md)


