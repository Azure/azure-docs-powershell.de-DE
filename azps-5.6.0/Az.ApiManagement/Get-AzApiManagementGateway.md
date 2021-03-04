---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/get-azapimanagementgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGateway.md
ms.openlocfilehash: 980adceb2e5a76532c9b3175c015d5f4e3a6b2e1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101943171"
---
# <span data-ttu-id="255c7-101">Get-AzApiManagementGateway</span><span class="sxs-lookup"><span data-stu-id="255c7-101">Get-AzApiManagementGateway</span></span>

## <span data-ttu-id="255c7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="255c7-102">SYNOPSIS</span></span>
<span data-ttu-id="255c7-103">Ruft das ganze oder bestimmte API-Verwaltungsgateway ab.</span><span class="sxs-lookup"><span data-stu-id="255c7-103">Gets all or specific API management Gateway.</span></span>

## <span data-ttu-id="255c7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="255c7-104">SYNTAX</span></span>

### <span data-ttu-id="255c7-105">GetAllGateways (Standard)</span><span class="sxs-lookup"><span data-stu-id="255c7-105">GetAllGateways (Default)</span></span>
```
Get-AzApiManagementGateway -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="255c7-106">GetByGatewayId</span><span class="sxs-lookup"><span data-stu-id="255c7-106">GetByGatewayId</span></span>
```
Get-AzApiManagementGateway -Context <PsApiManagementContext> -GatewayId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="255c7-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="255c7-107">DESCRIPTION</span></span>
<span data-ttu-id="255c7-108">Das **Get-AzApiManagementGateway-Cmdlet** ruft alle oder bestimmte API-Verwaltungsgateways ab.</span><span class="sxs-lookup"><span data-stu-id="255c7-108">The **Get-AzApiManagementGateway** cmdlet gets all or specific API management Gateway.</span></span>

## <span data-ttu-id="255c7-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="255c7-109">EXAMPLES</span></span>

### <span data-ttu-id="255c7-110">Beispiel 1: Alle Gateways erhalten</span><span class="sxs-lookup"><span data-stu-id="255c7-110">Example 1: Get all gateways</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGateway -Context $apimContext
```

<span data-ttu-id="255c7-111">Dieser Befehl ruft alle Gateways ab.</span><span class="sxs-lookup"><span data-stu-id="255c7-111">This command gets all gateways.</span></span>

### <span data-ttu-id="255c7-112">Beispiel 2: Erhalten eines Gateways nach ID</span><span class="sxs-lookup"><span data-stu-id="255c7-112">Example 2: Get a gateway by ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGateway -Context $apimContext -GatewayId "0123456789"
```

<span data-ttu-id="255c7-113">Dieser Befehl ruft das Gateway 0123456789 ab.</span><span class="sxs-lookup"><span data-stu-id="255c7-113">This command gets the gateway 0123456789.</span></span>

## <span data-ttu-id="255c7-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="255c7-114">PARAMETERS</span></span>

### <span data-ttu-id="255c7-115">-Context</span><span class="sxs-lookup"><span data-stu-id="255c7-115">-Context</span></span>
<span data-ttu-id="255c7-116">Instanz von PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="255c7-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="255c7-117">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="255c7-117">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="255c7-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="255c7-118">-DefaultProfile</span></span>
<span data-ttu-id="255c7-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="255c7-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="255c7-120">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="255c7-120">-GatewayId</span></span>
<span data-ttu-id="255c7-121">Bezeichner eines Gateways.</span><span class="sxs-lookup"><span data-stu-id="255c7-121">Identifier of a gateway.</span></span>
<span data-ttu-id="255c7-122">Wenn angegeben, wird versucht, das Gateway durch den Bezeichner zu finden.</span><span class="sxs-lookup"><span data-stu-id="255c7-122">If specified will try to find gateway by the identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByGatewayId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="255c7-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="255c7-123">CommonParameters</span></span>
<span data-ttu-id="255c7-124">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="255c7-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="255c7-125">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="255c7-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="255c7-126">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="255c7-126">INPUTS</span></span>

### <span data-ttu-id="255c7-127">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="255c7-127">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="255c7-128">System.String</span><span class="sxs-lookup"><span data-stu-id="255c7-128">System.String</span></span>

## <span data-ttu-id="255c7-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="255c7-129">OUTPUTS</span></span>

### <span data-ttu-id="255c7-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGateway</span><span class="sxs-lookup"><span data-stu-id="255c7-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGateway</span></span>

## <span data-ttu-id="255c7-131">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="255c7-131">NOTES</span></span>

## <span data-ttu-id="255c7-132">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="255c7-132">RELATED LINKS</span></span>
