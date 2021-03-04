---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/powershell/module/az.search/new-azsearchsharedprivatelinkresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/New-AzSearchSharedPrivateLinkResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/New-AzSearchSharedPrivateLinkResource.md
ms.openlocfilehash: 683a6105273bcd2ff2f254352cf6e991491c035d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101930816"
---
# <span data-ttu-id="2943e-101">New-AzSearchSharedPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="2943e-101">New-AzSearchSharedPrivateLinkResource</span></span>

## <span data-ttu-id="2943e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2943e-102">SYNOPSIS</span></span>
<span data-ttu-id="2943e-103">Erstellt eine freigegebene private Linkressource für den Azure Cognitive Search-Dienst.</span><span class="sxs-lookup"><span data-stu-id="2943e-103">Creates a shared private link resource for the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="2943e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2943e-104">SYNTAX</span></span>

```
New-AzSearchSharedPrivateLinkResource [-ResourceGroupName] <String> [-ServiceName] <String> [-Name] <String>
 [-PrivateLinkResourceId] <String> [-GroupId] <String> [-RequestMessage] <String> [[-ResourceRegion] <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2943e-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2943e-105">DESCRIPTION</span></span>
<span data-ttu-id="2943e-106">Die **New-AzSearchSharedPrivateLinkResource** erstellt eine freigegebene private Linkressource für den Azure Cognitive Search-Dienst.</span><span class="sxs-lookup"><span data-stu-id="2943e-106">The **New-AzSearchSharedPrivateLinkResource** creates a shared private link resource for the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="2943e-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="2943e-107">EXAMPLES</span></span>

### <span data-ttu-id="2943e-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="2943e-108">Example 1</span></span>
```powershell
PS C:\> New-AzSearchSharedPrivateLinkResource -ResourceGroupName arjagann -ServiceName arjagann-test-cuseuap -Name blob-pe -PrivateLinkResourceId /subscriptions/a4337210-c6b0-4de4-907a-688f1c120d9a/resourcegroups/PETesting/providers/Microsoft.Storage/storageAccounts/petesting -GroupId blob -RequestMessage "Please approve" 

Id                    : /subscriptions/a4337210-c6b0-4de4-907a-688f1c120d9a/resourceGroups/arjagann/providers/Microsoft.Search/searchServices/arjagann-test-cuseuap/sharedPrivateLinkResources/blob-pe
Type                  : Microsoft.Search/searchServices/sharedPrivateLinkResources
Status                : Pending
Name                  : blob-pe
GroupId               : blob
PrivateLinkResourceId : /subscriptions/a4337210-c6b0-4de4-907a-688f1c120d9a/resourcegroups/PETesting/providers/Microsoft.Storage/storageAccounts/petesting
ProvisioningState     : Succeeded
RequestMessage        : Please approve
ResourceRegion        :
```

<span data-ttu-id="2943e-109">In diesem Beispiel wird eine freigegebene private Linkressource mit dem Blobdienst eines Speicherkontos für den Azure Cognitive Search-Dienst erstellt.</span><span class="sxs-lookup"><span data-stu-id="2943e-109">This example creates a shared private link resource to the blob service of a storage account for the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="2943e-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="2943e-110">PARAMETERS</span></span>

### <span data-ttu-id="2943e-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2943e-111">-AsJob</span></span>
<span data-ttu-id="2943e-112">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="2943e-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2943e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2943e-113">-DefaultProfile</span></span>
<span data-ttu-id="2943e-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2943e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2943e-115">-GroupId</span><span class="sxs-lookup"><span data-stu-id="2943e-115">-GroupId</span></span>
<span data-ttu-id="2943e-116">Ressourcengruppen-ID für freigegebene private Verknüpfungen</span><span class="sxs-lookup"><span data-stu-id="2943e-116">Shared private link resource group id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2943e-117">-Name</span><span class="sxs-lookup"><span data-stu-id="2943e-117">-Name</span></span>
<span data-ttu-id="2943e-118">Azure Cognitive Search Shared private link resource</span><span class="sxs-lookup"><span data-stu-id="2943e-118">Azure Cognitive Search Shared private link resource</span></span>

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

### <span data-ttu-id="2943e-119">-PrivateLinkResourceId</span><span class="sxs-lookup"><span data-stu-id="2943e-119">-PrivateLinkResourceId</span></span>
<span data-ttu-id="2943e-120">Zielressourcen-ID für freigegebene private Links</span><span class="sxs-lookup"><span data-stu-id="2943e-120">Shared private link target resource id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2943e-121">-RequestMessage</span><span class="sxs-lookup"><span data-stu-id="2943e-121">-RequestMessage</span></span>
<span data-ttu-id="2943e-122">Nachricht zur Ressourcenanforderung für freigegebene private Verknüpfungen</span><span class="sxs-lookup"><span data-stu-id="2943e-122">Shared private link resource request message</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2943e-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2943e-123">-ResourceGroupName</span></span>
<span data-ttu-id="2943e-124">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="2943e-124">Resource Group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2943e-125">-ResourceRegion</span><span class="sxs-lookup"><span data-stu-id="2943e-125">-ResourceRegion</span></span>
<span data-ttu-id="2943e-126">(Optional) Ressourcenregion für freigegebene private Verknüpfungen</span><span class="sxs-lookup"><span data-stu-id="2943e-126">(Optional) Shared private link resource region</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2943e-127">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="2943e-127">-ServiceName</span></span>
<span data-ttu-id="2943e-128">Name des Azure Cognitive Search Service.</span><span class="sxs-lookup"><span data-stu-id="2943e-128">Azure Cognitive Search Service name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2943e-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="2943e-129">-Confirm</span></span>
<span data-ttu-id="2943e-130">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2943e-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2943e-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2943e-131">-WhatIf</span></span>
<span data-ttu-id="2943e-132">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2943e-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2943e-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2943e-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2943e-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2943e-134">CommonParameters</span></span>
<span data-ttu-id="2943e-135">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2943e-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2943e-136">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2943e-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2943e-137">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="2943e-137">INPUTS</span></span>

### <span data-ttu-id="2943e-138">Keine</span><span class="sxs-lookup"><span data-stu-id="2943e-138">None</span></span>

## <span data-ttu-id="2943e-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="2943e-139">OUTPUTS</span></span>

### <span data-ttu-id="2943e-140">Microsoft.Azure.Commands.Management.Search.Models.PSSharedPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="2943e-140">Microsoft.Azure.Commands.Management.Search.Models.PSSharedPrivateLinkResource</span></span>

## <span data-ttu-id="2943e-141">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="2943e-141">NOTES</span></span>

## <span data-ttu-id="2943e-142">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="2943e-142">RELATED LINKS</span></span>

[<span data-ttu-id="2943e-143">Get-AzSearchSharedPrivateLinkResource.md</span><span class="sxs-lookup"><span data-stu-id="2943e-143">Get-AzSearchSharedPrivateLinkResource.md</span></span>](./Get-AzSearchSharedPrivateLinkResource.md)

[<span data-ttu-id="2943e-144">Remove-AzSearchSharedPrivateLinkResource.md</span><span class="sxs-lookup"><span data-stu-id="2943e-144">Remove-AzSearchSharedPrivateLinkResource.md</span></span>](./Remove-AzSearchSharedPrivateLinkResource.md)

[<span data-ttu-id="2943e-145">Set-AzSearchSharedPrivateLinkResource.md</span><span class="sxs-lookup"><span data-stu-id="2943e-145">Set-AzSearchSharedPrivateLinkResource.md</span></span>](./Set-AzSearchSharedPrivateLinkResource.md)
