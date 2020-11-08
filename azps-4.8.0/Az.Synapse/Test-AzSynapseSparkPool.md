---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/test-azsynapsesparkpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseSparkPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseSparkPool.md
ms.openlocfilehash: 6304e730e6b3b0a4f8edc0f42fc024852acbfc12
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94007670"
---
# <span data-ttu-id="c38f3-101">Test-AzSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="c38f3-101">Test-AzSynapseSparkPool</span></span>

## <span data-ttu-id="c38f3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c38f3-102">SYNOPSIS</span></span>
<span data-ttu-id="c38f3-103">Überprüft, ob ein Synapse Analytics-Spark-Pool vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="c38f3-103">Checks for the existence of a Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="c38f3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c38f3-104">SYNTAX</span></span>

### <span data-ttu-id="c38f3-105">TestByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="c38f3-105">TestByNameParameterSet (Default)</span></span>
```
Test-AzSynapseSparkPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c38f3-106">TestByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c38f3-106">TestByParentObjectParameterSet</span></span>
```
Test-AzSynapseSparkPool -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c38f3-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c38f3-107">DESCRIPTION</span></span>
<span data-ttu-id="c38f3-108">Das Cmdlet **Test-AzSynapseSparkPool** überprüft, ob ein Spark-Pool für Synapse-Analysen vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="c38f3-108">The **Test-AzSynapseSparkPool** cmdlet checks for the existence of a Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="c38f3-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c38f3-109">EXAMPLES</span></span>

### <span data-ttu-id="c38f3-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c38f3-110">Example 1</span></span>
```powershell
PS C:\> Test-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool
```

<span data-ttu-id="c38f3-111">Dieser Befehl überprüft das vorhanden sein des angegebenen Spark-Pools.</span><span class="sxs-lookup"><span data-stu-id="c38f3-111">This command checks the existence of the specified Spark pool.</span></span>

## <span data-ttu-id="c38f3-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="c38f3-112">PARAMETERS</span></span>

### <span data-ttu-id="c38f3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c38f3-113">-DefaultProfile</span></span>
<span data-ttu-id="c38f3-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c38f3-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c38f3-115">-Name</span><span class="sxs-lookup"><span data-stu-id="c38f3-115">-Name</span></span>
<span data-ttu-id="c38f3-116">Name des Synapsen-Spark-Pools.</span><span class="sxs-lookup"><span data-stu-id="c38f3-116">Name of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="c38f3-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c38f3-117">-ResourceGroupName</span></span>
<span data-ttu-id="c38f3-118">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="c38f3-118">Resource group name.</span></span>

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

### <span data-ttu-id="c38f3-119">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="c38f3-119">-WorkspaceName</span></span>
<span data-ttu-id="c38f3-120">Name des Synapse-Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="c38f3-120">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="c38f3-121">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="c38f3-121">-WorkspaceObject</span></span>
<span data-ttu-id="c38f3-122">Arbeitsbereichs Eingabeobjekt, in der Regel durch die Pipeline übergeben.</span><span class="sxs-lookup"><span data-stu-id="c38f3-122">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="c38f3-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c38f3-123">CommonParameters</span></span>
<span data-ttu-id="c38f3-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c38f3-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c38f3-125">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c38f3-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c38f3-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c38f3-126">INPUTS</span></span>

### <span data-ttu-id="c38f3-127">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="c38f3-127">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="c38f3-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c38f3-128">OUTPUTS</span></span>

### <span data-ttu-id="c38f3-129">System. Object</span><span class="sxs-lookup"><span data-stu-id="c38f3-129">System.Object</span></span>
## <span data-ttu-id="c38f3-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="c38f3-130">NOTES</span></span>

## <span data-ttu-id="c38f3-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c38f3-131">RELATED LINKS</span></span>
