---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/new-azsynapsesqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSqlDatabase.md
ms.openlocfilehash: b89feae28cee95c63184fd5c0e172a4cb005cac2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98383590"
---
# <span data-ttu-id="831da-101">New-AzSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="831da-101">New-AzSynapseSqlDatabase</span></span>

## <span data-ttu-id="831da-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="831da-102">SYNOPSIS</span></span>
<span data-ttu-id="831da-103">Erstellt eine Synapse Analytics SQL Datenbank.</span><span class="sxs-lookup"><span data-stu-id="831da-103">Creates a Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="831da-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="831da-104">SYNTAX</span></span>

### <span data-ttu-id="831da-105">CreateByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="831da-105">CreateByNameParameterSet (Default)</span></span>
```
New-AzSynapseSqlDatabase [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Tag <Hashtable>] [-Collation <String>] [-MaxSizeInBytes <Int64>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="831da-106">CreateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="831da-106">CreateByParentObjectParameterSet</span></span>
```
New-AzSynapseSqlDatabase -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-Tag <Hashtable>]
 [-Collation <String>] [-MaxSizeInBytes <Int64>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="831da-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="831da-107">DESCRIPTION</span></span>
<span data-ttu-id="831da-108">Das **Cmdlet "Get-AzSynapseSqlDatabase"** ruft Informationen zu einer Azure Synapse Analytics SQL ab.</span><span class="sxs-lookup"><span data-stu-id="831da-108">The **Get-AzSynapseSqlDatabase** cmdlet gets information about an Azure Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="831da-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="831da-109">EXAMPLES</span></span>

### <span data-ttu-id="831da-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="831da-110">Example 1</span></span>
```powershell
PS C:\> New-AzSynapseSqlDatabase -WorkspaceName ContosoWorkspace -Name ContosoSqlDatabase
```

<span data-ttu-id="831da-111">Mit diesem Befehl wird eine Azure Synapse Analytics SQL erstellt.</span><span class="sxs-lookup"><span data-stu-id="831da-111">This command creates an Azure Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="831da-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="831da-112">PARAMETERS</span></span>

### <span data-ttu-id="831da-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="831da-113">-AsJob</span></span>
<span data-ttu-id="831da-114">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="831da-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="831da-115">-Collation</span><span class="sxs-lookup"><span data-stu-id="831da-115">-Collation</span></span>
<span data-ttu-id="831da-116">Die Sortierung definiert die Regeln zum Sortieren und Vergleichen von Daten und kann nach der Erstellung SQL nicht mehr geändert werden.</span><span class="sxs-lookup"><span data-stu-id="831da-116">Collation defines the rules that sort and compare data, and cannot be changed after SQL pool creation.</span></span>
<span data-ttu-id="831da-117">Die Standardsortierung ist SQL_Latin1_General_CP1_CI_AS.</span><span class="sxs-lookup"><span data-stu-id="831da-117">The default collation is SQL_Latin1_General_CP1_CI_AS.</span></span>

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

### <span data-ttu-id="831da-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="831da-118">-DefaultProfile</span></span>
<span data-ttu-id="831da-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="831da-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="831da-120">-MaxSizeInBytes</span><span class="sxs-lookup"><span data-stu-id="831da-120">-MaxSizeInBytes</span></span>
<span data-ttu-id="831da-121">Gibt die maximale Größe der Datenbank in Bytes an.</span><span class="sxs-lookup"><span data-stu-id="831da-121">Specifies the maximum size of the database in bytes.</span></span>

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

### <span data-ttu-id="831da-122">-Name</span><span class="sxs-lookup"><span data-stu-id="831da-122">-Name</span></span>
<span data-ttu-id="831da-123">Name der Datenbank von Synapse SQL Datenbank.</span><span class="sxs-lookup"><span data-stu-id="831da-123">Name of Synapse SQL Database.</span></span>

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

### <span data-ttu-id="831da-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="831da-124">-ResourceGroupName</span></span>
<span data-ttu-id="831da-125">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="831da-125">Resource group name.</span></span>

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

### <span data-ttu-id="831da-126">-Tag</span><span class="sxs-lookup"><span data-stu-id="831da-126">-Tag</span></span>
<span data-ttu-id="831da-127">Ein Zeichenfolgenverzeichnis mit Tags, die der Ressource zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="831da-127">A string,string dictionary of tags associated with the resource.</span></span>

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

### <span data-ttu-id="831da-128">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="831da-128">-WorkspaceName</span></span>
<span data-ttu-id="831da-129">Name des Synapse-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="831da-129">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="831da-130">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="831da-130">-WorkspaceObject</span></span>
<span data-ttu-id="831da-131">Arbeitsbereichseingabeobjekts, das in der Regel über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="831da-131">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="831da-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="831da-132">-Confirm</span></span>
<span data-ttu-id="831da-133">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="831da-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="831da-134">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="831da-134">-WhatIf</span></span>
<span data-ttu-id="831da-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="831da-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="831da-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="831da-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="831da-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="831da-137">CommonParameters</span></span>
<span data-ttu-id="831da-138">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="831da-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="831da-139">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="831da-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="831da-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="831da-140">INPUTS</span></span>

### <span data-ttu-id="831da-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="831da-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="831da-142">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="831da-142">OUTPUTS</span></span>

### <span data-ttu-id="831da-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="831da-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlDatabase</span></span>

## <span data-ttu-id="831da-144">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="831da-144">NOTES</span></span>

## <span data-ttu-id="831da-145">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="831da-145">RELATED LINKS</span></span>
