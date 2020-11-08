---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/import-azakscredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Import-AzAksCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Import-AzAksCredential.md
ms.openlocfilehash: fe4e56e809dd2cda7c650e24b55ae3867a23a7b5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94177320"
---
# <span data-ttu-id="279b0-101">Import-AzAksCredential</span><span class="sxs-lookup"><span data-stu-id="279b0-101">Import-AzAksCredential</span></span>

## <span data-ttu-id="279b0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="279b0-102">SYNOPSIS</span></span>
<span data-ttu-id="279b0-103">Importieren und Zusammenführen der Kubectl-Konfiguration für einen verwalteten Kubernetes-Cluster</span><span class="sxs-lookup"><span data-stu-id="279b0-103">Import and merge Kubectl config for a managed Kubernetes Cluster.</span></span>

## <span data-ttu-id="279b0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="279b0-104">SYNTAX</span></span>

### <span data-ttu-id="279b0-105">GroupNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="279b0-105">GroupNameParameterSet (Default)</span></span>
```
Import-AzAksCredential [-ResourceGroupName] <String> [-Name] <String> [-Admin] [-ConfigPath <String>] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="279b0-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="279b0-106">InputObjectParameterSet</span></span>
```
Import-AzAksCredential -InputObject <PSKubernetesCluster> [-Admin] [-ConfigPath <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="279b0-107">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="279b0-107">IdParameterSet</span></span>
```
Import-AzAksCredential [-Id] <String> [-Admin] [-ConfigPath <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="279b0-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="279b0-108">DESCRIPTION</span></span>
<span data-ttu-id="279b0-109">Importieren und Zusammenführen der Kubectl-Konfiguration für einen verwalteten Kubernetes-Cluster</span><span class="sxs-lookup"><span data-stu-id="279b0-109">Import and merge Kubectl config for a managed Kubernetes Cluster.</span></span>

## <span data-ttu-id="279b0-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="279b0-110">EXAMPLES</span></span>

### <span data-ttu-id="279b0-111">Importieren und Zusammenführen der Kubectl-Konfiguration</span><span class="sxs-lookup"><span data-stu-id="279b0-111">Import and merge Kubectl config</span></span>
```
PS C:\> Import-AzAksCredential -ResourceGroupName group -Name myCluster
```

## <span data-ttu-id="279b0-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="279b0-112">PARAMETERS</span></span>

### <span data-ttu-id="279b0-113">– Administrator</span><span class="sxs-lookup"><span data-stu-id="279b0-113">-Admin</span></span>
<span data-ttu-id="279b0-114">Rufen Sie die "clusterAdmin' kubectl config" anstelle des standardmäßigen "clusterUser" ab.</span><span class="sxs-lookup"><span data-stu-id="279b0-114">Get the 'clusterAdmin' kubectl config instead of the default 'clusterUser'.</span></span>

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

### <span data-ttu-id="279b0-115">-ConfigPath</span><span class="sxs-lookup"><span data-stu-id="279b0-115">-ConfigPath</span></span>
<span data-ttu-id="279b0-116">Eine kubectl-Konfigurationsdatei zum Erstellen oder aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="279b0-116">A kubectl config file to create or update.</span></span>
<span data-ttu-id="279b0-117">Verwenden Sie "-", um stattdessen YAML auf stdout zu drucken.</span><span class="sxs-lookup"><span data-stu-id="279b0-117">Use '-' to print YAML to stdout instead.</span></span>
<span data-ttu-id="279b0-118">Standard:% Home%/.Kube/config.</span><span class="sxs-lookup"><span data-stu-id="279b0-118">Default: %Home%/.kube/config.</span></span>

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

### <span data-ttu-id="279b0-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="279b0-119">-DefaultProfile</span></span>
<span data-ttu-id="279b0-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="279b0-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="279b0-121">-Force</span><span class="sxs-lookup"><span data-stu-id="279b0-121">-Force</span></span>
<span data-ttu-id="279b0-122">Importieren der Kubernetes-Konfiguration, auch wenn dies die Standardeinstellung ist</span><span class="sxs-lookup"><span data-stu-id="279b0-122">Import Kubernetes config even if it is the default</span></span>

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

### <span data-ttu-id="279b0-123">-ID</span><span class="sxs-lookup"><span data-stu-id="279b0-123">-Id</span></span>
<span data-ttu-id="279b0-124">ID eines verwalteten Kubernetes-Clusters</span><span class="sxs-lookup"><span data-stu-id="279b0-124">Id of a managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="279b0-125">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="279b0-125">-InputObject</span></span>
<span data-ttu-id="279b0-126">Ein PSKubernetesCluster-Objekt, das normalerweise durch die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="279b0-126">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="279b0-127">-Name</span><span class="sxs-lookup"><span data-stu-id="279b0-127">-Name</span></span>
<span data-ttu-id="279b0-128">Name Ihres verwalteten Kubernetes-Clusters</span><span class="sxs-lookup"><span data-stu-id="279b0-128">Name of your managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="279b0-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="279b0-129">-PassThru</span></span>
<span data-ttu-id="279b0-130">Gibt "true" zurück, wenn der Import erfolgreich ist</span><span class="sxs-lookup"><span data-stu-id="279b0-130">Returns true if import is successful</span></span>

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

### <span data-ttu-id="279b0-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="279b0-131">-ResourceGroupName</span></span>
<span data-ttu-id="279b0-132">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="279b0-132">Resource group name</span></span>

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

### <span data-ttu-id="279b0-133">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="279b0-133">-Confirm</span></span>
<span data-ttu-id="279b0-134">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="279b0-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="279b0-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="279b0-135">-WhatIf</span></span>
<span data-ttu-id="279b0-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="279b0-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="279b0-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="279b0-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="279b0-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="279b0-138">CommonParameters</span></span>
<span data-ttu-id="279b0-139">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="279b0-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="279b0-140">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="279b0-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="279b0-141">Eingaben</span><span class="sxs-lookup"><span data-stu-id="279b0-141">INPUTS</span></span>

### <span data-ttu-id="279b0-142">Microsoft. Azure. Commands. AKS. Models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="279b0-142">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

### <span data-ttu-id="279b0-143">System. String</span><span class="sxs-lookup"><span data-stu-id="279b0-143">System.String</span></span>

## <span data-ttu-id="279b0-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="279b0-144">OUTPUTS</span></span>

### <span data-ttu-id="279b0-145">System. String</span><span class="sxs-lookup"><span data-stu-id="279b0-145">System.String</span></span>

## <span data-ttu-id="279b0-146">Notizen</span><span class="sxs-lookup"><span data-stu-id="279b0-146">NOTES</span></span>

## <span data-ttu-id="279b0-147">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="279b0-147">RELATED LINKS</span></span>
