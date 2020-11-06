---
external help file: Microsoft.Azure.Commands.Aks.dll-Help.xml
Module Name: AzureRM.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.aks/set-azurermaks
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Aks/Commands.Aks/help/Set-AzureRmAks.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Aks/Commands.Aks/help/Set-AzureRmAks.md
ms.openlocfilehash: b5d3248c81507abf6092aa4354691975c4b4bc13
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93480709"
---
# <span data-ttu-id="54b77-101">Set-AzureRmAks</span><span class="sxs-lookup"><span data-stu-id="54b77-101">Set-AzureRmAks</span></span>

## <span data-ttu-id="54b77-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="54b77-102">SYNOPSIS</span></span>
<span data-ttu-id="54b77-103">Aktualisieren oder Erstellen eines verwalteten Kubernetes-Clusters</span><span class="sxs-lookup"><span data-stu-id="54b77-103">Update or create a managed Kubernetes cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="54b77-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="54b77-104">SYNTAX</span></span>

### <span data-ttu-id="54b77-105">defaultParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="54b77-105">defaultParameterSet (Default)</span></span>
```
Set-AzureRmAks [-ResourceGroupName] <String> [-Name] <String> [[-ClientIdAndSecret] <PSCredential>]
 [-Location <String>] [-AdminUserName <String>] [-DnsNamePrefix <String>] [-KubernetesVersion <String>]
 [-NodeCount <Int32>] [-NodeOsDiskSize <Int32>] [-NodeVmSize <String>] [-SshKeyValue <String>] [-AsJob]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="54b77-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="54b77-106">InputObjectParameterSet</span></span>
```
Set-AzureRmAks -InputObject <PSKubernetesCluster> [-Location <String>] [-AdminUserName <String>]
 [-DnsNamePrefix <String>] [-KubernetesVersion <String>] [-NodeCount <Int32>] [-NodeOsDiskSize <Int32>]
 [-NodeVmSize <String>] [-SshKeyValue <String>] [-AsJob] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="54b77-107">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="54b77-107">IdParameterSet</span></span>
```
Set-AzureRmAks [-Id] <String> [-Location <String>] [-AdminUserName <String>] [-DnsNamePrefix <String>]
 [-KubernetesVersion <String>] [-NodeCount <Int32>] [-NodeOsDiskSize <Int32>] [-NodeVmSize <String>]
 [-SshKeyValue <String>] [-AsJob] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="54b77-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="54b77-108">DESCRIPTION</span></span>
<span data-ttu-id="54b77-109">Aktualisieren oder Erstellen eines verwalteten Kubernetes-Clusters</span><span class="sxs-lookup"><span data-stu-id="54b77-109">Update or create a managed Kubernetes cluster.</span></span>

## <span data-ttu-id="54b77-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="54b77-110">EXAMPLES</span></span>

### <span data-ttu-id="54b77-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="54b77-111">Example 1</span></span>
```
PS C:\> Get-AzureRmAks -ResourceGroupName group -Name myCluster | Set-AzureRmAks -NodeCount 5
```

<span data-ttu-id="54b77-112">Stellen Sie die Anzahl der Knoten im Kubernetes-Cluster auf 5 ein.</span><span class="sxs-lookup"><span data-stu-id="54b77-112">Set the number of nodes in the Kubernetes cluster to 5.</span></span>

## <span data-ttu-id="54b77-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="54b77-113">PARAMETERS</span></span>

### <span data-ttu-id="54b77-114">-Nation aus AdminUsername</span><span class="sxs-lookup"><span data-stu-id="54b77-114">-AdminUserName</span></span>
<span data-ttu-id="54b77-115">Benutzername für die virtuellen Linux-Computer.</span><span class="sxs-lookup"><span data-stu-id="54b77-115">User name for the Linux Virtual Machines.</span></span>

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

### <span data-ttu-id="54b77-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="54b77-116">-AsJob</span></span>
<span data-ttu-id="54b77-117">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="54b77-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="54b77-118">-ClientIdAndSecret</span><span class="sxs-lookup"><span data-stu-id="54b77-118">-ClientIdAndSecret</span></span>
<span data-ttu-id="54b77-119">Die Client-ID und der Client Schlüssel, die dem AAD-Application/Service-Prinzipal zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="54b77-119">The client id and client secret associated with the AAD application / service principal.</span></span>

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

### <span data-ttu-id="54b77-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54b77-120">-DefaultProfile</span></span>
<span data-ttu-id="54b77-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="54b77-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54b77-122">-DnsNamePrefix</span><span class="sxs-lookup"><span data-stu-id="54b77-122">-DnsNamePrefix</span></span>
<span data-ttu-id="54b77-123">Das DNS-Namenspräfix für den Cluster.</span><span class="sxs-lookup"><span data-stu-id="54b77-123">The DNS name prefix for the cluster.</span></span>

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

### <span data-ttu-id="54b77-124">-ID</span><span class="sxs-lookup"><span data-stu-id="54b77-124">-Id</span></span>
<span data-ttu-id="54b77-125">ID eines verwalteten Kubernetes-Clusters</span><span class="sxs-lookup"><span data-stu-id="54b77-125">Id of a managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="54b77-126">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="54b77-126">-InputObject</span></span>
<span data-ttu-id="54b77-127">Ein PSKubernetesCluster-Objekt, das normalerweise durch die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="54b77-127">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="54b77-128">-KubernetesVersion</span><span class="sxs-lookup"><span data-stu-id="54b77-128">-KubernetesVersion</span></span>
<span data-ttu-id="54b77-129">Die Version von Kubernetes, die zum Erstellen des Clusters verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="54b77-129">The version of Kubernetes to use for creating the cluster.</span></span>

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

### <span data-ttu-id="54b77-130">-Standort</span><span class="sxs-lookup"><span data-stu-id="54b77-130">-Location</span></span>
<span data-ttu-id="54b77-131">Azure-Speicherort für den Cluster.</span><span class="sxs-lookup"><span data-stu-id="54b77-131">Azure location for the cluster.</span></span>
<span data-ttu-id="54b77-132">Standardmäßig wird der Speicherort der Ressourcengruppe verwendet.</span><span class="sxs-lookup"><span data-stu-id="54b77-132">Defaults to the location of the resource group.</span></span>

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

### <span data-ttu-id="54b77-133">-Name</span><span class="sxs-lookup"><span data-stu-id="54b77-133">-Name</span></span>
<span data-ttu-id="54b77-134">Kubernetes verwalteter Cluster Name.</span><span class="sxs-lookup"><span data-stu-id="54b77-134">Kubernetes managed cluster Name.</span></span>

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

### <span data-ttu-id="54b77-135">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="54b77-135">-NodeCount</span></span>
<span data-ttu-id="54b77-136">Die Standardanzahl von Knoten für die Knoten Pools.</span><span class="sxs-lookup"><span data-stu-id="54b77-136">The default number of nodes for the node pools.</span></span>

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

### <span data-ttu-id="54b77-137">-NodeOsDiskSize</span><span class="sxs-lookup"><span data-stu-id="54b77-137">-NodeOsDiskSize</span></span>
<span data-ttu-id="54b77-138">Die Standardanzahl von Knoten für die Knoten Pools.</span><span class="sxs-lookup"><span data-stu-id="54b77-138">The default number of nodes for the node pools.</span></span>

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

### <span data-ttu-id="54b77-139">-NodeVmSize</span><span class="sxs-lookup"><span data-stu-id="54b77-139">-NodeVmSize</span></span>
<span data-ttu-id="54b77-140">Die Größe des virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="54b77-140">The size of the Virtual Machine.</span></span>

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

### <span data-ttu-id="54b77-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="54b77-141">-ResourceGroupName</span></span>
<span data-ttu-id="54b77-142">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="54b77-142">Resource Group Name.</span></span>

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

### <span data-ttu-id="54b77-143">-SshKeyValue</span><span class="sxs-lookup"><span data-stu-id="54b77-143">-SshKeyValue</span></span>
<span data-ttu-id="54b77-144">SSH-Schlüsseldatei Wert oder Schlüssel Dateipfad.</span><span class="sxs-lookup"><span data-stu-id="54b77-144">SSH key file value or key file path.</span></span>
<span data-ttu-id="54b77-145">Standardmäßig ist {Home}/.ssh/id_rsa. pub.</span><span class="sxs-lookup"><span data-stu-id="54b77-145">Defaults to {HOME}/.ssh/id_rsa.pub.</span></span>

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

### <span data-ttu-id="54b77-146">-Tag</span><span class="sxs-lookup"><span data-stu-id="54b77-146">-Tag</span></span>
<span data-ttu-id="54b77-147">Tags, die auf die Ressource angewendet werden sollen</span><span class="sxs-lookup"><span data-stu-id="54b77-147">Tags to be applied to the resource</span></span>

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

### <span data-ttu-id="54b77-148">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="54b77-148">-Confirm</span></span>
<span data-ttu-id="54b77-149">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="54b77-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="54b77-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="54b77-150">-WhatIf</span></span>
<span data-ttu-id="54b77-151">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="54b77-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="54b77-152">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="54b77-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="54b77-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54b77-153">CommonParameters</span></span>
<span data-ttu-id="54b77-154">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="54b77-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54b77-155">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="54b77-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54b77-156">Eingaben</span><span class="sxs-lookup"><span data-stu-id="54b77-156">INPUTS</span></span>

### <span data-ttu-id="54b77-157">Microsoft. Azure. Commands. AKS. Models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="54b77-157">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>
<span data-ttu-id="54b77-158">Parameter: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="54b77-158">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="54b77-159">System. String</span><span class="sxs-lookup"><span data-stu-id="54b77-159">System.String</span></span>

## <span data-ttu-id="54b77-160">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="54b77-160">OUTPUTS</span></span>

### <span data-ttu-id="54b77-161">Microsoft. Azure. Commands. AKS. Models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="54b77-161">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="54b77-162">Notizen</span><span class="sxs-lookup"><span data-stu-id="54b77-162">NOTES</span></span>

## <span data-ttu-id="54b77-163">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="54b77-163">RELATED LINKS</span></span>
