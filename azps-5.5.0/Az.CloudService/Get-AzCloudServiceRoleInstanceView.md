---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/en-us/powershell/module/az.cloudservice/get-azcloudserviceroleinstanceview
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Get-AzCloudServiceRoleInstanceView.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Get-AzCloudServiceRoleInstanceView.md
ms.openlocfilehash: a86ebbda321f37a38b3d014377081087f37feb9e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100149025"
---
# <span data-ttu-id="bb39e-101">Get-AzCloudServiceRoleInstanceView</span><span class="sxs-lookup"><span data-stu-id="bb39e-101">Get-AzCloudServiceRoleInstanceView</span></span>

## <span data-ttu-id="bb39e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bb39e-102">SYNOPSIS</span></span>
<span data-ttu-id="bb39e-103">Ruft Informationen zum Laufzeitstatus einer Rolleninstanz in einem Clouddienst ab.</span><span class="sxs-lookup"><span data-stu-id="bb39e-103">Retrieves information about the run-time state of a role instance in a cloud service.</span></span>

## <span data-ttu-id="bb39e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bb39e-104">SYNTAX</span></span>

```
Get-AzCloudServiceRoleInstanceView -CloudServiceName <String> -ResourceGroupName <String>
 -RoleInstanceName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="bb39e-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bb39e-105">DESCRIPTION</span></span>
<span data-ttu-id="bb39e-106">Ruft Informationen zum Laufzeitstatus einer Rolleninstanz in einem Clouddienst ab.</span><span class="sxs-lookup"><span data-stu-id="bb39e-106">Retrieves information about the run-time state of a role instance in a cloud service.</span></span>

## <span data-ttu-id="bb39e-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="bb39e-107">EXAMPLES</span></span>

### <span data-ttu-id="bb39e-108">Beispiel 1: Erhalten von Details zur Instanzansicht für die Rolleninstanz des Clouddiensts</span><span class="sxs-lookup"><span data-stu-id="bb39e-108">Example 1: Get instance view details for cloud service role instance</span></span>
```powershell
PS C:\> Get-AzCloudServiceRoleInstanceView -ResourceGroupName "ContosOrg" -CloudServiceName "ContosoCS" -RoleInstanceName "ContosoFrontEnd_IN_0"

Statuses           PlatformFaultDomain PlatformUpdateDomain
--------           ------------------- --------------------
{RoleStateStarted} 0                   0

```

<span data-ttu-id="bb39e-109">Dieses Cmdlet ruft die Instanzansicht der Rolleninstanz mit dem Namen ContosoFrontEnd_IN_0 des Clouddiensts "ContosoCS" ab, der zur Ressourcengruppe "ContosOrg" gehört.</span><span class="sxs-lookup"><span data-stu-id="bb39e-109">This cmdlet gets the instance view of the role instance named ContosoFrontEnd_IN_0 of cloud service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

## <span data-ttu-id="bb39e-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bb39e-110">PARAMETERS</span></span>

### <span data-ttu-id="bb39e-111">-CloudServiceName</span><span class="sxs-lookup"><span data-stu-id="bb39e-111">-CloudServiceName</span></span>
<span data-ttu-id="bb39e-112">.</span><span class="sxs-lookup"><span data-stu-id="bb39e-112">.</span></span>

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

### <span data-ttu-id="bb39e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb39e-113">-DefaultProfile</span></span>
<span data-ttu-id="bb39e-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="bb39e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bb39e-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb39e-115">-ResourceGroupName</span></span>
<span data-ttu-id="bb39e-116">.</span><span class="sxs-lookup"><span data-stu-id="bb39e-116">.</span></span>

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

### <span data-ttu-id="bb39e-117">-RoleInstanceName</span><span class="sxs-lookup"><span data-stu-id="bb39e-117">-RoleInstanceName</span></span>
<span data-ttu-id="bb39e-118">Der Name der Rolleninstanz.</span><span class="sxs-lookup"><span data-stu-id="bb39e-118">Name of the role instance.</span></span>

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

### <span data-ttu-id="bb39e-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="bb39e-119">-SubscriptionId</span></span>
<span data-ttu-id="bb39e-120">Abonnementanmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="bb39e-120">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="bb39e-121">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="bb39e-121">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="bb39e-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb39e-122">CommonParameters</span></span>
<span data-ttu-id="bb39e-123">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb39e-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb39e-124">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bb39e-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb39e-125">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="bb39e-125">INPUTS</span></span>

## <span data-ttu-id="bb39e-126">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="bb39e-126">OUTPUTS</span></span>

### <span data-ttu-id="bb39e-127">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.IRoleInstanceView</span><span class="sxs-lookup"><span data-stu-id="bb39e-127">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.IRoleInstanceView</span></span>

## <span data-ttu-id="bb39e-128">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="bb39e-128">NOTES</span></span>

<span data-ttu-id="bb39e-129">ALIASE</span><span class="sxs-lookup"><span data-stu-id="bb39e-129">ALIASES</span></span>

## <span data-ttu-id="bb39e-130">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="bb39e-130">RELATED LINKS</span></span>

