---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationsecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationSecurityGroup.md
ms.openlocfilehash: aa03f7d410d704e8e5b9ea4b974e3050a3304342
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98467388"
---
# <span data-ttu-id="1d3de-101">Get-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="1d3de-101">Get-AzApplicationSecurityGroup</span></span>

## <span data-ttu-id="1d3de-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1d3de-102">SYNOPSIS</span></span>
<span data-ttu-id="1d3de-103">Ruft eine Anwendungssicherheitsgruppe ab.</span><span class="sxs-lookup"><span data-stu-id="1d3de-103">Gets an application security group.</span></span>

## <span data-ttu-id="1d3de-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1d3de-104">SYNTAX</span></span>

```
Get-AzApplicationSecurityGroup [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1d3de-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1d3de-105">DESCRIPTION</span></span>
<span data-ttu-id="1d3de-106">Das **Cmdlet "Get-AzApplicationSecurityGroup"** ruft eine Anwendungssicherheitsgruppe ab.</span><span class="sxs-lookup"><span data-stu-id="1d3de-106">The **Get-AzApplicationSecurityGroup** cmdlet gets an application security group.</span></span>

## <span data-ttu-id="1d3de-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="1d3de-107">EXAMPLES</span></span>

### <span data-ttu-id="1d3de-108">Beispiel 1: Rufen Sie alle Anwendungssicherheitsgruppen ab.</span><span class="sxs-lookup"><span data-stu-id="1d3de-108">Example 1: Retrieve all application security groups.</span></span>
```
PS C:\> Get-AzApplicationSecurityGroup

ProvisioningState : Succeeded
ResourceGroupName : MyResourceGroup
Location          : southcentralus
ResourceGuid      :
Type              : Microsoft.Network/applicationSecurityGroups
Tag               : {}
TagsTable         :
Name              : MyApplicationSecurityGroup1
Etag              : W/"00000000-0000-0000-0000-000000000000"
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/MyResourceGroup/providers/Microsof
                    t.Network/applicationSecurityGroups/MyApplicationSecurityGroup1

ProvisioningState : Succeeded
ResourceGroupName : MyResourceGroup
Location          : southcentralus
ResourceGuid      :
Type              : Microsoft.Network/applicationSecurityGroups
Tag               : {}
TagsTable         :
Name              : MyApplicationSecurityGroup2
Etag              : W/"00000000-0000-0000-0000-000000000000"
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/MyResourceGroup/providers/Microsof
                    t.Network/applicationSecurityGroups/MyApplicationSecurityGroup2
```

<span data-ttu-id="1d3de-109">Der oben aufgeführte Befehl gibt alle Anwendungssicherheitsgruppen im Abonnement zurück.</span><span class="sxs-lookup"><span data-stu-id="1d3de-109">The command above returns the all application security groups in the subscription.</span></span>

### <span data-ttu-id="1d3de-110">Beispiel 2: Abrufen von Anwendungssicherheitsgruppen in einer Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="1d3de-110">Example 2: Retrieve application security groups in a resource group.</span></span>
```
PS C:\> Get-AzApplicationSecurityGroup -ResourceGroupName MyResourceGroup

ProvisioningState : Succeeded
ResourceGroupName : MyResourceGroup
Location          : southcentralus
ResourceGuid      :
Type              : Microsoft.Network/applicationSecurityGroups
Tag               : {}
TagsTable         :
Name              : MyApplicationSecurityGroup1
Etag              : W/"00000000-0000-0000-0000-000000000000"
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/MyResourceGroup/providers/Microsof
                    t.Network/applicationSecurityGroups/MyApplicationSecurityGroup1

ProvisioningState : Succeeded
ResourceGroupName : MyResourceGroup
Location          : southcentralus
ResourceGuid      :
Type              : Microsoft.Network/applicationSecurityGroups
Tag               : {}
TagsTable         :
Name              : MyApplicationSecurityGroup2
Etag              : W/"00000000-0000-0000-0000-000000000000"
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/MyResourceGroup/providers/Microsof
                    t.Network/applicationSecurityGroups/MyApplicationSecurityGroup2
```

<span data-ttu-id="1d3de-111">Der oben aufgeführte Befehl gibt alle Anwendungssicherheitsgruppen zurück, die zur Ressourcengruppe "MyResourceGroup" gehören.</span><span class="sxs-lookup"><span data-stu-id="1d3de-111">The command above returns all application security groups that belong to the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="1d3de-112">Beispiel 3: Abrufen einer bestimmten Anwendungssicherheitsgruppe.</span><span class="sxs-lookup"><span data-stu-id="1d3de-112">Example 3: Retrieve a specific application security group.</span></span>
```
PS C:\> Get-AzApplicationSecurityGroup -ResourceGroupName MyResourceGroup -Name MyApplicationSecurityGroup1

ProvisioningState : Succeeded
ResourceGroupName : MyResourceGroup
Location          : southcentralus
ResourceGuid      :
Type              : Microsoft.Network/applicationSecurityGroups
Tag               : {}
TagsTable         :
Name              : MyApplicationSecurityGroup1
Etag              : W/"00000000-0000-0000-0000-000000000000"
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/MyResourceGroup/providers/Microsof
                    t.Network/applicationSecurityGroups/MyApplicationSecurityGroup1
```

<span data-ttu-id="1d3de-113">Der oben aufgeführte Befehl gibt die Anwendungssicherheitsgruppe "MyApplicationSecurityGroup" unter der Ressourcengruppe "MyResourceGroup" zurück.</span><span class="sxs-lookup"><span data-stu-id="1d3de-113">The command above returns the application security group MyApplicationSecurityGroup under the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="1d3de-114">Beispiel 4: Abrufen von Anwendungssicherheitsgruppen mithilfe der Filterung.</span><span class="sxs-lookup"><span data-stu-id="1d3de-114">Example 4: Retrieve application security groups using filtering.</span></span>
```
PS C:\> Get-AzApplicationSecurityGroup -Name MyApplicationSecurityGroup*

ProvisioningState : Succeeded
ResourceGroupName : MyResourceGroup
Location          : southcentralus
ResourceGuid      :
Type              : Microsoft.Network/applicationSecurityGroups
Tag               : {}
TagsTable         :
Name              : MyApplicationSecurityGroup1
Etag              : W/"00000000-0000-0000-0000-000000000000"
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/MyResourceGroup/providers/Microsof
                    t.Network/applicationSecurityGroups/MyApplicationSecurityGroup1

ProvisioningState : Succeeded
ResourceGroupName : MyResourceGroup
Location          : southcentralus
ResourceGuid      :
Type              : Microsoft.Network/applicationSecurityGroups
Tag               : {}
TagsTable         :
Name              : MyApplicationSecurityGroup2
Etag              : W/"00000000-0000-0000-0000-000000000000"
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/MyResourceGroup/providers/Microsof
                    t.Network/applicationSecurityGroups/MyApplicationSecurityGroup2
```

<span data-ttu-id="1d3de-115">Der oben aufgeführte Befehl gibt alle Anwendungssicherheitsgruppen zurück, die mit "MyApplicationSecurityGroup" beginnen.</span><span class="sxs-lookup"><span data-stu-id="1d3de-115">The command above returns all application security groups that start with "MyApplicationSecurityGroup".</span></span>

## <span data-ttu-id="1d3de-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1d3de-116">PARAMETERS</span></span>

### <span data-ttu-id="1d3de-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d3de-117">-DefaultProfile</span></span>
<span data-ttu-id="1d3de-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1d3de-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1d3de-119">-Name</span><span class="sxs-lookup"><span data-stu-id="1d3de-119">-Name</span></span>
<span data-ttu-id="1d3de-120">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="1d3de-120">The resource name.</span></span>

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

### <span data-ttu-id="1d3de-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1d3de-121">-ResourceGroupName</span></span>
<span data-ttu-id="1d3de-122">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="1d3de-122">The resource group name.</span></span>

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

### <span data-ttu-id="1d3de-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d3de-123">CommonParameters</span></span>
<span data-ttu-id="1d3de-124">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1d3de-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d3de-125">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1d3de-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d3de-126">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="1d3de-126">INPUTS</span></span>

### <span data-ttu-id="1d3de-127">System.String</span><span class="sxs-lookup"><span data-stu-id="1d3de-127">System.String</span></span>

## <span data-ttu-id="1d3de-128">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="1d3de-128">OUTPUTS</span></span>

### <span data-ttu-id="1d3de-129">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="1d3de-129">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup</span></span>

## <span data-ttu-id="1d3de-130">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="1d3de-130">NOTES</span></span>

## <span data-ttu-id="1d3de-131">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="1d3de-131">RELATED LINKS</span></span>

[<span data-ttu-id="1d3de-132">New-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="1d3de-132">New-AzApplicationSecurityGroup</span></span>](./New-AzApplicationSecurityGroup.md)

[<span data-ttu-id="1d3de-133">Remove-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="1d3de-133">Remove-AzApplicationSecurityGroup</span></span>](./Remove-AzApplicationSecurityGroup.md)

[<span data-ttu-id="1d3de-134">Get-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1d3de-134">Get-AzNetworkSecurityRuleConfig</span></span>](./Get-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="1d3de-135">Get-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="1d3de-135">Get-AzNetworkInterfaceIpConfig</span></span>](./Get-AzNetworkInterfaceIpConfig.md)
