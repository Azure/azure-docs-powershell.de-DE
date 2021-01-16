---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesqlpooltransparentdataencryption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolTransparentDataEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolTransparentDataEncryption.md
ms.openlocfilehash: 5e127388b756c19422990bf27ee40e351bfc2581
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98383800"
---
# <span data-ttu-id="a4ecf-101">Get-AzSynapseSqlPoolTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="a4ecf-101">Get-AzSynapseSqlPoolTransparentDataEncryption</span></span>

## <span data-ttu-id="a4ecf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a4ecf-102">SYNOPSIS</span></span>
<span data-ttu-id="a4ecf-103">Ruft den Status "TDE" für einen SQL ab.</span><span class="sxs-lookup"><span data-stu-id="a4ecf-103">Gets the TDE state for a SQL pool.</span></span>

## <span data-ttu-id="a4ecf-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a4ecf-104">SYNTAX</span></span>

### <span data-ttu-id="a4ecf-105">GetByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="a4ecf-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSqlPoolTransparentDataEncryption [-ResourceGroupName <String>] -WorkspaceName <String>
 -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a4ecf-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a4ecf-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseSqlPoolTransparentDataEncryption -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a4ecf-107">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a4ecf-107">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseSqlPoolTransparentDataEncryption -InputObject <PSSynapseSqlPool>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a4ecf-108">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a4ecf-108">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSqlPoolTransparentDataEncryption -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a4ecf-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a4ecf-109">DESCRIPTION</span></span>
<span data-ttu-id="a4ecf-110">Das **Cmdlet "Get-AzSynapseSqlPoolTransparentDataEncryption"** ruft den Status der transparenten Datenverschlüsselung (Transparent Data Encryption, TDE) für einen Azure Synapse Analytics SQL ab.</span><span class="sxs-lookup"><span data-stu-id="a4ecf-110">The **Get-AzSynapseSqlPoolTransparentDataEncryption** cmdlet gets the state of Transparent Data Encryption (TDE) for an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="a4ecf-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a4ecf-111">EXAMPLES</span></span>

### <span data-ttu-id="a4ecf-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a4ecf-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPoolTransparentDataEncryption -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="a4ecf-113">Dieser Befehl ruft den Status "TDE" für den SQL "ContosoSqlPool" unter dem Arbeitsbereich "ContosoWorkspace" ab.</span><span class="sxs-lookup"><span data-stu-id="a4ecf-113">This command gets the status of TDE for the SQL pool named ContosoSqlPool under the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="a4ecf-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a4ecf-114">PARAMETERS</span></span>

### <span data-ttu-id="a4ecf-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4ecf-115">-DefaultProfile</span></span>
<span data-ttu-id="a4ecf-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a4ecf-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a4ecf-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a4ecf-117">-InputObject</span></span>
<span data-ttu-id="a4ecf-118">SQL pool-Eingabeobjekts, das in der Regel über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="a4ecf-118">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: GetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a4ecf-119">-Name</span><span class="sxs-lookup"><span data-stu-id="a4ecf-119">-Name</span></span>
<span data-ttu-id="a4ecf-120">Name des Synapse SQL Pools.</span><span class="sxs-lookup"><span data-stu-id="a4ecf-120">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet, GetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4ecf-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4ecf-121">-ResourceGroupName</span></span>
<span data-ttu-id="a4ecf-122">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="a4ecf-122">Resource group name.</span></span>

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

### <span data-ttu-id="a4ecf-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a4ecf-123">-ResourceId</span></span>
<span data-ttu-id="a4ecf-124">Ressourcenbezeichner von Synapse SQL Pool.</span><span class="sxs-lookup"><span data-stu-id="a4ecf-124">Resource identifier of Synapse SQL Pool.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4ecf-125">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="a4ecf-125">-WorkspaceName</span></span>
<span data-ttu-id="a4ecf-126">Name des Synapse-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="a4ecf-126">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="a4ecf-127">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="a4ecf-127">-WorkspaceObject</span></span>
<span data-ttu-id="a4ecf-128">Arbeitsbereichseingabeobjekts, das in der Regel über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="a4ecf-128">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: GetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a4ecf-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4ecf-129">CommonParameters</span></span>
<span data-ttu-id="a4ecf-130">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a4ecf-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4ecf-131">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a4ecf-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4ecf-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a4ecf-132">INPUTS</span></span>

### <span data-ttu-id="a4ecf-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="a4ecf-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="a4ecf-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="a4ecf-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="a4ecf-135">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a4ecf-135">OUTPUTS</span></span>

### <span data-ttu-id="a4ecf-136">Microsoft.Azure.Commands.Synapse.Models.PSTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="a4ecf-136">Microsoft.Azure.Commands.Synapse.Models.PSTransparentDataEncryption</span></span>

## <span data-ttu-id="a4ecf-137">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="a4ecf-137">NOTES</span></span>

## <span data-ttu-id="a4ecf-138">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="a4ecf-138">RELATED LINKS</span></span>
