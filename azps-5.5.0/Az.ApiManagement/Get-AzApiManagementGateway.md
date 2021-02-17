---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGateway.md
ms.openlocfilehash: 80b059a82264cf7d0adedbfca477616abcaa232d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100171900"
---
# <span data-ttu-id="6b156-101">Get-AzApiManagementGateway</span><span class="sxs-lookup"><span data-stu-id="6b156-101">Get-AzApiManagementGateway</span></span>

## <span data-ttu-id="6b156-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6b156-102">SYNOPSIS</span></span>
<span data-ttu-id="6b156-103">Ruft das sämtliche oder bestimmte API-Verwaltungsgateway ab.</span><span class="sxs-lookup"><span data-stu-id="6b156-103">Gets all or specific API management Gateway.</span></span>

## <span data-ttu-id="6b156-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6b156-104">SYNTAX</span></span>

### <span data-ttu-id="6b156-105">GetAllGateways (Standard)</span><span class="sxs-lookup"><span data-stu-id="6b156-105">GetAllGateways (Default)</span></span>
```
Get-AzApiManagementGateway -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6b156-106">GetByGatewayId</span><span class="sxs-lookup"><span data-stu-id="6b156-106">GetByGatewayId</span></span>
```
Get-AzApiManagementGateway -Context <PsApiManagementContext> -GatewayId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6b156-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6b156-107">DESCRIPTION</span></span>
<span data-ttu-id="6b156-108">Das **Cmdlet "Get-AzApiManagementGateway"** ruft das spezifische API-Verwaltungsgateway ab.</span><span class="sxs-lookup"><span data-stu-id="6b156-108">The **Get-AzApiManagementGateway** cmdlet gets all or specific API management Gateway.</span></span>

## <span data-ttu-id="6b156-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="6b156-109">EXAMPLES</span></span>

### <span data-ttu-id="6b156-110">Beispiel 1: Alle Gateways erhalten</span><span class="sxs-lookup"><span data-stu-id="6b156-110">Example 1: Get all gateways</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGateway -Context $apimContext
```

<span data-ttu-id="6b156-111">Dieser Befehl ruft alle Gateways ab.</span><span class="sxs-lookup"><span data-stu-id="6b156-111">This command gets all gateways.</span></span>

### <span data-ttu-id="6b156-112">Beispiel 2: Erhalten eines Gateways nach ID</span><span class="sxs-lookup"><span data-stu-id="6b156-112">Example 2: Get a gateway by ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGateway -Context $apimContext -GatewayId "0123456789"
```

<span data-ttu-id="6b156-113">Dieser Befehl ruft das Gateway 0123456789 ab.</span><span class="sxs-lookup"><span data-stu-id="6b156-113">This command gets the gateway 0123456789.</span></span>

## <span data-ttu-id="6b156-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6b156-114">PARAMETERS</span></span>

### <span data-ttu-id="6b156-115">-Context</span><span class="sxs-lookup"><span data-stu-id="6b156-115">-Context</span></span>
<span data-ttu-id="6b156-116">Instanz von PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="6b156-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="6b156-117">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="6b156-117">This parameter is required.</span></span>

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

### <span data-ttu-id="6b156-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b156-118">-DefaultProfile</span></span>
<span data-ttu-id="6b156-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6b156-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6b156-120">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="6b156-120">-GatewayId</span></span>
<span data-ttu-id="6b156-121">Id eines Gateways.</span><span class="sxs-lookup"><span data-stu-id="6b156-121">Identifier of a gateway.</span></span>
<span data-ttu-id="6b156-122">Bei Angabe wird versucht, das Gateway nach dem Bezeichner zu finden.</span><span class="sxs-lookup"><span data-stu-id="6b156-122">If specified will try to find gateway by the identifier.</span></span>

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

### <span data-ttu-id="6b156-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b156-123">CommonParameters</span></span>
<span data-ttu-id="6b156-124">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6b156-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b156-125">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6b156-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b156-126">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="6b156-126">INPUTS</span></span>

### <span data-ttu-id="6b156-127">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="6b156-127">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="6b156-128">System.String</span><span class="sxs-lookup"><span data-stu-id="6b156-128">System.String</span></span>

## <span data-ttu-id="6b156-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="6b156-129">OUTPUTS</span></span>

### <span data-ttu-id="6b156-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGateway</span><span class="sxs-lookup"><span data-stu-id="6b156-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGateway</span></span>

## <span data-ttu-id="6b156-131">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="6b156-131">NOTES</span></span>

## <span data-ttu-id="6b156-132">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="6b156-132">RELATED LINKS</span></span>
