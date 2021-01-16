---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/en-us/powershell/module/az.maintenance/new-azapplyupdate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/New-AzApplyUpdate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/New-AzApplyUpdate.md
ms.openlocfilehash: 05403ce85b80238aeee8749322bdd94d28be68da
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98298336"
---
# <span data-ttu-id="e69d4-101">New-AzApplyUpdate</span><span class="sxs-lookup"><span data-stu-id="e69d4-101">New-AzApplyUpdate</span></span>

## <span data-ttu-id="e69d4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e69d4-102">SYNOPSIS</span></span>
<span data-ttu-id="e69d4-103">Anwenden von Wartungsupdates auf eine Ressource</span><span class="sxs-lookup"><span data-stu-id="e69d4-103">Apply maintenance updates to resource</span></span>

## <span data-ttu-id="e69d4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e69d4-104">SYNTAX</span></span>

```
New-AzApplyUpdate [-ResourceGroupName] <String> [-ProviderName] <String> [-ResourceParentType <String>]
 [-ResourceParentName <String>] [-ResourceType] <String> [-ResourceName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e69d4-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e69d4-105">DESCRIPTION</span></span>
<span data-ttu-id="e69d4-106">Anwenden von Wartungsupdates auf eine Ressource</span><span class="sxs-lookup"><span data-stu-id="e69d4-106">Apply maintenance updates to resource</span></span>

## <span data-ttu-id="e69d4-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e69d4-107">EXAMPLES</span></span>

### <span data-ttu-id="e69d4-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e69d4-108">Example 1</span></span>
```powershell
PS C:\> New-AzApplyUpdate -ResourceGroupName smdtest$region -ResourceParentType hostGroups -ResourceParentName smddhg$region -ResourceType hosts -ResourceName smddh$region -ProviderName Microsoft.Compute


Status         : InProgress
ResourceId     : /subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/smdtestwestus2/providers/Microsoft.Compute/hostGroups/smddhgwestus2/hosts/smddhwestus2
LastUpdateTime : 11/8/2019 9:39:01 AM
Id             :
/subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/smdtestwestus2/providers/Microsoft.Compute/hostGroups/smddhgwestus2/hosts/smddhwestus2/providers/Microsoft.Maintenance/applyUpdates/cbd4c97d-2011-4fa3-9df1-525f97e74eac
Name           : cbd4c97d-2011-4fa3-9df1-525f97e74eac
Type           : Microsoft.Maintenance/applyUpdates
```

<span data-ttu-id="e69d4-109">Anwenden von Wartungsupdates auf eine Ressource</span><span class="sxs-lookup"><span data-stu-id="e69d4-109">Apply maintenance updates to resource</span></span>

## <span data-ttu-id="e69d4-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e69d4-110">PARAMETERS</span></span>

### <span data-ttu-id="e69d4-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e69d4-111">-AsJob</span></span>
<span data-ttu-id="e69d4-112">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="e69d4-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e69d4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e69d4-113">-DefaultProfile</span></span>
<span data-ttu-id="e69d4-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e69d4-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e69d4-115">-ProviderName</span><span class="sxs-lookup"><span data-stu-id="e69d4-115">-ProviderName</span></span>
<span data-ttu-id="e69d4-116">Der Name des Ressourcenanbieters.</span><span class="sxs-lookup"><span data-stu-id="e69d4-116">The resource provider Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e69d4-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e69d4-117">-ResourceGroupName</span></span>
<span data-ttu-id="e69d4-118">Der Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="e69d4-118">The resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e69d4-119">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="e69d4-119">-ResourceName</span></span>
<span data-ttu-id="e69d4-120">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="e69d4-120">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e69d4-121">-ResourceParentName</span><span class="sxs-lookup"><span data-stu-id="e69d4-121">-ResourceParentName</span></span>
<span data-ttu-id="e69d4-122">Der Name der übergeordneten Ressource.</span><span class="sxs-lookup"><span data-stu-id="e69d4-122">The parent resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e69d4-123">-ResourceParentType</span><span class="sxs-lookup"><span data-stu-id="e69d4-123">-ResourceParentType</span></span>
<span data-ttu-id="e69d4-124">Der übergeordnete Ressourcentyp.</span><span class="sxs-lookup"><span data-stu-id="e69d4-124">The parent resource type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e69d4-125">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="e69d4-125">-ResourceType</span></span>
<span data-ttu-id="e69d4-126">Der Ressourcentyp.</span><span class="sxs-lookup"><span data-stu-id="e69d4-126">The resource type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e69d4-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e69d4-127">-Confirm</span></span>
<span data-ttu-id="e69d4-128">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e69d4-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e69d4-129">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="e69d4-129">-WhatIf</span></span>
<span data-ttu-id="e69d4-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e69d4-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e69d4-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e69d4-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e69d4-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e69d4-132">CommonParameters</span></span>
<span data-ttu-id="e69d4-133">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e69d4-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e69d4-134">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e69d4-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e69d4-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e69d4-135">INPUTS</span></span>

### <span data-ttu-id="e69d4-136">System.String</span><span class="sxs-lookup"><span data-stu-id="e69d4-136">System.String</span></span>

## <span data-ttu-id="e69d4-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e69d4-137">OUTPUTS</span></span>

### <span data-ttu-id="e69d4-138">Microsoft.Azure.Commands.Maintenance.Models.PSApplyUpdate</span><span class="sxs-lookup"><span data-stu-id="e69d4-138">Microsoft.Azure.Commands.Maintenance.Models.PSApplyUpdate</span></span>

## <span data-ttu-id="e69d4-139">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="e69d4-139">NOTES</span></span>

## <span data-ttu-id="e69d4-140">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="e69d4-140">RELATED LINKS</span></span>
