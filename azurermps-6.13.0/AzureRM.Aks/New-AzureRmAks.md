---
external help file: Microsoft.Azure.Commands.Aks.dll-Help.xml
Module Name: AzureRM.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.aks/new-azurermaks
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Aks/Commands.Aks/help/New-AzureRmAks.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Aks/Commands.Aks/help/New-AzureRmAks.md
ms.openlocfilehash: f91b4f2afdb1c6aaf7cbac16f952a333d3d362b3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663724"
---
# <span data-ttu-id="d4510-101">New-AzureRmAks</span><span class="sxs-lookup"><span data-stu-id="d4510-101">New-AzureRmAks</span></span>

## <span data-ttu-id="d4510-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d4510-102">SYNOPSIS</span></span>
<span data-ttu-id="d4510-103">Erstellen eines neuen verwalteten Kubernetes-Clusters</span><span class="sxs-lookup"><span data-stu-id="d4510-103">Create a new managed Kubernetes cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d4510-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d4510-104">SYNTAX</span></span>

```
New-AzureRmAks [-Force] [-ResourceGroupName] <String> [-Name] <String> [[-ClientIdAndSecret] <PSCredential>]
 [-Location <String>] [-AdminUserName <String>] [-DnsNamePrefix <String>] [-KubernetesVersion <String>]
 [-NodeCount <Int32>] [-NodeOsDiskSize <Int32>] [-NodeVmSize <String>] [-SshKeyValue <String>] [-AsJob]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d4510-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d4510-105">DESCRIPTION</span></span>

<span data-ttu-id="d4510-106">Erstellen eines neuen verwalteten Kubernetes-Clusters</span><span class="sxs-lookup"><span data-stu-id="d4510-106">Create a new managed Kubernetes cluster.</span></span>

## <span data-ttu-id="d4510-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d4510-107">EXAMPLES</span></span>

### <span data-ttu-id="d4510-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d4510-108">Example 1</span></span>

<span data-ttu-id="d4510-109">Erstellen Sie einen neuen verwalteten Kubernetes-Cluster mit Standard-params.</span><span class="sxs-lookup"><span data-stu-id="d4510-109">Create a new managed Kubernetes cluster with default params.</span></span>

```
PS C:\> New-AzureRmAks -ResourceGroupName group -Name myCluster
```

## <span data-ttu-id="d4510-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="d4510-110">PARAMETERS</span></span>

### <span data-ttu-id="d4510-111">-Nation aus AdminUsername</span><span class="sxs-lookup"><span data-stu-id="d4510-111">-AdminUserName</span></span>
<span data-ttu-id="d4510-112">Benutzername für die virtuellen Linux-Computer.</span><span class="sxs-lookup"><span data-stu-id="d4510-112">User name for the Linux Virtual Machines.</span></span>

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

### <span data-ttu-id="d4510-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d4510-113">-AsJob</span></span>
<span data-ttu-id="d4510-114">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="d4510-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d4510-115">-ClientIdAndSecret</span><span class="sxs-lookup"><span data-stu-id="d4510-115">-ClientIdAndSecret</span></span>
<span data-ttu-id="d4510-116">Die Client-ID und der Client Schlüssel, die dem AAD-Application/Service-Prinzipal zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="d4510-116">The client id and client secret associated with the AAD application / service principal.</span></span>

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

### <span data-ttu-id="d4510-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4510-117">-DefaultProfile</span></span>
<span data-ttu-id="d4510-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d4510-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d4510-119">-DnsNamePrefix</span><span class="sxs-lookup"><span data-stu-id="d4510-119">-DnsNamePrefix</span></span>
<span data-ttu-id="d4510-120">Das DNS-Namenspräfix für den Cluster.</span><span class="sxs-lookup"><span data-stu-id="d4510-120">The DNS name prefix for the cluster.</span></span>

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

### <span data-ttu-id="d4510-121">-Force</span><span class="sxs-lookup"><span data-stu-id="d4510-121">-Force</span></span>
<span data-ttu-id="d4510-122">Erstellen eines Clusters, auch wenn er bereits vorhanden ist</span><span class="sxs-lookup"><span data-stu-id="d4510-122">Create cluster even if it already exists</span></span>

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

### <span data-ttu-id="d4510-123">-KubernetesVersion</span><span class="sxs-lookup"><span data-stu-id="d4510-123">-KubernetesVersion</span></span>
<span data-ttu-id="d4510-124">Die Version von Kubernetes, die zum Erstellen des Clusters verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="d4510-124">The version of Kubernetes to use for creating the cluster.</span></span>

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

### <span data-ttu-id="d4510-125">-Standort</span><span class="sxs-lookup"><span data-stu-id="d4510-125">-Location</span></span>
<span data-ttu-id="d4510-126">Azure-Speicherort für den Cluster.</span><span class="sxs-lookup"><span data-stu-id="d4510-126">Azure location for the cluster.</span></span>
<span data-ttu-id="d4510-127">Standardmäßig wird der Speicherort der Ressourcengruppe verwendet.</span><span class="sxs-lookup"><span data-stu-id="d4510-127">Defaults to the location of the resource group.</span></span>

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

### <span data-ttu-id="d4510-128">-Name</span><span class="sxs-lookup"><span data-stu-id="d4510-128">-Name</span></span>
<span data-ttu-id="d4510-129">Kubernetes verwalteter Cluster Name.</span><span class="sxs-lookup"><span data-stu-id="d4510-129">Kubernetes managed cluster Name.</span></span>

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

### <span data-ttu-id="d4510-130">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="d4510-130">-NodeCount</span></span>
<span data-ttu-id="d4510-131">Die Standardanzahl von Knoten für die Knoten Pools.</span><span class="sxs-lookup"><span data-stu-id="d4510-131">The default number of nodes for the node pools.</span></span>

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

### <span data-ttu-id="d4510-132">-NodeOsDiskSize</span><span class="sxs-lookup"><span data-stu-id="d4510-132">-NodeOsDiskSize</span></span>
<span data-ttu-id="d4510-133">Die Größe der Betriebssystem Diskette für jeden Knoten im Knoten Pool in GB.</span><span class="sxs-lookup"><span data-stu-id="d4510-133">Size in GB of the OS disk for each node in the node pool.</span></span> <span data-ttu-id="d4510-134">Mind. 30 GB.</span><span class="sxs-lookup"><span data-stu-id="d4510-134">Minimum 30 GB.</span></span>

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

### <span data-ttu-id="d4510-135">-NodeVmSize</span><span class="sxs-lookup"><span data-stu-id="d4510-135">-NodeVmSize</span></span>
<span data-ttu-id="d4510-136">Die Größe des virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="d4510-136">The size of the Virtual Machine.</span></span>

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

### <span data-ttu-id="d4510-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4510-137">-ResourceGroupName</span></span>
<span data-ttu-id="d4510-138">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="d4510-138">Resource Group Name.</span></span>

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

### <span data-ttu-id="d4510-139">-SshKeyValue</span><span class="sxs-lookup"><span data-stu-id="d4510-139">-SshKeyValue</span></span>
<span data-ttu-id="d4510-140">SSH-Schlüsseldatei Wert oder Schlüssel Dateipfad.</span><span class="sxs-lookup"><span data-stu-id="d4510-140">SSH key file value or key file path.</span></span>
<span data-ttu-id="d4510-141">Standardmäßig ist {Home}/.ssh/id_rsa. pub.</span><span class="sxs-lookup"><span data-stu-id="d4510-141">Defaults to {HOME}/.ssh/id_rsa.pub.</span></span>

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

### <span data-ttu-id="d4510-142">-Tag</span><span class="sxs-lookup"><span data-stu-id="d4510-142">-Tag</span></span>
<span data-ttu-id="d4510-143">Tags, die auf die Ressource angewendet werden sollen</span><span class="sxs-lookup"><span data-stu-id="d4510-143">Tags to be applied to the resource</span></span>

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

### <span data-ttu-id="d4510-144">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d4510-144">-Confirm</span></span>
<span data-ttu-id="d4510-145">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d4510-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d4510-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d4510-146">-WhatIf</span></span>
<span data-ttu-id="d4510-147">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d4510-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d4510-148">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d4510-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d4510-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4510-149">CommonParameters</span></span>
<span data-ttu-id="d4510-150">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d4510-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4510-151">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d4510-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4510-152">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d4510-152">INPUTS</span></span>

### <span data-ttu-id="d4510-153">Keine</span><span class="sxs-lookup"><span data-stu-id="d4510-153">None</span></span>

## <span data-ttu-id="d4510-154">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d4510-154">OUTPUTS</span></span>

### <span data-ttu-id="d4510-155">Microsoft. Azure. Commands. AKS. Models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="d4510-155">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="d4510-156">Notizen</span><span class="sxs-lookup"><span data-stu-id="d4510-156">NOTES</span></span>

## <span data-ttu-id="d4510-157">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d4510-157">RELATED LINKS</span></span>
