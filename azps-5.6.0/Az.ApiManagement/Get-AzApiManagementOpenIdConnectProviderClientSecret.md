---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/get-azapimanagementopenidconnectproviderclientsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementOpenIdConnectProviderClientSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementOpenIdConnectProviderClientSecret.md
ms.openlocfilehash: 0c6757b32a81c689b4b9bbc3397fdd52c19ae4bc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101949795"
---
# <span data-ttu-id="0f185-101">Get-AzApiManagementOpenIdConnectProviderClientSecret</span><span class="sxs-lookup"><span data-stu-id="0f185-101">Get-AzApiManagementOpenIdConnectProviderClientSecret</span></span>

## <span data-ttu-id="0f185-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0f185-102">SYNOPSIS</span></span>
<span data-ttu-id="0f185-103">Ruft den geheimen OpenID Connect-Anbieterclient ab.</span><span class="sxs-lookup"><span data-stu-id="0f185-103">Gets OpenID Connect provider client secret.</span></span>

## <span data-ttu-id="0f185-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0f185-104">SYNTAX</span></span>

```
Get-AzApiManagementOpenIdConnectProviderClientSecret -Context <PsApiManagementContext>
 -OpenIdConnectProviderId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0f185-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0f185-105">DESCRIPTION</span></span>
<span data-ttu-id="0f185-106">Ruft den geheimen OpenID Connect-Anbieterclient ab.</span><span class="sxs-lookup"><span data-stu-id="0f185-106">Gets OpenID Connect provider client secret.</span></span>

## <span data-ttu-id="0f185-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="0f185-107">EXAMPLES</span></span>

### <span data-ttu-id="0f185-108">Beispiel 1: Erstellen eines Geheimtipps eines Anbieterclients mithilfe einer ID</span><span class="sxs-lookup"><span data-stu-id="0f185-108">Example 1: Get a provider client secret by using an ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementOpenIdConnectProviderClientSecret -Context $apimContext -OpenIdConnectProviderId "OICProvider01"
```

<span data-ttu-id="0f185-109">Dieser Befehl ruft einen Clientgeheimnis des Anbieters ab, der über die ID OICProvider01 verfügt.</span><span class="sxs-lookup"><span data-stu-id="0f185-109">This command gets a client secret of the provider that has the ID OICProvider01.</span></span>

## <span data-ttu-id="0f185-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="0f185-110">PARAMETERS</span></span>

### <span data-ttu-id="0f185-111">-Context</span><span class="sxs-lookup"><span data-stu-id="0f185-111">-Context</span></span>
<span data-ttu-id="0f185-112">Instanz von PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="0f185-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="0f185-113">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="0f185-113">This parameter is required.</span></span>

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

### <span data-ttu-id="0f185-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f185-114">-DefaultProfile</span></span>
<span data-ttu-id="0f185-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0f185-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0f185-116">-OpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="0f185-116">-OpenIdConnectProviderId</span></span>
<span data-ttu-id="0f185-117">Bezeichner eines OpenID Connect-Anbieters.</span><span class="sxs-lookup"><span data-stu-id="0f185-117">Identifier of a OpenID Connect Provider.</span></span>
<span data-ttu-id="0f185-118">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="0f185-118">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f185-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f185-119">CommonParameters</span></span>
<span data-ttu-id="0f185-120">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0f185-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f185-121">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0f185-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f185-122">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="0f185-122">INPUTS</span></span>

### <span data-ttu-id="0f185-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="0f185-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="0f185-124">System.String</span><span class="sxs-lookup"><span data-stu-id="0f185-124">System.String</span></span>

## <span data-ttu-id="0f185-125">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="0f185-125">OUTPUTS</span></span>

### <span data-ttu-id="0f185-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementClientSecret</span><span class="sxs-lookup"><span data-stu-id="0f185-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementClientSecret</span></span>

## <span data-ttu-id="0f185-127">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="0f185-127">NOTES</span></span>

## <span data-ttu-id="0f185-128">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="0f185-128">RELATED LINKS</span></span>
