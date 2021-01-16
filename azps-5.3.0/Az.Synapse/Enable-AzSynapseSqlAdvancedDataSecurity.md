---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/enable-azsynapsesqladvanceddatasecurity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Enable-AzSynapseSqlAdvancedDataSecurity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Enable-AzSynapseSqlAdvancedDataSecurity.md
ms.openlocfilehash: dea0770af8cca14ebd523f67b69d7a12931183ec
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98384136"
---
# <span data-ttu-id="fe648-101">Enable-AzSynapseSqlAdvancedDataSecurity</span><span class="sxs-lookup"><span data-stu-id="fe648-101">Enable-AzSynapseSqlAdvancedDataSecurity</span></span>

## <span data-ttu-id="fe648-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fe648-102">SYNOPSIS</span></span>
<span data-ttu-id="fe648-103">Aktiviert Advanced Data Security in einem Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="fe648-103">Enables Advanced Data Security on a workspace.</span></span>

## <span data-ttu-id="fe648-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fe648-104">SYNTAX</span></span>

### <span data-ttu-id="fe648-105">EnableByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="fe648-105">EnableByNameParameterSet (Default)</span></span>
```
Enable-AzSynapseSqlAdvancedDataSecurity [-ResourceGroupName <String>] -WorkspaceName <String>
 [-DoNotConfigureVulnerabilityAssessment] [-DeploymentName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fe648-106">EnableByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fe648-106">EnableByInputObjectParameterSet</span></span>
```
Enable-AzSynapseSqlAdvancedDataSecurity -InputObject <PSSynapseWorkspace>
 [-DoNotConfigureVulnerabilityAssessment] [-DeploymentName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fe648-107">EnableByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fe648-107">EnableByResourceIdParameterSet</span></span>
```
Enable-AzSynapseSqlAdvancedDataSecurity -ResourceId <String> [-DoNotConfigureVulnerabilityAssessment]
 [-DeploymentName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fe648-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fe648-108">DESCRIPTION</span></span>
<span data-ttu-id="fe648-109">Das **Cmdlet Enable-AzSynapseSqlAdvancedDataSecurity** aktiviert Advanced Data Security in einem Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="fe648-109">The **Enable-AzSynapseSqlAdvancedDataSecurity** cmdlet enables Advanced Data Security on a workspace.</span></span> <span data-ttu-id="fe648-110">Advanced Data Security ist ein einheitliches Sicherheitspaket mit Datenklassifizierung, Sicherheitsrisikobewertung und Advanced Threat Protection für Ihren Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="fe648-110">Advanced Data Security is a unified security package that includes Data Classification, Vulnerability Assessment and Advanced Threat Protection for your workspace.</span></span> <span data-ttu-id="fe648-111">(Es wird automatisch ein neues Speicherkonto erstellt, um Sicherheitsrisikobewertungen zu sparen.</span><span class="sxs-lookup"><span data-stu-id="fe648-111">(A new storage account will automatically be created for saving vulnerability assessments.</span></span> <span data-ttu-id="fe648-112">Wenn zu diesem Zweck zuvor ein Speicherkonto erstellt wurde, wird es stattdessen verwendet.)</span><span class="sxs-lookup"><span data-stu-id="fe648-112">If a storage account was previously created for this purpose, it will be used instead)</span></span>

## <span data-ttu-id="fe648-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="fe648-113">EXAMPLES</span></span>

### <span data-ttu-id="fe648-114">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="fe648-114">Example 1</span></span>
```powershell
PS C:\> Enable-AzSynapseSqlAdvancedDataSecurity -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="fe648-115">Dieser Befehl aktiviert die erweiterte Datensicherheit des Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="fe648-115">This command enables workspace Advanced Data Security.</span></span>

### <span data-ttu-id="fe648-116">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="fe648-116">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseWorkspace -Name ContosoWorkspace | Enable-AzSynapseSqlAdvancedDataSecurity
```

<span data-ttu-id="fe648-117">Mit diesem Befehl wird die erweiterte Datensicherheit des Arbeitsbereichs über die Pipeline aktiviert.</span><span class="sxs-lookup"><span data-stu-id="fe648-117">This command enables workspace Advanced Data Security through pipeline.</span></span>

### <span data-ttu-id="fe648-118">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="fe648-118">Example 3</span></span>
```powershell
PS C:\> Enable-AzSynapseSqlAdvancedDataSecurity -WorkspaceName ContosoWorkspace -DoNotConfigureVulnerabilityAssessment
```

<span data-ttu-id="fe648-119">Mit diesem Befehl wird advanced Data Security für den Arbeitsbereich über Pipeline aktiviert, und die Sicherheitsrisikobewertung wird nicht automatisch aktiviert.</span><span class="sxs-lookup"><span data-stu-id="fe648-119">This command enables workspace Advanced Data Security through pipeline and does not auto enable Vulnerability Assessment.</span></span>

## <span data-ttu-id="fe648-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fe648-120">PARAMETERS</span></span>

### <span data-ttu-id="fe648-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fe648-121">-AsJob</span></span>
<span data-ttu-id="fe648-122">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="fe648-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fe648-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe648-123">-DefaultProfile</span></span>
<span data-ttu-id="fe648-124">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fe648-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fe648-125">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="fe648-125">-DeploymentName</span></span>
<span data-ttu-id="fe648-126">Geben Sie einen benutzerdefinierten Namen für die Advanced Data Security-Bereitstellung an.</span><span class="sxs-lookup"><span data-stu-id="fe648-126">Supply a custom name for Advanced Data Security deployment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe648-127">-DoNotConfigureVulnerabilityAssessment</span><span class="sxs-lookup"><span data-stu-id="fe648-127">-DoNotConfigureVulnerabilityAssessment</span></span>
<span data-ttu-id="fe648-128">Aktivieren Sie die Sicherheitsrisikobewertung nicht automatisch (dadurch wird kein Speicherkonto erstellt).</span><span class="sxs-lookup"><span data-stu-id="fe648-128">Do not auto enable Vulnerability Assessment (This will not create a storage account).</span></span>

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

### <span data-ttu-id="fe648-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fe648-129">-InputObject</span></span>
<span data-ttu-id="fe648-130">Arbeitsbereichseingabeobjekts, das in der Regel über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="fe648-130">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: EnableByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fe648-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe648-131">-ResourceGroupName</span></span>
<span data-ttu-id="fe648-132">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="fe648-132">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: EnableByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe648-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fe648-133">-ResourceId</span></span>
<span data-ttu-id="fe648-134">Ressourcenbezeichner des Synapse-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="fe648-134">Resource identifier of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: EnableByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe648-135">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="fe648-135">-WorkspaceName</span></span>
<span data-ttu-id="fe648-136">Name des Synapse-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="fe648-136">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: EnableByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe648-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fe648-137">-Confirm</span></span>
<span data-ttu-id="fe648-138">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="fe648-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fe648-139">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="fe648-139">-WhatIf</span></span>
<span data-ttu-id="fe648-140">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fe648-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fe648-141">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="fe648-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fe648-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe648-142">CommonParameters</span></span>
<span data-ttu-id="fe648-143">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe648-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe648-144">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fe648-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe648-145">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="fe648-145">INPUTS</span></span>

### <span data-ttu-id="fe648-146">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="fe648-146">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="fe648-147">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="fe648-147">OUTPUTS</span></span>

### <span data-ttu-id="fe648-148">Microsoft.Azure.Commands.Synapse.Models.WorkspaceAdvancedDataSecurityPolicy</span><span class="sxs-lookup"><span data-stu-id="fe648-148">Microsoft.Azure.Commands.Synapse.Models.WorkspaceAdvancedDataSecurityPolicy</span></span>

## <span data-ttu-id="fe648-149">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="fe648-149">NOTES</span></span>

## <span data-ttu-id="fe648-150">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="fe648-150">RELATED LINKS</span></span>
