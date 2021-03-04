---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 15B6EAE2-56ED-4A01-B8EA-52B9FCDC1F66
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/get-azapimanagementopenidconnectprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementOpenIdConnectProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementOpenIdConnectProvider.md
ms.openlocfilehash: 1a46cccc38e1b562786e9eda88f3336430559fc0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101949803"
---
# <span data-ttu-id="90de9-101">Get-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="90de9-101">Get-AzApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="90de9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="90de9-102">SYNOPSIS</span></span>
<span data-ttu-id="90de9-103">Ruft OpenID Connect-Anbieter ab.</span><span class="sxs-lookup"><span data-stu-id="90de9-103">Gets OpenID Connect providers.</span></span>

## <span data-ttu-id="90de9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="90de9-104">SYNTAX</span></span>

### <span data-ttu-id="90de9-105">GetAllOpenIdConnectProviders (Standard)</span><span class="sxs-lookup"><span data-stu-id="90de9-105">GetAllOpenIdConnectProviders (Default)</span></span>
```
Get-AzApiManagementOpenIdConnectProvider -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="90de9-106">GetByOpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="90de9-106">GetByOpenIdConnectProviderId</span></span>
```
Get-AzApiManagementOpenIdConnectProvider -Context <PsApiManagementContext> [-OpenIdConnectProviderId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="90de9-107">GetByName</span><span class="sxs-lookup"><span data-stu-id="90de9-107">GetByName</span></span>
```
Get-AzApiManagementOpenIdConnectProvider -Context <PsApiManagementContext> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="90de9-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="90de9-108">DESCRIPTION</span></span>
<span data-ttu-id="90de9-109">Das **Get-AzApiManagementOpenIdConnectProvider-Cmdlet** ruft OpenID Connect-Anbieter in Azure API Management ab.</span><span class="sxs-lookup"><span data-stu-id="90de9-109">The **Get-AzApiManagementOpenIdConnectProvider** cmdlet gets OpenID Connect providers in Azure API Management.</span></span>
<span data-ttu-id="90de9-110">ClientSecret wird nicht in ergebnisdetails einbezogen.</span><span class="sxs-lookup"><span data-stu-id="90de9-110">ClientSecret will not be included into result details.</span></span> <span data-ttu-id="90de9-111">Verwenden Sie **Get-AzApiManagementOpenIdConnectProviderClientSecret,** um den Geheimtipp des Clients zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="90de9-111">To get client secret, use **Get-AzApiManagementOpenIdConnectProviderClientSecret**.</span></span>

## <span data-ttu-id="90de9-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="90de9-112">EXAMPLES</span></span>

### <span data-ttu-id="90de9-113">Beispiel 1: Alle Anbieter erhalten</span><span class="sxs-lookup"><span data-stu-id="90de9-113">Example 1: Get all providers</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementOpenIdConnectProvider -Context $apimContext
```

<span data-ttu-id="90de9-114">Dieser Befehl ruft alle OpenID Connect-Anbieter für den angegebenen Kontext ab.</span><span class="sxs-lookup"><span data-stu-id="90de9-114">This command gets all OpenID Connect providers for the specified context.</span></span>

### <span data-ttu-id="90de9-115">Beispiel 2: Erstellen eines Anbieters mithilfe einer ID</span><span class="sxs-lookup"><span data-stu-id="90de9-115">Example 2: Get a provider by using an ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementOpenIdConnectProvider -Context $apimContext -OpenIdConnectProviderId "OICProvider01"
```

<span data-ttu-id="90de9-116">Dieser Befehl ruft den Anbieter ab, der über die ID OICProvider01 verfügt.</span><span class="sxs-lookup"><span data-stu-id="90de9-116">This command gets the provider that has the ID OICProvider01.</span></span>

### <span data-ttu-id="90de9-117">Beispiel 3: Erhalten eines Anbieters mithilfe eines Namens</span><span class="sxs-lookup"><span data-stu-id="90de9-117">Example 3: Get a provider by using a name</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementOpenIdConnectProvider -Context $apimContext -Name "Contoso OpenID Connect Provider"
```

<span data-ttu-id="90de9-118">Dieser Befehl ruft den Anbieter namens Contoso OpenID Connect Provider ab.</span><span class="sxs-lookup"><span data-stu-id="90de9-118">This command gets the provider named Contoso OpenID Connect Provider.</span></span>

## <span data-ttu-id="90de9-119">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="90de9-119">PARAMETERS</span></span>

### <span data-ttu-id="90de9-120">-Context</span><span class="sxs-lookup"><span data-stu-id="90de9-120">-Context</span></span>
<span data-ttu-id="90de9-121">Gibt ein **PsApiManagementContext-Objekt** an.</span><span class="sxs-lookup"><span data-stu-id="90de9-121">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="90de9-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90de9-122">-DefaultProfile</span></span>
<span data-ttu-id="90de9-123">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="90de9-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="90de9-124">-Name</span><span class="sxs-lookup"><span data-stu-id="90de9-124">-Name</span></span>
<span data-ttu-id="90de9-125">Gibt einen Anzeigenamen eines Anbieters an.</span><span class="sxs-lookup"><span data-stu-id="90de9-125">Specifies a friendly name of a provider.</span></span>
<span data-ttu-id="90de9-126">Wenn Sie einen Namen angeben, ruft dieses Cmdlet diesen Anbieter ab.</span><span class="sxs-lookup"><span data-stu-id="90de9-126">If you specify a name, this cmdlet gets that provider.</span></span>

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

### <span data-ttu-id="90de9-127">-OpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="90de9-127">-OpenIdConnectProviderId</span></span>
<span data-ttu-id="90de9-128">Gibt eine ID des Anbieters an, den dieses Cmdlet entfernt.</span><span class="sxs-lookup"><span data-stu-id="90de9-128">Specifies an ID of the provider that this cmdlet removes.</span></span>
<span data-ttu-id="90de9-129">Wenn Sie eine ID angeben, ruft dieses Cmdlet diesen Anbieter ab.</span><span class="sxs-lookup"><span data-stu-id="90de9-129">If you specify an ID, this cmdlet gets that provider.</span></span>

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

### <span data-ttu-id="90de9-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90de9-130">CommonParameters</span></span>
<span data-ttu-id="90de9-131">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="90de9-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90de9-132">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="90de9-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90de9-133">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="90de9-133">INPUTS</span></span>

### <span data-ttu-id="90de9-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="90de9-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="90de9-135">System.String</span><span class="sxs-lookup"><span data-stu-id="90de9-135">System.String</span></span>

## <span data-ttu-id="90de9-136">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="90de9-136">OUTPUTS</span></span>

### <span data-ttu-id="90de9-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="90de9-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="90de9-138">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="90de9-138">NOTES</span></span>

## <span data-ttu-id="90de9-139">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="90de9-139">RELATED LINKS</span></span>

[<span data-ttu-id="90de9-140">New-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="90de9-140">New-AzApiManagementOpenIdConnectProvider</span></span>](./New-AzApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="90de9-141">Remove-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="90de9-141">Remove-AzApiManagementOpenIdConnectProvider</span></span>](./Remove-AzApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="90de9-142">Set-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="90de9-142">Set-AzApiManagementOpenIdConnectProvider</span></span>](./Set-AzApiManagementOpenIdConnectProvider.md)


