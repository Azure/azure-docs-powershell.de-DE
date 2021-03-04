---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/get-azsynapsedroppedsqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseDroppedSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseDroppedSqlPool.md
ms.openlocfilehash: 26e4e5c77913f01b8a7097f6baebd68977ceed22
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101933531"
---
# <span data-ttu-id="c2885-101">Get-AzSynapseDroppedSqlPool</span><span class="sxs-lookup"><span data-stu-id="c2885-101">Get-AzSynapseDroppedSqlPool</span></span>

## <span data-ttu-id="c2885-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c2885-102">SYNOPSIS</span></span>
<span data-ttu-id="c2885-103">Ruft eine verworfene Sql-Pool-Sicherung eines Synapse Sql-Pools ab.</span><span class="sxs-lookup"><span data-stu-id="c2885-103">Gets a dropped Sql pool backup of a Synapse Sql Pool.</span></span>

## <span data-ttu-id="c2885-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c2885-104">SYNTAX</span></span>

### <span data-ttu-id="c2885-105">GetByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="c2885-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseDroppedSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c2885-106">DroppedSqlPoolResourceId</span><span class="sxs-lookup"><span data-stu-id="c2885-106">DroppedSqlPoolResourceId</span></span>
```
Get-AzSynapseDroppedSqlPool [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c2885-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c2885-107">DESCRIPTION</span></span>
<span data-ttu-id="c2885-108">Das **Get-AzSynapseDroppedSqlPool-Cmdlet** ruft eine angegebene gelöschte SQL-Poolsicherung ab, die Sie wiederherstellen können, oder alle gelöschten Sicherungen, die Sie in einem Arbeitsbereich wiederherstellen können.</span><span class="sxs-lookup"><span data-stu-id="c2885-108">The **Get-AzSynapseDroppedSqlPool** cmdlet gets a specified deleted SQL pool backup that you can restore, or all deleted backups that you can restore in a workspace.</span></span> 


## <span data-ttu-id="c2885-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c2885-109">EXAMPLES</span></span>

### <span data-ttu-id="c2885-110">Beispiel 1: Erhalten eines angegebenen verworfenen Sqlpools aus einem SQL-Pool</span><span class="sxs-lookup"><span data-stu-id="c2885-110">Example 1: Get a specified dropped sqlpools from a sql pool</span></span>
```powershell
PS C:\> Get-AzSynapseDroppedSqlPool -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -Name "ContosoSqlPool"
```
<span data-ttu-id="c2885-111">Das Cmdlet ruft abgelegte Sqlpools für einen SQL-Pool ab.</span><span class="sxs-lookup"><span data-stu-id="c2885-111">The cmdlet retrieves dropped sqlpools for a sql pool.</span></span>

### <span data-ttu-id="c2885-112">Beispiel 2: Alle verworfenen Sqlpools in einem Arbeitsbereich</span><span class="sxs-lookup"><span data-stu-id="c2885-112">Example 2: Get all dropped sqlpool on a workspace</span></span>
```
PS C:\>Get-AzSynapseDroppedSqlPool -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace"
```
<span data-ttu-id="c2885-113">Dieser Befehl ruft alle verfügbaren abgelegten Sqlpools in einem angegebenen Arbeitsbereich ab.</span><span class="sxs-lookup"><span data-stu-id="c2885-113">This command gets all available dropped sqlpool on a specified workspace.</span></span>

## <span data-ttu-id="c2885-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="c2885-114">PARAMETERS</span></span>

### <span data-ttu-id="c2885-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2885-115">-DefaultProfile</span></span>
<span data-ttu-id="c2885-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c2885-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c2885-117">-Name</span><span class="sxs-lookup"><span data-stu-id="c2885-117">-Name</span></span>
<span data-ttu-id="c2885-118">Der Synapse Sql-Pool.</span><span class="sxs-lookup"><span data-stu-id="c2885-118">The Synapse Sql pool.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases: AzSynapseDroppedSqlPool

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2885-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c2885-119">-ResourceId</span></span>
<span data-ttu-id="c2885-120">Geben Sie eine abgelegte Sql Pool-Ressourcen-ID ein.</span><span class="sxs-lookup"><span data-stu-id="c2885-120">Input a Dropped Sql Pool Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: DroppedSqlPoolResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2885-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2885-121">-ResourceGroupName</span></span>
<span data-ttu-id="c2885-122">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="c2885-122">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2885-123">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="c2885-123">-WorkspaceName</span></span>
<span data-ttu-id="c2885-124">Name des Synapse-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="c2885-124">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2885-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2885-125">CommonParameters</span></span>
<span data-ttu-id="c2885-126">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2885-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2885-127">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c2885-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2885-128">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c2885-128">INPUTS</span></span>

### <span data-ttu-id="c2885-129">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="c2885-129">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="c2885-130">Microsoft.Azure.Commands.Synapse.Models.PSSynapseResourceGroup</span><span class="sxs-lookup"><span data-stu-id="c2885-130">Microsoft.Azure.Commands.Synapse.Models.PSSynapseResourceGroup</span></span>

## <span data-ttu-id="c2885-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c2885-131">OUTPUTS</span></span>

### <span data-ttu-id="c2885-132">Microsoft.Azure.Commands.Synapse.Models.PSDroppedSqlPoolBackupModel</span><span class="sxs-lookup"><span data-stu-id="c2885-132">Microsoft.Azure.Commands.Synapse.Models.PSDroppedSqlPoolBackupModel</span></span>

## <span data-ttu-id="c2885-133">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="c2885-133">NOTES</span></span>

## <span data-ttu-id="c2885-134">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="c2885-134">RELATED LINKS</span></span>
