---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/set-azsynapsesqlpoolsensitivityclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseSqlPoolSensitivityClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseSqlPoolSensitivityClassification.md
ms.openlocfilehash: 2eec7ea6f89bea726cdbee483162ec455e5722aa
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101939219"
---
# <span data-ttu-id="b16b8-101">Set-AzSynapseSqlPoolSensitivityClassification</span><span class="sxs-lookup"><span data-stu-id="b16b8-101">Set-AzSynapseSqlPoolSensitivityClassification</span></span>

## <span data-ttu-id="b16b8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b16b8-102">SYNOPSIS</span></span>
<span data-ttu-id="b16b8-103">Legt die Informationstypen und Vertraulichkeitsbeschriftungen von Spalten im SQL fest.</span><span class="sxs-lookup"><span data-stu-id="b16b8-103">Sets the information types and sensitivity labels of columns in the SQL pool.</span></span>

## <span data-ttu-id="b16b8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b16b8-104">SYNTAX</span></span>

### <span data-ttu-id="b16b8-105">ClassificationObjectParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="b16b8-105">ClassificationObjectParameterSet (Default)</span></span>
```
Set-AzSynapseSqlPoolSensitivityClassification -ClassificationObject <SqlPoolSensitivityClassificationModel>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b16b8-106">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="b16b8-106">ColumnParameterSet</span></span>
```
Set-AzSynapseSqlPoolSensitivityClassification [-SensitivityLabel <String>] [-InformationType <String>]
 [-ResourceGroupName] <String> [-WorkspaceName] <String> [-SqlPoolName] <String> -SchemaName <String>
 -TableName <String> -ColumnName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b16b8-107">SqlPoolObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="b16b8-107">SqlPoolObjectColumnParameterSet</span></span>
```
Set-AzSynapseSqlPoolSensitivityClassification [-SensitivityLabel <String>] [-InformationType <String>]
 -SqlPoolObject <PSSynapseSqlPool> -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b16b8-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b16b8-108">DESCRIPTION</span></span>
<span data-ttu-id="b16b8-109">Das Set-AzSynapseSqlPoolSensitivityClassification-Cmdlet legt die Informationstypen und Vertraulichkeitsbeschriftungen von Spalten im SQL fest.</span><span class="sxs-lookup"><span data-stu-id="b16b8-109">The Set-AzSynapseSqlPoolSensitivityClassification cmdlet sets the information types and sensitivity labels of columns in the SQL pool.</span></span>

## <span data-ttu-id="b16b8-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b16b8-110">EXAMPLES</span></span>

### <span data-ttu-id="b16b8-111">Beispiel 1: Festlegen von Informationstyp und Vertraulichkeitsbeschriftung einer Spalte in einem Azure Synapse SQL Pool.</span><span class="sxs-lookup"><span data-stu-id="b16b8-111">Example 1: Set information type and sensitivity label of a column in an Azure Synapse SQL pool.</span></span>
```powershell
PS C:\> Set-AzSynapseSqlPoolSensitivityClassification -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -SqlPoolName ContosoSqlPool -SchemaName schema -TableName table -ColumnName column -InformationType informationType -SensitivityLabel label
```

### <span data-ttu-id="b16b8-112">Beispiel 2: Festlegen empfohlener Informationstypen und Vertraulichkeitsbeschriftungen von Spalten in einem Azure Synapse SQL Pool.</span><span class="sxs-lookup"><span data-stu-id="b16b8-112">Example 2: Set recommended information types and sensitivity labels of columns in an Azure Synapse SQL pool.</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPoolSensitivityRecommendation -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -Name ContosoSqlPool | Set-AzSynapseSqlPoolSensitivityClassification
```

### <span data-ttu-id="b16b8-113">Beispiel 3: Festlegen von Informationstyp und Vertraulichkeitsbeschriftung einer Spalte in einem Azure Synapse-SQL mithilfe von Piping.</span><span class="sxs-lookup"><span data-stu-id="b16b8-113">Example 3: Set information type and sensitivity label of a column in an Azure Synapse SQL pool, using piping.</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPool -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -Name ContosoSqlPool | Set-AzSynapseSqlPoolSensitivityClassification  -SchemaName schema -TableName table -ColumnName column -InformationType informationType -SensitivityLabel label
```

## <span data-ttu-id="b16b8-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="b16b8-114">PARAMETERS</span></span>

### <span data-ttu-id="b16b8-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b16b8-115">-AsJob</span></span>
<span data-ttu-id="b16b8-116">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="b16b8-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b16b8-117">-ClassificationObject</span><span class="sxs-lookup"><span data-stu-id="b16b8-117">-ClassificationObject</span></span>
<span data-ttu-id="b16b8-118">Ein Objekt, das eine SQL Pool-Vertraulichkeitsklassifizierung darstellt.</span><span class="sxs-lookup"><span data-stu-id="b16b8-118">An object representing a SQL Pool Sensitivity Classification.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.DataClassification.SqlPoolSensitivityClassificationModel
Parameter Sets: ClassificationObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b16b8-119">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="b16b8-119">-ColumnName</span></span>
<span data-ttu-id="b16b8-120">Name der Spalte.</span><span class="sxs-lookup"><span data-stu-id="b16b8-120">Name of column.</span></span>

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

### <span data-ttu-id="b16b8-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b16b8-121">-DefaultProfile</span></span>
<span data-ttu-id="b16b8-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b16b8-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b16b8-123">-InformationType</span><span class="sxs-lookup"><span data-stu-id="b16b8-123">-InformationType</span></span>
<span data-ttu-id="b16b8-124">Ein Name, der den Informationstyp der in der Spalte gespeicherten Daten beschreibt.</span><span class="sxs-lookup"><span data-stu-id="b16b8-124">A name that describes the information type of the data stored in the column.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet, SqlPoolObjectColumnParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b16b8-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b16b8-125">-PassThru</span></span>
<span data-ttu-id="b16b8-126">Dieses Cmdlet gibt standardmäßig kein -Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="b16b8-126">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="b16b8-127">Wenn dieser Schalter angegeben ist, gibt er "true" zurück, wenn er erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="b16b8-127">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="b16b8-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b16b8-128">-ResourceGroupName</span></span>
<span data-ttu-id="b16b8-129">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="b16b8-129">Resource group name.</span></span>

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

### <span data-ttu-id="b16b8-130">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="b16b8-130">-SchemaName</span></span>
<span data-ttu-id="b16b8-131">Name des Schemas.</span><span class="sxs-lookup"><span data-stu-id="b16b8-131">Name of schema.</span></span>

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

### <span data-ttu-id="b16b8-132">-SensitivityLabel</span><span class="sxs-lookup"><span data-stu-id="b16b8-132">-SensitivityLabel</span></span>
<span data-ttu-id="b16b8-133">Ein Name, der die Vertraulichkeit der in der Spalte gespeicherten Daten beschreibt.</span><span class="sxs-lookup"><span data-stu-id="b16b8-133">A name that describes the sensitivity of the data stored in the column.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet, SqlPoolObjectColumnParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b16b8-134">-SqlPoolName</span><span class="sxs-lookup"><span data-stu-id="b16b8-134">-SqlPoolName</span></span>
<span data-ttu-id="b16b8-135">Name des Synapse SQL Pools.</span><span class="sxs-lookup"><span data-stu-id="b16b8-135">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="b16b8-136">-SqlPoolObject</span><span class="sxs-lookup"><span data-stu-id="b16b8-136">-SqlPoolObject</span></span>
<span data-ttu-id="b16b8-137">SQL -Pooleingabeobjekt, das in der Regel über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="b16b8-137">SQL pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="b16b8-138">-TableName</span><span class="sxs-lookup"><span data-stu-id="b16b8-138">-TableName</span></span>
<span data-ttu-id="b16b8-139">Name der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="b16b8-139">Name of table.</span></span>

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

### <span data-ttu-id="b16b8-140">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="b16b8-140">-WorkspaceName</span></span>
<span data-ttu-id="b16b8-141">Name des Synapse-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="b16b8-141">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="b16b8-142">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b16b8-142">-Confirm</span></span>
<span data-ttu-id="b16b8-143">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b16b8-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b16b8-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b16b8-144">-WhatIf</span></span>
<span data-ttu-id="b16b8-145">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b16b8-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b16b8-146">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b16b8-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b16b8-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b16b8-147">CommonParameters</span></span>
<span data-ttu-id="b16b8-148">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b16b8-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b16b8-149">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b16b8-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b16b8-150">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b16b8-150">INPUTS</span></span>

### <span data-ttu-id="b16b8-151">System.String</span><span class="sxs-lookup"><span data-stu-id="b16b8-151">System.String</span></span>

### <span data-ttu-id="b16b8-152">Microsoft.Azure.Commands.Synapse.Models.DataClassification.SqlPoolSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="b16b8-152">Microsoft.Azure.Commands.Synapse.Models.DataClassification.SqlPoolSensitivityClassificationModel</span></span>

### <span data-ttu-id="b16b8-153">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="b16b8-153">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="b16b8-154">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b16b8-154">OUTPUTS</span></span>

### <span data-ttu-id="b16b8-155">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b16b8-155">System.Boolean</span></span>

## <span data-ttu-id="b16b8-156">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="b16b8-156">NOTES</span></span>

## <span data-ttu-id="b16b8-157">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="b16b8-157">RELATED LINKS</span></span>
