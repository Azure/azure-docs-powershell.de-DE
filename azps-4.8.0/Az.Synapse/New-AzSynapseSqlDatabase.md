---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/new-azsynapsesqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSqlDatabase.md
ms.openlocfilehash: 16f2df5900fcc522f0ff3afb7b9f5b14ea5f0b64
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94008768"
---
# <span data-ttu-id="5ea5b-101">New-AzSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="5ea5b-101">New-AzSynapseSqlDatabase</span></span>

## <span data-ttu-id="5ea5b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5ea5b-102">SYNOPSIS</span></span>
<span data-ttu-id="5ea5b-103">Erstellt eine Synapse Analytics SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="5ea5b-103">Creates a Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="5ea5b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5ea5b-104">SYNTAX</span></span>

### <span data-ttu-id="5ea5b-105">CreateByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="5ea5b-105">CreateByNameParameterSet (Default)</span></span>
```
New-AzSynapseSqlDatabase [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Tag <Hashtable>] [-Collation <String>] [-MaxSizeInBytes <Int64>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5ea5b-106">CreateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5ea5b-106">CreateByParentObjectParameterSet</span></span>
```
New-AzSynapseSqlDatabase -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-Tag <Hashtable>]
 [-Collation <String>] [-MaxSizeInBytes <Int64>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5ea5b-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5ea5b-107">DESCRIPTION</span></span>
<span data-ttu-id="5ea5b-108">Das Cmdlet " **Get-AzSynapseSqlDatabase** " Ruft Informationen zu einer Azure Synapse Analytics SQL-Datenbank ab.</span><span class="sxs-lookup"><span data-stu-id="5ea5b-108">The **Get-AzSynapseSqlDatabase** cmdlet gets information about an Azure Synapse Analytics SQL database.</span></span>


## <span data-ttu-id="5ea5b-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5ea5b-109">EXAMPLES</span></span>

### <span data-ttu-id="5ea5b-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="5ea5b-110">Example 1</span></span>
```powershell
PS C:\> New-AzSynapseSqlDatabase -WorkspaceName ContosoWorkspace -Name ContosoSqlDatabase 
```

<span data-ttu-id="5ea5b-111">Mit diesem Befehl wird eine Azure Synapse Analytics SQL-Datenbank erstellt.</span><span class="sxs-lookup"><span data-stu-id="5ea5b-111">This command creates an Azure Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="5ea5b-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="5ea5b-112">PARAMETERS</span></span>

### <span data-ttu-id="5ea5b-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5ea5b-113">-AsJob</span></span>
<span data-ttu-id="5ea5b-114">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="5ea5b-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5ea5b-115">-Sortierung</span><span class="sxs-lookup"><span data-stu-id="5ea5b-115">-Collation</span></span>
<span data-ttu-id="5ea5b-116">Sortierung definiert die Regeln, die Daten sortieren und vergleichen, und kann nach der SQL Pool-Erstellung nicht mehr geändert werden.</span><span class="sxs-lookup"><span data-stu-id="5ea5b-116">Collation defines the rules that sort and compare data, and cannot be changed after SQL pool creation.</span></span>
<span data-ttu-id="5ea5b-117">Die Standardsortierung ist SQL_Latin1_General_CP1_CI_AS.</span><span class="sxs-lookup"><span data-stu-id="5ea5b-117">The default collation is SQL_Latin1_General_CP1_CI_AS.</span></span>

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

### <span data-ttu-id="5ea5b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ea5b-118">-DefaultProfile</span></span>
<span data-ttu-id="5ea5b-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5ea5b-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5ea5b-120">-MaxSizeInBytes</span><span class="sxs-lookup"><span data-stu-id="5ea5b-120">-MaxSizeInBytes</span></span>
<span data-ttu-id="5ea5b-121">Gibt die maximale Größe der Datenbank in Bytes an.</span><span class="sxs-lookup"><span data-stu-id="5ea5b-121">Specifies the maximum size of the database in bytes.</span></span>

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

### <span data-ttu-id="5ea5b-122">-Name</span><span class="sxs-lookup"><span data-stu-id="5ea5b-122">-Name</span></span>
<span data-ttu-id="5ea5b-123">Name der Synapse-SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="5ea5b-123">Name of Synapse SQL Database.</span></span>

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

### <span data-ttu-id="5ea5b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ea5b-124">-ResourceGroupName</span></span>
<span data-ttu-id="5ea5b-125">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="5ea5b-125">Resource group name.</span></span>

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

### <span data-ttu-id="5ea5b-126">-Tag</span><span class="sxs-lookup"><span data-stu-id="5ea5b-126">-Tag</span></span>
<span data-ttu-id="5ea5b-127">Eine Zeichenfolge, Zeichenfolgenwörterbuch von Tags, die der Ressource zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="5ea5b-127">A string,string dictionary of tags associated with the resource.</span></span>

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

### <span data-ttu-id="5ea5b-128">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="5ea5b-128">-WorkspaceName</span></span>
<span data-ttu-id="5ea5b-129">Name des Synapse-Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="5ea5b-129">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="5ea5b-130">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="5ea5b-130">-WorkspaceObject</span></span>
<span data-ttu-id="5ea5b-131">Arbeitsbereichs Eingabeobjekt, in der Regel durch die Pipeline übergeben.</span><span class="sxs-lookup"><span data-stu-id="5ea5b-131">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="5ea5b-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="5ea5b-132">-Confirm</span></span>
<span data-ttu-id="5ea5b-133">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5ea5b-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5ea5b-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5ea5b-134">-WhatIf</span></span>
<span data-ttu-id="5ea5b-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5ea5b-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5ea5b-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5ea5b-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5ea5b-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ea5b-137">CommonParameters</span></span>
<span data-ttu-id="5ea5b-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ea5b-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ea5b-139">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5ea5b-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ea5b-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5ea5b-140">INPUTS</span></span>

### <span data-ttu-id="5ea5b-141">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="5ea5b-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="5ea5b-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5ea5b-142">OUTPUTS</span></span>

### <span data-ttu-id="5ea5b-143">Microsoft. Azure. Commands. Synapse. Models. PSSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="5ea5b-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlDatabase</span></span>

## <span data-ttu-id="5ea5b-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="5ea5b-144">NOTES</span></span>

## <span data-ttu-id="5ea5b-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5ea5b-145">RELATED LINKS</span></span>
