---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/update-azsynapsesqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSqlDatabase.md
ms.openlocfilehash: a939ef485976a746e705de10a4706b03c63f910e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101939096"
---
# <span data-ttu-id="61afc-101">Update-AzSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="61afc-101">Update-AzSynapseSqlDatabase</span></span>

## <span data-ttu-id="61afc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="61afc-102">SYNOPSIS</span></span>
<span data-ttu-id="61afc-103">Aktualisiert eine Synapse Analytics SQL Datenbank.</span><span class="sxs-lookup"><span data-stu-id="61afc-103">Updates a Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="61afc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="61afc-104">SYNTAX</span></span>

### <span data-ttu-id="61afc-105">UpdateByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="61afc-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzSynapseSqlDatabase [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-MaxSizeInBytes <Int64>] [-Tag <Hashtable>] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="61afc-106">UpdateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="61afc-106">UpdateByParentObjectParameterSet</span></span>
```
Update-AzSynapseSqlDatabase -Name <String> [-MaxSizeInBytes <Int64>] -WorkspaceObject <PSSynapseWorkspace>
 [-Tag <Hashtable>] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="61afc-107">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="61afc-107">UpdateByInputObjectParameterSet</span></span>
```
Update-AzSynapseSqlDatabase -InputObject <PSSynapseSqlDatabase> [-Tag <Hashtable>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="61afc-108">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="61afc-108">UpdateByResourceIdParameterSet</span></span>
```
Update-AzSynapseSqlDatabase -ResourceId <String> [-Tag <Hashtable>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="61afc-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="61afc-109">DESCRIPTION</span></span>
<span data-ttu-id="61afc-110">Das **Cmdlet Update-AzSynapseSqlDatabase** aktualisiert eine Azure Synapse Analytics SQL Datenbank.</span><span class="sxs-lookup"><span data-stu-id="61afc-110">The **Update-AzSynapseSqlDatabase** cmdlet updates an Azure Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="61afc-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="61afc-111">EXAMPLES</span></span>

### <span data-ttu-id="61afc-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="61afc-112">Example 1</span></span>
```powershell
PS C:\> Update-AzSynapseSqlDatabase -WorkspaceName ContosoWorkspace -Name ContosoSqlDatabase -Tag @{'key'='value'}
```

<span data-ttu-id="61afc-113">Mit diesem Befehl wird eine Azure Synapse Analytics-SQL aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="61afc-113">This command updates an Azure Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="61afc-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="61afc-114">PARAMETERS</span></span>

### <span data-ttu-id="61afc-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="61afc-115">-AsJob</span></span>
<span data-ttu-id="61afc-116">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="61afc-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="61afc-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61afc-117">-DefaultProfile</span></span>
<span data-ttu-id="61afc-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="61afc-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="61afc-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="61afc-119">-InputObject</span></span>
<span data-ttu-id="61afc-120">SQL Datenbankeingabeobjekt, das normalerweise über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="61afc-120">SQL Database input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="61afc-121">-MaxSizeInBytes</span><span class="sxs-lookup"><span data-stu-id="61afc-121">-MaxSizeInBytes</span></span>
<span data-ttu-id="61afc-122">Gibt die maximale Größe der Datenbank in Bytes an.</span><span class="sxs-lookup"><span data-stu-id="61afc-122">Specifies the maximum size of the database in bytes.</span></span>

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

### <span data-ttu-id="61afc-123">-Name</span><span class="sxs-lookup"><span data-stu-id="61afc-123">-Name</span></span>
<span data-ttu-id="61afc-124">Name von Synapse SQL Datenbank.</span><span class="sxs-lookup"><span data-stu-id="61afc-124">Name of Synapse SQL Database.</span></span>

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

### <span data-ttu-id="61afc-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="61afc-125">-PassThru</span></span>
<span data-ttu-id="61afc-126">Dieses Cmdlet gibt standardmäßig kein -Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="61afc-126">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="61afc-127">Wenn dieser Schalter angegeben ist, gibt er "true" zurück, wenn er erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="61afc-127">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="61afc-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="61afc-128">-ResourceGroupName</span></span>
<span data-ttu-id="61afc-129">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="61afc-129">Resource group name.</span></span>

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

### <span data-ttu-id="61afc-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="61afc-130">-ResourceId</span></span>
<span data-ttu-id="61afc-131">Ressourcenbezeichner von Synapse SQL Datenbank.</span><span class="sxs-lookup"><span data-stu-id="61afc-131">Resource identifier of Synapse SQL Database.</span></span>

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

### <span data-ttu-id="61afc-132">-Tag</span><span class="sxs-lookup"><span data-stu-id="61afc-132">-Tag</span></span>
<span data-ttu-id="61afc-133">Eine Zeichenfolge, ein Zeichenfolgenwörterbuch mit Tags, die der Ressource zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="61afc-133">A string,string dictionary of tags associated with the resource.</span></span>

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

### <span data-ttu-id="61afc-134">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="61afc-134">-WorkspaceName</span></span>
<span data-ttu-id="61afc-135">Name des Synapse-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="61afc-135">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="61afc-136">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="61afc-136">-WorkspaceObject</span></span>
<span data-ttu-id="61afc-137">Arbeitsbereichseingabeobjekt, das in der Regel über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="61afc-137">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="61afc-138">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="61afc-138">-Confirm</span></span>
<span data-ttu-id="61afc-139">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="61afc-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="61afc-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="61afc-140">-WhatIf</span></span>
<span data-ttu-id="61afc-141">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="61afc-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="61afc-142">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="61afc-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="61afc-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61afc-143">CommonParameters</span></span>
<span data-ttu-id="61afc-144">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61afc-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61afc-145">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="61afc-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61afc-146">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="61afc-146">INPUTS</span></span>

### <span data-ttu-id="61afc-147">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="61afc-147">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="61afc-148">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="61afc-148">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlDatabase</span></span>

## <span data-ttu-id="61afc-149">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="61afc-149">OUTPUTS</span></span>

### <span data-ttu-id="61afc-150">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="61afc-150">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlDatabase</span></span>

## <span data-ttu-id="61afc-151">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="61afc-151">NOTES</span></span>

## <span data-ttu-id="61afc-152">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="61afc-152">RELATED LINKS</span></span>
