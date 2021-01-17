---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 17D7EBD2-FE3F-4D24-A1AA-8C45B9B1FEF5
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementRegion.md
ms.openlocfilehash: 70816b054acc7667d2246ea72901c65890f9389e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98381925"
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
Mit dem Cmdlet **"Remove-AzApiManagementRegion"** wird eine Instanz des Typs **"Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion"** aus einer Sammlung von **"AdditionalRegions"** der bereitgestellten Instanz des Typs **"Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement"** entfernt.
Dieses Cmdlet ändert die Bereitstellung nicht allein, sondern aktualisiert die Instanz von **PsApiManagement** im Arbeitsspeicher.
Um eine Bereitstellung einer API Management zu aktualisieren, übergeben Sie die geänderte **"PsApiManagementInstance"** an **Set-AzApiManagement.**

## BEISPIELE

### Beispiel 1: Entfernen einer Region aus einer Instanz "PsApiManagement"
```
PS C:\>Remove-AzApiManagementRegion -ApiManagement $ApiManagement -Location "East US"
```

Mit diesem Befehl wird die Region "Ost US" aus der Instanz **"PsApiManagement"** entfernt.

### Beispiel 2: Entfernen einer Region aus einer "PsApiManagement"-Instanz mithilfe einer Reihe von Befehlen
```
PS C:\>Get-AzApiManagement -ResourceGroupName "Contoso" -Name ContosoApi | Remove-AzApiManagementRegion -Location "East US" | Set-AzApiManagement
```

Dieser erste Befehl ruft eine Instanz von **"PsApiManagement" aus** der Ressourcengruppe "Contoso" namens "ContosoApi" ab.
Der letzte Befehl entfernt dann die Region mit dem Namen "OST US" aus dieser Instanz und aktualisiert dann die Bereitstellung.

## PARAMETERS

### -ApiManagement
Gibt die **Instanz "PsApiManagement"** an, aus der dieses Cmdlet den zusätzlichen Bereitstellungsbereich entfernt.

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
Gibt den Speicherort der Region an, die von diesem Cmdlet entfernt wird.
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

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## EINGABEN

### Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement

### System.String

## AUSGABEN

### Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement

## HINWEISE

## LINKS ZU VERWANDTEN THEMEN

[Add-AzApiManagementRegion](./Add-AzApiManagementRegion.md)

[Update-AzApiManagementRegion](./Update-AzApiManagementRegion.md)


