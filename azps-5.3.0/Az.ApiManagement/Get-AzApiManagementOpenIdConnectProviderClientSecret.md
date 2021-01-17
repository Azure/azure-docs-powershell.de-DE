---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementopenidconnectproviderclientsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementOpenIdConnectProviderClientSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementOpenIdConnectProviderClientSecret.md
ms.openlocfilehash: dcc66b6d28157ff9d5551e2fdf0cab18f7727828
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98471472"
---
# <span data-ttu-id="ab146-101">Get-AzApiManagementOpenIdConnectProviderClientSecret</span><span class="sxs-lookup"><span data-stu-id="ab146-101">Get-AzApiManagementOpenIdConnectProviderClientSecret</span></span>

## <span data-ttu-id="ab146-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ab146-102">SYNOPSIS</span></span>
<span data-ttu-id="ab146-103">Ruft den geheimen Schlüssel des OpenID Connect-Anbieters ab.</span><span class="sxs-lookup"><span data-stu-id="ab146-103">Gets OpenID Connect provider client secret.</span></span>

## <span data-ttu-id="ab146-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ab146-104">SYNTAX</span></span>

```
Get-AzApiManagementOpenIdConnectProviderClientSecret -Context <PsApiManagementContext>
 -OpenIdConnectProviderId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ab146-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ab146-105">DESCRIPTION</span></span>
<span data-ttu-id="ab146-106">Ruft den geheimen Schlüssel des OpenID Connect-Anbieters ab.</span><span class="sxs-lookup"><span data-stu-id="ab146-106">Gets OpenID Connect provider client secret.</span></span>

## <span data-ttu-id="ab146-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ab146-107">EXAMPLES</span></span>

### <span data-ttu-id="ab146-108">Beispiel 1: Erhalten eines geheimen Anbieterclients mithilfe einer ID</span><span class="sxs-lookup"><span data-stu-id="ab146-108">Example 1: Get a provider client secret by using an ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementOpenIdConnectProviderClientSecret -Context $apimContext -OpenIdConnectProviderId "OICProvider01"
```

<span data-ttu-id="ab146-109">Dieser Befehl ruft einen geheimen Clientgeheimnis des Anbieters ab, der die ID OICProvider01 besitzt.</span><span class="sxs-lookup"><span data-stu-id="ab146-109">This command gets a client secret of the provider that has the ID OICProvider01.</span></span>

## <span data-ttu-id="ab146-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ab146-110">PARAMETERS</span></span>

### <span data-ttu-id="ab146-111">-Context</span><span class="sxs-lookup"><span data-stu-id="ab146-111">-Context</span></span>
<span data-ttu-id="ab146-112">Instanz von PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="ab146-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="ab146-113">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="ab146-113">This parameter is required.</span></span>

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

### <span data-ttu-id="ab146-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab146-114">-DefaultProfile</span></span>
<span data-ttu-id="ab146-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ab146-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ab146-116">-OpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="ab146-116">-OpenIdConnectProviderId</span></span>
<span data-ttu-id="ab146-117">Id eines OpenID Connect-Anbieters.</span><span class="sxs-lookup"><span data-stu-id="ab146-117">Identifier of a OpenID Connect Provider.</span></span>
<span data-ttu-id="ab146-118">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="ab146-118">This parameter is required.</span></span>

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

### <span data-ttu-id="ab146-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab146-119">CommonParameters</span></span>
<span data-ttu-id="ab146-120">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ab146-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab146-121">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ab146-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab146-122">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ab146-122">INPUTS</span></span>

### <span data-ttu-id="ab146-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="ab146-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="ab146-124">System.String</span><span class="sxs-lookup"><span data-stu-id="ab146-124">System.String</span></span>

## <span data-ttu-id="ab146-125">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ab146-125">OUTPUTS</span></span>

### <span data-ttu-id="ab146-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementClientSecret</span><span class="sxs-lookup"><span data-stu-id="ab146-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementClientSecret</span></span>

## <span data-ttu-id="ab146-127">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="ab146-127">NOTES</span></span>

## <span data-ttu-id="ab146-128">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="ab146-128">RELATED LINKS</span></span>
