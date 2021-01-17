---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/add-azservicefabricmanagednodetypevmsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricManagedNodeTypeVMSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricManagedNodeTypeVMSecret.md
ms.openlocfilehash: 36ed679066d1850851ff0e90f39eb6f9ef8ffa1a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98471831"
---
# <span data-ttu-id="73879-101">Add-AzServiceFabricManagedNodeTypeVMSecret</span><span class="sxs-lookup"><span data-stu-id="73879-101">Add-AzServiceFabricManagedNodeTypeVMSecret</span></span>

## <span data-ttu-id="73879-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="73879-102">SYNOPSIS</span></span>
<span data-ttu-id="73879-103">Fügen Sie dem Knotentyp ein geheimes Zertifikat hinzu.</span><span class="sxs-lookup"><span data-stu-id="73879-103">Add certificate secret to the node type.</span></span>

## <span data-ttu-id="73879-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="73879-104">SYNTAX</span></span>

### <span data-ttu-id="73879-105">ByObj (Standard)</span><span class="sxs-lookup"><span data-stu-id="73879-105">ByObj (Default)</span></span>
```
Add-AzServiceFabricManagedNodeTypeVMSecret [-InputObject] <PSManagedNodeType> -SourceVaultId <String>
 -CertificateUrl <String> -CertificateStore <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="73879-106">ByName</span><span class="sxs-lookup"><span data-stu-id="73879-106">ByName</span></span>
```
Add-AzServiceFabricManagedNodeTypeVMSecret [-ResourceGroupName] <String> [-ClusterName] <String>
 [-Name] <String> -SourceVaultId <String> -CertificateUrl <String> -CertificateStore <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="73879-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="73879-107">DESCRIPTION</span></span>
<span data-ttu-id="73879-108">Fügen Sie dem Knotentyp ein geheimes Zertifikat hinzu.</span><span class="sxs-lookup"><span data-stu-id="73879-108">Add certificate secret to the node type.</span></span> <span data-ttu-id="73879-109">Das Geheime muss in einem Azure Key Vault gespeichert sein.</span><span class="sxs-lookup"><span data-stu-id="73879-109">The secret must be stored in an Azure Key Vault.</span></span> <span data-ttu-id="73879-110">Weitere Informationen zum Schlüsseltresor finden Sie unter "Was ist der Azure Key Vault?".</span><span class="sxs-lookup"><span data-stu-id="73879-110">For more information relating to Key Vault, see What is Azure Key Vault?</span></span> <span data-ttu-id="73879-111">(https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/).</span><span class="sxs-lookup"><span data-stu-id="73879-111">(https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/).</span></span> <span data-ttu-id="73879-112">Weitere Informationen zu den Cmdlets finden Sie unter Azure Key Vault Cmdlets (in der Microsoft Developer Network-Bibliothek oder https://msdn.microsoft.com/library/azure/dn868052.aspx) Set-AzKeyVaultSecret Cmdlet).</span><span class="sxs-lookup"><span data-stu-id="73879-112">For more information about the cmdlets, see Azure Key Vault Cmdlets (https://msdn.microsoft.com/library/azure/dn868052.aspx) in the Microsoft Developer Network library or the Set-AzKeyVaultSecret cmdlet.</span></span>

## <span data-ttu-id="73879-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="73879-113">EXAMPLES</span></span>

### <span data-ttu-id="73879-114">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="73879-114">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
Add-AzServiceFabricManagedNodeTypeVMSecret -ResourceGroupName $rgName -ClusterName $clusterName -NodeTypeName $NodeTypeName -SourceVaultId /subscriptions/XXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/testRG/providers/Microsoft.KeyVault/vaults/testkv -CertificateUrl https://testskv.vault.azure.net:443/secrets/TestCert/xxxxxxxxxxxxxxxxxxxxxxxx -CertificateStore My -Verbose
```

<span data-ttu-id="73879-115">Mit diesem Komma wird ein geheimes Zertifikat aus dem angegebenen Schlüssel und geheimen Bezeichner hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="73879-115">This commad adds a certificate secret from the keyvault and secret identifier specified.</span></span>

### <span data-ttu-id="73879-116">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="73879-116">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
$nodeType = Get-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -Name $NodeTypeName

$nodeType | Add-AzServiceFabricManagedNodeTypeVMSecret -SourceVaultId /subscriptions/XXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/testRG/providers/Microsoft.KeyVault/vaults/testkv -CertificateUrl https://testskv.vault.azure.net:443/secrets/TestCert/xxxxxxxxxxxxxxxxxxxxxxxx -CertificateStore My -Verbose
```

<span data-ttu-id="73879-117">Mit diesem Komma wird ein geheimes Zertifikat aus dem angegebenen Schlüssel und geheimen Bezeichner mit Pipette hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="73879-117">This commad adds a certificate secret from the keyvault and secret identifier specified, with piping.</span></span>

## <span data-ttu-id="73879-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="73879-118">PARAMETERS</span></span>

### <span data-ttu-id="73879-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="73879-119">-AsJob</span></span>
<span data-ttu-id="73879-120">Führen Sie das Cmdlet im Hintergrund aus, und geben Sie einen Auftrag zurück, um den Fortschritt nachverfolgt zu können.</span><span class="sxs-lookup"><span data-stu-id="73879-120">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="73879-121">-CertificateStore</span><span class="sxs-lookup"><span data-stu-id="73879-121">-CertificateStore</span></span>
<span data-ttu-id="73879-122">Gibt den Zertifikatspeicher auf dem virtuellen Computer an, dem das Zertifikat hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="73879-122">Specifies the certificate store on the Virtual Machine to which the certificate should be added.</span></span>
<span data-ttu-id="73879-123">Der angegebene Zertifikatspeicher befindet sich implizit im LocalMachine-Konto.</span><span class="sxs-lookup"><span data-stu-id="73879-123">The specified certificate store is implicitly in the LocalMachine account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73879-124">-CertificateUrl</span><span class="sxs-lookup"><span data-stu-id="73879-124">-CertificateUrl</span></span>
<span data-ttu-id="73879-125">Dies ist die URL eines Zertifikats, das als geheimer Schlüssel in den Schlüsseltresor hochgeladen wurde.</span><span class="sxs-lookup"><span data-stu-id="73879-125">This is the URL of a certificate that has been uploaded to Key Vault as a secret.</span></span>
<span data-ttu-id="73879-126">Informationen zum Hinzufügen eines Geheimschlüssels zum Schlüsseltresor finden Sie unter Hinzufügen eines Schlüssels oder geheimen Schlüssels \[ zum Schlüsseltresor \] ( https://docs.microsoft.com/azure/key-vault/key-vault-get-started/#add) .</span><span class="sxs-lookup"><span data-stu-id="73879-126">For adding a secret to the Key Vault, see \[Add a key or secret to the key vault\](https://docs.microsoft.com/azure/key-vault/key-vault-get-started/#add).</span></span>
<span data-ttu-id="73879-127">In diesem Fall muss Ihr Zertifikat die #A0 des folgenden JSON-Objekts sein, das in UTF-8 codiert ist: \<br\> \<br\> { \<br\> "data":" \<Base64-encoded-certificate\> ", \<br\> "dataType":"pfx", \<br\> "password":" \<pfx-file-password\> " \<br\> }/</span><span class="sxs-lookup"><span data-stu-id="73879-127">In this case, your certificate needs to be It is the Base64 encoding of the following JSON Object which is encoded in UTF-8: \<br\>\<br\> {\<br\>  "data":"\<Base64-encoded-certificate\>",\<br\>  "dataType":"pfx",\<br\>  "password":"\<pfx-file-password\>"\<br\>}/</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73879-128">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="73879-128">-ClusterName</span></span>
<span data-ttu-id="73879-129">Geben Sie den Namen des Cluster an.</span><span class="sxs-lookup"><span data-stu-id="73879-129">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73879-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73879-130">-DefaultProfile</span></span>
<span data-ttu-id="73879-131">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="73879-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="73879-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="73879-132">-InputObject</span></span>
<span data-ttu-id="73879-133">Knotentypressource</span><span class="sxs-lookup"><span data-stu-id="73879-133">Node Type resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType
Parameter Sets: ByObj
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="73879-134">-Name</span><span class="sxs-lookup"><span data-stu-id="73879-134">-Name</span></span>
<span data-ttu-id="73879-135">Geben Sie den Namen des Knotentyps an.</span><span class="sxs-lookup"><span data-stu-id="73879-135">Specify the name of the node type.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: NodeTypeName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73879-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="73879-136">-ResourceGroupName</span></span>
<span data-ttu-id="73879-137">Geben Sie den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="73879-137">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73879-138">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="73879-138">-SourceVaultId</span></span>
<span data-ttu-id="73879-139">Die Ressourcen-ID des Schlüsseltresor, die die Zertifikate enthält.</span><span class="sxs-lookup"><span data-stu-id="73879-139">Key Vault resource id containing the certificates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73879-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="73879-140">-Confirm</span></span>
<span data-ttu-id="73879-141">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="73879-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="73879-142">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="73879-142">-WhatIf</span></span>
<span data-ttu-id="73879-143">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="73879-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="73879-144">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="73879-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="73879-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73879-145">CommonParameters</span></span>
<span data-ttu-id="73879-146">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="73879-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73879-147">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="73879-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73879-148">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="73879-148">INPUTS</span></span>

### <span data-ttu-id="73879-149">System.String</span><span class="sxs-lookup"><span data-stu-id="73879-149">System.String</span></span>

## <span data-ttu-id="73879-150">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="73879-150">OUTPUTS</span></span>

### <span data-ttu-id="73879-151">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="73879-151">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType</span></span>

## <span data-ttu-id="73879-152">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="73879-152">NOTES</span></span>

## <span data-ttu-id="73879-153">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="73879-153">RELATED LINKS</span></span>
