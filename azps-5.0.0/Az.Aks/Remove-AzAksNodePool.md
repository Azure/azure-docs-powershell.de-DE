---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/remove-azaksnodepool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Remove-AzAksNodePool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Remove-AzAksNodePool.md
ms.openlocfilehash: 13bc647a0b2cbbc415c12aabb9e14016e3d34149
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94177312"
---
# <span data-ttu-id="a4510-101">Remove-AzAksNodePool</span><span class="sxs-lookup"><span data-stu-id="a4510-101">Remove-AzAksNodePool</span></span>

## <span data-ttu-id="a4510-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a4510-102">SYNOPSIS</span></span>
<span data-ttu-id="a4510-103">Löschen des Knoten Pools aus verwaltetem Cluster</span><span class="sxs-lookup"><span data-stu-id="a4510-103">Delete node pool from managed cluster.</span></span>

## <span data-ttu-id="a4510-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a4510-104">SYNTAX</span></span>

### <span data-ttu-id="a4510-105">GroupNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="a4510-105">GroupNameParameterSet (Default)</span></span>
```
Remove-AzAksNodePool [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String> [-PassThru]
 [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a4510-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a4510-106">InputObjectParameterSet</span></span>
```
Remove-AzAksNodePool -InputObject <PSNodePool> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a4510-107">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a4510-107">IdParameterSet</span></span>
```
Remove-AzAksNodePool [-Id] <String> [-PassThru] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a4510-108">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a4510-108">ParentObjectParameterSet</span></span>
```
Remove-AzAksNodePool [-Name] <String> -ClusterObject <PSKubernetesCluster> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a4510-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a4510-109">DESCRIPTION</span></span>
<span data-ttu-id="a4510-110">Löschen des Knoten Pools aus verwaltetem Cluster</span><span class="sxs-lookup"><span data-stu-id="a4510-110">Delete node pool from managed cluster.</span></span>

## <span data-ttu-id="a4510-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a4510-111">EXAMPLES</span></span>

### <span data-ttu-id="a4510-112">Löschen eines angegebenen Knoten Pools</span><span class="sxs-lookup"><span data-stu-id="a4510-112">Delete specified node pool</span></span>
```powershell
PS C:\> Remove-AzAksNodePool -ResourceGroupName myResourceGroup -CulsterName myCluster -Name winpool
```

## <span data-ttu-id="a4510-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="a4510-113">PARAMETERS</span></span>

### <span data-ttu-id="a4510-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a4510-114">-AsJob</span></span>
<span data-ttu-id="a4510-115">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="a4510-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a4510-116">-Clustername</span><span class="sxs-lookup"><span data-stu-id="a4510-116">-ClusterName</span></span>
<span data-ttu-id="a4510-117">Name Ihres verwalteten Kubernetes-Clusters</span><span class="sxs-lookup"><span data-stu-id="a4510-117">Name of your managed Kubernetes cluster</span></span>

```yaml
Type: System.String
Parameter Sets: GroupNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4510-118">-Clusterobject</span><span class="sxs-lookup"><span data-stu-id="a4510-118">-ClusterObject</span></span>
<span data-ttu-id="a4510-119">Das Clusterobjekt.</span><span class="sxs-lookup"><span data-stu-id="a4510-119">The cluster object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster
Parameter Sets: ParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4510-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4510-120">-DefaultProfile</span></span>
<span data-ttu-id="a4510-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a4510-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a4510-122">-Force</span><span class="sxs-lookup"><span data-stu-id="a4510-122">-Force</span></span>
<span data-ttu-id="a4510-123">Entfernen des Knoten Pools ohne Eingabeaufforderung</span><span class="sxs-lookup"><span data-stu-id="a4510-123">Remove node pool without prompt</span></span>

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

### <span data-ttu-id="a4510-124">-ID</span><span class="sxs-lookup"><span data-stu-id="a4510-124">-Id</span></span>
<span data-ttu-id="a4510-125">ID eines Knoten Pools in verwaltetem Kubernetes-Cluster</span><span class="sxs-lookup"><span data-stu-id="a4510-125">Id of an node pool in managed Kubernetes cluster</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSet
Aliases: ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4510-126">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="a4510-126">-InputObject</span></span>
<span data-ttu-id="a4510-127">Ein PSAgentPool-Objekt, das normalerweise durch die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="a4510-127">A PSAgentPool object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Aks.Models.PSNodePool
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a4510-128">-Name</span><span class="sxs-lookup"><span data-stu-id="a4510-128">-Name</span></span>
<span data-ttu-id="a4510-129">Name des Knoten Pools</span><span class="sxs-lookup"><span data-stu-id="a4510-129">Name of your node pool</span></span>

```yaml
Type: System.String
Parameter Sets: GroupNameParameterSet, ParentObjectParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4510-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a4510-130">-PassThru</span></span>
<span data-ttu-id="a4510-131">{{Fill passthru Description}}</span><span class="sxs-lookup"><span data-stu-id="a4510-131">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="a4510-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4510-132">-ResourceGroupName</span></span>
<span data-ttu-id="a4510-133">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="a4510-133">Resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: GroupNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4510-134">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a4510-134">-Confirm</span></span>
<span data-ttu-id="a4510-135">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a4510-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a4510-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a4510-136">-WhatIf</span></span>
<span data-ttu-id="a4510-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a4510-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a4510-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a4510-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a4510-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4510-139">CommonParameters</span></span>
<span data-ttu-id="a4510-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a4510-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4510-141">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a4510-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4510-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a4510-142">INPUTS</span></span>

### <span data-ttu-id="a4510-143">Microsoft. Azure. Commands. AKS. Models. PSNodePool</span><span class="sxs-lookup"><span data-stu-id="a4510-143">Microsoft.Azure.Commands.Aks.Models.PSNodePool</span></span>

### <span data-ttu-id="a4510-144">System. String</span><span class="sxs-lookup"><span data-stu-id="a4510-144">System.String</span></span>

## <span data-ttu-id="a4510-145">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a4510-145">OUTPUTS</span></span>

### <span data-ttu-id="a4510-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a4510-146">System.Boolean</span></span>

## <span data-ttu-id="a4510-147">Notizen</span><span class="sxs-lookup"><span data-stu-id="a4510-147">NOTES</span></span>

## <span data-ttu-id="a4510-148">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a4510-148">RELATED LINKS</span></span>
