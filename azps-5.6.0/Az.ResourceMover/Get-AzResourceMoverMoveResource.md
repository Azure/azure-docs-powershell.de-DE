---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/powershell/module/az.resourcemover/get-azresourcemovermoveresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Get-AzResourceMoverMoveResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Get-AzResourceMoverMoveResource.md
ms.openlocfilehash: a60d41f27962a1e803067c8172b3e388a31ba601
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101943594"
---
# <span data-ttu-id="7651c-101">Get-AzResourceMoverMoveResource</span><span class="sxs-lookup"><span data-stu-id="7651c-101">Get-AzResourceMoverMoveResource</span></span>

## <span data-ttu-id="7651c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7651c-102">SYNOPSIS</span></span>
<span data-ttu-id="7651c-103">Ruft die Ressource verschieben ab.</span><span class="sxs-lookup"><span data-stu-id="7651c-103">Gets the Move Resource.</span></span>

## <span data-ttu-id="7651c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7651c-104">SYNTAX</span></span>

### <span data-ttu-id="7651c-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="7651c-105">List (Default)</span></span>
```
Get-AzResourceMoverMoveResource -MoveCollectionName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-Filter <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="7651c-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="7651c-106">Get</span></span>
```
Get-AzResourceMoverMoveResource -MoveCollectionName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="7651c-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7651c-107">DESCRIPTION</span></span>
<span data-ttu-id="7651c-108">Ruft die Ressource verschieben ab.</span><span class="sxs-lookup"><span data-stu-id="7651c-108">Gets the Move Resource.</span></span>

## <span data-ttu-id="7651c-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="7651c-109">EXAMPLES</span></span>

### <span data-ttu-id="7651c-110">Beispiel 1: Erhalten Sie Details aller Ressourcen in der Sammlung Verschieben.</span><span class="sxs-lookup"><span data-stu-id="7651c-110">Example 1: Get details of all the resources in the Move collection.</span></span>
```powershell
PS C:\>Get-AzResourceMoverMoveResource -MoveCollectionName "PS-centralus-westcentralus-demoRMS" -ResourceGroupName "RG-MoveCollection-demoRMS"         

DependsOn                         : {/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/PSDemoRM/providers/Microsoft.Network/networkInterfaces/psdemov
                                    m111, /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourcegroups/PSDemoRM}
DependsOnOverride                 : {}
ErrorsPropertiesCode              : 
ErrorsPropertiesDetail            : 
ErrorsPropertiesMessage           : 
ErrorsPropertiesTarget            : 
ExistingTargetId                  : 
Id                                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/RG-MoveCollection-demoRMS/providers/Microsoft.Migrate/moveColle
                                    ctions/PS-centralus-westcentralus-demoRMS1/moveResources/PSDemoVM
IsResolveRequired                 : False
JobStatusJobName                  : 
JobStatusJobProgress              : 
MoveStatusErrorsPropertiesCode    : 
MoveStatusErrorsPropertiesDetail  : 
MoveStatusErrorsPropertiesMessage : 
MoveStatusErrorsPropertiesTarget  : 
MoveStatusMoveState               : PreparePending
Name                              : PSDemoVM
ProvisioningState                 : Succeeded
ResourceSetting                   : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api202101.VirtualMachineResourceSettings
SourceId                          : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/PSDemoRM/providers/Microsoft.Compute/virtualMachines/PSDemoVM
SourceResourceSetting             : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api202101.VirtualMachineResourceSettings
TargetId                          : 
Type                              : 

DependsOn                         : {/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/psdemorm/providers/Microsoft.Network/virtualNetworks/psdemorm-
                                    vnet, /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourcegroups/psdemorm/providers/microsoft.network/networksecuritygroup
                                    s/psdemovm-nsg, /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourcegroups/psdemorm}
DependsOnOverride                 : {}
ErrorsPropertiesCode              : 
ErrorsPropertiesDetail            : 
ErrorsPropertiesMessage           : 
ErrorsPropertiesTarget            : 
ExistingTargetId                  : 
Id                                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/RG-MoveCollection-demoRMS/providers/Microsoft.Migrate/moveColle
                                    ctions/PS-centralus-westcentralus-demoRMS1/moveResources/psdemovm111
IsResolveRequired                 : False
JobStatusJobName                  : 
JobStatusJobProgress              : 
MoveStatusErrorsPropertiesCode    : 
MoveStatusErrorsPropertiesDetail  : 
MoveStatusErrorsPropertiesMessage : 
MoveStatusErrorsPropertiesTarget  : 
MoveStatusMoveState               : PreparePending
Name                              : psdemovm111
ProvisioningState                 : Succeeded
ResourceSetting                   : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api202101.NetworkInterfaceResourceSettings
SourceId                          : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourcegroups/psdemorm/providers/microsoft.network/networkinterfaces/psdemovm
                                    111
SourceResourceSetting             : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api202101.NetworkInterfaceResourceSettings
TargetId                          : 
Type                              : 

DependsOn                         : {/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourcegroups/psdemorm}
DependsOnOverride                 : {}
ErrorsPropertiesCode              : 
ErrorsPropertiesDetail            : 
ErrorsPropertiesMessage           : 
ErrorsPropertiesTarget            : 
ExistingTargetId                  : 
Id                                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/RG-MoveCollection-demoRMS/providers/Microsoft.Migrate/moveColle
                                    ctions/PS-centralus-westcentralus-demoRMS1/moveResources/psdemorm-vnet
IsResolveRequired                 : False
JobStatusJobName                  : 
JobStatusJobProgress              : 
MoveStatusErrorsPropertiesCode    : 
MoveStatusErrorsPropertiesDetail  : 
MoveStatusErrorsPropertiesMessage : 
MoveStatusErrorsPropertiesTarget  : 
MoveStatusMoveState               : PreparePending
Name                              : psdemorm-vnet
ProvisioningState                 : Succeeded
ResourceSetting                   : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api202101.VirtualNetworkResourceSettings
SourceId                          : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/psdemorm/providers/Microsoft.Network/virtualNetworks/psdemorm-v
                                    net
SourceResourceSetting             : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api202101.VirtualNetworkResourceSettings
TargetId                          : 
Type                              : 

DependsOn                         : {/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourcegroups/psdemorm}
DependsOnOverride                 : {}
ErrorsPropertiesCode              : 
ErrorsPropertiesDetail            : 
ErrorsPropertiesMessage           : 
ErrorsPropertiesTarget            : 
ExistingTargetId                  : 
Id                                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/RG-MoveCollection-demoRMS/providers/Microsoft.Migrate/moveColle
                                    ctions/PS-centralus-westcentralus-demoRMS1/moveResources/psdemovm-nsg
IsResolveRequired                 : False
JobStatusJobName                  : 
JobStatusJobProgress              : 
MoveStatusErrorsPropertiesCode    : 
MoveStatusErrorsPropertiesDetail  : 
MoveStatusErrorsPropertiesMessage : 
MoveStatusErrorsPropertiesTarget  : 
MoveStatusMoveState               : PreparePending
Name                              : psdemovm-nsg
ProvisioningState                 : Succeeded
ResourceSetting                   : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api202101.NetworkSecurityGroupResourceSettings
SourceId                          : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourcegroups/psdemorm/providers/microsoft.network/networksecuritygroups/psde
                                    movm-nsg
SourceResourceSetting             : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api202101.NetworkSecurityGroupResourceSettings
TargetId                          : 
Type                              : 

DependsOn                         : {}
DependsOnOverride                 : {}
ErrorsPropertiesCode              : 
ErrorsPropertiesDetail            : 
ErrorsPropertiesMessage           : 
ErrorsPropertiesTarget            : 
ExistingTargetId                  : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourcegroups/PSDemoRM-target
Id                                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/RG-MoveCollection-demoRMS/providers/Microsoft.Migrate/moveColle
                                    ctions/PS-centralus-westcentralus-demoRMS1/moveResources/psdemorm
IsResolveRequired                 : False
JobStatusJobName                  : 
JobStatusJobProgress              : 
MoveStatusErrorsPropertiesCode    : 
MoveStatusErrorsPropertiesDetail  : 
MoveStatusErrorsPropertiesMessage : 
MoveStatusErrorsPropertiesTarget  : 
MoveStatusMoveState               : DeleteSourcePending
Name                              : psdemorm
ProvisioningState                 : Succeeded
ResourceSetting                   : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api202101.ResourceSettings
SourceId                          : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourcegroups/psdemorm
SourceResourceSetting             : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api202101.ResourceSettings
TargetId                          : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourcegroups/PSDemoRM-target
Type                              :

```

<span data-ttu-id="7651c-111">Hier erhalten Sie Details zu allen Ressourcen in der Sammlung verschieben.</span><span class="sxs-lookup"><span data-stu-id="7651c-111">Get details of all the resources in the move collection.</span></span>

### <span data-ttu-id="7651c-112">Beispiel 2: Details zu bestimmten Ressourcen in einer Sammlung Verschieben mithilfe des Ressourcennamens verschieben.</span><span class="sxs-lookup"><span data-stu-id="7651c-112">Example 2: Get details of a specific resources in a Move collection using move resource name .</span></span>
```powershell
PS C:\> Get-AzResourceMoverMoveResource -MoveCollectionName "PS-centralus-westcentralus-demoRMS" -ResourceGroupName "RG-MoveCollection-demoRMS" -Name "PSDemoVM"   
                                                     
DependsOn                         : {/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/PSDemoRM/providers/Microsoft.Network/networkInterfaces/psdemov
                                    m111, /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourcegroups/PSDemoRM}
DependsOnOverride                 : {}
ErrorsPropertiesCode              : 
ErrorsPropertiesDetail            : 
ErrorsPropertiesMessage           : 
ErrorsPropertiesTarget            : 
ExistingTargetId                  : 
Id                                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/RG-MoveCollection-demoRMS/providers/Microsoft.Migrate/moveColle
                                    ctions/PS-centralus-westcentralus-demoRMS/moveResources/PSDemoVM
IsResolveRequired                 : False
JobStatusJobName                  : 
JobStatusJobProgress              : 
MoveStatusErrorsPropertiesCode    : 
MoveStatusErrorsPropertiesDetail  : 
MoveStatusErrorsPropertiesMessage : 
MoveStatusErrorsPropertiesTarget  : 
MoveStatusMoveState               : PreparePending
Name                              : PSDemoVM
ProvisioningState                 : Succeeded
ResourceSetting                   : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api202101.VirtualMachineResourceSettings
SourceId                          : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/PSDemoRM/providers/Microsoft.Compute/virtualMachines/PSDemoVM
SourceResourceSetting             : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api202101.VirtualMachineResourceSettings
TargetId                          : 
Type                              : 

```

<span data-ttu-id="7651c-113">Hier erhalten Sie Details zu bestimmten Ressourcen in einer Sammlung Verschieben mithilfe des Ressourcennamens verschieben.</span><span class="sxs-lookup"><span data-stu-id="7651c-113">Get details of a specific resources in a Move collection using move resource name .</span></span>

### <span data-ttu-id="7651c-114">Beispiel 3:Details zu bestimmten Ressourcen in einer Move-Sammlung mithilfe von Filtern wie : SourceResourceName, SourceId, MoveState, IsResolveRequired, ProvisioningState</span><span class="sxs-lookup"><span data-stu-id="7651c-114">Example 3:Get details of a specific resources in a Move collection using filters such as : SourceResourceName, SourceId, MoveState, IsResolveRequired, ProvisioningState</span></span>
```powershell
PS C:\WINDOWS\system32> Get-AzResourceMoverMoveResource -MoveCollectionName "PS-centralus-westcentralus-demoRMS1" -ResourceGroupName "RG-MoveCollection-demoRMS" -Filter "Properties/SourceResourceName eq 'psdemovm111'"


DependsOn                         : {/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/psdemorm/providers/Microsoft.Network/virtualNetworks/psdemorm-
                                    vnet, /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourcegroups/psdemorm/providers/microsoft.network/networksecuritygroup
                                    s/psdemovm-nsg, /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourcegroups/psdemorm}
DependsOnOverride                 : {}
ErrorsPropertiesCode              : 
ErrorsPropertiesDetail            : 
ErrorsPropertiesMessage           : 
ErrorsPropertiesTarget            : 
ExistingTargetId                  : 
Id                                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/RG-MoveCollection-demoRMS/providers/Microsoft.Migrate/moveColle
                                    ctions/PS-centralus-westcentralus-demoRMS1/moveResources/psdemovm111
IsResolveRequired                 : False
JobStatusJobName                  : 
JobStatusJobProgress              : 
MoveStatusErrorsPropertiesCode    : 
MoveStatusErrorsPropertiesDetail  : 
MoveStatusErrorsPropertiesMessage : 
MoveStatusErrorsPropertiesTarget  : 
MoveStatusMoveState               : PreparePending
Name                              : psdemovm111
ProvisioningState                 : Succeeded
ResourceSetting                   : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api202101.NetworkInterfaceResourceSettings
SourceId                          : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourcegroups/psdemorm/providers/microsoft.network/networkinterfaces/psdemovm
                                    111
SourceResourceSetting             : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api202101.NetworkInterfaceResourceSettings
TargetId                          : 
Type                              : 

```

<span data-ttu-id="7651c-115">Abrufen von Details zu bestimmten Ressourcen in einer Move-Sammlung mithilfe von Filtern wie armid , moveStatusMoveState(verify) usw.</span><span class="sxs-lookup"><span data-stu-id="7651c-115">Get details of a specific resources in a Move collection using filter such as armid ,moveStatusMoveState(verify) etc.</span></span>

## <span data-ttu-id="7651c-116">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="7651c-116">PARAMETERS</span></span>

### <span data-ttu-id="7651c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7651c-117">-DefaultProfile</span></span>
<span data-ttu-id="7651c-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7651c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7651c-119">-Filter</span><span class="sxs-lookup"><span data-stu-id="7651c-119">-Filter</span></span>
<span data-ttu-id="7651c-120">Der Filter, der für den Vorgang angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="7651c-120">The filter to apply on the operation.</span></span>
<span data-ttu-id="7651c-121">Sie können z. B. $filter=Properties/ProvisioningState eq 'Succeeded' verwenden.</span><span class="sxs-lookup"><span data-stu-id="7651c-121">For example, you can use $filter=Properties/ProvisioningState eq 'Succeeded'.</span></span>

```yaml
Type: System.String
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7651c-122">-MoveCollectionName</span><span class="sxs-lookup"><span data-stu-id="7651c-122">-MoveCollectionName</span></span>
<span data-ttu-id="7651c-123">Der Name der Sammlung verschieben.</span><span class="sxs-lookup"><span data-stu-id="7651c-123">The Move Collection Name.</span></span>

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

### <span data-ttu-id="7651c-124">-Name</span><span class="sxs-lookup"><span data-stu-id="7651c-124">-Name</span></span>
<span data-ttu-id="7651c-125">Der Name der Ressource verschieben.</span><span class="sxs-lookup"><span data-stu-id="7651c-125">The Move Resource Name.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: MoveResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7651c-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7651c-126">-ResourceGroupName</span></span>
<span data-ttu-id="7651c-127">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="7651c-127">The Resource Group Name.</span></span>

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

### <span data-ttu-id="7651c-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7651c-128">-SubscriptionId</span></span>
<span data-ttu-id="7651c-129">Die Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="7651c-129">The Subscription ID.</span></span>

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

### <span data-ttu-id="7651c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7651c-130">CommonParameters</span></span>
<span data-ttu-id="7651c-131">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7651c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7651c-132">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7651c-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7651c-133">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="7651c-133">INPUTS</span></span>

## <span data-ttu-id="7651c-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="7651c-134">OUTPUTS</span></span>

### <span data-ttu-id="7651c-135">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api202101.IMoveResource</span><span class="sxs-lookup"><span data-stu-id="7651c-135">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api202101.IMoveResource</span></span>

## <span data-ttu-id="7651c-136">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="7651c-136">NOTES</span></span>

<span data-ttu-id="7651c-137">ALIASE</span><span class="sxs-lookup"><span data-stu-id="7651c-137">ALIASES</span></span>

## <span data-ttu-id="7651c-138">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="7651c-138">RELATED LINKS</span></span>

