---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azddosprotectionplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzDdosProtectionPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzDdosProtectionPlan.md
ms.openlocfilehash: 2b5cc008e96d12828d5f834fd5fa4a30f83ea70f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101926592"
---
# <span data-ttu-id="6f064-101">Get-AzDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="6f064-101">Get-AzDdosProtectionPlan</span></span>

## <span data-ttu-id="6f064-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6f064-102">SYNOPSIS</span></span>
<span data-ttu-id="6f064-103">Ruft einen DDoS-Schutzplan ab.</span><span class="sxs-lookup"><span data-stu-id="6f064-103">Gets a DDoS protection plan.</span></span>

## <span data-ttu-id="6f064-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6f064-104">SYNTAX</span></span>

```
Get-AzDdosProtectionPlan [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6f064-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6f064-105">DESCRIPTION</span></span>
<span data-ttu-id="6f064-106">Das Get-AzDdosProtectionPlan-Cmdlet erhält einen DDoS-Schutzplan.</span><span class="sxs-lookup"><span data-stu-id="6f064-106">The Get-AzDdosProtectionPlan cmdlet gets a DDoS protection plan.</span></span>

## <span data-ttu-id="6f064-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="6f064-107">EXAMPLES</span></span>

### <span data-ttu-id="6f064-108">Beispiel 1: Erhalten eines bestimmten DDoS-Schutzplans</span><span class="sxs-lookup"><span data-stu-id="6f064-108">Example 1: Get a specific DDoS protection plan</span></span>
```
D:\> Get-AzDdosProtectionPlan -ResourceGroupName ResourceGroupName -Name DdosProtectionPlanName


Name              : DdosProtectionPlanName
Id                : /subscriptions/d1dbd366-9871-45ac-84b7-fb318152a9e0/resourceGroups/ResourceGroupName/providers/Microsoft.Network/ddosProtectionPlans/DdosProtectionPlanName
Etag              : W/"a20e5592-9b51-423b-9758-b00cd322f744"
ProvisioningState : Succeeded
VirtualNetworks   : [
                      {
                        "Id": "/subscriptions/d1dbd366-9871-45ac-84b7-fb318152a9e0/resourceGroups/ResourceGroupName/providers/Microsoft.Network/virtualNetworks/VnetName"
                      }
                    ]
```

<span data-ttu-id="6f064-109">In diesem Fall müssen wir sowohl **ResourceGroupName-** als auch **Name-Attribute** angeben, die der Ressourcengruppe bzw. dem Namen des DDoS-Schutzplans entsprechen.</span><span class="sxs-lookup"><span data-stu-id="6f064-109">In this case, we need to specify both **ResourceGroupName** and **Name** attributes, which correspond to the resource group and the name of the DDoS protection plan, respectively.</span></span>

### <span data-ttu-id="6f064-110">Beispiel 2: Alle DDoS-Schutzpläne in einer Ressourcengruppe erhalten</span><span class="sxs-lookup"><span data-stu-id="6f064-110">Example 2: Get all DDoS protection plans in a resource group</span></span>
```
D:\> Get-AzDdosProtectionPlan -ResourceGroupName ResourceGroupName


Name              : DdosProtectionPlanName
Id                : /subscriptions/d1dbd366-9871-45ac-84b7-fb318152a9e0/resourceGroups/ResourceGroupName/providers/Microsoft.Network/ddosProtectionPlans/DdosProtectionPlanName
Etag              : W/"a20e5592-9b51-423b-9758-b00cd322f744"
ProvisioningState : Succeeded
VirtualNetworks   : [
                      {
                        "Id": "/subscriptions/d1dbd366-9871-45ac-84b7-fb318152a9e0/resourceGroups/ResourceGroupName/providers/Microsoft.Network/virtualNetworks/VnetName"
                      }
                    ]
```

<span data-ttu-id="6f064-111">In diesem Szenario geben wir nur den Parameter **ResourceGroupName an,** um eine Liste der DDoS-Schutzpläne zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="6f064-111">In this scenario, we only specify the parameter **ResourceGroupName** to get a list of DDoS protection plans.</span></span>

### <span data-ttu-id="6f064-112">Beispiel 3: Alle DDoS-Schutzpläne in einem Abonnement erhalten</span><span class="sxs-lookup"><span data-stu-id="6f064-112">Example 3: Get all DDoS protection plans in a subscription</span></span>
```
D:\> Get-AzDdosProtectionPlan


Name              : DdosProtectionPlanName
Id                : /subscriptions/d1dbd366-9871-45ac-84b7-fb318152a9e0/resourceGroups/ResourceGroupName/providers/Microsoft.Network/ddosProtectionPlans/DdosProtectionPlanName
Etag              : W/"a20e5592-9b51-423b-9758-b00cd322f744"
ProvisioningState : Succeeded
VirtualNetworks   : [
                      {
                        "Id": "/subscriptions/d1dbd366-9871-45ac-84b7-fb318152a9e0/resourceGroups/ResourceGroupName/providers/Microsoft.Network/virtualNetworks/VnetName"
                      }
                    ]
```

<span data-ttu-id="6f064-113">Hier geben wir keine Parameter an, um eine Liste aller DDoS-Schutzpläne in einem Abonnement zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="6f064-113">Here, we do not specify any parameters to get a list of all DDoS protection plans in a subscription.</span></span>

### <span data-ttu-id="6f064-114">Beispiel 4: Alle DDoS-Schutzpläne in einem Abonnement erhalten</span><span class="sxs-lookup"><span data-stu-id="6f064-114">Example 4: Get all DDoS protection plans in a subscription</span></span>
```
D:\> Get-AzDdosProtectionPlan -Name test*


Name              : test1
Id                : /subscriptions/d1dbd366-9871-45ac-84b7-fb318152a9e0/resourceGroups/ResourceGroupName/providers/Microsoft.Network/ddosProtectionPlans/test1
Etag              : W/"a20e5592-9b51-423b-9758-b00cd322f744"
ProvisioningState : Succeeded
VirtualNetworks   : [
                      {
                        "Id": "/subscriptions/d1dbd366-9871-45ac-84b7-fb318152a9e0/resourceGroups/ResourceGroupName/providers/Microsoft.Network/virtualNetworks/VnetName"
                      }
                    ]

Name              : test2
Id                : /subscriptions/d1dbd366-9871-45ac-84b7-fb318152a9e0/resourceGroups/ResourceGroupName/providers/Microsoft.Network/ddosProtectionPlans/test2
Etag              : W/"a20e5592-9b51-423b-9758-b00cd322f744"
ProvisioningState : Succeeded
VirtualNetworks   : [
                      {
                        "Id": "/subscriptions/d1dbd366-9871-45ac-84b7-fb318152a9e0/resourceGroups/ResourceGroupName/providers/Microsoft.Network/virtualNetworks/VnetName"
                      }
                    ]
```

<span data-ttu-id="6f064-115">Dieses Cmdlet gibt alle DdosProtectionPlans zurück, die mit "test" beginnen.</span><span class="sxs-lookup"><span data-stu-id="6f064-115">This cmdlet returns all DdosProtectionPlans that start with "test".</span></span>

## <span data-ttu-id="6f064-116">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="6f064-116">PARAMETERS</span></span>

### <span data-ttu-id="6f064-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f064-117">-DefaultProfile</span></span>
<span data-ttu-id="6f064-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6f064-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6f064-119">-Name</span><span class="sxs-lookup"><span data-stu-id="6f064-119">-Name</span></span>
<span data-ttu-id="6f064-120">Gibt den Namen des DDoS-Schutzplans an.</span><span class="sxs-lookup"><span data-stu-id="6f064-120">Specifies the name of the DDoS protection plan.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="6f064-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6f064-121">-ResourceGroupName</span></span>
<span data-ttu-id="6f064-122">Gibt den Namen der Ressourcengruppe des DDoS-Schutzplans an.</span><span class="sxs-lookup"><span data-stu-id="6f064-122">Specifies the name of the DDoS protection plan resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="6f064-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f064-123">CommonParameters</span></span>
<span data-ttu-id="6f064-124">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6f064-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f064-125">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6f064-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f064-126">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="6f064-126">INPUTS</span></span>

### <span data-ttu-id="6f064-127">System.String</span><span class="sxs-lookup"><span data-stu-id="6f064-127">System.String</span></span>

## <span data-ttu-id="6f064-128">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="6f064-128">OUTPUTS</span></span>

### <span data-ttu-id="6f064-129">Microsoft.Azure.Commands.Network.Models.PSDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="6f064-129">Microsoft.Azure.Commands.Network.Models.PSDdosProtectionPlan</span></span>

## <span data-ttu-id="6f064-130">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="6f064-130">NOTES</span></span>

## <span data-ttu-id="6f064-131">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="6f064-131">RELATED LINKS</span></span>

[<span data-ttu-id="6f064-132">New-AzDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="6f064-132">New-AzDdosProtectionPlan</span></span>](./New-AzDdosProtectionPlan.md)

[<span data-ttu-id="6f064-133">Remove-AzDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="6f064-133">Remove-AzDdosProtectionPlan</span></span>](./Remove-AzDdosProtectionPlan.md)

[<span data-ttu-id="6f064-134">New-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="6f064-134">New-AzVirtualNetwork</span></span>](./New-AzVirtualNetwork.md)

[<span data-ttu-id="6f064-135">Set-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="6f064-135">Set-AzVirtualNetwork</span></span>](./Set-AzVirtualNetwork.md)

[<span data-ttu-id="6f064-136">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="6f064-136">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)