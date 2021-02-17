---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapselinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseLinkedService.md
ms.openlocfilehash: d7f494b6ba943214106363a5b7dfe4dfb5cdd877
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100164617"
---
# <span data-ttu-id="d3dce-101">Get-AzSynapseLinkedService</span><span class="sxs-lookup"><span data-stu-id="d3dce-101">Get-AzSynapseLinkedService</span></span>

## <span data-ttu-id="d3dce-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d3dce-102">SYNOPSIS</span></span>
<span data-ttu-id="d3dce-103">Ruft Informationen zu verknüpften Diensten im Arbeitsbereich ab.</span><span class="sxs-lookup"><span data-stu-id="d3dce-103">Gets information about linked services in workspace.</span></span>

## <span data-ttu-id="d3dce-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d3dce-104">SYNTAX</span></span>

### <span data-ttu-id="d3dce-105">GetByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="d3dce-105">GetByName (Default)</span></span>
```
Get-AzSynapseLinkedService -WorkspaceName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d3dce-106">GetByObject</span><span class="sxs-lookup"><span data-stu-id="d3dce-106">GetByObject</span></span>
```
Get-AzSynapseLinkedService -WorkspaceObject <PSSynapseWorkspace> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d3dce-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d3dce-107">DESCRIPTION</span></span>
<span data-ttu-id="d3dce-108">Das **Cmdlet "Get-AzSynapseLinkedService"** ruft Informationen zu verknüpften Diensten im Arbeitsbereich ab.</span><span class="sxs-lookup"><span data-stu-id="d3dce-108">The **Get-AzSynapseLinkedService** cmdlet gets information about linked services in workspace.</span></span>
<span data-ttu-id="d3dce-109">Wenn Sie den Namen eines verknüpften Diensts angeben, ruft dieses Cmdlet Informationen zu diesem verknüpften Dienst ab.</span><span class="sxs-lookup"><span data-stu-id="d3dce-109">If you specify the name of a linked service, this cmdlet gets information about that linked service.</span></span>
<span data-ttu-id="d3dce-110">Wenn Sie keinen Namen angeben, ruft dieses Cmdlet Informationen zu allen verknüpften Diensten im Arbeitsbereich ab.</span><span class="sxs-lookup"><span data-stu-id="d3dce-110">If you do not specify a name, this cmdlet gets information about all the linked services in the workspace.</span></span>

## <span data-ttu-id="d3dce-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d3dce-111">EXAMPLES</span></span>

### <span data-ttu-id="d3dce-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d3dce-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseLinkedService -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="d3dce-113">Dieser Befehl ruft Informationen zu allen verknüpften Diensten im Arbeitsbereich "ContosoWorkspace" ab.</span><span class="sxs-lookup"><span data-stu-id="d3dce-113">This command gets information about all linked services in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="d3dce-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="d3dce-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseLinkedService -WorkspaceName ContosoWorkspace -Name ContosoLinkedService
```

<span data-ttu-id="d3dce-115">Dieser Befehl ruft Informationen über den verknüpften Dienst "ContosoLinkedService" im Arbeitsbereich "ContosoWorkspace" ab.</span><span class="sxs-lookup"><span data-stu-id="d3dce-115">This command gets information about the linked service named ContosoLinkedService in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="d3dce-116">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="d3dce-116">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseLinkedService -Name ContosoLinkedService
```

<span data-ttu-id="d3dce-117">Dieser Befehl ruft über die Pipeline Informationen über den verknüpften Dienst "ContosoLinkedService" im Arbeitsbereich namens "ContosoWorkspace" ab.</span><span class="sxs-lookup"><span data-stu-id="d3dce-117">This command gets information about the linked service named ContosoLinkedService in the workspace named ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="d3dce-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d3dce-118">PARAMETERS</span></span>

### <span data-ttu-id="d3dce-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3dce-119">-DefaultProfile</span></span>
<span data-ttu-id="d3dce-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d3dce-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d3dce-121">-Name</span><span class="sxs-lookup"><span data-stu-id="d3dce-121">-Name</span></span>
<span data-ttu-id="d3dce-122">Der Name des verknüpften Diensts.</span><span class="sxs-lookup"><span data-stu-id="d3dce-122">The linked service name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: LinkedServiceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3dce-123">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="d3dce-123">-WorkspaceName</span></span>
<span data-ttu-id="d3dce-124">Name des Synapse-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="d3dce-124">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3dce-125">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="d3dce-125">-WorkspaceObject</span></span>
<span data-ttu-id="d3dce-126">Arbeitsbereichseingabeobjekts, das in der Regel über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="d3dce-126">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: GetByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d3dce-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3dce-127">CommonParameters</span></span>
<span data-ttu-id="d3dce-128">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3dce-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3dce-129">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d3dce-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3dce-130">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d3dce-130">INPUTS</span></span>

### <span data-ttu-id="d3dce-131">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="d3dce-131">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="d3dce-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d3dce-132">OUTPUTS</span></span>

### <span data-ttu-id="d3dce-133">Microsoft.Azure.Commands.Synapse.Models.PSLinkedServiceResource</span><span class="sxs-lookup"><span data-stu-id="d3dce-133">Microsoft.Azure.Commands.Synapse.Models.PSLinkedServiceResource</span></span>

## <span data-ttu-id="d3dce-134">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="d3dce-134">NOTES</span></span>

## <span data-ttu-id="d3dce-135">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="d3dce-135">RELATED LINKS</span></span>
