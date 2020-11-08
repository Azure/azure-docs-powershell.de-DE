---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azhostgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzHostGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzHostGroup.md
ms.openlocfilehash: 2fdb5317504bb1bc08ed45e8224a30a61cca8e8c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94177273"
---
# <span data-ttu-id="9cc5e-101">New-AzHostGroup</span><span class="sxs-lookup"><span data-stu-id="9cc5e-101">New-AzHostGroup</span></span>

## <span data-ttu-id="9cc5e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9cc5e-102">SYNOPSIS</span></span>
<span data-ttu-id="9cc5e-103">Erstellt eine Hostgruppe.</span><span class="sxs-lookup"><span data-stu-id="9cc5e-103">Creates a host group.</span></span>

## <span data-ttu-id="9cc5e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9cc5e-104">SYNTAX</span></span>

```
New-AzHostGroup [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 -PlatformFaultDomain <Int32> [-Zone <String[]>] [-SupportAutomaticPlacement <bool>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9cc5e-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9cc5e-105">DESCRIPTION</span></span>
<span data-ttu-id="9cc5e-106">Mit diesem Cmdlet wird eine Host Gruppe erstellt.</span><span class="sxs-lookup"><span data-stu-id="9cc5e-106">This cmdlet will create a Host group.</span></span>

## <span data-ttu-id="9cc5e-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9cc5e-107">EXAMPLES</span></span>

### <span data-ttu-id="9cc5e-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="9cc5e-108">Example 1</span></span>
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

<span data-ttu-id="9cc5e-109">Dieser Befehl erstellt eine Hostgruppe in der angegebenen Position und Zone.</span><span class="sxs-lookup"><span data-stu-id="9cc5e-109">This command creates a host group in the given location and zone.</span></span>

## <span data-ttu-id="9cc5e-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="9cc5e-110">PARAMETERS</span></span>

### <span data-ttu-id="9cc5e-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9cc5e-111">-AsJob</span></span>
<span data-ttu-id="9cc5e-112">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="9cc5e-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9cc5e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9cc5e-113">-DefaultProfile</span></span>
<span data-ttu-id="9cc5e-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="9cc5e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9cc5e-115">-Standort</span><span class="sxs-lookup"><span data-stu-id="9cc5e-115">-Location</span></span>
<span data-ttu-id="9cc5e-116">Gibt die Position an.</span><span class="sxs-lookup"><span data-stu-id="9cc5e-116">Specifies location.</span></span>

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

### <span data-ttu-id="9cc5e-117">-Name</span><span class="sxs-lookup"><span data-stu-id="9cc5e-117">-Name</span></span>
<span data-ttu-id="9cc5e-118">Gibt den Namen der Hostgruppe an.</span><span class="sxs-lookup"><span data-stu-id="9cc5e-118">Specifies the name of the host group.</span></span>

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

### <span data-ttu-id="9cc5e-119">-PlatformFaultDomain</span><span class="sxs-lookup"><span data-stu-id="9cc5e-119">-PlatformFaultDomain</span></span>
<span data-ttu-id="9cc5e-120">Gibt die Anzahl der fehlerdomänen an, die die Hostgruppe überspannen kann.</span><span class="sxs-lookup"><span data-stu-id="9cc5e-120">Specifies the number of fault domains that the host group can span.</span></span>  <span data-ttu-id="9cc5e-121">Der Mindestwert ist 1, und der Höchstwert ist 3.</span><span class="sxs-lookup"><span data-stu-id="9cc5e-121">The minimum value is 1 and the maximum value is 3.</span></span>

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

### <span data-ttu-id="9cc5e-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9cc5e-122">-ResourceGroupName</span></span>
<span data-ttu-id="9cc5e-123">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="9cc5e-123">The name of the resource group.</span></span>

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

### <span data-ttu-id="9cc5e-124">-Tag</span><span class="sxs-lookup"><span data-stu-id="9cc5e-124">-Tag</span></span>
<span data-ttu-id="9cc5e-125">Gibt Tags an</span><span class="sxs-lookup"><span data-stu-id="9cc5e-125">Specifies Tags</span></span>

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

### <span data-ttu-id="9cc5e-126">-Zone</span><span class="sxs-lookup"><span data-stu-id="9cc5e-126">-Zone</span></span>
<span data-ttu-id="9cc5e-127">Gibt Zonen der Hostgruppe an.</span><span class="sxs-lookup"><span data-stu-id="9cc5e-127">Specifies Zones of the host group.</span></span>

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

### <span data-ttu-id="9cc5e-128">-SupportAutomaticPlacement</span><span class="sxs-lookup"><span data-stu-id="9cc5e-128">-SupportAutomaticPlacement</span></span>
<span data-ttu-id="9cc5e-129">Gibt an, ob Hostgroup die automatische Platzierung von VM aktiviert.</span><span class="sxs-lookup"><span data-stu-id="9cc5e-129">Specifies if HostGroup will enable automatic placement of vm's.</span></span>
<span data-ttu-id="9cc5e-130">Automatische Platzierung bedeutet, dass diese VMS auf dedizierten, von Azure ausgewählten Hosts unter der dedizierten Hostgruppe platziert werden.</span><span class="sxs-lookup"><span data-stu-id="9cc5e-130">Automatic placement means these VMs are placed on dedicated hosts, chosen by Azure, under the dedicated host group.</span></span>
<span data-ttu-id="9cc5e-131">Wenn keine Angabe erfolgt, lautet der Standardwert true.</span><span class="sxs-lookup"><span data-stu-id="9cc5e-131">If not specified, default value will be true.</span></span>

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


### <span data-ttu-id="9cc5e-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="9cc5e-132">-Confirm</span></span>
<span data-ttu-id="9cc5e-133">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9cc5e-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9cc5e-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9cc5e-134">-WhatIf</span></span>
<span data-ttu-id="9cc5e-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9cc5e-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9cc5e-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9cc5e-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9cc5e-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9cc5e-137">CommonParameters</span></span>
<span data-ttu-id="9cc5e-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9cc5e-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9cc5e-139">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9cc5e-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9cc5e-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9cc5e-140">INPUTS</span></span>

### <span data-ttu-id="9cc5e-141">System. String</span><span class="sxs-lookup"><span data-stu-id="9cc5e-141">System.String</span></span>

## <span data-ttu-id="9cc5e-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9cc5e-142">OUTPUTS</span></span>

### <span data-ttu-id="9cc5e-143">Microsoft. Azure. Commands. Compute. Automation. Models. PSHostGroup</span><span class="sxs-lookup"><span data-stu-id="9cc5e-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSHostGroup</span></span>

## <span data-ttu-id="9cc5e-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="9cc5e-144">NOTES</span></span>

## <span data-ttu-id="9cc5e-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9cc5e-145">RELATED LINKS</span></span>
