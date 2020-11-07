---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/new-azaks
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/New-AzAks.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/New-AzAks.md
ms.openlocfilehash: 1de3cef0d14213a52873742f9bf878aaa545e8bf
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93658410"
---
# <span data-ttu-id="d9eb4-101">New-AzAks</span><span class="sxs-lookup"><span data-stu-id="d9eb4-101">New-AzAks</span></span>

## <span data-ttu-id="d9eb4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d9eb4-102">SYNOPSIS</span></span>
<span data-ttu-id="d9eb4-103">Erstellen eines neuen verwalteten Kubernetes-Clusters</span><span class="sxs-lookup"><span data-stu-id="d9eb4-103">Create a new managed Kubernetes cluster.</span></span>

## <span data-ttu-id="d9eb4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d9eb4-104">SYNTAX</span></span>

```
New-AzAks [-Force] [-ResourceGroupName] <String> [-Name] <String> [[-ClientIdAndSecret] <PSCredential>]
 [-Location <String>] [-AdminUserName <String>] [-DnsNamePrefix <String>] [-KubernetesVersion <String>]
 [-NodeCount <Int32>] [-NodeOsDiskSize <Int32>] [-NodeVmSize <String>] [-SshKeyValue <String>] [-AsJob]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d9eb4-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d9eb4-105">DESCRIPTION</span></span>

<span data-ttu-id="d9eb4-106">Erstellen eines neuen verwalteten Kubernetes-Clusters</span><span class="sxs-lookup"><span data-stu-id="d9eb4-106">Create a new managed Kubernetes cluster.</span></span>

## <span data-ttu-id="d9eb4-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d9eb4-107">EXAMPLES</span></span>

### <span data-ttu-id="d9eb4-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d9eb4-108">Example 1</span></span>

<span data-ttu-id="d9eb4-109">Erstellen Sie einen neuen verwalteten Kubernetes-Cluster mit Standard-params.</span><span class="sxs-lookup"><span data-stu-id="d9eb4-109">Create a new managed Kubernetes cluster with default params.</span></span>

```
PS C:\> New-AzAks -ResourceGroupName group -Name myCluster
```

## <span data-ttu-id="d9eb4-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="d9eb4-110">PARAMETERS</span></span>

### <span data-ttu-id="d9eb4-111">-Nation aus AdminUsername</span><span class="sxs-lookup"><span data-stu-id="d9eb4-111">-AdminUserName</span></span>
<span data-ttu-id="d9eb4-112">Benutzername für die virtuellen Linux-Computer.</span><span class="sxs-lookup"><span data-stu-id="d9eb4-112">User name for the Linux Virtual Machines.</span></span>

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

### <span data-ttu-id="d9eb4-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d9eb4-113">-AsJob</span></span>
<span data-ttu-id="d9eb4-114">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="d9eb4-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d9eb4-115">-ClientIdAndSecret</span><span class="sxs-lookup"><span data-stu-id="d9eb4-115">-ClientIdAndSecret</span></span>
<span data-ttu-id="d9eb4-116">Die Client-ID und der Client Schlüssel, die dem AAD-Application/Service-Prinzipal zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="d9eb4-116">The client id and client secret associated with the AAD application / service principal.</span></span>

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

### <span data-ttu-id="d9eb4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9eb4-117">-DefaultProfile</span></span>
<span data-ttu-id="d9eb4-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d9eb4-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d9eb4-119">-DnsNamePrefix</span><span class="sxs-lookup"><span data-stu-id="d9eb4-119">-DnsNamePrefix</span></span>
<span data-ttu-id="d9eb4-120">Das DNS-Namenspräfix für den Cluster.</span><span class="sxs-lookup"><span data-stu-id="d9eb4-120">The DNS name prefix for the cluster.</span></span>

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

### <span data-ttu-id="d9eb4-121">-Force</span><span class="sxs-lookup"><span data-stu-id="d9eb4-121">-Force</span></span>
<span data-ttu-id="d9eb4-122">Erstellen eines Clusters, auch wenn er bereits vorhanden ist</span><span class="sxs-lookup"><span data-stu-id="d9eb4-122">Create cluster even if it already exists</span></span>

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

### <span data-ttu-id="d9eb4-123">-KubernetesVersion</span><span class="sxs-lookup"><span data-stu-id="d9eb4-123">-KubernetesVersion</span></span>
<span data-ttu-id="d9eb4-124">Die Version von Kubernetes, die zum Erstellen des Clusters verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="d9eb4-124">The version of Kubernetes to use for creating the cluster.</span></span>

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

### <span data-ttu-id="d9eb4-125">-Standort</span><span class="sxs-lookup"><span data-stu-id="d9eb4-125">-Location</span></span>
<span data-ttu-id="d9eb4-126">Azure-Speicherort für den Cluster.</span><span class="sxs-lookup"><span data-stu-id="d9eb4-126">Azure location for the cluster.</span></span>
<span data-ttu-id="d9eb4-127">Standardmäßig wird der Speicherort der Ressourcengruppe verwendet.</span><span class="sxs-lookup"><span data-stu-id="d9eb4-127">Defaults to the location of the resource group.</span></span>

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

### <span data-ttu-id="d9eb4-128">-Name</span><span class="sxs-lookup"><span data-stu-id="d9eb4-128">-Name</span></span>
<span data-ttu-id="d9eb4-129">Kubernetes verwalteter Cluster Name.</span><span class="sxs-lookup"><span data-stu-id="d9eb4-129">Kubernetes managed cluster Name.</span></span>

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

### <span data-ttu-id="d9eb4-130">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="d9eb4-130">-NodeCount</span></span>
<span data-ttu-id="d9eb4-131">Die Standardanzahl von Knoten für die Knoten Pools.</span><span class="sxs-lookup"><span data-stu-id="d9eb4-131">The default number of nodes for the node pools.</span></span>

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

### <span data-ttu-id="d9eb4-132">-NodeOsDiskSize</span><span class="sxs-lookup"><span data-stu-id="d9eb4-132">-NodeOsDiskSize</span></span>
<span data-ttu-id="d9eb4-133">Die Größe der Betriebssystem Diskette für jeden Knoten im Knoten Pool in GB.</span><span class="sxs-lookup"><span data-stu-id="d9eb4-133">Size in GB of the OS disk for each node in the node pool.</span></span> <span data-ttu-id="d9eb4-134">Mind. 30 GB.</span><span class="sxs-lookup"><span data-stu-id="d9eb4-134">Minimum 30 GB.</span></span>

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

### <span data-ttu-id="d9eb4-135">-NodeVmSize</span><span class="sxs-lookup"><span data-stu-id="d9eb4-135">-NodeVmSize</span></span>
<span data-ttu-id="d9eb4-136">Die Größe des virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="d9eb4-136">The size of the Virtual Machine.</span></span>

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

### <span data-ttu-id="d9eb4-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d9eb4-137">-ResourceGroupName</span></span>
<span data-ttu-id="d9eb4-138">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="d9eb4-138">Resource Group Name.</span></span>

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

### <span data-ttu-id="d9eb4-139">-SshKeyValue</span><span class="sxs-lookup"><span data-stu-id="d9eb4-139">-SshKeyValue</span></span>
<span data-ttu-id="d9eb4-140">SSH-Schlüsseldatei Wert oder Schlüssel Dateipfad.</span><span class="sxs-lookup"><span data-stu-id="d9eb4-140">SSH key file value or key file path.</span></span>
<span data-ttu-id="d9eb4-141">Standardmäßig ist {Home}/.ssh/id_rsa. pub.</span><span class="sxs-lookup"><span data-stu-id="d9eb4-141">Defaults to {HOME}/.ssh/id_rsa.pub.</span></span>

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

### <span data-ttu-id="d9eb4-142">-Tag</span><span class="sxs-lookup"><span data-stu-id="d9eb4-142">-Tag</span></span>
<span data-ttu-id="d9eb4-143">Tags, die auf die Ressource angewendet werden sollen</span><span class="sxs-lookup"><span data-stu-id="d9eb4-143">Tags to be applied to the resource</span></span>

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

### <span data-ttu-id="d9eb4-144">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d9eb4-144">-Confirm</span></span>
<span data-ttu-id="d9eb4-145">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d9eb4-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d9eb4-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d9eb4-146">-WhatIf</span></span>
<span data-ttu-id="d9eb4-147">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d9eb4-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d9eb4-148">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d9eb4-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d9eb4-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9eb4-149">CommonParameters</span></span>
<span data-ttu-id="d9eb4-150">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9eb4-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9eb4-151">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d9eb4-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9eb4-152">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d9eb4-152">INPUTS</span></span>

### <span data-ttu-id="d9eb4-153">Keine</span><span class="sxs-lookup"><span data-stu-id="d9eb4-153">None</span></span>

## <span data-ttu-id="d9eb4-154">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d9eb4-154">OUTPUTS</span></span>

### <span data-ttu-id="d9eb4-155">Microsoft. Azure. Commands. AKS. Models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="d9eb4-155">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="d9eb4-156">Notizen</span><span class="sxs-lookup"><span data-stu-id="d9eb4-156">NOTES</span></span>

## <span data-ttu-id="d9eb4-157">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d9eb4-157">RELATED LINKS</span></span>
