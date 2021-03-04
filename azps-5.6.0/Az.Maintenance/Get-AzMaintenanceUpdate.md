---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/powershell/module/az.maintenance/get-azmaintenanceupdate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Get-AzMaintenanceUpdate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Get-AzMaintenanceUpdate.md
ms.openlocfilehash: dd2fb366e4e15a2c2b21c53c5bddb32bc99939ba
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101922880"
---
# <span data-ttu-id="742d9-101">Get-AzMaintenanceUpdate</span><span class="sxs-lookup"><span data-stu-id="742d9-101">Get-AzMaintenanceUpdate</span></span>

## <span data-ttu-id="742d9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="742d9-102">SYNOPSIS</span></span>
<span data-ttu-id="742d9-103">Erhalten sie ausstehende Wartungsupdates für die Ressource.</span><span class="sxs-lookup"><span data-stu-id="742d9-103">Get pending maintenance updates to resource.</span></span>

## <span data-ttu-id="742d9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="742d9-104">SYNTAX</span></span>

```
Get-AzMaintenanceUpdate [-ResourceGroupName] <String> [-ProviderName] <String> [-ResourceParentType <String>]
 [-ResourceParentName <String>] [-ResourceType] <String> [-ResourceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="742d9-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="742d9-105">DESCRIPTION</span></span>
<span data-ttu-id="742d9-106">Erhalten sie ausstehende Wartungsupdates für die Ressource.</span><span class="sxs-lookup"><span data-stu-id="742d9-106">Get pending maintenance updates to resource.</span></span>

## <span data-ttu-id="742d9-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="742d9-107">EXAMPLES</span></span>

### <span data-ttu-id="742d9-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="742d9-108">Example 1</span></span>
```powershell
PS C:\> Get-AzMaintenanceUpdate -ResourceGroupName smdtest$location -ResourceParentType hostGroups -ResourceParentName smddhg$location -ResourceType hosts -ResourceName smddh$location -ProviderName Microsoft.Compute

MaintenanceScope    : Host
ImpactType          : Freeze
Status              : Pending
ImpactDurationInSec : 9
NotBefore           : 1/24/2020 5:11:41 AM
ResourceId          : /subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/smdtestwestus2/providers/Microsoft.Compute/hostGroups/smddhgwestus2/hosts/smddhwestus2
```

<span data-ttu-id="742d9-109">Erhalten sie ausstehende Wartungsupdates für die Ressource.</span><span class="sxs-lookup"><span data-stu-id="742d9-109">Get pending maintenance updates to resource.</span></span>

## <span data-ttu-id="742d9-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="742d9-110">PARAMETERS</span></span>

### <span data-ttu-id="742d9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="742d9-111">-DefaultProfile</span></span>
<span data-ttu-id="742d9-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="742d9-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="742d9-113">-ProviderName</span><span class="sxs-lookup"><span data-stu-id="742d9-113">-ProviderName</span></span>
<span data-ttu-id="742d9-114">Name des Ressourcenanbieters.</span><span class="sxs-lookup"><span data-stu-id="742d9-114">The resource provider Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="742d9-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="742d9-115">-ResourceGroupName</span></span>
<span data-ttu-id="742d9-116">Der Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="742d9-116">The resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="742d9-117">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="742d9-117">-ResourceName</span></span>
<span data-ttu-id="742d9-118">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="742d9-118">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="742d9-119">-ResourceParentName</span><span class="sxs-lookup"><span data-stu-id="742d9-119">-ResourceParentName</span></span>
<span data-ttu-id="742d9-120">Der übergeordnete Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="742d9-120">The parent resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="742d9-121">-ResourceParentType</span><span class="sxs-lookup"><span data-stu-id="742d9-121">-ResourceParentType</span></span>
<span data-ttu-id="742d9-122">Der übergeordnete Ressourcentyp.</span><span class="sxs-lookup"><span data-stu-id="742d9-122">The parent resource type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="742d9-123">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="742d9-123">-ResourceType</span></span>
<span data-ttu-id="742d9-124">Der Ressourcentyp.</span><span class="sxs-lookup"><span data-stu-id="742d9-124">The resource type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="742d9-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="742d9-125">CommonParameters</span></span>
<span data-ttu-id="742d9-126">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="742d9-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="742d9-127">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="742d9-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="742d9-128">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="742d9-128">INPUTS</span></span>

### <span data-ttu-id="742d9-129">System.String</span><span class="sxs-lookup"><span data-stu-id="742d9-129">System.String</span></span>

## <span data-ttu-id="742d9-130">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="742d9-130">OUTPUTS</span></span>

### <span data-ttu-id="742d9-131">Microsoft.Azure.Management.Maintenance.Models.Update</span><span class="sxs-lookup"><span data-stu-id="742d9-131">Microsoft.Azure.Management.Maintenance.Models.Update</span></span>

## <span data-ttu-id="742d9-132">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="742d9-132">NOTES</span></span>

## <span data-ttu-id="742d9-133">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="742d9-133">RELATED LINKS</span></span>
