---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/en-us/powershell/module/az.cloudservice/get-azcloudserviceinstanceview
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Get-AzCloudServiceInstanceView.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Get-AzCloudServiceInstanceView.md
ms.openlocfilehash: 4ad5b8a7b4369a5a0dd2b5ccc883ddc561a40af5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100167985"
---
# <span data-ttu-id="89d32-101">Get-AzCloudServiceInstanceView</span><span class="sxs-lookup"><span data-stu-id="89d32-101">Get-AzCloudServiceInstanceView</span></span>

## <span data-ttu-id="89d32-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="89d32-102">SYNOPSIS</span></span>
<span data-ttu-id="89d32-103">Ruft den Status eines Clouddiensts ab.</span><span class="sxs-lookup"><span data-stu-id="89d32-103">Gets the status of a cloud service.</span></span>

## <span data-ttu-id="89d32-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="89d32-104">SYNTAX</span></span>

```
Get-AzCloudServiceInstanceView -CloudServiceName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="89d32-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="89d32-105">DESCRIPTION</span></span>
<span data-ttu-id="89d32-106">Ruft den Status eines Clouddiensts ab.</span><span class="sxs-lookup"><span data-stu-id="89d32-106">Gets the status of a cloud service.</span></span>

## <span data-ttu-id="89d32-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="89d32-107">EXAMPLES</span></span>

### <span data-ttu-id="89d32-108">Beispiel 1: Anzeigen der Clouddienstinstanzansicht</span><span class="sxs-lookup"><span data-stu-id="89d32-108">Example 1: Get cloud service instance view</span></span>
```powershell
PS C:\>$cloudServiceInstanceView = Get-AzCloudServiceInstanceView -ResourceGroupName "ContosOrg" -CloudServiceName "ContosoCS"

PS C:\>$cloudServiceInstanceView
RoleInstanceStatusesSummary                                   Statuses
---------------------------                                   --------
{{ProvisioningState/succeeded : 4}, {PowerState/started : 4}} {Provisioning succeeded, Started, Current Upgrade Domain of cloud service is -1., Max Upgrade Domain of cloud service is 1.}

PS C:\>$cloudServiceInstanceView.ToJsonString()
{
  "roleInstance": {
    "statusesSummary": [
      {
        "code": "ProvisioningState/succeeded",
        "count": 4
      },
      {
        "code": "PowerState/started",
        "count": 4
      }
    ]
  },
  "statuses": [
    {
      "code": "ProvisioningState/succeeded",
      "displayStatus": "Provisioning succeeded",
      "level": "Info",
      "time": "2020-10-28T13:26:48.8109686Z"
    },
    {
      "code": "PowerState/started",
      "displayStatus": "Started",
      "level": "Info",
      "time": "2020-10-28T13:26:48.8109686Z"
    },
    {
      "code": "CurrentUpgradeDomain/-1",
      "displayStatus": "Current Upgrade Domain of cloud service is -1.",
      "level": "Info"
    },
    {
      "code": "MaxUpgradeDomain/1",
      "displayStatus": "Max Upgrade Domain of cloud service is 1.",
      "level": "Info"
    }
  ]
}
```

<span data-ttu-id="89d32-109">Dieses Cmdlet ruft die Instanzansicht des Clouddiensts "ContosoCS" ab, der zur Ressourcengruppe "ContosOrg" gehört.</span><span class="sxs-lookup"><span data-stu-id="89d32-109">This cmdlet gets the instance view of the cloud service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

## <span data-ttu-id="89d32-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="89d32-110">PARAMETERS</span></span>

### <span data-ttu-id="89d32-111">-CloudServiceName</span><span class="sxs-lookup"><span data-stu-id="89d32-111">-CloudServiceName</span></span>
<span data-ttu-id="89d32-112">Der Name des Clouddiensts.</span><span class="sxs-lookup"><span data-stu-id="89d32-112">Name of the cloud service.</span></span>

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

### <span data-ttu-id="89d32-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89d32-113">-DefaultProfile</span></span>
<span data-ttu-id="89d32-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="89d32-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="89d32-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="89d32-115">-ResourceGroupName</span></span>
<span data-ttu-id="89d32-116">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="89d32-116">Name of the resource group.</span></span>

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

### <span data-ttu-id="89d32-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="89d32-117">-SubscriptionId</span></span>
<span data-ttu-id="89d32-118">Abonnementanmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="89d32-118">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="89d32-119">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="89d32-119">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="89d32-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89d32-120">CommonParameters</span></span>
<span data-ttu-id="89d32-121">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="89d32-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89d32-122">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="89d32-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89d32-123">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="89d32-123">INPUTS</span></span>

## <span data-ttu-id="89d32-124">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="89d32-124">OUTPUTS</span></span>

### <span data-ttu-id="89d32-125">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.ICloudServiceInstanceView</span><span class="sxs-lookup"><span data-stu-id="89d32-125">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.ICloudServiceInstanceView</span></span>

## <span data-ttu-id="89d32-126">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="89d32-126">NOTES</span></span>

<span data-ttu-id="89d32-127">ALIASE</span><span class="sxs-lookup"><span data-stu-id="89d32-127">ALIASES</span></span>

## <span data-ttu-id="89d32-128">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="89d32-128">RELATED LINKS</span></span>

