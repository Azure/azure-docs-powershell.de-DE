---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementidentityprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementIdentityProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementIdentityProvider.md
ms.openlocfilehash: b267fc854127c1cb098481ac483a7572c8b2e12f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98289552"
---
# <span data-ttu-id="b1279-101">Get-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="b1279-101">Get-AzApiManagementIdentityProvider</span></span>

## <span data-ttu-id="b1279-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b1279-102">SYNOPSIS</span></span>
<span data-ttu-id="b1279-103">Erhalten Sie die Konfigurationsdetails des Identitätsanbieters.</span><span class="sxs-lookup"><span data-stu-id="b1279-103">Get the identity provider configuration details.</span></span>

## <span data-ttu-id="b1279-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b1279-104">SYNTAX</span></span>

### <span data-ttu-id="b1279-105">AllIdentityProviders (Standard)</span><span class="sxs-lookup"><span data-stu-id="b1279-105">AllIdentityProviders (Default)</span></span>
```
Get-AzApiManagementIdentityProvider -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b1279-106">IdentityProviderByType</span><span class="sxs-lookup"><span data-stu-id="b1279-106">IdentityProviderByType</span></span>
```
Get-AzApiManagementIdentityProvider -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b1279-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b1279-107">DESCRIPTION</span></span>
<span data-ttu-id="b1279-108">Erhalten Sie die Konfigurationsdetails des Identitätsanbieters.</span><span class="sxs-lookup"><span data-stu-id="b1279-108">Get the identity provider configuration details.</span></span>
<span data-ttu-id="b1279-109">ClientSecret wird nicht in die Ergebnisdetails eingeschlossen.</span><span class="sxs-lookup"><span data-stu-id="b1279-109">ClientSecret will not be included into result details.</span></span> <span data-ttu-id="b1279-110">Um den geheimen Clientgeheimnis zu erhalten, **verwenden Sie "Get-AzApiManagementIdentityProviderClientSecret".**</span><span class="sxs-lookup"><span data-stu-id="b1279-110">To get client secret, use **Get-AzApiManagementIdentityProviderClientSecret**.</span></span>

## <span data-ttu-id="b1279-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b1279-111">EXAMPLES</span></span>

### <span data-ttu-id="b1279-112">Beispiel 1: Alle Identitätsanbieter erhalten</span><span class="sxs-lookup"><span data-stu-id="b1279-112">Example 1: Get all Identity Providers</span></span>

```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementIdentityProvider -Context $apimContext
```

<span data-ttu-id="b1279-113">Holen Sie sich die Konfiguration des Identitätsanbieters für den Dienst.</span><span class="sxs-lookup"><span data-stu-id="b1279-113">Get all the identity provider Configuration on the service.</span></span>

### <span data-ttu-id="b1279-114">Beispiel 2: Holen Sie sich den AAD-Typidentitätsanbieter.</span><span class="sxs-lookup"><span data-stu-id="b1279-114">Example 2: Get the AAD Type Identity Provider</span></span>
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

<span data-ttu-id="b1279-115">Ruft die Konfiguration des Identitätsanbieters von Azure Active Directory ab.</span><span class="sxs-lookup"><span data-stu-id="b1279-115">Gets the Identity Provider Configuration of Azure Active Directory.</span></span>

### <span data-ttu-id="b1279-116">Beispiel 3: Den AAD B2C-Typidentitätsanbieter erhalten</span><span class="sxs-lookup"><span data-stu-id="b1279-116">Example 3: Get the AAD B2C Type Identity Provider</span></span>
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

<span data-ttu-id="b1279-117">Ruft die Konfiguration des Identitätsanbieters von Azure Active Directory ab.</span><span class="sxs-lookup"><span data-stu-id="b1279-117">Gets the Identity Provider Configuration of Azure Active Directory.</span></span>

## <span data-ttu-id="b1279-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b1279-118">PARAMETERS</span></span>

### <span data-ttu-id="b1279-119">-Context</span><span class="sxs-lookup"><span data-stu-id="b1279-119">-Context</span></span>
<span data-ttu-id="b1279-120">Instanz von PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="b1279-120">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="b1279-121">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="b1279-121">This parameter is required.</span></span>

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

### <span data-ttu-id="b1279-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1279-122">-DefaultProfile</span></span>
<span data-ttu-id="b1279-123">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b1279-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b1279-124">-Type</span><span class="sxs-lookup"><span data-stu-id="b1279-124">-Type</span></span>
<span data-ttu-id="b1279-125">Id eines Identitätsanbieters.</span><span class="sxs-lookup"><span data-stu-id="b1279-125">Identifier of a Identity Provider.</span></span>
<span data-ttu-id="b1279-126">Bei Angabe wird versucht, die Konfiguration des Identitätsanbieters nach dem Bezeichner zu finden.</span><span class="sxs-lookup"><span data-stu-id="b1279-126">If specified will try to find identity provider configuration by the identifier.</span></span>
<span data-ttu-id="b1279-127">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="b1279-127">This parameter is optional.</span></span>

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

### <span data-ttu-id="b1279-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1279-128">CommonParameters</span></span>
<span data-ttu-id="b1279-129">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b1279-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1279-130">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b1279-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1279-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b1279-131">INPUTS</span></span>

### <span data-ttu-id="b1279-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="b1279-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="b1279-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType</span><span class="sxs-lookup"><span data-stu-id="b1279-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType</span></span>

## <span data-ttu-id="b1279-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b1279-134">OUTPUTS</span></span>

### <span data-ttu-id="b1279-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="b1279-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProvider</span></span>

## <span data-ttu-id="b1279-136">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="b1279-136">NOTES</span></span>

## <span data-ttu-id="b1279-137">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="b1279-137">RELATED LINKS</span></span>
