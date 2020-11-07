---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/set-azaks
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Set-AzAks.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Set-AzAks.md
ms.openlocfilehash: 9b63ede0bbd24adb98159ca6cfee08238b26aabc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93658406"
---
# <span data-ttu-id="9ef3c-101">Set-AzAks</span><span class="sxs-lookup"><span data-stu-id="9ef3c-101">Set-AzAks</span></span>

## <span data-ttu-id="9ef3c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9ef3c-102">SYNOPSIS</span></span>
<span data-ttu-id="9ef3c-103">Aktualisieren oder Erstellen eines verwalteten Kubernetes-Clusters</span><span class="sxs-lookup"><span data-stu-id="9ef3c-103">Update or create a managed Kubernetes cluster.</span></span>

## <span data-ttu-id="9ef3c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9ef3c-104">SYNTAX</span></span>

### <span data-ttu-id="9ef3c-105">defaultParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="9ef3c-105">defaultParameterSet (Default)</span></span>
```
Set-AzAks [-ResourceGroupName] <String> [-Name] <String> [[-ClientIdAndSecret] <PSCredential>]
 [-Location <String>] [-AdminUserName <String>] [-DnsNamePrefix <String>] [-KubernetesVersion <String>]
 [-NodeCount <Int32>] [-NodeOsDiskSize <Int32>] [-NodeVmSize <String>] [-SshKeyValue <String>] [-AsJob]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9ef3c-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9ef3c-106">InputObjectParameterSet</span></span>
```
Set-AzAks -InputObject <PSKubernetesCluster> [-Location <String>] [-AdminUserName <String>]
 [-DnsNamePrefix <String>] [-KubernetesVersion <String>] [-NodeCount <Int32>] [-NodeOsDiskSize <Int32>]
 [-NodeVmSize <String>] [-SshKeyValue <String>] [-AsJob] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9ef3c-107">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9ef3c-107">IdParameterSet</span></span>
```
Set-AzAks [-Id] <String> [-Location <String>] [-AdminUserName <String>] [-DnsNamePrefix <String>]
 [-KubernetesVersion <String>] [-NodeCount <Int32>] [-NodeOsDiskSize <Int32>] [-NodeVmSize <String>]
 [-SshKeyValue <String>] [-AsJob] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9ef3c-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9ef3c-108">DESCRIPTION</span></span>
<span data-ttu-id="9ef3c-109">Aktualisieren oder Erstellen eines verwalteten Kubernetes-Clusters</span><span class="sxs-lookup"><span data-stu-id="9ef3c-109">Update or create a managed Kubernetes cluster.</span></span>

## <span data-ttu-id="9ef3c-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9ef3c-110">EXAMPLES</span></span>

### <span data-ttu-id="9ef3c-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="9ef3c-111">Example 1</span></span>
```
PS C:\> Get-AzAks -ResourceGroupName group -Name myCluster | Set-AzAks -NodeCount 5
```

<span data-ttu-id="9ef3c-112">Stellen Sie die Anzahl der Knoten im Kubernetes-Cluster auf 5 ein.</span><span class="sxs-lookup"><span data-stu-id="9ef3c-112">Set the number of nodes in the Kubernetes cluster to 5.</span></span>

## <span data-ttu-id="9ef3c-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="9ef3c-113">PARAMETERS</span></span>

### <span data-ttu-id="9ef3c-114">-Nation aus AdminUsername</span><span class="sxs-lookup"><span data-stu-id="9ef3c-114">-AdminUserName</span></span>
<span data-ttu-id="9ef3c-115">Benutzername für die virtuellen Linux-Computer.</span><span class="sxs-lookup"><span data-stu-id="9ef3c-115">User name for the Linux Virtual Machines.</span></span>

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

### <span data-ttu-id="9ef3c-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9ef3c-116">-AsJob</span></span>
<span data-ttu-id="9ef3c-117">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="9ef3c-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9ef3c-118">-ClientIdAndSecret</span><span class="sxs-lookup"><span data-stu-id="9ef3c-118">-ClientIdAndSecret</span></span>
<span data-ttu-id="9ef3c-119">Die Client-ID und der Client Schlüssel, die dem AAD-Application/Service-Prinzipal zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="9ef3c-119">The client id and client secret associated with the AAD application / service principal.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: defaultParameterSet
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ef3c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ef3c-120">-DefaultProfile</span></span>
<span data-ttu-id="9ef3c-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="9ef3c-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9ef3c-122">-DnsNamePrefix</span><span class="sxs-lookup"><span data-stu-id="9ef3c-122">-DnsNamePrefix</span></span>
<span data-ttu-id="9ef3c-123">Das DNS-Namenspräfix für den Cluster.</span><span class="sxs-lookup"><span data-stu-id="9ef3c-123">The DNS name prefix for the cluster.</span></span>

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

### <span data-ttu-id="9ef3c-124">-ID</span><span class="sxs-lookup"><span data-stu-id="9ef3c-124">-Id</span></span>
<span data-ttu-id="9ef3c-125">ID eines verwalteten Kubernetes-Clusters</span><span class="sxs-lookup"><span data-stu-id="9ef3c-125">Id of a managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="9ef3c-126">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="9ef3c-126">-InputObject</span></span>
<span data-ttu-id="9ef3c-127">Ein PSKubernetesCluster-Objekt, das normalerweise durch die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="9ef3c-127">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="9ef3c-128">-KubernetesVersion</span><span class="sxs-lookup"><span data-stu-id="9ef3c-128">-KubernetesVersion</span></span>
<span data-ttu-id="9ef3c-129">Die Version von Kubernetes, die zum Erstellen des Clusters verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="9ef3c-129">The version of Kubernetes to use for creating the cluster.</span></span>

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

### <span data-ttu-id="9ef3c-130">-Standort</span><span class="sxs-lookup"><span data-stu-id="9ef3c-130">-Location</span></span>
<span data-ttu-id="9ef3c-131">Azure-Speicherort für den Cluster.</span><span class="sxs-lookup"><span data-stu-id="9ef3c-131">Azure location for the cluster.</span></span>
<span data-ttu-id="9ef3c-132">Standardmäßig wird der Speicherort der Ressourcengruppe verwendet.</span><span class="sxs-lookup"><span data-stu-id="9ef3c-132">Defaults to the location of the resource group.</span></span>

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

### <span data-ttu-id="9ef3c-133">-Name</span><span class="sxs-lookup"><span data-stu-id="9ef3c-133">-Name</span></span>
<span data-ttu-id="9ef3c-134">Kubernetes verwalteter Cluster Name.</span><span class="sxs-lookup"><span data-stu-id="9ef3c-134">Kubernetes managed cluster Name.</span></span>

```yaml
Type: System.String
Parameter Sets: defaultParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ef3c-135">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="9ef3c-135">-NodeCount</span></span>
<span data-ttu-id="9ef3c-136">Die Standardanzahl von Knoten für die Knoten Pools.</span><span class="sxs-lookup"><span data-stu-id="9ef3c-136">The default number of nodes for the node pools.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ef3c-137">-NodeOsDiskSize</span><span class="sxs-lookup"><span data-stu-id="9ef3c-137">-NodeOsDiskSize</span></span>
<span data-ttu-id="9ef3c-138">Die Standardanzahl von Knoten für die Knoten Pools.</span><span class="sxs-lookup"><span data-stu-id="9ef3c-138">The default number of nodes for the node pools.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ef3c-139">-NodeVmSize</span><span class="sxs-lookup"><span data-stu-id="9ef3c-139">-NodeVmSize</span></span>
<span data-ttu-id="9ef3c-140">Die Größe des virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="9ef3c-140">The size of the Virtual Machine.</span></span>

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

### <span data-ttu-id="9ef3c-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ef3c-141">-ResourceGroupName</span></span>
<span data-ttu-id="9ef3c-142">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="9ef3c-142">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: defaultParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ef3c-143">-SshKeyValue</span><span class="sxs-lookup"><span data-stu-id="9ef3c-143">-SshKeyValue</span></span>
<span data-ttu-id="9ef3c-144">SSH-Schlüsseldatei Wert oder Schlüssel Dateipfad.</span><span class="sxs-lookup"><span data-stu-id="9ef3c-144">SSH key file value or key file path.</span></span>
<span data-ttu-id="9ef3c-145">Standardmäßig ist {Home}/.ssh/id_rsa. pub.</span><span class="sxs-lookup"><span data-stu-id="9ef3c-145">Defaults to {HOME}/.ssh/id_rsa.pub.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SshKeyPath

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ef3c-146">-Tag</span><span class="sxs-lookup"><span data-stu-id="9ef3c-146">-Tag</span></span>
<span data-ttu-id="9ef3c-147">Tags, die auf die Ressource angewendet werden sollen</span><span class="sxs-lookup"><span data-stu-id="9ef3c-147">Tags to be applied to the resource</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ef3c-148">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="9ef3c-148">-Confirm</span></span>
<span data-ttu-id="9ef3c-149">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9ef3c-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9ef3c-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9ef3c-150">-WhatIf</span></span>
<span data-ttu-id="9ef3c-151">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9ef3c-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9ef3c-152">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9ef3c-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9ef3c-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ef3c-153">CommonParameters</span></span>
<span data-ttu-id="9ef3c-154">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9ef3c-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ef3c-155">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9ef3c-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ef3c-156">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9ef3c-156">INPUTS</span></span>

### <span data-ttu-id="9ef3c-157">Microsoft. Azure. Commands. AKS. Models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="9ef3c-157">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

### <span data-ttu-id="9ef3c-158">System. String</span><span class="sxs-lookup"><span data-stu-id="9ef3c-158">System.String</span></span>

## <span data-ttu-id="9ef3c-159">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9ef3c-159">OUTPUTS</span></span>

### <span data-ttu-id="9ef3c-160">Microsoft. Azure. Commands. AKS. Models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="9ef3c-160">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="9ef3c-161">Notizen</span><span class="sxs-lookup"><span data-stu-id="9ef3c-161">NOTES</span></span>

## <span data-ttu-id="9ef3c-162">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9ef3c-162">RELATED LINKS</span></span>
