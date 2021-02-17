---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/disable-azsynapsesqlpoolsensitivityrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Disable-AzSynapseSqlPoolSensitivityRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Disable-AzSynapseSqlPoolSensitivityRecommendation.md
ms.openlocfilehash: 72ee99f3d62470c4a3a62719006152a5f52cd8d1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100164644"
---
# <span data-ttu-id="746e9-101">Disable-AzSynapseSqlPoolSensitivityRecommendation</span><span class="sxs-lookup"><span data-stu-id="746e9-101">Disable-AzSynapseSqlPoolSensitivityRecommendation</span></span>

## <span data-ttu-id="746e9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="746e9-102">SYNOPSIS</span></span>
<span data-ttu-id="746e9-103">Deaktiviert (schließt) Vertraulichkeitsempfehlungen für Spalten im SQL Pool.</span><span class="sxs-lookup"><span data-stu-id="746e9-103">Disables (dismisses) sensitivity recommendations on columns in the SQL pool.</span></span>

## <span data-ttu-id="746e9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="746e9-104">SYNTAX</span></span>

### <span data-ttu-id="746e9-105">InputObjectParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="746e9-105">InputObjectParameterSet (Default)</span></span>
```
Disable-AzSynapseSqlPoolSensitivityRecommendation -InputObject <SqlPoolSensitivityClassificationModel>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="746e9-106">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="746e9-106">ColumnParameterSet</span></span>
```
Disable-AzSynapseSqlPoolSensitivityRecommendation [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SqlPoolName] <String> -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="746e9-107">SqlPoolObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="746e9-107">SqlPoolObjectColumnParameterSet</span></span>
```
Disable-AzSynapseSqlPoolSensitivityRecommendation -SqlPoolObject <PSSynapseSqlPool> -SchemaName <String>
 -TableName <String> -ColumnName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="746e9-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="746e9-108">DESCRIPTION</span></span>
<span data-ttu-id="746e9-109">Das Disable-AzSynapseSqlPoolSensitivityRecommendation-Cmdlet deaktiviert (schließt) Vertraulichkeitsempfehlungen für Spalten im SQL Pool.</span><span class="sxs-lookup"><span data-stu-id="746e9-109">The Disable-AzSynapseSqlPoolSensitivityRecommendation cmdlet disables (dismisses) sensitivity recommendations on columns in the SQL pool.</span></span>

## <span data-ttu-id="746e9-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="746e9-110">EXAMPLES</span></span>

### <span data-ttu-id="746e9-111">Beispiel 1: Deaktivieren Sie Vertraulichkeitsempfehlungen für eine bestimmte Spalte in einem Azure Synapse SQL-Pool.</span><span class="sxs-lookup"><span data-stu-id="746e9-111">Example 1: Disable sensitivity recommendations on a given column in an Azure Synapse SQL pool.</span></span>
```powershell
PS C:\> Disable-AzSynapseSqlPoolSensitivityRecommendation -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -SqlPoolName ContosoSqlPool -SchemaName schema -TableName table -ColumnName column
```

### <span data-ttu-id="746e9-112">Beispiel 2: Deaktivieren Sie Vertraulichkeitsempfehlungen für Spalten, die Vertraulichkeitsempfehlungen in einem Azure Synapse SQL mit Piping enthalten.</span><span class="sxs-lookup"><span data-stu-id="746e9-112">Example 2: Disable sensitivity recommendations on columns which have sensitivity recommendations in an Azure Synapse SQL pool using Piping.</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPoolSensitivityRecommendation -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -SqlPoolName ContosoSqlPool | Disable-AzSynapseSqlPoolSensitivityRecommendation
```

### <span data-ttu-id="746e9-113">Beispiel 3: Deaktivieren Von Vertraulichkeitsempfehlungen für eine bestimmte Spalte in einem Azure Synapse SQL mithilfe von Piping.</span><span class="sxs-lookup"><span data-stu-id="746e9-113">Example 3: Disable sensitivity recommendations on a given column in an Azure Synapse SQL pool using Piping.</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPool -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -Name ContosoSqlPool | Disable-AzSynapseSqlPoolSensitivityRecommendation -SchemaName schema -TableName table -ColumnName column
```

## <span data-ttu-id="746e9-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="746e9-114">PARAMETERS</span></span>

### <span data-ttu-id="746e9-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="746e9-115">-AsJob</span></span>
<span data-ttu-id="746e9-116">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="746e9-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="746e9-117">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="746e9-117">-ColumnName</span></span>
<span data-ttu-id="746e9-118">Name der Spalte.</span><span class="sxs-lookup"><span data-stu-id="746e9-118">Name of column.</span></span>

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

### <span data-ttu-id="746e9-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="746e9-119">-DefaultProfile</span></span>
<span data-ttu-id="746e9-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="746e9-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="746e9-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="746e9-121">-InputObject</span></span>
<span data-ttu-id="746e9-122">Ein Objekt, das eine SQL A0 darstellt.</span><span class="sxs-lookup"><span data-stu-id="746e9-122">An object representing a SQL Pool Sensitivity Classification.</span></span>

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

### <span data-ttu-id="746e9-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="746e9-123">-PassThru</span></span>
<span data-ttu-id="746e9-124">Dieses Cmdlet gibt standardmäßig kein Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="746e9-124">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="746e9-125">Wenn dieser Schalter angegeben ist, wird "true" zurückgegeben, wenn er erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="746e9-125">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="746e9-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="746e9-126">-ResourceGroupName</span></span>
<span data-ttu-id="746e9-127">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="746e9-127">Resource group name.</span></span>

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

### <span data-ttu-id="746e9-128">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="746e9-128">-SchemaName</span></span>
<span data-ttu-id="746e9-129">Name des Schemas.</span><span class="sxs-lookup"><span data-stu-id="746e9-129">Name of schema.</span></span>

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

### <span data-ttu-id="746e9-130">-SqlPoolName</span><span class="sxs-lookup"><span data-stu-id="746e9-130">-SqlPoolName</span></span>
<span data-ttu-id="746e9-131">Name des Synapse SQL Pools.</span><span class="sxs-lookup"><span data-stu-id="746e9-131">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="746e9-132">-SqlPoolObject</span><span class="sxs-lookup"><span data-stu-id="746e9-132">-SqlPoolObject</span></span>
<span data-ttu-id="746e9-133">SQL pool-Eingabeobjekts, das in der Regel über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="746e9-133">SQL pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="746e9-134">-TableName</span><span class="sxs-lookup"><span data-stu-id="746e9-134">-TableName</span></span>
<span data-ttu-id="746e9-135">Name der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="746e9-135">Name of table.</span></span>

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

### <span data-ttu-id="746e9-136">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="746e9-136">-WorkspaceName</span></span>
<span data-ttu-id="746e9-137">Name des Synapse-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="746e9-137">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="746e9-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="746e9-138">-Confirm</span></span>
<span data-ttu-id="746e9-139">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="746e9-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="746e9-140">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="746e9-140">-WhatIf</span></span>
<span data-ttu-id="746e9-141">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="746e9-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="746e9-142">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="746e9-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="746e9-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="746e9-143">CommonParameters</span></span>
<span data-ttu-id="746e9-144">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="746e9-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="746e9-145">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="746e9-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="746e9-146">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="746e9-146">INPUTS</span></span>

### <span data-ttu-id="746e9-147">Microsoft.Azure.Commands.Synapse.Models.DataClassification.SqlPoolSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="746e9-147">Microsoft.Azure.Commands.Synapse.Models.DataClassification.SqlPoolSensitivityClassificationModel</span></span>

### <span data-ttu-id="746e9-148">System.String</span><span class="sxs-lookup"><span data-stu-id="746e9-148">System.String</span></span>

### <span data-ttu-id="746e9-149">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="746e9-149">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="746e9-150">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="746e9-150">OUTPUTS</span></span>

### <span data-ttu-id="746e9-151">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="746e9-151">System.Boolean</span></span>

## <span data-ttu-id="746e9-152">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="746e9-152">NOTES</span></span>

## <span data-ttu-id="746e9-153">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="746e9-153">RELATED LINKS</span></span>
