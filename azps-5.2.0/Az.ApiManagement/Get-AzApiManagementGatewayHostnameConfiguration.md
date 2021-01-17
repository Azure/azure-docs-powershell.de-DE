---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementgatewayhostnameconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGatewayHostnameConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGatewayHostnameConfiguration.md
ms.openlocfilehash: ecdae500b0c1d81635e23ca6ca4bc4c803665912
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98365446"
---
# <span data-ttu-id="2d3c6-101">Get-AzApiManagementGatewayHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="2d3c6-101">Get-AzApiManagementGatewayHostnameConfiguration</span></span>

## <span data-ttu-id="2d3c6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2d3c6-102">SYNOPSIS</span></span>
<span data-ttu-id="2d3c6-103">Ruft die Konfiguration des ganzen oder spezifischen Hostnamens für das vorhandene Gateway ab.</span><span class="sxs-lookup"><span data-stu-id="2d3c6-103">Gets all or specific hostname configuration for the existing Gateway.</span></span>

## <span data-ttu-id="2d3c6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2d3c6-104">SYNTAX</span></span>

### <span data-ttu-id="2d3c6-105">GetByGatewayId (Standard)</span><span class="sxs-lookup"><span data-stu-id="2d3c6-105">GetByGatewayId (Default)</span></span>
```
Get-AzApiManagementGatewayHostnameConfiguration -Context <PsApiManagementContext> -GatewayId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2d3c6-106">GetByGatewayHostnameId</span><span class="sxs-lookup"><span data-stu-id="2d3c6-106">GetByGatewayHostnameId</span></span>
```
Get-AzApiManagementGatewayHostnameConfiguration -Context <PsApiManagementContext> -GatewayId <String>
 -GatewayHostnameConfigurationId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2d3c6-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2d3c6-107">DESCRIPTION</span></span>
<span data-ttu-id="2d3c6-108">Das **Cmdlet "Get-AzApiManagementGatewayHostnameConfiguration"** ruft eine ganz oder eine bestimmte Hostnamenkonfiguration für das vorhandene Gateway ab.</span><span class="sxs-lookup"><span data-stu-id="2d3c6-108">The **Get-AzApiManagementGatewayHostnameConfiguration** cmdlet gets all or specific hostname configuration for the existing Gateway.</span></span>

## <span data-ttu-id="2d3c6-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="2d3c6-109">EXAMPLES</span></span>

### <span data-ttu-id="2d3c6-110">Beispiel 1: Alle Hostnamenkonfigurationen für das Gateway erhalten</span><span class="sxs-lookup"><span data-stu-id="2d3c6-110">Example 1: Get all hostname configurations for the gateway</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGatewayHostnameConfiguration -Context $apimContext  -GatewayId "0123456789"
```

<span data-ttu-id="2d3c6-111">Dieser Befehl ruft alle Hostnamenkonfigurationen für ein "0123456789"-Gateway ab.</span><span class="sxs-lookup"><span data-stu-id="2d3c6-111">This command gets all hostname configurations for a "0123456789" gateway.</span></span>

### <span data-ttu-id="2d3c6-112">Beispiel 2: Erhalten einer Hostnamenkonfiguration für das Gateway</span><span class="sxs-lookup"><span data-stu-id="2d3c6-112">Example 2: Get a hostname configuration for the gateway</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGatewayHostnameConfiguration -Context $apimContext -GatewayId "0123456789" -GatewayHostnameConfigurationId "123"
```

<span data-ttu-id="2d3c6-113">Dieser Befehl ruft die Konfiguration des Hostnamens "123" für ein "0123456789"-Gateway ab.</span><span class="sxs-lookup"><span data-stu-id="2d3c6-113">This command gets "123" hostname configuration for a "0123456789" gateway.</span></span>

## <span data-ttu-id="2d3c6-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2d3c6-114">PARAMETERS</span></span>

### <span data-ttu-id="2d3c6-115">-Context</span><span class="sxs-lookup"><span data-stu-id="2d3c6-115">-Context</span></span>
<span data-ttu-id="2d3c6-116">Instanz von PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="2d3c6-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="2d3c6-117">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="2d3c6-117">This parameter is required.</span></span>

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

### <span data-ttu-id="2d3c6-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d3c6-118">-DefaultProfile</span></span>
<span data-ttu-id="2d3c6-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2d3c6-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2d3c6-120">-GatewayHostnameConfigurationId</span><span class="sxs-lookup"><span data-stu-id="2d3c6-120">-GatewayHostnameConfigurationId</span></span>
<span data-ttu-id="2d3c6-121">Hostname-Konfigurations-ID.</span><span class="sxs-lookup"><span data-stu-id="2d3c6-121">Hostname Configuration identifier.</span></span>
<span data-ttu-id="2d3c6-122">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="2d3c6-122">This parameter is optional.</span></span>

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

### <span data-ttu-id="2d3c6-123">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="2d3c6-123">-GatewayId</span></span>
<span data-ttu-id="2d3c6-124">Gateway-ID.</span><span class="sxs-lookup"><span data-stu-id="2d3c6-124">Gateway identifier.</span></span>
<span data-ttu-id="2d3c6-125">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="2d3c6-125">This parameter is required.</span></span>

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

### <span data-ttu-id="2d3c6-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d3c6-126">CommonParameters</span></span>
<span data-ttu-id="2d3c6-127">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2d3c6-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d3c6-128">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2d3c6-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d3c6-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="2d3c6-129">INPUTS</span></span>

### <span data-ttu-id="2d3c6-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="2d3c6-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="2d3c6-131">System.String</span><span class="sxs-lookup"><span data-stu-id="2d3c6-131">System.String</span></span>

## <span data-ttu-id="2d3c6-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="2d3c6-132">OUTPUTS</span></span>

### <span data-ttu-id="2d3c6-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGatewayHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="2d3c6-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGatewayHostnameConfiguration</span></span>

## <span data-ttu-id="2d3c6-134">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="2d3c6-134">NOTES</span></span>

## <span data-ttu-id="2d3c6-135">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="2d3c6-135">RELATED LINKS</span></span>
