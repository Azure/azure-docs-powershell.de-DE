---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/remove-azpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeering.md
ms.openlocfilehash: 414a732dd80850a31a87f88d3dfdbf091cb4a6a6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100169489"
---
# <span data-ttu-id="51219-101">Remove-AzPeering</span><span class="sxs-lookup"><span data-stu-id="51219-101">Remove-AzPeering</span></span>

## <span data-ttu-id="51219-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="51219-102">SYNOPSIS</span></span>
<span data-ttu-id="51219-103">Löschen oder Entfernen eines Peerings</span><span class="sxs-lookup"><span data-stu-id="51219-103">Delete or remove a peering.</span></span> <span data-ttu-id="51219-104">Dadurch werden alle untergeordneten Ressourcen gelöscht oder eine Warnung für die Ressource angezeigt.</span><span class="sxs-lookup"><span data-stu-id="51219-104">This will delete all child resources or alerting on the resource.</span></span>

## <span data-ttu-id="51219-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="51219-105">SYNTAX</span></span>

### <span data-ttu-id="51219-106">ByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="51219-106">ByName (Default)</span></span>
```
Remove-AzPeering [-ResourceGroupName] <String> [-Name] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="51219-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="51219-107">InputObject</span></span>
```
Remove-AzPeering [-InputObject] <PSPeering> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="51219-108">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="51219-108">ByResourceId</span></span>
```
Remove-AzPeering -ResourceId <String> [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="51219-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="51219-109">DESCRIPTION</span></span>
<span data-ttu-id="51219-110">Löschen Sie eine Peeringressource nach und nach.</span><span class="sxs-lookup"><span data-stu-id="51219-110">Perminently delete a peering resource.</span></span>

## <span data-ttu-id="51219-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="51219-111">EXAMPLES</span></span>

### <span data-ttu-id="51219-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="51219-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzPeering -ResourceId $resourceId
```

<span data-ttu-id="51219-113">Entfernen Sie ein Peering nach Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="51219-113">Remove a peering by resource id.</span></span>

## <span data-ttu-id="51219-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="51219-114">PARAMETERS</span></span>

### <span data-ttu-id="51219-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="51219-115">-AsJob</span></span>
<span data-ttu-id="51219-116">Führen Sie die Ausführung im Hintergrund aus.</span><span class="sxs-lookup"><span data-stu-id="51219-116">Run in the background.</span></span>

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

### <span data-ttu-id="51219-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51219-117">-DefaultProfile</span></span>
<span data-ttu-id="51219-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="51219-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="51219-119">-Force</span><span class="sxs-lookup"><span data-stu-id="51219-119">-Force</span></span>
<span data-ttu-id="51219-120">Erzwingen des Vorgangs</span><span class="sxs-lookup"><span data-stu-id="51219-120">Force the operation to complete</span></span>

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

### <span data-ttu-id="51219-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="51219-121">-InputObject</span></span>
<span data-ttu-id="51219-122">Verwenden sie Get-AzPeering, um dieses Objekt abzurufen.</span><span class="sxs-lookup"><span data-stu-id="51219-122">Use Get-AzPeering to retrieve this object.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="51219-123">-Name</span><span class="sxs-lookup"><span data-stu-id="51219-123">-Name</span></span>
<span data-ttu-id="51219-124">Der eindeutige Name von PSPeering.</span><span class="sxs-lookup"><span data-stu-id="51219-124">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51219-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="51219-125">-PassThru</span></span>
<span data-ttu-id="51219-126">"True" zurückgeben, wenn dies abgeschlossen ist</span><span class="sxs-lookup"><span data-stu-id="51219-126">Return true if complete</span></span>

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

### <span data-ttu-id="51219-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="51219-127">-ResourceGroupName</span></span>
<span data-ttu-id="51219-128">Der Name einer vorhandenen Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="51219-128">The create or use an existing resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51219-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="51219-129">-ResourceId</span></span>
<span data-ttu-id="51219-130">Der Zeichenfolgenname der Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="51219-130">The resource id string name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51219-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="51219-131">-Confirm</span></span>
<span data-ttu-id="51219-132">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="51219-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="51219-133">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="51219-133">-WhatIf</span></span>
<span data-ttu-id="51219-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="51219-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="51219-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="51219-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="51219-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51219-136">CommonParameters</span></span>
<span data-ttu-id="51219-137">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="51219-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51219-138">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="51219-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51219-139">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="51219-139">INPUTS</span></span>

### <span data-ttu-id="51219-140">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span><span class="sxs-lookup"><span data-stu-id="51219-140">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

### <span data-ttu-id="51219-141">System.String</span><span class="sxs-lookup"><span data-stu-id="51219-141">System.String</span></span>

## <span data-ttu-id="51219-142">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="51219-142">OUTPUTS</span></span>

### <span data-ttu-id="51219-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="51219-143">System.Boolean</span></span>

## <span data-ttu-id="51219-144">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="51219-144">NOTES</span></span>

## <span data-ttu-id="51219-145">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="51219-145">RELATED LINKS</span></span>
