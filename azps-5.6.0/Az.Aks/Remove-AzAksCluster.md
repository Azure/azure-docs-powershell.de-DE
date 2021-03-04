---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/powershell/module/az.aks/remove-azakscluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Remove-AzAksCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Remove-AzAksCluster.md
ms.openlocfilehash: 0f0a1c530e4f02e031307006c0e6bf994f9a7c5f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101924288"
---
# <span data-ttu-id="e1fd8-101">Remove-AzAksCluster</span><span class="sxs-lookup"><span data-stu-id="e1fd8-101">Remove-AzAksCluster</span></span>

## <span data-ttu-id="e1fd8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e1fd8-102">SYNOPSIS</span></span>
<span data-ttu-id="e1fd8-103">Löschen Sie einen verwalteten Kubernetes-Cluster.</span><span class="sxs-lookup"><span data-stu-id="e1fd8-103">Delete a managed Kubernetes cluster.</span></span>

## <span data-ttu-id="e1fd8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e1fd8-104">SYNTAX</span></span>

### <span data-ttu-id="e1fd8-105">GroupNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="e1fd8-105">GroupNameParameterSet (Default)</span></span>
```
Remove-AzAksCluster [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e1fd8-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e1fd8-106">InputObjectParameterSet</span></span>
```
Remove-AzAksCluster -InputObject <PSKubernetesCluster> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e1fd8-107">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e1fd8-107">IdParameterSet</span></span>
```
Remove-AzAksCluster [-Id] <String> [-PassThru] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e1fd8-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e1fd8-108">DESCRIPTION</span></span>
<span data-ttu-id="e1fd8-109">Löschen Sie einen verwalteten Kubernetes-Cluster.</span><span class="sxs-lookup"><span data-stu-id="e1fd8-109">Delete a managed Kubernetes cluster.</span></span>

## <span data-ttu-id="e1fd8-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e1fd8-110">EXAMPLES</span></span>

### <span data-ttu-id="e1fd8-111">Löschen eines vorhandenen verwalteten Kubernetes-Clusters</span><span class="sxs-lookup"><span data-stu-id="e1fd8-111">Delete an existing managed Kubernetes cluster</span></span>
```powershell
PS C:\> Remove-AzAks -ResourceGroupName group -Name myCluster
```

## <span data-ttu-id="e1fd8-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="e1fd8-112">PARAMETERS</span></span>

### <span data-ttu-id="e1fd8-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e1fd8-113">-AsJob</span></span>
<span data-ttu-id="e1fd8-114">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="e1fd8-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e1fd8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1fd8-115">-DefaultProfile</span></span>
<span data-ttu-id="e1fd8-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e1fd8-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e1fd8-117">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="e1fd8-117">-Force</span></span>
<span data-ttu-id="e1fd8-118">Entfernen des verwalteten Kubernetes-Clusters ohne Eingabeaufforderung</span><span class="sxs-lookup"><span data-stu-id="e1fd8-118">Remove managed Kubernetes cluster without prompt</span></span>

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

### <span data-ttu-id="e1fd8-119">-ID</span><span class="sxs-lookup"><span data-stu-id="e1fd8-119">-Id</span></span>
<span data-ttu-id="e1fd8-120">ID eines verwalteten Kubernetes-Clusters</span><span class="sxs-lookup"><span data-stu-id="e1fd8-120">Id of a managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="e1fd8-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e1fd8-121">-InputObject</span></span>
<span data-ttu-id="e1fd8-122">Ein PSKubernetesCluster-Objekt, das normalerweise über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="e1fd8-122">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e1fd8-123">-Name</span><span class="sxs-lookup"><span data-stu-id="e1fd8-123">-Name</span></span>
<span data-ttu-id="e1fd8-124">Name Des verwalteten Kubernetes-Clusters</span><span class="sxs-lookup"><span data-stu-id="e1fd8-124">Name of your managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="e1fd8-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e1fd8-125">-PassThru</span></span>
<span data-ttu-id="e1fd8-126">Gibt "true" zurück, wenn das Löschen erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="e1fd8-126">Returns true if deletion is successful</span></span>

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

### <span data-ttu-id="e1fd8-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e1fd8-127">-ResourceGroupName</span></span>
<span data-ttu-id="e1fd8-128">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="e1fd8-128">Resource group name</span></span>

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

### <span data-ttu-id="e1fd8-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e1fd8-129">-Confirm</span></span>
<span data-ttu-id="e1fd8-130">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e1fd8-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e1fd8-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e1fd8-131">-WhatIf</span></span>
<span data-ttu-id="e1fd8-132">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e1fd8-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e1fd8-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e1fd8-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e1fd8-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1fd8-134">CommonParameters</span></span>
<span data-ttu-id="e1fd8-135">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e1fd8-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1fd8-136">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e1fd8-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1fd8-137">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e1fd8-137">INPUTS</span></span>

### <span data-ttu-id="e1fd8-138">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="e1fd8-138">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

### <span data-ttu-id="e1fd8-139">System.String</span><span class="sxs-lookup"><span data-stu-id="e1fd8-139">System.String</span></span>

## <span data-ttu-id="e1fd8-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e1fd8-140">OUTPUTS</span></span>

### <span data-ttu-id="e1fd8-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="e1fd8-141">System.Boolean</span></span>

## <span data-ttu-id="e1fd8-142">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="e1fd8-142">NOTES</span></span>

## <span data-ttu-id="e1fd8-143">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="e1fd8-143">RELATED LINKS</span></span>
