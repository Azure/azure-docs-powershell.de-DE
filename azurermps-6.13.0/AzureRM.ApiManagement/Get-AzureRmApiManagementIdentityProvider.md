---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementidentityprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementIdentityProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementIdentityProvider.md
ms.openlocfilehash: 88147f9f26ecd31af1963c5ab378bb00262ef2ae
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663399"
---
# Get-AzureRmApiManagementIdentityProvider

## Synopsis
Rufen Sie die Konfigurationsdetails des Identitätsanbieters ab.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

### AllIdentityProviders (Standard)
```
Get-AzureRmApiManagementIdentityProvider -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### IdentityProviderByType
```
Get-AzureRmApiManagementIdentityProvider -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Rufen Sie die Konfigurationsdetails des Identitätsanbieters ab.

## Beispiele

### Beispiel 1: Abrufen aller Identitätsanbieter

```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementIdentityProvider -Context $apimContext
```

Rufen Sie alle Identität Anbieterkonfiguration für den Dienst ab.

### Abrufen des Aad-Typ-Identitätsanbieters
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementIdentityProvider -Context $apimContext -Type Aad
```

Ruft die Identität Anbieterkonfiguration von Azure Active Directory ab.

## Parameter

### -Context
Instanz von PsApiManagementContext.
Dieser Parameter ist erforderlich.

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

### -Typ
Bezeichner eines Identitätsanbieters.
Wenn angegeben, wird versucht, die Konfiguration des Identitätsanbieters anhand des Bezeichners zu finden.
Dieser Parameter ist optional.

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType
Parameter Sets: IdentityProviderByType
Aliases:
Accepted values: Facebook, Google, Microsoft, Twitter, Aad, AadB2C

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext

### Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementIdentityProviderType

## Ausgaben

### Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementIdentityProvider

## Notizen

## Verwandte Links
