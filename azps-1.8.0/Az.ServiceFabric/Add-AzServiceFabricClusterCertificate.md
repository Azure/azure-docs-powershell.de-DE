---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/add-azservicefabricclustercertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricClusterCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricClusterCertificate.md
ms.openlocfilehash: bf96b4a21e12e41ce067d669b50c05831a162a8b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93659331"
---
# <span data-ttu-id="cded4-101">Add-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="cded4-101">Add-AzServiceFabricClusterCertificate</span></span>

## <span data-ttu-id="cded4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="cded4-102">SYNOPSIS</span></span>
<span data-ttu-id="cded4-103">Hinzufügen eines sekundären Cluster Zertifikats zum Cluster</span><span class="sxs-lookup"><span data-stu-id="cded4-103">Add a secondary cluster certificate to the cluster.</span></span>

## <span data-ttu-id="cded4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="cded4-104">SYNTAX</span></span>

### <span data-ttu-id="cded4-105">ByExistingKeyVault</span><span class="sxs-lookup"><span data-stu-id="cded4-105">ByExistingKeyVault</span></span>
```
Add-AzServiceFabricClusterCertificate [-ResourceGroupName] <String> [-Name] <String> -SecretIdentifier <String>
 [-CertificateCommonName <String>] [-CertificateIssuerThumbprint <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cded4-106">ByNewPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="cded4-106">ByNewPfxAndVaultName</span></span>
```
Add-AzServiceFabricClusterCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-KeyVaultResouceGroupName <String>] [-KeyVaultName <String>] [-CertificateOutputFolder <String>]
 [-CertificatePassword <SecureString>] -CertificateSubjectName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cded4-107">ByExistingPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="cded4-107">ByExistingPfxAndVaultName</span></span>
```
Add-AzServiceFabricClusterCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-KeyVaultResouceGroupName <String>] [-KeyVaultName <String>] -CertificateFile <String>
 [-CertificatePassword <SecureString>] [-CertificateCommonName <String>]
 [-CertificateIssuerThumbprint <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="cded4-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cded4-108">DESCRIPTION</span></span>
<span data-ttu-id="cded4-109">Verwenden **Sie Add-AzServiceFabricClusterCertificate** zum Hinzufügen eines sekundären Cluster Zertifikats, entweder aus einem vorhandenen Azure Key Vault oder durch Erstellen eines neuen Azure Key Vault mithilfe eines vorhandenen Zertifikats oder aus einem neuen selbstsignierten Zertifikat, das erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="cded4-109">Use **Add-AzServiceFabricClusterCertificate** to add a secondary cluster certificate, either from an existing Azure key vault or creating a new Azure key vault using an existing certificate provided or from a new self-signed certificate created.</span></span> <span data-ttu-id="cded4-110">Wenn vorhanden, wird der sekundäre Cluster überschrieben.</span><span class="sxs-lookup"><span data-stu-id="cded4-110">It will override the secondary cluster if there is any.</span></span>

## <span data-ttu-id="cded4-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="cded4-111">EXAMPLES</span></span>

### <span data-ttu-id="cded4-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="cded4-112">Example 1</span></span>
```
Add-AzServiceFabricClusterCertificate -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' 
-SecretIdentifier 'https://contoso03vault.vault.azure.net/secrets/contoso03vaultrg/7f7de9131c034172b9df37ccc549524f'
```

<span data-ttu-id="cded4-113">Mit diesem Befehl wird ein Zertifikat im vorhandenen Azure Key Vault als sekundäres Cluster Zertifikat hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="cded4-113">This command will add a certificate in the existing Azure key vault as a secondary cluster certificate.</span></span>

### <span data-ttu-id="cded4-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="cded4-114">Example 2</span></span>
```
PS c:\> $pwd = ConvertTo-SecureString -String "123" -AsPlainText -Force
PS c:\> add-AzServiceFabricClusterCertificate -ResourceGroupName 'Group2' -Name 'Contoso02SFCluster'  -CertificateSubjectName 'Contoso.com' 
-CertificateOutputFolder 'c:\test' -CertificatePassword $pwd
```

<span data-ttu-id="cded4-115">Mit diesem Befehl wird im Azure Key Vault ein selbstsigniertes Zertifikat erstellt und der Cluster so aktualisiert, dass es als sekundäres Cluster Zertifikat verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="cded4-115">This command will create a self-signed certificate in the Azure key vault and upgrade the cluster to use it as a secondary cluster certificate.</span></span>

## <span data-ttu-id="cded4-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="cded4-116">PARAMETERS</span></span>

### <span data-ttu-id="cded4-117">-CertificateCommonName</span><span class="sxs-lookup"><span data-stu-id="cded4-117">-CertificateCommonName</span></span>
<span data-ttu-id="cded4-118">Allgemeiner Zertifikatname</span><span class="sxs-lookup"><span data-stu-id="cded4-118">Certificate common name</span></span>

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

### <span data-ttu-id="cded4-119">-Certificatedatei</span><span class="sxs-lookup"><span data-stu-id="cded4-119">-CertificateFile</span></span>
<span data-ttu-id="cded4-120">Der vorhandene Zertifikat Dateipfad.</span><span class="sxs-lookup"><span data-stu-id="cded4-120">The existing certificate file path.</span></span>

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

### <span data-ttu-id="cded4-121">-CertificateIssuerThumbprint</span><span class="sxs-lookup"><span data-stu-id="cded4-121">-CertificateIssuerThumbprint</span></span>
<span data-ttu-id="cded4-122">Fingerabdruck des Zertifikatausstellers, getrennt durch Kommas, wenn mehr als eine</span><span class="sxs-lookup"><span data-stu-id="cded4-122">Certificate issuer thumbprint, separated by commas if more than one</span></span>

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

### <span data-ttu-id="cded4-123">-CertificateOutputFolder</span><span class="sxs-lookup"><span data-stu-id="cded4-123">-CertificateOutputFolder</span></span>
<span data-ttu-id="cded4-124">Der Ordner des neuen Zertifikats, das erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="cded4-124">The folder of the new certificate to be created.</span></span>

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

### <span data-ttu-id="cded4-125">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="cded4-125">-CertificatePassword</span></span>
<span data-ttu-id="cded4-126">Das Kennwort der Zertifikatsdatei.</span><span class="sxs-lookup"><span data-stu-id="cded4-126">The password of the certificate file.</span></span>

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

### <span data-ttu-id="cded4-127">-CertificateSubjectName</span><span class="sxs-lookup"><span data-stu-id="cded4-127">-CertificateSubjectName</span></span>
<span data-ttu-id="cded4-128">Der DNS-Name des zu erstellenden Zertifikats.</span><span class="sxs-lookup"><span data-stu-id="cded4-128">The Dns name of the certificate to be created.</span></span>

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

### <span data-ttu-id="cded4-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cded4-129">-DefaultProfile</span></span>
<span data-ttu-id="cded4-130">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="cded4-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cded4-131">-Keyvaultname</span><span class="sxs-lookup"><span data-stu-id="cded4-131">-KeyVaultName</span></span>
<span data-ttu-id="cded4-132">Azure Key Vault-Name.</span><span class="sxs-lookup"><span data-stu-id="cded4-132">Azure key vault name.</span></span>

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

### <span data-ttu-id="cded4-133">-KeyVaultResouceGroupName</span><span class="sxs-lookup"><span data-stu-id="cded4-133">-KeyVaultResouceGroupName</span></span>
<span data-ttu-id="cded4-134">Azure Key Vault-Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="cded4-134">Azure key vault resource group name.</span></span>

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

### <span data-ttu-id="cded4-135">-Name</span><span class="sxs-lookup"><span data-stu-id="cded4-135">-Name</span></span>
<span data-ttu-id="cded4-136">Geben Sie den Namen des Clusters an.</span><span class="sxs-lookup"><span data-stu-id="cded4-136">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="cded4-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cded4-137">-ResourceGroupName</span></span>
<span data-ttu-id="cded4-138">Gibt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="cded4-138">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="cded4-139">-SecretIdentifier</span><span class="sxs-lookup"><span data-stu-id="cded4-139">-SecretIdentifier</span></span>
<span data-ttu-id="cded4-140">Die vorhandene Azure Key Vault Secret-URL.</span><span class="sxs-lookup"><span data-stu-id="cded4-140">The existing Azure key vault secret Url.</span></span>

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

### <span data-ttu-id="cded4-141">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="cded4-141">-Confirm</span></span>
<span data-ttu-id="cded4-142">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="cded4-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cded4-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cded4-143">-WhatIf</span></span>
<span data-ttu-id="cded4-144">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="cded4-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cded4-145">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="cded4-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cded4-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cded4-146">CommonParameters</span></span>
<span data-ttu-id="cded4-147">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cded4-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cded4-148">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cded4-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cded4-149">Eingaben</span><span class="sxs-lookup"><span data-stu-id="cded4-149">INPUTS</span></span>

### <span data-ttu-id="cded4-150">System. String</span><span class="sxs-lookup"><span data-stu-id="cded4-150">System.String</span></span>

### <span data-ttu-id="cded4-151">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="cded4-151">System.Security.SecureString</span></span>

## <span data-ttu-id="cded4-152">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="cded4-152">OUTPUTS</span></span>

### <span data-ttu-id="cded4-153">Microsoft. Azure. Commands. ServiceFabric. Models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="cded4-153">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="cded4-154">Notizen</span><span class="sxs-lookup"><span data-stu-id="cded4-154">NOTES</span></span>

## <span data-ttu-id="cded4-155">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="cded4-155">RELATED LINKS</span></span>

[<span data-ttu-id="cded4-156">Remove-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="cded4-156">Remove-AzServiceFabricClusterCertificate</span></span>](./Remove-AzServiceFabricClusterCertificate.md)

[<span data-ttu-id="cded4-157">Neu – AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="cded4-157">New-AzServiceFabricCluster</span></span>](./New-AzServiceFabricCluster.md)

[<span data-ttu-id="cded4-158">Add-AzServiceFabricApplicationCertificate</span><span class="sxs-lookup"><span data-stu-id="cded4-158">Add-AzServiceFabricApplicationCertificate</span></span>](./Add-AzServiceFabricApplicationCertificate.md)
