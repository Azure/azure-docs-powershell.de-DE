---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/test-azsynapsesqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseSqlDatabase.md
ms.openlocfilehash: e97c10359d00fefa30c783e67c7a3bc64c16a214
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94007666"
---
# <span data-ttu-id="412f1-101">Test-AzSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="412f1-101">Test-AzSynapseSqlDatabase</span></span>

## <span data-ttu-id="412f1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="412f1-102">SYNOPSIS</span></span>
<span data-ttu-id="412f1-103">Überprüft, ob eine Synapse Analytics SQL-Datenbank vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="412f1-103">Checks for the existence of a Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="412f1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="412f1-104">SYNTAX</span></span>

### <span data-ttu-id="412f1-105">TestByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="412f1-105">TestByNameParameterSet (Default)</span></span>
```
Test-AzSynapseSqlDatabase [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="412f1-106">TestByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="412f1-106">TestByParentObjectParameterSet</span></span>
```
Test-AzSynapseSqlDatabase -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="412f1-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="412f1-107">DESCRIPTION</span></span>
<span data-ttu-id="412f1-108">Das Cmdlet **Test-AzSynapseSqlDatabase** überprüft, ob eine Synapse Analytics SQL-Datenbank vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="412f1-108">The **Test-AzSynapseSqlDatabase** cmdlet checks for the existence of a Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="412f1-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="412f1-109">EXAMPLES</span></span>

### <span data-ttu-id="412f1-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="412f1-110">Example 1</span></span>
```powershell
PS C:\> Test-AzSynapseSqlDatabase -WorkspaceName ContosoWorkspace -Name ContosoSqlDatabase
```

<span data-ttu-id="412f1-111">Dieser Befehl überprüft das vorhanden sein der angegebenen SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="412f1-111">This command checks the existence of the specified SQL database.</span></span>

## <span data-ttu-id="412f1-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="412f1-112">PARAMETERS</span></span>

### <span data-ttu-id="412f1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="412f1-113">-DefaultProfile</span></span>
<span data-ttu-id="412f1-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="412f1-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="412f1-115">-Name</span><span class="sxs-lookup"><span data-stu-id="412f1-115">-Name</span></span>
<span data-ttu-id="412f1-116">Name der Synapse-SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="412f1-116">Name of Synapse SQL Database.</span></span>

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

### <span data-ttu-id="412f1-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="412f1-117">-ResourceGroupName</span></span>
<span data-ttu-id="412f1-118">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="412f1-118">Resource group name.</span></span>

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

### <span data-ttu-id="412f1-119">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="412f1-119">-WorkspaceName</span></span>
<span data-ttu-id="412f1-120">Name des Synapse-Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="412f1-120">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="412f1-121">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="412f1-121">-WorkspaceObject</span></span>
<span data-ttu-id="412f1-122">Arbeitsbereichs Eingabeobjekt, in der Regel durch die Pipeline übergeben.</span><span class="sxs-lookup"><span data-stu-id="412f1-122">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="412f1-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="412f1-123">CommonParameters</span></span>
<span data-ttu-id="412f1-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="412f1-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="412f1-125">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="412f1-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="412f1-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="412f1-126">INPUTS</span></span>

### <span data-ttu-id="412f1-127">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="412f1-127">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="412f1-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="412f1-128">OUTPUTS</span></span>

### <span data-ttu-id="412f1-129">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="412f1-129">System.Boolean</span></span>

## <span data-ttu-id="412f1-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="412f1-130">NOTES</span></span>

## <span data-ttu-id="412f1-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="412f1-131">RELATED LINKS</span></span>
