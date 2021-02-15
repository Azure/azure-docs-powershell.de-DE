---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/new-azservicefabricmanagedcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricManagedCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricManagedCluster.md
ms.openlocfilehash: 9dd54f0f1ca56a8bedf3550e238a4308b519925d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100173948"
---
# <span data-ttu-id="f6465-101">New-AzServiceFabricManagedCluster</span><span class="sxs-lookup"><span data-stu-id="f6465-101">New-AzServiceFabricManagedCluster</span></span>

## <span data-ttu-id="f6465-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f6465-102">SYNOPSIS</span></span>
<span data-ttu-id="f6465-103">Erstellen sie einen neuen verwalteten Cluster.</span><span class="sxs-lookup"><span data-stu-id="f6465-103">Create new managed cluster.</span></span>

## <span data-ttu-id="f6465-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f6465-104">SYNTAX</span></span>

### <span data-ttu-id="f6465-105">ClientCertByTp (Standard)</span><span class="sxs-lookup"><span data-stu-id="f6465-105">ClientCertByTp (Default)</span></span>
```
New-AzServiceFabricManagedCluster [-ResourceGroupName] <String> [-Name] <String> -Location <String>
 [-UpgradeMode <ClusterUpgradeMode>] [-CodeVersion <String>] [-ClientCertIsAdmin]
 -ClientCertThumbprint <String> -AdminPassword <SecureString> [-AdminUserName <String>]
 [-HttpGatewayConnectionPort <Int32>] [-ClientConnectionPort <Int32>] [-DnsName <String>]
 [-ReverseProxyEndpointPort <Int32>] [-Sku <ManagedClusterSku>] [-UseTestExtension] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f6465-106">ClientCertByCn</span><span class="sxs-lookup"><span data-stu-id="f6465-106">ClientCertByCn</span></span>
```
New-AzServiceFabricManagedCluster [-ResourceGroupName] <String> [-Name] <String> -Location <String>
 [-UpgradeMode <ClusterUpgradeMode>] [-CodeVersion <String>] [-ClientCertIsAdmin]
 -ClientCertCommonName <String> [-ClientCertIssuerThumbprint <String[]>] -AdminPassword <SecureString>
 [-AdminUserName <String>] [-HttpGatewayConnectionPort <Int32>] [-ClientConnectionPort <Int32>]
 [-DnsName <String>] [-ReverseProxyEndpointPort <Int32>] [-Sku <ManagedClusterSku>] [-UseTestExtension]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f6465-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f6465-107">DESCRIPTION</span></span>
<span data-ttu-id="f6465-108">Mit diesem Cmdlet wird eine verwaltete Clusterressource ohne Knotentypen erstellt.</span><span class="sxs-lookup"><span data-stu-id="f6465-108">This cmdlet will create a managed cluster resource without node types.</span></span> <span data-ttu-id="f6465-109">Zum Bootstrapen des Cluster muss ein primärer Knotentyp hinzugefügt werden. Verwenden Sie ["New-AzServiceFabricManagedNodeType".](./New-AzServiceFabricManagedNodeType.md)</span><span class="sxs-lookup"><span data-stu-id="f6465-109">To bootstrap the cluster A primary node type needs to be added use [New-AzServiceFabricManagedNodeType](./New-AzServiceFabricManagedNodeType.md).</span></span>

## <span data-ttu-id="f6465-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f6465-110">EXAMPLES</span></span>

### <span data-ttu-id="f6465-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f6465-111">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$password = ConvertTo-SecureString -AsPlainText -Force "testpass1234!@#$"
New-AzServiceFabricManagedCluster -ResourceGroupName $rgName -Location centraluseuap -ClusterName $clusterName -AdminPassword $password -Verbose
```

<span data-ttu-id="f6465-112">Mit diesem Befehl wird eine Clusterressource mit einer Standard-SKU erstellt.</span><span class="sxs-lookup"><span data-stu-id="f6465-112">This command creates a cluster resource with default basic sku.</span></span>

### <span data-ttu-id="f6465-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="f6465-113">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$password = ConvertTo-SecureString -AsPlainText -Force "testpass1234!@#$"
New-AzServiceFabricManagedCluster -ResourceGroupName $rgName -Location centraluseuap -ClusterName $clusterName -ClientCertThumbprint XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX -ClientCertIsAdmin -AdminPassword $password -Sku Standard -Verbose
```

<span data-ttu-id="f6465-114">Mit diesem Befehl wird eine Clusterressource in zentraluseuap mit einem anfänglichen Administratorclientzertifikat und einer Standard-SKU erstellt.</span><span class="sxs-lookup"><span data-stu-id="f6465-114">This command creates a cluster resource in centraluseuap with an initial admin client certificate and standard sku.</span></span>

## <span data-ttu-id="f6465-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f6465-115">PARAMETERS</span></span>

### <span data-ttu-id="f6465-116">-AdminPassword</span><span class="sxs-lookup"><span data-stu-id="f6465-116">-AdminPassword</span></span>
<span data-ttu-id="f6465-117">Administratorkennwort für die virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="f6465-117">Admin password used for the virtual machines.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6465-118">-AdminUserName</span><span class="sxs-lookup"><span data-stu-id="f6465-118">-AdminUserName</span></span>
<span data-ttu-id="f6465-119">Administratorkennwort für die virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="f6465-119">Admin password used for the virtual machines.</span></span>
<span data-ttu-id="f6465-120">Standard: vmadmin.</span><span class="sxs-lookup"><span data-stu-id="f6465-120">Default: vmadmin.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: "vmadmin"
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6465-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f6465-121">-AsJob</span></span>
<span data-ttu-id="f6465-122">Führen Sie das Cmdlet im Hintergrund aus, und geben Sie einen Auftrag zurück, um den Fortschritt nachverfolgt zu können.</span><span class="sxs-lookup"><span data-stu-id="f6465-122">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="f6465-123">-ClientCertCommonName</span><span class="sxs-lookup"><span data-stu-id="f6465-123">-ClientCertCommonName</span></span>
<span data-ttu-id="f6465-124">Gemeinsamer Name des Clientzertifikats.</span><span class="sxs-lookup"><span data-stu-id="f6465-124">Client certificate common name.</span></span>

```yaml
Type: System.String
Parameter Sets: ClientCertByCn
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6465-125">-ClientCertIsAdmin</span><span class="sxs-lookup"><span data-stu-id="f6465-125">-ClientCertIsAdmin</span></span>
<span data-ttu-id="f6465-126">Wird verwendet, um anzugeben, ob das Clientzertifikat über Administratorebene verfügt.</span><span class="sxs-lookup"><span data-stu-id="f6465-126">Use to specify if the client certificate has administrator level.</span></span>

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

### <span data-ttu-id="f6465-127">-ClientCertIssuerThumbprint</span><span class="sxs-lookup"><span data-stu-id="f6465-127">-ClientCertIssuerThumbprint</span></span>
<span data-ttu-id="f6465-128">Liste der Ausstellerdrückdrucke für das Clientzertifikat.</span><span class="sxs-lookup"><span data-stu-id="f6465-128">List of Issuer thumbprints for the client certificate.</span></span>
<span data-ttu-id="f6465-129">Wird nur in Kombination mit ClientCertCommonName verwendet.</span><span class="sxs-lookup"><span data-stu-id="f6465-129">Only use in combination with ClientCertCommonName.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ClientCertByCn
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6465-130">-ClientCertThumbprint</span><span class="sxs-lookup"><span data-stu-id="f6465-130">-ClientCertThumbprint</span></span>
<span data-ttu-id="f6465-131">Fingerabdruck des Clientzertifikats.</span><span class="sxs-lookup"><span data-stu-id="f6465-131">Client certificate thumbprint.</span></span>

```yaml
Type: System.String
Parameter Sets: ClientCertByTp
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6465-132">-ClientConnectionPort</span><span class="sxs-lookup"><span data-stu-id="f6465-132">-ClientConnectionPort</span></span>
<span data-ttu-id="f6465-133">Port, der für Clientverbindungen zum Cluster verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="f6465-133">Port used for client connections to the cluster.</span></span>
<span data-ttu-id="f6465-134">Standard: 19000.</span><span class="sxs-lookup"><span data-stu-id="f6465-134">Default: 19000.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 19000
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6465-135">-CodeVersion</span><span class="sxs-lookup"><span data-stu-id="f6465-135">-CodeVersion</span></span>
<span data-ttu-id="f6465-136">Cluster service fabric code version.</span><span class="sxs-lookup"><span data-stu-id="f6465-136">Cluster service fabric code version.</span></span>
<span data-ttu-id="f6465-137">Wird nur verwendet, wenn der Upgrademodus manuell ist.</span><span class="sxs-lookup"><span data-stu-id="f6465-137">Only use if upgrade mode is Manual.</span></span>

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

### <span data-ttu-id="f6465-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6465-138">-DefaultProfile</span></span>
<span data-ttu-id="f6465-139">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f6465-139">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f6465-140">-DnsName</span><span class="sxs-lookup"><span data-stu-id="f6465-140">-DnsName</span></span>
<span data-ttu-id="f6465-141">Dns-Name des Clusters.</span><span class="sxs-lookup"><span data-stu-id="f6465-141">Cluster's dns name.</span></span>

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

### <span data-ttu-id="f6465-142">-HttpGatewayConnectionPort</span><span class="sxs-lookup"><span data-stu-id="f6465-142">-HttpGatewayConnectionPort</span></span>
<span data-ttu-id="f6465-143">Port, der für http-Verbindungen mit dem Cluster verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="f6465-143">Port used for http connections to the cluster.</span></span>
<span data-ttu-id="f6465-144">Standard: 19080.</span><span class="sxs-lookup"><span data-stu-id="f6465-144">Default: 19080.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 19080
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6465-145">-Location</span><span class="sxs-lookup"><span data-stu-id="f6465-145">-Location</span></span>
<span data-ttu-id="f6465-146">Ressourcenspeicherort</span><span class="sxs-lookup"><span data-stu-id="f6465-146">The resource location</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f6465-147">-Name</span><span class="sxs-lookup"><span data-stu-id="f6465-147">-Name</span></span>
<span data-ttu-id="f6465-148">Geben Sie den Namen des Cluster an.</span><span class="sxs-lookup"><span data-stu-id="f6465-148">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6465-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f6465-149">-ResourceGroupName</span></span>
<span data-ttu-id="f6465-150">Geben Sie den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="f6465-150">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="f6465-151">-ReverseProxyEndpointPort</span><span class="sxs-lookup"><span data-stu-id="f6465-151">-ReverseProxyEndpointPort</span></span>
<span data-ttu-id="f6465-152">Endpunkt, der vom Reverseproxy verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="f6465-152">Endpoint used by reverse proxy.</span></span>

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

### <span data-ttu-id="f6465-153">-SKU</span><span class="sxs-lookup"><span data-stu-id="f6465-153">-Sku</span></span>
<span data-ttu-id="f6465-154">Die Cluster-SKU, die Optionen sind "Standard": Sie hat mindestens drei Startknoten und lässt nur einen Knotentyp und "Standard" zu: Sie hat mindestens fünf Startknoten und lässt mehrere Knotentypen zu.</span><span class="sxs-lookup"><span data-stu-id="f6465-154">Cluster's Sku, the options are Basic: it will have a minimum of 3 seed nodes and only allows 1 node type and Standard: it will have a minimum of 5 seed nodes and allows multiple node types.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.ManagedClusterSku
Parameter Sets: (All)
Aliases:
Accepted values: Basic, Standard

Required: False
Position: Named
Default value: Basic
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6465-155">-UpgradeMode</span><span class="sxs-lookup"><span data-stu-id="f6465-155">-UpgradeMode</span></span>
<span data-ttu-id="f6465-156">Cluster service fabric code version upgrade mode.</span><span class="sxs-lookup"><span data-stu-id="f6465-156">Cluster service fabric code version upgrade mode.</span></span>
<span data-ttu-id="f6465-157">Automatisch oder manuell</span><span class="sxs-lookup"><span data-stu-id="f6465-157">Automatic or Manual.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.ClusterUpgradeMode
Parameter Sets: (All)
Aliases:
Accepted values: Automatic, Manual

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6465-158">-UseTestExtension</span><span class="sxs-lookup"><span data-stu-id="f6465-158">-UseTestExtension</span></span>
<span data-ttu-id="f6465-159">If Specify The cluster will be crated with service test vmss extension.</span><span class="sxs-lookup"><span data-stu-id="f6465-159">If Specify The cluster will be crated with service test vmss extension.</span></span>

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

### <span data-ttu-id="f6465-160">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f6465-160">-Confirm</span></span>
<span data-ttu-id="f6465-161">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f6465-161">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f6465-162">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="f6465-162">-WhatIf</span></span>
<span data-ttu-id="f6465-163">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f6465-163">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f6465-164">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f6465-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f6465-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6465-165">CommonParameters</span></span>
<span data-ttu-id="f6465-166">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f6465-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6465-167">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f6465-167">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6465-168">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f6465-168">INPUTS</span></span>

### <span data-ttu-id="f6465-169">System.String</span><span class="sxs-lookup"><span data-stu-id="f6465-169">System.String</span></span>

## <span data-ttu-id="f6465-170">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f6465-170">OUTPUTS</span></span>

### <span data-ttu-id="f6465-171">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedCluster</span><span class="sxs-lookup"><span data-stu-id="f6465-171">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedCluster</span></span>

## <span data-ttu-id="f6465-172">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="f6465-172">NOTES</span></span>

## <span data-ttu-id="f6465-173">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="f6465-173">RELATED LINKS</span></span>

[<span data-ttu-id="f6465-174">New-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="f6465-174">New-AzServiceFabricManagedNodeType</span></span>](./New-AzServiceFabricManagedNodeType.md)