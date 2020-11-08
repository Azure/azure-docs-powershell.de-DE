---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/add-azservicefabricmanagednodetypevmsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricManagedNodeTypeVMSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricManagedNodeTypeVMSecret.md
ms.openlocfilehash: 36ed679066d1850851ff0e90f39eb6f9ef8ffa1a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94175888"
---
# <span data-ttu-id="42f07-101">Add-AzServiceFabricManagedNodeTypeVMSecret</span><span class="sxs-lookup"><span data-stu-id="42f07-101">Add-AzServiceFabricManagedNodeTypeVMSecret</span></span>

## <span data-ttu-id="42f07-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="42f07-102">SYNOPSIS</span></span>
<span data-ttu-id="42f07-103">Fügen Sie dem Knotentyp Zertifikatschlüssel hinzu.</span><span class="sxs-lookup"><span data-stu-id="42f07-103">Add certificate secret to the node type.</span></span>

## <span data-ttu-id="42f07-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="42f07-104">SYNTAX</span></span>

### <span data-ttu-id="42f07-105">ByObj (Standard)</span><span class="sxs-lookup"><span data-stu-id="42f07-105">ByObj (Default)</span></span>
```
Add-AzServiceFabricManagedNodeTypeVMSecret [-InputObject] <PSManagedNodeType> -SourceVaultId <String>
 -CertificateUrl <String> -CertificateStore <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="42f07-106">ByName</span><span class="sxs-lookup"><span data-stu-id="42f07-106">ByName</span></span>
```
Add-AzServiceFabricManagedNodeTypeVMSecret [-ResourceGroupName] <String> [-ClusterName] <String>
 [-Name] <String> -SourceVaultId <String> -CertificateUrl <String> -CertificateStore <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="42f07-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="42f07-107">DESCRIPTION</span></span>
<span data-ttu-id="42f07-108">Fügen Sie dem Knotentyp Zertifikatschlüssel hinzu.</span><span class="sxs-lookup"><span data-stu-id="42f07-108">Add certificate secret to the node type.</span></span> <span data-ttu-id="42f07-109">Der Schlüssel muss in einem Azure Key Vault gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="42f07-109">The secret must be stored in an Azure Key Vault.</span></span> <span data-ttu-id="42f07-110">Weitere Informationen zu Key Vault finden Sie unter Was ist Azure Key Vault?</span><span class="sxs-lookup"><span data-stu-id="42f07-110">For more information relating to Key Vault, see What is Azure Key Vault?</span></span> <span data-ttu-id="42f07-111">(https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/).</span><span class="sxs-lookup"><span data-stu-id="42f07-111">(https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/).</span></span> <span data-ttu-id="42f07-112">Weitere Informationen zu den Cmdlets finden Sie unter Azure Key Vault-Cmdlets ( https://msdn.microsoft.com/library/azure/dn868052.aspx) in der Microsoft Developer-Netzwerkbibliothek oder im Set-AzKeyVaultSecret-Cmdlets.</span><span class="sxs-lookup"><span data-stu-id="42f07-112">For more information about the cmdlets, see Azure Key Vault Cmdlets (https://msdn.microsoft.com/library/azure/dn868052.aspx) in the Microsoft Developer Network library or the Set-AzKeyVaultSecret cmdlet.</span></span>

## <span data-ttu-id="42f07-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="42f07-113">EXAMPLES</span></span>

### <span data-ttu-id="42f07-114">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="42f07-114">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
Add-AzServiceFabricManagedNodeTypeVMSecret -ResourceGroupName $rgName -ClusterName $clusterName -NodeTypeName $NodeTypeName -SourceVaultId /subscriptions/XXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/testRG/providers/Microsoft.KeyVault/vaults/testkv -CertificateUrl https://testskv.vault.azure.net:443/secrets/TestCert/xxxxxxxxxxxxxxxxxxxxxxxx -CertificateStore My -Verbose
```

<span data-ttu-id="42f07-115">Durch dieses Komma wird ein Zertifikatschlüssel aus dem angegebenen keyvault-und geheim Bezeichner hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="42f07-115">This commad adds a certificate secret from the keyvault and secret identifier specified.</span></span>

### <span data-ttu-id="42f07-116">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="42f07-116">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
$nodeType = Get-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -Name $NodeTypeName

$nodeType | Add-AzServiceFabricManagedNodeTypeVMSecret -SourceVaultId /subscriptions/XXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/testRG/providers/Microsoft.KeyVault/vaults/testkv -CertificateUrl https://testskv.vault.azure.net:443/secrets/TestCert/xxxxxxxxxxxxxxxxxxxxxxxx -CertificateStore My -Verbose
```

<span data-ttu-id="42f07-117">Durch dieses Komma wird ein Zertifikatschlüssel aus dem angegebenen keyvault-und Secret Identifier mit Piping hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="42f07-117">This commad adds a certificate secret from the keyvault and secret identifier specified, with piping.</span></span>

## <span data-ttu-id="42f07-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="42f07-118">PARAMETERS</span></span>

### <span data-ttu-id="42f07-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="42f07-119">-AsJob</span></span>
<span data-ttu-id="42f07-120">Führen Sie das Cmdlet im Hintergrund aus, und geben Sie einen Auftrag zum Nachverfolgen des Fortschritts zurück.</span><span class="sxs-lookup"><span data-stu-id="42f07-120">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="42f07-121">-CertificateStore</span><span class="sxs-lookup"><span data-stu-id="42f07-121">-CertificateStore</span></span>
<span data-ttu-id="42f07-122">Gibt den Zertifikatspeicher auf dem virtuellen Computer an, dem das Zertifikat hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="42f07-122">Specifies the certificate store on the Virtual Machine to which the certificate should be added.</span></span>
<span data-ttu-id="42f07-123">Der angegebene Zertifikatspeicher ist implizit im LocalMachine-Konto.</span><span class="sxs-lookup"><span data-stu-id="42f07-123">The specified certificate store is implicitly in the LocalMachine account.</span></span>

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

### <span data-ttu-id="42f07-124">-CertificateUrl</span><span class="sxs-lookup"><span data-stu-id="42f07-124">-CertificateUrl</span></span>
<span data-ttu-id="42f07-125">Dies ist die URL eines Zertifikats, das als Secret in Key Vault hochgeladen wurde.</span><span class="sxs-lookup"><span data-stu-id="42f07-125">This is the URL of a certificate that has been uploaded to Key Vault as a secret.</span></span>
<span data-ttu-id="42f07-126">Informationen zum Hinzufügen eines Geheimnisses zum schlüsseltresor finden Sie unter \[ Hinzufügen eines Schlüssels oder einer geheim Taste zum schlüsseltresor \] ( https://docs.microsoft.com/azure/key-vault/key-vault-get-started/#add) .</span><span class="sxs-lookup"><span data-stu-id="42f07-126">For adding a secret to the Key Vault, see \[Add a key or secret to the key vault\](https://docs.microsoft.com/azure/key-vault/key-vault-get-started/#add).</span></span>
<span data-ttu-id="42f07-127">In diesem Fall muss es sich bei Ihrem Zertifikat um die Base64-Codierung des folgenden JSON-Objekts handeln, das in UTF-8 codiert ist: \<br\> \<br\> { \<br\> "Data": " \<Base64-encoded-certificate\> ", \<br\> "Datentyp": "PFX", \<br\> "Kennwort": " \<pfx-file-password\> " \<br\> }/</span><span class="sxs-lookup"><span data-stu-id="42f07-127">In this case, your certificate needs to be It is the Base64 encoding of the following JSON Object which is encoded in UTF-8: \<br\>\<br\> {\<br\>  "data":"\<Base64-encoded-certificate\>",\<br\>  "dataType":"pfx",\<br\>  "password":"\<pfx-file-password\>"\<br\>}/</span></span>

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

### <span data-ttu-id="42f07-128">-Clustername</span><span class="sxs-lookup"><span data-stu-id="42f07-128">-ClusterName</span></span>
<span data-ttu-id="42f07-129">Geben Sie den Namen des Clusters an.</span><span class="sxs-lookup"><span data-stu-id="42f07-129">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="42f07-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42f07-130">-DefaultProfile</span></span>
<span data-ttu-id="42f07-131">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="42f07-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="42f07-132">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="42f07-132">-InputObject</span></span>
<span data-ttu-id="42f07-133">Knotentyp Ressource</span><span class="sxs-lookup"><span data-stu-id="42f07-133">Node Type resource</span></span>

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

### <span data-ttu-id="42f07-134">-Name</span><span class="sxs-lookup"><span data-stu-id="42f07-134">-Name</span></span>
<span data-ttu-id="42f07-135">Geben Sie den Namen des Knotentyps an.</span><span class="sxs-lookup"><span data-stu-id="42f07-135">Specify the name of the node type.</span></span>

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

### <span data-ttu-id="42f07-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42f07-136">-ResourceGroupName</span></span>
<span data-ttu-id="42f07-137">Geben Sie den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="42f07-137">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="42f07-138">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="42f07-138">-SourceVaultId</span></span>
<span data-ttu-id="42f07-139">Die schlüsseltresor-Ressourcen-ID mit den Zertifikaten.</span><span class="sxs-lookup"><span data-stu-id="42f07-139">Key Vault resource id containing the certificates.</span></span>

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

### <span data-ttu-id="42f07-140">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="42f07-140">-Confirm</span></span>
<span data-ttu-id="42f07-141">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="42f07-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="42f07-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="42f07-142">-WhatIf</span></span>
<span data-ttu-id="42f07-143">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="42f07-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="42f07-144">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="42f07-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="42f07-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42f07-145">CommonParameters</span></span>
<span data-ttu-id="42f07-146">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="42f07-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42f07-147">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="42f07-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42f07-148">Eingaben</span><span class="sxs-lookup"><span data-stu-id="42f07-148">INPUTS</span></span>

### <span data-ttu-id="42f07-149">System. String</span><span class="sxs-lookup"><span data-stu-id="42f07-149">System.String</span></span>

## <span data-ttu-id="42f07-150">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="42f07-150">OUTPUTS</span></span>

### <span data-ttu-id="42f07-151">Microsoft. Azure. Commands. ServiceFabric. Models. PSManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="42f07-151">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType</span></span>

## <span data-ttu-id="42f07-152">Notizen</span><span class="sxs-lookup"><span data-stu-id="42f07-152">NOTES</span></span>

## <span data-ttu-id="42f07-153">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="42f07-153">RELATED LINKS</span></span>
