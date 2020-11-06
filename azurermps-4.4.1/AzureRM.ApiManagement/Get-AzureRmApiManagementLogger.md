---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: A935ABAC-6C60-4AE3-9434-B9BCC1182A34
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementLogger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementLogger.md
ms.openlocfilehash: 48033c250286c59e2cadfadc1a5b5d28f869a66c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500978"
---
# Get-AzureRmApiManagementLogger

## Synopsis
Ruft API-Verwaltungs Protokollierungs Objekte ab.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

### Abrufen aller Protokollierungen (Standard)
```
Get-AzureRmApiManagementLogger -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### Abrufen nach Protokollierungs-ID
```
Get-AzureRmApiManagementLogger -Context <PsApiManagementContext> -LoggerId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzureRmApiManagementLogger** " Ruft eine Azure API-Verwaltungs **Protokollierung** oder alle Protokollierungen ab.

## Beispiele

### Beispiel 1: Abrufen aller Protokollierungen
```
PS C:\>Get-AzureRmApiManagementLogger -Context $ApimContext
```

Dieser Befehl ruft alle Protokollierungen für den angegebenen Kontext ab.

### Beispiel 2: Abrufen einer bestimmten Protokollierung
```
PS C:\>Get-AzureRmApiManagementLogger -Context $ApimContext -LoggerId "Logger123"
```

Dieser Befehl entfernt eine Protokollierung mit der ID Logger123.

## Parameter

### -Context
Gibt ein **PsApiManagementContext** -Objekt an.

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Protokollierungs-Nr
Gibt die ID der bestimmten Protokollierung an, die abgerufen werden soll.

```yaml
Type: System.String
Parameter Sets: Get by logger ID
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

## Ausgaben

### IList<Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementLogger>

## Notizen

## Verwandte Links

[Neu – AzureRmApiManagementLogger](./New-AzureRmApiManagementLogger.md)

[Remove-AzureRmApiManagementLogger](./Remove-AzureRmApiManagementLogger.md)

[Satz-AzureRmApiManagementLogger](./Set-AzureRmApiManagementLogger.md)


