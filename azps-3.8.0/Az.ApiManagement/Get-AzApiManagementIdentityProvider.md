---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementidentityprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementIdentityProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementIdentityProvider.md
ms.openlocfilehash: 75525d3c77c3e2113c0e3cff5a7741ab916d7485
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93996635"
---
# <span data-ttu-id="b321c-101">Get-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="b321c-101">Get-AzApiManagementIdentityProvider</span></span>

## <span data-ttu-id="b321c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b321c-102">SYNOPSIS</span></span>
<span data-ttu-id="b321c-103">Rufen Sie die Konfigurationsdetails des Identitätsanbieters ab.</span><span class="sxs-lookup"><span data-stu-id="b321c-103">Get the identity provider configuration details.</span></span>

## <span data-ttu-id="b321c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b321c-104">SYNTAX</span></span>

### <span data-ttu-id="b321c-105">AllIdentityProviders (Standard)</span><span class="sxs-lookup"><span data-stu-id="b321c-105">AllIdentityProviders (Default)</span></span>
```
Get-AzApiManagementIdentityProvider -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b321c-106">IdentityProviderByType</span><span class="sxs-lookup"><span data-stu-id="b321c-106">IdentityProviderByType</span></span>
```
Get-AzApiManagementIdentityProvider -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b321c-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b321c-107">DESCRIPTION</span></span>
<span data-ttu-id="b321c-108">Rufen Sie die Konfigurationsdetails des Identitätsanbieters ab.</span><span class="sxs-lookup"><span data-stu-id="b321c-108">Get the identity provider configuration details.</span></span>

## <span data-ttu-id="b321c-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b321c-109">EXAMPLES</span></span>

### <span data-ttu-id="b321c-110">Beispiel 1: Abrufen aller Identitätsanbieter</span><span class="sxs-lookup"><span data-stu-id="b321c-110">Example 1: Get all Identity Providers</span></span>

```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementIdentityProvider -Context $apimContext
```

<span data-ttu-id="b321c-111">Rufen Sie alle Identität Anbieterkonfiguration für den Dienst ab.</span><span class="sxs-lookup"><span data-stu-id="b321c-111">Get all the identity provider Configuration on the service.</span></span>

### <span data-ttu-id="b321c-112">Beispiel 2: Abrufen des Aad-Identitätsanbieters</span><span class="sxs-lookup"><span data-stu-id="b321c-112">Example 2: Get the AAD Type Identity Provider</span></span>
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

<span data-ttu-id="b321c-113">Ruft die Identität Anbieterkonfiguration von Azure Active Directory ab.</span><span class="sxs-lookup"><span data-stu-id="b321c-113">Gets the Identity Provider Configuration of Azure Active Directory.</span></span>

### <span data-ttu-id="b321c-114">Beispiel 3: Abrufen des Aad B2C-Identitätsanbieters</span><span class="sxs-lookup"><span data-stu-id="b321c-114">Example 3: Get the AAD B2C Type Identity Provider</span></span>
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

<span data-ttu-id="b321c-115">Ruft die Identität Anbieterkonfiguration von Azure Active Directory ab.</span><span class="sxs-lookup"><span data-stu-id="b321c-115">Gets the Identity Provider Configuration of Azure Active Directory.</span></span>

## <span data-ttu-id="b321c-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="b321c-116">PARAMETERS</span></span>

### <span data-ttu-id="b321c-117">-Context</span><span class="sxs-lookup"><span data-stu-id="b321c-117">-Context</span></span>
<span data-ttu-id="b321c-118">Instanz von PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="b321c-118">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="b321c-119">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="b321c-119">This parameter is required.</span></span>

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

### <span data-ttu-id="b321c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b321c-120">-DefaultProfile</span></span>
<span data-ttu-id="b321c-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b321c-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b321c-122">-Typ</span><span class="sxs-lookup"><span data-stu-id="b321c-122">-Type</span></span>
<span data-ttu-id="b321c-123">Bezeichner eines Identitätsanbieters.</span><span class="sxs-lookup"><span data-stu-id="b321c-123">Identifier of a Identity Provider.</span></span>
<span data-ttu-id="b321c-124">Wenn angegeben, wird versucht, die Konfiguration des Identitätsanbieters anhand des Bezeichners zu finden.</span><span class="sxs-lookup"><span data-stu-id="b321c-124">If specified will try to find identity provider configuration by the identifier.</span></span>
<span data-ttu-id="b321c-125">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="b321c-125">This parameter is optional.</span></span>

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

### <span data-ttu-id="b321c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b321c-126">CommonParameters</span></span>
<span data-ttu-id="b321c-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b321c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b321c-128">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b321c-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b321c-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b321c-129">INPUTS</span></span>

### <span data-ttu-id="b321c-130">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="b321c-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="b321c-131">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementIdentityProviderType</span><span class="sxs-lookup"><span data-stu-id="b321c-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType</span></span>

## <span data-ttu-id="b321c-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b321c-132">OUTPUTS</span></span>

### <span data-ttu-id="b321c-133">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="b321c-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProvider</span></span>

## <span data-ttu-id="b321c-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="b321c-134">NOTES</span></span>

## <span data-ttu-id="b321c-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b321c-135">RELATED LINKS</span></span>
