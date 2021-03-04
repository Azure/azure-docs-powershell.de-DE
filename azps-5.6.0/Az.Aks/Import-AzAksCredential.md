---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/powershell/module/az.aks/import-azakscredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Import-AzAksCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Import-AzAksCredential.md
ms.openlocfilehash: 06ea31f48dbe3b1d5a103598f7f16953bfc449ac
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101926051"
---
# <span data-ttu-id="4c464-101">Import-AzAksCredential</span><span class="sxs-lookup"><span data-stu-id="4c464-101">Import-AzAksCredential</span></span>

## <span data-ttu-id="4c464-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4c464-102">SYNOPSIS</span></span>
<span data-ttu-id="4c464-103">Importieren und Zusammenführen der Kubectl-Konfiguration für einen verwalteten Kubernetes-Cluster.</span><span class="sxs-lookup"><span data-stu-id="4c464-103">Import and merge Kubectl config for a managed Kubernetes Cluster.</span></span>

## <span data-ttu-id="4c464-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4c464-104">SYNTAX</span></span>

### <span data-ttu-id="4c464-105">GroupNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="4c464-105">GroupNameParameterSet (Default)</span></span>
```
Import-AzAksCredential [-ResourceGroupName] <String> [-Name] <String> [-Admin] [-ConfigPath <String>] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4c464-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4c464-106">InputObjectParameterSet</span></span>
```
Import-AzAksCredential -InputObject <PSKubernetesCluster> [-Admin] [-ConfigPath <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4c464-107">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4c464-107">IdParameterSet</span></span>
```
Import-AzAksCredential [-Id] <String> [-Admin] [-ConfigPath <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4c464-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4c464-108">DESCRIPTION</span></span>
<span data-ttu-id="4c464-109">Importieren und Zusammenführen der Kubectl-Konfiguration für einen verwalteten Kubernetes-Cluster.</span><span class="sxs-lookup"><span data-stu-id="4c464-109">Import and merge Kubectl config for a managed Kubernetes Cluster.</span></span>

## <span data-ttu-id="4c464-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="4c464-110">EXAMPLES</span></span>

### <span data-ttu-id="4c464-111">Importieren und Zusammenführen der Kubectl-Konfiguration</span><span class="sxs-lookup"><span data-stu-id="4c464-111">Import and merge Kubectl config</span></span>
```
PS C:\> Import-AzAksCredential -ResourceGroupName group -Name myCluster
```

## <span data-ttu-id="4c464-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="4c464-112">PARAMETERS</span></span>

### <span data-ttu-id="4c464-113">-Administrator</span><span class="sxs-lookup"><span data-stu-id="4c464-113">-Admin</span></span>
<span data-ttu-id="4c464-114">Holen Sie sich die kubectl-Konfiguration "clusterAdmin" anstelle des Standardmäßigen "clusterUser".</span><span class="sxs-lookup"><span data-stu-id="4c464-114">Get the 'clusterAdmin' kubectl config instead of the default 'clusterUser'.</span></span>

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

### <span data-ttu-id="4c464-115">-ConfigPath</span><span class="sxs-lookup"><span data-stu-id="4c464-115">-ConfigPath</span></span>
<span data-ttu-id="4c464-116">Eine kubectl-Konfigurationsdatei zum Erstellen oder Aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="4c464-116">A kubectl config file to create or update.</span></span>
<span data-ttu-id="4c464-117">Verwenden Sie "-", um STATTDESSEN YAML zu drucken.</span><span class="sxs-lookup"><span data-stu-id="4c464-117">Use '-' to print YAML to stdout instead.</span></span>
<span data-ttu-id="4c464-118">Standard: %Home%/.kube/config.</span><span class="sxs-lookup"><span data-stu-id="4c464-118">Default: %Home%/.kube/config.</span></span>

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

### <span data-ttu-id="4c464-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c464-119">-DefaultProfile</span></span>
<span data-ttu-id="4c464-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4c464-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4c464-121">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="4c464-121">-Force</span></span>
<span data-ttu-id="4c464-122">Importieren von Kubernetes config, auch wenn dies die Standardkonfiguration ist</span><span class="sxs-lookup"><span data-stu-id="4c464-122">Import Kubernetes config even if it is the default</span></span>

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

### <span data-ttu-id="4c464-123">-ID</span><span class="sxs-lookup"><span data-stu-id="4c464-123">-Id</span></span>
<span data-ttu-id="4c464-124">ID eines verwalteten Kubernetes-Clusters</span><span class="sxs-lookup"><span data-stu-id="4c464-124">Id of a managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="4c464-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4c464-125">-InputObject</span></span>
<span data-ttu-id="4c464-126">Ein PSKubernetesCluster-Objekt, das normalerweise über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="4c464-126">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="4c464-127">-Name</span><span class="sxs-lookup"><span data-stu-id="4c464-127">-Name</span></span>
<span data-ttu-id="4c464-128">Name Des verwalteten Kubernetes-Clusters</span><span class="sxs-lookup"><span data-stu-id="4c464-128">Name of your managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="4c464-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4c464-129">-PassThru</span></span>
<span data-ttu-id="4c464-130">Gibt "true" zurück, wenn der Import erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="4c464-130">Returns true if import is successful</span></span>

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

### <span data-ttu-id="4c464-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4c464-131">-ResourceGroupName</span></span>
<span data-ttu-id="4c464-132">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="4c464-132">Resource group name</span></span>

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

### <span data-ttu-id="4c464-133">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="4c464-133">-Confirm</span></span>
<span data-ttu-id="4c464-134">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4c464-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4c464-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4c464-135">-WhatIf</span></span>
<span data-ttu-id="4c464-136">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4c464-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4c464-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4c464-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4c464-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c464-138">CommonParameters</span></span>
<span data-ttu-id="4c464-139">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4c464-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c464-140">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4c464-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c464-141">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="4c464-141">INPUTS</span></span>

### <span data-ttu-id="4c464-142">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="4c464-142">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

### <span data-ttu-id="4c464-143">System.String</span><span class="sxs-lookup"><span data-stu-id="4c464-143">System.String</span></span>

## <span data-ttu-id="4c464-144">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="4c464-144">OUTPUTS</span></span>

### <span data-ttu-id="4c464-145">System.String</span><span class="sxs-lookup"><span data-stu-id="4c464-145">System.String</span></span>

## <span data-ttu-id="4c464-146">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="4c464-146">NOTES</span></span>

## <span data-ttu-id="4c464-147">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="4c464-147">RELATED LINKS</span></span>
