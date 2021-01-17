---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/import-azakscredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Import-AzAksCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Import-AzAksCredential.md
ms.openlocfilehash: fe4e56e809dd2cda7c650e24b55ae3867a23a7b5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98469143"
---
# <span data-ttu-id="58a93-101">Import-AzAksCredential</span><span class="sxs-lookup"><span data-stu-id="58a93-101">Import-AzAksCredential</span></span>

## <span data-ttu-id="58a93-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="58a93-102">SYNOPSIS</span></span>
<span data-ttu-id="58a93-103">Importieren und verbinden Sie die Konfigurationskonfiguration von Kubectl für einen verwalteten Kubernetes-Cluster.</span><span class="sxs-lookup"><span data-stu-id="58a93-103">Import and merge Kubectl config for a managed Kubernetes Cluster.</span></span>

## <span data-ttu-id="58a93-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="58a93-104">SYNTAX</span></span>

### <span data-ttu-id="58a93-105">GroupNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="58a93-105">GroupNameParameterSet (Default)</span></span>
```
Import-AzAksCredential [-ResourceGroupName] <String> [-Name] <String> [-Admin] [-ConfigPath <String>] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="58a93-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="58a93-106">InputObjectParameterSet</span></span>
```
Import-AzAksCredential -InputObject <PSKubernetesCluster> [-Admin] [-ConfigPath <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="58a93-107">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="58a93-107">IdParameterSet</span></span>
```
Import-AzAksCredential [-Id] <String> [-Admin] [-ConfigPath <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="58a93-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="58a93-108">DESCRIPTION</span></span>
<span data-ttu-id="58a93-109">Importieren und verbinden Sie die Konfigurationskonfiguration von Kubectl für einen verwalteten Kubernetes-Cluster.</span><span class="sxs-lookup"><span data-stu-id="58a93-109">Import and merge Kubectl config for a managed Kubernetes Cluster.</span></span>

## <span data-ttu-id="58a93-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="58a93-110">EXAMPLES</span></span>

### <span data-ttu-id="58a93-111">Importieren und Zusammenführen der Konfigurationskonfiguration von Kubectl</span><span class="sxs-lookup"><span data-stu-id="58a93-111">Import and merge Kubectl config</span></span>
```
PS C:\> Import-AzAksCredential -ResourceGroupName group -Name myCluster
```

## <span data-ttu-id="58a93-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="58a93-112">PARAMETERS</span></span>

### <span data-ttu-id="58a93-113">-Admin</span><span class="sxs-lookup"><span data-stu-id="58a93-113">-Admin</span></span>
<span data-ttu-id="58a93-114">Holen Sie sich die Kubectl-Konfiguration "clusterAdmin" anstelle des Standardmäßigen "clusterUser".</span><span class="sxs-lookup"><span data-stu-id="58a93-114">Get the 'clusterAdmin' kubectl config instead of the default 'clusterUser'.</span></span>

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

### <span data-ttu-id="58a93-115">-ConfigPath</span><span class="sxs-lookup"><span data-stu-id="58a93-115">-ConfigPath</span></span>
<span data-ttu-id="58a93-116">Eine kubectl-Konfigurationsdatei zum Erstellen oder Aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="58a93-116">A kubectl config file to create or update.</span></span>
<span data-ttu-id="58a93-117">Verwenden Sie "-", um YAML stattdessen zum Drucken zu drucken.</span><span class="sxs-lookup"><span data-stu-id="58a93-117">Use '-' to print YAML to stdout instead.</span></span>
<span data-ttu-id="58a93-118">Standard: %Home%/.kube/config.</span><span class="sxs-lookup"><span data-stu-id="58a93-118">Default: %Home%/.kube/config.</span></span>

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

### <span data-ttu-id="58a93-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58a93-119">-DefaultProfile</span></span>
<span data-ttu-id="58a93-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="58a93-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="58a93-121">-Force</span><span class="sxs-lookup"><span data-stu-id="58a93-121">-Force</span></span>
<span data-ttu-id="58a93-122">Import Kubernetes config, auch wenn dies die Standardkonfiguration ist</span><span class="sxs-lookup"><span data-stu-id="58a93-122">Import Kubernetes config even if it is the default</span></span>

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

### <span data-ttu-id="58a93-123">-ID</span><span class="sxs-lookup"><span data-stu-id="58a93-123">-Id</span></span>
<span data-ttu-id="58a93-124">ID eines verwalteten Kubernetes-Clusters</span><span class="sxs-lookup"><span data-stu-id="58a93-124">Id of a managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="58a93-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="58a93-125">-InputObject</span></span>
<span data-ttu-id="58a93-126">Ein PSAkiernetesCluster-Objekt, das normalerweise über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="58a93-126">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="58a93-127">-Name</span><span class="sxs-lookup"><span data-stu-id="58a93-127">-Name</span></span>
<span data-ttu-id="58a93-128">Name des verwalteten Kubernetes-Cluster</span><span class="sxs-lookup"><span data-stu-id="58a93-128">Name of your managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="58a93-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="58a93-129">-PassThru</span></span>
<span data-ttu-id="58a93-130">Gibt "true" zurück, wenn der Importvorgang erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="58a93-130">Returns true if import is successful</span></span>

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

### <span data-ttu-id="58a93-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58a93-131">-ResourceGroupName</span></span>
<span data-ttu-id="58a93-132">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="58a93-132">Resource group name</span></span>

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

### <span data-ttu-id="58a93-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="58a93-133">-Confirm</span></span>
<span data-ttu-id="58a93-134">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="58a93-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="58a93-135">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="58a93-135">-WhatIf</span></span>
<span data-ttu-id="58a93-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="58a93-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="58a93-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="58a93-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="58a93-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58a93-138">CommonParameters</span></span>
<span data-ttu-id="58a93-139">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58a93-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58a93-140">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="58a93-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58a93-141">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="58a93-141">INPUTS</span></span>

### <span data-ttu-id="58a93-142">Microsoft.Azure.Commands.Aks.Models.PSAkiernetesCluster</span><span class="sxs-lookup"><span data-stu-id="58a93-142">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

### <span data-ttu-id="58a93-143">System.String</span><span class="sxs-lookup"><span data-stu-id="58a93-143">System.String</span></span>

## <span data-ttu-id="58a93-144">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="58a93-144">OUTPUTS</span></span>

### <span data-ttu-id="58a93-145">System.String</span><span class="sxs-lookup"><span data-stu-id="58a93-145">System.String</span></span>

## <span data-ttu-id="58a93-146">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="58a93-146">NOTES</span></span>

## <span data-ttu-id="58a93-147">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="58a93-147">RELATED LINKS</span></span>
