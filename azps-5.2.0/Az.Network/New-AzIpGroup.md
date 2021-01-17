---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azipgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpGroup.md
ms.openlocfilehash: 6ae61090f98cbb9929cc5ad1b2745fbf88f21a2a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98370291"
---
# <span data-ttu-id="ca732-101">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="ca732-101">New-AzIpGroup</span></span>

## <span data-ttu-id="ca732-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ca732-102">SYNOPSIS</span></span>
<span data-ttu-id="ca732-103">Erstellt eine Azure IpGroup.</span><span class="sxs-lookup"><span data-stu-id="ca732-103">Creates an Azure IpGroup.</span></span>

## <span data-ttu-id="ca732-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ca732-104">SYNTAX</span></span>

```
New-AzIpGroup -Name <String> -ResourceGroupName <String> [-IpAddress <String[]>] -Location <String>
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ca732-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ca732-105">DESCRIPTION</span></span>
<span data-ttu-id="ca732-106">Das **Cmdlet "New-AzIpGroup"** erstellt eine Azure IpGroup</span><span class="sxs-lookup"><span data-stu-id="ca732-106">The **New-AzIpGroup** cmdlet creates an Azure IpGroup</span></span>

## <span data-ttu-id="ca732-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ca732-107">EXAMPLES</span></span>

### <span data-ttu-id="ca732-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ca732-108">Example 1</span></span>
```powershell
New-AzIpGroup -Name ipGroup -ResourceGroupName ipGroupRG -Location 'West US'
```

### <span data-ttu-id="ca732-109">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="ca732-109">Example 2</span></span>
```powershell
New-AzIpGroup -Name ipGroup -ResourceGroupName ipGroupRG -Location 'West US' -IpAddress 10.0.0.0/24,11.9.0.0/24
```

## <span data-ttu-id="ca732-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ca732-110">PARAMETERS</span></span>

### <span data-ttu-id="ca732-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ca732-111">-AsJob</span></span>
<span data-ttu-id="ca732-112">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="ca732-112">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca732-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca732-113">-DefaultProfile</span></span>
<span data-ttu-id="ca732-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ca732-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca732-115">-Force</span><span class="sxs-lookup"><span data-stu-id="ca732-115">-Force</span></span>
<span data-ttu-id="ca732-116">Bestätigen Sie sie nicht, wenn Sie eine Ressource überschreiben möchten.</span><span class="sxs-lookup"><span data-stu-id="ca732-116">Do not ask for confirmation if you want to overwrite a resource</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca732-117">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="ca732-117">-IpAddress</span></span>
<span data-ttu-id="ca732-118">In der IpGroup definierte IpAddresses</span><span class="sxs-lookup"><span data-stu-id="ca732-118">IpAddresses defined in the IpGroup</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca732-119">-Location</span><span class="sxs-lookup"><span data-stu-id="ca732-119">-Location</span></span>
<span data-ttu-id="ca732-120">Der Speicherort.</span><span class="sxs-lookup"><span data-stu-id="ca732-120">The location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca732-121">-Name</span><span class="sxs-lookup"><span data-stu-id="ca732-121">-Name</span></span>
<span data-ttu-id="ca732-122">Der Name der ipgroup.</span><span class="sxs-lookup"><span data-stu-id="ca732-122">The name of the ipgroup.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca732-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca732-123">-ResourceGroupName</span></span>
<span data-ttu-id="ca732-124">Der Ressourcengruppenname der IP-Gruppe.</span><span class="sxs-lookup"><span data-stu-id="ca732-124">The resource group name of the ipgroup.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca732-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="ca732-125">-Tag</span></span>
<span data-ttu-id="ca732-126">Eine Hashtable, die Ressourcentags darstellt.</span><span class="sxs-lookup"><span data-stu-id="ca732-126">A hashtable which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca732-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ca732-127">-Confirm</span></span>
<span data-ttu-id="ca732-128">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ca732-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca732-129">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="ca732-129">-WhatIf</span></span>
<span data-ttu-id="ca732-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ca732-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ca732-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ca732-131">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca732-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca732-132">CommonParameters</span></span>
<span data-ttu-id="ca732-133">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ca732-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca732-134">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ca732-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca732-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ca732-135">INPUTS</span></span>

### <span data-ttu-id="ca732-136">System.String</span><span class="sxs-lookup"><span data-stu-id="ca732-136">System.String</span></span>

### <span data-ttu-id="ca732-137">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="ca732-137">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="ca732-138">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="ca732-138">System.Collections.Hashtable</span></span>

## <span data-ttu-id="ca732-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ca732-139">OUTPUTS</span></span>

### <span data-ttu-id="ca732-140">Microsoft.Azure.Commands.Network.Models.PSIpGroup</span><span class="sxs-lookup"><span data-stu-id="ca732-140">Microsoft.Azure.Commands.Network.Models.PSIpGroup</span></span>

## <span data-ttu-id="ca732-141">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="ca732-141">NOTES</span></span>

## <span data-ttu-id="ca732-142">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="ca732-142">RELATED LINKS</span></span>
