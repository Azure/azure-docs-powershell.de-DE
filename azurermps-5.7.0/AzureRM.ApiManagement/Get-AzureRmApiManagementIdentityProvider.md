---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementidentityprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementIdentityProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementIdentityProvider.md
ms.openlocfilehash: e25e3bfad6c40b136c3cbaa65999b8118e0abd11
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500630"
---
# <span data-ttu-id="56320-101">Get-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="56320-101">Get-AzureRmApiManagementIdentityProvider</span></span>

## <span data-ttu-id="56320-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="56320-102">SYNOPSIS</span></span>
<span data-ttu-id="56320-103">Rufen Sie die Konfigurationsdetails des Identitätsanbieters ab.</span><span class="sxs-lookup"><span data-stu-id="56320-103">Get the identity provider configuration details.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="56320-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="56320-104">SYNTAX</span></span>

### <span data-ttu-id="56320-105">AllIdentityProviders (Standard)</span><span class="sxs-lookup"><span data-stu-id="56320-105">AllIdentityProviders (Default)</span></span>
```
Get-AzureRmApiManagementIdentityProvider -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="56320-106">IdentityProviderByType</span><span class="sxs-lookup"><span data-stu-id="56320-106">IdentityProviderByType</span></span>
```
Get-AzureRmApiManagementIdentityProvider -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="56320-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="56320-107">DESCRIPTION</span></span>
<span data-ttu-id="56320-108">Rufen Sie die Konfigurationsdetails des Identitätsanbieters ab.</span><span class="sxs-lookup"><span data-stu-id="56320-108">Get the identity provider configuration details.</span></span>

## <span data-ttu-id="56320-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="56320-109">EXAMPLES</span></span>

### <span data-ttu-id="56320-110">Beispiel 1: Abrufen aller Identitätsanbieter</span><span class="sxs-lookup"><span data-stu-id="56320-110">Example 1: Get all Identity Providers</span></span>

```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementIdentityProvider -Context $apimContext
```

<span data-ttu-id="56320-111">Rufen Sie alle Identität Anbieterkonfiguration für den Dienst ab.</span><span class="sxs-lookup"><span data-stu-id="56320-111">Get all the identity provider Configuration on the service.</span></span>

### <span data-ttu-id="56320-112">Abrufen des Aad-Typ-Identitätsanbieters</span><span class="sxs-lookup"><span data-stu-id="56320-112">Get the AAD Type Identity Provider</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementIdentityProvider -Context $apimContext -Type Aad
```

<span data-ttu-id="56320-113">Ruft die Identität Anbieterkonfiguration von Azure Active Directory ab.</span><span class="sxs-lookup"><span data-stu-id="56320-113">Gets the Identity Provider Configuration of Azure Active Directory.</span></span>

## <span data-ttu-id="56320-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="56320-114">PARAMETERS</span></span>

### <span data-ttu-id="56320-115">-Context</span><span class="sxs-lookup"><span data-stu-id="56320-115">-Context</span></span>
<span data-ttu-id="56320-116">Instanz von PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="56320-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="56320-117">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="56320-117">This parameter is required.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="56320-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56320-118">-DefaultProfile</span></span>
<span data-ttu-id="56320-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="56320-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56320-120">-Typ</span><span class="sxs-lookup"><span data-stu-id="56320-120">-Type</span></span>
<span data-ttu-id="56320-121">Bezeichner eines Identitätsanbieters.</span><span class="sxs-lookup"><span data-stu-id="56320-121">Identifier of a Identity Provider.</span></span>
<span data-ttu-id="56320-122">Wenn angegeben, wird versucht, die Konfiguration des Identitätsanbieters anhand des Bezeichners zu finden.</span><span class="sxs-lookup"><span data-stu-id="56320-122">If specified will try to find identity provider configuration by the identifier.</span></span>
<span data-ttu-id="56320-123">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="56320-123">This parameter is optional.</span></span>

```yaml
Type: PsApiManagementIdentityProviderType
Parameter Sets: IdentityProviderByType
Aliases: 
Accepted values: Facebook, Google, Microsoft, Twitter, Aad

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="56320-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56320-124">CommonParameters</span></span>
<span data-ttu-id="56320-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56320-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56320-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="56320-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56320-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="56320-127">INPUTS</span></span>

### <span data-ttu-id="56320-128">Keine</span><span class="sxs-lookup"><span data-stu-id="56320-128">None</span></span>
<span data-ttu-id="56320-129">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="56320-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="56320-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="56320-130">OUTPUTS</span></span>

### <span data-ttu-id="56320-131">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="56320-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProvider</span></span>
<span data-ttu-id="56320-132">Die Details des im API-Verwaltungsdienst konfigurierten Identitätsanbieters.</span><span class="sxs-lookup"><span data-stu-id="56320-132">The details of the Identity Provider configured in API Management service.</span></span>

### <span data-ttu-id="56320-133">IList<Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementIdentityProvider></span><span class="sxs-lookup"><span data-stu-id="56320-133">IList<Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProvider></span></span>
<span data-ttu-id="56320-134">Die Liste der im API-Verwaltungsdienst konfigurierten Identitätsanbieter.</span><span class="sxs-lookup"><span data-stu-id="56320-134">The list of Identity Providers configured in API Management service.</span></span>

## <span data-ttu-id="56320-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="56320-135">NOTES</span></span>

## <span data-ttu-id="56320-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="56320-136">RELATED LINKS</span></span>

