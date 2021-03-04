---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 5B7B285A-6418-44D7-BD78-E14AFFAA7765
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/update-azapimanagementregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementRegion.md
ms.openlocfilehash: c2e01d4a3f6ee3466151202a1c1d681c9f4e5486
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101944303"
---
# Update-AzApiManagementRegion

## SYNOPSIS
Aktualisiert den vorhandenen Bereitstellungsbereich in der PsApiManagement-Instanz.

## SYNTAX

```
Update-AzApiManagementRegion -ApiManagement <PsApiManagement> -Location <String> -Sku <PsApiManagementSku>
 -Capacity <Int32> [-VirtualNetwork <PsApiManagementVirtualNetwork>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## BESCHREIBUNG
Das **Update-AzApiManagementRegion-Cmdlet** aktualisiert eine vorhandene Instanz vom Typ **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion** in einer Sammlung von **AdditionalRegions-Objekten** eines bereitgestellten Instanzentyps vom Typ **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement**.
Dieses Cmdlet stellt nichts mehr zur Verfügung, sondern aktualisiert eine Instanz von **PsApiManagement** im Arbeitsspeicher.
Zum Aktualisieren einer Bereitstellung einer API-Verwaltung verwenden Sie die geänderte **PsApiManagementInstance** für das Set-AzApiManagement cmdlet.

## BEISPIELE

### Beispiel 1: Erhöht die Kapazität der zusätzlichen Region in einer PsApiManagement-Instanz
```powershell
PS C:\>$apimService = Get-AzApiManagement -ResourceGroupName $resourceGroupName -Name $apiManagementName
PS C:\>$apimService = Update-AzApiManagementRegion -ApiManagement $apimService -Location "North Central US" -Capacity 2 -Sku Premium
PS C:\>$apimService = Set-AzApiManagement -InputObject $apimService -PassThru
```

Dieser Befehl ruft den API Management Premium SKU-Dienst ab, der Regionen in Süd-Zentral-USA und Nord-Zentral-USA hat. Anschließend wird die Kapazität der Region "Usa, Norden, Mitte" mithilfe von **Set-AzApiManagement** auf 2 erhöht. Das nächste Cmdlet **Set-AzApiManagement** wendet die Konfigurationsänderung auf den Api-Verwaltungsdienst an.

### Beispiel 2

Aktualisiert den vorhandenen Bereitstellungsbereich in der PsApiManagement-Instanz. (automatisch generiert)

```powershell
<!-- Aladdin Generated Example --> 
Update-AzApiManagementRegion -ApiManagement <PsApiManagement> -Capacity 2 -Location 'North Central US' -Sku Developer -VirtualNetwork <PsApiManagementVirtualNetwork>
```

## PARAMETER

### -ApiManagement
Gibt die **PsApiManagement-Instanz** zum Aktualisieren eines vorhandenen Bereitstellungsbereichs in an.

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
Gibt den neuen SKU-Kapazitätswert für die Bereitstellungsregion an.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.

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
Gibt den Speicherort des zu aktualisierenden Bereitstellungsbereichs an.
Gibt den Speicherort der neuen Bereitstellungsregion unter der unterstützten Region für den Api-Verwaltungsdienst an.
Um gültige Speicherorte zu erhalten, verwenden Sie das cmdlet Get-AzResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | wobei {$_. ResourceTypes[0]. ResourceTypeName -eq "service"} | Select-Object Speicherorte

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

### -Sku
Gibt den neuen Wert der Ebene für den Bereitstellungsbereich an.
Gültige Werte sind:
- Entwickler
- Standard
- Premium

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku
Parameter Sets: (All)
Aliases:
Accepted values: Developer, Standard, Premium, Basic, Consumption

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VirtualNetwork
Gibt eine virtuelle Netzwerkkonfiguration für die Bereitstellungsregion an.
Durch $null werden virtuelle Netzwerkkonfigurationen für die Region entfernt.

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## EINGABEN

### Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement

### System.String

### Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku

### System.Int32

### Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork

## AUSGABEN

### Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement

## NOTIZEN

## VERWANDTE LINKS

[Add-AzApiManagementRegion](./Add-AzApiManagementRegion.md)

[Remove-AzApiManagementRegion](./Remove-AzApiManagementRegion.md)

[Set-AzApiManagement](./Set-AzApiManagement.md)
