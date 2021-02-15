---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/set-azsearchsharedprivatelinkresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Set-AzSearchSharedPrivateLinkResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Set-AzSearchSharedPrivateLinkResource.md
ms.openlocfilehash: 5fd69c2ec5542ebcf8737f24cfbe068d775f1c04
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100145900"
---
# <span data-ttu-id="0de63-101">Set-AzSearchSharedPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="0de63-101">Set-AzSearchSharedPrivateLinkResource</span></span>

## <span data-ttu-id="0de63-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0de63-102">SYNOPSIS</span></span>
<span data-ttu-id="0de63-103">Aktualisieren Sie die Ressource für freigegebene private Links für den Azure Cognitive Search-Dienst.</span><span class="sxs-lookup"><span data-stu-id="0de63-103">Update the shared private link resource for the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="0de63-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0de63-104">SYNTAX</span></span>

### <span data-ttu-id="0de63-105">ResourceNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="0de63-105">ResourceNameParameterSet (Default)</span></span>
```
Set-AzSearchSharedPrivateLinkResource [-ResourceGroupName] <String> [-ServiceName] <String> [-Name] <String>
 -RequestMessage <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0de63-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0de63-106">ParentObjectParameterSet</span></span>
```
Set-AzSearchSharedPrivateLinkResource -ParentObject <PSSearchService> [-Name] <String> -RequestMessage <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0de63-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0de63-107">ResourceIdParameterSet</span></span>
```
Set-AzSearchSharedPrivateLinkResource [-ResourceId] <String> -RequestMessage <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0de63-108">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0de63-108">InputObjectParameterSet</span></span>
```
Set-AzSearchSharedPrivateLinkResource -RequestMessage <String> -InputObject <PSSharedPrivateLinkResource>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0de63-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0de63-109">DESCRIPTION</span></span>
<span data-ttu-id="0de63-110">Diese **Set-AzSearchSharedPrivateLinkResource** aktualisiert die Ressource für freigegebene private Links für den Azure Cognitive Search-Dienst.</span><span class="sxs-lookup"><span data-stu-id="0de63-110">This **Set-AzSearchSharedPrivateLinkResource** updates the shared private link resource for the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="0de63-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="0de63-111">EXAMPLES</span></span>

### <span data-ttu-id="0de63-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="0de63-112">Example 1</span></span>
```powershell
PS C:\> Set-AzSearchSharedPrivateLinkResource -ResourceGroupName arjagann -ServiceName arjagann-test-cuseuap -Name blob-pe -RequestMessage "Please kindly approve"


Id                    : /subscriptions/a4337210-c6b0-4de4-907a-688f1c120d9a/resourceGroups/arjagann/providers/Microsoft.Search/searchServices/arjagann-test-cuseuap/sharedPrivateLinkResources/blob-pe
Type                  : Microsoft.Search/searchServices/sharedPrivateLinkResources
Status                : Pending
Name                  : blob-pe
GroupId               : blob
PrivateLinkResourceId : /subscriptions/a4337210-c6b0-4de4-907a-688f1c120d9a/resourcegroups/PETesting/providers/Microsoft.Storage/storageAccounts/petesting
ProvisioningState     : Succeeded
RequestMessage        : Please kindly approve
ResourceRegion        :
```

<span data-ttu-id="0de63-113">In diesem Beispiel wird die Anforderungsmeldung für die ausstehende Ressource für freigegebene private Links für den Azure Cognitive Search-Dienst aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="0de63-113">This example updates the request message for the pending shared private link resource for the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="0de63-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0de63-114">PARAMETERS</span></span>

### <span data-ttu-id="0de63-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0de63-115">-AsJob</span></span>
<span data-ttu-id="0de63-116">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="0de63-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0de63-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0de63-117">-DefaultProfile</span></span>
<span data-ttu-id="0de63-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0de63-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0de63-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0de63-119">-InputObject</span></span>
<span data-ttu-id="0de63-120">Ressourceneingabeobjekt für freigegebene private Links</span><span class="sxs-lookup"><span data-stu-id="0de63-120">Shared private link resource input object</span></span>

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

### <span data-ttu-id="0de63-121">-Name</span><span class="sxs-lookup"><span data-stu-id="0de63-121">-Name</span></span>
<span data-ttu-id="0de63-122">Azure Cognitive Search Shared Private Link resource</span><span class="sxs-lookup"><span data-stu-id="0de63-122">Azure Cognitive Search Shared private link resource</span></span>

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

### <span data-ttu-id="0de63-123">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="0de63-123">-ParentObject</span></span>
<span data-ttu-id="0de63-124">Azure Cognitive Search Service Input Object.</span><span class="sxs-lookup"><span data-stu-id="0de63-124">Azure Cognitive Search Service Input Object.</span></span>

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

### <span data-ttu-id="0de63-125">-RequestMessage</span><span class="sxs-lookup"><span data-stu-id="0de63-125">-RequestMessage</span></span>
<span data-ttu-id="0de63-126">Anforderungsmeldung für einen freigegebenen privaten Link</span><span class="sxs-lookup"><span data-stu-id="0de63-126">Shared private link resource request message</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0de63-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0de63-127">-ResourceGroupName</span></span>
<span data-ttu-id="0de63-128">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="0de63-128">Resource Group name.</span></span>

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

### <span data-ttu-id="0de63-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0de63-129">-ResourceId</span></span>
<span data-ttu-id="0de63-130">Ressourcen-ID für freigegebenen privaten Link</span><span class="sxs-lookup"><span data-stu-id="0de63-130">Shared private link resource id</span></span>

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

### <span data-ttu-id="0de63-131">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="0de63-131">-ServiceName</span></span>
<span data-ttu-id="0de63-132">Name des Azure Cognitive Search Service.</span><span class="sxs-lookup"><span data-stu-id="0de63-132">Azure Cognitive Search Service name.</span></span>

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

### <span data-ttu-id="0de63-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0de63-133">-Confirm</span></span>
<span data-ttu-id="0de63-134">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0de63-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0de63-135">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="0de63-135">-WhatIf</span></span>
<span data-ttu-id="0de63-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0de63-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0de63-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0de63-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0de63-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0de63-138">CommonParameters</span></span>
<span data-ttu-id="0de63-139">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0de63-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0de63-140">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0de63-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0de63-141">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="0de63-141">INPUTS</span></span>

### <span data-ttu-id="0de63-142">Keine</span><span class="sxs-lookup"><span data-stu-id="0de63-142">None</span></span>

## <span data-ttu-id="0de63-143">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="0de63-143">OUTPUTS</span></span>

### <span data-ttu-id="0de63-144">Microsoft.Azure.Commands.Management.Search.Models.PSSharedPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="0de63-144">Microsoft.Azure.Commands.Management.Search.Models.PSSharedPrivateLinkResource</span></span>

## <span data-ttu-id="0de63-145">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="0de63-145">NOTES</span></span>

## <span data-ttu-id="0de63-146">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="0de63-146">RELATED LINKS</span></span>

[<span data-ttu-id="0de63-147">New-AzSearchSharedPrivateLinkResource.md</span><span class="sxs-lookup"><span data-stu-id="0de63-147">New-AzSearchSharedPrivateLinkResource.md</span></span>](./New-AzSearchSharedPrivateLinkResource.md)

[<span data-ttu-id="0de63-148">Get-AzSearchSharedPrivateLinkResource.md</span><span class="sxs-lookup"><span data-stu-id="0de63-148">Get-AzSearchSharedPrivateLinkResource.md</span></span>](./Get-AzSearchSharedPrivateLinkResource.md)

[<span data-ttu-id="0de63-149">Remove-AzSearchSharedPrivateLinkResource.md</span><span class="sxs-lookup"><span data-stu-id="0de63-149">Remove-AzSearchSharedPrivateLinkResource.md</span></span>](./Remove-AzSearchSharedPrivateLinkResource.md)