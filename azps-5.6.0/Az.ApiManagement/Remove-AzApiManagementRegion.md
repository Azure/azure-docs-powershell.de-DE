---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 17D7EBD2-FE3F-4D24-A1AA-8C45B9B1FEF5
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/remove-azapimanagementregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementRegion.md
ms.openlocfilehash: 2e6ae18054f7ad3e122169522d111adfe612b955
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101947640"
---
# Remove-AzApiManagementRegion

## SYNOPSIS
Entfernt einen vorhandenen Bereitstellungsbereich aus der PsApiManagement-Instanz.

## SYNTAX

```
Remove-AzApiManagementRegion -ApiManagement <PsApiManagement> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESCHREIBUNG
Das **Cmdlet Remove-AzApiManagementRegion** entfernt die Instanz des Typs **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion** aus einer Sammlung von **AdditionalRegions** von, die die Instanz des Typs **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement enthält.**
Dieses Cmdlet ändert die Bereitstellung nicht allein, sondern aktualisiert die Instanz von **PsApiManagement** im Arbeitsspeicher.
Um eine Bereitstellung einer API-Verwaltung zu aktualisieren, übergeben Sie die geänderte **PsApiManagementInstance** an **Set-AzApiManagement**.

## BEISPIELE

### Beispiel 1: Entfernen einer Region aus einer PsApiManagement-Instanz
```
PS C:\>Remove-AzApiManagementRegion -ApiManagement $ApiManagement -Location "East US"
```

Mit diesem Befehl wird die Region "Ost-USA" aus der **PsApiManagement-Instanz** entfernt.

### Beispiel 2: Entfernen einer Region aus einer PsApiManagement-Instanz mit einer Reihe von Befehlen
```
PS C:\>Get-AzApiManagement -ResourceGroupName "Contoso" -Name ContosoApi | Remove-AzApiManagementRegion -Location "East US" | Set-AzApiManagement
```

Dieser erste Befehl ruft eine Instanz von **PsApiManagement aus** der Ressourcengruppe Contoso namens ContosoApi ab.
Der letzte Befehl entfernt dann die Region "Ost-USA" aus dieser Instanz und aktualisiert dann die Bereitstellung.

## PARAMETER

### -ApiManagement
Gibt die **PsApiManagement-Instanz** an, aus der dieses Cmdlet den zusätzlichen Bereitstellungsbereich entfernt.

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

### -DefaultProfile

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
Gibt den Speicherort des Von diesem Cmdlets entfernten Bereich an.
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

### CommonParameters
Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## EINGABEN

### Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement

### System.String

## AUSGABEN

### Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement

## NOTIZEN

## VERWANDTE LINKS

[Add-AzApiManagementRegion](./Add-AzApiManagementRegion.md)

[Update-AzApiManagementRegion](./Update-AzApiManagementRegion.md)


