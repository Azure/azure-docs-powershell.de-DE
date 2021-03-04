---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/powershell/module/az.cloudservice/get-azcloudserviceroleinstanceview
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Get-AzCloudServiceRoleInstanceView.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Get-AzCloudServiceRoleInstanceView.md
ms.openlocfilehash: 3d3d8e5cd7855e03d5f02ddaee6b38c98aeacb0d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101946648"
---
# <span data-ttu-id="6d574-101">Get-AzCloudServiceRoleInstanceView</span><span class="sxs-lookup"><span data-stu-id="6d574-101">Get-AzCloudServiceRoleInstanceView</span></span>

## <span data-ttu-id="6d574-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6d574-102">SYNOPSIS</span></span>
<span data-ttu-id="6d574-103">Ruft Informationen zum Laufzeitzustand einer Rolleninstanz in einem Clouddienst ab.</span><span class="sxs-lookup"><span data-stu-id="6d574-103">Retrieves information about the run-time state of a role instance in a cloud service.</span></span>

## <span data-ttu-id="6d574-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6d574-104">SYNTAX</span></span>

```
Get-AzCloudServiceRoleInstanceView -CloudServiceName <String> -ResourceGroupName <String>
 -RoleInstanceName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="6d574-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6d574-105">DESCRIPTION</span></span>
<span data-ttu-id="6d574-106">Ruft Informationen zum Laufzeitzustand einer Rolleninstanz in einem Clouddienst ab.</span><span class="sxs-lookup"><span data-stu-id="6d574-106">Retrieves information about the run-time state of a role instance in a cloud service.</span></span>

## <span data-ttu-id="6d574-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="6d574-107">EXAMPLES</span></span>

### <span data-ttu-id="6d574-108">Beispiel 1: Anzeigen von Details zur Instanzansicht für die Rolleninstanz des Clouddiensts</span><span class="sxs-lookup"><span data-stu-id="6d574-108">Example 1: Get instance view details for cloud service role instance</span></span>
```powershell
PS C:\> Get-AzCloudServiceRoleInstanceView -ResourceGroupName "ContosOrg" -CloudServiceName "ContosoCS" -RoleInstanceName "ContosoFrontEnd_IN_0"

Statuses           PlatformFaultDomain PlatformUpdateDomain
--------           ------------------- --------------------
{RoleStateStarted} 0                   0

```

<span data-ttu-id="6d574-109">Dieses Cmdlet ruft die Instanzansicht der Rolleninstanz mit dem Namen ContosoFrontEnd_IN_0 des Clouddiensts ContosoCS ab, der zur Ressourcengruppe "ContosOrg" gehört.</span><span class="sxs-lookup"><span data-stu-id="6d574-109">This cmdlet gets the instance view of the role instance named ContosoFrontEnd_IN_0 of cloud service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

## <span data-ttu-id="6d574-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="6d574-110">PARAMETERS</span></span>

### <span data-ttu-id="6d574-111">-CloudServiceName</span><span class="sxs-lookup"><span data-stu-id="6d574-111">-CloudServiceName</span></span>
<span data-ttu-id="6d574-112">.</span><span class="sxs-lookup"><span data-stu-id="6d574-112">.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d574-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d574-113">-DefaultProfile</span></span>
<span data-ttu-id="6d574-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6d574-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d574-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6d574-115">-ResourceGroupName</span></span>
<span data-ttu-id="6d574-116">.</span><span class="sxs-lookup"><span data-stu-id="6d574-116">.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d574-117">-RoleInstanceName</span><span class="sxs-lookup"><span data-stu-id="6d574-117">-RoleInstanceName</span></span>
<span data-ttu-id="6d574-118">Name der Rolleninstanz.</span><span class="sxs-lookup"><span data-stu-id="6d574-118">Name of the role instance.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d574-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6d574-119">-SubscriptionId</span></span>
<span data-ttu-id="6d574-120">Abonnementanmeldeinformationen, mit denen Microsoft Azure-Abonnement eindeutig identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="6d574-120">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="6d574-121">Die Abonnement-ID ist Teil des URI für jeden Dienstanruf.</span><span class="sxs-lookup"><span data-stu-id="6d574-121">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d574-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d574-122">CommonParameters</span></span>
<span data-ttu-id="6d574-123">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6d574-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d574-124">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6d574-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d574-125">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="6d574-125">INPUTS</span></span>

## <span data-ttu-id="6d574-126">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="6d574-126">OUTPUTS</span></span>

### <span data-ttu-id="6d574-127">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.IRoleInstanceView</span><span class="sxs-lookup"><span data-stu-id="6d574-127">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.IRoleInstanceView</span></span>

## <span data-ttu-id="6d574-128">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="6d574-128">NOTES</span></span>

<span data-ttu-id="6d574-129">ALIASE</span><span class="sxs-lookup"><span data-stu-id="6d574-129">ALIASES</span></span>

## <span data-ttu-id="6d574-130">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="6d574-130">RELATED LINKS</span></span>

