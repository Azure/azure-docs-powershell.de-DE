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
# <span data-ttu-id="0078b-101">Get-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="0078b-101">Get-AzureRmApiManagementIdentityProvider</span></span>

## <span data-ttu-id="0078b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0078b-102">SYNOPSIS</span></span>
<span data-ttu-id="0078b-103">Rufen Sie die Konfigurationsdetails des Identitätsanbieters ab.</span><span class="sxs-lookup"><span data-stu-id="0078b-103">Get the identity provider configuration details.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0078b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0078b-104">SYNTAX</span></span>

### <span data-ttu-id="0078b-105">AllIdentityProviders (Standard)</span><span class="sxs-lookup"><span data-stu-id="0078b-105">AllIdentityProviders (Default)</span></span>
```
Get-AzureRmApiManagementIdentityProvider -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0078b-106">IdentityProviderByType</span><span class="sxs-lookup"><span data-stu-id="0078b-106">IdentityProviderByType</span></span>
```
Get-AzureRmApiManagementIdentityProvider -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0078b-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0078b-107">DESCRIPTION</span></span>
<span data-ttu-id="0078b-108">Rufen Sie die Konfigurationsdetails des Identitätsanbieters ab.</span><span class="sxs-lookup"><span data-stu-id="0078b-108">Get the identity provider configuration details.</span></span>

## <span data-ttu-id="0078b-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0078b-109">EXAMPLES</span></span>

### <span data-ttu-id="0078b-110">Beispiel 1: Abrufen aller Identitätsanbieter</span><span class="sxs-lookup"><span data-stu-id="0078b-110">Example 1: Get all Identity Providers</span></span>

```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementIdentityProvider -Context $apimContext
```

<span data-ttu-id="0078b-111">Rufen Sie alle Identität Anbieterkonfiguration für den Dienst ab.</span><span class="sxs-lookup"><span data-stu-id="0078b-111">Get all the identity provider Configuration on the service.</span></span>

### <span data-ttu-id="0078b-112">Abrufen des Aad-Typ-Identitätsanbieters</span><span class="sxs-lookup"><span data-stu-id="0078b-112">Get the AAD Type Identity Provider</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementIdentityProvider -Context $apimContext -Type Aad
```

<span data-ttu-id="0078b-113">Ruft die Identität Anbieterkonfiguration von Azure Active Directory ab.</span><span class="sxs-lookup"><span data-stu-id="0078b-113">Gets the Identity Provider Configuration of Azure Active Directory.</span></span>

## <span data-ttu-id="0078b-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="0078b-114">PARAMETERS</span></span>

### <span data-ttu-id="0078b-115">-Context</span><span class="sxs-lookup"><span data-stu-id="0078b-115">-Context</span></span>
<span data-ttu-id="0078b-116">Instanz von PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="0078b-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="0078b-117">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="0078b-117">This parameter is required.</span></span>

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

### <span data-ttu-id="0078b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0078b-118">-DefaultProfile</span></span>
<span data-ttu-id="0078b-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0078b-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0078b-120">-Typ</span><span class="sxs-lookup"><span data-stu-id="0078b-120">-Type</span></span>
<span data-ttu-id="0078b-121">Bezeichner eines Identitätsanbieters.</span><span class="sxs-lookup"><span data-stu-id="0078b-121">Identifier of a Identity Provider.</span></span>
<span data-ttu-id="0078b-122">Wenn angegeben, wird versucht, die Konfiguration des Identitätsanbieters anhand des Bezeichners zu finden.</span><span class="sxs-lookup"><span data-stu-id="0078b-122">If specified will try to find identity provider configuration by the identifier.</span></span>
<span data-ttu-id="0078b-123">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="0078b-123">This parameter is optional.</span></span>

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

### <span data-ttu-id="0078b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0078b-124">CommonParameters</span></span>
<span data-ttu-id="0078b-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0078b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0078b-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0078b-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0078b-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0078b-127">INPUTS</span></span>

### <span data-ttu-id="0078b-128">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="0078b-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="0078b-129">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementIdentityProviderType</span><span class="sxs-lookup"><span data-stu-id="0078b-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType</span></span>

## <span data-ttu-id="0078b-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0078b-130">OUTPUTS</span></span>

### <span data-ttu-id="0078b-131">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="0078b-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProvider</span></span>

## <span data-ttu-id="0078b-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="0078b-132">NOTES</span></span>

## <span data-ttu-id="0078b-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0078b-133">RELATED LINKS</span></span>
