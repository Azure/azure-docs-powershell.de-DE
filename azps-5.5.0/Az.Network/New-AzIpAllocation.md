---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azipallocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpAllocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpAllocation.md
ms.openlocfilehash: 9a6c84c0ff5d22a4f6c6038266598c6adfe19b29
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100151684"
---
# <span data-ttu-id="1bee3-101">New-AzIpAllocation</span><span class="sxs-lookup"><span data-stu-id="1bee3-101">New-AzIpAllocation</span></span>

## <span data-ttu-id="1bee3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1bee3-102">SYNOPSIS</span></span>
<span data-ttu-id="1bee3-103">Erstellt eine Azure IpAllocation.</span><span class="sxs-lookup"><span data-stu-id="1bee3-103">Creates an Azure IpAllocation.</span></span>

## <span data-ttu-id="1bee3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1bee3-104">SYNTAX</span></span>

```
New-AzIpAllocation -Name <String> -ResourceGroupName <String> -Location <String>
 -IpAllocationType <String> [-Prefix <String>] [-PrefixLength <Int32>] [-PrefixType <String>]
 [-IpamAllocationId <String>] [-IpAllocationTag <Hashtable>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1bee3-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1bee3-105">DESCRIPTION</span></span>
<span data-ttu-id="1bee3-106">Das **Cmdlet "New-AzIpAllocation"** erstellt eine Azure IpAllocation</span><span class="sxs-lookup"><span data-stu-id="1bee3-106">The **New-AzIpAllocation** cmdlet creates an Azure IpAllocation</span></span>

## <span data-ttu-id="1bee3-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="1bee3-107">EXAMPLES</span></span>

### <span data-ttu-id="1bee3-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="1bee3-108">Example 1</span></span>
```powershell
New-AzIpAllocation -ResourceName 'TestIpAllocation'  -ResourceGroupName 'TestResourcegroupName' -Location 'eastus' -IpAllocationType 'Hypernet' -Prefix '1.2.3.4/32' -IpAllocationTag @{"VnetId"="vnet1"}
```

### <span data-ttu-id="1bee3-109">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="1bee3-109">Example 2</span></span>
```powershell
New-AzIpAllocation -ResourceName 'TestIpAllocation'  -ResourceGroupName 'TestResourcegroupName' -Location 'eastus' -IpAllocationType 'Hypernet' -PrefixLength 32 -PrefixType 'ipv4' -IpAllocationTag @{"VnetId"="vnet1"}
```

## <span data-ttu-id="1bee3-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1bee3-110">PARAMETERS</span></span>

### <span data-ttu-id="1bee3-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1bee3-111">-AsJob</span></span>
<span data-ttu-id="1bee3-112">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="1bee3-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1bee3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1bee3-113">-DefaultProfile</span></span>
<span data-ttu-id="1bee3-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1bee3-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1bee3-115">-Force</span><span class="sxs-lookup"><span data-stu-id="1bee3-115">-Force</span></span>
<span data-ttu-id="1bee3-116">Bestätigen Sie sie nicht, wenn Sie eine Ressource außer Kraft setzen möchten.</span><span class="sxs-lookup"><span data-stu-id="1bee3-116">Do not ask for confirmation if you want to override a resource</span></span>

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

### <span data-ttu-id="1bee3-117">-IpAllocationTag</span><span class="sxs-lookup"><span data-stu-id="1bee3-117">-IpAllocationTag</span></span>
<span data-ttu-id="1bee3-118">Die Zuordnungstags der IP-Zuweisung</span><span class="sxs-lookup"><span data-stu-id="1bee3-118">The allocation tags of the IP allocation</span></span>

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

### <span data-ttu-id="1bee3-119">-IpAllocationType</span><span class="sxs-lookup"><span data-stu-id="1bee3-119">-IpAllocationType</span></span>
<span data-ttu-id="1bee3-120">Der Typ der IP-Zuweisung</span><span class="sxs-lookup"><span data-stu-id="1bee3-120">The type of the IP allocation</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Hypernet, Undefined

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1bee3-121">-IpamAllocationId</span><span class="sxs-lookup"><span data-stu-id="1bee3-121">-IpamAllocationId</span></span>
<span data-ttu-id="1bee3-122">Die Ipam-Zuweisungs-ID der IP-Zuweisung</span><span class="sxs-lookup"><span data-stu-id="1bee3-122">The ipam allocation ID of the IP allocation</span></span>

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

### <span data-ttu-id="1bee3-123">-Location</span><span class="sxs-lookup"><span data-stu-id="1bee3-123">-Location</span></span>
<span data-ttu-id="1bee3-124">aus.</span><span class="sxs-lookup"><span data-stu-id="1bee3-124">location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1bee3-125">-Name</span><span class="sxs-lookup"><span data-stu-id="1bee3-125">-Name</span></span>
<span data-ttu-id="1bee3-126">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="1bee3-126">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1bee3-127">-Prefix</span><span class="sxs-lookup"><span data-stu-id="1bee3-127">-Prefix</span></span>
<span data-ttu-id="1bee3-128">Das Präfix der IP-Zuweisung</span><span class="sxs-lookup"><span data-stu-id="1bee3-128">The prefix of the IP allocation</span></span>

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

### <span data-ttu-id="1bee3-129">-PrefixLength</span><span class="sxs-lookup"><span data-stu-id="1bee3-129">-PrefixLength</span></span>
<span data-ttu-id="1bee3-130">Die Präfixlänge der IP-Zuweisung</span><span class="sxs-lookup"><span data-stu-id="1bee3-130">The prefix length of the IP allocation</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1bee3-131">-PrefixType</span><span class="sxs-lookup"><span data-stu-id="1bee3-131">-PrefixType</span></span>
<span data-ttu-id="1bee3-132">Der Präfixtyp der IP-Zuweisung</span><span class="sxs-lookup"><span data-stu-id="1bee3-132">The prefix type of the IP allocation</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: IPV4, IPV6

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1bee3-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1bee3-133">-ResourceGroupName</span></span>
<span data-ttu-id="1bee3-134">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="1bee3-134">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1bee3-135">-Tag</span><span class="sxs-lookup"><span data-stu-id="1bee3-135">-Tag</span></span>
<span data-ttu-id="1bee3-136">Eine Hashtable, die Ressourcentags darstellt.</span><span class="sxs-lookup"><span data-stu-id="1bee3-136">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="1bee3-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1bee3-137">-Confirm</span></span>
<span data-ttu-id="1bee3-138">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1bee3-138">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1bee3-139">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="1bee3-139">-WhatIf</span></span>
<span data-ttu-id="1bee3-140">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1bee3-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1bee3-141">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1bee3-141">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1bee3-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1bee3-142">CommonParameters</span></span>
<span data-ttu-id="1bee3-143">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1bee3-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1bee3-144">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1bee3-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1bee3-145">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="1bee3-145">INPUTS</span></span>

### <span data-ttu-id="1bee3-146">System.String</span><span class="sxs-lookup"><span data-stu-id="1bee3-146">System.String</span></span>

### <span data-ttu-id="1bee3-147">System.Nullable'1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="1bee3-147">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="1bee3-148">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="1bee3-148">System.Collections.Hashtable</span></span>

## <span data-ttu-id="1bee3-149">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="1bee3-149">OUTPUTS</span></span>

### <span data-ttu-id="1bee3-150">Microsoft.Azure.Commands.Network.Models.PSIpAllocation</span><span class="sxs-lookup"><span data-stu-id="1bee3-150">Microsoft.Azure.Commands.Network.Models.PSIpAllocation</span></span>

## <span data-ttu-id="1bee3-151">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="1bee3-151">NOTES</span></span>

## <span data-ttu-id="1bee3-152">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="1bee3-152">RELATED LINKS</span></span>
