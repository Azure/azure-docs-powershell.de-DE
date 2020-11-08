---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/update-azsynapsesqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSqlDatabase.md
ms.openlocfilehash: 8f555b18605156aa3394ac02539b7b464feb3ab9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94176365"
---
# <span data-ttu-id="cfbcf-101">Update-AzSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="cfbcf-101">Update-AzSynapseSqlDatabase</span></span>

## <span data-ttu-id="cfbcf-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="cfbcf-102">SYNOPSIS</span></span>
<span data-ttu-id="cfbcf-103">Aktualisiert eine Synapse Analytics SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="cfbcf-103">Updates a Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="cfbcf-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="cfbcf-104">SYNTAX</span></span>

### <span data-ttu-id="cfbcf-105">UpdateByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="cfbcf-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzSynapseSqlDatabase [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-MaxSizeInBytes <Int64>] [-Tag <Hashtable>] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cfbcf-106">UpdateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cfbcf-106">UpdateByParentObjectParameterSet</span></span>
```
Update-AzSynapseSqlDatabase -Name <String> [-MaxSizeInBytes <Int64>] -WorkspaceObject <PSSynapseWorkspace>
 [-Tag <Hashtable>] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cfbcf-107">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cfbcf-107">UpdateByInputObjectParameterSet</span></span>
```
Update-AzSynapseSqlDatabase -InputObject <PSSynapseSqlDatabase> [-Tag <Hashtable>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cfbcf-108">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cfbcf-108">UpdateByResourceIdParameterSet</span></span>
```
Update-AzSynapseSqlDatabase -ResourceId <String> [-Tag <Hashtable>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cfbcf-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cfbcf-109">DESCRIPTION</span></span>
<span data-ttu-id="cfbcf-110">Das Cmdlet **Update-AzSynapseSqlDatabase** aktualisiert eine Azure Synapse Analytics SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="cfbcf-110">The **Update-AzSynapseSqlDatabase** cmdlet updates an Azure Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="cfbcf-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="cfbcf-111">EXAMPLES</span></span>

### <span data-ttu-id="cfbcf-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="cfbcf-112">Example 1</span></span>
```powershell
PS C:\> Update-AzSynapseSqlDatabase -WorkspaceName ContosoWorkspace -Name ContosoSqlDatabase -Tag @{'key'='value'}
```

<span data-ttu-id="cfbcf-113">Dieser Befehl aktualisiert eine Azure Synapse Analytics SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="cfbcf-113">This command updates an Azure Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="cfbcf-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="cfbcf-114">PARAMETERS</span></span>

### <span data-ttu-id="cfbcf-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cfbcf-115">-AsJob</span></span>
<span data-ttu-id="cfbcf-116">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="cfbcf-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cfbcf-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cfbcf-117">-DefaultProfile</span></span>
<span data-ttu-id="cfbcf-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="cfbcf-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cfbcf-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="cfbcf-119">-InputObject</span></span>
<span data-ttu-id="cfbcf-120">SQL-Datenbankeingabe Objekt, in der Regel durch die Pipeline übergeben.</span><span class="sxs-lookup"><span data-stu-id="cfbcf-120">SQL Database input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="cfbcf-121">-MaxSizeInBytes</span><span class="sxs-lookup"><span data-stu-id="cfbcf-121">-MaxSizeInBytes</span></span>
<span data-ttu-id="cfbcf-122">Gibt die maximale Größe der Datenbank in Bytes an.</span><span class="sxs-lookup"><span data-stu-id="cfbcf-122">Specifies the maximum size of the database in bytes.</span></span>

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

### <span data-ttu-id="cfbcf-123">-Name</span><span class="sxs-lookup"><span data-stu-id="cfbcf-123">-Name</span></span>
<span data-ttu-id="cfbcf-124">Name der Synapse-SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="cfbcf-124">Name of Synapse SQL Database.</span></span>

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

### <span data-ttu-id="cfbcf-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cfbcf-125">-PassThru</span></span>
<span data-ttu-id="cfbcf-126">Dieses Cmdlet gibt standardmäßig kein Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="cfbcf-126">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="cfbcf-127">Wenn dieser Schalter angegeben wird, wird true zurückgegeben, wenn er erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="cfbcf-127">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="cfbcf-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cfbcf-128">-ResourceGroupName</span></span>
<span data-ttu-id="cfbcf-129">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="cfbcf-129">Resource group name.</span></span>

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

### <span data-ttu-id="cfbcf-130">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="cfbcf-130">-ResourceId</span></span>
<span data-ttu-id="cfbcf-131">Ressourcen-ID der Synapse-SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="cfbcf-131">Resource identifier of Synapse SQL Database.</span></span>

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

### <span data-ttu-id="cfbcf-132">-Tag</span><span class="sxs-lookup"><span data-stu-id="cfbcf-132">-Tag</span></span>
<span data-ttu-id="cfbcf-133">Eine Zeichenfolge, Zeichenfolgenwörterbuch von Tags, die der Ressource zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="cfbcf-133">A string,string dictionary of tags associated with the resource.</span></span>

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

### <span data-ttu-id="cfbcf-134">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="cfbcf-134">-WorkspaceName</span></span>
<span data-ttu-id="cfbcf-135">Name des Synapse-Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="cfbcf-135">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="cfbcf-136">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="cfbcf-136">-WorkspaceObject</span></span>
<span data-ttu-id="cfbcf-137">Arbeitsbereichs Eingabeobjekt, in der Regel durch die Pipeline übergeben.</span><span class="sxs-lookup"><span data-stu-id="cfbcf-137">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="cfbcf-138">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="cfbcf-138">-Confirm</span></span>
<span data-ttu-id="cfbcf-139">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="cfbcf-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cfbcf-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cfbcf-140">-WhatIf</span></span>
<span data-ttu-id="cfbcf-141">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="cfbcf-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cfbcf-142">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="cfbcf-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cfbcf-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cfbcf-143">CommonParameters</span></span>
<span data-ttu-id="cfbcf-144">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cfbcf-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cfbcf-145">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cfbcf-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cfbcf-146">Eingaben</span><span class="sxs-lookup"><span data-stu-id="cfbcf-146">INPUTS</span></span>

### <span data-ttu-id="cfbcf-147">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="cfbcf-147">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="cfbcf-148">Microsoft. Azure. Commands. Synapse. Models. PSSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="cfbcf-148">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlDatabase</span></span>

## <span data-ttu-id="cfbcf-149">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="cfbcf-149">OUTPUTS</span></span>

### <span data-ttu-id="cfbcf-150">Microsoft. Azure. Commands. Synapse. Models. PSSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="cfbcf-150">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlDatabase</span></span>

## <span data-ttu-id="cfbcf-151">Notizen</span><span class="sxs-lookup"><span data-stu-id="cfbcf-151">NOTES</span></span>

## <span data-ttu-id="cfbcf-152">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="cfbcf-152">RELATED LINKS</span></span>
