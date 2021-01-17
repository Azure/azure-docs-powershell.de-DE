---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricmanagedclusterclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricManagedClusterClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricManagedClusterClientCertificate.md
ms.openlocfilehash: d9a3e5488fe55a1d5090fb21ffb211e6fcec53c2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98471784"
---
# <span data-ttu-id="0d326-101">Remove-AzServiceFabricManagedClusterClientCertificate</span><span class="sxs-lookup"><span data-stu-id="0d326-101">Remove-AzServiceFabricManagedClusterClientCertificate</span></span>

## <span data-ttu-id="0d326-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0d326-102">SYNOPSIS</span></span>
<span data-ttu-id="0d326-103">Geben Sie das Clientzertifikat per Fingerabdruck oder allgemeinem Namen ab.</span><span class="sxs-lookup"><span data-stu-id="0d326-103">Remvoe client certificate by thumbprint or common name.</span></span>

## <span data-ttu-id="0d326-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0d326-104">SYNTAX</span></span>

### <span data-ttu-id="0d326-105">ClientCertByTpByObj (Standard)</span><span class="sxs-lookup"><span data-stu-id="0d326-105">ClientCertByTpByObj (Default)</span></span>
```
Remove-AzServiceFabricManagedClusterClientCertificate [-InputObject] <PSManagedCluster> -Thumbprint <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0d326-106">ClientCertByCnTpName</span><span class="sxs-lookup"><span data-stu-id="0d326-106">ClientCertByCnTpName</span></span>
```
Remove-AzServiceFabricManagedClusterClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 -Thumbprint <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0d326-107">ClientCertByCnByName</span><span class="sxs-lookup"><span data-stu-id="0d326-107">ClientCertByCnByName</span></span>
```
Remove-AzServiceFabricManagedClusterClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 -CommonName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0d326-108">ClientCertByCnByObj</span><span class="sxs-lookup"><span data-stu-id="0d326-108">ClientCertByCnByObj</span></span>
```
Remove-AzServiceFabricManagedClusterClientCertificate [-InputObject] <PSManagedCluster> -CommonName <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0d326-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0d326-109">DESCRIPTION</span></span>
<span data-ttu-id="0d326-110">Geben Sie das Clientzertifikat per Fingerabdruck oder allgemeinem Namen neu aus.</span><span class="sxs-lookup"><span data-stu-id="0d326-110">Remvoe client certificate by thumbprint or common name.</span></span>

## <span data-ttu-id="0d326-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="0d326-111">EXAMPLES</span></span>

### <span data-ttu-id="0d326-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="0d326-112">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
Remove-AzServiceFabricManagedClusterClientCertificate -ResourceGroupName $rgName -Name $clusterName -CommonName 'Contoso.com'
```

<span data-ttu-id="0d326-113">Entfernen Sie das Clientzertifikat nach allgemeinem Namen.</span><span class="sxs-lookup"><span data-stu-id="0d326-113">Remove client certificate by common name.</span></span>

### <span data-ttu-id="0d326-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="0d326-114">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
Remove-AzServiceFabricManagedClusterClientCertificate -ResourceGroupName $rgName -Name $clusterName -Thumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A
```

<span data-ttu-id="0d326-115">Entfernen Sie das Clientzertifikat durch Fingerabdruck.</span><span class="sxs-lookup"><span data-stu-id="0d326-115">Remove client certificate by thumbprint.</span></span>

### <span data-ttu-id="0d326-116">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="0d326-116">Example 3</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$cluster = Get-AzServiceFabricManagedCluster -ResourceGroupName $rgName -Name $clusterName

$cluster | Remove-AzServiceFabricManagedClusterClientCertificate -Thumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A
```

<span data-ttu-id="0d326-117">Entfernen Sie das Clientzertifikat durch Fingerabdruck mit Pipette.</span><span class="sxs-lookup"><span data-stu-id="0d326-117">Remove client certificate by thumbprint, with piping.</span></span>

## <span data-ttu-id="0d326-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0d326-118">PARAMETERS</span></span>

### <span data-ttu-id="0d326-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0d326-119">-AsJob</span></span>
<span data-ttu-id="0d326-120">Führen Sie das Cmdlet im Hintergrund aus, und geben Sie einen Auftrag zurück, um den Fortschritt nachverfolgt zu können.</span><span class="sxs-lookup"><span data-stu-id="0d326-120">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="0d326-121">-CommonName</span><span class="sxs-lookup"><span data-stu-id="0d326-121">-CommonName</span></span>
<span data-ttu-id="0d326-122">Gemeinsamer Name des Clientzertifikats.</span><span class="sxs-lookup"><span data-stu-id="0d326-122">Client certificate common name.</span></span>

```yaml
Type: System.String
Parameter Sets: ClientCertByCnByName, ClientCertByCnByObj
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d326-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d326-123">-DefaultProfile</span></span>
<span data-ttu-id="0d326-124">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0d326-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0d326-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0d326-125">-InputObject</span></span>
<span data-ttu-id="0d326-126">Verwaltete Clusterressource</span><span class="sxs-lookup"><span data-stu-id="0d326-126">Managed cluster resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedCluster
Parameter Sets: ClientCertByTpByObj, ClientCertByCnByObj
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0d326-127">-Name</span><span class="sxs-lookup"><span data-stu-id="0d326-127">-Name</span></span>
<span data-ttu-id="0d326-128">Geben Sie den Namen des Cluster an.</span><span class="sxs-lookup"><span data-stu-id="0d326-128">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: ClientCertByCnTpName, ClientCertByCnByName
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d326-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0d326-129">-PassThru</span></span>
<span data-ttu-id="0d326-130">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="0d326-130">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="0d326-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0d326-131">-ResourceGroupName</span></span>
<span data-ttu-id="0d326-132">Geben Sie den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="0d326-132">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ClientCertByCnTpName, ClientCertByCnByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d326-133">-Thumbprint</span><span class="sxs-lookup"><span data-stu-id="0d326-133">-Thumbprint</span></span>
<span data-ttu-id="0d326-134">Fingerabdruck des Clientzertifikats.</span><span class="sxs-lookup"><span data-stu-id="0d326-134">Client certificate thumbprint.</span></span>

```yaml
Type: System.String
Parameter Sets: ClientCertByTpByObj, ClientCertByCnTpName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d326-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0d326-135">-Confirm</span></span>
<span data-ttu-id="0d326-136">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0d326-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0d326-137">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="0d326-137">-WhatIf</span></span>
<span data-ttu-id="0d326-138">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0d326-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0d326-139">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0d326-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0d326-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d326-140">CommonParameters</span></span>
<span data-ttu-id="0d326-141">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0d326-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d326-142">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0d326-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d326-143">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="0d326-143">INPUTS</span></span>

### <span data-ttu-id="0d326-144">System.String</span><span class="sxs-lookup"><span data-stu-id="0d326-144">System.String</span></span>

## <span data-ttu-id="0d326-145">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="0d326-145">OUTPUTS</span></span>

### <span data-ttu-id="0d326-146">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedCluster</span><span class="sxs-lookup"><span data-stu-id="0d326-146">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedCluster</span></span>

## <span data-ttu-id="0d326-147">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="0d326-147">NOTES</span></span>

## <span data-ttu-id="0d326-148">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="0d326-148">RELATED LINKS</span></span>
