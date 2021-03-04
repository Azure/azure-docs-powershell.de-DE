---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/add-azservicefabricclustercertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricClusterCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricClusterCertificate.md
ms.openlocfilehash: 379bd710413fee83a2fdb6b10dc7fb42f0f207bf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101927552"
---
# <span data-ttu-id="12daa-101">Add-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="12daa-101">Add-AzServiceFabricClusterCertificate</span></span>

## <span data-ttu-id="12daa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="12daa-102">SYNOPSIS</span></span>
<span data-ttu-id="12daa-103">Fügen Sie dem Cluster ein sekundäres Clusterzertifikat hinzu.</span><span class="sxs-lookup"><span data-stu-id="12daa-103">Add a secondary cluster certificate to the cluster.</span></span>

## <span data-ttu-id="12daa-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="12daa-104">SYNTAX</span></span>

### <span data-ttu-id="12daa-105">ByExistingKeyVault</span><span class="sxs-lookup"><span data-stu-id="12daa-105">ByExistingKeyVault</span></span>
```
Add-AzServiceFabricClusterCertificate [-ResourceGroupName] <String> [-Name] <String> -SecretIdentifier <String>
 [-Thumbprint <String>] [-CertificateCommonName <String>] [-CertificateIssuerThumbprint <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="12daa-106">ByNewPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="12daa-106">ByNewPfxAndVaultName</span></span>
```
Add-AzServiceFabricClusterCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-KeyVaultResourceGroupName <String>] [-KeyVaultName <String>] [-CertificateOutputFolder <String>]
 [-CertificatePassword <SecureString>] -CertificateSubjectName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="12daa-107">ByExistingPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="12daa-107">ByExistingPfxAndVaultName</span></span>
```
Add-AzServiceFabricClusterCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-KeyVaultResourceGroupName <String>] [-KeyVaultName <String>] -CertificateFile <String>
 [-CertificatePassword <SecureString>] [-CertificateCommonName <String>]
 [-CertificateIssuerThumbprint <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="12daa-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="12daa-108">DESCRIPTION</span></span>
<span data-ttu-id="12daa-109">Verwenden **Sie Add-AzServiceFabricClusterCertificate,** um ein sekundäres Clusterzertifikat hinzuzufügen, entweder aus einem vorhandenen Azure-Schlüsseltresor oder zum Erstellen eines neuen Azure-Schlüsseltresors mithilfe eines vorhandenen Zertifikats oder eines neuen selbst signierten Zertifikats, das erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="12daa-109">Use **Add-AzServiceFabricClusterCertificate** to add a secondary cluster certificate, either from an existing Azure key vault or creating a new Azure key vault using an existing certificate provided or from a new self-signed certificate created.</span></span> <span data-ttu-id="12daa-110">Wenn vorhanden ist, überschreibt es den sekundären Cluster.</span><span class="sxs-lookup"><span data-stu-id="12daa-110">It will override the secondary cluster if there is any.</span></span>

## <span data-ttu-id="12daa-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="12daa-111">EXAMPLES</span></span>

### <span data-ttu-id="12daa-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="12daa-112">Example 1</span></span>
```powershell
Add-AzServiceFabricClusterCertificate -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' 
-SecretIdentifier 'https://contoso03vault.vault.azure.net/secrets/contoso03vaultrg/7f7de9131c034172b9df37ccc549524f'
```

<span data-ttu-id="12daa-113">Mit diesem Befehl wird ein Zertifikat im vorhandenen Azure-Schlüsseltresor als sekundäres Clusterzertifikat hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="12daa-113">This command will add a certificate in the existing Azure key vault as a secondary cluster certificate.</span></span>

### <span data-ttu-id="12daa-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="12daa-114">Example 2</span></span>
```
PS c:\> $pwd = ConvertTo-SecureString -String "123" -AsPlainText -Force
PS c:\> add-AzServiceFabricClusterCertificate -ResourceGroupName 'Group2' -Name 'Contoso02SFCluster'  -CertificateSubjectName 'Contoso.com' 
-CertificateOutputFolder 'c:\test' -CertificatePassword $pwd
```

<span data-ttu-id="12daa-115">Mit diesem Befehl wird ein selbst signiertes Zertifikat im Azure-Schlüsseltresor erstellt und der Cluster aktualisiert, um es als sekundäres Clusterzertifikat zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="12daa-115">This command will create a self-signed certificate in the Azure key vault and upgrade the cluster to use it as a secondary cluster certificate.</span></span>

## <span data-ttu-id="12daa-116">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="12daa-116">PARAMETERS</span></span>

### <span data-ttu-id="12daa-117">-CertificateCommonName</span><span class="sxs-lookup"><span data-stu-id="12daa-117">-CertificateCommonName</span></span>
<span data-ttu-id="12daa-118">Häufiger Name des Zertifikats</span><span class="sxs-lookup"><span data-stu-id="12daa-118">Certificate common name</span></span>

```yaml
Type: System.String
Parameter Sets: ByExistingKeyVault, ByExistingPfxAndVaultName
Aliases: CertCommonName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12daa-119">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="12daa-119">-CertificateFile</span></span>
<span data-ttu-id="12daa-120">Der Pfad zum vorhandenen Zertifikat</span><span class="sxs-lookup"><span data-stu-id="12daa-120">The path to the existing certificate</span></span>

```yaml
Type: System.String
Parameter Sets: ByExistingPfxAndVaultName
Aliases: Source

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="12daa-121">-CertificateIssuerThumbprint</span><span class="sxs-lookup"><span data-stu-id="12daa-121">-CertificateIssuerThumbprint</span></span>
<span data-ttu-id="12daa-122">Fingerabdruck des Zertifikatausstellers, getrennt durch Kommas, wenn mehr als eins</span><span class="sxs-lookup"><span data-stu-id="12daa-122">Certificate issuer thumbprint, separated by commas if more than one</span></span>

```yaml
Type: System.String
Parameter Sets: ByExistingKeyVault, ByExistingPfxAndVaultName
Aliases: CertIssuerThumbprint

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12daa-123">-CertificateOutputFolder</span><span class="sxs-lookup"><span data-stu-id="12daa-123">-CertificateOutputFolder</span></span>
<span data-ttu-id="12daa-124">Der Ordner, in dem das neue Zertifikat heruntergeladen werden muss.</span><span class="sxs-lookup"><span data-stu-id="12daa-124">The folder where the new certificate needs to be downloaded.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNewPfxAndVaultName
Aliases: Destination

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="12daa-125">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="12daa-125">-CertificatePassword</span></span>
<span data-ttu-id="12daa-126">Das Kennwort des Zertifikats</span><span class="sxs-lookup"><span data-stu-id="12daa-126">The password of the certificate</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: ByNewPfxAndVaultName, ByExistingPfxAndVaultName
Aliases: CertPassword

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="12daa-127">-CertificateSubjectName</span><span class="sxs-lookup"><span data-stu-id="12daa-127">-CertificateSubjectName</span></span>
<span data-ttu-id="12daa-128">Der Betreffname des Zertifikats</span><span class="sxs-lookup"><span data-stu-id="12daa-128">The subject name of the certificate</span></span>

```yaml
Type: System.String
Parameter Sets: ByNewPfxAndVaultName
Aliases: Subject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="12daa-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12daa-129">-DefaultProfile</span></span>
<span data-ttu-id="12daa-130">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="12daa-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="12daa-131">-KeyVaultName</span><span class="sxs-lookup"><span data-stu-id="12daa-131">-KeyVaultName</span></span>
<span data-ttu-id="12daa-132">Azure Key Vault name, if not given it will be default to the resource group name</span><span class="sxs-lookup"><span data-stu-id="12daa-132">Azure key vault name, if not given it will be defaulted to the resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: ByNewPfxAndVaultName, ByExistingPfxAndVaultName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="12daa-133">-KeyVaultResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12daa-133">-KeyVaultResourceGroupName</span></span>
<span data-ttu-id="12daa-134">Der Name der Azure Key Vault-Ressourcengruppe, sofern nicht angegeben, wird standardmäßig als Ressourcengruppenname verwendet.</span><span class="sxs-lookup"><span data-stu-id="12daa-134">Azure key vault resource group name, if not given it will be defaulted to resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: ByNewPfxAndVaultName, ByExistingPfxAndVaultName
Aliases: KeyVaultResouceGroupName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="12daa-135">-Name</span><span class="sxs-lookup"><span data-stu-id="12daa-135">-Name</span></span>
<span data-ttu-id="12daa-136">Angeben des Namens des Clusters</span><span class="sxs-lookup"><span data-stu-id="12daa-136">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="12daa-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12daa-137">-ResourceGroupName</span></span>
<span data-ttu-id="12daa-138">Geben Sie den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="12daa-138">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="12daa-139">-SecretIdentifier</span><span class="sxs-lookup"><span data-stu-id="12daa-139">-SecretIdentifier</span></span>
<span data-ttu-id="12daa-140">Die vorhandene geheime Azure-Schlüsseltresor-URL, z. B. https://mykv.vault.azure.net:443/secrets/mysecrets/55ec7c4dc61a462bbc645ffc9b4b225f ' '</span><span class="sxs-lookup"><span data-stu-id="12daa-140">The existing Azure key vault secret URL, for example 'https://mykv.vault.azure.net:443/secrets/mysecrets/55ec7c4dc61a462bbc645ffc9b4b225f'</span></span>

```yaml
Type: System.String
Parameter Sets: ByExistingKeyVault
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="12daa-141">-Thumbprint</span><span class="sxs-lookup"><span data-stu-id="12daa-141">-Thumbprint</span></span>
<span data-ttu-id="12daa-142">Der Fingerabdruck für das Zertifikat korreliert mit dem SecretIdentifier.</span><span class="sxs-lookup"><span data-stu-id="12daa-142">The thumbprint for the certificate correspoinding to the SecretIdentifier.</span></span> <span data-ttu-id="12daa-143">Verwenden Sie dies, wenn das Zertifikat nicht verwaltet wird, da das Zertifikat im Schlüsseltresor nur als Geheimspeicher gespeichert ist und das Cmdlet den Fingerabdruck nicht erneut abspeichern kann.</span><span class="sxs-lookup"><span data-stu-id="12daa-143">Use this if the certificate is not managed as the key vault would only have the certificate stored as a secret and the cmdlet is unable to retreive the thumbprint.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExistingKeyVault
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="12daa-144">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="12daa-144">-Confirm</span></span>
<span data-ttu-id="12daa-145">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="12daa-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="12daa-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="12daa-146">-WhatIf</span></span>
<span data-ttu-id="12daa-147">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="12daa-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="12daa-148">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="12daa-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="12daa-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12daa-149">CommonParameters</span></span>
<span data-ttu-id="12daa-150">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12daa-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12daa-151">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="12daa-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12daa-152">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="12daa-152">INPUTS</span></span>

### <span data-ttu-id="12daa-153">System.String</span><span class="sxs-lookup"><span data-stu-id="12daa-153">System.String</span></span>

### <span data-ttu-id="12daa-154">System.Security.SecureString</span><span class="sxs-lookup"><span data-stu-id="12daa-154">System.Security.SecureString</span></span>

## <span data-ttu-id="12daa-155">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="12daa-155">OUTPUTS</span></span>

### <span data-ttu-id="12daa-156">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span><span class="sxs-lookup"><span data-stu-id="12daa-156">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="12daa-157">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="12daa-157">NOTES</span></span>

## <span data-ttu-id="12daa-158">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="12daa-158">RELATED LINKS</span></span>

[<span data-ttu-id="12daa-159">Remove-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="12daa-159">Remove-AzServiceFabricClusterCertificate</span></span>](./Remove-AzServiceFabricClusterCertificate.md)

[<span data-ttu-id="12daa-160">New-AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="12daa-160">New-AzServiceFabricCluster</span></span>](./New-AzServiceFabricCluster.md)
