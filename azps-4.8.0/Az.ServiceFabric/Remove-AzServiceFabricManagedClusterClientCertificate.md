---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricmanagedclusterclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricManagedClusterClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricManagedClusterClientCertificate.md
ms.openlocfilehash: d9a3e5488fe55a1d5090fb21ffb211e6fcec53c2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94174160"
---
# <span data-ttu-id="ddb10-101">Remove-AzServiceFabricManagedClusterClientCertificate</span><span class="sxs-lookup"><span data-stu-id="ddb10-101">Remove-AzServiceFabricManagedClusterClientCertificate</span></span>

## <span data-ttu-id="ddb10-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ddb10-102">SYNOPSIS</span></span>
<span data-ttu-id="ddb10-103">Remvoe-Clientzertifikat nach Fingerabdruck oder allgemeinem Namen.</span><span class="sxs-lookup"><span data-stu-id="ddb10-103">Remvoe client certificate by thumbprint or common name.</span></span>

## <span data-ttu-id="ddb10-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ddb10-104">SYNTAX</span></span>

### <span data-ttu-id="ddb10-105">ClientCertByTpByObj (Standard)</span><span class="sxs-lookup"><span data-stu-id="ddb10-105">ClientCertByTpByObj (Default)</span></span>
```
Remove-AzServiceFabricManagedClusterClientCertificate [-InputObject] <PSManagedCluster> -Thumbprint <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ddb10-106">ClientCertByCnTpName</span><span class="sxs-lookup"><span data-stu-id="ddb10-106">ClientCertByCnTpName</span></span>
```
Remove-AzServiceFabricManagedClusterClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 -Thumbprint <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ddb10-107">ClientCertByCnByName</span><span class="sxs-lookup"><span data-stu-id="ddb10-107">ClientCertByCnByName</span></span>
```
Remove-AzServiceFabricManagedClusterClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 -CommonName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ddb10-108">ClientCertByCnByObj</span><span class="sxs-lookup"><span data-stu-id="ddb10-108">ClientCertByCnByObj</span></span>
```
Remove-AzServiceFabricManagedClusterClientCertificate [-InputObject] <PSManagedCluster> -CommonName <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ddb10-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ddb10-109">DESCRIPTION</span></span>
<span data-ttu-id="ddb10-110">Remvoe-Clientzertifikat nach Fingerabdruck oder allgemeinem Namen.</span><span class="sxs-lookup"><span data-stu-id="ddb10-110">Remvoe client certificate by thumbprint or common name.</span></span>

## <span data-ttu-id="ddb10-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ddb10-111">EXAMPLES</span></span>

### <span data-ttu-id="ddb10-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ddb10-112">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
Remove-AzServiceFabricManagedClusterClientCertificate -ResourceGroupName $rgName -Name $clusterName -CommonName 'Contoso.com'
```

<span data-ttu-id="ddb10-113">Entfernen Sie das Clientzertifikat nach dem allgemeinen Namen.</span><span class="sxs-lookup"><span data-stu-id="ddb10-113">Remove client certificate by common name.</span></span>

### <span data-ttu-id="ddb10-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="ddb10-114">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
Remove-AzServiceFabricManagedClusterClientCertificate -ResourceGroupName $rgName -Name $clusterName -Thumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A
```

<span data-ttu-id="ddb10-115">Clientzertifikat nach Fingerabdruck entfernen</span><span class="sxs-lookup"><span data-stu-id="ddb10-115">Remove client certificate by thumbprint.</span></span>

### <span data-ttu-id="ddb10-116">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="ddb10-116">Example 3</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$cluster = Get-AzServiceFabricManagedCluster -ResourceGroupName $rgName -Name $clusterName

$cluster | Remove-AzServiceFabricManagedClusterClientCertificate -Thumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A
```

<span data-ttu-id="ddb10-117">Entfernen Sie das Clientzertifikat mit dem Fingerabdruck mit Piping.</span><span class="sxs-lookup"><span data-stu-id="ddb10-117">Remove client certificate by thumbprint, with piping.</span></span>

## <span data-ttu-id="ddb10-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="ddb10-118">PARAMETERS</span></span>

### <span data-ttu-id="ddb10-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ddb10-119">-AsJob</span></span>
<span data-ttu-id="ddb10-120">Führen Sie das Cmdlet im Hintergrund aus, und geben Sie einen Auftrag zum Nachverfolgen des Fortschritts zurück.</span><span class="sxs-lookup"><span data-stu-id="ddb10-120">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="ddb10-121">-CommonName</span><span class="sxs-lookup"><span data-stu-id="ddb10-121">-CommonName</span></span>
<span data-ttu-id="ddb10-122">Allgemeiner Name des Client Zertifikats.</span><span class="sxs-lookup"><span data-stu-id="ddb10-122">Client certificate common name.</span></span>

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

### <span data-ttu-id="ddb10-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ddb10-123">-DefaultProfile</span></span>
<span data-ttu-id="ddb10-124">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ddb10-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ddb10-125">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="ddb10-125">-InputObject</span></span>
<span data-ttu-id="ddb10-126">Verwaltete Clusterressource</span><span class="sxs-lookup"><span data-stu-id="ddb10-126">Managed cluster resource</span></span>

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

### <span data-ttu-id="ddb10-127">-Name</span><span class="sxs-lookup"><span data-stu-id="ddb10-127">-Name</span></span>
<span data-ttu-id="ddb10-128">Geben Sie den Namen des Clusters an.</span><span class="sxs-lookup"><span data-stu-id="ddb10-128">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="ddb10-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ddb10-129">-PassThru</span></span>
<span data-ttu-id="ddb10-130">{{Fill passthru Description}}</span><span class="sxs-lookup"><span data-stu-id="ddb10-130">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="ddb10-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ddb10-131">-ResourceGroupName</span></span>
<span data-ttu-id="ddb10-132">Geben Sie den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="ddb10-132">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="ddb10-133">-Fingerabdruck</span><span class="sxs-lookup"><span data-stu-id="ddb10-133">-Thumbprint</span></span>
<span data-ttu-id="ddb10-134">Fingerabdruck des Client Zertifikats.</span><span class="sxs-lookup"><span data-stu-id="ddb10-134">Client certificate thumbprint.</span></span>

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

### <span data-ttu-id="ddb10-135">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ddb10-135">-Confirm</span></span>
<span data-ttu-id="ddb10-136">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ddb10-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ddb10-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ddb10-137">-WhatIf</span></span>
<span data-ttu-id="ddb10-138">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ddb10-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ddb10-139">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ddb10-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ddb10-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ddb10-140">CommonParameters</span></span>
<span data-ttu-id="ddb10-141">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ddb10-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ddb10-142">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ddb10-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ddb10-143">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ddb10-143">INPUTS</span></span>

### <span data-ttu-id="ddb10-144">System. String</span><span class="sxs-lookup"><span data-stu-id="ddb10-144">System.String</span></span>

## <span data-ttu-id="ddb10-145">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ddb10-145">OUTPUTS</span></span>

### <span data-ttu-id="ddb10-146">Microsoft. Azure. Commands. ServiceFabric. Models. PSManagedCluster</span><span class="sxs-lookup"><span data-stu-id="ddb10-146">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedCluster</span></span>

## <span data-ttu-id="ddb10-147">Notizen</span><span class="sxs-lookup"><span data-stu-id="ddb10-147">NOTES</span></span>

## <span data-ttu-id="ddb10-148">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ddb10-148">RELATED LINKS</span></span>
