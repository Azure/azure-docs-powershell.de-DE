---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/get-azapimanagementidentityprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementIdentityProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementIdentityProvider.md
ms.openlocfilehash: f09dc3079335521f099af5cbd397b6a56a57a7c8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101922571"
---
# <span data-ttu-id="82079-101">Get-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="82079-101">Get-AzApiManagementIdentityProvider</span></span>

## <span data-ttu-id="82079-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="82079-102">SYNOPSIS</span></span>
<span data-ttu-id="82079-103">Hier erhalten Sie die Konfigurationsdetails des Identitätsanbieters.</span><span class="sxs-lookup"><span data-stu-id="82079-103">Get the identity provider configuration details.</span></span>

## <span data-ttu-id="82079-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="82079-104">SYNTAX</span></span>

### <span data-ttu-id="82079-105">AllIdentityProviders (Standard)</span><span class="sxs-lookup"><span data-stu-id="82079-105">AllIdentityProviders (Default)</span></span>
```
Get-AzApiManagementIdentityProvider -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="82079-106">IdentityProviderByType</span><span class="sxs-lookup"><span data-stu-id="82079-106">IdentityProviderByType</span></span>
```
Get-AzApiManagementIdentityProvider -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="82079-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="82079-107">DESCRIPTION</span></span>
<span data-ttu-id="82079-108">Hier erhalten Sie die Konfigurationsdetails des Identitätsanbieters.</span><span class="sxs-lookup"><span data-stu-id="82079-108">Get the identity provider configuration details.</span></span>
<span data-ttu-id="82079-109">ClientSecret wird nicht in ergebnisdetails einbezogen.</span><span class="sxs-lookup"><span data-stu-id="82079-109">ClientSecret will not be included into result details.</span></span> <span data-ttu-id="82079-110">Verwenden Sie **Get-AzApiManagementIdentityProviderClientSecret,** um den Geheimtipp des Clients zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="82079-110">To get client secret, use **Get-AzApiManagementIdentityProviderClientSecret**.</span></span>

## <span data-ttu-id="82079-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="82079-111">EXAMPLES</span></span>

### <span data-ttu-id="82079-112">Beispiel 1: Alle Identitätsanbieter erhalten</span><span class="sxs-lookup"><span data-stu-id="82079-112">Example 1: Get all Identity Providers</span></span>

```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementIdentityProvider -Context $apimContext
```

<span data-ttu-id="82079-113">Alle Identitätsanbieterkonfiguration für den Dienst erhalten.</span><span class="sxs-lookup"><span data-stu-id="82079-113">Get all the identity provider Configuration on the service.</span></span>

### <span data-ttu-id="82079-114">Beispiel 2: Holen Sie sich den AAD-Typidentitätsanbieter</span><span class="sxs-lookup"><span data-stu-id="82079-114">Example 2: Get the AAD Type Identity Provider</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\> Get-AzApiManagementIdentityProvider -Context $apimContext -Type Aad


Type                     : Aad
ClientId                 : aaa
ClientSecret             : xxxxx
AllowedTenants           : {contosotest.onmicrosoft.com}
Authority                : login.microsoftonline.com
SignupPolicyName         :
SigninPolicyName         :
ProfileEditingPolicyName :
PasswordResetPolicyName  :
SigninTenant             :
Id                       : /subscriptions/a200340d-6b82-494d-9dbf-687ba6e33f9e/resourceGroups/Api-Default-West-US/providers/Microsoft.ApiManagement/service/contoso/identityProviders/Aad
ResourceGroupName        : Api-Default-West-US
ServiceName              : contoso
```

<span data-ttu-id="82079-115">Ruft die Konfiguration des Identitätsanbieters von Azure Active Directory ab.</span><span class="sxs-lookup"><span data-stu-id="82079-115">Gets the Identity Provider Configuration of Azure Active Directory.</span></span>

### <span data-ttu-id="82079-116">Beispiel 3: Holen Sie sich den AAD B2C-Typidentitätsanbieter.</span><span class="sxs-lookup"><span data-stu-id="82079-116">Example 3: Get the AAD B2C Type Identity Provider</span></span>
```powershell
PS C:\>$context = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\> Get-AzApiManagementIdentityProvider -Context $context -Type AadB2C


Type                     : AadB2C
ClientId                 : f02dafe2-b8b8-48ec-a38e-27e5c16c51e5
ClientSecret             : xxxxxx
AllowedTenants           : {contosoaadb2c.onmicrosoft.com}
Authority                : login.microsoftonline.com
SignupPolicyName         : B2C_1_policy-signup
SigninPolicyName         : B2C_1_policy-signin
ProfileEditingPolicyName :
PasswordResetPolicyName  :
SigninTenant             : contosoaadb2c.onmicrosoft.com
Id                       : /subscriptions/a200340d-6b82-494d-9dbf-687ba6e33f9e/resourceGroups/Api-Default-West-US/providers/Microsoft.ApiManagement/service/contoso/identityProviders/AadB2C
ResourceGroupName        : Api-Default-West-US
ServiceName              : contoso
```

<span data-ttu-id="82079-117">Ruft die Konfiguration des Identitätsanbieters von Azure Active Directory ab.</span><span class="sxs-lookup"><span data-stu-id="82079-117">Gets the Identity Provider Configuration of Azure Active Directory.</span></span>

## <span data-ttu-id="82079-118">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="82079-118">PARAMETERS</span></span>

### <span data-ttu-id="82079-119">-Context</span><span class="sxs-lookup"><span data-stu-id="82079-119">-Context</span></span>
<span data-ttu-id="82079-120">Instanz von PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="82079-120">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="82079-121">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="82079-121">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="82079-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82079-122">-DefaultProfile</span></span>
<span data-ttu-id="82079-123">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="82079-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="82079-124">-Type</span><span class="sxs-lookup"><span data-stu-id="82079-124">-Type</span></span>
<span data-ttu-id="82079-125">Bezeichner eines Identitätsanbieters.</span><span class="sxs-lookup"><span data-stu-id="82079-125">Identifier of a Identity Provider.</span></span>
<span data-ttu-id="82079-126">Wenn angegeben, wird versucht, die Konfiguration des Identitätsanbieters durch den Bezeichner zu finden.</span><span class="sxs-lookup"><span data-stu-id="82079-126">If specified will try to find identity provider configuration by the identifier.</span></span>
<span data-ttu-id="82079-127">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="82079-127">This parameter is optional.</span></span>

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

### <span data-ttu-id="82079-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82079-128">CommonParameters</span></span>
<span data-ttu-id="82079-129">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="82079-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82079-130">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="82079-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82079-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="82079-131">INPUTS</span></span>

### <span data-ttu-id="82079-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="82079-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="82079-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType</span><span class="sxs-lookup"><span data-stu-id="82079-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType</span></span>

## <span data-ttu-id="82079-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="82079-134">OUTPUTS</span></span>

### <span data-ttu-id="82079-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="82079-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProvider</span></span>

## <span data-ttu-id="82079-136">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="82079-136">NOTES</span></span>

## <span data-ttu-id="82079-137">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="82079-137">RELATED LINKS</span></span>
