---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/set-azservicefabricmanagedcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Set-AzServiceFabricManagedCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Set-AzServiceFabricManagedCluster.md
ms.openlocfilehash: 4636dc8f8c8efdf9dae5f7d2094fd3432528f043
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98471771"
---
# <span data-ttu-id="cfdd5-101">Set-AzServiceFabricManagedCluster</span><span class="sxs-lookup"><span data-stu-id="cfdd5-101">Set-AzServiceFabricManagedCluster</span></span>

## <span data-ttu-id="cfdd5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cfdd5-102">SYNOPSIS</span></span>
<span data-ttu-id="cfdd5-103">Legen Sie Clusterressourceneigenschaften festgelegt.</span><span class="sxs-lookup"><span data-stu-id="cfdd5-103">Set cluster resource properties.</span></span>

## <span data-ttu-id="cfdd5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cfdd5-104">SYNTAX</span></span>

### <span data-ttu-id="cfdd5-105">ByObj (Standard)</span><span class="sxs-lookup"><span data-stu-id="cfdd5-105">ByObj (Default)</span></span>
```
Set-AzServiceFabricManagedCluster [-InputObject] <PSManagedCluster> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cfdd5-106">WithPramsByName</span><span class="sxs-lookup"><span data-stu-id="cfdd5-106">WithPramsByName</span></span>
```
Set-AzServiceFabricManagedCluster [-ResourceGroupName] <String> [-Name] <String>
 [-UpgradeMode <ClusterUpgradeMode>] [-CodeVersion <String>] [-HttpGatewayConnectionPort <Int32>]
 [-ClientConnectionPort <Int32>] [-DnsName <String>] [-ReverseProxyEndpointPort <Int32>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cfdd5-107">ByNameById</span><span class="sxs-lookup"><span data-stu-id="cfdd5-107">ByNameById</span></span>
```
Set-AzServiceFabricManagedCluster [-ResourceId] <String> [-UpgradeMode <ClusterUpgradeMode>]
 [-CodeVersion <String>] [-HttpGatewayConnectionPort <Int32>] [-ClientConnectionPort <Int32>]
 [-DnsName <String>] [-ReverseProxyEndpointPort <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cfdd5-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="cfdd5-108">DESCRIPTION</span></span>
<span data-ttu-id="cfdd5-109">Legen Sie Clusterressourceneigenschaften festgelegt.</span><span class="sxs-lookup"><span data-stu-id="cfdd5-109">Set cluster resource properties.</span></span>

## <span data-ttu-id="cfdd5-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="cfdd5-110">EXAMPLES</span></span>

### <span data-ttu-id="cfdd5-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="cfdd5-111">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
Update-AzServiceFabricManagedCluster -ResourceGroupName $rgName -Name $clusterName -DnsName testnewdns -ClientConnectionPort 50000 -Verbose
```

<span data-ttu-id="cfdd5-112">Aktualisieren Sie den Dnsnamen und den Clientverbindungsport für den Cluster.</span><span class="sxs-lookup"><span data-stu-id="cfdd5-112">Update dns name and client connection port for the cluster.</span></span>

### <span data-ttu-id="cfdd5-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="cfdd5-113">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$cluster = Get-AzServiceFabricManagedCluster -ResourceGroupName $rgName -Name $clusterName

$cluster.DnsName = "testnewdns"
$cluster.ClientConnectionPort = 50000
$cluster | Set-AzServiceFabricManagedCluster
```

<span data-ttu-id="cfdd5-114">Aktualisieren Sie den Dnsnamen und den Clientverbindungsport für den Cluster mit Piping.</span><span class="sxs-lookup"><span data-stu-id="cfdd5-114">Update dns name and client connection port for the cluster, with piping.</span></span>

## <span data-ttu-id="cfdd5-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cfdd5-115">PARAMETERS</span></span>

### <span data-ttu-id="cfdd5-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cfdd5-116">-AsJob</span></span>
<span data-ttu-id="cfdd5-117">Führen Sie das Cmdlet im Hintergrund aus, und geben Sie einen Auftrag zurück, um den Fortschritt nachverfolgt zu können.</span><span class="sxs-lookup"><span data-stu-id="cfdd5-117">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="cfdd5-118">-ClientConnectionPort</span><span class="sxs-lookup"><span data-stu-id="cfdd5-118">-ClientConnectionPort</span></span>
<span data-ttu-id="cfdd5-119">Port, der für Clientverbindungen zum Cluster verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="cfdd5-119">Port used for client connections to the cluster.</span></span> <span data-ttu-id="cfdd5-120">Standard: 19000.</span><span class="sxs-lookup"><span data-stu-id="cfdd5-120">Default: 19000.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: WithPramsByName, ByNameById
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cfdd5-121">-CodeVersion</span><span class="sxs-lookup"><span data-stu-id="cfdd5-121">-CodeVersion</span></span>
<span data-ttu-id="cfdd5-122">Clustercodeversion.</span><span class="sxs-lookup"><span data-stu-id="cfdd5-122">Cluster code version.</span></span> <span data-ttu-id="cfdd5-123">Wird nur verwendet, wenn der Upgrademodus manuell ist.</span><span class="sxs-lookup"><span data-stu-id="cfdd5-123">Only use if upgrade mode is Manual.</span></span>

```yaml
Type: System.String
Parameter Sets: WithPramsByName, ByNameById
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cfdd5-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cfdd5-124">-DefaultProfile</span></span>
<span data-ttu-id="cfdd5-125">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="cfdd5-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cfdd5-126">-DnsName</span><span class="sxs-lookup"><span data-stu-id="cfdd5-126">-DnsName</span></span>
<span data-ttu-id="cfdd5-127">Dns-Name des Clusters.</span><span class="sxs-lookup"><span data-stu-id="cfdd5-127">Cluster's dns name.</span></span>

```yaml
Type: System.String
Parameter Sets: WithPramsByName, ByNameById
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cfdd5-128">-HttpGatewayConnectionPort</span><span class="sxs-lookup"><span data-stu-id="cfdd5-128">-HttpGatewayConnectionPort</span></span>
<span data-ttu-id="cfdd5-129">Port, der für http-Verbindungen mit dem Cluster verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="cfdd5-129">Port used for http connections to the cluster.</span></span> <span data-ttu-id="cfdd5-130">Standard: 19080.</span><span class="sxs-lookup"><span data-stu-id="cfdd5-130">Default: 19080.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: WithPramsByName, ByNameById
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cfdd5-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cfdd5-131">-InputObject</span></span>
<span data-ttu-id="cfdd5-132">Verwaltete Clusterressource</span><span class="sxs-lookup"><span data-stu-id="cfdd5-132">Managed Cluster resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedCluster
Parameter Sets: ByObj
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cfdd5-133">-Name</span><span class="sxs-lookup"><span data-stu-id="cfdd5-133">-Name</span></span>
<span data-ttu-id="cfdd5-134">Geben Sie den Namen des Cluster an.</span><span class="sxs-lookup"><span data-stu-id="cfdd5-134">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: WithPramsByName
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cfdd5-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cfdd5-135">-ResourceGroupName</span></span>
<span data-ttu-id="cfdd5-136">Geben Sie den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="cfdd5-136">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: WithPramsByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cfdd5-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cfdd5-137">-ResourceId</span></span>
<span data-ttu-id="cfdd5-138">Ressourcen-ID des verwalteten Clusters</span><span class="sxs-lookup"><span data-stu-id="cfdd5-138">Managed Cluster resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameById
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cfdd5-139">-ReverseProxyEndpointPort</span><span class="sxs-lookup"><span data-stu-id="cfdd5-139">-ReverseProxyEndpointPort</span></span>
<span data-ttu-id="cfdd5-140">Endpunkt, der vom Reverseproxy verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="cfdd5-140">Endpoint used by reverse proxy.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: WithPramsByName, ByNameById
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cfdd5-141">-UpgradeMode</span><span class="sxs-lookup"><span data-stu-id="cfdd5-141">-UpgradeMode</span></span>
<span data-ttu-id="cfdd5-142">Upgrademodus für Clustercodeversion.</span><span class="sxs-lookup"><span data-stu-id="cfdd5-142">Cluster code version upgrade mode.</span></span> <span data-ttu-id="cfdd5-143">Automatisch oder manuell</span><span class="sxs-lookup"><span data-stu-id="cfdd5-143">Automatic or Manual.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ServiceFabric.Models.ClusterUpgradeMode]
Parameter Sets: WithPramsByName, ByNameById
Aliases:
Accepted values: Automatic, Manual

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cfdd5-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cfdd5-144">-Confirm</span></span>
<span data-ttu-id="cfdd5-145">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="cfdd5-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cfdd5-146">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="cfdd5-146">-WhatIf</span></span>
<span data-ttu-id="cfdd5-147">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="cfdd5-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cfdd5-148">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="cfdd5-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cfdd5-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cfdd5-149">CommonParameters</span></span>
<span data-ttu-id="cfdd5-150">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cfdd5-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cfdd5-151">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cfdd5-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cfdd5-152">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="cfdd5-152">INPUTS</span></span>

### <span data-ttu-id="cfdd5-153">System.String</span><span class="sxs-lookup"><span data-stu-id="cfdd5-153">System.String</span></span>

## <span data-ttu-id="cfdd5-154">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="cfdd5-154">OUTPUTS</span></span>

### <span data-ttu-id="cfdd5-155">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedCluster</span><span class="sxs-lookup"><span data-stu-id="cfdd5-155">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedCluster</span></span>

## <span data-ttu-id="cfdd5-156">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="cfdd5-156">NOTES</span></span>

## <span data-ttu-id="cfdd5-157">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="cfdd5-157">RELATED LINKS</span></span>
