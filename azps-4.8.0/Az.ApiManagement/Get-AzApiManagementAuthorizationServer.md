---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 8B0116E5-0AED-4050-BF11-1BFE65DB9436
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementauthorizationserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementAuthorizationServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementAuthorizationServer.md
ms.openlocfilehash: ad06e1f9c37920c2362db3a94cdfbace91bf3796
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94010331"
---
# Get-AzApiManagementAuthorizationServer

## Synopsis
Ruft einen autorisierungsserver für die API-Verwaltung ab.

## Syntax

### ContextParameterSet (Standard)
```
Get-AzApiManagementAuthorizationServer -Context <PsApiManagementContext> [-ServerId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceIdParameterSet
```
Get-AzApiManagementAuthorizationServer [-ServerId <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzApiManagementAuthorizationServer** " ruft alle Azure API-Verwaltungs autorisierungsserver oder den angegebenen autorisierungsserver ab.
ClientSecret wird nicht in Ergebnisdetails eingeschlossen. Verwenden **Sie Get-AzApiManagementAuthorizationServerClientSecret** , um Client Secret zu erhalten.

## Beispiele

### Beispiel 1: Abrufen aller autorisierungsserver
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementAuthorizationServer -Context $ApiMgmtContext
```

Dieser Befehl ruft alle autorisierungsserver für die API-Verwaltung ab.

### Beispiel 2: Abrufen eines angegebenen autorisierungsservers
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementAuthorizationServer -Context $ApiMgmtContext -ServerId "0123456789"
```

Dieser Befehl ruft den angegebenen autorisierungsserver ab.

## Parameter

### -Context

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ContextParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
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

### -Resourcen-Nr
Arm-Ressourcenbezeichner des autorisierungsservers. Wenn angegeben, wird versucht, den autorisierungsserver anhand des Bezeichners zu finden. Dieser Parameter ist erforderlich.

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Server-Nr
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## Eingaben

### Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext

### System. String

## Ausgaben

### Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementOAuth2AuthorizationServer

## Notizen

## Verwandte Links

[Neu – AzApiManagementAuthorizationServer](./New-AzApiManagementAuthorizationServer.md)

[Remove-AzApiManagementAuthorizationServer](./Remove-AzApiManagementAuthorizationServer.md)

[Satz-AzApiManagementAuthorizationServer](./Set-AzApiManagementAuthorizationServer.md)


