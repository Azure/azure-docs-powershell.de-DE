---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/add-azservicefabricclustercertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricClusterCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricClusterCertificate.md
ms.openlocfilehash: c3ddf8373b467b3f7821d9470f67f2b864201949
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100145809"
---
# <span data-ttu-id="5c0c4-101">Add-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="5c0c4-101">Add-AzServiceFabricClusterCertificate</span></span>

## <span data-ttu-id="5c0c4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5c0c4-102">SYNOPSIS</span></span>
<span data-ttu-id="5c0c4-103">Fügen Sie dem Cluster ein Zertifikat für einen sekundären Cluster hinzu.</span><span class="sxs-lookup"><span data-stu-id="5c0c4-103">Add a secondary cluster certificate to the cluster.</span></span>

## <span data-ttu-id="5c0c4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5c0c4-104">SYNTAX</span></span>

### <span data-ttu-id="5c0c4-105">ByExistingKeyVault</span><span class="sxs-lookup"><span data-stu-id="5c0c4-105">ByExistingKeyVault</span></span>
```
Add-AzServiceFabricClusterCertificate [-ResourceGroupName] <String> [-Name] <String> -SecretIdentifier <String>
 [-Thumbprint <String>] [-CertificateCommonName <String>] [-CertificateIssuerThumbprint <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5c0c4-106">ByNewPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="5c0c4-106">ByNewPfxAndVaultName</span></span>
```
Add-AzServiceFabricClusterCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-KeyVaultResourceGroupName <String>] [-KeyVaultName <String>] [-CertificateOutputFolder <String>]
 [-CertificatePassword <SecureString>] -CertificateSubjectName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5c0c4-107">ByExistingPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="5c0c4-107">ByExistingPfxAndVaultName</span></span>
```
Add-AzServiceFabricClusterCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-KeyVaultResourceGroupName <String>] [-KeyVaultName <String>] -CertificateFile <String>
 [-CertificatePassword <SecureString>] [-CertificateCommonName <String>]
 [-CertificateIssuerThumbprint <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5c0c4-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5c0c4-108">DESCRIPTION</span></span>
<span data-ttu-id="5c0c4-109">Verwenden Sie **Add-AzServiceFabricClusterCertificate,** um ein sekundäres Clusterzertifikat hinzuzufügen, entweder aus einem vorhandenen Azure-Schlüsseltresor oder durch Erstellen eines neuen Azure-Schlüsseltresors mithilfe eines vorhandenen Zertifikats, das bereitgestellt wird, oder eines neuen selbst signierten Zertifikats.</span><span class="sxs-lookup"><span data-stu-id="5c0c4-109">Use **Add-AzServiceFabricClusterCertificate** to add a secondary cluster certificate, either from an existing Azure key vault or creating a new Azure key vault using an existing certificate provided or from a new self-signed certificate created.</span></span> <span data-ttu-id="5c0c4-110">Der sekundäre Cluster wird außer Kraft setzen, falls vorhanden.</span><span class="sxs-lookup"><span data-stu-id="5c0c4-110">It will override the secondary cluster if there is any.</span></span>

## <span data-ttu-id="5c0c4-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="5c0c4-111">EXAMPLES</span></span>

### <span data-ttu-id="5c0c4-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="5c0c4-112">Example 1</span></span>
```powershell
Add-AzServiceFabricClusterCertificate -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' 
-SecretIdentifier 'https://contoso03vault.vault.azure.net/secrets/contoso03vaultrg/7f7de9131c034172b9df37ccc549524f'
```

<span data-ttu-id="5c0c4-113">Mit diesem Befehl wird ein Zertifikat im vorhandenen Azure -Schlüsseltresor als sekundäres Clusterzertifikat hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="5c0c4-113">This command will add a certificate in the existing Azure key vault as a secondary cluster certificate.</span></span>

### <span data-ttu-id="5c0c4-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="5c0c4-114">Example 2</span></span>
```
PS c:\> $pwd = ConvertTo-SecureString -String "123" -AsPlainText -Force
PS c:\> add-AzServiceFabricClusterCertificate -ResourceGroupName 'Group2' -Name 'Contoso02SFCluster'  -CertificateSubjectName 'Contoso.com' 
-CertificateOutputFolder 'c:\test' -CertificatePassword $pwd
```

<span data-ttu-id="5c0c4-115">Mit diesem Befehl wird ein selbst signiertes Zertifikat im Azure -Schlüsseltresor erstellt und der Cluster aktualisiert, um es als sekundäres Clusterzertifikat zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="5c0c4-115">This command will create a self-signed certificate in the Azure key vault and upgrade the cluster to use it as a secondary cluster certificate.</span></span>

## <span data-ttu-id="5c0c4-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5c0c4-116">PARAMETERS</span></span>

### <span data-ttu-id="5c0c4-117">-CertificateCommonName</span><span class="sxs-lookup"><span data-stu-id="5c0c4-117">-CertificateCommonName</span></span>
<span data-ttu-id="5c0c4-118">Häufig verwendeter Zertifikatname</span><span class="sxs-lookup"><span data-stu-id="5c0c4-118">Certificate common name</span></span>

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

### <span data-ttu-id="5c0c4-119">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="5c0c4-119">-CertificateFile</span></span>
<span data-ttu-id="5c0c4-120">Der Pfad zum vorhandenen Zertifikat</span><span class="sxs-lookup"><span data-stu-id="5c0c4-120">The path to the existing certificate</span></span>

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

### <span data-ttu-id="5c0c4-121">-CertificateIssuerThumbprint</span><span class="sxs-lookup"><span data-stu-id="5c0c4-121">-CertificateIssuerThumbprint</span></span>
<span data-ttu-id="5c0c4-122">Aussteller des Zertifikats mit Fingerabdruck, durch Kommas getrennt, wenn mehrere</span><span class="sxs-lookup"><span data-stu-id="5c0c4-122">Certificate issuer thumbprint, separated by commas if more than one</span></span>

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

### <span data-ttu-id="5c0c4-123">-CertificateOutputFolder</span><span class="sxs-lookup"><span data-stu-id="5c0c4-123">-CertificateOutputFolder</span></span>
<span data-ttu-id="5c0c4-124">Der Ordner, in den das neue Zertifikat heruntergeladen werden muss.</span><span class="sxs-lookup"><span data-stu-id="5c0c4-124">The folder where the new certificate needs to be downloaded.</span></span>

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

### <span data-ttu-id="5c0c4-125">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="5c0c4-125">-CertificatePassword</span></span>
<span data-ttu-id="5c0c4-126">Das Kennwort des Zertifikats</span><span class="sxs-lookup"><span data-stu-id="5c0c4-126">The password of the certificate</span></span>

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

### <span data-ttu-id="5c0c4-127">-CertificateSubjectName</span><span class="sxs-lookup"><span data-stu-id="5c0c4-127">-CertificateSubjectName</span></span>
<span data-ttu-id="5c0c4-128">Der Betreffname des Zertifikats</span><span class="sxs-lookup"><span data-stu-id="5c0c4-128">The subject name of the certificate</span></span>

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

### <span data-ttu-id="5c0c4-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c0c4-129">-DefaultProfile</span></span>
<span data-ttu-id="5c0c4-130">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5c0c4-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5c0c4-131">-KeyVaultName</span><span class="sxs-lookup"><span data-stu-id="5c0c4-131">-KeyVaultName</span></span>
<span data-ttu-id="5c0c4-132">Azure Key Vault name, if not given it will be default to the resource group name</span><span class="sxs-lookup"><span data-stu-id="5c0c4-132">Azure key vault name, if not given it will be defaulted to the resource group name</span></span>

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

### <span data-ttu-id="5c0c4-133">-KeyVaultResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5c0c4-133">-KeyVaultResourceGroupName</span></span>
<span data-ttu-id="5c0c4-134">Der Name der Azure-Schlüsseltresor-Ressourcengruppe, wenn dieser nicht angegeben wird, wird standardmäßig auf "Ressourcengruppenname" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="5c0c4-134">Azure key vault resource group name, if not given it will be defaulted to resource group name</span></span>

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

### <span data-ttu-id="5c0c4-135">-Name</span><span class="sxs-lookup"><span data-stu-id="5c0c4-135">-Name</span></span>
<span data-ttu-id="5c0c4-136">Angeben des Namens des Clusters</span><span class="sxs-lookup"><span data-stu-id="5c0c4-136">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="5c0c4-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5c0c4-137">-ResourceGroupName</span></span>
<span data-ttu-id="5c0c4-138">Geben Sie den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="5c0c4-138">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="5c0c4-139">-SecretIdentifier</span><span class="sxs-lookup"><span data-stu-id="5c0c4-139">-SecretIdentifier</span></span>
<span data-ttu-id="5c0c4-140">Die vorhandene geheime Azure Key Vault-URL, z. B. https://mykv.vault.azure.net:443/secrets/mysecrets/55ec7c4dc61a462bbc645ffc9b4b225f ' '</span><span class="sxs-lookup"><span data-stu-id="5c0c4-140">The existing Azure key vault secret URL, for example 'https://mykv.vault.azure.net:443/secrets/mysecrets/55ec7c4dc61a462bbc645ffc9b4b225f'</span></span>

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

### <span data-ttu-id="5c0c4-141">-Thumbprint</span><span class="sxs-lookup"><span data-stu-id="5c0c4-141">-Thumbprint</span></span>
<span data-ttu-id="5c0c4-142">Der Fingerabdruck für das Zertifikat, das dem SecretIdentifier-Konto korreliert.</span><span class="sxs-lookup"><span data-stu-id="5c0c4-142">The thumbprint for the certificate correspoinding to the SecretIdentifier.</span></span> <span data-ttu-id="5c0c4-143">Verwenden Sie diese Informationen, wenn das Zertifikat nicht verwaltet wird, da der Schlüsseltresor nur das Zertifikat als geheimes Zertifikat speichern würde und das Cmdlet den Fingerdruck nicht erneut abspeichern kann.</span><span class="sxs-lookup"><span data-stu-id="5c0c4-143">Use this if the certificate is not managed as the key vault would only have the certificate stored as a secret and the cmdlet is unable to retreive the thumbprint.</span></span>

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

### <span data-ttu-id="5c0c4-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5c0c4-144">-Confirm</span></span>
<span data-ttu-id="5c0c4-145">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5c0c4-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5c0c4-146">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="5c0c4-146">-WhatIf</span></span>
<span data-ttu-id="5c0c4-147">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5c0c4-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5c0c4-148">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5c0c4-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5c0c4-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c0c4-149">CommonParameters</span></span>
<span data-ttu-id="5c0c4-150">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5c0c4-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c0c4-151">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5c0c4-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c0c4-152">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="5c0c4-152">INPUTS</span></span>

### <span data-ttu-id="5c0c4-153">System.String</span><span class="sxs-lookup"><span data-stu-id="5c0c4-153">System.String</span></span>

### <span data-ttu-id="5c0c4-154">System.Security.SecureString</span><span class="sxs-lookup"><span data-stu-id="5c0c4-154">System.Security.SecureString</span></span>

## <span data-ttu-id="5c0c4-155">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="5c0c4-155">OUTPUTS</span></span>

### <span data-ttu-id="5c0c4-156">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span><span class="sxs-lookup"><span data-stu-id="5c0c4-156">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="5c0c4-157">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="5c0c4-157">NOTES</span></span>

## <span data-ttu-id="5c0c4-158">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="5c0c4-158">RELATED LINKS</span></span>

[<span data-ttu-id="5c0c4-159">Remove-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="5c0c4-159">Remove-AzServiceFabricClusterCertificate</span></span>](./Remove-AzServiceFabricClusterCertificate.md)

[<span data-ttu-id="5c0c4-160">New-AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="5c0c4-160">New-AzServiceFabricCluster</span></span>](./New-AzServiceFabricCluster.md)
