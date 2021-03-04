---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/new-azhostgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzHostGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzHostGroup.md
ms.openlocfilehash: 69ab5a7ae89184a5d77344d45801da307e7840bd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101922451"
---
# <span data-ttu-id="4e681-101">New-AzHostGroup</span><span class="sxs-lookup"><span data-stu-id="4e681-101">New-AzHostGroup</span></span>

## <span data-ttu-id="4e681-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4e681-102">SYNOPSIS</span></span>
<span data-ttu-id="4e681-103">Erstellt eine Hostgruppe.</span><span class="sxs-lookup"><span data-stu-id="4e681-103">Creates a host group.</span></span>

## <span data-ttu-id="4e681-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4e681-104">SYNTAX</span></span>

```
New-AzHostGroup [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 -PlatformFaultDomain <Int32> [-Zone <String[]>] [-SupportAutomaticPlacement <bool>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4e681-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4e681-105">DESCRIPTION</span></span>
<span data-ttu-id="4e681-106">Mit diesem Cmdlet wird eine Hostgruppe erstellt.</span><span class="sxs-lookup"><span data-stu-id="4e681-106">This cmdlet will create a Host group.</span></span>

## <span data-ttu-id="4e681-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="4e681-107">EXAMPLES</span></span>

### <span data-ttu-id="4e681-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="4e681-108">Example 1</span></span>
```
PS C:\> New-AzHostGroup -ResourceGroupName $resourceGroupName -Name $hostGroupName -Location $location -Zone $zone

ResourceGroupName        : myrg01
PlatformFaultDomainCount : 2
Hosts                    : {/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myrg01/providers/Microsoft.Compute/hostGroups/myhostgroup01/hosts/myhost01}
Zones                    : {1}
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myrg01/providers/Microsoft.Compute/hostGroups/myhostgroup01
Name                     : myhostgroup01
Location                 : eastus
Tags                     : {[key1, val1]}
```

<span data-ttu-id="4e681-109">Mit diesem Befehl wird eine Hostgruppe an der angegebenen Position und Zone erstellt.</span><span class="sxs-lookup"><span data-stu-id="4e681-109">This command creates a host group in the given location and zone.</span></span>

## <span data-ttu-id="4e681-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="4e681-110">PARAMETERS</span></span>

### <span data-ttu-id="4e681-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4e681-111">-AsJob</span></span>
<span data-ttu-id="4e681-112">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="4e681-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4e681-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e681-113">-DefaultProfile</span></span>
<span data-ttu-id="4e681-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4e681-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4e681-115">-Location</span><span class="sxs-lookup"><span data-stu-id="4e681-115">-Location</span></span>
<span data-ttu-id="4e681-116">Gibt den Speicherort an.</span><span class="sxs-lookup"><span data-stu-id="4e681-116">Specifies location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e681-117">-Name</span><span class="sxs-lookup"><span data-stu-id="4e681-117">-Name</span></span>
<span data-ttu-id="4e681-118">Gibt den Namen der Hostgruppe an.</span><span class="sxs-lookup"><span data-stu-id="4e681-118">Specifies the name of the host group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HostGroupName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e681-119">-PlatformFaultDomain</span><span class="sxs-lookup"><span data-stu-id="4e681-119">-PlatformFaultDomain</span></span>
<span data-ttu-id="4e681-120">Gibt die Anzahl der Fehlerdomänen an, die die Hostgruppe umfassen kann.</span><span class="sxs-lookup"><span data-stu-id="4e681-120">Specifies the number of fault domains that the host group can span.</span></span>  <span data-ttu-id="4e681-121">Der Mindestwert ist 1, und der maximal zulässige Wert ist 3.</span><span class="sxs-lookup"><span data-stu-id="4e681-121">The minimum value is 1 and the maximum value is 3.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e681-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e681-122">-ResourceGroupName</span></span>
<span data-ttu-id="4e681-123">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="4e681-123">The name of the resource group.</span></span>

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

### <span data-ttu-id="4e681-124">-Tag</span><span class="sxs-lookup"><span data-stu-id="4e681-124">-Tag</span></span>
<span data-ttu-id="4e681-125">Gibt Kategorien an</span><span class="sxs-lookup"><span data-stu-id="4e681-125">Specifies Tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e681-126">-Zone</span><span class="sxs-lookup"><span data-stu-id="4e681-126">-Zone</span></span>
<span data-ttu-id="4e681-127">Gibt Zonen der Hostgruppe an.</span><span class="sxs-lookup"><span data-stu-id="4e681-127">Specifies Zones of the host group.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e681-128">-SupportAutomaticPlacement</span><span class="sxs-lookup"><span data-stu-id="4e681-128">-SupportAutomaticPlacement</span></span>
<span data-ttu-id="4e681-129">Gibt an, ob HostGroup die automatische Platzierung von vm-n aktiviert.</span><span class="sxs-lookup"><span data-stu-id="4e681-129">Specifies if HostGroup will enable automatic placement of vm's.</span></span>
<span data-ttu-id="4e681-130">Automatische Platzierung bedeutet, dass diese VMs auf dedizierten Hosts platziert werden, die von Azure ausgewählt wurden, unter der dedizierten Hostgruppe.</span><span class="sxs-lookup"><span data-stu-id="4e681-130">Automatic placement means these VMs are placed on dedicated hosts, chosen by Azure, under the dedicated host group.</span></span>
<span data-ttu-id="4e681-131">Wenn nicht angegeben, ist der Standardwert "false".</span><span class="sxs-lookup"><span data-stu-id="4e681-131">If not specified, default value will be false.</span></span>

```yaml
Type: bool
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: True
Accept pipeline input: False
Accept wildcard characters: False
```


### <span data-ttu-id="4e681-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="4e681-132">-Confirm</span></span>
<span data-ttu-id="4e681-133">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4e681-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4e681-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4e681-134">-WhatIf</span></span>
<span data-ttu-id="4e681-135">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4e681-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4e681-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4e681-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4e681-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e681-137">CommonParameters</span></span>
<span data-ttu-id="4e681-138">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4e681-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e681-139">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4e681-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e681-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="4e681-140">INPUTS</span></span>

### <span data-ttu-id="4e681-141">System.String</span><span class="sxs-lookup"><span data-stu-id="4e681-141">System.String</span></span>

## <span data-ttu-id="4e681-142">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="4e681-142">OUTPUTS</span></span>

### <span data-ttu-id="4e681-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSHostGroup</span><span class="sxs-lookup"><span data-stu-id="4e681-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSHostGroup</span></span>

## <span data-ttu-id="4e681-144">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="4e681-144">NOTES</span></span>

## <span data-ttu-id="4e681-145">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="4e681-145">RELATED LINKS</span></span>
