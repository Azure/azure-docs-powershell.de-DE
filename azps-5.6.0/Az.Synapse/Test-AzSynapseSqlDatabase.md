---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/test-azsynapsesqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseSqlDatabase.md
ms.openlocfilehash: e797cba0c05b6dbaee11d540b9efc3aca7e7efcf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101948243"
---
# <span data-ttu-id="fbbb6-101">Test-AzSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="fbbb6-101">Test-AzSynapseSqlDatabase</span></span>

## <span data-ttu-id="fbbb6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fbbb6-102">SYNOPSIS</span></span>
<span data-ttu-id="fbbb6-103">Überprüft das Vorhandensein einer Synapse Analytics-SQL Datenbank.</span><span class="sxs-lookup"><span data-stu-id="fbbb6-103">Checks for the existence of a Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="fbbb6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fbbb6-104">SYNTAX</span></span>

### <span data-ttu-id="fbbb6-105">TestByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="fbbb6-105">TestByNameParameterSet (Default)</span></span>
```
Test-AzSynapseSqlDatabase [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fbbb6-106">TestByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fbbb6-106">TestByParentObjectParameterSet</span></span>
```
Test-AzSynapseSqlDatabase -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fbbb6-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fbbb6-107">DESCRIPTION</span></span>
<span data-ttu-id="fbbb6-108">Das **Cmdlet Test-AzSynapseSqlDatabase** überprüft das Vorhandensein einer Synapse Analytics-SQL Datenbank.</span><span class="sxs-lookup"><span data-stu-id="fbbb6-108">The **Test-AzSynapseSqlDatabase** cmdlet checks for the existence of a Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="fbbb6-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="fbbb6-109">EXAMPLES</span></span>

### <span data-ttu-id="fbbb6-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="fbbb6-110">Example 1</span></span>
```powershell
PS C:\> Test-AzSynapseSqlDatabase -WorkspaceName ContosoWorkspace -Name ContosoSqlDatabase
```

<span data-ttu-id="fbbb6-111">Dieser Befehl überprüft das Vorhandensein der angegebenen SQL Datenbank.</span><span class="sxs-lookup"><span data-stu-id="fbbb6-111">This command checks the existence of the specified SQL database.</span></span>

## <span data-ttu-id="fbbb6-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="fbbb6-112">PARAMETERS</span></span>

### <span data-ttu-id="fbbb6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fbbb6-113">-DefaultProfile</span></span>
<span data-ttu-id="fbbb6-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fbbb6-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fbbb6-115">-Name</span><span class="sxs-lookup"><span data-stu-id="fbbb6-115">-Name</span></span>
<span data-ttu-id="fbbb6-116">Name von Synapse SQL Datenbank.</span><span class="sxs-lookup"><span data-stu-id="fbbb6-116">Name of Synapse SQL Database.</span></span>

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

### <span data-ttu-id="fbbb6-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fbbb6-117">-ResourceGroupName</span></span>
<span data-ttu-id="fbbb6-118">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="fbbb6-118">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: TestByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbbb6-119">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="fbbb6-119">-WorkspaceName</span></span>
<span data-ttu-id="fbbb6-120">Name des Synapse-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="fbbb6-120">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: TestByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbbb6-121">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="fbbb6-121">-WorkspaceObject</span></span>
<span data-ttu-id="fbbb6-122">Arbeitsbereichseingabeobjekt, das in der Regel über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="fbbb6-122">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: TestByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fbbb6-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fbbb6-123">CommonParameters</span></span>
<span data-ttu-id="fbbb6-124">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fbbb6-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fbbb6-125">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fbbb6-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fbbb6-126">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="fbbb6-126">INPUTS</span></span>

### <span data-ttu-id="fbbb6-127">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="fbbb6-127">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="fbbb6-128">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="fbbb6-128">OUTPUTS</span></span>

### <span data-ttu-id="fbbb6-129">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="fbbb6-129">System.Boolean</span></span>

## <span data-ttu-id="fbbb6-130">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="fbbb6-130">NOTES</span></span>

## <span data-ttu-id="fbbb6-131">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="fbbb6-131">RELATED LINKS</span></span>
