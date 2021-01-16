---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 5B7B285A-6418-44D7-BD78-E14AFFAA7765
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/update-azapimanagementregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementRegion.md
ms.openlocfilehash: 8552592acb45702c866c8d918121b8dd61d126a8
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98381533"
---
# Update-AzApiManagementRegion

## SYNOPSIS
Aktualisiert die vorhandene Bereitstellungsregion in der PsApiManagement-Instanz.

## SYNTAX

```
Update-AzApiManagementRegion -ApiManagement <PsApiManagement> -Location <String> -Sku <PsApiManagementSku>
 -Capacity <Int32> [-VirtualNetwork <PsApiManagementVirtualNetwork>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## BESCHREIBUNG
Das **Cmdlet "Update-AzApiManagementRegion"** aktualisiert eine vorhandene Instanz des Typs **"Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion"** in einer Sammlung von **"AdditionalRegions"-Objekten** einer bereitgestellten Instanz des Typs **"Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement".**
Mit diesem Cmdlet wird nichts bereitgestellt, sondern eine Instanz von **PsApiManagement** im Arbeitsspeicher aktualisiert.
Um eine Bereitstellung einer API Management zu aktualisieren, verwenden Sie die geänderte **PsApiManagementInstance** für das Set-AzApiManagement Cmdlet.

## BEISPIELE

### Beispiel 1: Erhöht die Kapazität der zusätzlichen Region in einer PsApiManagement-Instanz.
```powershell
PS C:\>$apimService = Get-AzApiManagement -ResourceGroupName $resourceGroupName -Name $apiManagementName
PS C:\>$apimService = Update-AzApiManagementRegion -ApiManagement $apimService -Location "North Central US" -Capacity 2 -Sku Premium
PS C:\>$apimService = Set-AzApiManagement -InputObject $apimService -PassThru
```

Mit diesem Befehl wird der API Management Premium-SKU-Dienst mit Regionen in der Mitte Süden und der Mitte des Nordens der USA bereitgestellt. Anschließend erhöht sie die Kapazität der Region "USA, Nord-Mitte" mithilfe von **Set-AzApiManagement auf** 2. Das nächste Cmdlet **"Set-AzApiManagement"** wendet die Konfigurationsänderung auf den Api-Verwaltungsdienst an.

### Beispiel 2

Aktualisiert die vorhandene Bereitstellungsregion in der PsApiManagement-Instanz. (automatisch generiert)

```powershell
<!-- Aladdin Generated Example --> 
Update-AzApiManagementRegion -ApiManagement <PsApiManagement> -Capacity 2 -Location 'North Central US' -Sku Developer -VirtualNetwork <PsApiManagementVirtualNetwork>
```

## PARAMETERS

### -ApiManagement
Gibt die **Instanz "PsApiManagement"** an, in der eine vorhandene Bereitstellungsregion aktualisiert werden soll.

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
Gibt den Speicherort der zu aktualisierenden Bereitstellungsregion an.
Gibt den Speicherort der neuen Bereitstellungsregion unter der unterstützten Region für den Api-Verwaltungsdienst an.
Verwenden Sie zum Abrufen gültiger Speicherorte das Cmdlet Get-AzResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | dabei {$_. ResourceTypes[0]. ResourceTypeName -eq "service"} | Select-Object von Speicherorten

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

### -SKU
Gibt den neuen Tierwert für die Bereitstellungsregion an.
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
Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## EINGABEN

### Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement

### System.String

### Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku

### System.Int32

### Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork

## AUSGABEN

### Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement

## HINWEISE

## LINKS ZU VERWANDTEN THEMEN

[Add-AzApiManagementRegion](./Add-AzApiManagementRegion.md)

[Remove-AzApiManagementRegion](./Remove-AzApiManagementRegion.md)

[Set-AzApiManagement](./Set-AzApiManagement.md)
