---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/remove-azsynapsesqlpoolrestorepoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlPoolRestorePoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlPoolRestorePoint.md
ms.openlocfilehash: 6105b043ee1e21ddbf2f29ce6bf0819639a133d3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101928419"
---
# <span data-ttu-id="5baa1-101">Remove-AzSynapseSqlPoolRestorePoint</span><span class="sxs-lookup"><span data-stu-id="5baa1-101">Remove-AzSynapseSqlPoolRestorePoint</span></span>

## <span data-ttu-id="5baa1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5baa1-102">SYNOPSIS</span></span>
<span data-ttu-id="5baa1-103">Löscht einen Synapse Analytics SQL Poolwiederherstellungspunkt.</span><span class="sxs-lookup"><span data-stu-id="5baa1-103">Deletes a Synapse Analytics SQL pool restore point.</span></span>

## <span data-ttu-id="5baa1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5baa1-104">SYNTAX</span></span>

### <span data-ttu-id="5baa1-105">DeleteByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="5baa1-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseSqlPoolRestorePoint [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 -RestorePointCreationDate <DateTime> [-PassThru] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5baa1-106">DeleteByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5baa1-106">DeleteByParentObjectParameterSet</span></span>
```
Remove-AzSynapseSqlPoolRestorePoint -RestorePointCreationDate <DateTime> -SqlPoolObject <PSSynapseSqlPool>
 [-PassThru] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5baa1-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5baa1-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzSynapseSqlPoolRestorePoint -InputObject <PSRestorePoint> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5baa1-108">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5baa1-108">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzSynapseSqlPoolRestorePoint -ResourceId <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5baa1-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5baa1-109">DESCRIPTION</span></span>
<span data-ttu-id="5baa1-110">Das **Cmdlet Remove-AzSynapseSqlPoolRestorePoint** löscht einen Azure Synapse Analytics-SQL-Wiederherstellungspunkt endgültig.</span><span class="sxs-lookup"><span data-stu-id="5baa1-110">The **Remove-AzSynapseSqlPoolRestorePoint** cmdlet permanently deletes an Azure Synapse Analytics SQL pool restore point.</span></span>

## <span data-ttu-id="5baa1-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="5baa1-111">EXAMPLES</span></span>

### <span data-ttu-id="5baa1-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="5baa1-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseSqlPoolRestorePoint -WorkspaceName ContosoWorkspace -SqlPoolName ContosoSqlPool -Name ContosoSqlPoolRestorePointCreationDate
```

<span data-ttu-id="5baa1-113">Mit diesem Befehl wird ein Azure Synapse Analytics SQL Poolwiederherstellungspunkt gelöscht.</span><span class="sxs-lookup"><span data-stu-id="5baa1-113">This command deletes an Azure Synapse Analytics SQL pool restore point.</span></span>

### <span data-ttu-id="5baa1-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="5baa1-114">Example 2</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
PS C:\> $pool | Remove-AzSynapseSqlPoolRestorePoint -Name ContosoSqlPoolRestorePointCreationDate
```

<span data-ttu-id="5baa1-115">Mit diesem Befehl wird ein Azure Synapse Analytics SQL pool restore point through pipeline gelöscht.</span><span class="sxs-lookup"><span data-stu-id="5baa1-115">This command deletes an Azure Synapse Analytics SQL pool restore point through pipeline.</span></span>

### <span data-ttu-id="5baa1-116">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="5baa1-116">Example 3</span></span>
```powershell
PS C:\> $points = Get-AzSynapseSqlPoolRestorePoint -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
PS C:\> $points[index] | Remove-AzSynapseSqlPoolRestorePoint
```

<span data-ttu-id="5baa1-117">Mit diesem Befehl wird ein Azure Synapse Analytics SQL pool restore point through pipeline gelöscht.</span><span class="sxs-lookup"><span data-stu-id="5baa1-117">This command deletes an Azure Synapse Analytics SQL pool restore point through pipeline.</span></span>

### <span data-ttu-id="5baa1-118">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="5baa1-118">Example 4</span></span>
```powershell
PS C:\> Remove-AzSynapseSqlPoolRestorePoint -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/sqlPools/ContosoSqlPool/SqlPoolRestorePoints/RestorePointCreationDate
```

<span data-ttu-id="5baa1-119">Mit diesem Befehl wird ein Azure Synapse Analytics SQL Poolwiederherstellungspunkt mit der angegebenen Ressourcen-ID gelöscht.</span><span class="sxs-lookup"><span data-stu-id="5baa1-119">This command deletes an Azure Synapse Analytics SQL pool restore point with the specified resource ID.</span></span>

## <span data-ttu-id="5baa1-120">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="5baa1-120">PARAMETERS</span></span>

### <span data-ttu-id="5baa1-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5baa1-121">-AsJob</span></span>
<span data-ttu-id="5baa1-122">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="5baa1-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5baa1-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5baa1-123">-DefaultProfile</span></span>
<span data-ttu-id="5baa1-124">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5baa1-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5baa1-125">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="5baa1-125">-Force</span></span>
<span data-ttu-id="5baa1-126">Bitten Sie nicht um Bestätigung.</span><span class="sxs-lookup"><span data-stu-id="5baa1-126">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="5baa1-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5baa1-127">-InputObject</span></span>
<span data-ttu-id="5baa1-128">SQL pool restore point creation time input object, usually passed through the pipeline.</span><span class="sxs-lookup"><span data-stu-id="5baa1-128">SQL pool restore point creation time input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSRestorePoint
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5baa1-129">-Name</span><span class="sxs-lookup"><span data-stu-id="5baa1-129">-Name</span></span>
<span data-ttu-id="5baa1-130">Name des Synapse SQL Pools.</span><span class="sxs-lookup"><span data-stu-id="5baa1-130">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases: SqlPoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5baa1-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5baa1-131">-PassThru</span></span>
<span data-ttu-id="5baa1-132">Dieses Cmdlet gibt standardmäßig kein -Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="5baa1-132">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="5baa1-133">Wenn dieser Schalter angegeben ist, gibt er "true" zurück, wenn er erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="5baa1-133">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="5baa1-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5baa1-134">-ResourceGroupName</span></span>
<span data-ttu-id="5baa1-135">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="5baa1-135">Resource group name.</span></span>

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

### <span data-ttu-id="5baa1-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5baa1-136">-ResourceId</span></span>
<span data-ttu-id="5baa1-137">Ressourcenbezeichner von Synapse SQL Pool.</span><span class="sxs-lookup"><span data-stu-id="5baa1-137">Resource identifier of Synapse SQL Pool.</span></span>

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

### <span data-ttu-id="5baa1-138">-RestorePointCreationDate</span><span class="sxs-lookup"><span data-stu-id="5baa1-138">-RestorePointCreationDate</span></span>
<span data-ttu-id="5baa1-139">Name von Synapse SQL Datum der Punkterstellung wiederherstellen.</span><span class="sxs-lookup"><span data-stu-id="5baa1-139">Name of Synapse SQL Restore Point Creation Date .</span></span>

```yaml
Type: System.DateTime
Parameter Sets: DeleteByNameParameterSet, DeleteByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5baa1-140">-SqlPoolObject</span><span class="sxs-lookup"><span data-stu-id="5baa1-140">-SqlPoolObject</span></span>
<span data-ttu-id="5baa1-141">Sql Pool-Eingabeobjekt, das in der Regel über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="5baa1-141">Sql Pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: DeleteByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5baa1-142">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="5baa1-142">-WorkspaceName</span></span>
<span data-ttu-id="5baa1-143">Name des Synapse-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="5baa1-143">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="5baa1-144">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="5baa1-144">-Confirm</span></span>
<span data-ttu-id="5baa1-145">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5baa1-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5baa1-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5baa1-146">-WhatIf</span></span>
<span data-ttu-id="5baa1-147">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5baa1-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5baa1-148">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5baa1-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5baa1-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5baa1-149">CommonParameters</span></span>
<span data-ttu-id="5baa1-150">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5baa1-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5baa1-151">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5baa1-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5baa1-152">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="5baa1-152">INPUTS</span></span>

### <span data-ttu-id="5baa1-153">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="5baa1-153">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="5baa1-154">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="5baa1-154">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

### <span data-ttu-id="5baa1-155">Microsoft.Azure.Commands.Synapse.Models.PSRestorePoint</span><span class="sxs-lookup"><span data-stu-id="5baa1-155">Microsoft.Azure.Commands.Synapse.Models.PSRestorePoint</span></span>

### <span data-ttu-id="5baa1-156">System.String</span><span class="sxs-lookup"><span data-stu-id="5baa1-156">System.String</span></span>

## <span data-ttu-id="5baa1-157">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="5baa1-157">OUTPUTS</span></span>

### <span data-ttu-id="5baa1-158">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="5baa1-158">System.Boolean</span></span>

## <span data-ttu-id="5baa1-159">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="5baa1-159">NOTES</span></span>

## <span data-ttu-id="5baa1-160">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="5baa1-160">RELATED LINKS</span></span>
