---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementidentityproviderclientsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementIdentityProviderClientSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementIdentityProviderClientSecret.md
ms.openlocfilehash: d75d385bc158e0855601d3432dff79b2e4339f2f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98471484"
---
# <span data-ttu-id="ea2b2-101">Get-AzApiManagementIdentityProviderClientSecret</span><span class="sxs-lookup"><span data-stu-id="ea2b2-101">Get-AzApiManagementIdentityProviderClientSecret</span></span>

## <span data-ttu-id="ea2b2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ea2b2-102">SYNOPSIS</span></span>
<span data-ttu-id="ea2b2-103">Holen Sie sich den geheimen Client geheimen Identitätsanbieter.</span><span class="sxs-lookup"><span data-stu-id="ea2b2-103">Get the identity provider client secret.</span></span>

## <span data-ttu-id="ea2b2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ea2b2-104">SYNTAX</span></span>

```
Get-AzApiManagementIdentityProviderClientSecret -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ea2b2-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ea2b2-105">DESCRIPTION</span></span>
<span data-ttu-id="ea2b2-106">Holen Sie sich den geheimen Client geheimen Identitätsanbieter.</span><span class="sxs-lookup"><span data-stu-id="ea2b2-106">Get the identity provider client secret.</span></span>

## <span data-ttu-id="ea2b2-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ea2b2-107">EXAMPLES</span></span>

### <span data-ttu-id="ea2b2-108">Beispiel 1: Den Geheimen Clientgeheimnis des AAD-Typidentitätsanbieters erhalten</span><span class="sxs-lookup"><span data-stu-id="ea2b2-108">Example 1: Get the client secret of AAD Type Identity Provider</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\> Get-AzApiManagementIdentityProviderClientSecret -Context $apimContext -Type Aad
```

<span data-ttu-id="ea2b2-109">Ruft den geheimen Clientgeheimnis der Identitätsanbieterkonfiguration von Azure Active Directory ab.</span><span class="sxs-lookup"><span data-stu-id="ea2b2-109">Gets the client secret of the Identity Provider Configuration of Azure Active Directory.</span></span>

## <span data-ttu-id="ea2b2-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ea2b2-110">PARAMETERS</span></span>

### <span data-ttu-id="ea2b2-111">-Context</span><span class="sxs-lookup"><span data-stu-id="ea2b2-111">-Context</span></span>
<span data-ttu-id="ea2b2-112">Instanz von PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="ea2b2-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="ea2b2-113">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="ea2b2-113">This parameter is required.</span></span>

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

### <span data-ttu-id="ea2b2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea2b2-114">-DefaultProfile</span></span>
<span data-ttu-id="ea2b2-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ea2b2-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ea2b2-116">-Type</span><span class="sxs-lookup"><span data-stu-id="ea2b2-116">-Type</span></span>
<span data-ttu-id="ea2b2-117">Id eines Identitätsanbieters.</span><span class="sxs-lookup"><span data-stu-id="ea2b2-117">Identifier of a Identity Provider.</span></span>
<span data-ttu-id="ea2b2-118">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="ea2b2-118">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType
Parameter Sets: (All)
Aliases:
Accepted values: Facebook, Google, Microsoft, Twitter, Aad, AadB2C

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea2b2-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea2b2-119">CommonParameters</span></span>
<span data-ttu-id="ea2b2-120">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea2b2-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea2b2-121">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ea2b2-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea2b2-122">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ea2b2-122">INPUTS</span></span>

### <span data-ttu-id="ea2b2-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="ea2b2-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="ea2b2-124">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType</span><span class="sxs-lookup"><span data-stu-id="ea2b2-124">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType</span></span>

## <span data-ttu-id="ea2b2-125">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ea2b2-125">OUTPUTS</span></span>

### <span data-ttu-id="ea2b2-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementClientSecret</span><span class="sxs-lookup"><span data-stu-id="ea2b2-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementClientSecret</span></span>

## <span data-ttu-id="ea2b2-127">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="ea2b2-127">NOTES</span></span>

## <span data-ttu-id="ea2b2-128">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="ea2b2-128">RELATED LINKS</span></span>
