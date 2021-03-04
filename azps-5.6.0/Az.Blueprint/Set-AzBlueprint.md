---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/powershell/module/az.blueprint/set-azblueprint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Set-AzBlueprint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Set-AzBlueprint.md
ms.openlocfilehash: 5511be0e20c99a6a120e2f7591287b9ee17b0943
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101925163"
---
# <span data-ttu-id="cf8d8-101">Set-AzBlueprint</span><span class="sxs-lookup"><span data-stu-id="cf8d8-101">Set-AzBlueprint</span></span>

## <span data-ttu-id="cf8d8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cf8d8-102">SYNOPSIS</span></span>
<span data-ttu-id="cf8d8-103">Aktualisieren sie eine Blaupausendefinition.</span><span class="sxs-lookup"><span data-stu-id="cf8d8-103">Update a blueprint definition.</span></span>

## <span data-ttu-id="cf8d8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cf8d8-104">SYNTAX</span></span>

### <span data-ttu-id="cf8d8-105">UpdateBlueprintBySubscription (Standard)</span><span class="sxs-lookup"><span data-stu-id="cf8d8-105">UpdateBlueprintBySubscription (Default)</span></span>
```
Set-AzBlueprint -Name <String> [-SubscriptionId <String>] -BlueprintFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cf8d8-106">UpdateBlueprintByManagementGroup</span><span class="sxs-lookup"><span data-stu-id="cf8d8-106">UpdateBlueprintByManagementGroup</span></span>
```
Set-AzBlueprint -Name <String> -ManagementGroupId <String> -BlueprintFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cf8d8-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="cf8d8-107">DESCRIPTION</span></span>
<span data-ttu-id="cf8d8-108">Aktualisieren Sie eine Blaupausendefinition, und speichern Sie sie in der angegebenen Abonnement- oder Verwaltungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="cf8d8-108">Update a blueprint definition and save it within the specified subscription or management group.</span></span>

## <span data-ttu-id="cf8d8-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="cf8d8-109">EXAMPLES</span></span>

### <span data-ttu-id="cf8d8-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="cf8d8-110">Example 1</span></span>
```powershell
PS C:\> Set-AzBlueprint -Name MyBlueprint -SubscriptionId 00000000-1111-0000-1111-000000000000 -BlueprintFile C:\Blueprint.json

Name              : SimpleBlueprint
Id                : /providers/Microsoft.Management/managementGroups/{mgId}/providers/Microsoft.Blueprint/blueprints/SimpleBlueprint
ManagementGroupId : myManagementGroupId
Versions          : 
Description       : test
TimeCreated       : 2019-05-12
TargetScope       : Subscription
Parameters        : {enforcetaganditsvalue_tagName, enforcetaganditsvalue_tagValue}
ResourceGroups    : {AppNetworkRG}
```

<span data-ttu-id="cf8d8-111">Aktualisieren Sie eine Blaupausendefinition mit neuen Parametern.</span><span class="sxs-lookup"><span data-stu-id="cf8d8-111">Update a blueprint definition with new parameters.</span></span>

## <span data-ttu-id="cf8d8-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="cf8d8-112">PARAMETERS</span></span>

### <span data-ttu-id="cf8d8-113">-BlueprintFile</span><span class="sxs-lookup"><span data-stu-id="cf8d8-113">-BlueprintFile</span></span>
<span data-ttu-id="cf8d8-114">Pfad zu einer Blueprint-JSON-Datei auf dem Datenträger.</span><span class="sxs-lookup"><span data-stu-id="cf8d8-114">Path to a Blueprint JSON file on disk.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf8d8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf8d8-115">-DefaultProfile</span></span>
<span data-ttu-id="cf8d8-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="cf8d8-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cf8d8-117">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="cf8d8-117">-ManagementGroupId</span></span>
<span data-ttu-id="cf8d8-118">Verwaltungsgruppen-ID, in der die Blaupausendefinition gespeichert wird oder gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="cf8d8-118">Management Group Id where the blueprint definition is or will be saved.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateBlueprintByManagementGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf8d8-119">-Name</span><span class="sxs-lookup"><span data-stu-id="cf8d8-119">-Name</span></span>
<span data-ttu-id="cf8d8-120">Name der Blaupausedefinition.</span><span class="sxs-lookup"><span data-stu-id="cf8d8-120">Blueprint definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf8d8-121">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="cf8d8-121">-SubscriptionId</span></span>
<span data-ttu-id="cf8d8-122">Abonnement-ID, bei der die Blaupausendefinition gespeichert wird oder gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="cf8d8-122">Subscription Id where the blueprint definition is or will be saved.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateBlueprintBySubscription
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf8d8-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="cf8d8-123">-Confirm</span></span>
<span data-ttu-id="cf8d8-124">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="cf8d8-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cf8d8-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cf8d8-125">-WhatIf</span></span>
<span data-ttu-id="cf8d8-126">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="cf8d8-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cf8d8-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="cf8d8-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cf8d8-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf8d8-128">CommonParameters</span></span>
<span data-ttu-id="cf8d8-129">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cf8d8-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf8d8-130">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cf8d8-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf8d8-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="cf8d8-131">INPUTS</span></span>

### <span data-ttu-id="cf8d8-132">System.String</span><span class="sxs-lookup"><span data-stu-id="cf8d8-132">System.String</span></span>

## <span data-ttu-id="cf8d8-133">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="cf8d8-133">OUTPUTS</span></span>

### <span data-ttu-id="cf8d8-134">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprint</span><span class="sxs-lookup"><span data-stu-id="cf8d8-134">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprint</span></span>

## <span data-ttu-id="cf8d8-135">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="cf8d8-135">NOTES</span></span>

## <span data-ttu-id="cf8d8-136">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="cf8d8-136">RELATED LINKS</span></span>
