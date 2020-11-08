---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/new-azservicefabricmanagedcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricManagedCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricManagedCluster.md
ms.openlocfilehash: 9dd54f0f1ca56a8bedf3550e238a4308b519925d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94176745"
---
# <span data-ttu-id="3edec-101">New-AzServiceFabricManagedCluster</span><span class="sxs-lookup"><span data-stu-id="3edec-101">New-AzServiceFabricManagedCluster</span></span>

## <span data-ttu-id="3edec-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3edec-102">SYNOPSIS</span></span>
<span data-ttu-id="3edec-103">Erstellen eines neuen verwalteten Clusters</span><span class="sxs-lookup"><span data-stu-id="3edec-103">Create new managed cluster.</span></span>

## <span data-ttu-id="3edec-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3edec-104">SYNTAX</span></span>

### <span data-ttu-id="3edec-105">ClientCertByTp (Standard)</span><span class="sxs-lookup"><span data-stu-id="3edec-105">ClientCertByTp (Default)</span></span>
```
New-AzServiceFabricManagedCluster [-ResourceGroupName] <String> [-Name] <String> -Location <String>
 [-UpgradeMode <ClusterUpgradeMode>] [-CodeVersion <String>] [-ClientCertIsAdmin]
 -ClientCertThumbprint <String> -AdminPassword <SecureString> [-AdminUserName <String>]
 [-HttpGatewayConnectionPort <Int32>] [-ClientConnectionPort <Int32>] [-DnsName <String>]
 [-ReverseProxyEndpointPort <Int32>] [-Sku <ManagedClusterSku>] [-UseTestExtension] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3edec-106">ClientCertByCn</span><span class="sxs-lookup"><span data-stu-id="3edec-106">ClientCertByCn</span></span>
```
New-AzServiceFabricManagedCluster [-ResourceGroupName] <String> [-Name] <String> -Location <String>
 [-UpgradeMode <ClusterUpgradeMode>] [-CodeVersion <String>] [-ClientCertIsAdmin]
 -ClientCertCommonName <String> [-ClientCertIssuerThumbprint <String[]>] -AdminPassword <SecureString>
 [-AdminUserName <String>] [-HttpGatewayConnectionPort <Int32>] [-ClientConnectionPort <Int32>]
 [-DnsName <String>] [-ReverseProxyEndpointPort <Int32>] [-Sku <ManagedClusterSku>] [-UseTestExtension]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3edec-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3edec-107">DESCRIPTION</span></span>
<span data-ttu-id="3edec-108">Mit diesem Cmdlet wird eine verwaltete Clusterressource ohne Knotentypen erstellt.</span><span class="sxs-lookup"><span data-stu-id="3edec-108">This cmdlet will create a managed cluster resource without node types.</span></span> <span data-ttu-id="3edec-109">Zum Bootstrap des Clusters muss ein primärer Knotentyp mit [New-AzServiceFabricManagedNodeType](./New-AzServiceFabricManagedNodeType.md)hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="3edec-109">To bootstrap the cluster A primary node type needs to be added use [New-AzServiceFabricManagedNodeType](./New-AzServiceFabricManagedNodeType.md).</span></span>

## <span data-ttu-id="3edec-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3edec-110">EXAMPLES</span></span>

### <span data-ttu-id="3edec-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="3edec-111">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$password = ConvertTo-SecureString -AsPlainText -Force "testpass1234!@#$"
New-AzServiceFabricManagedCluster -ResourceGroupName $rgName -Location centraluseuap -ClusterName $clusterName -AdminPassword $password -Verbose
```

<span data-ttu-id="3edec-112">Mit diesem Befehl wird eine Clusterressource mit der standardmäßigen Basis-SKU erstellt.</span><span class="sxs-lookup"><span data-stu-id="3edec-112">This command creates a cluster resource with default basic sku.</span></span>

### <span data-ttu-id="3edec-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="3edec-113">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$password = ConvertTo-SecureString -AsPlainText -Force "testpass1234!@#$"
New-AzServiceFabricManagedCluster -ResourceGroupName $rgName -Location centraluseuap -ClusterName $clusterName -ClientCertThumbprint XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX -ClientCertIsAdmin -AdminPassword $password -Sku Standard -Verbose
```

<span data-ttu-id="3edec-114">Dieser Befehl erstellt eine Clusterressource in centraluseuap mit einem anfänglichen Administrator Clientzertifikat und einer Standard-SKU.</span><span class="sxs-lookup"><span data-stu-id="3edec-114">This command creates a cluster resource in centraluseuap with an initial admin client certificate and standard sku.</span></span>

## <span data-ttu-id="3edec-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="3edec-115">PARAMETERS</span></span>

### <span data-ttu-id="3edec-116">-AdminPassword</span><span class="sxs-lookup"><span data-stu-id="3edec-116">-AdminPassword</span></span>
<span data-ttu-id="3edec-117">Das für die virtuellen Computer verwendete Administratorkennwort.</span><span class="sxs-lookup"><span data-stu-id="3edec-117">Admin password used for the virtual machines.</span></span>

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

### <span data-ttu-id="3edec-118">-Nation aus AdminUsername</span><span class="sxs-lookup"><span data-stu-id="3edec-118">-AdminUserName</span></span>
<span data-ttu-id="3edec-119">Das für die virtuellen Computer verwendete Administratorkennwort.</span><span class="sxs-lookup"><span data-stu-id="3edec-119">Admin password used for the virtual machines.</span></span>
<span data-ttu-id="3edec-120">Standard: vmadmin.</span><span class="sxs-lookup"><span data-stu-id="3edec-120">Default: vmadmin.</span></span>

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

### <span data-ttu-id="3edec-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3edec-121">-AsJob</span></span>
<span data-ttu-id="3edec-122">Führen Sie das Cmdlet im Hintergrund aus, und geben Sie einen Auftrag zum Nachverfolgen des Fortschritts zurück.</span><span class="sxs-lookup"><span data-stu-id="3edec-122">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="3edec-123">-ClientCertCommonName</span><span class="sxs-lookup"><span data-stu-id="3edec-123">-ClientCertCommonName</span></span>
<span data-ttu-id="3edec-124">Allgemeiner Name des Client Zertifikats.</span><span class="sxs-lookup"><span data-stu-id="3edec-124">Client certificate common name.</span></span>

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

### <span data-ttu-id="3edec-125">-ClientCertIsAdmin</span><span class="sxs-lookup"><span data-stu-id="3edec-125">-ClientCertIsAdmin</span></span>
<span data-ttu-id="3edec-126">Hiermit geben Sie an, ob das Clientzertifikat Administratorebene hat.</span><span class="sxs-lookup"><span data-stu-id="3edec-126">Use to specify if the client certificate has administrator level.</span></span>

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

### <span data-ttu-id="3edec-127">-ClientCertIssuerThumbprint</span><span class="sxs-lookup"><span data-stu-id="3edec-127">-ClientCertIssuerThumbprint</span></span>
<span data-ttu-id="3edec-128">Liste der Aussteller-Fingerabdrücke für das Clientzertifikat</span><span class="sxs-lookup"><span data-stu-id="3edec-128">List of Issuer thumbprints for the client certificate.</span></span>
<span data-ttu-id="3edec-129">Nur in Verbindung mit ClientCertCommonName verwenden.</span><span class="sxs-lookup"><span data-stu-id="3edec-129">Only use in combination with ClientCertCommonName.</span></span>

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

### <span data-ttu-id="3edec-130">-ClientCertThumbprint</span><span class="sxs-lookup"><span data-stu-id="3edec-130">-ClientCertThumbprint</span></span>
<span data-ttu-id="3edec-131">Fingerabdruck des Client Zertifikats.</span><span class="sxs-lookup"><span data-stu-id="3edec-131">Client certificate thumbprint.</span></span>

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

### <span data-ttu-id="3edec-132">-ClientConnectionPort</span><span class="sxs-lookup"><span data-stu-id="3edec-132">-ClientConnectionPort</span></span>
<span data-ttu-id="3edec-133">Port, der für Clientverbindungen mit dem Cluster verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="3edec-133">Port used for client connections to the cluster.</span></span>
<span data-ttu-id="3edec-134">Standard: 19000.</span><span class="sxs-lookup"><span data-stu-id="3edec-134">Default: 19000.</span></span>

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

### <span data-ttu-id="3edec-135">-CodeVersion</span><span class="sxs-lookup"><span data-stu-id="3edec-135">-CodeVersion</span></span>
<span data-ttu-id="3edec-136">Cluster Dienst-Fabric-Code Version.</span><span class="sxs-lookup"><span data-stu-id="3edec-136">Cluster service fabric code version.</span></span>
<span data-ttu-id="3edec-137">Nur verwenden, wenn der Aktualisierungsmodus manuell ist.</span><span class="sxs-lookup"><span data-stu-id="3edec-137">Only use if upgrade mode is Manual.</span></span>

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

### <span data-ttu-id="3edec-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3edec-138">-DefaultProfile</span></span>
<span data-ttu-id="3edec-139">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="3edec-139">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3edec-140">-DnsName</span><span class="sxs-lookup"><span data-stu-id="3edec-140">-DnsName</span></span>
<span data-ttu-id="3edec-141">Der DNS-Name des Clusters.</span><span class="sxs-lookup"><span data-stu-id="3edec-141">Cluster's dns name.</span></span>

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

### <span data-ttu-id="3edec-142">-HttpGatewayConnectionPort</span><span class="sxs-lookup"><span data-stu-id="3edec-142">-HttpGatewayConnectionPort</span></span>
<span data-ttu-id="3edec-143">Port, der für http-Verbindungen mit dem Cluster verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="3edec-143">Port used for http connections to the cluster.</span></span>
<span data-ttu-id="3edec-144">Standard: 19080.</span><span class="sxs-lookup"><span data-stu-id="3edec-144">Default: 19080.</span></span>

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

### <span data-ttu-id="3edec-145">-Standort</span><span class="sxs-lookup"><span data-stu-id="3edec-145">-Location</span></span>
<span data-ttu-id="3edec-146">Der Speicherort der Ressource</span><span class="sxs-lookup"><span data-stu-id="3edec-146">The resource location</span></span>

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

### <span data-ttu-id="3edec-147">-Name</span><span class="sxs-lookup"><span data-stu-id="3edec-147">-Name</span></span>
<span data-ttu-id="3edec-148">Geben Sie den Namen des Clusters an.</span><span class="sxs-lookup"><span data-stu-id="3edec-148">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="3edec-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3edec-149">-ResourceGroupName</span></span>
<span data-ttu-id="3edec-150">Geben Sie den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="3edec-150">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="3edec-151">-ReverseProxyEndpointPort</span><span class="sxs-lookup"><span data-stu-id="3edec-151">-ReverseProxyEndpointPort</span></span>
<span data-ttu-id="3edec-152">Vom Reverseproxy verwendeter Endpunkt.</span><span class="sxs-lookup"><span data-stu-id="3edec-152">Endpoint used by reverse proxy.</span></span>

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

### <span data-ttu-id="3edec-153">-SKU</span><span class="sxs-lookup"><span data-stu-id="3edec-153">-Sku</span></span>
<span data-ttu-id="3edec-154">Die SKU des Clusters, die Optionen sind einfach: Es hat mindestens 3 Seed-Knoten und ermöglicht nur 1 Knotentyp und Standard: Es hat mindestens 5 Seed-Knoten und ermöglicht die Ausführung mehrerer Knotentypen.</span><span class="sxs-lookup"><span data-stu-id="3edec-154">Cluster's Sku, the options are Basic: it will have a minimum of 3 seed nodes and only allows 1 node type and Standard: it will have a minimum of 5 seed nodes and allows multiple node types.</span></span>

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

### <span data-ttu-id="3edec-155">-UpgradeMode</span><span class="sxs-lookup"><span data-stu-id="3edec-155">-UpgradeMode</span></span>
<span data-ttu-id="3edec-156">Cluster Dienst Fabric Code-Versions Aktualisierungsmodus.</span><span class="sxs-lookup"><span data-stu-id="3edec-156">Cluster service fabric code version upgrade mode.</span></span>
<span data-ttu-id="3edec-157">Automatisch oder manuell.</span><span class="sxs-lookup"><span data-stu-id="3edec-157">Automatic or Manual.</span></span>

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

### <span data-ttu-id="3edec-158">-UseTestExtension</span><span class="sxs-lookup"><span data-stu-id="3edec-158">-UseTestExtension</span></span>
<span data-ttu-id="3edec-159">Wenn angeben, wird der Cluster mit der Dienst Test-VMSS-Erweiterung verschachtelt.</span><span class="sxs-lookup"><span data-stu-id="3edec-159">If Specify The cluster will be crated with service test vmss extension.</span></span>

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

### <span data-ttu-id="3edec-160">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="3edec-160">-Confirm</span></span>
<span data-ttu-id="3edec-161">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3edec-161">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3edec-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3edec-162">-WhatIf</span></span>
<span data-ttu-id="3edec-163">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3edec-163">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3edec-164">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3edec-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3edec-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3edec-165">CommonParameters</span></span>
<span data-ttu-id="3edec-166">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3edec-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3edec-167">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3edec-167">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3edec-168">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3edec-168">INPUTS</span></span>

### <span data-ttu-id="3edec-169">System. String</span><span class="sxs-lookup"><span data-stu-id="3edec-169">System.String</span></span>

## <span data-ttu-id="3edec-170">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3edec-170">OUTPUTS</span></span>

### <span data-ttu-id="3edec-171">Microsoft. Azure. Commands. ServiceFabric. Models. PSManagedCluster</span><span class="sxs-lookup"><span data-stu-id="3edec-171">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedCluster</span></span>

## <span data-ttu-id="3edec-172">Notizen</span><span class="sxs-lookup"><span data-stu-id="3edec-172">NOTES</span></span>

## <span data-ttu-id="3edec-173">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3edec-173">RELATED LINKS</span></span>

[<span data-ttu-id="3edec-174">Neu – AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="3edec-174">New-AzServiceFabricManagedNodeType</span></span>](./New-AzServiceFabricManagedNodeType.md)