---
external help file: Microsoft.Azure.Commands.Aks.dll-Help.xml
Module Name: AzureRM.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.aks/new-azurermaks
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Aks/Commands.Aks/help/New-AzureRmAks.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Aks/Commands.Aks/help/New-AzureRmAks.md
ms.openlocfilehash: ed68271ae29c7af0219fa08d1c342b636d7d3fbd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664706"
---
# <span data-ttu-id="cfce3-101">New-AzureRmAks</span><span class="sxs-lookup"><span data-stu-id="cfce3-101">New-AzureRmAks</span></span>

## <span data-ttu-id="cfce3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="cfce3-102">SYNOPSIS</span></span>
<span data-ttu-id="cfce3-103">Erstellen eines neuen verwalteten Kubernetes-Clusters</span><span class="sxs-lookup"><span data-stu-id="cfce3-103">Create a new managed Kubernetes cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cfce3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="cfce3-104">SYNTAX</span></span>

```
New-AzureRmAks [-ResourceGroupName] <String> [-Name] <String> [[-ClientIdAndSecret] <PSCredential>]
 [-Location <String>] [-AdminUserName <String>] [-DnsNamePrefix <String>] [-KubernetesVersion <String>]
 [-NodeCount <Int32>] [-NodeOsDiskSize <Int32>] [-NodeVmSize <String>] [-SshKeyValue <String>] [-Force] [-AsJob]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cfce3-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cfce3-105">DESCRIPTION</span></span>
<span data-ttu-id="cfce3-106">Erstellen eines neuen verwalteten Kubernetes-Clusters</span><span class="sxs-lookup"><span data-stu-id="cfce3-106">Create a new managed Kubernetes cluster.</span></span>

## <span data-ttu-id="cfce3-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="cfce3-107">EXAMPLES</span></span>

### <span data-ttu-id="cfce3-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="cfce3-108">Example 1</span></span>
<span data-ttu-id="cfce3-109">Erstellen eines neuen verwalteten Kubernetes-Clusters mit Standard-params</span><span class="sxs-lookup"><span data-stu-id="cfce3-109">Create a new managed Kubernetes cluster with default params</span></span>

```
PS C:\> New-AzureRmAks -ResourceGroupName group -Name myCluster
```

## <span data-ttu-id="cfce3-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="cfce3-110">PARAMETERS</span></span>

### <span data-ttu-id="cfce3-111">-Nation aus AdminUsername</span><span class="sxs-lookup"><span data-stu-id="cfce3-111">-AdminUserName</span></span>
<span data-ttu-id="cfce3-112">Benutzername für die virtuellen Linux-Computer.</span><span class="sxs-lookup"><span data-stu-id="cfce3-112">User name for the Linux Virtual Machines.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cfce3-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cfce3-113">-AsJob</span></span>
<span data-ttu-id="cfce3-114">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="cfce3-114">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cfce3-115">-ClientIdAndSecret</span><span class="sxs-lookup"><span data-stu-id="cfce3-115">-ClientIdAndSecret</span></span>
<span data-ttu-id="cfce3-116">Die Client-ID und der Client Schlüssel, die dem AAD-Application/Service-Prinzipal zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="cfce3-116">The client id and client secret associated with the AAD application / service principal.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cfce3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cfce3-117">-DefaultProfile</span></span>
<span data-ttu-id="cfce3-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="cfce3-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cfce3-119">-DnsNamePrefix</span><span class="sxs-lookup"><span data-stu-id="cfce3-119">-DnsNamePrefix</span></span>
<span data-ttu-id="cfce3-120">Das DNS-Namenspräfix für den Cluster.</span><span class="sxs-lookup"><span data-stu-id="cfce3-120">The DNS name prefix for the cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cfce3-121">-Force</span><span class="sxs-lookup"><span data-stu-id="cfce3-121">-Force</span></span>
<span data-ttu-id="cfce3-122">Erstellen eines Clusters, auch wenn er bereits vorhanden ist</span><span class="sxs-lookup"><span data-stu-id="cfce3-122">Create cluster even if it already exists</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cfce3-123">-KubernetesVersion</span><span class="sxs-lookup"><span data-stu-id="cfce3-123">-KubernetesVersion</span></span>
<span data-ttu-id="cfce3-124">Die Version von Kubernetes, die zum Erstellen des Clusters verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="cfce3-124">The version of Kubernetes to use for creating the cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cfce3-125">-Standort</span><span class="sxs-lookup"><span data-stu-id="cfce3-125">-Location</span></span>
<span data-ttu-id="cfce3-126">Azure-Speicherort für den Cluster.</span><span class="sxs-lookup"><span data-stu-id="cfce3-126">Azure location for the cluster.</span></span>
<span data-ttu-id="cfce3-127">Standardmäßig wird der Speicherort der Ressourcengruppe verwendet.</span><span class="sxs-lookup"><span data-stu-id="cfce3-127">Defaults to the location of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cfce3-128">-Name</span><span class="sxs-lookup"><span data-stu-id="cfce3-128">-Name</span></span>
<span data-ttu-id="cfce3-129">Kubernetes verwalteter Cluster Name.</span><span class="sxs-lookup"><span data-stu-id="cfce3-129">Kubernetes managed cluster Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cfce3-130">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="cfce3-130">-NodeCount</span></span>
<span data-ttu-id="cfce3-131">Die Standardanzahl von Knoten für die Knoten Pools.</span><span class="sxs-lookup"><span data-stu-id="cfce3-131">The default number of nodes for the node pools.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cfce3-132">-NodeOsDiskSize</span><span class="sxs-lookup"><span data-stu-id="cfce3-132">-NodeOsDiskSize</span></span>
<span data-ttu-id="cfce3-133">Die Standardanzahl von Knoten für die Knoten Pools.</span><span class="sxs-lookup"><span data-stu-id="cfce3-133">The default number of nodes for the node pools.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cfce3-134">-NodeVmSize</span><span class="sxs-lookup"><span data-stu-id="cfce3-134">-NodeVmSize</span></span>
<span data-ttu-id="cfce3-135">Die Größe des virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="cfce3-135">The size of the Virtual Machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cfce3-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cfce3-136">-ResourceGroupName</span></span>
<span data-ttu-id="cfce3-137">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="cfce3-137">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cfce3-138">-SshKeyValue</span><span class="sxs-lookup"><span data-stu-id="cfce3-138">-SshKeyValue</span></span>
<span data-ttu-id="cfce3-139">SSH-Schlüsseldatei Wert oder Schlüssel Dateipfad.</span><span class="sxs-lookup"><span data-stu-id="cfce3-139">SSH key file value or key file path.</span></span>
<span data-ttu-id="cfce3-140">Standardmäßig ist {Home}/.ssh/id_rsa. pub.</span><span class="sxs-lookup"><span data-stu-id="cfce3-140">Defaults to {HOME}/.ssh/id_rsa.pub.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SshKeyPath

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cfce3-141">-Tag</span><span class="sxs-lookup"><span data-stu-id="cfce3-141">-Tag</span></span>
<span data-ttu-id="cfce3-142">Tags, die auf die Ressource angewendet werden sollen</span><span class="sxs-lookup"><span data-stu-id="cfce3-142">Tags to be applied to the resource</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cfce3-143">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="cfce3-143">-Confirm</span></span>
<span data-ttu-id="cfce3-144">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="cfce3-144">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cfce3-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cfce3-145">-WhatIf</span></span>
<span data-ttu-id="cfce3-146">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="cfce3-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cfce3-147">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="cfce3-147">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cfce3-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cfce3-148">CommonParameters</span></span>
<span data-ttu-id="cfce3-149">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cfce3-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cfce3-150">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cfce3-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cfce3-151">Eingaben</span><span class="sxs-lookup"><span data-stu-id="cfce3-151">INPUTS</span></span>

### <span data-ttu-id="cfce3-152">Keine</span><span class="sxs-lookup"><span data-stu-id="cfce3-152">None</span></span>

## <span data-ttu-id="cfce3-153">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="cfce3-153">OUTPUTS</span></span>

### <span data-ttu-id="cfce3-154">Microsoft. Azure. Commands. AKS. Models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="cfce3-154">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="cfce3-155">Notizen</span><span class="sxs-lookup"><span data-stu-id="cfce3-155">NOTES</span></span>

## <span data-ttu-id="cfce3-156">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="cfce3-156">RELATED LINKS</span></span>
