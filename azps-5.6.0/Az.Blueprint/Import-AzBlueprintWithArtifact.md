---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/powershell/module/az.blueprint/import-azblueprintwithartifact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Import-AzBlueprintWithArtifact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Import-AzBlueprintWithArtifact.md
ms.openlocfilehash: eb0fddc34a83d5a23aeb990c920f36d7a3e03ff2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101932051"
---
# <span data-ttu-id="598df-101">Import-AzBlueprintWithArtifact</span><span class="sxs-lookup"><span data-stu-id="598df-101">Import-AzBlueprintWithArtifact</span></span>

## <span data-ttu-id="598df-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="598df-102">SYNOPSIS</span></span>
<span data-ttu-id="598df-103">Importieren Sie eine Blaupausendatei im JSON-Format in ein Blaupausenobjekt, und speichern Sie sie in der angegebenen Abonnement- oder Verwaltungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="598df-103">Import a blueprint file in JSON format to a blueprint object and save it within the specified subscription or management group.</span></span>

## <span data-ttu-id="598df-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="598df-104">SYNTAX</span></span>

```
Import-AzBlueprintWithArtifact -Name <String> [-SubscriptionId <String>] [-ManagementGroupId <String>]
 -InputPath <String> [-IncludeSubFolders] [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="598df-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="598df-105">DESCRIPTION</span></span>
<span data-ttu-id="598df-106">Importieren Sie eine Blaupausendefinition mit ihren Artefakten.</span><span class="sxs-lookup"><span data-stu-id="598df-106">Import a blueprint definition with its artifacts.</span></span> 

## <span data-ttu-id="598df-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="598df-107">EXAMPLES</span></span>

### <span data-ttu-id="598df-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="598df-108">Example 1</span></span>
```powershell
PS C:\> Import-AzBlueprintWithArtifact -Name MySimpleBlueprint -SubscriptionId 00000000-1111-0000-1111-000000000000 -InputPath  C:\Blueprints\SimpleBlueprint
```

<span data-ttu-id="598df-109">Importieren Sie eine Blaupausendefinition mit ihren Artefakten, und speichern Sie sie in einem Abonnement.</span><span class="sxs-lookup"><span data-stu-id="598df-109">Import a blueprint definition with its artifacts and save within a subscription.</span></span>

## <span data-ttu-id="598df-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="598df-110">PARAMETERS</span></span>

### <span data-ttu-id="598df-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="598df-111">-DefaultProfile</span></span>
<span data-ttu-id="598df-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="598df-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="598df-113">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="598df-113">-Force</span></span>
<span data-ttu-id="598df-114">Wenn die Ausführung auf "true" festgelegt ist, wird keine Bestätigung verlangt.</span><span class="sxs-lookup"><span data-stu-id="598df-114">When set to true, execution will not ask for a confirmation.</span></span>

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

### <span data-ttu-id="598df-115">-IncludeSubFolders</span><span class="sxs-lookup"><span data-stu-id="598df-115">-IncludeSubFolders</span></span>
<span data-ttu-id="598df-116">Wenn sie auf "true" festgelegt ist, wird das Artefakt in den Unterordnern eingeschlossen.</span><span class="sxs-lookup"><span data-stu-id="598df-116">When set to true, artifact in the subfolders will be included.</span></span>

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

### <span data-ttu-id="598df-117">-InputPath</span><span class="sxs-lookup"><span data-stu-id="598df-117">-InputPath</span></span>
<span data-ttu-id="598df-118">Pfad zu einer Blueprint-JSON-Datei auf dem Datenträger.</span><span class="sxs-lookup"><span data-stu-id="598df-118">Path to a Blueprint JSON file on disk.</span></span>

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

### <span data-ttu-id="598df-119">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="598df-119">-ManagementGroupId</span></span>
<span data-ttu-id="598df-120">Verwaltungsgruppen-ID, in der die Blaupausendefinition gespeichert wird oder gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="598df-120">Management Group Id where the blueprint definition is or will be saved.</span></span>

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

### <span data-ttu-id="598df-121">-Name</span><span class="sxs-lookup"><span data-stu-id="598df-121">-Name</span></span>
<span data-ttu-id="598df-122">Name der Blaupausedefinition.</span><span class="sxs-lookup"><span data-stu-id="598df-122">Blueprint definition name.</span></span>

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

### <span data-ttu-id="598df-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="598df-123">-PassThru</span></span>
<span data-ttu-id="598df-124">Wenn festgelegt, gibt das Cmdlet ein -Objekt zurück, das die importierte Blaupausendefinition darstellt.</span><span class="sxs-lookup"><span data-stu-id="598df-124">When set, the cmdlet will return an object representing the imported blueprint definition.</span></span> <span data-ttu-id="598df-125">Standardmäßig generiert dieses Cmdlet keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="598df-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="598df-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="598df-126">-SubscriptionId</span></span>
<span data-ttu-id="598df-127">Abonnement-ID, bei der die Blaupausendefinition gespeichert wird oder gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="598df-127">Subscription Id where the blueprint definition is or will be saved.</span></span>

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

### <span data-ttu-id="598df-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="598df-128">-Confirm</span></span>
<span data-ttu-id="598df-129">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="598df-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="598df-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="598df-130">-WhatIf</span></span>
<span data-ttu-id="598df-131">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="598df-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="598df-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="598df-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="598df-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="598df-133">CommonParameters</span></span>
<span data-ttu-id="598df-134">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="598df-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="598df-135">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="598df-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="598df-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="598df-136">INPUTS</span></span>

### <span data-ttu-id="598df-137">System.String</span><span class="sxs-lookup"><span data-stu-id="598df-137">System.String</span></span>

## <span data-ttu-id="598df-138">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="598df-138">OUTPUTS</span></span>

### <span data-ttu-id="598df-139">System.String</span><span class="sxs-lookup"><span data-stu-id="598df-139">System.String</span></span>

## <span data-ttu-id="598df-140">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="598df-140">NOTES</span></span>

## <span data-ttu-id="598df-141">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="598df-141">RELATED LINKS</span></span>
