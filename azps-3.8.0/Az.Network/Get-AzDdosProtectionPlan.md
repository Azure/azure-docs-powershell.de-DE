---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azddosprotectionplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzDdosProtectionPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzDdosProtectionPlan.md
ms.openlocfilehash: a94ed627d50b8523157d52d3a9c2bf1f8ab29229
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94005161"
---
# <span data-ttu-id="21d8d-101">Get-AzDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="21d8d-101">Get-AzDdosProtectionPlan</span></span>

## <span data-ttu-id="21d8d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="21d8d-102">SYNOPSIS</span></span>
<span data-ttu-id="21d8d-103">Ruft einen DDoS-Schutzplan ab.</span><span class="sxs-lookup"><span data-stu-id="21d8d-103">Gets a DDoS protection plan.</span></span>

## <span data-ttu-id="21d8d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="21d8d-104">SYNTAX</span></span>

```
Get-AzDdosProtectionPlan [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="21d8d-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="21d8d-105">DESCRIPTION</span></span>
<span data-ttu-id="21d8d-106">Das Get-AzDdosProtectionPlan-Cmdlet erhält einen DDoS-Schutzplan.</span><span class="sxs-lookup"><span data-stu-id="21d8d-106">The Get-AzDdosProtectionPlan cmdlet gets a DDoS protection plan.</span></span>

## <span data-ttu-id="21d8d-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="21d8d-107">EXAMPLES</span></span>

### <span data-ttu-id="21d8d-108">Beispiel 1: Abrufen eines speziellen DDoS-Schutzplans</span><span class="sxs-lookup"><span data-stu-id="21d8d-108">Example 1: Get a specific DDoS protection plan</span></span>
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

<span data-ttu-id="21d8d-109">In diesem Fall müssen wir sowohl **ResourceGroupName** -als auch **Name** -Attribute angeben, die der Ressourcengruppe und dem Namen des DDoS-Schutzplans entsprechen.</span><span class="sxs-lookup"><span data-stu-id="21d8d-109">In this case, we need to specify both **ResourceGroupName** and **Name** attributes, which correspond to the resource group and the name of the DDoS protection plan, respectively.</span></span>

### <span data-ttu-id="21d8d-110">Beispiel 2: Abrufen aller DDoS-schutzpläne in einer Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="21d8d-110">Example 2: Get all DDoS protection plans in a resource group</span></span>
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

<span data-ttu-id="21d8d-111">In diesem Szenario geben wir nur den Parameter **ResourceGroupName** an, um eine Liste der DDoS-schutzpläne zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="21d8d-111">In this scenario, we only specify the parameter **ResourceGroupName** to get a list of DDoS protection plans.</span></span>

### <span data-ttu-id="21d8d-112">Beispiel 3: Abrufen aller DDoS-schutzpläne in einem Abonnement</span><span class="sxs-lookup"><span data-stu-id="21d8d-112">Example 3: Get all DDoS protection plans in a subscription</span></span>
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

<span data-ttu-id="21d8d-113">Hier geben wir keine Parameter an, um eine Liste aller DDoS-schutzpläne in einem Abonnement zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="21d8d-113">Here, we do not specify any parameters to get a list of all DDoS protection plans in a subscription.</span></span>

### <span data-ttu-id="21d8d-114">Beispiel 4: Abrufen aller DDoS-schutzpläne in einem Abonnement</span><span class="sxs-lookup"><span data-stu-id="21d8d-114">Example 4: Get all DDoS protection plans in a subscription</span></span>
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

<span data-ttu-id="21d8d-115">Dieses Cmdlet gibt alle DdosProtectionPlans zurück, die mit "Test" beginnen.</span><span class="sxs-lookup"><span data-stu-id="21d8d-115">This cmdlet returns all DdosProtectionPlans that start with "test".</span></span>

## <span data-ttu-id="21d8d-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="21d8d-116">PARAMETERS</span></span>

### <span data-ttu-id="21d8d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21d8d-117">-DefaultProfile</span></span>
<span data-ttu-id="21d8d-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="21d8d-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="21d8d-119">-Name</span><span class="sxs-lookup"><span data-stu-id="21d8d-119">-Name</span></span>
<span data-ttu-id="21d8d-120">Gibt den Namen des DDoS-Schutzplans an.</span><span class="sxs-lookup"><span data-stu-id="21d8d-120">Specifies the name of the DDoS protection plan.</span></span>

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

### <span data-ttu-id="21d8d-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="21d8d-121">-ResourceGroupName</span></span>
<span data-ttu-id="21d8d-122">Gibt den Namen der DDoS-Schutzplan-Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="21d8d-122">Specifies the name of the DDoS protection plan resource group.</span></span>

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

### <span data-ttu-id="21d8d-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21d8d-123">CommonParameters</span></span>
<span data-ttu-id="21d8d-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="21d8d-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21d8d-125">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="21d8d-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21d8d-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="21d8d-126">INPUTS</span></span>

### <span data-ttu-id="21d8d-127">System. String</span><span class="sxs-lookup"><span data-stu-id="21d8d-127">System.String</span></span>

## <span data-ttu-id="21d8d-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="21d8d-128">OUTPUTS</span></span>

### <span data-ttu-id="21d8d-129">Microsoft.Azure.Commands.Network.Models.PSDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="21d8d-129">Microsoft.Azure.Commands.Network.Models.PSDdosProtectionPlan</span></span>

## <span data-ttu-id="21d8d-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="21d8d-130">NOTES</span></span>

## <span data-ttu-id="21d8d-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="21d8d-131">RELATED LINKS</span></span>

[<span data-ttu-id="21d8d-132">Neu – AzDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="21d8d-132">New-AzDdosProtectionPlan</span></span>](./New-AzDdosProtectionPlan.md)

[<span data-ttu-id="21d8d-133">Remove-AzDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="21d8d-133">Remove-AzDdosProtectionPlan</span></span>](./Remove-AzDdosProtectionPlan.md)

[<span data-ttu-id="21d8d-134">Neu – AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="21d8d-134">New-AzVirtualNetwork</span></span>](./New-AzVirtualNetwork.md)

[<span data-ttu-id="21d8d-135">Satz-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="21d8d-135">Set-AzVirtualNetwork</span></span>](./Set-AzVirtualNetwork.md)

[<span data-ttu-id="21d8d-136">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="21d8d-136">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)