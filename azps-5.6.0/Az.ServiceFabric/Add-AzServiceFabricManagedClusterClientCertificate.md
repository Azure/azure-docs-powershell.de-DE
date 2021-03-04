---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/add-azservicefabricmanagedclusterclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricManagedClusterClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricManagedClusterClientCertificate.md
ms.openlocfilehash: 11534ff7102295cd312410c5ecbae932fd9459e5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101927536"
---
# <span data-ttu-id="ec133-101">Add-AzServiceFabricManagedClusterClientCertificate</span><span class="sxs-lookup"><span data-stu-id="ec133-101">Add-AzServiceFabricManagedClusterClientCertificate</span></span>

## <span data-ttu-id="ec133-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ec133-102">SYNOPSIS</span></span>
<span data-ttu-id="ec133-103">Fügen Sie dem Cluster gemeinsamen Namen oder Fingerabdruck des Zertifikats hinzu.</span><span class="sxs-lookup"><span data-stu-id="ec133-103">Add certificate common name or thumbprint to the cluster.</span></span> <span data-ttu-id="ec133-104">Dadurch wird das Zertifikat erneut für den Cluster für Clientauthentifizierungszwecke registriert.</span><span class="sxs-lookup"><span data-stu-id="ec133-104">This will register the certificate agains the cluster for client authentication purposes.</span></span>

## <span data-ttu-id="ec133-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ec133-105">SYNTAX</span></span>

### <span data-ttu-id="ec133-106">ClientCertByTpByObj (Standard)</span><span class="sxs-lookup"><span data-stu-id="ec133-106">ClientCertByTpByObj (Default)</span></span>
```
Add-AzServiceFabricManagedClusterClientCertificate [-InputObject] <PSManagedCluster> [-Admin]
 -Thumbprint <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ec133-107">ClientCertByTpByName</span><span class="sxs-lookup"><span data-stu-id="ec133-107">ClientCertByTpByName</span></span>
```
Add-AzServiceFabricManagedClusterClientCertificate [-ResourceGroupName] <String> [-Name] <String> [-Admin]
 -Thumbprint <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ec133-108">ClientCertByCnByName</span><span class="sxs-lookup"><span data-stu-id="ec133-108">ClientCertByCnByName</span></span>
```
Add-AzServiceFabricManagedClusterClientCertificate [-ResourceGroupName] <String> [-Name] <String> [-Admin]
 -CommonName <String> [-IssuerThumbprint <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ec133-109">ClientCertByCnByObj</span><span class="sxs-lookup"><span data-stu-id="ec133-109">ClientCertByCnByObj</span></span>
```
Add-AzServiceFabricManagedClusterClientCertificate [-InputObject] <PSManagedCluster> [-Admin]
 -CommonName <String> [-IssuerThumbprint <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ec133-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ec133-110">DESCRIPTION</span></span>
<span data-ttu-id="ec133-111">Fügen Sie dem Cluster gemeinsamen Namen oder Fingerabdruck des Zertifikats hinzu.</span><span class="sxs-lookup"><span data-stu-id="ec133-111">Add certificate common name or thumbprint to the cluster.</span></span> <span data-ttu-id="ec133-112">Dadurch wird das Zertifikat erneut für den Cluster für Clientauthentifizierungszwecke registriert.</span><span class="sxs-lookup"><span data-stu-id="ec133-112">This will register the certificate agains the cluster for client authentication purposes.</span></span>

## <span data-ttu-id="ec133-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ec133-113">EXAMPLES</span></span>

### <span data-ttu-id="ec133-114">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ec133-114">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
Add-AzServiceFabricManagedClusterClientCertificate -ResourceGroupName $rgName -ClusterName $clusterName -Thumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A -Admin
```

<span data-ttu-id="ec133-115">Mit diesem Befehl wird das Zertifikat mit dem Fingerabdruck '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A' zum Cluster hinzugefügt, damit der Client das Zertifikat als Administrator für die Kommunikation mit dem Cluster verwenden kann.</span><span class="sxs-lookup"><span data-stu-id="ec133-115">This command will add the certificate with thumbprint '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A' to the cluster, so the client can use the certificate as admin to communicate with the cluster.</span></span>

### <span data-ttu-id="ec133-116">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="ec133-116">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
Add-AzServiceFabricManagedClusterClientCertificate -ResourceGroupName $rgName -ClusterName $clusterName -CommonName 'Contoso.com' -IssuerThumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A, 5F3660C715EBBDA31DB1FFDCF508302348DE8E7B
```

<span data-ttu-id="ec133-117">Mit diesem Befehl wird ein schreibgeschütztes Clientzertifikat mit dem gemeinsamen Namen "Contoso.com" und zwei Ausstellern hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="ec133-117">This command will add a read only client certificate with common name 'Contoso.com' and 2 issuers.</span></span>

### <span data-ttu-id="ec133-118">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="ec133-118">Example 3</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$cluster = Get-AzServiceFabricManagedCluster -ResourceGroupName $rgName -Name $clusterName
$cluster | Add-AzServiceFabricManagedClusterClientCertificate -CommonName 'Contoso.com' -IssuerThumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A, 5F3660C715EBBDA31DB1FFDCF508302348DE8E7B
```

<span data-ttu-id="ec133-119">Mit diesem Befehl wird ein schreibgeschütztes Clientzertifikat mit dem gemeinsamen Namen "Contoso.com" und zwei Ausstellern mit Piping hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="ec133-119">This command will add a read only client certificate with common name 'Contoso.com' and 2 issuers, with piping.</span></span>

## <span data-ttu-id="ec133-120">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="ec133-120">PARAMETERS</span></span>

### <span data-ttu-id="ec133-121">-Administrator</span><span class="sxs-lookup"><span data-stu-id="ec133-121">-Admin</span></span>
<span data-ttu-id="ec133-122">Verwenden Sie diese Option, um anzugeben, ob das Clientzertifikat über Administratorebene verfügt.</span><span class="sxs-lookup"><span data-stu-id="ec133-122">Use to specify if the client certificate has administrator level.</span></span>

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

### <span data-ttu-id="ec133-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ec133-123">-AsJob</span></span>
<span data-ttu-id="ec133-124">Führen Sie das Cmdlet im Hintergrund aus, und geben Sie einen Auftrag zurück, um den Fortschritt zu verfolgen.</span><span class="sxs-lookup"><span data-stu-id="ec133-124">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="ec133-125">-CommonName</span><span class="sxs-lookup"><span data-stu-id="ec133-125">-CommonName</span></span>
<span data-ttu-id="ec133-126">Gemeinsamer Name des Clientzertifikats.</span><span class="sxs-lookup"><span data-stu-id="ec133-126">Client certificate common name.</span></span>

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

### <span data-ttu-id="ec133-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec133-127">-DefaultProfile</span></span>
<span data-ttu-id="ec133-128">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ec133-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ec133-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ec133-129">-InputObject</span></span>
<span data-ttu-id="ec133-130">Verwaltete Clusterressource</span><span class="sxs-lookup"><span data-stu-id="ec133-130">Managed cluster resource</span></span>

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

### <span data-ttu-id="ec133-131">-IssuerThumbprint</span><span class="sxs-lookup"><span data-stu-id="ec133-131">-IssuerThumbprint</span></span>
<span data-ttu-id="ec133-132">Liste der Ausstellerfingerabdrücke für das Clientzertifikat.</span><span class="sxs-lookup"><span data-stu-id="ec133-132">List of Issuer thumbprints for the client certificate.</span></span>
<span data-ttu-id="ec133-133">Nur in Kombination mit CommonName verwenden.</span><span class="sxs-lookup"><span data-stu-id="ec133-133">Only use in combination with CommonName.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ClientCertByCnByName, ClientCertByCnByObj
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec133-134">-Name</span><span class="sxs-lookup"><span data-stu-id="ec133-134">-Name</span></span>
<span data-ttu-id="ec133-135">Geben Sie den Namen des Clusters an.</span><span class="sxs-lookup"><span data-stu-id="ec133-135">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: ClientCertByTpByName, ClientCertByCnByName
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec133-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ec133-136">-ResourceGroupName</span></span>
<span data-ttu-id="ec133-137">Geben Sie den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="ec133-137">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ClientCertByTpByName, ClientCertByCnByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec133-138">-Thumbprint</span><span class="sxs-lookup"><span data-stu-id="ec133-138">-Thumbprint</span></span>
<span data-ttu-id="ec133-139">Fingerabdruck des Clientzertifikats.</span><span class="sxs-lookup"><span data-stu-id="ec133-139">Client certificate thumbprint.</span></span>

```yaml
Type: System.String
Parameter Sets: ClientCertByTpByObj, ClientCertByTpByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec133-140">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ec133-140">-Confirm</span></span>
<span data-ttu-id="ec133-141">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ec133-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ec133-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ec133-142">-WhatIf</span></span>
<span data-ttu-id="ec133-143">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ec133-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ec133-144">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ec133-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ec133-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec133-145">CommonParameters</span></span>
<span data-ttu-id="ec133-146">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ec133-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec133-147">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ec133-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec133-148">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ec133-148">INPUTS</span></span>

### <span data-ttu-id="ec133-149">System.String</span><span class="sxs-lookup"><span data-stu-id="ec133-149">System.String</span></span>

## <span data-ttu-id="ec133-150">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ec133-150">OUTPUTS</span></span>

### <span data-ttu-id="ec133-151">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedCluster</span><span class="sxs-lookup"><span data-stu-id="ec133-151">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedCluster</span></span>

## <span data-ttu-id="ec133-152">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="ec133-152">NOTES</span></span>

## <span data-ttu-id="ec133-153">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="ec133-153">RELATED LINKS</span></span>
