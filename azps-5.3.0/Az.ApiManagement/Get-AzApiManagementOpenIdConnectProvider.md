---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 15B6EAE2-56ED-4A01-B8EA-52B9FCDC1F66
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementopenidconnectprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementOpenIdConnectProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementOpenIdConnectProvider.md
ms.openlocfilehash: 6968b4ea1b222d0f046611f10e65f8073a4ba86a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98471473"
---
# <span data-ttu-id="42280-101">Get-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="42280-101">Get-AzApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="42280-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="42280-102">SYNOPSIS</span></span>
<span data-ttu-id="42280-103">Ruft OpenID Connect-Anbieter ab.</span><span class="sxs-lookup"><span data-stu-id="42280-103">Gets OpenID Connect providers.</span></span>

## <span data-ttu-id="42280-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="42280-104">SYNTAX</span></span>

### <span data-ttu-id="42280-105">GetAllOpenIdConnectProviders (Standard)</span><span class="sxs-lookup"><span data-stu-id="42280-105">GetAllOpenIdConnectProviders (Default)</span></span>
```
Get-AzApiManagementOpenIdConnectProvider -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="42280-106">GetByOpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="42280-106">GetByOpenIdConnectProviderId</span></span>
```
Get-AzApiManagementOpenIdConnectProvider -Context <PsApiManagementContext> [-OpenIdConnectProviderId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="42280-107">GetByName</span><span class="sxs-lookup"><span data-stu-id="42280-107">GetByName</span></span>
```
Get-AzApiManagementOpenIdConnectProvider -Context <PsApiManagementContext> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="42280-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="42280-108">DESCRIPTION</span></span>
<span data-ttu-id="42280-109">Das **Cmdlet "Get-AzApiManagementOpenIdConnectProvider"** ruft OpenID Connect-Anbieter in Azure API Management ab.</span><span class="sxs-lookup"><span data-stu-id="42280-109">The **Get-AzApiManagementOpenIdConnectProvider** cmdlet gets OpenID Connect providers in Azure API Management.</span></span>
<span data-ttu-id="42280-110">ClientSecret wird nicht in die Ergebnisdetails eingeschlossen.</span><span class="sxs-lookup"><span data-stu-id="42280-110">ClientSecret will not be included into result details.</span></span> <span data-ttu-id="42280-111">Um den geheimen Clientgeheimnis zu erhalten, verwenden **Sie "Get-AzApiManagementOpenIdConnectProviderClientSecret".**</span><span class="sxs-lookup"><span data-stu-id="42280-111">To get client secret, use **Get-AzApiManagementOpenIdConnectProviderClientSecret**.</span></span>

## <span data-ttu-id="42280-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="42280-112">EXAMPLES</span></span>

### <span data-ttu-id="42280-113">Beispiel 1: Alle Anbieter erhalten</span><span class="sxs-lookup"><span data-stu-id="42280-113">Example 1: Get all providers</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementOpenIdConnectProvider -Context $apimContext
```

<span data-ttu-id="42280-114">Dieser Befehl ruft alle OpenID Connect-Anbieter für den angegebenen Kontext ab.</span><span class="sxs-lookup"><span data-stu-id="42280-114">This command gets all OpenID Connect providers for the specified context.</span></span>

### <span data-ttu-id="42280-115">Beispiel 2: Erhalten eines Anbieters mithilfe einer ID</span><span class="sxs-lookup"><span data-stu-id="42280-115">Example 2: Get a provider by using an ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementOpenIdConnectProvider -Context $apimContext -OpenIdConnectProviderId "OICProvider01"
```

<span data-ttu-id="42280-116">Dieser Befehl ruft den Anbieter ab, der die ID OICProvider01 besitzt.</span><span class="sxs-lookup"><span data-stu-id="42280-116">This command gets the provider that has the ID OICProvider01.</span></span>

### <span data-ttu-id="42280-117">Beispiel 3: Erhalten eines Anbieters mithilfe eines Namens</span><span class="sxs-lookup"><span data-stu-id="42280-117">Example 3: Get a provider by using a name</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementOpenIdConnectProvider -Context $apimContext -Name "Contoso OpenID Connect Provider"
```

<span data-ttu-id="42280-118">Dieser Befehl ruft den Anbieter "Contoso OpenID Connect Provider" ab.</span><span class="sxs-lookup"><span data-stu-id="42280-118">This command gets the provider named Contoso OpenID Connect Provider.</span></span>

## <span data-ttu-id="42280-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="42280-119">PARAMETERS</span></span>

### <span data-ttu-id="42280-120">-Context</span><span class="sxs-lookup"><span data-stu-id="42280-120">-Context</span></span>
<span data-ttu-id="42280-121">Gibt ein **"PsApiManagementContext"-Objekt** an.</span><span class="sxs-lookup"><span data-stu-id="42280-121">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="42280-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42280-122">-DefaultProfile</span></span>
<span data-ttu-id="42280-123">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="42280-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="42280-124">-Name</span><span class="sxs-lookup"><span data-stu-id="42280-124">-Name</span></span>
<span data-ttu-id="42280-125">Gibt den Anzeigenamen eines Anbieters an.</span><span class="sxs-lookup"><span data-stu-id="42280-125">Specifies a friendly name of a provider.</span></span>
<span data-ttu-id="42280-126">Wenn Sie einen Namen angeben, ruft dieses Cmdlet diesen Anbieter ab.</span><span class="sxs-lookup"><span data-stu-id="42280-126">If you specify a name, this cmdlet gets that provider.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42280-127">-OpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="42280-127">-OpenIdConnectProviderId</span></span>
<span data-ttu-id="42280-128">Gibt die ID des Anbieters an, den dieses Cmdlet entfernt.</span><span class="sxs-lookup"><span data-stu-id="42280-128">Specifies an ID of the provider that this cmdlet removes.</span></span>
<span data-ttu-id="42280-129">Wenn Sie eine ID angeben, ruft dieses Cmdlet diesen Anbieter ab.</span><span class="sxs-lookup"><span data-stu-id="42280-129">If you specify an ID, this cmdlet gets that provider.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByOpenIdConnectProviderId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42280-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42280-130">CommonParameters</span></span>
<span data-ttu-id="42280-131">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="42280-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42280-132">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="42280-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42280-133">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="42280-133">INPUTS</span></span>

### <span data-ttu-id="42280-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="42280-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="42280-135">System.String</span><span class="sxs-lookup"><span data-stu-id="42280-135">System.String</span></span>

## <span data-ttu-id="42280-136">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="42280-136">OUTPUTS</span></span>

### <span data-ttu-id="42280-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="42280-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="42280-138">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="42280-138">NOTES</span></span>

## <span data-ttu-id="42280-139">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="42280-139">RELATED LINKS</span></span>

[<span data-ttu-id="42280-140">New-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="42280-140">New-AzApiManagementOpenIdConnectProvider</span></span>](./New-AzApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="42280-141">Remove-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="42280-141">Remove-AzApiManagementOpenIdConnectProvider</span></span>](./Remove-AzApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="42280-142">Set-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="42280-142">Set-AzApiManagementOpenIdConnectProvider</span></span>](./Set-AzApiManagementOpenIdConnectProvider.md)


