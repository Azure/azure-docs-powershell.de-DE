---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/import-azblueprintwithartifact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Import-AzBlueprintWithArtifact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Import-AzBlueprintWithArtifact.md
ms.openlocfilehash: 43877ecb7fe7e90f0619a26a54eea534ac1390b3
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98293458"
---
# <span data-ttu-id="833cb-101">Import-AzBlueprintWithArtifact</span><span class="sxs-lookup"><span data-stu-id="833cb-101">Import-AzBlueprintWithArtifact</span></span>

## <span data-ttu-id="833cb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="833cb-102">SYNOPSIS</span></span>
<span data-ttu-id="833cb-103">Importieren Sie eine Blaupausendatei im JSON-Format in ein Blaupausenobjekt, und speichern Sie sie in der angegebenen Abonnement- oder Verwaltungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="833cb-103">Import a blueprint file in JSON format to a blueprint object and save it within the specified subscription or management group.</span></span>

## <span data-ttu-id="833cb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="833cb-104">SYNTAX</span></span>

```
Import-AzBlueprintWithArtifact -Name <String> [-SubscriptionId <String>] [-ManagementGroupId <String>]
 -InputPath <String> [-IncludeSubFolders] [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="833cb-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="833cb-105">DESCRIPTION</span></span>
<span data-ttu-id="833cb-106">Importieren Sie eine Blaupausendefinition mit ihren Artefakten.</span><span class="sxs-lookup"><span data-stu-id="833cb-106">Import a blueprint definition with its artifacts.</span></span> 

## <span data-ttu-id="833cb-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="833cb-107">EXAMPLES</span></span>

### <span data-ttu-id="833cb-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="833cb-108">Example 1</span></span>
```powershell
PS C:\> Import-AzBlueprintWithArtifact -Name MySimpleBlueprint -SubscriptionId 00000000-1111-0000-1111-000000000000 -InputPath  C:\Blueprints\SimpleBlueprint
```

<span data-ttu-id="833cb-109">Importieren Sie eine Blaupausendefinition mit ihren Artefakten, und speichern Sie sie in einem Abonnement.</span><span class="sxs-lookup"><span data-stu-id="833cb-109">Import a blueprint definition with its artifacts and save within a subscription.</span></span>

## <span data-ttu-id="833cb-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="833cb-110">PARAMETERS</span></span>

### <span data-ttu-id="833cb-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="833cb-111">-DefaultProfile</span></span>
<span data-ttu-id="833cb-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="833cb-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="833cb-113">-Force</span><span class="sxs-lookup"><span data-stu-id="833cb-113">-Force</span></span>
<span data-ttu-id="833cb-114">Wenn dies auf "true" festgelegt ist, wird bei der Ausführung keine Bestätigung verlangt.</span><span class="sxs-lookup"><span data-stu-id="833cb-114">When set to true, execution will not ask for a confirmation.</span></span>

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

### <span data-ttu-id="833cb-115">-IncludeSubFolders</span><span class="sxs-lookup"><span data-stu-id="833cb-115">-IncludeSubFolders</span></span>
<span data-ttu-id="833cb-116">Wenn dies auf "true" festgelegt ist, wird das Artefakt in den Unterordnern eingeschlossen.</span><span class="sxs-lookup"><span data-stu-id="833cb-116">When set to true, artifact in the subfolders will be included.</span></span>

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

### <span data-ttu-id="833cb-117">-InputPath</span><span class="sxs-lookup"><span data-stu-id="833cb-117">-InputPath</span></span>
<span data-ttu-id="833cb-118">Pfad zu einer "Blueprint JSON"-Datei auf dem Datenträger.</span><span class="sxs-lookup"><span data-stu-id="833cb-118">Path to a Blueprint JSON file on disk.</span></span>

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

### <span data-ttu-id="833cb-119">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="833cb-119">-ManagementGroupId</span></span>
<span data-ttu-id="833cb-120">ID der Managementgruppe, in der die Blaupausendefinition gespeichert wird oder wird.</span><span class="sxs-lookup"><span data-stu-id="833cb-120">Management Group Id where the blueprint definition is or will be saved.</span></span>

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

### <span data-ttu-id="833cb-121">-Name</span><span class="sxs-lookup"><span data-stu-id="833cb-121">-Name</span></span>
<span data-ttu-id="833cb-122">Name der Blaupause.</span><span class="sxs-lookup"><span data-stu-id="833cb-122">Blueprint definition name.</span></span>

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

### <span data-ttu-id="833cb-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="833cb-123">-PassThru</span></span>
<span data-ttu-id="833cb-124">Nach dem Festlegen gibt das Cmdlet ein Objekt zurück, das die importierte Blaupausendefinition darstellt.</span><span class="sxs-lookup"><span data-stu-id="833cb-124">When set, the cmdlet will return an object representing the imported blueprint definition.</span></span> <span data-ttu-id="833cb-125">Standardmäßig generiert dieses Cmdlet keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="833cb-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="833cb-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="833cb-126">-SubscriptionId</span></span>
<span data-ttu-id="833cb-127">Abonnement-ID, mit der die Blaupausendefinition gespeichert wird oder wird.</span><span class="sxs-lookup"><span data-stu-id="833cb-127">Subscription Id where the blueprint definition is or will be saved.</span></span>

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

### <span data-ttu-id="833cb-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="833cb-128">-Confirm</span></span>
<span data-ttu-id="833cb-129">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="833cb-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="833cb-130">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="833cb-130">-WhatIf</span></span>
<span data-ttu-id="833cb-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="833cb-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="833cb-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="833cb-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="833cb-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="833cb-133">CommonParameters</span></span>
<span data-ttu-id="833cb-134">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="833cb-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="833cb-135">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="833cb-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="833cb-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="833cb-136">INPUTS</span></span>

### <span data-ttu-id="833cb-137">System.String</span><span class="sxs-lookup"><span data-stu-id="833cb-137">System.String</span></span>

## <span data-ttu-id="833cb-138">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="833cb-138">OUTPUTS</span></span>

### <span data-ttu-id="833cb-139">System.String</span><span class="sxs-lookup"><span data-stu-id="833cb-139">System.String</span></span>

## <span data-ttu-id="833cb-140">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="833cb-140">NOTES</span></span>

## <span data-ttu-id="833cb-141">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="833cb-141">RELATED LINKS</span></span>
