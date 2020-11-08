---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/new-azaks
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/New-AzAks.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/New-AzAks.md
ms.openlocfilehash: a5a376fea0dc40bbfd02ea1cb430c725c2bc14e8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94004091"
---
# <span data-ttu-id="9999f-101">New-AzAks</span><span class="sxs-lookup"><span data-stu-id="9999f-101">New-AzAks</span></span>

## <span data-ttu-id="9999f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9999f-102">SYNOPSIS</span></span>
<span data-ttu-id="9999f-103">Erstellen eines neuen verwalteten Kubernetes-Clusters</span><span class="sxs-lookup"><span data-stu-id="9999f-103">Create a new managed Kubernetes cluster.</span></span>

## <span data-ttu-id="9999f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9999f-104">SYNTAX</span></span>

```
New-AzAks [-Force] [-ResourceGroupName] <String> [-Name] <String> [[-ClientIdAndSecret] <PSCredential>]
 [-Location <String>] [-AdminUserName <String>] [-DnsNamePrefix <String>] [-KubernetesVersion <String>]
 [-NodeCount <Int32>] [-NodeOsDiskSize <Int32>] [-NodeVmSize <String>] [-SshKeyValue <String>] [-AsJob]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9999f-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9999f-105">DESCRIPTION</span></span>

<span data-ttu-id="9999f-106">Erstellen eines neuen verwalteten Kubernetes-Clusters</span><span class="sxs-lookup"><span data-stu-id="9999f-106">Create a new managed Kubernetes cluster.</span></span>

## <span data-ttu-id="9999f-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9999f-107">EXAMPLES</span></span>

### <span data-ttu-id="9999f-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="9999f-108">Example 1</span></span>

<span data-ttu-id="9999f-109">Erstellen Sie einen neuen verwalteten Kubernetes-Cluster mit Standard-params.</span><span class="sxs-lookup"><span data-stu-id="9999f-109">Create a new managed Kubernetes cluster with default params.</span></span>

```
PS C:\> New-AzAks -ResourceGroupName group -Name myCluster
```

## <span data-ttu-id="9999f-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="9999f-110">PARAMETERS</span></span>

### <span data-ttu-id="9999f-111">-Nation aus AdminUsername</span><span class="sxs-lookup"><span data-stu-id="9999f-111">-AdminUserName</span></span>
<span data-ttu-id="9999f-112">Benutzername für die virtuellen Linux-Computer.</span><span class="sxs-lookup"><span data-stu-id="9999f-112">User name for the Linux Virtual Machines.</span></span>

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

### <span data-ttu-id="9999f-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9999f-113">-AsJob</span></span>
<span data-ttu-id="9999f-114">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="9999f-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9999f-115">-ClientIdAndSecret</span><span class="sxs-lookup"><span data-stu-id="9999f-115">-ClientIdAndSecret</span></span>
<span data-ttu-id="9999f-116">Die Client-ID und der Client Schlüssel, die dem AAD-Application/Service-Prinzipal zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="9999f-116">The client id and client secret associated with the AAD application / service principal.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9999f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9999f-117">-DefaultProfile</span></span>
<span data-ttu-id="9999f-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="9999f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9999f-119">-DnsNamePrefix</span><span class="sxs-lookup"><span data-stu-id="9999f-119">-DnsNamePrefix</span></span>
<span data-ttu-id="9999f-120">Das DNS-Namenspräfix für den Cluster.</span><span class="sxs-lookup"><span data-stu-id="9999f-120">The DNS name prefix for the cluster.</span></span>

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

### <span data-ttu-id="9999f-121">-Force</span><span class="sxs-lookup"><span data-stu-id="9999f-121">-Force</span></span>
<span data-ttu-id="9999f-122">Erstellen eines Clusters, auch wenn er bereits vorhanden ist</span><span class="sxs-lookup"><span data-stu-id="9999f-122">Create cluster even if it already exists</span></span>

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

### <span data-ttu-id="9999f-123">-KubernetesVersion</span><span class="sxs-lookup"><span data-stu-id="9999f-123">-KubernetesVersion</span></span>
<span data-ttu-id="9999f-124">Die Version von Kubernetes, die zum Erstellen des Clusters verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="9999f-124">The version of Kubernetes to use for creating the cluster.</span></span>

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

### <span data-ttu-id="9999f-125">-Standort</span><span class="sxs-lookup"><span data-stu-id="9999f-125">-Location</span></span>
<span data-ttu-id="9999f-126">Azure-Speicherort für den Cluster.</span><span class="sxs-lookup"><span data-stu-id="9999f-126">Azure location for the cluster.</span></span>
<span data-ttu-id="9999f-127">Standardmäßig wird der Speicherort der Ressourcengruppe verwendet.</span><span class="sxs-lookup"><span data-stu-id="9999f-127">Defaults to the location of the resource group.</span></span>

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

### <span data-ttu-id="9999f-128">-Name</span><span class="sxs-lookup"><span data-stu-id="9999f-128">-Name</span></span>
<span data-ttu-id="9999f-129">Kubernetes verwalteter Cluster Name.</span><span class="sxs-lookup"><span data-stu-id="9999f-129">Kubernetes managed cluster Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9999f-130">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="9999f-130">-NodeCount</span></span>
<span data-ttu-id="9999f-131">Die Standardanzahl von Knoten für die Knoten Pools.</span><span class="sxs-lookup"><span data-stu-id="9999f-131">The default number of nodes for the node pools.</span></span>

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

### <span data-ttu-id="9999f-132">-NodeOsDiskSize</span><span class="sxs-lookup"><span data-stu-id="9999f-132">-NodeOsDiskSize</span></span>
<span data-ttu-id="9999f-133">Die Größe der Betriebssystem Diskette für jeden Knoten im Knoten Pool in GB.</span><span class="sxs-lookup"><span data-stu-id="9999f-133">Size in GB of the OS disk for each node in the node pool.</span></span> <span data-ttu-id="9999f-134">Mind. 30 GB.</span><span class="sxs-lookup"><span data-stu-id="9999f-134">Minimum 30 GB.</span></span>

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

### <span data-ttu-id="9999f-135">-NodeVmSize</span><span class="sxs-lookup"><span data-stu-id="9999f-135">-NodeVmSize</span></span>
<span data-ttu-id="9999f-136">Die Größe des virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="9999f-136">The size of the Virtual Machine.</span></span>

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

### <span data-ttu-id="9999f-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9999f-137">-ResourceGroupName</span></span>
<span data-ttu-id="9999f-138">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="9999f-138">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9999f-139">-SshKeyValue</span><span class="sxs-lookup"><span data-stu-id="9999f-139">-SshKeyValue</span></span>
<span data-ttu-id="9999f-140">SSH-Schlüsseldatei Wert oder Schlüssel Dateipfad.</span><span class="sxs-lookup"><span data-stu-id="9999f-140">SSH key file value or key file path.</span></span>
<span data-ttu-id="9999f-141">Standardmäßig ist {Home}/.ssh/id_rsa. pub.</span><span class="sxs-lookup"><span data-stu-id="9999f-141">Defaults to {HOME}/.ssh/id_rsa.pub.</span></span>

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

### <span data-ttu-id="9999f-142">-Tag</span><span class="sxs-lookup"><span data-stu-id="9999f-142">-Tag</span></span>
<span data-ttu-id="9999f-143">Tags, die auf die Ressource angewendet werden sollen</span><span class="sxs-lookup"><span data-stu-id="9999f-143">Tags to be applied to the resource</span></span>

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

### <span data-ttu-id="9999f-144">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="9999f-144">-Confirm</span></span>
<span data-ttu-id="9999f-145">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9999f-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9999f-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9999f-146">-WhatIf</span></span>
<span data-ttu-id="9999f-147">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9999f-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9999f-148">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9999f-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9999f-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9999f-149">CommonParameters</span></span>
<span data-ttu-id="9999f-150">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9999f-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9999f-151">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9999f-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9999f-152">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9999f-152">INPUTS</span></span>

### <span data-ttu-id="9999f-153">Keine</span><span class="sxs-lookup"><span data-stu-id="9999f-153">None</span></span>

## <span data-ttu-id="9999f-154">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9999f-154">OUTPUTS</span></span>

### <span data-ttu-id="9999f-155">Microsoft. Azure. Commands. AKS. Models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="9999f-155">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="9999f-156">Notizen</span><span class="sxs-lookup"><span data-stu-id="9999f-156">NOTES</span></span>

## <span data-ttu-id="9999f-157">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9999f-157">RELATED LINKS</span></span>
