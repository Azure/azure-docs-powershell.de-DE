---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/add-azservicefabricapplicationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricApplicationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricApplicationCertificate.md
ms.openlocfilehash: 58547205bc0edae3ea1ab9ff56d3df1ef71214f8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93659332"
---
# <span data-ttu-id="78ead-101">Add-AzServiceFabricApplicationCertificate</span><span class="sxs-lookup"><span data-stu-id="78ead-101">Add-AzServiceFabricApplicationCertificate</span></span>

## <span data-ttu-id="78ead-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="78ead-102">SYNOPSIS</span></span>
<span data-ttu-id="78ead-103">Hinzufügen eines neuen Zertifikats zu den Skalierungs Sätzen des virtuellen Computers, aus denen sich der Cluster besteht</span><span class="sxs-lookup"><span data-stu-id="78ead-103">Add a new certificate to the Virtual Machine Scale Set(s) that make up the cluster.</span></span> <span data-ttu-id="78ead-104">Das Zertifikat soll als Anwendungszertifikat verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="78ead-104">The certificate is intended to be used as an application certificate.</span></span>

## <span data-ttu-id="78ead-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="78ead-105">SYNTAX</span></span>

### <span data-ttu-id="78ead-106">ByExistingKeyVault</span><span class="sxs-lookup"><span data-stu-id="78ead-106">ByExistingKeyVault</span></span>
```
Add-AzServiceFabricApplicationCertificate [-ResourceGroupName] <String> [-Name] <String>
 -SecretIdentifier <String> [-CertificateCommonName <String>] [-CertificateIssuerThumbprint <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="78ead-107">ByNewPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="78ead-107">ByNewPfxAndVaultName</span></span>
```
Add-AzServiceFabricApplicationCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-KeyVaultResouceGroupName <String>] [-KeyVaultName <String>] [-CertificateOutputFolder <String>]
 [-CertificatePassword <SecureString>] -CertificateSubjectName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="78ead-108">ByExistingPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="78ead-108">ByExistingPfxAndVaultName</span></span>
```
Add-AzServiceFabricApplicationCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-KeyVaultResouceGroupName <String>] [-KeyVaultName <String>] -CertificateFile <String>
 [-CertificatePassword <SecureString>] [-CertificateCommonName <String>]
 [-CertificateIssuerThumbprint <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="78ead-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="78ead-109">DESCRIPTION</span></span>
<span data-ttu-id="78ead-110">Verwenden **Sie Add-AzServiceFabricApplicationCertificate** , um ein Zertifikat für alle Knoten im Cluster zu installieren.</span><span class="sxs-lookup"><span data-stu-id="78ead-110">Use **Add-AzServiceFabricApplicationCertificate** to install a certificate to all nodes in the cluster.</span></span> <span data-ttu-id="78ead-111">Sie können ein Zertifikat angeben, das Sie bereits besitzen, oder das System für Sie erstellen, und es in einen neuen oder vorhandenen Azure Key Vault hochladen.</span><span class="sxs-lookup"><span data-stu-id="78ead-111">You can specify a certificate you already have or have the system generate a new one for you, and upload it to a new or existing Azure key vault.</span></span>

## <span data-ttu-id="78ead-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="78ead-112">EXAMPLES</span></span>

### <span data-ttu-id="78ead-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="78ead-113">Example 1</span></span>
```
PS c:> Add-AzServiceFabricApplicationCertificate -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -SecretIdentifier 'https://contoso03vault.vault.azure.net/secrets/contoso03vaultrg/7f7de9131c034172b9df37ccc549524f'
```

<span data-ttu-id="78ead-114">Mit diesem Befehl wird ein Zertifikat aus dem vorhandenen Azure Key Vault zu allen Knotentypen des Clusters hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="78ead-114">This command will add a certificate from existing Azure key vault to all node types of the cluster.</span></span>

### <span data-ttu-id="78ead-115">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="78ead-115">Example 2</span></span>
```
PS c:\> $pwd = ConvertTo-SecureString -String '123' -AsPlainText -Force
PS C:\> Add-AzServiceFabricApplicationCertificate -ResourceGroupName 'Group2' -Name 'Contoso02SFCluster' -KeyVaultName 'Contoso02Vault' -KeyVaultResouceGroupName 'Contoso02VaultRg'
        -CertificateSubjectName 'cn=Contoso.com' -CertificateOutputFolder 'c:\test' -CertificatePassword $pwd
```

<span data-ttu-id="78ead-116">Mit diesem Befehl wird im Azure Key Vault ein selbstsigniertes Zertifikat mit dem Namen der Schlüssel Vault-Ressourcengruppe und dem schlüsseltresor Namen erstellt, auf allen Knotentypen des Clusters installiert und das Zertifikat Unterordner "c:\Test" heruntergeladen.</span><span class="sxs-lookup"><span data-stu-id="78ead-116">This command will create a self-signed certificate in the Azure key vault with the key vault resource group name and key vault Name, installs to all node types of the cluster, and downloads the certificate under folder 'c:\test'.</span></span> <span data-ttu-id="78ead-117">Der Name des heruntergeladenen Zertifikats entspricht dem Namen des schlüsseltresor-Zertifikats.</span><span class="sxs-lookup"><span data-stu-id="78ead-117">The name of the certificate downloaded is same as the name of key vault certificate.</span></span>

## <span data-ttu-id="78ead-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="78ead-118">PARAMETERS</span></span>

### <span data-ttu-id="78ead-119">-CertificateCommonName</span><span class="sxs-lookup"><span data-stu-id="78ead-119">-CertificateCommonName</span></span>
<span data-ttu-id="78ead-120">Allgemeiner Zertifikatname</span><span class="sxs-lookup"><span data-stu-id="78ead-120">Certificate common name</span></span>

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

### <span data-ttu-id="78ead-121">-Certificatedatei</span><span class="sxs-lookup"><span data-stu-id="78ead-121">-CertificateFile</span></span>
<span data-ttu-id="78ead-122">Der vorhandene Zertifikat Dateipfad.</span><span class="sxs-lookup"><span data-stu-id="78ead-122">The existing certificate file path.</span></span>

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

### <span data-ttu-id="78ead-123">-CertificateIssuerThumbprint</span><span class="sxs-lookup"><span data-stu-id="78ead-123">-CertificateIssuerThumbprint</span></span>
<span data-ttu-id="78ead-124">Fingerabdruck des Zertifikatausstellers, getrennt durch Kommas, wenn mehr als eine</span><span class="sxs-lookup"><span data-stu-id="78ead-124">Certificate issuer thumbprint, separated by commas if more than one</span></span>

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

### <span data-ttu-id="78ead-125">-CertificateOutputFolder</span><span class="sxs-lookup"><span data-stu-id="78ead-125">-CertificateOutputFolder</span></span>
<span data-ttu-id="78ead-126">Der Ordnerpfad des neuen Zertifikats, das erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="78ead-126">The folder path of the new certificate to be created.</span></span>

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

### <span data-ttu-id="78ead-127">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="78ead-127">-CertificatePassword</span></span>
<span data-ttu-id="78ead-128">Das Kennwort der PFX-Datei.</span><span class="sxs-lookup"><span data-stu-id="78ead-128">The password of the pfx file.</span></span>

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

### <span data-ttu-id="78ead-129">-CertificateSubjectName</span><span class="sxs-lookup"><span data-stu-id="78ead-129">-CertificateSubjectName</span></span>
<span data-ttu-id="78ead-130">Der DNS-Name des zu erstellenden Zertifikats.</span><span class="sxs-lookup"><span data-stu-id="78ead-130">The Dns name of the certificate to be created.</span></span>

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

### <span data-ttu-id="78ead-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78ead-131">-DefaultProfile</span></span>
<span data-ttu-id="78ead-132">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="78ead-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="78ead-133">-Keyvaultname</span><span class="sxs-lookup"><span data-stu-id="78ead-133">-KeyVaultName</span></span>
<span data-ttu-id="78ead-134">Azure Key Vault-Name.</span><span class="sxs-lookup"><span data-stu-id="78ead-134">Azure key vault name.</span></span>

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

### <span data-ttu-id="78ead-135">-KeyVaultResouceGroupName</span><span class="sxs-lookup"><span data-stu-id="78ead-135">-KeyVaultResouceGroupName</span></span>
<span data-ttu-id="78ead-136">Azure Key Vault-Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="78ead-136">Azure key vault resource group name.</span></span>

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

### <span data-ttu-id="78ead-137">-Name</span><span class="sxs-lookup"><span data-stu-id="78ead-137">-Name</span></span>
<span data-ttu-id="78ead-138">Geben Sie den Namen des Clusters an.</span><span class="sxs-lookup"><span data-stu-id="78ead-138">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="78ead-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78ead-139">-ResourceGroupName</span></span>
<span data-ttu-id="78ead-140">Geben Sie den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="78ead-140">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="78ead-141">-SecretIdentifier</span><span class="sxs-lookup"><span data-stu-id="78ead-141">-SecretIdentifier</span></span>
<span data-ttu-id="78ead-142">Der vorhandene Azure Key Vault-geheim-URI.</span><span class="sxs-lookup"><span data-stu-id="78ead-142">The existing Azure key vault secret uri.</span></span>

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

### <span data-ttu-id="78ead-143">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="78ead-143">-Confirm</span></span>
<span data-ttu-id="78ead-144">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="78ead-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="78ead-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="78ead-145">-WhatIf</span></span>
<span data-ttu-id="78ead-146">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="78ead-146">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="78ead-147">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="78ead-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="78ead-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78ead-148">CommonParameters</span></span>
<span data-ttu-id="78ead-149">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="78ead-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78ead-150">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="78ead-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78ead-151">Eingaben</span><span class="sxs-lookup"><span data-stu-id="78ead-151">INPUTS</span></span>

### <span data-ttu-id="78ead-152">System. String</span><span class="sxs-lookup"><span data-stu-id="78ead-152">System.String</span></span>

### <span data-ttu-id="78ead-153">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="78ead-153">System.Security.SecureString</span></span>

## <span data-ttu-id="78ead-154">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="78ead-154">OUTPUTS</span></span>

### <span data-ttu-id="78ead-155">Microsoft. Azure. Commands. ServiceFabric. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="78ead-155">Microsoft.Azure.Commands.ServiceFabric.Models.PSKeyVault</span></span>

## <span data-ttu-id="78ead-156">Notizen</span><span class="sxs-lookup"><span data-stu-id="78ead-156">NOTES</span></span>

## <span data-ttu-id="78ead-157">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="78ead-157">RELATED LINKS</span></span>

[<span data-ttu-id="78ead-158">Add-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="78ead-158">Add-AzServiceFabricClusterCertificate</span></span>](./Add-AzServiceFabricClusterCertificate.md)

[<span data-ttu-id="78ead-159">Neu – AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="78ead-159">New-AzServiceFabricCluster</span></span>](./New-AzServiceFabricCluster.md)
