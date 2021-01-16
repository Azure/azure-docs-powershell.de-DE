---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementhttpmessagediagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementHttpMessageDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementHttpMessageDiagnostic.md
ms.openlocfilehash: 10c84654bb5d074ee9f668062d1fa7a18d92f8b0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98356500"
---
# New-AzApiManagementHttpMessageDiagnostic

## SYNOPSIS
Erstellt eine Instanz von **"PsApiManagementHttpMessageDiagnostic",** bei der es sich um eine Http-Nachrichtendiagnoseeinstellung des Diagnosetools handelt.

## SYNTAX

```
New-AzApiManagementHttpMessageDiagnostic [-HeadersToLog <String[]>] [-BodyBytesToLog <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESCHREIBUNG
Das Cmdlet **"New-AzApiManagementHttpMessageDiagnostic"** erstellt die Diagnoseeinstellung "Http Message".

## BEISPIELE

### Beispiel 1: Erstellen einer grundlegenden Einstellung für die Http-Nachricht-Diagnose
```powershell
PS C:\>  New-AzApiManagementHttpMessageDiagnostic -Headers 'Content-Type', 'UserAgent' -BodyBytes 100

Headers                   Body
-------                   ----
{Content-Type, UserAgent} Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBodyDiagnosticSetting
```

Erstellen einer Http-Nachrichtendiagnoseeinstellung zum Protokollieren und Erstellen von Headern zusammen mit `Content-Type` `User-Agent` 100 Bytes `body`

## PARAMETERS

### -BodyBytesToLog
Anzahl der zu protokollierende Anforderungstextbytes. Dieser Parameter ist optional.

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

### -HeadersToLog
Das Array der zu protokollierenden Überschriften. Dieser Parameter ist optional.

```yaml
Type: System.String[]
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

### Keine

## AUSGABEN

### Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementHttpMessageDiagnostic

## HINWEISE

## LINKS ZU VERWANDTEN THEMEN

[New-AzApiManagementDiagnostic](./New-AzApiManagementDiagnostic.md)

[New-AzApiManagementSamplingSetting](./New-AzApiManagementHttpMessageDiagnostic.md)