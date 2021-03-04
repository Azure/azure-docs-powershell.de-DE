---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/get-azapimanagementgatewayhostnameconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGatewayHostnameConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGatewayHostnameConfiguration.md
ms.openlocfilehash: 27e833c526dea1b8df6451671ae2fd142c00b6e1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101933280"
---
# <span data-ttu-id="f9d19-101">Get-AzApiManagementGatewayHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="f9d19-101">Get-AzApiManagementGatewayHostnameConfiguration</span></span>

## <span data-ttu-id="f9d19-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f9d19-102">SYNOPSIS</span></span>
<span data-ttu-id="f9d19-103">Ruft alle oder bestimmte Hostnamenkonfigurationen für das vorhandene Gateway ab.</span><span class="sxs-lookup"><span data-stu-id="f9d19-103">Gets all or specific hostname configuration for the existing Gateway.</span></span>

## <span data-ttu-id="f9d19-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f9d19-104">SYNTAX</span></span>

### <span data-ttu-id="f9d19-105">GetByGatewayId (Standard)</span><span class="sxs-lookup"><span data-stu-id="f9d19-105">GetByGatewayId (Default)</span></span>
```
Get-AzApiManagementGatewayHostnameConfiguration -Context <PsApiManagementContext> -GatewayId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f9d19-106">GetByGatewayHostnameId</span><span class="sxs-lookup"><span data-stu-id="f9d19-106">GetByGatewayHostnameId</span></span>
```
Get-AzApiManagementGatewayHostnameConfiguration -Context <PsApiManagementContext> -GatewayId <String>
 -GatewayHostnameConfigurationId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f9d19-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f9d19-107">DESCRIPTION</span></span>
<span data-ttu-id="f9d19-108">Das **Get-AzApiManagementGatewayHostnameConfiguration-Cmdlet** ruft alle oder bestimmte Hostnamenkonfigurationen für das vorhandene Gateway ab.</span><span class="sxs-lookup"><span data-stu-id="f9d19-108">The **Get-AzApiManagementGatewayHostnameConfiguration** cmdlet gets all or specific hostname configuration for the existing Gateway.</span></span>

## <span data-ttu-id="f9d19-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f9d19-109">EXAMPLES</span></span>

### <span data-ttu-id="f9d19-110">Beispiel 1: Alle Hostnamenkonfigurationen für das Gateway erhalten</span><span class="sxs-lookup"><span data-stu-id="f9d19-110">Example 1: Get all hostname configurations for the gateway</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGatewayHostnameConfiguration -Context $apimContext  -GatewayId "0123456789"
```

<span data-ttu-id="f9d19-111">Dieser Befehl ruft alle Hostnamenkonfigurationen für ein "0123456789"-Gateway ab.</span><span class="sxs-lookup"><span data-stu-id="f9d19-111">This command gets all hostname configurations for a "0123456789" gateway.</span></span>

### <span data-ttu-id="f9d19-112">Beispiel 2: Erhalten einer Hostnamenkonfiguration für das Gateway</span><span class="sxs-lookup"><span data-stu-id="f9d19-112">Example 2: Get a hostname configuration for the gateway</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGatewayHostnameConfiguration -Context $apimContext -GatewayId "0123456789" -GatewayHostnameConfigurationId "123"
```

<span data-ttu-id="f9d19-113">Dieser Befehl ruft die Hostnamenkonfiguration "123" für ein Gateway "0123456789" ab.</span><span class="sxs-lookup"><span data-stu-id="f9d19-113">This command gets "123" hostname configuration for a "0123456789" gateway.</span></span>

## <span data-ttu-id="f9d19-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="f9d19-114">PARAMETERS</span></span>

### <span data-ttu-id="f9d19-115">-Context</span><span class="sxs-lookup"><span data-stu-id="f9d19-115">-Context</span></span>
<span data-ttu-id="f9d19-116">Instanz von PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="f9d19-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="f9d19-117">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="f9d19-117">This parameter is required.</span></span>

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

### <span data-ttu-id="f9d19-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9d19-118">-DefaultProfile</span></span>
<span data-ttu-id="f9d19-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f9d19-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f9d19-120">-GatewayHostnameConfigurationId</span><span class="sxs-lookup"><span data-stu-id="f9d19-120">-GatewayHostnameConfigurationId</span></span>
<span data-ttu-id="f9d19-121">Hostname-Konfigurationsbezeichner.</span><span class="sxs-lookup"><span data-stu-id="f9d19-121">Hostname Configuration identifier.</span></span>
<span data-ttu-id="f9d19-122">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="f9d19-122">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByGatewayHostnameId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9d19-123">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="f9d19-123">-GatewayId</span></span>
<span data-ttu-id="f9d19-124">Gatewaybezeichner.</span><span class="sxs-lookup"><span data-stu-id="f9d19-124">Gateway identifier.</span></span>
<span data-ttu-id="f9d19-125">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="f9d19-125">This parameter is required.</span></span>

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

### <span data-ttu-id="f9d19-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9d19-126">CommonParameters</span></span>
<span data-ttu-id="f9d19-127">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f9d19-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9d19-128">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f9d19-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9d19-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f9d19-129">INPUTS</span></span>

### <span data-ttu-id="f9d19-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="f9d19-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="f9d19-131">System.String</span><span class="sxs-lookup"><span data-stu-id="f9d19-131">System.String</span></span>

## <span data-ttu-id="f9d19-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f9d19-132">OUTPUTS</span></span>

### <span data-ttu-id="f9d19-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGatewayHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="f9d19-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGatewayHostnameConfiguration</span></span>

## <span data-ttu-id="f9d19-134">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="f9d19-134">NOTES</span></span>

## <span data-ttu-id="f9d19-135">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="f9d19-135">RELATED LINKS</span></span>
