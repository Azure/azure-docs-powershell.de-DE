---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: DBA7AD5F-CC13-417A-B753-F998942530BB
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagement.md
ms.openlocfilehash: c636da952c02b4f2b4795cd1703c276a23a8221c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93650404"
---
# Get-AzApiManagement

## Synopsis
Ruft eine Liste oder eine bestimmte API-Verwaltungsdienst Beschreibung ab.

## Syntax

### GetBySubscription (Standard)
```
Get-AzApiManagement [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetByResourceGroup
```
Get-AzApiManagement -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetByResource
```
Get-AzApiManagement -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzApiManagement** " Ruft eine Liste aller API-Verwaltungsdienste unter Abonnement oder angegebene Ressourcengruppe oder eine bestimmte API-Verwaltung ab.

## Beispiele

### Beispiel 1: Abrufen aller API-Verwaltungsdienste
```powershell
PS C:\>Get-AzApiManagement
```

Dieser Befehl ruft alle API-Verwaltungsdienste innerhalb eines Abonnements ab.

### Beispiel 2: Abrufen aller API-Verwaltungsdienste nach einem bestimmten Namen
```powershell
PS C:\>Get-AzApiManagement -ResourceGroupName "ContosoGroup" -Name "ContosoApi"
```

Mit diesem Befehl wird der gesamte API-Verwaltungsdienst nach Namen abgerufen.

## Parameter

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

### -Name
Gibt den Namen des API-Verwaltungsdiensts an.

```yaml
Type: System.String
Parameter Sets: GetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Gibt den Namen der Ressourcengruppe an, unter der dieses Cmdlet den API-Verwaltungsdienst erhält.

```yaml
Type: System.String
Parameter Sets: GetByResourceGroup, GetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### System. String

## Ausgaben

### Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement

## Notizen

## Verwandte Links

[Backup-AzApiManagement](./Backup-AzApiManagement.md)

[Neu – AzApiManagement](./New-AzApiManagement.md)

[Remove-AzApiManagement](./Remove-AzApiManagement.md)

[Wiederherstellen – AzApiManagement](./Restore-AzApiManagement.md)


