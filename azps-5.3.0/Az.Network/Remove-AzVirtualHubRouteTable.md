---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualhubroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualHubRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualHubRouteTable.md
ms.openlocfilehash: e55cb0629bb6376253f0b8f0b636eb0b43bcb742
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98385257"
---
# <span data-ttu-id="7fc14-101">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="7fc14-101">Remove-AzVirtualHubRouteTable</span></span>

## <span data-ttu-id="7fc14-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7fc14-102">SYNOPSIS</span></span>
<span data-ttu-id="7fc14-103">Löschen Einer virtuellen Hub-Routentabelle-Ressource, die einem virtuellen Hub zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="7fc14-103">Delete a virtual hub route table resource associated with a virtual hub.</span></span>

## <span data-ttu-id="7fc14-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7fc14-104">SYNTAX</span></span>

### <span data-ttu-id="7fc14-105">ByVirtualHubRouteTableName (Standard)</span><span class="sxs-lookup"><span data-stu-id="7fc14-105">ByVirtualHubRouteTableName (Default)</span></span>
```
Remove-AzVirtualHubRouteTable -ResourceGroupName <String> -HubName <String> -Name <String> [-AsJob] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7fc14-106">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="7fc14-106">ByVirtualHubObject</span></span>
```
Remove-AzVirtualHubRouteTable -Name <String> -VirtualHub <PSVirtualHub> [-AsJob] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7fc14-107">ByVirtualHubRouteTableObject</span><span class="sxs-lookup"><span data-stu-id="7fc14-107">ByVirtualHubRouteTableObject</span></span>
```
Remove-AzVirtualHubRouteTable [-InputObject <PSVirtualHubRouteTable>] [-AsJob] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7fc14-108">ByVirtualHubRouteTableResourceId</span><span class="sxs-lookup"><span data-stu-id="7fc14-108">ByVirtualHubRouteTableResourceId</span></span>
```
Remove-AzVirtualHubRouteTable -ResourceId <String> [-AsJob] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7fc14-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7fc14-109">DESCRIPTION</span></span>
<span data-ttu-id="7fc14-110">Löscht die angegebene Routentabelle, die dem angegebenen virtuellen Hub zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="7fc14-110">Deletes the specified route table that is associated with the specified virtual hub.</span></span>

## <span data-ttu-id="7fc14-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="7fc14-111">EXAMPLES</span></span>

### <span data-ttu-id="7fc14-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="7fc14-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzVirtualHubRouteTable�-ResourceGroupName�"testRg"�-HubName�"westushub"�-Name�"routeTable1"
```

<span data-ttu-id="7fc14-113">Mit diesem Befehl wird die routeTable1 des virtuellen Hubs "westushub" gelöscht.</span><span class="sxs-lookup"><span data-stu-id="7fc14-113">This command deletes the routeTable1 of the virtual hub westushub.</span></span>

## <span data-ttu-id="7fc14-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7fc14-114">PARAMETERS</span></span>

### <span data-ttu-id="7fc14-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7fc14-115">-AsJob</span></span>
<span data-ttu-id="7fc14-116">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="7fc14-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7fc14-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7fc14-117">-DefaultProfile</span></span>
<span data-ttu-id="7fc14-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7fc14-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7fc14-119">-Force</span><span class="sxs-lookup"><span data-stu-id="7fc14-119">-Force</span></span>
<span data-ttu-id="7fc14-120">Bestätigen Sie sie nicht, wenn Sie eine Ressource überschreiben möchten.</span><span class="sxs-lookup"><span data-stu-id="7fc14-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="7fc14-121">-HubName</span><span class="sxs-lookup"><span data-stu-id="7fc14-121">-HubName</span></span>
<span data-ttu-id="7fc14-122">Der Name der übergeordneten Ressource.</span><span class="sxs-lookup"><span data-stu-id="7fc14-122">The parent resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubRouteTableName
Aliases: VirtualHubName, ParentVirtualHubName, ParentResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fc14-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7fc14-123">-InputObject</span></span>
<span data-ttu-id="7fc14-124">Die zu entfernende Virtualhubroutetable-Ressource.</span><span class="sxs-lookup"><span data-stu-id="7fc14-124">The virtualhubroutetable resource to remove.</span></span>

```yaml
Type: PSVirtualHubRouteTable
Parameter Sets: ByVirtualHubRouteTableObject
Aliases: VirtualHubRouteTable

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7fc14-125">-Name</span><span class="sxs-lookup"><span data-stu-id="7fc14-125">-Name</span></span>
<span data-ttu-id="7fc14-126">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="7fc14-126">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubRouteTableName, ByVirtualHubObject
Aliases: ResourceName, VirtualHubRouteTableName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fc14-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7fc14-127">-PassThru</span></span>
<span data-ttu-id="7fc14-128">Gibt ein Objekt zurück, das das Element darstellt, für das dieser Vorgang ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7fc14-128">Returns an object representing the item on which this operation is being performed.</span></span>

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

### <span data-ttu-id="7fc14-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7fc14-129">-ResourceGroupName</span></span>
<span data-ttu-id="7fc14-130">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="7fc14-130">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubRouteTableName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fc14-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7fc14-131">-ResourceId</span></span>
<span data-ttu-id="7fc14-132">Die Ressourcen-ID der zu entfernende Virtualhubroutetable-Ressource.</span><span class="sxs-lookup"><span data-stu-id="7fc14-132">The resource id of the virtualhubroutetable resource to remove.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubRouteTableResourceId
Aliases: VirtualHubRouteTableId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7fc14-133">-VirtualHub</span><span class="sxs-lookup"><span data-stu-id="7fc14-133">-VirtualHub</span></span>
<span data-ttu-id="7fc14-134">{{ Fill VirtualHub Description }}</span><span class="sxs-lookup"><span data-stu-id="7fc14-134">{{ Fill VirtualHub Description }}</span></span>

```yaml
Type: PSVirtualHub
Parameter Sets: ByVirtualHubObject
Aliases: ParentVirtualHub, ParentObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7fc14-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7fc14-135">-Confirm</span></span>
<span data-ttu-id="7fc14-136">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7fc14-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7fc14-137">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="7fc14-137">-WhatIf</span></span>
<span data-ttu-id="7fc14-138">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7fc14-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7fc14-139">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7fc14-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7fc14-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7fc14-140">CommonParameters</span></span>
<span data-ttu-id="7fc14-141">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7fc14-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7fc14-142">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7fc14-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7fc14-143">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="7fc14-143">INPUTS</span></span>

### <span data-ttu-id="7fc14-144">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="7fc14-144">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="7fc14-145">Microsoft.Azure.Commands.Network.Models.PSVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="7fc14-145">Microsoft.Azure.Commands.Network.Models.PSVirtualHubRouteTable</span></span>

### <span data-ttu-id="7fc14-146">System.String</span><span class="sxs-lookup"><span data-stu-id="7fc14-146">System.String</span></span>

## <span data-ttu-id="7fc14-147">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="7fc14-147">OUTPUTS</span></span>

### <span data-ttu-id="7fc14-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="7fc14-148">System.Boolean</span></span>

## <span data-ttu-id="7fc14-149">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="7fc14-149">NOTES</span></span>

## <span data-ttu-id="7fc14-150">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="7fc14-150">RELATED LINKS</span></span>
