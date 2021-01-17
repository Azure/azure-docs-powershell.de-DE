---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/new-azsynapsesqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSqlDatabase.md
ms.openlocfilehash: b89feae28cee95c63184fd5c0e172a4cb005cac2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98356529"
---
# <span data-ttu-id="6407f-101">New-AzSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="6407f-101">New-AzSynapseSqlDatabase</span></span>

## <span data-ttu-id="6407f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6407f-102">SYNOPSIS</span></span>
<span data-ttu-id="6407f-103">Erstellt eine Synapse Analytics SQL Datenbank.</span><span class="sxs-lookup"><span data-stu-id="6407f-103">Creates a Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="6407f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6407f-104">SYNTAX</span></span>

### <span data-ttu-id="6407f-105">CreateByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="6407f-105">CreateByNameParameterSet (Default)</span></span>
```
New-AzSynapseSqlDatabase [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Tag <Hashtable>] [-Collation <String>] [-MaxSizeInBytes <Int64>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6407f-106">CreateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6407f-106">CreateByParentObjectParameterSet</span></span>
```
New-AzSynapseSqlDatabase -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-Tag <Hashtable>]
 [-Collation <String>] [-MaxSizeInBytes <Int64>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6407f-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6407f-107">DESCRIPTION</span></span>
<span data-ttu-id="6407f-108">Das **Cmdlet "Get-AzSynapseSqlDatabase"** ruft Informationen zu einer Azure Synapse Analytics SQL ab.</span><span class="sxs-lookup"><span data-stu-id="6407f-108">The **Get-AzSynapseSqlDatabase** cmdlet gets information about an Azure Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="6407f-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="6407f-109">EXAMPLES</span></span>

### <span data-ttu-id="6407f-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="6407f-110">Example 1</span></span>
```powershell
PS C:\> New-AzSynapseSqlDatabase -WorkspaceName ContosoWorkspace -Name ContosoSqlDatabase
```

<span data-ttu-id="6407f-111">Mit diesem Befehl wird eine Azure Synapse Analytics SQL erstellt.</span><span class="sxs-lookup"><span data-stu-id="6407f-111">This command creates an Azure Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="6407f-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6407f-112">PARAMETERS</span></span>

### <span data-ttu-id="6407f-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6407f-113">-AsJob</span></span>
<span data-ttu-id="6407f-114">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="6407f-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6407f-115">-Collation</span><span class="sxs-lookup"><span data-stu-id="6407f-115">-Collation</span></span>
<span data-ttu-id="6407f-116">Die Sortierung definiert die Regeln zum Sortieren und Vergleichen von Daten und kann nach der Erstellung SQL nicht mehr geändert werden.</span><span class="sxs-lookup"><span data-stu-id="6407f-116">Collation defines the rules that sort and compare data, and cannot be changed after SQL pool creation.</span></span>
<span data-ttu-id="6407f-117">Die Standardsortierung ist SQL_Latin1_General_CP1_CI_AS.</span><span class="sxs-lookup"><span data-stu-id="6407f-117">The default collation is SQL_Latin1_General_CP1_CI_AS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6407f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6407f-118">-DefaultProfile</span></span>
<span data-ttu-id="6407f-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6407f-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6407f-120">-MaxSizeInBytes</span><span class="sxs-lookup"><span data-stu-id="6407f-120">-MaxSizeInBytes</span></span>
<span data-ttu-id="6407f-121">Gibt die maximale Größe der Datenbank in Bytes an.</span><span class="sxs-lookup"><span data-stu-id="6407f-121">Specifies the maximum size of the database in bytes.</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6407f-122">-Name</span><span class="sxs-lookup"><span data-stu-id="6407f-122">-Name</span></span>
<span data-ttu-id="6407f-123">Name der Datenbank von Synapse SQL Datenbank.</span><span class="sxs-lookup"><span data-stu-id="6407f-123">Name of Synapse SQL Database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6407f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6407f-124">-ResourceGroupName</span></span>
<span data-ttu-id="6407f-125">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="6407f-125">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6407f-126">-Tag</span><span class="sxs-lookup"><span data-stu-id="6407f-126">-Tag</span></span>
<span data-ttu-id="6407f-127">Ein Zeichenfolgenverzeichnis mit Tags, die der Ressource zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="6407f-127">A string,string dictionary of tags associated with the resource.</span></span>

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

### <span data-ttu-id="6407f-128">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="6407f-128">-WorkspaceName</span></span>
<span data-ttu-id="6407f-129">Name des Synapse-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="6407f-129">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6407f-130">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="6407f-130">-WorkspaceObject</span></span>
<span data-ttu-id="6407f-131">Arbeitsbereichseingabeobjekts, das in der Regel über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="6407f-131">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: CreateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6407f-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6407f-132">-Confirm</span></span>
<span data-ttu-id="6407f-133">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6407f-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6407f-134">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="6407f-134">-WhatIf</span></span>
<span data-ttu-id="6407f-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6407f-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6407f-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6407f-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6407f-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6407f-137">CommonParameters</span></span>
<span data-ttu-id="6407f-138">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6407f-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6407f-139">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6407f-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6407f-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="6407f-140">INPUTS</span></span>

### <span data-ttu-id="6407f-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="6407f-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="6407f-142">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="6407f-142">OUTPUTS</span></span>

### <span data-ttu-id="6407f-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="6407f-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlDatabase</span></span>

## <span data-ttu-id="6407f-144">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="6407f-144">NOTES</span></span>

## <span data-ttu-id="6407f-145">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="6407f-145">RELATED LINKS</span></span>
