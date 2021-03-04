---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/add-azservicefabricmanagednodetypevmsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricManagedNodeTypeVMSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricManagedNodeTypeVMSecret.md
ms.openlocfilehash: 35d755bc117ccc4379be8d7344d8e7170594d555
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101927512"
---
# <span data-ttu-id="4b7b6-101">Add-AzServiceFabricManagedNodeTypeVMSecret</span><span class="sxs-lookup"><span data-stu-id="4b7b6-101">Add-AzServiceFabricManagedNodeTypeVMSecret</span></span>

## <span data-ttu-id="4b7b6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4b7b6-102">SYNOPSIS</span></span>
<span data-ttu-id="4b7b6-103">Fügen Sie dem Knotentyp den Zertifikatsgeheimnis hinzu.</span><span class="sxs-lookup"><span data-stu-id="4b7b6-103">Add certificate secret to the node type.</span></span>

## <span data-ttu-id="4b7b6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4b7b6-104">SYNTAX</span></span>

### <span data-ttu-id="4b7b6-105">ByObj (Standard)</span><span class="sxs-lookup"><span data-stu-id="4b7b6-105">ByObj (Default)</span></span>
```
Add-AzServiceFabricManagedNodeTypeVMSecret [-InputObject] <PSManagedNodeType> -SourceVaultId <String>
 -CertificateUrl <String> -CertificateStore <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4b7b6-106">ByName</span><span class="sxs-lookup"><span data-stu-id="4b7b6-106">ByName</span></span>
```
Add-AzServiceFabricManagedNodeTypeVMSecret [-ResourceGroupName] <String> [-ClusterName] <String>
 [-Name] <String> -SourceVaultId <String> -CertificateUrl <String> -CertificateStore <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4b7b6-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4b7b6-107">DESCRIPTION</span></span>
<span data-ttu-id="4b7b6-108">Fügen Sie dem Knotentyp den Zertifikatsgeheimnis hinzu.</span><span class="sxs-lookup"><span data-stu-id="4b7b6-108">Add certificate secret to the node type.</span></span> <span data-ttu-id="4b7b6-109">Der Geheimschlüssel muss in einem Azure Key Vault gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="4b7b6-109">The secret must be stored in an Azure Key Vault.</span></span> <span data-ttu-id="4b7b6-110">Weitere Informationen zum Schlüsseltresor finden Sie unter Was ist Azure Key Vault?</span><span class="sxs-lookup"><span data-stu-id="4b7b6-110">For more information relating to Key Vault, see What is Azure Key Vault?</span></span> <span data-ttu-id="4b7b6-111">(https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/).</span><span class="sxs-lookup"><span data-stu-id="4b7b6-111">(https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/).</span></span> <span data-ttu-id="4b7b6-112">Weitere Informationen zu den Cmdlets finden Sie unter Azure Key Vault Cmdlets ( in der Microsoft Developer Network-Bibliothek oder im Set-AzKeyVaultSecret https://msdn.microsoft.com/library/azure/dn868052.aspx) cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4b7b6-112">For more information about the cmdlets, see Azure Key Vault Cmdlets (https://msdn.microsoft.com/library/azure/dn868052.aspx) in the Microsoft Developer Network library or the Set-AzKeyVaultSecret cmdlet.</span></span>

## <span data-ttu-id="4b7b6-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="4b7b6-113">EXAMPLES</span></span>

### <span data-ttu-id="4b7b6-114">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="4b7b6-114">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
Add-AzServiceFabricManagedNodeTypeVMSecret -ResourceGroupName $rgName -ClusterName $clusterName -NodeTypeName $NodeTypeName -SourceVaultId /subscriptions/XXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/testRG/providers/Microsoft.KeyVault/vaults/testkv -CertificateUrl https://testskv.vault.azure.net:443/secrets/TestCert/xxxxxxxxxxxxxxxxxxxxxxxx -CertificateStore My -Verbose
```

<span data-ttu-id="4b7b6-115">Dieses Komma fügt einen Zertifikatschlüssel aus dem angegebenen Keyvault- und geheimen Bezeichner hinzu.</span><span class="sxs-lookup"><span data-stu-id="4b7b6-115">This commad adds a certificate secret from the keyvault and secret identifier specified.</span></span>

### <span data-ttu-id="4b7b6-116">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="4b7b6-116">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
$nodeType = Get-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -Name $NodeTypeName

$nodeType | Add-AzServiceFabricManagedNodeTypeVMSecret -SourceVaultId /subscriptions/XXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/testRG/providers/Microsoft.KeyVault/vaults/testkv -CertificateUrl https://testskv.vault.azure.net:443/secrets/TestCert/xxxxxxxxxxxxxxxxxxxxxxxx -CertificateStore My -Verbose
```

<span data-ttu-id="4b7b6-117">Mit diesem Komma wird ein Zertifikatschlüssel aus dem angegebenen Keyvault und dem geheimen Bezeichner mit Piping ergänzt.</span><span class="sxs-lookup"><span data-stu-id="4b7b6-117">This commad adds a certificate secret from the keyvault and secret identifier specified, with piping.</span></span>

## <span data-ttu-id="4b7b6-118">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="4b7b6-118">PARAMETERS</span></span>

### <span data-ttu-id="4b7b6-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4b7b6-119">-AsJob</span></span>
<span data-ttu-id="4b7b6-120">Führen Sie das Cmdlet im Hintergrund aus, und geben Sie einen Auftrag zurück, um den Fortschritt zu verfolgen.</span><span class="sxs-lookup"><span data-stu-id="4b7b6-120">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="4b7b6-121">-CertificateStore</span><span class="sxs-lookup"><span data-stu-id="4b7b6-121">-CertificateStore</span></span>
<span data-ttu-id="4b7b6-122">Gibt den Zertifikatspeicher auf dem virtuellen Computer an, dem das Zertifikat hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="4b7b6-122">Specifies the certificate store on the Virtual Machine to which the certificate should be added.</span></span>
<span data-ttu-id="4b7b6-123">Der angegebene Zertifikatspeicher befindet sich implizit im LocalMachine-Konto.</span><span class="sxs-lookup"><span data-stu-id="4b7b6-123">The specified certificate store is implicitly in the LocalMachine account.</span></span>

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

### <span data-ttu-id="4b7b6-124">-CertificateUrl</span><span class="sxs-lookup"><span data-stu-id="4b7b6-124">-CertificateUrl</span></span>
<span data-ttu-id="4b7b6-125">Dies ist die URL eines Zertifikats, das als Geheimer in den Schlüsseltresor hochgeladen wurde.</span><span class="sxs-lookup"><span data-stu-id="4b7b6-125">This is the URL of a certificate that has been uploaded to Key Vault as a secret.</span></span>
<span data-ttu-id="4b7b6-126">Informationen zum Hinzufügen eines Geheimschlüssels zum Schlüsseltresor finden Sie unter Hinzufügen eines Schlüssels oder Eines Geheimschlüssels \[ zum Schlüsseltresor \] ( https://docs.microsoft.com/azure/key-vault/key-vault-get-started/#add) .</span><span class="sxs-lookup"><span data-stu-id="4b7b6-126">For adding a secret to the Key Vault, see \[Add a key or secret to the key vault\](https://docs.microsoft.com/azure/key-vault/key-vault-get-started/#add).</span></span>
<span data-ttu-id="4b7b6-127">In diesem Fall muss Ihr Zertifikat die Base64-Codierung des folgenden #A0 sein, das in UTF-8 codiert ist: \<br\> \<br\> { \<br\> "data":" \<Base64-encoded-certificate\> ", \<br\> "dataType":"pfx", \<br\> "password":" \<pfx-file-password\> " \<br\> }/</span><span class="sxs-lookup"><span data-stu-id="4b7b6-127">In this case, your certificate needs to be It is the Base64 encoding of the following JSON Object which is encoded in UTF-8: \<br\>\<br\> {\<br\>  "data":"\<Base64-encoded-certificate\>",\<br\>  "dataType":"pfx",\<br\>  "password":"\<pfx-file-password\>"\<br\>}/</span></span>

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

### <span data-ttu-id="4b7b6-128">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="4b7b6-128">-ClusterName</span></span>
<span data-ttu-id="4b7b6-129">Geben Sie den Namen des Clusters an.</span><span class="sxs-lookup"><span data-stu-id="4b7b6-129">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="4b7b6-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b7b6-130">-DefaultProfile</span></span>
<span data-ttu-id="4b7b6-131">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4b7b6-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4b7b6-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4b7b6-132">-InputObject</span></span>
<span data-ttu-id="4b7b6-133">Knotentypressource</span><span class="sxs-lookup"><span data-stu-id="4b7b6-133">Node Type resource</span></span>

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

### <span data-ttu-id="4b7b6-134">-Name</span><span class="sxs-lookup"><span data-stu-id="4b7b6-134">-Name</span></span>
<span data-ttu-id="4b7b6-135">Geben Sie den Namen des Knotentyps an.</span><span class="sxs-lookup"><span data-stu-id="4b7b6-135">Specify the name of the node type.</span></span>

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

### <span data-ttu-id="4b7b6-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4b7b6-136">-ResourceGroupName</span></span>
<span data-ttu-id="4b7b6-137">Geben Sie den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="4b7b6-137">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="4b7b6-138">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="4b7b6-138">-SourceVaultId</span></span>
<span data-ttu-id="4b7b6-139">Schlüssel-Tresor-Ressourcen-ID, die die Zertifikate enthält.</span><span class="sxs-lookup"><span data-stu-id="4b7b6-139">Key Vault resource id containing the certificates.</span></span>

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

### <span data-ttu-id="4b7b6-140">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="4b7b6-140">-Confirm</span></span>
<span data-ttu-id="4b7b6-141">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4b7b6-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4b7b6-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4b7b6-142">-WhatIf</span></span>
<span data-ttu-id="4b7b6-143">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4b7b6-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4b7b6-144">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4b7b6-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4b7b6-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b7b6-145">CommonParameters</span></span>
<span data-ttu-id="4b7b6-146">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4b7b6-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b7b6-147">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4b7b6-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b7b6-148">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="4b7b6-148">INPUTS</span></span>

### <span data-ttu-id="4b7b6-149">System.String</span><span class="sxs-lookup"><span data-stu-id="4b7b6-149">System.String</span></span>

## <span data-ttu-id="4b7b6-150">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="4b7b6-150">OUTPUTS</span></span>

### <span data-ttu-id="4b7b6-151">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="4b7b6-151">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType</span></span>

## <span data-ttu-id="4b7b6-152">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="4b7b6-152">NOTES</span></span>

## <span data-ttu-id="4b7b6-153">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="4b7b6-153">RELATED LINKS</span></span>
