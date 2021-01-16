---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/add-azservicefabricmanagedclusterclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricManagedClusterClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricManagedClusterClientCertificate.md
ms.openlocfilehash: e948acb179a0ae6a338fa02f01d1cb7d6efbd4fe
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98303555"
---
# <span data-ttu-id="64b5e-101">Add-AzServiceFabricManagedClusterClientCertificate</span><span class="sxs-lookup"><span data-stu-id="64b5e-101">Add-AzServiceFabricManagedClusterClientCertificate</span></span>

## <span data-ttu-id="64b5e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="64b5e-102">SYNOPSIS</span></span>
<span data-ttu-id="64b5e-103">Fügen Sie dem Cluster einen allgemeinen Zertifikatnamen oder Einen Fingerabdruck hinzu.</span><span class="sxs-lookup"><span data-stu-id="64b5e-103">Add certificate common name or thumbprint to the cluster.</span></span> <span data-ttu-id="64b5e-104">Dadurch wird das Zertifikat erneut für den Cluster für Clientauthentifizierungszwecke registriert.</span><span class="sxs-lookup"><span data-stu-id="64b5e-104">This will register the certificate agains the cluster for client authentication purposes.</span></span>

## <span data-ttu-id="64b5e-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="64b5e-105">SYNTAX</span></span>

### <span data-ttu-id="64b5e-106">ClientCertByTpByObj (Standard)</span><span class="sxs-lookup"><span data-stu-id="64b5e-106">ClientCertByTpByObj (Default)</span></span>
```
Add-AzServiceFabricManagedClusterClientCertificate [-InputObject] <PSManagedCluster> [-Admin]
 -Thumbprint <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="64b5e-107">ClientCertByTpByName</span><span class="sxs-lookup"><span data-stu-id="64b5e-107">ClientCertByTpByName</span></span>
```
Add-AzServiceFabricManagedClusterClientCertificate [-ResourceGroupName] <String> [-Name] <String> [-Admin]
 -Thumbprint <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="64b5e-108">ClientCertByCnByName</span><span class="sxs-lookup"><span data-stu-id="64b5e-108">ClientCertByCnByName</span></span>
```
Add-AzServiceFabricManagedClusterClientCertificate [-ResourceGroupName] <String> [-Name] <String> [-Admin]
 -CommonName <String> [-IssuerThumbprint <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="64b5e-109">ClientCertByCnByObj</span><span class="sxs-lookup"><span data-stu-id="64b5e-109">ClientCertByCnByObj</span></span>
```
Add-AzServiceFabricManagedClusterClientCertificate [-InputObject] <PSManagedCluster> [-Admin]
 -CommonName <String> [-IssuerThumbprint <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="64b5e-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="64b5e-110">DESCRIPTION</span></span>
<span data-ttu-id="64b5e-111">Fügen Sie dem Cluster einen allgemeinen Zertifikatnamen oder Einen Fingerabdruck hinzu.</span><span class="sxs-lookup"><span data-stu-id="64b5e-111">Add certificate common name or thumbprint to the cluster.</span></span> <span data-ttu-id="64b5e-112">Dadurch wird das Zertifikat erneut für den Cluster für Clientauthentifizierungszwecke registriert.</span><span class="sxs-lookup"><span data-stu-id="64b5e-112">This will register the certificate agains the cluster for client authentication purposes.</span></span>

## <span data-ttu-id="64b5e-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="64b5e-113">EXAMPLES</span></span>

### <span data-ttu-id="64b5e-114">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="64b5e-114">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
Add-AzServiceFabricManagedClusterClientCertificate -ResourceGroupName $rgName -ClusterName $clusterName -Thumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A -Admin
```

<span data-ttu-id="64b5e-115">Mit diesem Befehl wird dem Cluster das Zertifikat mit dem Fingerabdruck '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A' hinzugefügt, damit der Client das Zertifikat als Administrator für die Kommunikation mit dem Cluster verwenden kann.</span><span class="sxs-lookup"><span data-stu-id="64b5e-115">This command will add the certificate with thumbprint '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A' to the cluster, so the client can use the certificate as admin to communicate with the cluster.</span></span>

### <span data-ttu-id="64b5e-116">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="64b5e-116">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
Add-AzServiceFabricManagedClusterClientCertificate -ResourceGroupName $rgName -ClusterName $clusterName -CommonName 'Contoso.com' -IssuerThumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A, 5F3660C715EBBDA31DB1FFDCF508302348DE8E7B
```

<span data-ttu-id="64b5e-117">Mit diesem Befehl wird ein schreibgeschütztes Clientzertifikat mit dem gemeinsamen Namen "Contoso.com" und zwei Ausstellern hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="64b5e-117">This command will add a read only client certificate with common name 'Contoso.com' and 2 issuers.</span></span>

### <span data-ttu-id="64b5e-118">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="64b5e-118">Example 3</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$cluster = Get-AzServiceFabricManagedCluster -ResourceGroupName $rgName -Name $clusterName
$cluster | Add-AzServiceFabricManagedClusterClientCertificate -CommonName 'Contoso.com' -IssuerThumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A, 5F3660C715EBBDA31DB1FFDCF508302348DE8E7B
```

<span data-ttu-id="64b5e-119">Mit diesem Befehl wird ein schreibgeschütztes Clientzertifikat mit dem gemeinsamen Namen "Contoso.com" und zwei Ausstellern mit Piping hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="64b5e-119">This command will add a read only client certificate with common name 'Contoso.com' and 2 issuers, with piping.</span></span>

## <span data-ttu-id="64b5e-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="64b5e-120">PARAMETERS</span></span>

### <span data-ttu-id="64b5e-121">-Admin</span><span class="sxs-lookup"><span data-stu-id="64b5e-121">-Admin</span></span>
<span data-ttu-id="64b5e-122">Wird verwendet, um anzugeben, ob das Clientzertifikat über Administratorebene verfügt.</span><span class="sxs-lookup"><span data-stu-id="64b5e-122">Use to specify if the client certificate has administrator level.</span></span>

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

### <span data-ttu-id="64b5e-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="64b5e-123">-AsJob</span></span>
<span data-ttu-id="64b5e-124">Führen Sie das Cmdlet im Hintergrund aus, und geben Sie einen Auftrag zurück, um den Fortschritt nachverfolgt zu können.</span><span class="sxs-lookup"><span data-stu-id="64b5e-124">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="64b5e-125">-CommonName</span><span class="sxs-lookup"><span data-stu-id="64b5e-125">-CommonName</span></span>
<span data-ttu-id="64b5e-126">Gemeinsamer Name des Clientzertifikats.</span><span class="sxs-lookup"><span data-stu-id="64b5e-126">Client certificate common name.</span></span>

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

### <span data-ttu-id="64b5e-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64b5e-127">-DefaultProfile</span></span>
<span data-ttu-id="64b5e-128">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="64b5e-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="64b5e-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="64b5e-129">-InputObject</span></span>
<span data-ttu-id="64b5e-130">Verwaltete Clusterressource</span><span class="sxs-lookup"><span data-stu-id="64b5e-130">Managed cluster resource</span></span>

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

### <span data-ttu-id="64b5e-131">-IssuerThumbprint</span><span class="sxs-lookup"><span data-stu-id="64b5e-131">-IssuerThumbprint</span></span>
<span data-ttu-id="64b5e-132">Liste der Ausstellerdrückdrucke für das Clientzertifikat.</span><span class="sxs-lookup"><span data-stu-id="64b5e-132">List of Issuer thumbprints for the client certificate.</span></span>
<span data-ttu-id="64b5e-133">Wird nur in Kombination mit CommonName verwendet.</span><span class="sxs-lookup"><span data-stu-id="64b5e-133">Only use in combination with CommonName.</span></span>

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

### <span data-ttu-id="64b5e-134">-Name</span><span class="sxs-lookup"><span data-stu-id="64b5e-134">-Name</span></span>
<span data-ttu-id="64b5e-135">Geben Sie den Namen des Cluster an.</span><span class="sxs-lookup"><span data-stu-id="64b5e-135">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="64b5e-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64b5e-136">-ResourceGroupName</span></span>
<span data-ttu-id="64b5e-137">Geben Sie den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="64b5e-137">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="64b5e-138">-Thumbprint</span><span class="sxs-lookup"><span data-stu-id="64b5e-138">-Thumbprint</span></span>
<span data-ttu-id="64b5e-139">Fingerabdruck des Clientzertifikats.</span><span class="sxs-lookup"><span data-stu-id="64b5e-139">Client certificate thumbprint.</span></span>

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

### <span data-ttu-id="64b5e-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="64b5e-140">-Confirm</span></span>
<span data-ttu-id="64b5e-141">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="64b5e-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="64b5e-142">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="64b5e-142">-WhatIf</span></span>
<span data-ttu-id="64b5e-143">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="64b5e-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="64b5e-144">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="64b5e-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="64b5e-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64b5e-145">CommonParameters</span></span>
<span data-ttu-id="64b5e-146">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64b5e-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64b5e-147">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="64b5e-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64b5e-148">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="64b5e-148">INPUTS</span></span>

### <span data-ttu-id="64b5e-149">System.String</span><span class="sxs-lookup"><span data-stu-id="64b5e-149">System.String</span></span>

## <span data-ttu-id="64b5e-150">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="64b5e-150">OUTPUTS</span></span>

### <span data-ttu-id="64b5e-151">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedCluster</span><span class="sxs-lookup"><span data-stu-id="64b5e-151">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedCluster</span></span>

## <span data-ttu-id="64b5e-152">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="64b5e-152">NOTES</span></span>

## <span data-ttu-id="64b5e-153">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="64b5e-153">RELATED LINKS</span></span>
