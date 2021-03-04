---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/powershell/module/az.search/set-azsearchsharedprivatelinkresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Set-AzSearchSharedPrivateLinkResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Set-AzSearchSharedPrivateLinkResource.md
ms.openlocfilehash: 7139831accd920858e7b97f775146d01b91cef3f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101928883"
---
# <span data-ttu-id="28598-101">Set-AzSearchSharedPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="28598-101">Set-AzSearchSharedPrivateLinkResource</span></span>

## <span data-ttu-id="28598-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="28598-102">SYNOPSIS</span></span>
<span data-ttu-id="28598-103">Aktualisieren Sie die freigegebene private Linkressource für den Azure Cognitive Search-Dienst.</span><span class="sxs-lookup"><span data-stu-id="28598-103">Update the shared private link resource for the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="28598-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="28598-104">SYNTAX</span></span>

### <span data-ttu-id="28598-105">ResourceNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="28598-105">ResourceNameParameterSet (Default)</span></span>
```
Set-AzSearchSharedPrivateLinkResource [-ResourceGroupName] <String> [-ServiceName] <String> [-Name] <String>
 -RequestMessage <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="28598-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="28598-106">ParentObjectParameterSet</span></span>
```
Set-AzSearchSharedPrivateLinkResource -ParentObject <PSSearchService> [-Name] <String> -RequestMessage <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="28598-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="28598-107">ResourceIdParameterSet</span></span>
```
Set-AzSearchSharedPrivateLinkResource [-ResourceId] <String> -RequestMessage <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="28598-108">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="28598-108">InputObjectParameterSet</span></span>
```
Set-AzSearchSharedPrivateLinkResource -RequestMessage <String> -InputObject <PSSharedPrivateLinkResource>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="28598-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="28598-109">DESCRIPTION</span></span>
<span data-ttu-id="28598-110">Diese **Set-AzSearchSharedPrivateLinkResource** aktualisiert die freigegebene private Linkressource für den Azure Cognitive Search-Dienst.</span><span class="sxs-lookup"><span data-stu-id="28598-110">This **Set-AzSearchSharedPrivateLinkResource** updates the shared private link resource for the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="28598-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="28598-111">EXAMPLES</span></span>

### <span data-ttu-id="28598-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="28598-112">Example 1</span></span>
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

<span data-ttu-id="28598-113">In diesem Beispiel wird die Anforderungsmeldung für die ausstehende Ressource für den freigegebenen privaten Link für den Azure Cognitive Search-Dienst aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="28598-113">This example updates the request message for the pending shared private link resource for the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="28598-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="28598-114">PARAMETERS</span></span>

### <span data-ttu-id="28598-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="28598-115">-AsJob</span></span>
<span data-ttu-id="28598-116">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="28598-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="28598-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28598-117">-DefaultProfile</span></span>
<span data-ttu-id="28598-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="28598-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="28598-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="28598-119">-InputObject</span></span>
<span data-ttu-id="28598-120">Ressourceneingabeobjekt für freigegebene private Verknüpfungen</span><span class="sxs-lookup"><span data-stu-id="28598-120">Shared private link resource input object</span></span>

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

### <span data-ttu-id="28598-121">-Name</span><span class="sxs-lookup"><span data-stu-id="28598-121">-Name</span></span>
<span data-ttu-id="28598-122">Azure Cognitive Search Shared private link resource</span><span class="sxs-lookup"><span data-stu-id="28598-122">Azure Cognitive Search Shared private link resource</span></span>

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

### <span data-ttu-id="28598-123">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="28598-123">-ParentObject</span></span>
<span data-ttu-id="28598-124">Azure Cognitive Search Service Input Object.</span><span class="sxs-lookup"><span data-stu-id="28598-124">Azure Cognitive Search Service Input Object.</span></span>

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

### <span data-ttu-id="28598-125">-RequestMessage</span><span class="sxs-lookup"><span data-stu-id="28598-125">-RequestMessage</span></span>
<span data-ttu-id="28598-126">Nachricht zur Ressourcenanforderung für freigegebene private Verknüpfungen</span><span class="sxs-lookup"><span data-stu-id="28598-126">Shared private link resource request message</span></span>

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

### <span data-ttu-id="28598-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="28598-127">-ResourceGroupName</span></span>
<span data-ttu-id="28598-128">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="28598-128">Resource Group name.</span></span>

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

### <span data-ttu-id="28598-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="28598-129">-ResourceId</span></span>
<span data-ttu-id="28598-130">Ressourcen-ID für freigegebene private Links</span><span class="sxs-lookup"><span data-stu-id="28598-130">Shared private link resource id</span></span>

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

### <span data-ttu-id="28598-131">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="28598-131">-ServiceName</span></span>
<span data-ttu-id="28598-132">Name des Azure Cognitive Search Service.</span><span class="sxs-lookup"><span data-stu-id="28598-132">Azure Cognitive Search Service name.</span></span>

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

### <span data-ttu-id="28598-133">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="28598-133">-Confirm</span></span>
<span data-ttu-id="28598-134">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="28598-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="28598-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="28598-135">-WhatIf</span></span>
<span data-ttu-id="28598-136">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="28598-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="28598-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="28598-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="28598-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28598-138">CommonParameters</span></span>
<span data-ttu-id="28598-139">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="28598-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28598-140">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="28598-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28598-141">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="28598-141">INPUTS</span></span>

### <span data-ttu-id="28598-142">Keine</span><span class="sxs-lookup"><span data-stu-id="28598-142">None</span></span>

## <span data-ttu-id="28598-143">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="28598-143">OUTPUTS</span></span>

### <span data-ttu-id="28598-144">Microsoft.Azure.Commands.Management.Search.Models.PSSharedPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="28598-144">Microsoft.Azure.Commands.Management.Search.Models.PSSharedPrivateLinkResource</span></span>

## <span data-ttu-id="28598-145">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="28598-145">NOTES</span></span>

## <span data-ttu-id="28598-146">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="28598-146">RELATED LINKS</span></span>

[<span data-ttu-id="28598-147">New-AzSearchSharedPrivateLinkResource.md</span><span class="sxs-lookup"><span data-stu-id="28598-147">New-AzSearchSharedPrivateLinkResource.md</span></span>](./New-AzSearchSharedPrivateLinkResource.md)

[<span data-ttu-id="28598-148">Get-AzSearchSharedPrivateLinkResource.md</span><span class="sxs-lookup"><span data-stu-id="28598-148">Get-AzSearchSharedPrivateLinkResource.md</span></span>](./Get-AzSearchSharedPrivateLinkResource.md)

[<span data-ttu-id="28598-149">Remove-AzSearchSharedPrivateLinkResource.md</span><span class="sxs-lookup"><span data-stu-id="28598-149">Remove-AzSearchSharedPrivateLinkResource.md</span></span>](./Remove-AzSearchSharedPrivateLinkResource.md)