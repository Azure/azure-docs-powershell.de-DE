---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsesqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlDatabase.md
ms.openlocfilehash: 2525792f7696c69a03a926850eaea20267d14fbf
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94010335"
---
# <span data-ttu-id="32fce-101">Remove-AzSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="32fce-101">Remove-AzSynapseSqlDatabase</span></span>

## <span data-ttu-id="32fce-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="32fce-102">SYNOPSIS</span></span>
<span data-ttu-id="32fce-103">Löscht eine Synapse Analytics SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="32fce-103">Deletes a Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="32fce-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="32fce-104">SYNTAX</span></span>

### <span data-ttu-id="32fce-105">DeleteByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="32fce-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseSqlDatabase [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="32fce-106">DeleteByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="32fce-106">DeleteByParentObjectParameterSet</span></span>
```
Remove-AzSynapseSqlDatabase -Name <String> -WorkspaceObject <PSSynapseWorkspace> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="32fce-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="32fce-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzSynapseSqlDatabase -InputObject <PSSynapseSqlDatabase> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="32fce-108">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="32fce-108">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzSynapseSqlDatabase -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="32fce-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="32fce-109">DESCRIPTION</span></span>
<span data-ttu-id="32fce-110">Das Cmdlet **Remove-AzSynapseSqlPool** löscht permanent eine Azure Synapse Analytics SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="32fce-110">The **Remove-AzSynapseSqlPool** cmdlet permanently deletes an Azure Synapse Analytics SQL database.</span></span>


## <span data-ttu-id="32fce-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="32fce-111">EXAMPLES</span></span>

### <span data-ttu-id="32fce-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="32fce-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseSqlDatabase -WorkspaceName ContosoWorkspace -Name ContosoSqlDatabase
```

<span data-ttu-id="32fce-113">Dieser Befehl löscht eine Azure Synapse Analytics SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="32fce-113">This command deletes an Azure Synapse Analytics SQL database.</span></span>

### <span data-ttu-id="32fce-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="32fce-114">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseSqlDatabase -Name ContosoSqlDatabase
```

<span data-ttu-id="32fce-115">Mit diesem Befehl wird eine Azure Synapse Analytics SQL-Datenbank durch Pipeline gelöscht.</span><span class="sxs-lookup"><span data-stu-id="32fce-115">This command deletes an Azure Synapse Analytics SQL database through pipeline.</span></span>

### <span data-ttu-id="32fce-116">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="32fce-116">Example 3</span></span>
```powershell
PS C:\> $database = Get-AzSynapseSqlDatabase -WorkspaceName ContosoWorkspace -Name ContosoSqlDatabase
PS C:\> $database | Remove-AzSynapseSqlDatabase
```

<span data-ttu-id="32fce-117">Mit diesem Befehl wird eine Azure Synapse Analytics SQL-Datenbank durch Pipeline gelöscht.</span><span class="sxs-lookup"><span data-stu-id="32fce-117">This command deletes an Azure Synapse Analytics SQL database through pipeline.</span></span>

### <span data-ttu-id="32fce-118">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="32fce-118">Example 4</span></span>
```powershell
PS C:\> Remove-AzSynapseSqlDatabase -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/sqlDatabases/ContosoSqlDatabase
```

<span data-ttu-id="32fce-119">Mit diesem Befehl wird eine Azure Synapse Analytics SQL-Datenbank mit der angegebenen Ressourcen-ID gelöscht.</span><span class="sxs-lookup"><span data-stu-id="32fce-119">This command deletes an Azure Synapse Analytics SQL database with the specified resource ID.</span></span>

## <span data-ttu-id="32fce-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="32fce-120">PARAMETERS</span></span>

### <span data-ttu-id="32fce-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="32fce-121">-AsJob</span></span>
<span data-ttu-id="32fce-122">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="32fce-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="32fce-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32fce-123">-DefaultProfile</span></span>
<span data-ttu-id="32fce-124">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="32fce-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="32fce-125">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="32fce-125">-InputObject</span></span>
<span data-ttu-id="32fce-126">SQL-Datenbankeingabe Objekt, in der Regel durch die Pipeline übergeben.</span><span class="sxs-lookup"><span data-stu-id="32fce-126">SQL Database input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="32fce-127">-Name</span><span class="sxs-lookup"><span data-stu-id="32fce-127">-Name</span></span>
<span data-ttu-id="32fce-128">Name der Synapse-SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="32fce-128">Name of Synapse SQL Database.</span></span>

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

### <span data-ttu-id="32fce-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="32fce-129">-PassThru</span></span>
<span data-ttu-id="32fce-130">Dieses Cmdlet gibt standardmäßig kein Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="32fce-130">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="32fce-131">Wenn dieser Schalter angegeben wird, wird true zurückgegeben, wenn er erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="32fce-131">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="32fce-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="32fce-132">-ResourceGroupName</span></span>
<span data-ttu-id="32fce-133">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="32fce-133">Resource group name.</span></span>

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

### <span data-ttu-id="32fce-134">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="32fce-134">-ResourceId</span></span>
<span data-ttu-id="32fce-135">Ressourcen-ID der Synapse-SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="32fce-135">Resource identifier of Synapse SQL Database.</span></span>

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

### <span data-ttu-id="32fce-136">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="32fce-136">-WorkspaceName</span></span>
<span data-ttu-id="32fce-137">Name des Synapse-Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="32fce-137">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="32fce-138">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="32fce-138">-WorkspaceObject</span></span>
<span data-ttu-id="32fce-139">Arbeitsbereichs Eingabeobjekt, in der Regel durch die Pipeline übergeben.</span><span class="sxs-lookup"><span data-stu-id="32fce-139">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="32fce-140">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="32fce-140">-Confirm</span></span>
<span data-ttu-id="32fce-141">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="32fce-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="32fce-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="32fce-142">-WhatIf</span></span>
<span data-ttu-id="32fce-143">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="32fce-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="32fce-144">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="32fce-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="32fce-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32fce-145">CommonParameters</span></span>
<span data-ttu-id="32fce-146">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="32fce-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32fce-147">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="32fce-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32fce-148">Eingaben</span><span class="sxs-lookup"><span data-stu-id="32fce-148">INPUTS</span></span>

### <span data-ttu-id="32fce-149">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="32fce-149">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="32fce-150">Microsoft. Azure. Commands. Synapse. Models. PSSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="32fce-150">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlDatabase</span></span>

### <span data-ttu-id="32fce-151">System. String</span><span class="sxs-lookup"><span data-stu-id="32fce-151">System.String</span></span>

## <span data-ttu-id="32fce-152">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="32fce-152">OUTPUTS</span></span>

### <span data-ttu-id="32fce-153">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="32fce-153">System.Boolean</span></span>

## <span data-ttu-id="32fce-154">Notizen</span><span class="sxs-lookup"><span data-stu-id="32fce-154">NOTES</span></span>

## <span data-ttu-id="32fce-155">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="32fce-155">RELATED LINKS</span></span>
