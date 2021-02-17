---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/get-azsearchsharedprivatelinkresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchSharedPrivateLinkResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchSharedPrivateLinkResource.md
ms.openlocfilehash: 1a49d73ea564cab6f01b9482a7c110aeaa7fc307
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100159940"
---
# <span data-ttu-id="69a31-101">Get-AzSearchSharedPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="69a31-101">Get-AzSearchSharedPrivateLinkResource</span></span>

## <span data-ttu-id="69a31-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="69a31-102">SYNOPSIS</span></span>
<span data-ttu-id="69a31-103">Ruft freigegebene private Linkressourcen des Azure Cognitive Search-Diensts ab.</span><span class="sxs-lookup"><span data-stu-id="69a31-103">Gets shared private link resources(s) of the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="69a31-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="69a31-104">SYNTAX</span></span>

### <span data-ttu-id="69a31-105">ResourceNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="69a31-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzSearchSharedPrivateLinkResource [-ResourceGroupName] <String> [-ServiceName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="69a31-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="69a31-106">ParentObjectParameterSet</span></span>
```
Get-AzSearchSharedPrivateLinkResource [-ParentObject] <PSSearchService> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="69a31-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="69a31-107">ResourceIdParameterSet</span></span>
```
Get-AzSearchSharedPrivateLinkResource [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="69a31-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="69a31-108">DESCRIPTION</span></span>
<span data-ttu-id="69a31-109">Das **Cmdlet "Get-AzSearchSharedPrivateLinkResource"** ruft ressourcen für freigegebene private Links des Azure Cognitive Search-Diensts ab.</span><span class="sxs-lookup"><span data-stu-id="69a31-109">The **Get-AzSearchSharedPrivateLinkResource** cmdlet gets shared private link resources(s) of the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="69a31-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="69a31-110">EXAMPLES</span></span>

### <span data-ttu-id="69a31-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="69a31-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSearchSharedPrivateLinkResource -ResourceGroupName arjagann -ServiceName arjagann-test-cuseuap

Id                    : /subscriptions/a4337210-c6b0-4de4-907a-688f1c120d9a/resourceGroups/arjagann/providers/Microsoft.Search/searchServices/arjagann-test-cuseuap/sharedPrivateLinkResources/table-pe
Type                  : Microsoft.Search/searchServices/sharedPrivateLinkResources
Status                : Pending
Name                  : table-pe
GroupId               : table
PrivateLinkResourceId : /subscriptions/a4337210-c6b0-4de4-907a-688f1c120d9a/resourcegroups/PETesting/providers/Microsoft.Storage/storageAccounts/petesting
ProvisioningState     : Succeeded
RequestMessage        : please approve
ResourceRegion        :

Id                    : /subscriptions/a4337210-c6b0-4de4-907a-688f1c120d9a/resourceGroups/arjagann/providers/Microsoft.Search/searchServices/arjagann-test-cuseuap/sharedPrivateLinkResources/cosmos-pe
Type                  : Microsoft.Search/searchServices/sharedPrivateLinkResources
Status                : Pending
Name                  : cosmos-pe
GroupId               : Sql
PrivateLinkResourceId : /subscriptions/dc95d1b6-71a8-4dff-bcc9-a1c282bdbd8b/resourceGroups/arjagann/providers/Microsoft.DocumentDb/databaseAccounts/arjagann-sql
ProvisioningState     : Succeeded
RequestMessage        : please approve
ResourceRegion        :

Id                    : /subscriptions/a4337210-c6b0-4de4-907a-688f1c120d9a/resourceGroups/arjagann/providers/Microsoft.Search/searchServices/arjagann-test-cuseuap/sharedPrivateLinkResources/blob-pe2
Type                  : Microsoft.Search/searchServices/sharedPrivateLinkResources
Status                : Pending
Name                  : blob-pe2
GroupId               : blob
PrivateLinkResourceId : /subscriptions/a4337210-c6b0-4de4-907a-688f1c120d9a/resourcegroups/PETesting/providers/Microsoft.Storage/storageAccounts/petesting2
ProvisioningState     : Succeeded
RequestMessage        : please approve
ResourceRegion        :
```

<span data-ttu-id="69a31-112">In diesem Beispiel werden alle ressourcen für freigegebene private Links des Azure Cognitive Search-Diensts aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="69a31-112">This example lists all the shared private link resources of the Azure Cognitive Search service.</span></span>

### <span data-ttu-id="69a31-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="69a31-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSearchSharedPrivateLinkResource -ResourceGroupName arjagann -ServiceName arjagann-test-cuseuap -Name table-pe

Id                    : /subscriptions/a4337210-c6b0-4de4-907a-688f1c120d9a/resourceGroups/arjagann/providers/Microsoft.Search/searchServices/arjagann-test-cuseuap/sharedPrivateLinkResources/table-pe
Type                  : Microsoft.Search/searchServices/sharedPrivateLinkResources
Status                : Pending
Name                  : table-pe
GroupId               : table
PrivateLinkResourceId : /subscriptions/a4337210-c6b0-4de4-907a-688f1c120d9a/resourcegroups/PETesting/providers/Microsoft.Storage/storageAccounts/petesting
ProvisioningState     : Succeeded
RequestMessage        : please approve
ResourceRegion        :
```

<span data-ttu-id="69a31-114">In diesem Beispiel wird eine bestimmte Ressource für freigegebene private Links nach dem Namen des Azure Cognitive Search-Diensts aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="69a31-114">This example lists a specific shared private link resource by name of the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="69a31-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="69a31-115">PARAMETERS</span></span>

### <span data-ttu-id="69a31-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69a31-116">-DefaultProfile</span></span>
<span data-ttu-id="69a31-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="69a31-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="69a31-118">-Name</span><span class="sxs-lookup"><span data-stu-id="69a31-118">-Name</span></span>
<span data-ttu-id="69a31-119">Azure Cognitive Search Shared Private Link resource</span><span class="sxs-lookup"><span data-stu-id="69a31-119">Azure Cognitive Search Shared private link resource</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet, ParentObjectParameterSet
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69a31-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="69a31-120">-ParentObject</span></span>
<span data-ttu-id="69a31-121">Azure Cognitive Search Service Input Object.</span><span class="sxs-lookup"><span data-stu-id="69a31-121">Azure Cognitive Search Service Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Search.Models.PSSearchService
Parameter Sets: ParentObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="69a31-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69a31-122">-ResourceGroupName</span></span>
<span data-ttu-id="69a31-123">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="69a31-123">Resource Group name.</span></span>

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

### <span data-ttu-id="69a31-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="69a31-124">-ResourceId</span></span>
<span data-ttu-id="69a31-125">Ressourcen-ID für freigegebenen privaten Link</span><span class="sxs-lookup"><span data-stu-id="69a31-125">Shared private link resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69a31-126">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="69a31-126">-ServiceName</span></span>
<span data-ttu-id="69a31-127">Name des Azure Cognitive Search Service.</span><span class="sxs-lookup"><span data-stu-id="69a31-127">Azure Cognitive Search Service name.</span></span>

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

### <span data-ttu-id="69a31-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="69a31-128">-Confirm</span></span>
<span data-ttu-id="69a31-129">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="69a31-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="69a31-130">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="69a31-130">-WhatIf</span></span>
<span data-ttu-id="69a31-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="69a31-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="69a31-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="69a31-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="69a31-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69a31-133">CommonParameters</span></span>
<span data-ttu-id="69a31-134">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69a31-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69a31-135">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="69a31-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69a31-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="69a31-136">INPUTS</span></span>

### <span data-ttu-id="69a31-137">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span><span class="sxs-lookup"><span data-stu-id="69a31-137">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="69a31-138">System.String</span><span class="sxs-lookup"><span data-stu-id="69a31-138">System.String</span></span>

## <span data-ttu-id="69a31-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="69a31-139">OUTPUTS</span></span>

### <span data-ttu-id="69a31-140">Microsoft.Azure.Commands.Management.Search.Models.PSSharedPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="69a31-140">Microsoft.Azure.Commands.Management.Search.Models.PSSharedPrivateLinkResource</span></span>

## <span data-ttu-id="69a31-141">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="69a31-141">NOTES</span></span>

## <span data-ttu-id="69a31-142">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="69a31-142">RELATED LINKS</span></span>

[<span data-ttu-id="69a31-143">New-AzSearchSharedPrivateLinkResource.md</span><span class="sxs-lookup"><span data-stu-id="69a31-143">New-AzSearchSharedPrivateLinkResource.md</span></span>](./New-AzSearchSharedPrivateLinkResource.md)

[<span data-ttu-id="69a31-144">Remove-AzSearchSharedPrivateLinkResource.md</span><span class="sxs-lookup"><span data-stu-id="69a31-144">Remove-AzSearchSharedPrivateLinkResource.md</span></span>](./Remove-AzSearchSharedPrivateLinkResource.md)

[<span data-ttu-id="69a31-145">Set-AzSearchSharedPrivateLinkResource.md</span><span class="sxs-lookup"><span data-stu-id="69a31-145">Set-AzSearchSharedPrivateLinkResource.md</span></span>](./Set-AzSearchSharedPrivateLinkResource.md)
