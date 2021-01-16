---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricmanagedclusterclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricManagedClusterClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricManagedClusterClientCertificate.md
ms.openlocfilehash: d9a3e5488fe55a1d5090fb21ffb211e6fcec53c2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98301139"
---
# <span data-ttu-id="d5843-101">Remove-AzServiceFabricManagedClusterClientCertificate</span><span class="sxs-lookup"><span data-stu-id="d5843-101">Remove-AzServiceFabricManagedClusterClientCertificate</span></span>

## <span data-ttu-id="d5843-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d5843-102">SYNOPSIS</span></span>
<span data-ttu-id="d5843-103">Geben Sie das Clientzertifikat per Fingerabdruck oder allgemeinem Namen neu aus.</span><span class="sxs-lookup"><span data-stu-id="d5843-103">Remvoe client certificate by thumbprint or common name.</span></span>

## <span data-ttu-id="d5843-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d5843-104">SYNTAX</span></span>

### <span data-ttu-id="d5843-105">ClientCertByTpByObj (Standard)</span><span class="sxs-lookup"><span data-stu-id="d5843-105">ClientCertByTpByObj (Default)</span></span>
```
Remove-AzServiceFabricManagedClusterClientCertificate [-InputObject] <PSManagedCluster> -Thumbprint <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d5843-106">ClientCertByCnTpName</span><span class="sxs-lookup"><span data-stu-id="d5843-106">ClientCertByCnTpName</span></span>
```
Remove-AzServiceFabricManagedClusterClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 -Thumbprint <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d5843-107">ClientCertByCnByName</span><span class="sxs-lookup"><span data-stu-id="d5843-107">ClientCertByCnByName</span></span>
```
Remove-AzServiceFabricManagedClusterClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 -CommonName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d5843-108">ClientCertByCnByObj</span><span class="sxs-lookup"><span data-stu-id="d5843-108">ClientCertByCnByObj</span></span>
```
Remove-AzServiceFabricManagedClusterClientCertificate [-InputObject] <PSManagedCluster> -CommonName <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d5843-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d5843-109">DESCRIPTION</span></span>
<span data-ttu-id="d5843-110">Geben Sie das Clientzertifikat per Fingerabdruck oder allgemeinem Namen neu aus.</span><span class="sxs-lookup"><span data-stu-id="d5843-110">Remvoe client certificate by thumbprint or common name.</span></span>

## <span data-ttu-id="d5843-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d5843-111">EXAMPLES</span></span>

### <span data-ttu-id="d5843-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d5843-112">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
Remove-AzServiceFabricManagedClusterClientCertificate -ResourceGroupName $rgName -Name $clusterName -CommonName 'Contoso.com'
```

<span data-ttu-id="d5843-113">Entfernen Sie das Clientzertifikat nach allgemeinem Namen.</span><span class="sxs-lookup"><span data-stu-id="d5843-113">Remove client certificate by common name.</span></span>

### <span data-ttu-id="d5843-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="d5843-114">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
Remove-AzServiceFabricManagedClusterClientCertificate -ResourceGroupName $rgName -Name $clusterName -Thumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A
```

<span data-ttu-id="d5843-115">Entfernen Sie das Clientzertifikat durch Fingerabdruck.</span><span class="sxs-lookup"><span data-stu-id="d5843-115">Remove client certificate by thumbprint.</span></span>

### <span data-ttu-id="d5843-116">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="d5843-116">Example 3</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$cluster = Get-AzServiceFabricManagedCluster -ResourceGroupName $rgName -Name $clusterName

$cluster | Remove-AzServiceFabricManagedClusterClientCertificate -Thumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A
```

<span data-ttu-id="d5843-117">Entfernen Sie das Clientzertifikat durch Fingerabdruck mit Pipette.</span><span class="sxs-lookup"><span data-stu-id="d5843-117">Remove client certificate by thumbprint, with piping.</span></span>

## <span data-ttu-id="d5843-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d5843-118">PARAMETERS</span></span>

### <span data-ttu-id="d5843-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d5843-119">-AsJob</span></span>
<span data-ttu-id="d5843-120">Führen Sie das Cmdlet im Hintergrund aus, und geben Sie einen Auftrag zurück, um den Fortschritt nachverfolgt zu können.</span><span class="sxs-lookup"><span data-stu-id="d5843-120">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="d5843-121">-CommonName</span><span class="sxs-lookup"><span data-stu-id="d5843-121">-CommonName</span></span>
<span data-ttu-id="d5843-122">Gemeinsamer Name des Clientzertifikats.</span><span class="sxs-lookup"><span data-stu-id="d5843-122">Client certificate common name.</span></span>

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

### <span data-ttu-id="d5843-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5843-123">-DefaultProfile</span></span>
<span data-ttu-id="d5843-124">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d5843-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d5843-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d5843-125">-InputObject</span></span>
<span data-ttu-id="d5843-126">Verwaltete Clusterressource</span><span class="sxs-lookup"><span data-stu-id="d5843-126">Managed cluster resource</span></span>

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

### <span data-ttu-id="d5843-127">-Name</span><span class="sxs-lookup"><span data-stu-id="d5843-127">-Name</span></span>
<span data-ttu-id="d5843-128">Geben Sie den Namen des Cluster an.</span><span class="sxs-lookup"><span data-stu-id="d5843-128">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="d5843-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d5843-129">-PassThru</span></span>
<span data-ttu-id="d5843-130">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="d5843-130">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="d5843-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d5843-131">-ResourceGroupName</span></span>
<span data-ttu-id="d5843-132">Geben Sie den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="d5843-132">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="d5843-133">-Thumbprint</span><span class="sxs-lookup"><span data-stu-id="d5843-133">-Thumbprint</span></span>
<span data-ttu-id="d5843-134">Fingerabdruck des Clientzertifikats.</span><span class="sxs-lookup"><span data-stu-id="d5843-134">Client certificate thumbprint.</span></span>

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

### <span data-ttu-id="d5843-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d5843-135">-Confirm</span></span>
<span data-ttu-id="d5843-136">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d5843-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d5843-137">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="d5843-137">-WhatIf</span></span>
<span data-ttu-id="d5843-138">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d5843-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d5843-139">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d5843-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d5843-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5843-140">CommonParameters</span></span>
<span data-ttu-id="d5843-141">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d5843-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5843-142">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d5843-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5843-143">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d5843-143">INPUTS</span></span>

### <span data-ttu-id="d5843-144">System.String</span><span class="sxs-lookup"><span data-stu-id="d5843-144">System.String</span></span>

## <span data-ttu-id="d5843-145">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d5843-145">OUTPUTS</span></span>

### <span data-ttu-id="d5843-146">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedCluster</span><span class="sxs-lookup"><span data-stu-id="d5843-146">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedCluster</span></span>

## <span data-ttu-id="d5843-147">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="d5843-147">NOTES</span></span>

## <span data-ttu-id="d5843-148">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="d5843-148">RELATED LINKS</span></span>
