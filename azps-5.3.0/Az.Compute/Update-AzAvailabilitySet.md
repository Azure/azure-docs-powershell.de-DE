---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azavailabilityset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzAvailabilitySet.md
ms.openlocfilehash: 689336bb7fbb7ef59be96a5bd6bcbfe49ddb64c0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98472935"
---
# <span data-ttu-id="c6274-101">Update-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="c6274-101">Update-AzAvailabilitySet</span></span>

## <span data-ttu-id="c6274-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c6274-102">SYNOPSIS</span></span>
<span data-ttu-id="c6274-103">Aktualisiert einen Verfügbarkeitssatz.</span><span class="sxs-lookup"><span data-stu-id="c6274-103">Updates an availability set.</span></span>

## <span data-ttu-id="c6274-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c6274-104">SYNTAX</span></span>

```
Update-AzAvailabilitySet [-AvailabilitySet] <PSAvailabilitySet> [[-Sku] <String>]
 [-ProximityPlacementGroupId <String>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c6274-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c6274-105">DESCRIPTION</span></span>
<span data-ttu-id="c6274-106">Das **Cmdlet "Update-AzAvailabilitySet"** aktualisiert einen Verfügbarkeitssatz.</span><span class="sxs-lookup"><span data-stu-id="c6274-106">The **Update-AzAvailabilitySet** cmdlet updates an availability set.</span></span>

## <span data-ttu-id="c6274-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c6274-107">EXAMPLES</span></span>

### <span data-ttu-id="c6274-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c6274-108">Example 1</span></span>
```
PS C:\> Get-AzAvailabilitySet -ResourceGroupName 'ResourceGroup01' -Name 'AvSet01' | Update-AzAvailabilitySet -Managed;
```

<span data-ttu-id="c6274-109">Mit diesem Befehl wird der Verfügbarkeitssatz "AvSet01" in der Ressourcengruppe mit dem Namen "ResourceGroup01" auf einen verwalteten Verfügbarkeitssatz aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="c6274-109">This command updates the availability set named 'AvSet01' in the resource group named 'ResourceGroup01' to a managed availability set.</span></span>

## <span data-ttu-id="c6274-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c6274-110">PARAMETERS</span></span>

### <span data-ttu-id="c6274-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c6274-111">-AsJob</span></span>
<span data-ttu-id="c6274-112">Führen Sie das Cmdlet im Hintergrund aus, und geben Sie einen Auftrag zurück, um den Fortschritt nachverfolgt zu können.</span><span class="sxs-lookup"><span data-stu-id="c6274-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="c6274-113">-AvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="c6274-113">-AvailabilitySet</span></span>
<span data-ttu-id="c6274-114">Gibt das Zu aktualisierende Verfügbarkeitssatzobjekt an.</span><span class="sxs-lookup"><span data-stu-id="c6274-114">Specifies the availability set object to be updated.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c6274-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6274-115">-DefaultProfile</span></span>
<span data-ttu-id="c6274-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c6274-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c6274-117">-ProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="c6274-117">-ProximityPlacementGroupId</span></span>
<span data-ttu-id="c6274-118">Die Ressourcen-ID der Näherungsplatzierungsgruppe, die mit diesem Verfügbarkeitssatz verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="c6274-118">The resource id of the Proximity Placement Group to use with this availability set.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6274-119">-SKU</span><span class="sxs-lookup"><span data-stu-id="c6274-119">-Sku</span></span>
<span data-ttu-id="c6274-120">Der Name der SKU</span><span class="sxs-lookup"><span data-stu-id="c6274-120">The Name of Sku</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6274-121">-Tag</span><span class="sxs-lookup"><span data-stu-id="c6274-121">-Tag</span></span>
<span data-ttu-id="c6274-122">Schlüssel-Wert-Paare in Form einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="c6274-122">Key-value pairs in the form of a hash table.</span></span>

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

### <span data-ttu-id="c6274-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c6274-123">-Confirm</span></span>
<span data-ttu-id="c6274-124">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c6274-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c6274-125">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="c6274-125">-WhatIf</span></span>
<span data-ttu-id="c6274-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c6274-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c6274-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c6274-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c6274-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6274-128">CommonParameters</span></span>
<span data-ttu-id="c6274-129">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c6274-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6274-130">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c6274-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6274-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c6274-131">INPUTS</span></span>

### <span data-ttu-id="c6274-132">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="c6274-132">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="c6274-133">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c6274-133">OUTPUTS</span></span>

### <span data-ttu-id="c6274-134">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="c6274-134">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="c6274-135">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="c6274-135">NOTES</span></span>

## <span data-ttu-id="c6274-136">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="c6274-136">RELATED LINKS</span></span>
