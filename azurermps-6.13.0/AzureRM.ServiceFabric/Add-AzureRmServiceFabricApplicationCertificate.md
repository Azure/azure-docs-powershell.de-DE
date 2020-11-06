---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicefabric/add-azurermservicefabricapplicationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Add-AzureRmServiceFabricApplicationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Add-AzureRmServiceFabricApplicationCertificate.md
ms.openlocfilehash: 982eb6bf8c579d3f6ef9a5c6b74299ecf1114eb6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93482025"
---
# <span data-ttu-id="2dca0-101">Add-AzureRmServiceFabricApplicationCertificate</span><span class="sxs-lookup"><span data-stu-id="2dca0-101">Add-AzureRmServiceFabricApplicationCertificate</span></span>

## <span data-ttu-id="2dca0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2dca0-102">SYNOPSIS</span></span>
<span data-ttu-id="2dca0-103">Hinzufügen eines neuen Zertifikats zu den Skalierungs Sätzen des virtuellen Computers, aus denen sich der Cluster besteht</span><span class="sxs-lookup"><span data-stu-id="2dca0-103">Add a new certificate to the Virtual Machine Scale Set(s) that make up the cluster.</span></span> <span data-ttu-id="2dca0-104">Das Zertifikat soll als Anwendungszertifikat verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2dca0-104">The certificate is intended to be used as an application certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2dca0-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="2dca0-105">SYNTAX</span></span>

### <span data-ttu-id="2dca0-106">ByExistingKeyVault</span><span class="sxs-lookup"><span data-stu-id="2dca0-106">ByExistingKeyVault</span></span>
```
Add-AzureRmServiceFabricApplicationCertificate [-ResourceGroupName] <String> [-Name] <String>
 -SecretIdentifier <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2dca0-107">ByNewPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="2dca0-107">ByNewPfxAndVaultName</span></span>
```
Add-AzureRmServiceFabricApplicationCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-KeyVaultResouceGroupName <String>] [-KeyVaultName <String>] [-CertificateOutputFolder <String>]
 [-CertificatePassword <SecureString>] -CertificateSubjectName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2dca0-108">ByExistingPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="2dca0-108">ByExistingPfxAndVaultName</span></span>
```
Add-AzureRmServiceFabricApplicationCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-KeyVaultResouceGroupName <String>] [-KeyVaultName <String>] -CertificateFile <String>
 [-CertificatePassword <SecureString>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2dca0-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2dca0-109">DESCRIPTION</span></span>
<span data-ttu-id="2dca0-110">Verwenden **Sie Add-AzureRmServiceFabricApplicationCertificate** , um ein Zertifikat für alle Knoten im Cluster zu installieren.</span><span class="sxs-lookup"><span data-stu-id="2dca0-110">Use **Add-AzureRmServiceFabricApplicationCertificate** to install a certificate to all nodes in the cluster.</span></span> <span data-ttu-id="2dca0-111">Sie können ein Zertifikat angeben, das Sie bereits besitzen, oder das System für Sie erstellen, und es in einen neuen oder vorhandenen Azure Key Vault hochladen.</span><span class="sxs-lookup"><span data-stu-id="2dca0-111">You can specify a certificate you already have or have the system generate a new one for you, and upload it to a new or existing Azure key vault.</span></span>

## <span data-ttu-id="2dca0-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2dca0-112">EXAMPLES</span></span>

### <span data-ttu-id="2dca0-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="2dca0-113">Example 1</span></span>
```
PS c:> Add-AzureRmServiceFabricApplicationCertificate -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -SecretIdentifier 'https://contoso03vault.vault.azure.net/secrets/contoso03vaultrg/7f7de9131c034172b9df37ccc549524f'
```

<span data-ttu-id="2dca0-114">Mit diesem Befehl wird ein Zertifikat aus dem vorhandenen Azure Key Vault zu allen Knotentypen des Clusters hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="2dca0-114">This command will add a certificate from existing Azure key vault to all node types of the cluster.</span></span>

### <span data-ttu-id="2dca0-115">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="2dca0-115">Example 2</span></span>
```
PS c:\> $pwd = ConvertTo-SecureString -String '123' -AsPlainText -Force
PS C:\> Add-AzureRmServiceFabricApplicationCertificate -ResourceGroupName 'Group2' -Name 'Contoso02SFCluster' -KeyVaultName 'Contoso02Vault' -KeyVaultResouceGroupName 'Contoso02VaultRg'
        -CertificateSubjectName 'cn=Contoso.com' -CertificateOutputFolder 'c:\test' -CertificatePassword $pwd
```

<span data-ttu-id="2dca0-116">Mit diesem Befehl wird im Azure Key Vault ein selbstsigniertes Zertifikat mit dem Namen der Schlüssel Vault-Ressourcengruppe und dem schlüsseltresor Namen erstellt, auf allen Knotentypen des Clusters installiert und das Zertifikat Unterordner "c:\Test" heruntergeladen.</span><span class="sxs-lookup"><span data-stu-id="2dca0-116">This command will create a self-signed certificate in the Azure key vault with the key vault resource group name and key vault Name, installs to all node types of the cluster, and downloads the certificate under folder 'c:\test'.</span></span> <span data-ttu-id="2dca0-117">Der Name des heruntergeladenen Zertifikats entspricht dem Namen des schlüsseltresor-Zertifikats.</span><span class="sxs-lookup"><span data-stu-id="2dca0-117">The name of the certificate downloaded is same as the name of key vault certificate.</span></span>

## <span data-ttu-id="2dca0-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="2dca0-118">PARAMETERS</span></span>

### <span data-ttu-id="2dca0-119">-Certificatedatei</span><span class="sxs-lookup"><span data-stu-id="2dca0-119">-CertificateFile</span></span>
<span data-ttu-id="2dca0-120">Der vorhandene Zertifikat Dateipfad.</span><span class="sxs-lookup"><span data-stu-id="2dca0-120">The existing certificate file path.</span></span>

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

### <span data-ttu-id="2dca0-121">-CertificateOutputFolder</span><span class="sxs-lookup"><span data-stu-id="2dca0-121">-CertificateOutputFolder</span></span>
<span data-ttu-id="2dca0-122">Der Ordnerpfad des neuen Zertifikats, das erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="2dca0-122">The folder path of the new certificate to be created.</span></span>

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

### <span data-ttu-id="2dca0-123">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="2dca0-123">-CertificatePassword</span></span>
<span data-ttu-id="2dca0-124">Das Kennwort der PFX-Datei.</span><span class="sxs-lookup"><span data-stu-id="2dca0-124">The password of the pfx file.</span></span>

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

### <span data-ttu-id="2dca0-125">-CertificateSubjectName</span><span class="sxs-lookup"><span data-stu-id="2dca0-125">-CertificateSubjectName</span></span>
<span data-ttu-id="2dca0-126">Der DNS-Name des zu erstellenden Zertifikats.</span><span class="sxs-lookup"><span data-stu-id="2dca0-126">The Dns name of the certificate to be created.</span></span>

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

### <span data-ttu-id="2dca0-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2dca0-127">-DefaultProfile</span></span>
<span data-ttu-id="2dca0-128">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2dca0-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2dca0-129">-Keyvaultname</span><span class="sxs-lookup"><span data-stu-id="2dca0-129">-KeyVaultName</span></span>
<span data-ttu-id="2dca0-130">Azure Key Vault-Name.</span><span class="sxs-lookup"><span data-stu-id="2dca0-130">Azure key vault name.</span></span>

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

### <span data-ttu-id="2dca0-131">-KeyVaultResouceGroupName</span><span class="sxs-lookup"><span data-stu-id="2dca0-131">-KeyVaultResouceGroupName</span></span>
<span data-ttu-id="2dca0-132">Azure Key Vault-Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="2dca0-132">Azure key vault resource group name.</span></span>

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

### <span data-ttu-id="2dca0-133">-Name</span><span class="sxs-lookup"><span data-stu-id="2dca0-133">-Name</span></span>
<span data-ttu-id="2dca0-134">Geben Sie den Namen des Clusters an.</span><span class="sxs-lookup"><span data-stu-id="2dca0-134">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="2dca0-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2dca0-135">-ResourceGroupName</span></span>
<span data-ttu-id="2dca0-136">Geben Sie den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="2dca0-136">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="2dca0-137">-SecretIdentifier</span><span class="sxs-lookup"><span data-stu-id="2dca0-137">-SecretIdentifier</span></span>
<span data-ttu-id="2dca0-138">Der vorhandene Azure Key Vault-geheim-URI.</span><span class="sxs-lookup"><span data-stu-id="2dca0-138">The existing Azure key vault secret uri.</span></span>

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

### <span data-ttu-id="2dca0-139">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="2dca0-139">-Confirm</span></span>
<span data-ttu-id="2dca0-140">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2dca0-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2dca0-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2dca0-141">-WhatIf</span></span>
<span data-ttu-id="2dca0-142">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2dca0-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2dca0-143">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2dca0-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2dca0-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2dca0-144">CommonParameters</span></span>
<span data-ttu-id="2dca0-145">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2dca0-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2dca0-146">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2dca0-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2dca0-147">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2dca0-147">INPUTS</span></span>

### <span data-ttu-id="2dca0-148">System. String</span><span class="sxs-lookup"><span data-stu-id="2dca0-148">System.String</span></span>
<span data-ttu-id="2dca0-149">Parameter: certificatedatei (ByValue), CertificateOutputFolder (ByValue), CertificateSubjectName (ByValue), keyvaultname (ByValue), KeyVaultResouceGroupName (ByValue), SecretIdentifier (ByValue)</span><span class="sxs-lookup"><span data-stu-id="2dca0-149">Parameters: CertificateFile (ByValue), CertificateOutputFolder (ByValue), CertificateSubjectName (ByValue), KeyVaultName (ByValue), KeyVaultResouceGroupName (ByValue), SecretIdentifier (ByValue)</span></span>

### <span data-ttu-id="2dca0-150">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="2dca0-150">System.Security.SecureString</span></span>
<span data-ttu-id="2dca0-151">Parameter: CertificatePassword (ByValue)</span><span class="sxs-lookup"><span data-stu-id="2dca0-151">Parameters: CertificatePassword (ByValue)</span></span>

## <span data-ttu-id="2dca0-152">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2dca0-152">OUTPUTS</span></span>

### <span data-ttu-id="2dca0-153">Microsoft. Azure. Commands. ServiceFabric. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="2dca0-153">Microsoft.Azure.Commands.ServiceFabric.Models.PSKeyVault</span></span>

## <span data-ttu-id="2dca0-154">Notizen</span><span class="sxs-lookup"><span data-stu-id="2dca0-154">NOTES</span></span>

## <span data-ttu-id="2dca0-155">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2dca0-155">RELATED LINKS</span></span>

[<span data-ttu-id="2dca0-156">Add-AzureRmServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="2dca0-156">Add-AzureRmServiceFabricClusterCertificate</span></span>](./Add-AzureRmServiceFabricClusterCertificate.md)

[<span data-ttu-id="2dca0-157">Neu – AzureRmServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="2dca0-157">New-AzureRmServiceFabricCluster</span></span>](./New-AzureRmServiceFabricCluster.md)
