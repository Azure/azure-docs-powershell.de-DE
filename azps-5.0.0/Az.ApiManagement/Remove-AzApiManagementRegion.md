---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 17D7EBD2-FE3F-4D24-A1AA-8C45B9B1FEF5
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementRegion.md
ms.openlocfilehash: 70816b054acc7667d2246ea72901c65890f9389e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94299865"
---
# Remove-AzApiManagementRegion

## Synopsis
Entfernt einen vorhandenen Bereitstellungsbereich aus der PsApiManagement-Instanz.

## Syntax

```
Remove-AzApiManagementRegion -ApiManagement <PsApiManagement> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **Remove-AzApiManagementRegion** entfernt eine Instanz des Typs **Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagementRegion** aus einer Sammlung von **AdditionalRegions** , die die Instanz des Typs **Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement** bereitgestellt hat.
Dieses Cmdlet ändert die Bereitstellung nicht selbst, sondern aktualisiert die Instanz von **PsApiManagement** im Arbeitsspeicher.
Wenn Sie eine Bereitstellung einer API-Verwaltung aktualisieren möchten, übergeben Sie den geänderten **PsApiManagementInstance** an **AzApiManagement**.

## Beispiele

### Beispiel 1: Entfernen eines Bereichs aus einer PsApiManagement-Instanz
```
PS C:\>Remove-AzApiManagementRegion -ApiManagement $ApiManagement -Location "East US"
```

Mit diesem Befehl wird die Region East US aus der **PsApiManagement** -Instanz entfernt.

### Beispiel 2: Entfernen eines Bereichs aus einer PsApiManagement-Instanz mithilfe einer Reihe von Befehlen
```
PS C:\>Get-AzApiManagement -ResourceGroupName "Contoso" -Name ContosoApi | Remove-AzApiManagementRegion -Location "East US" | Set-AzApiManagement
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

### -Standort
Gibt den Speicherort des Bereichs an, den dieses Cmdlet entfernt.
Gibt den Speicherort des neuen Bereitstellungsbereichs zwischen dem unterstützten Bereich für den API-Verwaltungsdienst an.
Verwenden Sie zum Abrufen gültiger Speicherorte das Cmdlet Get-AzResourceProvider-ProviderNamespace "Microsoft. ApiManagement" | wobei {$ _. Hilfswerte [0]. "-EQ"-Dienst "} | Select-Object Standorte

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
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## Eingaben

### Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement

### System. String

## Ausgaben

### Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement

## Notizen

## Verwandte Links

[Add-AzApiManagementRegion](./Add-AzApiManagementRegion.md)

[Update-AzApiManagementRegion](./Update-AzApiManagementRegion.md)


