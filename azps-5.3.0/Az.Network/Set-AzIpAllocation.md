---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azipallocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzIpAllocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzIpAllocation.md
ms.openlocfilehash: 4d817dcabe73972b3a8f21de5b9b0906d7a95cc2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98473405"
---
# <span data-ttu-id="47d00-101">Set-AzIpAllocation</span><span class="sxs-lookup"><span data-stu-id="47d00-101">Set-AzIpAllocation</span></span>

## <span data-ttu-id="47d00-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="47d00-102">SYNOPSIS</span></span>
<span data-ttu-id="47d00-103">Speichert eine geänderte IpAllocation.</span><span class="sxs-lookup"><span data-stu-id="47d00-103">Saves a modified IpAllocation.</span></span>

## <span data-ttu-id="47d00-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="47d00-104">SYNTAX</span></span>

### <span data-ttu-id="47d00-105">SetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="47d00-105">SetByNameParameterSet</span></span>
```
Set-AzIpAllocation [-ResourceGroupName] <String> [-Name] <String> [-IpAllocationTag <Hashtable>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="47d00-106">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="47d00-106">SetByResourceIdParameterSet</span></span>
```
Set-AzIpAllocation [-ResourceId] <String> [-IpAllocationTag <Hashtable>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="47d00-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="47d00-107">SetByInputObjectParameterSet</span></span>
```
Set-AzIpAllocation [-InputObject] <PSIpAllocation> [-IpAllocationTag <Hashtable>] [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="47d00-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="47d00-108">DESCRIPTION</span></span>
<span data-ttu-id="47d00-109">Das **Cmdlet "Set-AzIpAllocation"** aktualisiert eine Azure IpAllocation</span><span class="sxs-lookup"><span data-stu-id="47d00-109">The **Set-AzIpAllocation** cmdlet updates an Azure IpAllocation</span></span>

## <span data-ttu-id="47d00-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="47d00-110">EXAMPLES</span></span>

### <span data-ttu-id="47d00-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="47d00-111">Example 1</span></span>
```powershell
Set-AzIpAllocation -ResourceGroupName 'TestResourceGroup' -Name 'TestIpAllocation'  -IpAllocationTag @{"VnetId"="vnet1"}  -Tag @{"TestTag"="TestValue"}
```

## <span data-ttu-id="47d00-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="47d00-112">PARAMETERS</span></span>

### <span data-ttu-id="47d00-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="47d00-113">-AsJob</span></span>
<span data-ttu-id="47d00-114">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="47d00-114">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47d00-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47d00-115">-DefaultProfile</span></span>
<span data-ttu-id="47d00-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="47d00-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="47d00-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="47d00-117">-InputObject</span></span>
<span data-ttu-id="47d00-118">The IpAllocation</span><span class="sxs-lookup"><span data-stu-id="47d00-118">The IpAllocation</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSIpAllocation
Parameter Sets: SetByInputObjectParameterSet
Aliases: IpAllocation

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="47d00-119">-IpAllocationTag</span><span class="sxs-lookup"><span data-stu-id="47d00-119">-IpAllocationTag</span></span>
<span data-ttu-id="47d00-120">Die Zuordnungstags der IP-Zuweisung</span><span class="sxs-lookup"><span data-stu-id="47d00-120">The allocation tags of the IP allocation</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47d00-121">-Name</span><span class="sxs-lookup"><span data-stu-id="47d00-121">-Name</span></span>
<span data-ttu-id="47d00-122">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="47d00-122">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47d00-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47d00-123">-ResourceGroupName</span></span>
<span data-ttu-id="47d00-124">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="47d00-124">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47d00-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="47d00-125">-ResourceId</span></span>
<span data-ttu-id="47d00-126">IpAllocation-ID</span><span class="sxs-lookup"><span data-stu-id="47d00-126">IpAllocation Id</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases: IpAllocationId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47d00-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="47d00-127">-Tag</span></span>
<span data-ttu-id="47d00-128">Eine Hashtable, die Ressourcentags darstellt.</span><span class="sxs-lookup"><span data-stu-id="47d00-128">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47d00-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47d00-129">CommonParameters</span></span>
<span data-ttu-id="47d00-130">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47d00-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47d00-131">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="47d00-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47d00-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="47d00-132">INPUTS</span></span>

### <span data-ttu-id="47d00-133">Microsoft.Azure.Commands.Network.Models.PSIpAllocation</span><span class="sxs-lookup"><span data-stu-id="47d00-133">Microsoft.Azure.Commands.Network.Models.PSIpAllocation</span></span>

## <span data-ttu-id="47d00-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="47d00-134">OUTPUTS</span></span>

### <span data-ttu-id="47d00-135">Microsoft.Azure.Commands.Network.Models.PSIpAllocation</span><span class="sxs-lookup"><span data-stu-id="47d00-135">Microsoft.Azure.Commands.Network.Models.PSIpAllocation</span></span>

## <span data-ttu-id="47d00-136">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="47d00-136">NOTES</span></span>

## <span data-ttu-id="47d00-137">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="47d00-137">RELATED LINKS</span></span>
