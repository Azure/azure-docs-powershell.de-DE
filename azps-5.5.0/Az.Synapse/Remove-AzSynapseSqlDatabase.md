---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsesqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlDatabase.md
ms.openlocfilehash: 4951fbe707dbae8c1fdff34e828e468a2d3168bf
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100173556"
---
# <span data-ttu-id="75abb-101">Remove-AzSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="75abb-101">Remove-AzSynapseSqlDatabase</span></span>

## <span data-ttu-id="75abb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="75abb-102">SYNOPSIS</span></span>
<span data-ttu-id="75abb-103">Löscht eine Synapse Analytics SQL Datenbank.</span><span class="sxs-lookup"><span data-stu-id="75abb-103">Deletes a Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="75abb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="75abb-104">SYNTAX</span></span>

### <span data-ttu-id="75abb-105">DeleteByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="75abb-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseSqlDatabase [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-PassThru]
 [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="75abb-106">DeleteByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="75abb-106">DeleteByParentObjectParameterSet</span></span>
```
Remove-AzSynapseSqlDatabase -Name <String> -WorkspaceObject <PSSynapseWorkspace> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="75abb-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="75abb-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzSynapseSqlDatabase -InputObject <PSSynapseSqlDatabase> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="75abb-108">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="75abb-108">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzSynapseSqlDatabase -ResourceId <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="75abb-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="75abb-109">DESCRIPTION</span></span>
<span data-ttu-id="75abb-110">Das **Cmdlet "Remove-AzSynapseSqlPool"** löscht eine Azure Synapse Analytics SQL Datenbank.</span><span class="sxs-lookup"><span data-stu-id="75abb-110">The **Remove-AzSynapseSqlPool** cmdlet permanently deletes an Azure Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="75abb-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="75abb-111">EXAMPLES</span></span>

### <span data-ttu-id="75abb-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="75abb-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseSqlDatabase -WorkspaceName ContosoWorkspace -Name ContosoSqlDatabase
```

<span data-ttu-id="75abb-113">Mit diesem Befehl wird eine Azure Synapse Analytics SQL gelöscht.</span><span class="sxs-lookup"><span data-stu-id="75abb-113">This command deletes an Azure Synapse Analytics SQL database.</span></span>

### <span data-ttu-id="75abb-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="75abb-114">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseSqlDatabase -Name ContosoSqlDatabase
```

<span data-ttu-id="75abb-115">Mit diesem Befehl wird eine Azure Synapse Analytics SQL Pipeline gelöscht.</span><span class="sxs-lookup"><span data-stu-id="75abb-115">This command deletes an Azure Synapse Analytics SQL database through pipeline.</span></span>

### <span data-ttu-id="75abb-116">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="75abb-116">Example 3</span></span>
```powershell
PS C:\> $database = Get-AzSynapseSqlDatabase -WorkspaceName ContosoWorkspace -Name ContosoSqlDatabase
PS C:\> $database | Remove-AzSynapseSqlDatabase
```

<span data-ttu-id="75abb-117">Mit diesem Befehl wird eine Azure Synapse Analytics SQL Pipeline gelöscht.</span><span class="sxs-lookup"><span data-stu-id="75abb-117">This command deletes an Azure Synapse Analytics SQL database through pipeline.</span></span>

### <span data-ttu-id="75abb-118">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="75abb-118">Example 4</span></span>
```powershell
PS C:\> Remove-AzSynapseSqlDatabase -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/sqlDatabases/ContosoSqlDatabase
```

<span data-ttu-id="75abb-119">Mit diesem Befehl wird eine Azure Synapse Analytics SQL Datenbank mit der angegebenen Ressourcen-ID gelöscht.</span><span class="sxs-lookup"><span data-stu-id="75abb-119">This command deletes an Azure Synapse Analytics SQL database with the specified resource ID.</span></span>

## <span data-ttu-id="75abb-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="75abb-120">PARAMETERS</span></span>

### <span data-ttu-id="75abb-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="75abb-121">-AsJob</span></span>
<span data-ttu-id="75abb-122">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="75abb-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="75abb-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75abb-123">-DefaultProfile</span></span>
<span data-ttu-id="75abb-124">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="75abb-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="75abb-125">-Force</span><span class="sxs-lookup"><span data-stu-id="75abb-125">-Force</span></span>
<span data-ttu-id="75abb-126">Fordern Sie keine Bestätigung an.</span><span class="sxs-lookup"><span data-stu-id="75abb-126">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="75abb-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="75abb-127">-InputObject</span></span>
<span data-ttu-id="75abb-128">SQL Datenbankeingabeobjekts, das in der Regel über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="75abb-128">SQL Database input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlDatabase
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="75abb-129">-Name</span><span class="sxs-lookup"><span data-stu-id="75abb-129">-Name</span></span>
<span data-ttu-id="75abb-130">Name der Datenbank von Synapse SQL Datenbank.</span><span class="sxs-lookup"><span data-stu-id="75abb-130">Name of Synapse SQL Database.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet, DeleteByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75abb-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="75abb-131">-PassThru</span></span>
<span data-ttu-id="75abb-132">Dieses Cmdlet gibt standardmäßig kein Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="75abb-132">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="75abb-133">Wenn dieser Schalter angegeben ist, wird "true" zurückgegeben, wenn er erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="75abb-133">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="75abb-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75abb-134">-ResourceGroupName</span></span>
<span data-ttu-id="75abb-135">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="75abb-135">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75abb-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="75abb-136">-ResourceId</span></span>
<span data-ttu-id="75abb-137">Ressourcenbezeichner von Synapse SQL Datenbank.</span><span class="sxs-lookup"><span data-stu-id="75abb-137">Resource identifier of Synapse SQL Database.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75abb-138">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="75abb-138">-WorkspaceName</span></span>
<span data-ttu-id="75abb-139">Name des Synapse-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="75abb-139">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75abb-140">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="75abb-140">-WorkspaceObject</span></span>
<span data-ttu-id="75abb-141">Arbeitsbereichseingabeobjekts, das in der Regel über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="75abb-141">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: DeleteByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="75abb-142">-Confirm</span><span class="sxs-lookup"><span data-stu-id="75abb-142">-Confirm</span></span>
<span data-ttu-id="75abb-143">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="75abb-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="75abb-144">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="75abb-144">-WhatIf</span></span>
<span data-ttu-id="75abb-145">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="75abb-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="75abb-146">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="75abb-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="75abb-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75abb-147">CommonParameters</span></span>
<span data-ttu-id="75abb-148">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75abb-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75abb-149">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="75abb-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75abb-150">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="75abb-150">INPUTS</span></span>

### <span data-ttu-id="75abb-151">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="75abb-151">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="75abb-152">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="75abb-152">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlDatabase</span></span>

### <span data-ttu-id="75abb-153">System.String</span><span class="sxs-lookup"><span data-stu-id="75abb-153">System.String</span></span>

## <span data-ttu-id="75abb-154">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="75abb-154">OUTPUTS</span></span>

### <span data-ttu-id="75abb-155">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="75abb-155">System.Boolean</span></span>

## <span data-ttu-id="75abb-156">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="75abb-156">NOTES</span></span>

## <span data-ttu-id="75abb-157">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="75abb-157">RELATED LINKS</span></span>
