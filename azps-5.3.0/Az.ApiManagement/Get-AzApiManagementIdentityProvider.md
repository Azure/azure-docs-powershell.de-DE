---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementidentityprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementIdentityProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementIdentityProvider.md
ms.openlocfilehash: b267fc854127c1cb098481ac483a7572c8b2e12f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98471482"
---
# <span data-ttu-id="99134-101">Get-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="99134-101">Get-AzApiManagementIdentityProvider</span></span>

## <span data-ttu-id="99134-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="99134-102">SYNOPSIS</span></span>
<span data-ttu-id="99134-103">Erhalten Sie die Konfigurationsdetails des Identitätsanbieters.</span><span class="sxs-lookup"><span data-stu-id="99134-103">Get the identity provider configuration details.</span></span>

## <span data-ttu-id="99134-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="99134-104">SYNTAX</span></span>

### <span data-ttu-id="99134-105">AllIdentityProviders (Standard)</span><span class="sxs-lookup"><span data-stu-id="99134-105">AllIdentityProviders (Default)</span></span>
```
Get-AzApiManagementIdentityProvider -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="99134-106">IdentityProviderByType</span><span class="sxs-lookup"><span data-stu-id="99134-106">IdentityProviderByType</span></span>
```
Get-AzApiManagementIdentityProvider -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="99134-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="99134-107">DESCRIPTION</span></span>
<span data-ttu-id="99134-108">Erhalten Sie die Konfigurationsdetails des Identitätsanbieters.</span><span class="sxs-lookup"><span data-stu-id="99134-108">Get the identity provider configuration details.</span></span>
<span data-ttu-id="99134-109">ClientSecret wird nicht in die Ergebnisdetails eingeschlossen.</span><span class="sxs-lookup"><span data-stu-id="99134-109">ClientSecret will not be included into result details.</span></span> <span data-ttu-id="99134-110">Um einen geheimen Clientgeheimnis zu erhalten, verwenden **Sie "Get-AzApiManagementIdentityProviderClientSecret".**</span><span class="sxs-lookup"><span data-stu-id="99134-110">To get client secret, use **Get-AzApiManagementIdentityProviderClientSecret**.</span></span>

## <span data-ttu-id="99134-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="99134-111">EXAMPLES</span></span>

### <span data-ttu-id="99134-112">Beispiel 1: Alle Identitätsanbieter erhalten</span><span class="sxs-lookup"><span data-stu-id="99134-112">Example 1: Get all Identity Providers</span></span>

```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementIdentityProvider -Context $apimContext
```

<span data-ttu-id="99134-113">Holen Sie sich die Konfiguration des Identitätsanbieters für den Dienst.</span><span class="sxs-lookup"><span data-stu-id="99134-113">Get all the identity provider Configuration on the service.</span></span>

### <span data-ttu-id="99134-114">Beispiel 2: Holen Sie sich den AAD-Typidentitätsanbieter.</span><span class="sxs-lookup"><span data-stu-id="99134-114">Example 2: Get the AAD Type Identity Provider</span></span>
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

<span data-ttu-id="99134-115">Ruft die Konfiguration des Identitätsanbieters von Azure Active Directory ab.</span><span class="sxs-lookup"><span data-stu-id="99134-115">Gets the Identity Provider Configuration of Azure Active Directory.</span></span>

### <span data-ttu-id="99134-116">Beispiel 3: Den AAD B2C-Typidentitätsanbieter erhalten</span><span class="sxs-lookup"><span data-stu-id="99134-116">Example 3: Get the AAD B2C Type Identity Provider</span></span>
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

<span data-ttu-id="99134-117">Ruft die Identitätsanbieterkonfiguration von Azure Active Directory ab.</span><span class="sxs-lookup"><span data-stu-id="99134-117">Gets the Identity Provider Configuration of Azure Active Directory.</span></span>

## <span data-ttu-id="99134-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="99134-118">PARAMETERS</span></span>

### <span data-ttu-id="99134-119">-Context</span><span class="sxs-lookup"><span data-stu-id="99134-119">-Context</span></span>
<span data-ttu-id="99134-120">Instanz von PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="99134-120">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="99134-121">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="99134-121">This parameter is required.</span></span>

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

### <span data-ttu-id="99134-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99134-122">-DefaultProfile</span></span>
<span data-ttu-id="99134-123">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="99134-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="99134-124">-Type</span><span class="sxs-lookup"><span data-stu-id="99134-124">-Type</span></span>
<span data-ttu-id="99134-125">Id eines Identitätsanbieters.</span><span class="sxs-lookup"><span data-stu-id="99134-125">Identifier of a Identity Provider.</span></span>
<span data-ttu-id="99134-126">Bei Angabe wird versucht, die Konfiguration des Identitätsanbieters nach dem Bezeichner zu finden.</span><span class="sxs-lookup"><span data-stu-id="99134-126">If specified will try to find identity provider configuration by the identifier.</span></span>
<span data-ttu-id="99134-127">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="99134-127">This parameter is optional.</span></span>

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

### <span data-ttu-id="99134-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99134-128">CommonParameters</span></span>
<span data-ttu-id="99134-129">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="99134-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99134-130">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="99134-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99134-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="99134-131">INPUTS</span></span>

### <span data-ttu-id="99134-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="99134-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="99134-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType</span><span class="sxs-lookup"><span data-stu-id="99134-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType</span></span>

## <span data-ttu-id="99134-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="99134-134">OUTPUTS</span></span>

### <span data-ttu-id="99134-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="99134-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProvider</span></span>

## <span data-ttu-id="99134-136">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="99134-136">NOTES</span></span>

## <span data-ttu-id="99134-137">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="99134-137">RELATED LINKS</span></span>
