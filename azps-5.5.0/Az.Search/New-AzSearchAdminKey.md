---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/new-azsearchadminkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/New-AzSearchAdminKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/New-AzSearchAdminKey.md
ms.openlocfilehash: 28eabb6ccc583a1f3f141c9f02239eca84b04e81
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100159937"
---
# <span data-ttu-id="20634-101">New-AzSearchAdminKey</span><span class="sxs-lookup"><span data-stu-id="20634-101">New-AzSearchAdminKey</span></span>

## <span data-ttu-id="20634-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="20634-102">SYNOPSIS</span></span>
<span data-ttu-id="20634-103">Generiert einen Administratorschlüssel des Azure Cognitive Search-Diensts erneut.</span><span class="sxs-lookup"><span data-stu-id="20634-103">Regenerates an admin key of the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="20634-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="20634-104">SYNTAX</span></span>

### <span data-ttu-id="20634-105">ResourceNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="20634-105">ResourceNameParameterSet (Default)</span></span>
```
New-AzSearchAdminKey [-ResourceGroupName] <String> [-ServiceName] <String> -KeyKind <PSSearchAdminKeyKind>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="20634-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="20634-106">ParentObjectParameterSet</span></span>
```
New-AzSearchAdminKey [-ParentObject] <PSSearchService> -KeyKind <PSSearchAdminKeyKind> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="20634-107">ParentResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="20634-107">ParentResourceIdParameterSet</span></span>
```
New-AzSearchAdminKey [-ParentResourceId] <String> -KeyKind <PSSearchAdminKeyKind> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="20634-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="20634-108">DESCRIPTION</span></span>
<span data-ttu-id="20634-109">Das **Cmdlet "New-AzSearchAdminKey"** generiert einen Administratorschlüssel des Azure Cognitive Search-Diensts erneut.</span><span class="sxs-lookup"><span data-stu-id="20634-109">The **New-AzSearchAdminKey** cmdlet regenerates an admin key of the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="20634-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="20634-110">EXAMPLES</span></span>

### <span data-ttu-id="20634-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="20634-111">Example 1</span></span>
```powershell
PS C:\> New-AzSearchAdminKey -ResourceGroupName "TestAzureSearchPsGroup" -ServiceName "pstestazuresearch01" -KeyKind Primary

Confirm
Are you sure you want to regenerate 'Primary' key for Search Service 'pstestazuresearch01'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y

Primary                          Secondary
-------                          ---------
85B3813D11904B591BE8A196C2C743A1 CEF791D5BAC2E6C0B232C56702F21E87
```

<span data-ttu-id="20634-112">Im Beispiel wird der Primärschlüssel des Azure Cognitive Search-Diensts erneut generiert.</span><span class="sxs-lookup"><span data-stu-id="20634-112">The example regenerates Primary key of the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="20634-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="20634-113">PARAMETERS</span></span>

### <span data-ttu-id="20634-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20634-114">-DefaultProfile</span></span>
<span data-ttu-id="20634-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="20634-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="20634-116">-Force</span><span class="sxs-lookup"><span data-stu-id="20634-116">-Force</span></span>
<span data-ttu-id="20634-117">Fordern Sie keine Bestätigung an.</span><span class="sxs-lookup"><span data-stu-id="20634-117">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="20634-118">-KeyKind</span><span class="sxs-lookup"><span data-stu-id="20634-118">-KeyKind</span></span>
<span data-ttu-id="20634-119">Azure Cognitive Search Service Admin Key Kind (Primär/Sekundär).</span><span class="sxs-lookup"><span data-stu-id="20634-119">Azure Cognitive Search Service admin key kind (Primary/Secondary).</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Search.Models.PSSearchAdminKeyKind
Parameter Sets: (All)
Aliases:
Accepted values: Primary, Secondary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20634-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="20634-120">-ParentObject</span></span>
<span data-ttu-id="20634-121">Azure Cognitive Search Service Input Object.</span><span class="sxs-lookup"><span data-stu-id="20634-121">Azure Cognitive Search Service Input Object.</span></span>

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

### <span data-ttu-id="20634-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="20634-122">-ParentResourceId</span></span>
<span data-ttu-id="20634-123">Azure Cognitive Search Service Resource Id.</span><span class="sxs-lookup"><span data-stu-id="20634-123">Azure Cognitive Search Service Resource Id.</span></span>

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

### <span data-ttu-id="20634-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="20634-124">-ResourceGroupName</span></span>
<span data-ttu-id="20634-125">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="20634-125">Resource Group name.</span></span>

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

### <span data-ttu-id="20634-126">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="20634-126">-ServiceName</span></span>
<span data-ttu-id="20634-127">Name des Azure Cognitive Search Service.</span><span class="sxs-lookup"><span data-stu-id="20634-127">Azure Cognitive Search Service name.</span></span>

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

### <span data-ttu-id="20634-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="20634-128">-Confirm</span></span>
<span data-ttu-id="20634-129">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="20634-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="20634-130">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="20634-130">-WhatIf</span></span>
<span data-ttu-id="20634-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="20634-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="20634-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="20634-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="20634-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20634-133">CommonParameters</span></span>
<span data-ttu-id="20634-134">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20634-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20634-135">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="20634-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20634-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="20634-136">INPUTS</span></span>

### <span data-ttu-id="20634-137">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span><span class="sxs-lookup"><span data-stu-id="20634-137">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="20634-138">System.String</span><span class="sxs-lookup"><span data-stu-id="20634-138">System.String</span></span>

## <span data-ttu-id="20634-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="20634-139">OUTPUTS</span></span>

### <span data-ttu-id="20634-140">Microsoft.Azure.Commands.Management.Search.Models.PSSearchAdminKey</span><span class="sxs-lookup"><span data-stu-id="20634-140">Microsoft.Azure.Commands.Management.Search.Models.PSSearchAdminKey</span></span>

## <span data-ttu-id="20634-141">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="20634-141">NOTES</span></span>

## <span data-ttu-id="20634-142">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="20634-142">RELATED LINKS</span></span>

[<span data-ttu-id="20634-143">Get-AzSearchAdminKeyPair</span><span class="sxs-lookup"><span data-stu-id="20634-143">Get-AzSearchAdminKeyPair</span></span>](./Get-AzSearchAdminKeyPair.md)
