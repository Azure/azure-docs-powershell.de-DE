---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/add-azservicefabricmanagedclusterclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricManagedClusterClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricManagedClusterClientCertificate.md
ms.openlocfilehash: e948acb179a0ae6a338fa02f01d1cb7d6efbd4fe
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94007794"
---
# <span data-ttu-id="5fdce-101">Add-AzServiceFabricManagedClusterClientCertificate</span><span class="sxs-lookup"><span data-stu-id="5fdce-101">Add-AzServiceFabricManagedClusterClientCertificate</span></span>

## <span data-ttu-id="5fdce-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5fdce-102">SYNOPSIS</span></span>
<span data-ttu-id="5fdce-103">Fügen Sie dem Cluster den allgemeinen Namen oder Fingerabdruck des Zertifikats hinzu.</span><span class="sxs-lookup"><span data-stu-id="5fdce-103">Add certificate common name or thumbprint to the cluster.</span></span> <span data-ttu-id="5fdce-104">Dadurch wird das Zertifikat beim erneuten Registrieren des Clusters für Client Authentifizierungszwecke registriert.</span><span class="sxs-lookup"><span data-stu-id="5fdce-104">This will register the certificate agains the cluster for client authentication purposes.</span></span>

## <span data-ttu-id="5fdce-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="5fdce-105">SYNTAX</span></span>

### <span data-ttu-id="5fdce-106">ClientCertByTpByObj (Standard)</span><span class="sxs-lookup"><span data-stu-id="5fdce-106">ClientCertByTpByObj (Default)</span></span>
```
Add-AzServiceFabricManagedClusterClientCertificate [-InputObject] <PSManagedCluster> [-Admin]
 -Thumbprint <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5fdce-107">ClientCertByTpByName</span><span class="sxs-lookup"><span data-stu-id="5fdce-107">ClientCertByTpByName</span></span>
```
Add-AzServiceFabricManagedClusterClientCertificate [-ResourceGroupName] <String> [-Name] <String> [-Admin]
 -Thumbprint <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5fdce-108">ClientCertByCnByName</span><span class="sxs-lookup"><span data-stu-id="5fdce-108">ClientCertByCnByName</span></span>
```
Add-AzServiceFabricManagedClusterClientCertificate [-ResourceGroupName] <String> [-Name] <String> [-Admin]
 -CommonName <String> [-IssuerThumbprint <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5fdce-109">ClientCertByCnByObj</span><span class="sxs-lookup"><span data-stu-id="5fdce-109">ClientCertByCnByObj</span></span>
```
Add-AzServiceFabricManagedClusterClientCertificate [-InputObject] <PSManagedCluster> [-Admin]
 -CommonName <String> [-IssuerThumbprint <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5fdce-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5fdce-110">DESCRIPTION</span></span>
<span data-ttu-id="5fdce-111">Fügen Sie dem Cluster den allgemeinen Namen oder Fingerabdruck des Zertifikats hinzu.</span><span class="sxs-lookup"><span data-stu-id="5fdce-111">Add certificate common name or thumbprint to the cluster.</span></span> <span data-ttu-id="5fdce-112">Dadurch wird das Zertifikat beim erneuten Registrieren des Clusters für Client Authentifizierungszwecke registriert.</span><span class="sxs-lookup"><span data-stu-id="5fdce-112">This will register the certificate agains the cluster for client authentication purposes.</span></span>

## <span data-ttu-id="5fdce-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5fdce-113">EXAMPLES</span></span>

### <span data-ttu-id="5fdce-114">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="5fdce-114">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
Add-AzServiceFabricManagedClusterClientCertificate -ResourceGroupName $rgName -ClusterName $clusterName -Thumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A -Admin
```

<span data-ttu-id="5fdce-115">Mit diesem Befehl wird dem Cluster das Zertifikat mit dem Fingerabdruck "5F3660C715EBBDA31DB1FFDCF508302348DE8E7A" hinzugefügt, sodass der Client das Zertifikat als Administrator für die Kommunikation mit dem Cluster verwenden kann.</span><span class="sxs-lookup"><span data-stu-id="5fdce-115">This command will add the certificate with thumbprint '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A' to the cluster, so the client can use the certificate as admin to communicate with the cluster.</span></span>

### <span data-ttu-id="5fdce-116">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="5fdce-116">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
Add-AzServiceFabricManagedClusterClientCertificate -ResourceGroupName $rgName -ClusterName $clusterName -CommonName 'Contoso.com' -IssuerThumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A, 5F3660C715EBBDA31DB1FFDCF508302348DE8E7B
```

<span data-ttu-id="5fdce-117">Mit diesem Befehl wird ein nur-Lese-Clientzertifikat mit dem allgemeinen Namen "contoso.com" und 2 Emittenten hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="5fdce-117">This command will add a read only client certificate with common name 'Contoso.com' and 2 issuers.</span></span>

### <span data-ttu-id="5fdce-118">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="5fdce-118">Example 3</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$cluster = Get-AzServiceFabricManagedCluster -ResourceGroupName $rgName -Name $clusterName
$cluster | Add-AzServiceFabricManagedClusterClientCertificate -CommonName 'Contoso.com' -IssuerThumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A, 5F3660C715EBBDA31DB1FFDCF508302348DE8E7B
```

<span data-ttu-id="5fdce-119">Mit diesem Befehl wird ein schreibgeschütztes Clientzertifikat mit dem allgemeinen Namen "contoso.com" und 2 Emittenten mit Piping hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="5fdce-119">This command will add a read only client certificate with common name 'Contoso.com' and 2 issuers, with piping.</span></span>

## <span data-ttu-id="5fdce-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="5fdce-120">PARAMETERS</span></span>

### <span data-ttu-id="5fdce-121">– Administrator</span><span class="sxs-lookup"><span data-stu-id="5fdce-121">-Admin</span></span>
<span data-ttu-id="5fdce-122">Hiermit geben Sie an, ob das Clientzertifikat Administratorebene hat.</span><span class="sxs-lookup"><span data-stu-id="5fdce-122">Use to specify if the client certificate has administrator level.</span></span>

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

### <span data-ttu-id="5fdce-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5fdce-123">-AsJob</span></span>
<span data-ttu-id="5fdce-124">Führen Sie das Cmdlet im Hintergrund aus, und geben Sie einen Auftrag zum Nachverfolgen des Fortschritts zurück.</span><span class="sxs-lookup"><span data-stu-id="5fdce-124">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="5fdce-125">-CommonName</span><span class="sxs-lookup"><span data-stu-id="5fdce-125">-CommonName</span></span>
<span data-ttu-id="5fdce-126">Allgemeiner Name des Client Zertifikats.</span><span class="sxs-lookup"><span data-stu-id="5fdce-126">Client certificate common name.</span></span>

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

### <span data-ttu-id="5fdce-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5fdce-127">-DefaultProfile</span></span>
<span data-ttu-id="5fdce-128">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5fdce-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5fdce-129">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="5fdce-129">-InputObject</span></span>
<span data-ttu-id="5fdce-130">Verwaltete Clusterressource</span><span class="sxs-lookup"><span data-stu-id="5fdce-130">Managed cluster resource</span></span>

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

### <span data-ttu-id="5fdce-131">-IssuerThumbprint</span><span class="sxs-lookup"><span data-stu-id="5fdce-131">-IssuerThumbprint</span></span>
<span data-ttu-id="5fdce-132">Liste der Aussteller-Fingerabdrücke für das Clientzertifikat</span><span class="sxs-lookup"><span data-stu-id="5fdce-132">List of Issuer thumbprints for the client certificate.</span></span>
<span data-ttu-id="5fdce-133">Verwenden Sie nur in Kombination mit CommonName.</span><span class="sxs-lookup"><span data-stu-id="5fdce-133">Only use in combination with CommonName.</span></span>

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

### <span data-ttu-id="5fdce-134">-Name</span><span class="sxs-lookup"><span data-stu-id="5fdce-134">-Name</span></span>
<span data-ttu-id="5fdce-135">Geben Sie den Namen des Clusters an.</span><span class="sxs-lookup"><span data-stu-id="5fdce-135">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="5fdce-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5fdce-136">-ResourceGroupName</span></span>
<span data-ttu-id="5fdce-137">Geben Sie den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="5fdce-137">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="5fdce-138">-Fingerabdruck</span><span class="sxs-lookup"><span data-stu-id="5fdce-138">-Thumbprint</span></span>
<span data-ttu-id="5fdce-139">Fingerabdruck des Client Zertifikats.</span><span class="sxs-lookup"><span data-stu-id="5fdce-139">Client certificate thumbprint.</span></span>

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

### <span data-ttu-id="5fdce-140">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="5fdce-140">-Confirm</span></span>
<span data-ttu-id="5fdce-141">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5fdce-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5fdce-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5fdce-142">-WhatIf</span></span>
<span data-ttu-id="5fdce-143">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5fdce-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5fdce-144">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5fdce-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5fdce-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5fdce-145">CommonParameters</span></span>
<span data-ttu-id="5fdce-146">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5fdce-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5fdce-147">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5fdce-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5fdce-148">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5fdce-148">INPUTS</span></span>

### <span data-ttu-id="5fdce-149">System. String</span><span class="sxs-lookup"><span data-stu-id="5fdce-149">System.String</span></span>

## <span data-ttu-id="5fdce-150">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5fdce-150">OUTPUTS</span></span>

### <span data-ttu-id="5fdce-151">Microsoft. Azure. Commands. ServiceFabric. Models. PSManagedCluster</span><span class="sxs-lookup"><span data-stu-id="5fdce-151">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedCluster</span></span>

## <span data-ttu-id="5fdce-152">Notizen</span><span class="sxs-lookup"><span data-stu-id="5fdce-152">NOTES</span></span>

## <span data-ttu-id="5fdce-153">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5fdce-153">RELATED LINKS</span></span>
