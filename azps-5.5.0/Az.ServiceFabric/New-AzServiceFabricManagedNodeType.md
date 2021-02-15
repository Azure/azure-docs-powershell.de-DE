---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/new-azservicefabricmanagednodetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricManagedNodeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricManagedNodeType.md
ms.openlocfilehash: 3e89e807acfb2507834686574931011bf398c76c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100173945"
---
# <span data-ttu-id="04890-101">New-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="04890-101">New-AzServiceFabricManagedNodeType</span></span>

## <span data-ttu-id="04890-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="04890-102">SYNOPSIS</span></span>
<span data-ttu-id="04890-103">Erstellen sie eine neue Knotentypressource.</span><span class="sxs-lookup"><span data-stu-id="04890-103">Create new node type resource.</span></span>

## <span data-ttu-id="04890-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="04890-104">SYNTAX</span></span>

```
New-AzServiceFabricManagedNodeType [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 -InstanceCount <Int32> [-Primary] [-DiskSize <Int32>] [-ApplicationStartPort <Int32>]
 [-ApplicationEndPort <Int32>] [-EphemeralStartPort <Int32>] [-EphemeralEndPort <Int32>] [-VmSize <String>]
 [-VmImagePublisher <String>] [-VmImageOffer <String>] [-VmImageSku <String>] [-VmImageVersion <String>]
 [-Capacity <Hashtable>] [-PlacementProperty <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="04890-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="04890-105">DESCRIPTION</span></span>
<span data-ttu-id="04890-106">Erstellen Sie eine neue Knotentypressource für einen bestimmten Cluster.</span><span class="sxs-lookup"><span data-stu-id="04890-106">Create new node type resource for an specific cluster.</span></span>

## <span data-ttu-id="04890-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="04890-107">EXAMPLES</span></span>

### <span data-ttu-id="04890-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="04890-108">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
New-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -Name $NodeTypeName -Primary -InstanceCount 3
```

<span data-ttu-id="04890-109">Erstellen Sie den primären Knotentyp mit drei Knoten.</span><span class="sxs-lookup"><span data-stu-id="04890-109">Create primary node type with 3 nodes.</span></span>

### <span data-ttu-id="04890-110">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="04890-110">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
New-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -Name $NodeTypeName -InstanceCount 5 -Primary -PlacementProperty @{NodeColor="Green";SomeProperty="5";} -Capacity @{ClientConnections="65536";} -ApplicationStartPort 20575 -ApplicationEndPort 20605 -EphemeralStartPort 20606 -EphemeralEndPort 20861
```

<span data-ttu-id="04890-111">Erstellen Sie einen primären Knotentyp mit 5 Knoten, und geben Sie Platzierungseigenschaften, Kapazitäten, Anwendungs- und kurzlebige Ports an.</span><span class="sxs-lookup"><span data-stu-id="04890-111">Create primary node type with 5 nodes and specifying placement properties, capacities, application and ephemeral ports.</span></span>

## <span data-ttu-id="04890-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="04890-112">PARAMETERS</span></span>

### <span data-ttu-id="04890-113">-ApplicationEndPort</span><span class="sxs-lookup"><span data-stu-id="04890-113">-ApplicationEndPort</span></span>
<span data-ttu-id="04890-114">Anwendungsendport einer Reihe von Ports.</span><span class="sxs-lookup"><span data-stu-id="04890-114">Application End port of a range of ports.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04890-115">-ApplicationStartPort</span><span class="sxs-lookup"><span data-stu-id="04890-115">-ApplicationStartPort</span></span>
<span data-ttu-id="04890-116">Anwendungsstartport einer Reihe von Ports</span><span class="sxs-lookup"><span data-stu-id="04890-116">Application start port of a range of ports.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04890-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="04890-117">-AsJob</span></span>
<span data-ttu-id="04890-118">Führen Sie das Cmdlet im Hintergrund aus, und geben Sie einen Auftrag zurück, um den Fortschritt nachverfolgt zu können.</span><span class="sxs-lookup"><span data-stu-id="04890-118">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="04890-119">-Capacity</span><span class="sxs-lookup"><span data-stu-id="04890-119">-Capacity</span></span>
<span data-ttu-id="04890-120">Auf die Knoten im Knotentyp als Schlüssel/Wert-Paare angewendete Kapazitätstags verwendet der Clusterressourcen-Manager diese Tags, um zu verstehen, wie viel Ressourcen ein Knoten enthält.</span><span class="sxs-lookup"><span data-stu-id="04890-120">Capacity tags applied to the nodes in the node type as key/value pairs, the cluster resource manager uses these tags to understand how much resource a node has.</span></span>
<span data-ttu-id="04890-121">Durch das Aktualisieren dieser Einstellung werden die aktuellen Werte überschrieben.</span><span class="sxs-lookup"><span data-stu-id="04890-121">Updating this will override the current values.</span></span>

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

### <span data-ttu-id="04890-122">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="04890-122">-ClusterName</span></span>
<span data-ttu-id="04890-123">Geben Sie den Namen des Cluster an.</span><span class="sxs-lookup"><span data-stu-id="04890-123">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="04890-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04890-124">-DefaultProfile</span></span>
<span data-ttu-id="04890-125">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="04890-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="04890-126">-DiskSize</span><span class="sxs-lookup"><span data-stu-id="04890-126">-DiskSize</span></span>
<span data-ttu-id="04890-127">Datenträgergröße für jede vm im Knotentyp in GBs.</span><span class="sxs-lookup"><span data-stu-id="04890-127">Disk size for each vm in the node type in GBs.</span></span>
<span data-ttu-id="04890-128">Standard 100.</span><span class="sxs-lookup"><span data-stu-id="04890-128">Default 100.</span></span>

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

### <span data-ttu-id="04890-129">-EphemeralEndPort</span><span class="sxs-lookup"><span data-stu-id="04890-129">-EphemeralEndPort</span></span>
<span data-ttu-id="04890-130">Kurzlebiger Endport eines Portsbereichs.</span><span class="sxs-lookup"><span data-stu-id="04890-130">Ephemeral end port of a range of ports.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04890-131">-EphemeralStartPort</span><span class="sxs-lookup"><span data-stu-id="04890-131">-EphemeralStartPort</span></span>
<span data-ttu-id="04890-132">Kurzlebiger Startport eines Portsbereichs.</span><span class="sxs-lookup"><span data-stu-id="04890-132">Ephemeral start port of a range of ports.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04890-133">-InstanceCount</span><span class="sxs-lookup"><span data-stu-id="04890-133">-InstanceCount</span></span>
<span data-ttu-id="04890-134">Die Anzahl der Knoten im Knotentyp.</span><span class="sxs-lookup"><span data-stu-id="04890-134">The number of nodes in the node type.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04890-135">-Name</span><span class="sxs-lookup"><span data-stu-id="04890-135">-Name</span></span>
<span data-ttu-id="04890-136">Geben Sie den Namen des Knotentyps an.</span><span class="sxs-lookup"><span data-stu-id="04890-136">Specify the name of the node type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NodeTypeName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="04890-137">-PlacementProperty</span><span class="sxs-lookup"><span data-stu-id="04890-137">-PlacementProperty</span></span>
<span data-ttu-id="04890-138">Placement tags applied to nodes in the node type as key/value pairs, which can be used to indicate where certain services (workload) should run.</span><span class="sxs-lookup"><span data-stu-id="04890-138">Placement tags applied to nodes in the node type as key/value pairs, which can be used to indicate where certain services (workload) should run.</span></span>
<span data-ttu-id="04890-139">Durch das Aktualisieren dieser Einstellung werden die aktuellen Werte überschrieben.</span><span class="sxs-lookup"><span data-stu-id="04890-139">Updating this will override the current values.</span></span>

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

### <span data-ttu-id="04890-140">-Primary</span><span class="sxs-lookup"><span data-stu-id="04890-140">-Primary</span></span>
<span data-ttu-id="04890-141">Geben Sie an, ob der Knotentyp primär ist.</span><span class="sxs-lookup"><span data-stu-id="04890-141">Specify if the node type is primary.</span></span>
<span data-ttu-id="04890-142">Auf diesem Knotentyp werden Systemdienste ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="04890-142">On this node type will run system services.</span></span>
<span data-ttu-id="04890-143">Nur ein Knotentyp sollte als primär markiert werden.</span><span class="sxs-lookup"><span data-stu-id="04890-143">Only one node type should be marked as primary.</span></span>
<span data-ttu-id="04890-144">Der primäre Knotentyp kann für vorhandene Cluster nicht gelöscht oder geändert werden.</span><span class="sxs-lookup"><span data-stu-id="04890-144">Primary node type cannot be deleted or changed for existing clusters.</span></span>

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

### <span data-ttu-id="04890-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="04890-145">-ResourceGroupName</span></span>
<span data-ttu-id="04890-146">Geben Sie den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="04890-146">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="04890-147">-VmImageOffer</span><span class="sxs-lookup"><span data-stu-id="04890-147">-VmImageOffer</span></span>
<span data-ttu-id="04890-148">Der Angebotstyp des Azure Virtual Machines Marketplace-Bilds.</span><span class="sxs-lookup"><span data-stu-id="04890-148">The offer type of the Azure Virtual Machines Marketplace image.</span></span>
<span data-ttu-id="04890-149">Standard: WindowsServer.</span><span class="sxs-lookup"><span data-stu-id="04890-149">Default: WindowsServer.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: "WindowsServer"
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04890-150">-VmImagePublisher</span><span class="sxs-lookup"><span data-stu-id="04890-150">-VmImagePublisher</span></span>
<span data-ttu-id="04890-151">Der Herausgeber des Azure Virtual Machines Marketplace-Bilds.</span><span class="sxs-lookup"><span data-stu-id="04890-151">The publisher of the Azure Virtual Machines Marketplace image.</span></span>
<span data-ttu-id="04890-152">Standard: MicrosoftWindowsServer.</span><span class="sxs-lookup"><span data-stu-id="04890-152">Default: MicrosoftWindowsServer.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: "MicrosoftWindowsServer"
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04890-153">-VmImageSku</span><span class="sxs-lookup"><span data-stu-id="04890-153">-VmImageSku</span></span>
<span data-ttu-id="04890-154">Die SKU des Azure Virtual Machines Marketplace-Bilds.</span><span class="sxs-lookup"><span data-stu-id="04890-154">The SKU of the Azure Virtual Machines Marketplace image.</span></span>
<span data-ttu-id="04890-155">Standard: 2019-Rechenzentrum.</span><span class="sxs-lookup"><span data-stu-id="04890-155">Default: 2019-Datacenter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: "2019-Datacenter"
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04890-156">-VmImageVersion</span><span class="sxs-lookup"><span data-stu-id="04890-156">-VmImageVersion</span></span>
<span data-ttu-id="04890-157">Die Version des Azure Virtual Machines Marketplace-Bilds.</span><span class="sxs-lookup"><span data-stu-id="04890-157">The version of the Azure Virtual Machines Marketplace image.</span></span>
<span data-ttu-id="04890-158">Standard: neueste Version.</span><span class="sxs-lookup"><span data-stu-id="04890-158">Default: latest.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: "latest"
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04890-159">-VmSize</span><span class="sxs-lookup"><span data-stu-id="04890-159">-VmSize</span></span>
<span data-ttu-id="04890-160">Die Größe virtueller Computer im Pool.</span><span class="sxs-lookup"><span data-stu-id="04890-160">The size of virtual machines in the pool.</span></span>
<span data-ttu-id="04890-161">Alle virtuellen Computer in einem Pool haben die gleiche Größe.</span><span class="sxs-lookup"><span data-stu-id="04890-161">All virtual machines in a pool are the same size.</span></span>
<span data-ttu-id="04890-162">Standard: Standard_D2.</span><span class="sxs-lookup"><span data-stu-id="04890-162">Default: Standard_D2.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: "Standard_D2"
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04890-163">-Confirm</span><span class="sxs-lookup"><span data-stu-id="04890-163">-Confirm</span></span>
<span data-ttu-id="04890-164">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="04890-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="04890-165">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="04890-165">-WhatIf</span></span>
<span data-ttu-id="04890-166">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="04890-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="04890-167">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="04890-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="04890-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04890-168">CommonParameters</span></span>
<span data-ttu-id="04890-169">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="04890-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04890-170">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="04890-170">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04890-171">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="04890-171">INPUTS</span></span>

### <span data-ttu-id="04890-172">System.String</span><span class="sxs-lookup"><span data-stu-id="04890-172">System.String</span></span>

## <span data-ttu-id="04890-173">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="04890-173">OUTPUTS</span></span>

### <span data-ttu-id="04890-174">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="04890-174">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType</span></span>

## <span data-ttu-id="04890-175">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="04890-175">NOTES</span></span>

## <span data-ttu-id="04890-176">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="04890-176">RELATED LINKS</span></span>
