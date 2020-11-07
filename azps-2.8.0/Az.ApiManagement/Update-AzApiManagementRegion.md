---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 5B7B285A-6418-44D7-BD78-E14AFFAA7765
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/update-azapimanagementregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementRegion.md
ms.openlocfilehash: 7fa565eb16ced9e9146b219d7850354e499ef06e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93658117"
---
# Update-AzApiManagementRegion

## Synopsis
Aktualisiert den vorhandenen Bereitstellungsbereich in PsApiManagement-Instanz.

## Syntax

```
Update-AzApiManagementRegion -ApiManagement <PsApiManagement> -Location <String> -Sku <PsApiManagementSku>
 -Capacity <Int32> [-VirtualNetwork <PsApiManagementVirtualNetwork>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **Update-AzApiManagementRegion** aktualisiert eine vorhandene Instanz des Typs **Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagementRegion** in einer Sammlung von **AdditionalRegions** -Objekten einer bereitgestellten Instanz des Typs **Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement**.
Dieses Cmdlet stellt nichts bereit, sondern aktualisiert eine Instanz von **PsApiManagement** im Arbeitsspeicher.
Verwenden Sie zum Aktualisieren einer Bereitstellung einer API-Verwaltung das geänderte **PsApiManagementInstance** -Cmdlet für das Set-AzApiManagement-Cmdlet.

## Beispiele

### Beispiel 1: erhöht die Kapazität des zusätzlichen Bereichs in einer PsApiManagement-Instanz
```powershell
PS C:\>$apimService = Get-AzApiManagement -ResourceGroupName $resourceGroupName -Name $apiManagementName
PS C:\>$apimService = Update-AzApiManagementRegion -ApiManagement $apimService -Location "North Central US" -Capacity 2 -Sku Premium
PS C:\>$apimService = Set-AzApiManagement -InputObject $apimService -PassThru
```

Dieser Befehl ruft den API-Management-Premium-SKU-Dienst ab, wobei Regionen in Süd-Zentralamerika und Nord-Zentralamerika enthalten sind. Sie erhöht dann die Kapazität der Nord zentralen US-Region auf 2 mit dem **AzApiManagement**. Das nächste Cmdlet **-Satz-AzApiManagement** wendet die Konfigurationsänderung auf den API-Verwaltungsdienst an.

## Parameter

### -ApiManagement
Gibt die **PsApiManagement** -Instanz an, in der ein vorhandener Bereitstellungsbereich aktualisiert werden soll.

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
Gibt den neuen SKU-Kapazitätswert für den Bereitstellungsbereich an.

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
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.

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
Gibt den Speicherort des Bereitstellungsbereichs an, der aktualisiert werden soll.
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

### -SKU
Gibt den neuen Stufenwert für den Bereitstellungsbereich an.
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
Gibt eine virtuelle Netzwerkkonfiguration für den Bereitstellungsbereich an.
Durch Übergabe von $NULL wird die Konfiguration des virtuellen Netzwerks für den Bereich entfernt.

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
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## Eingaben

### Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement

### System. String

### Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagementSku

### System. Int32

### Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagementVirtualNetwork

## Ausgaben

### Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement

## Notizen

## Verwandte Links

[Add-AzApiManagementRegion](./Add-AzApiManagementRegion.md)

[Remove-AzApiManagementRegion](./Remove-AzApiManagementRegion.md)

[Satz-AzApiManagement](./Set-AzApiManagement.md)
