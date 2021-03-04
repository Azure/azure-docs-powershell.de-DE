---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/get-azapimanagementgatewaykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGatewayKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGatewayKey.md
ms.openlocfilehash: 08931af2c5d4f4747bd02a759e374d8fccd247c0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101933275"
---
# <span data-ttu-id="4ce17-101">Get-AzApiManagementGatewayKey</span><span class="sxs-lookup"><span data-stu-id="4ce17-101">Get-AzApiManagementGatewayKey</span></span>

## <span data-ttu-id="4ce17-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4ce17-102">SYNOPSIS</span></span>
<span data-ttu-id="4ce17-103">Ruft Schlüssel des vorhandenen Gateways ab</span><span class="sxs-lookup"><span data-stu-id="4ce17-103">Gets keys of the existing Gateway</span></span>

## <span data-ttu-id="4ce17-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4ce17-104">SYNTAX</span></span>

```
Get-AzApiManagementGatewayKey -Context <PsApiManagementContext> -GatewayId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4ce17-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4ce17-105">DESCRIPTION</span></span>
<span data-ttu-id="4ce17-106">Das **Get-AzApiManagementGatewayKey-Cmdlet** ruft Schlüssel des vorhandenen Gateways ab.</span><span class="sxs-lookup"><span data-stu-id="4ce17-106">The **Get-AzApiManagementGatewayKey** cmdlet gets keys of the existing Gateway</span></span>

## <span data-ttu-id="4ce17-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="4ce17-107">EXAMPLES</span></span>

### <span data-ttu-id="4ce17-108">Beispiel 2: Erhalten eines Gateways nach ID</span><span class="sxs-lookup"><span data-stu-id="4ce17-108">Example 2: Get a gateway by ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGatewayKey -Context $apimContext -GatewayId "0123456789"
```

<span data-ttu-id="4ce17-109">Dieser Befehl ruft die Schlüssel für ein "0123456789"-Gateway ab.</span><span class="sxs-lookup"><span data-stu-id="4ce17-109">This command gets the keys for a "0123456789" gateway.</span></span>

## <span data-ttu-id="4ce17-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="4ce17-110">PARAMETERS</span></span>

### <span data-ttu-id="4ce17-111">-Context</span><span class="sxs-lookup"><span data-stu-id="4ce17-111">-Context</span></span>
<span data-ttu-id="4ce17-112">Instanz von PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="4ce17-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="4ce17-113">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="4ce17-113">This parameter is required.</span></span>

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

### <span data-ttu-id="4ce17-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ce17-114">-DefaultProfile</span></span>
<span data-ttu-id="4ce17-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4ce17-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4ce17-116">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="4ce17-116">-GatewayId</span></span>
<span data-ttu-id="4ce17-117">Gatewaybezeichner.</span><span class="sxs-lookup"><span data-stu-id="4ce17-117">Gateway identifier.</span></span>
<span data-ttu-id="4ce17-118">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="4ce17-118">This parameter is required.</span></span>

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

### <span data-ttu-id="4ce17-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ce17-119">CommonParameters</span></span>
<span data-ttu-id="4ce17-120">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ce17-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ce17-121">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4ce17-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ce17-122">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="4ce17-122">INPUTS</span></span>

### <span data-ttu-id="4ce17-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="4ce17-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="4ce17-124">System.String</span><span class="sxs-lookup"><span data-stu-id="4ce17-124">System.String</span></span>

## <span data-ttu-id="4ce17-125">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="4ce17-125">OUTPUTS</span></span>

### <span data-ttu-id="4ce17-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGatewayKey</span><span class="sxs-lookup"><span data-stu-id="4ce17-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGatewayKey</span></span>

## <span data-ttu-id="4ce17-127">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="4ce17-127">NOTES</span></span>

## <span data-ttu-id="4ce17-128">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="4ce17-128">RELATED LINKS</span></span>
