---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/powershell/module/az.search/remove-azsearchsharedprivatelinkresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Remove-AzSearchSharedPrivateLinkResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Remove-AzSearchSharedPrivateLinkResource.md
ms.openlocfilehash: ed5c5bf502e1d19b0ba095e5db68f1f116a71137
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101920443"
---
# <span data-ttu-id="13367-101">Remove-AzSearchSharedPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="13367-101">Remove-AzSearchSharedPrivateLinkResource</span></span>

## <span data-ttu-id="13367-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="13367-102">SYNOPSIS</span></span>
<span data-ttu-id="13367-103">Entfernen Sie die freigegebene private Linkressource aus dem Azure Cognitive Search-Dienst.</span><span class="sxs-lookup"><span data-stu-id="13367-103">Remove the shared private link resource from the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="13367-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="13367-104">SYNTAX</span></span>

### <span data-ttu-id="13367-105">ResourceNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="13367-105">ResourceNameParameterSet (Default)</span></span>
```
Remove-AzSearchSharedPrivateLinkResource [-ResourceGroupName] <String> [-ServiceName] <String> [-Name] <String>
 [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="13367-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="13367-106">ParentObjectParameterSet</span></span>
```
Remove-AzSearchSharedPrivateLinkResource -ParentObject <PSSearchService> [-Name] <String> [-Force] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="13367-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="13367-107">ResourceIdParameterSet</span></span>
```
Remove-AzSearchSharedPrivateLinkResource [-ResourceId] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="13367-108">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="13367-108">InputObjectParameterSet</span></span>
```
Remove-AzSearchSharedPrivateLinkResource -InputObject <PSSharedPrivateLinkResource> [-Force] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="13367-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="13367-109">DESCRIPTION</span></span>
<span data-ttu-id="13367-110">Das **Cmdlet Remove-AzSearchSharedPrivateLinkResource** entfernt die freigegebene private Linkressource aus dem Azure Cognitive Search-Dienst.</span><span class="sxs-lookup"><span data-stu-id="13367-110">The **Remove-AzSearchSharedPrivateLinkResource** cmdlet removes the shared private link resource from the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="13367-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="13367-111">EXAMPLES</span></span>

### <span data-ttu-id="13367-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="13367-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSearchSharedPrivateLinkResource -ResourceGroupName arjagann -ServiceName arjagann-test-cuseuap -Name blob-pe

Confirm
Remove Shared Private Link Resource 'blob-pe'.
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="13367-113">In diesem Beispiel wird eine freigegebene private Linkressource nach dem Namen des Azure Cognitive Search-Diensts gelöscht.</span><span class="sxs-lookup"><span data-stu-id="13367-113">This example deletes a shared private link resource by name of the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="13367-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="13367-114">PARAMETERS</span></span>

### <span data-ttu-id="13367-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="13367-115">-AsJob</span></span>
<span data-ttu-id="13367-116">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="13367-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="13367-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13367-117">-DefaultProfile</span></span>
<span data-ttu-id="13367-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="13367-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="13367-119">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="13367-119">-Force</span></span>
<span data-ttu-id="13367-120">Bitten Sie nicht um Bestätigung.</span><span class="sxs-lookup"><span data-stu-id="13367-120">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="13367-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="13367-121">-InputObject</span></span>
<span data-ttu-id="13367-122">Ressourceneingabeobjekt für freigegebene private Verknüpfungen</span><span class="sxs-lookup"><span data-stu-id="13367-122">Shared private link resource input object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Search.Models.PSSharedPrivateLinkResource
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="13367-123">-Name</span><span class="sxs-lookup"><span data-stu-id="13367-123">-Name</span></span>
<span data-ttu-id="13367-124">Azure Cognitive Search Shared private link resource</span><span class="sxs-lookup"><span data-stu-id="13367-124">Azure Cognitive Search Shared private link resource</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet, ParentObjectParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13367-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="13367-125">-ParentObject</span></span>
<span data-ttu-id="13367-126">Azure Cognitive Search Service Input Object.</span><span class="sxs-lookup"><span data-stu-id="13367-126">Azure Cognitive Search Service Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Search.Models.PSSearchService
Parameter Sets: ParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="13367-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="13367-127">-PassThru</span></span>
<span data-ttu-id="13367-128">Dieses Cmdlet gibt standardmäßig kein -Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="13367-128">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="13367-129">Wenn dieser Schalter angegeben ist, gibt er "true" zurück, wenn er erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="13367-129">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="13367-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13367-130">-ResourceGroupName</span></span>
<span data-ttu-id="13367-131">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="13367-131">Resource Group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13367-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="13367-132">-ResourceId</span></span>
<span data-ttu-id="13367-133">Ressourcen-ID für freigegebene private Links</span><span class="sxs-lookup"><span data-stu-id="13367-133">Shared private link resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13367-134">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="13367-134">-ServiceName</span></span>
<span data-ttu-id="13367-135">Name des Azure Cognitive Search Service.</span><span class="sxs-lookup"><span data-stu-id="13367-135">Azure Cognitive Search Service name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13367-136">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="13367-136">-Confirm</span></span>
<span data-ttu-id="13367-137">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="13367-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="13367-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="13367-138">-WhatIf</span></span>
<span data-ttu-id="13367-139">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="13367-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="13367-140">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="13367-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="13367-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13367-141">CommonParameters</span></span>
<span data-ttu-id="13367-142">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13367-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13367-143">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="13367-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13367-144">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="13367-144">INPUTS</span></span>

### <span data-ttu-id="13367-145">Keine</span><span class="sxs-lookup"><span data-stu-id="13367-145">None</span></span>

## <span data-ttu-id="13367-146">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="13367-146">OUTPUTS</span></span>

### <span data-ttu-id="13367-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="13367-147">System.Boolean</span></span>

## <span data-ttu-id="13367-148">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="13367-148">NOTES</span></span>

## <span data-ttu-id="13367-149">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="13367-149">RELATED LINKS</span></span>

[<span data-ttu-id="13367-150">New-AzSearchSharedPrivateLinkResource.md</span><span class="sxs-lookup"><span data-stu-id="13367-150">New-AzSearchSharedPrivateLinkResource.md</span></span>](./New-AzSearchSharedPrivateLinkResource.md)

[<span data-ttu-id="13367-151">Get-AzSearchSharedPrivateLinkResource.md</span><span class="sxs-lookup"><span data-stu-id="13367-151">Get-AzSearchSharedPrivateLinkResource.md</span></span>](./Get-AzSearchSharedPrivateLinkResource.md)

[<span data-ttu-id="13367-152">Set-AzSearchSharedPrivateLinkResource.md</span><span class="sxs-lookup"><span data-stu-id="13367-152">Set-AzSearchSharedPrivateLinkResource.md</span></span>](./Set-AzSearchSharedPrivateLinkResource.md)