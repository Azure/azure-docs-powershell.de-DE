---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsesqlpoolrestorepoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlPoolRestorePoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlPoolRestorePoint.md
ms.openlocfilehash: 63c0dbc30557230f67e419bcde482e445f3df758
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100174953"
---
# <span data-ttu-id="ce19e-101">Remove-AzSynapseSqlPoolRestorePoint</span><span class="sxs-lookup"><span data-stu-id="ce19e-101">Remove-AzSynapseSqlPoolRestorePoint</span></span>

## <span data-ttu-id="ce19e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ce19e-102">SYNOPSIS</span></span>
<span data-ttu-id="ce19e-103">Löscht einen Synapse Analytics SQL Poolwiederherstellungspunkt.</span><span class="sxs-lookup"><span data-stu-id="ce19e-103">Deletes a Synapse Analytics SQL pool restore point.</span></span>

## <span data-ttu-id="ce19e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ce19e-104">SYNTAX</span></span>

### <span data-ttu-id="ce19e-105">DeleteByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="ce19e-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseSqlPoolRestorePoint [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 -RestorePointCreationDate <DateTime> [-PassThru] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ce19e-106">DeleteByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ce19e-106">DeleteByParentObjectParameterSet</span></span>
```
Remove-AzSynapseSqlPoolRestorePoint -RestorePointCreationDate <DateTime> -SqlPoolObject <PSSynapseSqlPool>
 [-PassThru] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ce19e-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ce19e-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzSynapseSqlPoolRestorePoint -InputObject <PSRestorePoint> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ce19e-108">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ce19e-108">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzSynapseSqlPoolRestorePoint -ResourceId <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ce19e-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ce19e-109">DESCRIPTION</span></span>
<span data-ttu-id="ce19e-110">Das **Cmdlet "Remove-AzSynapseSqlPoolRestorePoint"** löscht einen Azure Synapse Analytics SQL Poolwiederherstellungspunkt dauerhaft.</span><span class="sxs-lookup"><span data-stu-id="ce19e-110">The **Remove-AzSynapseSqlPoolRestorePoint** cmdlet permanently deletes an Azure Synapse Analytics SQL pool restore point.</span></span>

## <span data-ttu-id="ce19e-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ce19e-111">EXAMPLES</span></span>

### <span data-ttu-id="ce19e-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ce19e-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseSqlPoolRestorePoint -WorkspaceName ContosoWorkspace -SqlPoolName ContosoSqlPool -Name ContosoSqlPoolRestorePointCreationDate
```

<span data-ttu-id="ce19e-113">Mit diesem Befehl wird ein Azure Synapse Analytics SQL Wiederherstellungspunkt des Pools gelöscht.</span><span class="sxs-lookup"><span data-stu-id="ce19e-113">This command deletes an Azure Synapse Analytics SQL pool restore point.</span></span>

### <span data-ttu-id="ce19e-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="ce19e-114">Example 2</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
PS C:\> $pool | Remove-AzSynapseSqlPoolRestorePoint -Name ContosoSqlPoolRestorePointCreationDate
```

<span data-ttu-id="ce19e-115">Mit diesem Befehl wird ein Azure Synapse Analytics SQL Poolwiederherstellungspunkt über die Pipeline gelöscht.</span><span class="sxs-lookup"><span data-stu-id="ce19e-115">This command deletes an Azure Synapse Analytics SQL pool restore point through pipeline.</span></span>

### <span data-ttu-id="ce19e-116">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="ce19e-116">Example 3</span></span>
```powershell
PS C:\> $points = Get-AzSynapseSqlPoolRestorePoint -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
PS C:\> $points[index] | Remove-AzSynapseSqlPoolRestorePoint
```

<span data-ttu-id="ce19e-117">Mit diesem Befehl wird ein Azure Synapse Analytics SQL Poolwiederherstellungspunkt über die Pipeline gelöscht.</span><span class="sxs-lookup"><span data-stu-id="ce19e-117">This command deletes an Azure Synapse Analytics SQL pool restore point through pipeline.</span></span>

### <span data-ttu-id="ce19e-118">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="ce19e-118">Example 4</span></span>
```powershell
PS C:\> Remove-AzSynapseSqlPoolRestorePoint -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/sqlPools/ContosoSqlPool/SqlPoolRestorePoints/RestorePointCreationDate
```

<span data-ttu-id="ce19e-119">Mit diesem Befehl wird ein Azure Synapse Analytics-SQL-Wiederherstellungspunkt mit der angegebenen Ressourcen-ID gelöscht.</span><span class="sxs-lookup"><span data-stu-id="ce19e-119">This command deletes an Azure Synapse Analytics SQL pool restore point with the specified resource ID.</span></span>

## <span data-ttu-id="ce19e-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ce19e-120">PARAMETERS</span></span>

### <span data-ttu-id="ce19e-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ce19e-121">-AsJob</span></span>
<span data-ttu-id="ce19e-122">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="ce19e-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ce19e-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce19e-123">-DefaultProfile</span></span>
<span data-ttu-id="ce19e-124">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ce19e-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ce19e-125">-Force</span><span class="sxs-lookup"><span data-stu-id="ce19e-125">-Force</span></span>
<span data-ttu-id="ce19e-126">Fordern Sie keine Bestätigung an.</span><span class="sxs-lookup"><span data-stu-id="ce19e-126">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="ce19e-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ce19e-127">-InputObject</span></span>
<span data-ttu-id="ce19e-128">SQL eingabeobjekt für die Erstellungszeit des Poolwiederherstellungspunkts, das in der Regel über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="ce19e-128">SQL pool restore point creation time input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="ce19e-129">-Name</span><span class="sxs-lookup"><span data-stu-id="ce19e-129">-Name</span></span>
<span data-ttu-id="ce19e-130">Name des Synapse SQL Pools.</span><span class="sxs-lookup"><span data-stu-id="ce19e-130">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="ce19e-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ce19e-131">-PassThru</span></span>
<span data-ttu-id="ce19e-132">Dieses Cmdlet gibt standardmäßig kein Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="ce19e-132">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="ce19e-133">Wenn dieser Schalter angegeben ist, wird "true" zurückgegeben, wenn er erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="ce19e-133">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="ce19e-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ce19e-134">-ResourceGroupName</span></span>
<span data-ttu-id="ce19e-135">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="ce19e-135">Resource group name.</span></span>

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

### <span data-ttu-id="ce19e-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ce19e-136">-ResourceId</span></span>
<span data-ttu-id="ce19e-137">Ressourcenbezeichner von Synapse SQL Pool.</span><span class="sxs-lookup"><span data-stu-id="ce19e-137">Resource identifier of Synapse SQL Pool.</span></span>

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

### <span data-ttu-id="ce19e-138">-RestorePointCreationDate</span><span class="sxs-lookup"><span data-stu-id="ce19e-138">-RestorePointCreationDate</span></span>
<span data-ttu-id="ce19e-139">Name von "Synapse" SQL Erstellungsdatum des Wiederherstellungspunkts.</span><span class="sxs-lookup"><span data-stu-id="ce19e-139">Name of Synapse SQL Restore Point Creation Date .</span></span>

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

### <span data-ttu-id="ce19e-140">-SqlPoolObject</span><span class="sxs-lookup"><span data-stu-id="ce19e-140">-SqlPoolObject</span></span>
<span data-ttu-id="ce19e-141">Sql Pool-Eingabeobjekt, das in der Regel über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="ce19e-141">Sql Pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="ce19e-142">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="ce19e-142">-WorkspaceName</span></span>
<span data-ttu-id="ce19e-143">Name des Synapse-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="ce19e-143">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="ce19e-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ce19e-144">-Confirm</span></span>
<span data-ttu-id="ce19e-145">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ce19e-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ce19e-146">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="ce19e-146">-WhatIf</span></span>
<span data-ttu-id="ce19e-147">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ce19e-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ce19e-148">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ce19e-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ce19e-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce19e-149">CommonParameters</span></span>
<span data-ttu-id="ce19e-150">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ce19e-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce19e-151">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ce19e-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce19e-152">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ce19e-152">INPUTS</span></span>

### <span data-ttu-id="ce19e-153">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="ce19e-153">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="ce19e-154">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="ce19e-154">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

### <span data-ttu-id="ce19e-155">Microsoft.Azure.Commands.Synapse.Models.PSRestorePoint</span><span class="sxs-lookup"><span data-stu-id="ce19e-155">Microsoft.Azure.Commands.Synapse.Models.PSRestorePoint</span></span>

### <span data-ttu-id="ce19e-156">System.String</span><span class="sxs-lookup"><span data-stu-id="ce19e-156">System.String</span></span>

## <span data-ttu-id="ce19e-157">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ce19e-157">OUTPUTS</span></span>

### <span data-ttu-id="ce19e-158">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ce19e-158">System.Boolean</span></span>

## <span data-ttu-id="ce19e-159">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="ce19e-159">NOTES</span></span>

## <span data-ttu-id="ce19e-160">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="ce19e-160">RELATED LINKS</span></span>
