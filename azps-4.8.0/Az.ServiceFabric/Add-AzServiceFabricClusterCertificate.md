---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/add-azservicefabricclustercertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricClusterCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricClusterCertificate.md
ms.openlocfilehash: c3ddf8373b467b3f7821d9470f67f2b864201949
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94007796"
---
# <span data-ttu-id="854a8-101">Add-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="854a8-101">Add-AzServiceFabricClusterCertificate</span></span>

## <span data-ttu-id="854a8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="854a8-102">SYNOPSIS</span></span>
<span data-ttu-id="854a8-103">Hinzufügen eines sekundären Cluster Zertifikats zum Cluster</span><span class="sxs-lookup"><span data-stu-id="854a8-103">Add a secondary cluster certificate to the cluster.</span></span>

## <span data-ttu-id="854a8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="854a8-104">SYNTAX</span></span>

### <span data-ttu-id="854a8-105">ByExistingKeyVault</span><span class="sxs-lookup"><span data-stu-id="854a8-105">ByExistingKeyVault</span></span>
```
Add-AzServiceFabricClusterCertificate [-ResourceGroupName] <String> [-Name] <String> -SecretIdentifier <String>
 [-Thumbprint <String>] [-CertificateCommonName <String>] [-CertificateIssuerThumbprint <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="854a8-106">ByNewPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="854a8-106">ByNewPfxAndVaultName</span></span>
```
Add-AzServiceFabricClusterCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-KeyVaultResourceGroupName <String>] [-KeyVaultName <String>] [-CertificateOutputFolder <String>]
 [-CertificatePassword <SecureString>] -CertificateSubjectName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="854a8-107">ByExistingPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="854a8-107">ByExistingPfxAndVaultName</span></span>
```
Add-AzServiceFabricClusterCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-KeyVaultResourceGroupName <String>] [-KeyVaultName <String>] -CertificateFile <String>
 [-CertificatePassword <SecureString>] [-CertificateCommonName <String>]
 [-CertificateIssuerThumbprint <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="854a8-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="854a8-108">DESCRIPTION</span></span>
<span data-ttu-id="854a8-109">Verwenden **Sie Add-AzServiceFabricClusterCertificate** zum Hinzufügen eines sekundären Cluster Zertifikats, entweder aus einem vorhandenen Azure Key Vault oder durch Erstellen eines neuen Azure Key Vault mithilfe eines vorhandenen Zertifikats oder aus einem neuen selbstsignierten Zertifikat, das erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="854a8-109">Use **Add-AzServiceFabricClusterCertificate** to add a secondary cluster certificate, either from an existing Azure key vault or creating a new Azure key vault using an existing certificate provided or from a new self-signed certificate created.</span></span> <span data-ttu-id="854a8-110">Wenn vorhanden, wird der sekundäre Cluster überschrieben.</span><span class="sxs-lookup"><span data-stu-id="854a8-110">It will override the secondary cluster if there is any.</span></span>

## <span data-ttu-id="854a8-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="854a8-111">EXAMPLES</span></span>

### <span data-ttu-id="854a8-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="854a8-112">Example 1</span></span>
```powershell
Add-AzServiceFabricClusterCertificate -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' 
-SecretIdentifier 'https://contoso03vault.vault.azure.net/secrets/contoso03vaultrg/7f7de9131c034172b9df37ccc549524f'
```

<span data-ttu-id="854a8-113">Mit diesem Befehl wird ein Zertifikat im vorhandenen Azure Key Vault als sekundäres Cluster Zertifikat hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="854a8-113">This command will add a certificate in the existing Azure key vault as a secondary cluster certificate.</span></span>

### <span data-ttu-id="854a8-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="854a8-114">Example 2</span></span>
```
PS c:\> $pwd = ConvertTo-SecureString -String "123" -AsPlainText -Force
PS c:\> add-AzServiceFabricClusterCertificate -ResourceGroupName 'Group2' -Name 'Contoso02SFCluster'  -CertificateSubjectName 'Contoso.com' 
-CertificateOutputFolder 'c:\test' -CertificatePassword $pwd
```

<span data-ttu-id="854a8-115">Mit diesem Befehl wird im Azure Key Vault ein selbstsigniertes Zertifikat erstellt und der Cluster so aktualisiert, dass es als sekundäres Cluster Zertifikat verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="854a8-115">This command will create a self-signed certificate in the Azure key vault and upgrade the cluster to use it as a secondary cluster certificate.</span></span>

## <span data-ttu-id="854a8-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="854a8-116">PARAMETERS</span></span>

### <span data-ttu-id="854a8-117">-CertificateCommonName</span><span class="sxs-lookup"><span data-stu-id="854a8-117">-CertificateCommonName</span></span>
<span data-ttu-id="854a8-118">Allgemeiner Zertifikatname</span><span class="sxs-lookup"><span data-stu-id="854a8-118">Certificate common name</span></span>

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

### <span data-ttu-id="854a8-119">-Certificatedatei</span><span class="sxs-lookup"><span data-stu-id="854a8-119">-CertificateFile</span></span>
<span data-ttu-id="854a8-120">Der Pfad zum vorhandenen Zertifikat</span><span class="sxs-lookup"><span data-stu-id="854a8-120">The path to the existing certificate</span></span>

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

### <span data-ttu-id="854a8-121">-CertificateIssuerThumbprint</span><span class="sxs-lookup"><span data-stu-id="854a8-121">-CertificateIssuerThumbprint</span></span>
<span data-ttu-id="854a8-122">Fingerabdruck des Zertifikatausstellers, getrennt durch Kommas, wenn mehr als eine</span><span class="sxs-lookup"><span data-stu-id="854a8-122">Certificate issuer thumbprint, separated by commas if more than one</span></span>

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

### <span data-ttu-id="854a8-123">-CertificateOutputFolder</span><span class="sxs-lookup"><span data-stu-id="854a8-123">-CertificateOutputFolder</span></span>
<span data-ttu-id="854a8-124">Der Ordner, in dem das neue Zertifikat heruntergeladen werden muss.</span><span class="sxs-lookup"><span data-stu-id="854a8-124">The folder where the new certificate needs to be downloaded.</span></span>

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

### <span data-ttu-id="854a8-125">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="854a8-125">-CertificatePassword</span></span>
<span data-ttu-id="854a8-126">Das Kennwort des Zertifikats</span><span class="sxs-lookup"><span data-stu-id="854a8-126">The password of the certificate</span></span>

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

### <span data-ttu-id="854a8-127">-CertificateSubjectName</span><span class="sxs-lookup"><span data-stu-id="854a8-127">-CertificateSubjectName</span></span>
<span data-ttu-id="854a8-128">Der Name des Antragstellers des Zertifikats</span><span class="sxs-lookup"><span data-stu-id="854a8-128">The subject name of the certificate</span></span>

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

### <span data-ttu-id="854a8-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="854a8-129">-DefaultProfile</span></span>
<span data-ttu-id="854a8-130">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="854a8-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="854a8-131">-Keyvaultname</span><span class="sxs-lookup"><span data-stu-id="854a8-131">-KeyVaultName</span></span>
<span data-ttu-id="854a8-132">Azure Key Vault-Name, wenn nicht angegeben, wird der Name der Ressourcengruppe standardmäßig verwendet.</span><span class="sxs-lookup"><span data-stu-id="854a8-132">Azure key vault name, if not given it will be defaulted to the resource group name</span></span>

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

### <span data-ttu-id="854a8-133">-KeyVaultResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="854a8-133">-KeyVaultResourceGroupName</span></span>
<span data-ttu-id="854a8-134">Azure Key Vault-Ressourcengruppenname, wenn nicht angegeben, wird der Name der Ressourcengruppe standardmäßig verwendet.</span><span class="sxs-lookup"><span data-stu-id="854a8-134">Azure key vault resource group name, if not given it will be defaulted to resource group name</span></span>

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

### <span data-ttu-id="854a8-135">-Name</span><span class="sxs-lookup"><span data-stu-id="854a8-135">-Name</span></span>
<span data-ttu-id="854a8-136">Angeben des Namens des Clusters</span><span class="sxs-lookup"><span data-stu-id="854a8-136">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="854a8-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="854a8-137">-ResourceGroupName</span></span>
<span data-ttu-id="854a8-138">Geben Sie den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="854a8-138">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="854a8-139">-SecretIdentifier</span><span class="sxs-lookup"><span data-stu-id="854a8-139">-SecretIdentifier</span></span>
<span data-ttu-id="854a8-140">Die vorhandene Azure Key Vault Secret-URL, beispielsweise ' https://mykv.vault.azure.net:443/secrets/mysecrets/55ec7c4dc61a462bbc645ffc9b4b225f '</span><span class="sxs-lookup"><span data-stu-id="854a8-140">The existing Azure key vault secret URL, for example 'https://mykv.vault.azure.net:443/secrets/mysecrets/55ec7c4dc61a462bbc645ffc9b4b225f'</span></span>

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

### <span data-ttu-id="854a8-141">-Fingerabdruck</span><span class="sxs-lookup"><span data-stu-id="854a8-141">-Thumbprint</span></span>
<span data-ttu-id="854a8-142">Der Fingerabdruck für das Zertifikat correspoinding dem SecretIdentifier.</span><span class="sxs-lookup"><span data-stu-id="854a8-142">The thumbprint for the certificate correspoinding to the SecretIdentifier.</span></span> <span data-ttu-id="854a8-143">Verwenden Sie diese Vorgehensweise, wenn das Zertifikat nicht verwaltet wird, da der schlüsseltresor nur das Zertifikat als geheim speichern und das Cmdlet den Fingerabdruck nicht abrufen kann.</span><span class="sxs-lookup"><span data-stu-id="854a8-143">Use this if the certificate is not managed as the key vault would only have the certificate stored as a secret and the cmdlet is unable to retreive the thumbprint.</span></span>

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

### <span data-ttu-id="854a8-144">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="854a8-144">-Confirm</span></span>
<span data-ttu-id="854a8-145">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="854a8-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="854a8-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="854a8-146">-WhatIf</span></span>
<span data-ttu-id="854a8-147">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="854a8-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="854a8-148">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="854a8-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="854a8-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="854a8-149">CommonParameters</span></span>
<span data-ttu-id="854a8-150">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="854a8-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="854a8-151">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="854a8-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="854a8-152">Eingaben</span><span class="sxs-lookup"><span data-stu-id="854a8-152">INPUTS</span></span>

### <span data-ttu-id="854a8-153">System. String</span><span class="sxs-lookup"><span data-stu-id="854a8-153">System.String</span></span>

### <span data-ttu-id="854a8-154">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="854a8-154">System.Security.SecureString</span></span>

## <span data-ttu-id="854a8-155">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="854a8-155">OUTPUTS</span></span>

### <span data-ttu-id="854a8-156">Microsoft. Azure. Commands. ServiceFabric. Models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="854a8-156">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="854a8-157">Notizen</span><span class="sxs-lookup"><span data-stu-id="854a8-157">NOTES</span></span>

## <span data-ttu-id="854a8-158">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="854a8-158">RELATED LINKS</span></span>

[<span data-ttu-id="854a8-159">Remove-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="854a8-159">Remove-AzServiceFabricClusterCertificate</span></span>](./Remove-AzServiceFabricClusterCertificate.md)

[<span data-ttu-id="854a8-160">Neu – AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="854a8-160">New-AzServiceFabricCluster</span></span>](./New-AzServiceFabricCluster.md)
