---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Add-AzureRmServiceFabricApplicationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Add-AzureRmServiceFabricApplicationCertificate.md
ms.openlocfilehash: 6d77c795415bca1a8bffbed6d09062f394782e94
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503189"
---
# <span data-ttu-id="a3ee9-101">Add-AzureRmServiceFabricApplicationCertificate</span><span class="sxs-lookup"><span data-stu-id="a3ee9-101">Add-AzureRmServiceFabricApplicationCertificate</span></span>

## <span data-ttu-id="a3ee9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a3ee9-102">SYNOPSIS</span></span>
<span data-ttu-id="a3ee9-103">Hinzufügen eines neuen Zertifikats zu den Skalierungs Sätzen des virtuellen Computers, aus denen sich der Cluster besteht</span><span class="sxs-lookup"><span data-stu-id="a3ee9-103">Add a new certificate to the Virtual Machine Scale Set(s) that make up the cluster.</span></span> <span data-ttu-id="a3ee9-104">Das Zertifikat soll als Anwendungszertifikat verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a3ee9-104">The certificate is intended to be used as an application certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a3ee9-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a3ee9-105">SYNTAX</span></span>

### <span data-ttu-id="a3ee9-106">ByExistingKeyVault</span><span class="sxs-lookup"><span data-stu-id="a3ee9-106">ByExistingKeyVault</span></span>
```
Add-AzureRmServiceFabricApplicationCertificate [-ResourceGroupName] <String> [-Name] <String>
 -SecretIdentifier <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a3ee9-107">ByNewPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="a3ee9-107">ByNewPfxAndVaultName</span></span>
```
Add-AzureRmServiceFabricApplicationCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-KeyVaultResouceGroupName <String>] [-KeyVaultName <String>] [-CertificateOutputFolder <String>]
 [-CertificatePassword <SecureString>] -CertificateSubjectName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a3ee9-108">ByExistingPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="a3ee9-108">ByExistingPfxAndVaultName</span></span>
```
Add-AzureRmServiceFabricApplicationCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-KeyVaultResouceGroupName <String>] [-KeyVaultName <String>] -CertificateFile <String>
 [-CertificatePassword <SecureString>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a3ee9-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a3ee9-109">DESCRIPTION</span></span>
<span data-ttu-id="a3ee9-110">Verwenden **Sie Add-AzureRmServiceFabricApplicationCertificate** , um ein Zertifikat für alle Knoten im Cluster zu installieren.</span><span class="sxs-lookup"><span data-stu-id="a3ee9-110">Use **Add-AzureRmServiceFabricApplicationCertificate** to install a certificate to all nodes in the cluster.</span></span> <span data-ttu-id="a3ee9-111">Sie können ein Zertifikat angeben, das Sie bereits besitzen, oder das System für Sie erstellen, und es in einen neuen oder vorhandenen Azure Key Vault hochladen.</span><span class="sxs-lookup"><span data-stu-id="a3ee9-111">You can specify a certificate you already have or have the system generate a new one for you, and upload it to a new or existing Azure key vault.</span></span>

## <span data-ttu-id="a3ee9-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a3ee9-112">EXAMPLES</span></span>

### <span data-ttu-id="a3ee9-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a3ee9-113">Example 1</span></span>
```
PS c:> Add-AzureRmServiceFabricApplicationCertificate -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -SecretIdentifier 'https://contoso03vault.vault.azure.net/secrets/contoso03vaultrg/7f7de9131c034172b9df37ccc549524f'
```

<span data-ttu-id="a3ee9-114">Mit diesem Befehl wird ein Zertifikat aus dem vorhandenen Azure Key Vault zu allen Knotentypen des Clusters hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="a3ee9-114">This command will add a certificate from existing Azure key vault to all node types of the cluster.</span></span>

### <span data-ttu-id="a3ee9-115">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="a3ee9-115">Example 2</span></span>
```
PS c:\> $pwd = ConvertTo-SecureString -String '123' -AsPlainText -Force
PS C:\> Add-AzureRmServiceFabricApplicationCertificate -ResourceGroupName 'Group2' -Name 'Contoso02SFCluster' -KeyVaultName 'Contoso02Vault' -KeyVaultResouceGroupName 'Contoso02VaultRg'
        -CertificateSubjectName 'cn=Contoso.com' -CertificateOutputFolder 'c:\test' -CertificatePassword $pwd
```

<span data-ttu-id="a3ee9-116">Mit diesem Befehl wird im Azure Key Vault ein selbstsigniertes Zertifikat mit dem Namen der Schlüssel Vault-Ressourcengruppe und dem schlüsseltresor Namen erstellt, auf allen Knotentypen des Clusters installiert und das Zertifikat Unterordner "c:\Test" heruntergeladen.</span><span class="sxs-lookup"><span data-stu-id="a3ee9-116">This command will create a self-signed certificate in the Azure key vault with the key vault resource group name and key vault Name, installs to all node types of the cluster, and downloads the certificate under folder 'c:\test'.</span></span> <span data-ttu-id="a3ee9-117">Der Name des heruntergeladenen Zertifikats entspricht dem Namen des schlüsseltresor-Zertifikats.</span><span class="sxs-lookup"><span data-stu-id="a3ee9-117">The name of the certificate downloaded is same as the name of key vault certificate.</span></span>

## <span data-ttu-id="a3ee9-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="a3ee9-118">PARAMETERS</span></span>

### <span data-ttu-id="a3ee9-119">-Certificatedatei</span><span class="sxs-lookup"><span data-stu-id="a3ee9-119">-CertificateFile</span></span>
<span data-ttu-id="a3ee9-120">Der vorhandene Zertifikat Dateipfad.</span><span class="sxs-lookup"><span data-stu-id="a3ee9-120">The existing certificate file path.</span></span>

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

### <span data-ttu-id="a3ee9-121">-CertificateOutputFolder</span><span class="sxs-lookup"><span data-stu-id="a3ee9-121">-CertificateOutputFolder</span></span>
<span data-ttu-id="a3ee9-122">Der Ordnerpfad des neuen Zertifikats, das erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="a3ee9-122">The folder path of the new certificate to be created.</span></span>

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

### <span data-ttu-id="a3ee9-123">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="a3ee9-123">-CertificatePassword</span></span>
<span data-ttu-id="a3ee9-124">Das Kennwort der PFX-Datei.</span><span class="sxs-lookup"><span data-stu-id="a3ee9-124">The password of the pfx file.</span></span>

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

### <span data-ttu-id="a3ee9-125">-CertificateSubjectName</span><span class="sxs-lookup"><span data-stu-id="a3ee9-125">-CertificateSubjectName</span></span>
<span data-ttu-id="a3ee9-126">Der DNS-Name des zu erstellenden Zertifikats.</span><span class="sxs-lookup"><span data-stu-id="a3ee9-126">The Dns name of the certificate to be created.</span></span>

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

### <span data-ttu-id="a3ee9-127">-Keyvaultname</span><span class="sxs-lookup"><span data-stu-id="a3ee9-127">-KeyVaultName</span></span>
<span data-ttu-id="a3ee9-128">Azure Key Vault-Name.</span><span class="sxs-lookup"><span data-stu-id="a3ee9-128">Azure key vault name.</span></span>

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

### <span data-ttu-id="a3ee9-129">-KeyVaultResouceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3ee9-129">-KeyVaultResouceGroupName</span></span>
<span data-ttu-id="a3ee9-130">Azure Key Vault-Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="a3ee9-130">Azure key vault resource group name.</span></span>

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

### <span data-ttu-id="a3ee9-131">-Name</span><span class="sxs-lookup"><span data-stu-id="a3ee9-131">-Name</span></span>
<span data-ttu-id="a3ee9-132">Geben Sie den Namen des Clusters an.</span><span class="sxs-lookup"><span data-stu-id="a3ee9-132">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="a3ee9-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3ee9-133">-ResourceGroupName</span></span>
<span data-ttu-id="a3ee9-134">Geben Sie den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="a3ee9-134">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="a3ee9-135">-SecretIdentifier</span><span class="sxs-lookup"><span data-stu-id="a3ee9-135">-SecretIdentifier</span></span>
<span data-ttu-id="a3ee9-136">Der vorhandene Azure Key Vault-geheim-URI.</span><span class="sxs-lookup"><span data-stu-id="a3ee9-136">The existing Azure key vault secret uri.</span></span>

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

### <span data-ttu-id="a3ee9-137">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a3ee9-137">-Confirm</span></span>
<span data-ttu-id="a3ee9-138">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a3ee9-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a3ee9-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a3ee9-139">-WhatIf</span></span>
<span data-ttu-id="a3ee9-140">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a3ee9-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a3ee9-141">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a3ee9-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a3ee9-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3ee9-142">-DefaultProfile</span></span>
<span data-ttu-id="a3ee9-143">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a3ee9-143">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3ee9-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3ee9-144">CommonParameters</span></span>
<span data-ttu-id="a3ee9-145">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3ee9-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3ee9-146">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a3ee9-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3ee9-147">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a3ee9-147">INPUTS</span></span>

### <span data-ttu-id="a3ee9-148">System. String</span><span class="sxs-lookup"><span data-stu-id="a3ee9-148">System.String</span></span>

## <span data-ttu-id="a3ee9-149">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a3ee9-149">OUTPUTS</span></span>

### <span data-ttu-id="a3ee9-150">Microsoft. Azure. Commands. ServiceFabric. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="a3ee9-150">Microsoft.Azure.Commands.ServiceFabric.Models.PSKeyVault</span></span>

## <span data-ttu-id="a3ee9-151">Notizen</span><span class="sxs-lookup"><span data-stu-id="a3ee9-151">NOTES</span></span>

## <span data-ttu-id="a3ee9-152">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a3ee9-152">RELATED LINKS</span></span>

[<span data-ttu-id="a3ee9-153">Add-AzureRmServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="a3ee9-153">Add-AzureRmServiceFabricClusterCertificate</span></span>](./Add-AzureRmServiceFabricClusterCertificate.md)

[<span data-ttu-id="a3ee9-154">Neu – AzureRmServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="a3ee9-154">New-AzureRmServiceFabricCluster</span></span>](./New-AzureRmServiceFabricCluster.md)
