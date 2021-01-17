---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzDiskAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzDiskAccess.md
ms.openlocfilehash: 4b67364f0d079c7cd5fbbdd89b1a84b4dc6fee0e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98473045"
---
# <span data-ttu-id="b1762-101">Remove-AzDiskAccess</span><span class="sxs-lookup"><span data-stu-id="b1762-101">Remove-AzDiskAccess</span></span>

## <span data-ttu-id="b1762-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b1762-102">SYNOPSIS</span></span>
<span data-ttu-id="b1762-103">Entfernt eine Datenträgerzugriffsressource.</span><span class="sxs-lookup"><span data-stu-id="b1762-103">Removes a disk access resource.</span></span>

## <span data-ttu-id="b1762-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b1762-104">SYNTAX</span></span>

### <span data-ttu-id="b1762-105">DefaultParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="b1762-105">DefaultParameterSet (Default)</span></span>
```
Remove-AzDiskAccess [-ResourceGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b1762-106">ResourceIDParameterSet</span><span class="sxs-lookup"><span data-stu-id="b1762-106">ResourceIDParameterSet</span></span>
```
Remove-AzDiskAccess [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b1762-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b1762-107">InputObjectParameterSet</span></span>
```
Remove-AzDiskAccess [-InputObject] <PSDiskAccess> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b1762-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b1762-108">DESCRIPTION</span></span>
<span data-ttu-id="b1762-109">Das **Cmdlet "Remove-AzDiskAccess"** entfernt eine Ressource für den Datenträgerzugriff.</span><span class="sxs-lookup"><span data-stu-id="b1762-109">The **Remove-AzDiskAccess** cmdlet removes a disk access resource.</span></span>

## <span data-ttu-id="b1762-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b1762-110">EXAMPLES</span></span>

### <span data-ttu-id="b1762-111">Beispiel 1: Entfernen des Datenträgerzugriffs mit dem Standardparametersatz</span><span class="sxs-lookup"><span data-stu-id="b1762-111">Example 1: Remove Disk Access using Default Parameter Set</span></span>
```
PS C:\> Remove-AzDiskAccess -ResourceGroupName "ResourceGroup01" -Name "DiskAccess01"
```

<span data-ttu-id="b1762-112">Mit diesem Befehl wird der Datenträgerzugriff mit dem Namen "DiskAccess01" in der Ressourcengruppe "ResourceGroup01" entfernt.</span><span class="sxs-lookup"><span data-stu-id="b1762-112">This command removes the disk access named "DiskAccess01" in resource group "ResourceGroup01"</span></span>

### <span data-ttu-id="b1762-113">Beispiel 2: Entfernen des Datenträgerzugriffs mithilfe der Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="b1762-113">Example 2: Remove Disk Access using Resource ID</span></span>
```
PS C:\> $myDiskAccess = Get-AzDiskAccess -ResourceGroupName "ResourceGroup01" -Name "DiskAccess01"
PS C:\> Remove-AzDiskAccess -ResourceId $myDiskAccess.id
```

<span data-ttu-id="b1762-114">Mit diesem Befehl wird der Datenträgerzugriff nach Ressourcen-ID entfernt.</span><span class="sxs-lookup"><span data-stu-id="b1762-114">This command removes the disk access by Resource ID</span></span>

### <span data-ttu-id="b1762-115">Beispiel 3: Entfernen des Datenträgerzugriffs mithilfe des Eingabeobjekts</span><span class="sxs-lookup"><span data-stu-id="b1762-115">Example 3: Remove Disk Access using Input Object</span></span>
```
PS C:\> $myDiskAccess = Get-AzDiskAccess -ResourceGroupName "ResourceGroup01" -Name "DiskAccess01"
PS C:\> Remove-AzDiskAccess -InputObject $myDiskAccess
```

<span data-ttu-id="b1762-116">Mit diesem Befehl wird der Datenträgerzugriff von InputObject entfernt.</span><span class="sxs-lookup"><span data-stu-id="b1762-116">This command removes the disk access by InputObject</span></span>

### <span data-ttu-id="b1762-117">Beispiel 4: Entfernen des Datenträgerzugriffs durch Piping des Eingabeobjekts</span><span class="sxs-lookup"><span data-stu-id="b1762-117">Example 4: Remove Disk Access by piping Input Object</span></span>
```
PS C:\> Get-AzDiskAccess -ResourceGroupName "ResourceGroup01" -Name "DiskAccess01" | Remove-AzDiskAccess 
```

<span data-ttu-id="b1762-118">Mit diesem Befehl wird der Datenträgerzugriff entfernt, indem das InputObject-Objekt</span><span class="sxs-lookup"><span data-stu-id="b1762-118">This command removes the disk access by piping the InputObject</span></span>

## <span data-ttu-id="b1762-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b1762-119">PARAMETERS</span></span>

### <span data-ttu-id="b1762-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b1762-120">-AsJob</span></span>
<span data-ttu-id="b1762-121">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="b1762-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b1762-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1762-122">-DefaultProfile</span></span>
<span data-ttu-id="b1762-123">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b1762-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b1762-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b1762-124">-InputObject</span></span>
<span data-ttu-id="b1762-125">PowerShell Disk Access Object</span><span class="sxs-lookup"><span data-stu-id="b1762-125">PowerShell Disk Access Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskAccess
Parameter Sets: InputObjectParameterSet
Aliases: DiskAccess

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b1762-126">-Name</span><span class="sxs-lookup"><span data-stu-id="b1762-126">-Name</span></span>
<span data-ttu-id="b1762-127">Gibt den Namen eines Datenträgerzugriffs an.</span><span class="sxs-lookup"><span data-stu-id="b1762-127">Specifies the name of a disk access.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet
Aliases: DiskAccessName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1762-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1762-128">-ResourceGroupName</span></span>
<span data-ttu-id="b1762-129">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="b1762-129">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1762-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b1762-130">-ResourceId</span></span>
<span data-ttu-id="b1762-131">Ressourcen-ID für den Datenträgerzugriff.</span><span class="sxs-lookup"><span data-stu-id="b1762-131">Resource ID for your disk access.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIDParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1762-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b1762-132">-Confirm</span></span>
<span data-ttu-id="b1762-133">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b1762-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b1762-134">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="b1762-134">-WhatIf</span></span>
<span data-ttu-id="b1762-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b1762-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b1762-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b1762-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b1762-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1762-137">CommonParameters</span></span>
<span data-ttu-id="b1762-138">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b1762-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1762-139">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b1762-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1762-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b1762-140">INPUTS</span></span>

### <span data-ttu-id="b1762-141">System.String</span><span class="sxs-lookup"><span data-stu-id="b1762-141">System.String</span></span>

### <span data-ttu-id="b1762-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskAccess</span><span class="sxs-lookup"><span data-stu-id="b1762-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskAccess</span></span>

## <span data-ttu-id="b1762-143">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b1762-143">OUTPUTS</span></span>

### <span data-ttu-id="b1762-144">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="b1762-144">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="b1762-145">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="b1762-145">NOTES</span></span>

## <span data-ttu-id="b1762-146">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="b1762-146">RELATED LINKS</span></span>
