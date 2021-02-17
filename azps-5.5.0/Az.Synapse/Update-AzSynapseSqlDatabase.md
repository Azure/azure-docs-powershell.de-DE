---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/update-azsynapsesqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSqlDatabase.md
ms.openlocfilehash: 8f555b18605156aa3394ac02539b7b464feb3ab9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100149881"
---
# <span data-ttu-id="d24f1-101">Update-AzSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="d24f1-101">Update-AzSynapseSqlDatabase</span></span>

## <span data-ttu-id="d24f1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d24f1-102">SYNOPSIS</span></span>
<span data-ttu-id="d24f1-103">Aktualisiert eine Synapse Analytics SQL Datenbank.</span><span class="sxs-lookup"><span data-stu-id="d24f1-103">Updates a Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="d24f1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d24f1-104">SYNTAX</span></span>

### <span data-ttu-id="d24f1-105">UpdateByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="d24f1-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzSynapseSqlDatabase [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-MaxSizeInBytes <Int64>] [-Tag <Hashtable>] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d24f1-106">UpdateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d24f1-106">UpdateByParentObjectParameterSet</span></span>
```
Update-AzSynapseSqlDatabase -Name <String> [-MaxSizeInBytes <Int64>] -WorkspaceObject <PSSynapseWorkspace>
 [-Tag <Hashtable>] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d24f1-107">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d24f1-107">UpdateByInputObjectParameterSet</span></span>
```
Update-AzSynapseSqlDatabase -InputObject <PSSynapseSqlDatabase> [-Tag <Hashtable>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d24f1-108">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d24f1-108">UpdateByResourceIdParameterSet</span></span>
```
Update-AzSynapseSqlDatabase -ResourceId <String> [-Tag <Hashtable>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d24f1-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d24f1-109">DESCRIPTION</span></span>
<span data-ttu-id="d24f1-110">Das **Cmdlet "Update-AzSynapseSqlDatabase"** aktualisiert eine Azure Synapse Analytics SQL Datenbank.</span><span class="sxs-lookup"><span data-stu-id="d24f1-110">The **Update-AzSynapseSqlDatabase** cmdlet updates an Azure Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="d24f1-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d24f1-111">EXAMPLES</span></span>

### <span data-ttu-id="d24f1-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d24f1-112">Example 1</span></span>
```powershell
PS C:\> Update-AzSynapseSqlDatabase -WorkspaceName ContosoWorkspace -Name ContosoSqlDatabase -Tag @{'key'='value'}
```

<span data-ttu-id="d24f1-113">Mit diesem Befehl wird eine Azure Synapse Analytics SQL aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="d24f1-113">This command updates an Azure Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="d24f1-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d24f1-114">PARAMETERS</span></span>

### <span data-ttu-id="d24f1-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d24f1-115">-AsJob</span></span>
<span data-ttu-id="d24f1-116">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="d24f1-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d24f1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d24f1-117">-DefaultProfile</span></span>
<span data-ttu-id="d24f1-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d24f1-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d24f1-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d24f1-119">-InputObject</span></span>
<span data-ttu-id="d24f1-120">SQL Datenbankeingabeobjekts, das in der Regel über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="d24f1-120">SQL Database input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlDatabase
Parameter Sets: UpdateByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d24f1-121">-MaxSizeInBytes</span><span class="sxs-lookup"><span data-stu-id="d24f1-121">-MaxSizeInBytes</span></span>
<span data-ttu-id="d24f1-122">Gibt die maximale Größe der Datenbank in Bytes an.</span><span class="sxs-lookup"><span data-stu-id="d24f1-122">Specifies the maximum size of the database in bytes.</span></span>

```yaml
Type: System.Int64
Parameter Sets: UpdateByNameParameterSet, UpdateByParentObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d24f1-123">-Name</span><span class="sxs-lookup"><span data-stu-id="d24f1-123">-Name</span></span>
<span data-ttu-id="d24f1-124">Name der Datenbank von Synapse SQL Datenbank.</span><span class="sxs-lookup"><span data-stu-id="d24f1-124">Name of Synapse SQL Database.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet, UpdateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d24f1-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d24f1-125">-PassThru</span></span>
<span data-ttu-id="d24f1-126">Dieses Cmdlet gibt standardmäßig kein Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="d24f1-126">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="d24f1-127">Wenn dieser Schalter angegeben ist, wird "true" zurückgegeben, wenn er erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="d24f1-127">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="d24f1-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d24f1-128">-ResourceGroupName</span></span>
<span data-ttu-id="d24f1-129">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="d24f1-129">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d24f1-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d24f1-130">-ResourceId</span></span>
<span data-ttu-id="d24f1-131">Ressourcenbezeichner von Synapse SQL Datenbank.</span><span class="sxs-lookup"><span data-stu-id="d24f1-131">Resource identifier of Synapse SQL Database.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d24f1-132">-Tag</span><span class="sxs-lookup"><span data-stu-id="d24f1-132">-Tag</span></span>
<span data-ttu-id="d24f1-133">Ein Zeichenfolgenverzeichnis mit Tags, die der Ressource zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="d24f1-133">A string,string dictionary of tags associated with the resource.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d24f1-134">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="d24f1-134">-WorkspaceName</span></span>
<span data-ttu-id="d24f1-135">Name des Synapse-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="d24f1-135">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d24f1-136">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="d24f1-136">-WorkspaceObject</span></span>
<span data-ttu-id="d24f1-137">Arbeitsbereichseingabeobjekts, das in der Regel über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="d24f1-137">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: UpdateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d24f1-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d24f1-138">-Confirm</span></span>
<span data-ttu-id="d24f1-139">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d24f1-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d24f1-140">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="d24f1-140">-WhatIf</span></span>
<span data-ttu-id="d24f1-141">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d24f1-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d24f1-142">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d24f1-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d24f1-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d24f1-143">CommonParameters</span></span>
<span data-ttu-id="d24f1-144">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d24f1-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d24f1-145">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d24f1-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d24f1-146">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d24f1-146">INPUTS</span></span>

### <span data-ttu-id="d24f1-147">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="d24f1-147">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="d24f1-148">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="d24f1-148">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlDatabase</span></span>

## <span data-ttu-id="d24f1-149">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d24f1-149">OUTPUTS</span></span>

### <span data-ttu-id="d24f1-150">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="d24f1-150">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlDatabase</span></span>

## <span data-ttu-id="d24f1-151">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="d24f1-151">NOTES</span></span>

## <span data-ttu-id="d24f1-152">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="d24f1-152">RELATED LINKS</span></span>
