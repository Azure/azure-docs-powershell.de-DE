---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/enable-azsynapsesqlpoolsensitivityrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Enable-AzSynapseSqlPoolSensitivityRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Enable-AzSynapseSqlPoolSensitivityRecommendation.md
ms.openlocfilehash: 52abddf2db18a6e70a1b876629feff0761bed014
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98460036"
---
# <span data-ttu-id="3a19d-101">Enable-AzSynapseSqlPoolSensitivityRecommendation</span><span class="sxs-lookup"><span data-stu-id="3a19d-101">Enable-AzSynapseSqlPoolSensitivityRecommendation</span></span>

## <span data-ttu-id="3a19d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3a19d-102">SYNOPSIS</span></span>
<span data-ttu-id="3a19d-103">Aktiviert Vertraulichkeitsempfehlungen für Spalten (Empfehlungen sind standardmäßig für alle Spalten aktiviert) im SQL Pool.</span><span class="sxs-lookup"><span data-stu-id="3a19d-103">Enables sensitivity recommendations on columns (recommendations are enabled by default on all columns) in the SQL pool.</span></span>

## <span data-ttu-id="3a19d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3a19d-104">SYNTAX</span></span>

### <span data-ttu-id="3a19d-105">InputObjectParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="3a19d-105">InputObjectParameterSet (Default)</span></span>
```
Enable-AzSynapseSqlPoolSensitivityRecommendation -InputObject <SqlPoolSensitivityClassificationModel>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3a19d-106">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="3a19d-106">ColumnParameterSet</span></span>
```
Enable-AzSynapseSqlPoolSensitivityRecommendation [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SqlPoolName] <String> -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3a19d-107">SqlPoolObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="3a19d-107">SqlPoolObjectColumnParameterSet</span></span>
```
Enable-AzSynapseSqlPoolSensitivityRecommendation -SqlPoolObject <PSSynapseSqlPool> -SchemaName <String>
 -TableName <String> -ColumnName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3a19d-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3a19d-108">DESCRIPTION</span></span>
<span data-ttu-id="3a19d-109">Das Enable-AzSynapseSqlPoolSensitivityRecommendation ermöglicht Vertraulichkeitsempfehlungen für Spalten im SQL Pool.</span><span class="sxs-lookup"><span data-stu-id="3a19d-109">The Enable-AzSynapseSqlPoolSensitivityRecommendation cmdlet enables sensitivity recommendations on columns in the SQL pool.</span></span>

## <span data-ttu-id="3a19d-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="3a19d-110">EXAMPLES</span></span>

### <span data-ttu-id="3a19d-111">Beispiel 1: Aktivieren von Vertraulichkeitsempfehlungen für eine bestimmte Spalte in einem Azure Synapse SQL Pool.</span><span class="sxs-lookup"><span data-stu-id="3a19d-111">Example 1: Enable sensitivity recommendations on a given column in an Azure Synapse SQL pool.</span></span>
```powershell
PS C:\> Enable-AzSynapseSqlPoolSensitivityRecommendation -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -SqlPoolName ContosoSqlPool -SchemaName schema -TableName table -ColumnName column
```

### <span data-ttu-id="3a19d-112">Beispiel 2: Aktivieren von Vertraulichkeitsempfehlungen für eine bestimmte Spalte von Azure Synapse SQL mit Piping.</span><span class="sxs-lookup"><span data-stu-id="3a19d-112">Example 2: Enable sensitivity recommendations on a given column Azure Synapse SQL pool using Piping.</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPool -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -Name ContosoSqlPool | Enable-AzSynapseSqlPoolSensitivityRecommendation -SchemaName schema -TableName table -ColumnName column
```

## <span data-ttu-id="3a19d-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3a19d-113">PARAMETERS</span></span>

### <span data-ttu-id="3a19d-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3a19d-114">-AsJob</span></span>
<span data-ttu-id="3a19d-115">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="3a19d-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3a19d-116">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="3a19d-116">-ColumnName</span></span>
<span data-ttu-id="3a19d-117">Name der Spalte.</span><span class="sxs-lookup"><span data-stu-id="3a19d-117">Name of column.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet, SqlPoolObjectColumnParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a19d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a19d-118">-DefaultProfile</span></span>
<span data-ttu-id="3a19d-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3a19d-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3a19d-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3a19d-120">-InputObject</span></span>
<span data-ttu-id="3a19d-121">Ein Objekt, das eine SQL A0 darstellt.</span><span class="sxs-lookup"><span data-stu-id="3a19d-121">An object representing a SQL Pool Sensitivity Classification.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.DataClassification.SqlPoolSensitivityClassificationModel
Parameter Sets: InputObjectParameterSet
Aliases: ClassificationObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3a19d-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3a19d-122">-PassThru</span></span>
<span data-ttu-id="3a19d-123">Dieses Cmdlet gibt standardmäßig kein Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="3a19d-123">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="3a19d-124">Wenn dieser Schalter angegeben ist, wird "true" zurückgegeben, wenn er erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="3a19d-124">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="3a19d-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a19d-125">-ResourceGroupName</span></span>
<span data-ttu-id="3a19d-126">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="3a19d-126">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a19d-127">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="3a19d-127">-SchemaName</span></span>
<span data-ttu-id="3a19d-128">Name des Schemas.</span><span class="sxs-lookup"><span data-stu-id="3a19d-128">Name of schema.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet, SqlPoolObjectColumnParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a19d-129">-SqlPoolName</span><span class="sxs-lookup"><span data-stu-id="3a19d-129">-SqlPoolName</span></span>
<span data-ttu-id="3a19d-130">Name des Synapse SQL Pools.</span><span class="sxs-lookup"><span data-stu-id="3a19d-130">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a19d-131">-SqlPoolObject</span><span class="sxs-lookup"><span data-stu-id="3a19d-131">-SqlPoolObject</span></span>
<span data-ttu-id="3a19d-132">SQL pool-Eingabeobjekts, das in der Regel über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="3a19d-132">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: SqlPoolObjectColumnParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3a19d-133">-TableName</span><span class="sxs-lookup"><span data-stu-id="3a19d-133">-TableName</span></span>
<span data-ttu-id="3a19d-134">Name der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="3a19d-134">Name of table.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet, SqlPoolObjectColumnParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a19d-135">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="3a19d-135">-WorkspaceName</span></span>
<span data-ttu-id="3a19d-136">Name des Synapse-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="3a19d-136">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a19d-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3a19d-137">-Confirm</span></span>
<span data-ttu-id="3a19d-138">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3a19d-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3a19d-139">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="3a19d-139">-WhatIf</span></span>
<span data-ttu-id="3a19d-140">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3a19d-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3a19d-141">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3a19d-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3a19d-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a19d-142">CommonParameters</span></span>
<span data-ttu-id="3a19d-143">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3a19d-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a19d-144">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3a19d-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a19d-145">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="3a19d-145">INPUTS</span></span>

### <span data-ttu-id="3a19d-146">Microsoft.Azure.Commands.Synapse.Models.DataClassification.SqlPoolSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="3a19d-146">Microsoft.Azure.Commands.Synapse.Models.DataClassification.SqlPoolSensitivityClassificationModel</span></span>

### <span data-ttu-id="3a19d-147">System.String</span><span class="sxs-lookup"><span data-stu-id="3a19d-147">System.String</span></span>

### <span data-ttu-id="3a19d-148">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="3a19d-148">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="3a19d-149">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="3a19d-149">OUTPUTS</span></span>

### <span data-ttu-id="3a19d-150">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="3a19d-150">System.Boolean</span></span>

## <span data-ttu-id="3a19d-151">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="3a19d-151">NOTES</span></span>

## <span data-ttu-id="3a19d-152">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="3a19d-152">RELATED LINKS</span></span>
