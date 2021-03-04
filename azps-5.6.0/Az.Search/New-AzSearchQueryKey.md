---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/powershell/module/az.search/new-azsearchquerykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/New-AzSearchQueryKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/New-AzSearchQueryKey.md
ms.openlocfilehash: 3c6335264c0d658b0c068efba30c39b4caca407b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101928491"
---
# <span data-ttu-id="7a987-101">New-AzSearchQueryKey</span><span class="sxs-lookup"><span data-stu-id="7a987-101">New-AzSearchQueryKey</span></span>

## <span data-ttu-id="7a987-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7a987-102">SYNOPSIS</span></span>
<span data-ttu-id="7a987-103">Erstellen Sie einen neuen Abfrageschlüssel für den Azure Cognitive Search-Dienst.</span><span class="sxs-lookup"><span data-stu-id="7a987-103">Create a new query key for the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="7a987-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7a987-104">SYNTAX</span></span>

### <span data-ttu-id="7a987-105">ResourceNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="7a987-105">ResourceNameParameterSet (Default)</span></span>
```
New-AzSearchQueryKey [-ResourceGroupName] <String> [-ServiceName] <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7a987-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7a987-106">ParentObjectParameterSet</span></span>
```
New-AzSearchQueryKey [-ParentObject] <PSSearchService> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7a987-107">ParentResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7a987-107">ParentResourceIdParameterSet</span></span>
```
New-AzSearchQueryKey [-ParentResourceId] <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7a987-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7a987-108">DESCRIPTION</span></span>
<span data-ttu-id="7a987-109">Das **Cmdlet New-AzSearchQueryKey** erstellt einen neuen Abfrageschlüssel für den Azure Cognitive Search-Dienst.</span><span class="sxs-lookup"><span data-stu-id="7a987-109">The **New-AzSearchQueryKey** cmdlet creates a new query key for the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="7a987-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="7a987-110">EXAMPLES</span></span>

### <span data-ttu-id="7a987-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="7a987-111">Example 1</span></span>
```powershell
PS C:\> New-AzSearchQueryKey -ResourceGroupName "TestAzureSearchPsGroup" -ServiceName "pstestazuresearch01" -Name "NewQueryKey1" -Force

Name         Key                             
----         ---                             
NewQueryKey1 65FBCF561228C5F0E01F8F2114C80459
```

<span data-ttu-id="7a987-112">Im Beispiel wird ein neuer Abfrageschlüssel für den Azure Cognitive Search-Dienst erstellt.</span><span class="sxs-lookup"><span data-stu-id="7a987-112">The example creates a new query key for the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="7a987-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="7a987-113">PARAMETERS</span></span>

### <span data-ttu-id="7a987-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a987-114">-DefaultProfile</span></span>
<span data-ttu-id="7a987-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7a987-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7a987-116">-Name</span><span class="sxs-lookup"><span data-stu-id="7a987-116">-Name</span></span>
<span data-ttu-id="7a987-117">Name des Azure Cognitive Search Service-Abfrageschlüssels.</span><span class="sxs-lookup"><span data-stu-id="7a987-117">Azure Cognitive Search Service query key name.</span></span>

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

### <span data-ttu-id="7a987-118">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="7a987-118">-ParentObject</span></span>
<span data-ttu-id="7a987-119">Azure Cognitive Search Service Input Object.</span><span class="sxs-lookup"><span data-stu-id="7a987-119">Azure Cognitive Search Service Input Object.</span></span>

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

### <span data-ttu-id="7a987-120">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="7a987-120">-ParentResourceId</span></span>
<span data-ttu-id="7a987-121">Azure Cognitive Search Service Resource Id.</span><span class="sxs-lookup"><span data-stu-id="7a987-121">Azure Cognitive Search Service Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ParentResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a987-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a987-122">-ResourceGroupName</span></span>
<span data-ttu-id="7a987-123">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="7a987-123">Resource Group name.</span></span>

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

### <span data-ttu-id="7a987-124">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="7a987-124">-ServiceName</span></span>
<span data-ttu-id="7a987-125">Name des Azure Cognitive Search Service.</span><span class="sxs-lookup"><span data-stu-id="7a987-125">Azure Cognitive Search Service name.</span></span>

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

### <span data-ttu-id="7a987-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="7a987-126">-Confirm</span></span>
<span data-ttu-id="7a987-127">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7a987-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7a987-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7a987-128">-WhatIf</span></span>
<span data-ttu-id="7a987-129">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7a987-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7a987-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7a987-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7a987-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a987-131">CommonParameters</span></span>
<span data-ttu-id="7a987-132">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a987-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a987-133">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7a987-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a987-134">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="7a987-134">INPUTS</span></span>

### <span data-ttu-id="7a987-135">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span><span class="sxs-lookup"><span data-stu-id="7a987-135">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="7a987-136">System.String</span><span class="sxs-lookup"><span data-stu-id="7a987-136">System.String</span></span>

## <span data-ttu-id="7a987-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="7a987-137">OUTPUTS</span></span>

### <span data-ttu-id="7a987-138">Microsoft.Azure.Commands.Management.Search.Models.PSSearchQueryKey</span><span class="sxs-lookup"><span data-stu-id="7a987-138">Microsoft.Azure.Commands.Management.Search.Models.PSSearchQueryKey</span></span>

## <span data-ttu-id="7a987-139">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="7a987-139">NOTES</span></span>

## <span data-ttu-id="7a987-140">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="7a987-140">RELATED LINKS</span></span>

[<span data-ttu-id="7a987-141">Get-AzSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="7a987-141">Get-AzSearchQueryKey.md</span></span>](./Get-AzSearchQueryKey.md)

[<span data-ttu-id="7a987-142">Remove-AzSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="7a987-142">Remove-AzSearchQueryKey.md</span></span>](./Remove-AzSearchQueryKey.md)
