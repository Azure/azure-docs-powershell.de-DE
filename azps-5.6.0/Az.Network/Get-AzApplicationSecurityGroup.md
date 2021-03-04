---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azapplicationsecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationSecurityGroup.md
ms.openlocfilehash: 52b6a4b7c5f78359ffc046953101aaa01bb7a435
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101940259"
---
# <span data-ttu-id="aed6e-101">Get-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="aed6e-101">Get-AzApplicationSecurityGroup</span></span>

## <span data-ttu-id="aed6e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aed6e-102">SYNOPSIS</span></span>
<span data-ttu-id="aed6e-103">Ruft eine Anwendungssicherheitsgruppe ab.</span><span class="sxs-lookup"><span data-stu-id="aed6e-103">Gets an application security group.</span></span>

## <span data-ttu-id="aed6e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="aed6e-104">SYNTAX</span></span>

```
Get-AzApplicationSecurityGroup [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aed6e-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="aed6e-105">DESCRIPTION</span></span>
<span data-ttu-id="aed6e-106">Das **Get-AzApplicationSecurityGroup-Cmdlet** ruft eine Anwendungssicherheitsgruppe ab.</span><span class="sxs-lookup"><span data-stu-id="aed6e-106">The **Get-AzApplicationSecurityGroup** cmdlet gets an application security group.</span></span>

## <span data-ttu-id="aed6e-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="aed6e-107">EXAMPLES</span></span>

### <span data-ttu-id="aed6e-108">Beispiel 1: Abrufen aller Anwendungssicherheitsgruppen.</span><span class="sxs-lookup"><span data-stu-id="aed6e-108">Example 1: Retrieve all application security groups.</span></span>
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

<span data-ttu-id="aed6e-109">Der obige Befehl gibt alle Anwendungssicherheitsgruppen im Abonnement zurück.</span><span class="sxs-lookup"><span data-stu-id="aed6e-109">The command above returns the all application security groups in the subscription.</span></span>

### <span data-ttu-id="aed6e-110">Beispiel 2: Abrufen von Anwendungssicherheitsgruppen in einer Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="aed6e-110">Example 2: Retrieve application security groups in a resource group.</span></span>
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

<span data-ttu-id="aed6e-111">Der obige Befehl gibt alle Anwendungssicherheitsgruppen zurück, die zur Ressourcengruppe MyResourceGroup gehören.</span><span class="sxs-lookup"><span data-stu-id="aed6e-111">The command above returns all application security groups that belong to the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="aed6e-112">Beispiel 3: Abrufen einer bestimmten Anwendungssicherheitsgruppe.</span><span class="sxs-lookup"><span data-stu-id="aed6e-112">Example 3: Retrieve a specific application security group.</span></span>
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

<span data-ttu-id="aed6e-113">Der obige Befehl gibt die Anwendungssicherheitsgruppe MyApplicationSecurityGroup unter der Ressourcengruppe MyResourceGroup zurück.</span><span class="sxs-lookup"><span data-stu-id="aed6e-113">The command above returns the application security group MyApplicationSecurityGroup under the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="aed6e-114">Beispiel 4: Abrufen von Anwendungssicherheitsgruppen mithilfe von Filtern.</span><span class="sxs-lookup"><span data-stu-id="aed6e-114">Example 4: Retrieve application security groups using filtering.</span></span>
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

<span data-ttu-id="aed6e-115">Der obige Befehl gibt alle Anwendungssicherheitsgruppen zurück, die mit "MyApplicationSecurityGroup" beginnen.</span><span class="sxs-lookup"><span data-stu-id="aed6e-115">The command above returns all application security groups that start with "MyApplicationSecurityGroup".</span></span>

## <span data-ttu-id="aed6e-116">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="aed6e-116">PARAMETERS</span></span>

### <span data-ttu-id="aed6e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aed6e-117">-DefaultProfile</span></span>
<span data-ttu-id="aed6e-118">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="aed6e-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aed6e-119">-Name</span><span class="sxs-lookup"><span data-stu-id="aed6e-119">-Name</span></span>
<span data-ttu-id="aed6e-120">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="aed6e-120">The resource name.</span></span>

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

### <span data-ttu-id="aed6e-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aed6e-121">-ResourceGroupName</span></span>
<span data-ttu-id="aed6e-122">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="aed6e-122">The resource group name.</span></span>

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

### <span data-ttu-id="aed6e-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aed6e-123">CommonParameters</span></span>
<span data-ttu-id="aed6e-124">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aed6e-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aed6e-125">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="aed6e-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aed6e-126">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="aed6e-126">INPUTS</span></span>

### <span data-ttu-id="aed6e-127">System.String</span><span class="sxs-lookup"><span data-stu-id="aed6e-127">System.String</span></span>

## <span data-ttu-id="aed6e-128">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="aed6e-128">OUTPUTS</span></span>

### <span data-ttu-id="aed6e-129">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="aed6e-129">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup</span></span>

## <span data-ttu-id="aed6e-130">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="aed6e-130">NOTES</span></span>

## <span data-ttu-id="aed6e-131">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="aed6e-131">RELATED LINKS</span></span>

[<span data-ttu-id="aed6e-132">New-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="aed6e-132">New-AzApplicationSecurityGroup</span></span>](./New-AzApplicationSecurityGroup.md)

[<span data-ttu-id="aed6e-133">Remove-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="aed6e-133">Remove-AzApplicationSecurityGroup</span></span>](./Remove-AzApplicationSecurityGroup.md)

[<span data-ttu-id="aed6e-134">Get-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="aed6e-134">Get-AzNetworkSecurityRuleConfig</span></span>](./Get-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="aed6e-135">Get-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="aed6e-135">Get-AzNetworkInterfaceIpConfig</span></span>](./Get-AzNetworkInterfaceIpConfig.md)
