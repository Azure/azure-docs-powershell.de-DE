---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementgatewaykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGatewayKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGatewayKey.md
ms.openlocfilehash: d58d33789f491098a62d7628ce6495ef2ba8870b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100171893"
---
# <span data-ttu-id="9eb42-101">Get-AzApiManagementGatewayKey</span><span class="sxs-lookup"><span data-stu-id="9eb42-101">Get-AzApiManagementGatewayKey</span></span>

## <span data-ttu-id="9eb42-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9eb42-102">SYNOPSIS</span></span>
<span data-ttu-id="9eb42-103">Ruft Schlüssel des vorhandenen Gateways ab</span><span class="sxs-lookup"><span data-stu-id="9eb42-103">Gets keys of the existing Gateway</span></span>

## <span data-ttu-id="9eb42-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9eb42-104">SYNTAX</span></span>

```
Get-AzApiManagementGatewayKey -Context <PsApiManagementContext> -GatewayId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9eb42-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9eb42-105">DESCRIPTION</span></span>
<span data-ttu-id="9eb42-106">Das **Cmdlet "Get-AzApiManagementGatewayKey"** ruft Schlüssel des vorhandenen Gateways ab.</span><span class="sxs-lookup"><span data-stu-id="9eb42-106">The **Get-AzApiManagementGatewayKey** cmdlet gets keys of the existing Gateway</span></span>

## <span data-ttu-id="9eb42-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="9eb42-107">EXAMPLES</span></span>

### <span data-ttu-id="9eb42-108">Beispiel 2: Erhalten eines Gateways nach ID</span><span class="sxs-lookup"><span data-stu-id="9eb42-108">Example 2: Get a gateway by ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGatewayKey -Context $apimContext -GatewayId "0123456789"
```

<span data-ttu-id="9eb42-109">Dieser Befehl ruft die Schlüssel für ein "0123456789"-Gateway ab.</span><span class="sxs-lookup"><span data-stu-id="9eb42-109">This command gets the keys for a "0123456789" gateway.</span></span>

## <span data-ttu-id="9eb42-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9eb42-110">PARAMETERS</span></span>

### <span data-ttu-id="9eb42-111">-Context</span><span class="sxs-lookup"><span data-stu-id="9eb42-111">-Context</span></span>
<span data-ttu-id="9eb42-112">Instanz von PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="9eb42-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="9eb42-113">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="9eb42-113">This parameter is required.</span></span>

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

### <span data-ttu-id="9eb42-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9eb42-114">-DefaultProfile</span></span>
<span data-ttu-id="9eb42-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9eb42-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9eb42-116">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="9eb42-116">-GatewayId</span></span>
<span data-ttu-id="9eb42-117">Gateway-ID.</span><span class="sxs-lookup"><span data-stu-id="9eb42-117">Gateway identifier.</span></span>
<span data-ttu-id="9eb42-118">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="9eb42-118">This parameter is required.</span></span>

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

### <span data-ttu-id="9eb42-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9eb42-119">CommonParameters</span></span>
<span data-ttu-id="9eb42-120">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9eb42-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9eb42-121">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9eb42-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9eb42-122">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="9eb42-122">INPUTS</span></span>

### <span data-ttu-id="9eb42-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="9eb42-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="9eb42-124">System.String</span><span class="sxs-lookup"><span data-stu-id="9eb42-124">System.String</span></span>

## <span data-ttu-id="9eb42-125">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="9eb42-125">OUTPUTS</span></span>

### <span data-ttu-id="9eb42-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGatewayKey</span><span class="sxs-lookup"><span data-stu-id="9eb42-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGatewayKey</span></span>

## <span data-ttu-id="9eb42-127">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="9eb42-127">NOTES</span></span>

## <span data-ttu-id="9eb42-128">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="9eb42-128">RELATED LINKS</span></span>
