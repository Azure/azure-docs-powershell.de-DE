---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/remove-azsynapsesqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlDatabase.md
ms.openlocfilehash: a60bcb20610449b9f76ff3e62684da43a2a792c8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101922603"
---
# <span data-ttu-id="e9115-101">Remove-AzSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="e9115-101">Remove-AzSynapseSqlDatabase</span></span>

## <span data-ttu-id="e9115-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e9115-102">SYNOPSIS</span></span>
<span data-ttu-id="e9115-103">Löscht eine Synapse Analytics-SQL Datenbank.</span><span class="sxs-lookup"><span data-stu-id="e9115-103">Deletes a Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="e9115-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e9115-104">SYNTAX</span></span>

### <span data-ttu-id="e9115-105">DeleteByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="e9115-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseSqlDatabase [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-PassThru]
 [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e9115-106">DeleteByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e9115-106">DeleteByParentObjectParameterSet</span></span>
```
Remove-AzSynapseSqlDatabase -Name <String> -WorkspaceObject <PSSynapseWorkspace> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e9115-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e9115-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzSynapseSqlDatabase -InputObject <PSSynapseSqlDatabase> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e9115-108">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e9115-108">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzSynapseSqlDatabase -ResourceId <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e9115-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e9115-109">DESCRIPTION</span></span>
<span data-ttu-id="e9115-110">Das **Cmdlet Remove-AzSynapseSqlPool** löscht eine Azure Synapse Analytics-SQL Datenbank.</span><span class="sxs-lookup"><span data-stu-id="e9115-110">The **Remove-AzSynapseSqlPool** cmdlet permanently deletes an Azure Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="e9115-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e9115-111">EXAMPLES</span></span>

### <span data-ttu-id="e9115-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e9115-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseSqlDatabase -WorkspaceName ContosoWorkspace -Name ContosoSqlDatabase
```

<span data-ttu-id="e9115-113">Mit diesem Befehl wird eine Azure Synapse Analytics-SQL gelöscht.</span><span class="sxs-lookup"><span data-stu-id="e9115-113">This command deletes an Azure Synapse Analytics SQL database.</span></span>

### <span data-ttu-id="e9115-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="e9115-114">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseSqlDatabase -Name ContosoSqlDatabase
```

<span data-ttu-id="e9115-115">Mit diesem Befehl wird eine Azure Synapse Analytics SQL Pipeline gelöscht.</span><span class="sxs-lookup"><span data-stu-id="e9115-115">This command deletes an Azure Synapse Analytics SQL database through pipeline.</span></span>

### <span data-ttu-id="e9115-116">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="e9115-116">Example 3</span></span>
```powershell
PS C:\> $database = Get-AzSynapseSqlDatabase -WorkspaceName ContosoWorkspace -Name ContosoSqlDatabase
PS C:\> $database | Remove-AzSynapseSqlDatabase
```

<span data-ttu-id="e9115-117">Mit diesem Befehl wird eine Azure Synapse Analytics SQL Pipeline gelöscht.</span><span class="sxs-lookup"><span data-stu-id="e9115-117">This command deletes an Azure Synapse Analytics SQL database through pipeline.</span></span>

### <span data-ttu-id="e9115-118">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="e9115-118">Example 4</span></span>
```powershell
PS C:\> Remove-AzSynapseSqlDatabase -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/sqlDatabases/ContosoSqlDatabase
```

<span data-ttu-id="e9115-119">Mit diesem Befehl wird eine Azure Synapse Analytics SQL datenbank mit der angegebenen Ressourcen-ID gelöscht.</span><span class="sxs-lookup"><span data-stu-id="e9115-119">This command deletes an Azure Synapse Analytics SQL database with the specified resource ID.</span></span>

## <span data-ttu-id="e9115-120">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="e9115-120">PARAMETERS</span></span>

### <span data-ttu-id="e9115-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e9115-121">-AsJob</span></span>
<span data-ttu-id="e9115-122">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="e9115-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e9115-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9115-123">-DefaultProfile</span></span>
<span data-ttu-id="e9115-124">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e9115-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e9115-125">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="e9115-125">-Force</span></span>
<span data-ttu-id="e9115-126">Bitten Sie nicht um Bestätigung.</span><span class="sxs-lookup"><span data-stu-id="e9115-126">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="e9115-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e9115-127">-InputObject</span></span>
<span data-ttu-id="e9115-128">SQL Datenbankeingabeobjekt, das normalerweise über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="e9115-128">SQL Database input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="e9115-129">-Name</span><span class="sxs-lookup"><span data-stu-id="e9115-129">-Name</span></span>
<span data-ttu-id="e9115-130">Name von Synapse SQL Datenbank.</span><span class="sxs-lookup"><span data-stu-id="e9115-130">Name of Synapse SQL Database.</span></span>

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

### <span data-ttu-id="e9115-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e9115-131">-PassThru</span></span>
<span data-ttu-id="e9115-132">Dieses Cmdlet gibt standardmäßig kein -Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="e9115-132">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="e9115-133">Wenn dieser Schalter angegeben ist, gibt er "true" zurück, wenn er erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="e9115-133">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="e9115-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e9115-134">-ResourceGroupName</span></span>
<span data-ttu-id="e9115-135">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="e9115-135">Resource group name.</span></span>

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

### <span data-ttu-id="e9115-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e9115-136">-ResourceId</span></span>
<span data-ttu-id="e9115-137">Ressourcenbezeichner von Synapse SQL Datenbank.</span><span class="sxs-lookup"><span data-stu-id="e9115-137">Resource identifier of Synapse SQL Database.</span></span>

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

### <span data-ttu-id="e9115-138">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="e9115-138">-WorkspaceName</span></span>
<span data-ttu-id="e9115-139">Name des Synapse-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="e9115-139">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="e9115-140">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="e9115-140">-WorkspaceObject</span></span>
<span data-ttu-id="e9115-141">Arbeitsbereichseingabeobjekt, das in der Regel über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="e9115-141">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="e9115-142">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e9115-142">-Confirm</span></span>
<span data-ttu-id="e9115-143">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e9115-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e9115-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e9115-144">-WhatIf</span></span>
<span data-ttu-id="e9115-145">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e9115-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e9115-146">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e9115-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e9115-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9115-147">CommonParameters</span></span>
<span data-ttu-id="e9115-148">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e9115-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9115-149">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e9115-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9115-150">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e9115-150">INPUTS</span></span>

### <span data-ttu-id="e9115-151">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="e9115-151">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="e9115-152">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="e9115-152">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlDatabase</span></span>

### <span data-ttu-id="e9115-153">System.String</span><span class="sxs-lookup"><span data-stu-id="e9115-153">System.String</span></span>

## <span data-ttu-id="e9115-154">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e9115-154">OUTPUTS</span></span>

### <span data-ttu-id="e9115-155">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="e9115-155">System.Boolean</span></span>

## <span data-ttu-id="e9115-156">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="e9115-156">NOTES</span></span>

## <span data-ttu-id="e9115-157">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="e9115-157">RELATED LINKS</span></span>
