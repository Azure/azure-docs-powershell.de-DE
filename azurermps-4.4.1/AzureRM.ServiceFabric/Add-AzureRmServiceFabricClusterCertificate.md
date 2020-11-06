---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Add-AzureRmServiceFabricClusterCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Add-AzureRmServiceFabricClusterCertificate.md
ms.openlocfilehash: 498b09867436e6aa272abd8796b41f159cd388f8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503186"
---
# <span data-ttu-id="40e5e-101">Add-AzureRmServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="40e5e-101">Add-AzureRmServiceFabricClusterCertificate</span></span>

## <span data-ttu-id="40e5e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="40e5e-102">SYNOPSIS</span></span>
<span data-ttu-id="40e5e-103">Hinzufügen eines sekundären Cluster Zertifikats zum Cluster</span><span class="sxs-lookup"><span data-stu-id="40e5e-103">Add a secondary cluster certificate to the cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="40e5e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="40e5e-104">SYNTAX</span></span>

### <span data-ttu-id="40e5e-105">ByExistingKeyVault</span><span class="sxs-lookup"><span data-stu-id="40e5e-105">ByExistingKeyVault</span></span>
```
Add-AzureRmServiceFabricClusterCertificate [-ResourceGroupName] <String> [-Name] <String>
 -SecretIdentifier <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="40e5e-106">ByNewPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="40e5e-106">ByNewPfxAndVaultName</span></span>
```
Add-AzureRmServiceFabricClusterCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-KeyVaultResouceGroupName <String>] [-KeyVaultName <String>] [-CertificateOutputFolder <String>]
 [-CertificatePassword <SecureString>] -CertificateSubjectName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="40e5e-107">ByExistingPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="40e5e-107">ByExistingPfxAndVaultName</span></span>
```
Add-AzureRmServiceFabricClusterCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-KeyVaultResouceGroupName <String>] [-KeyVaultName <String>] -CertificateFile <String>
 [-CertificatePassword <SecureString>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="40e5e-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="40e5e-108">DESCRIPTION</span></span>
<span data-ttu-id="40e5e-109">Verwenden **Sie Add-AzureRmServiceFabricClusterCertificate** zum Hinzufügen eines sekundären Cluster Zertifikats, entweder aus einem vorhandenen Azure Key Vault oder durch Erstellen eines neuen Azure Key Vault mithilfe eines vorhandenen Zertifikats oder aus einem neuen selbstsignierten Zertifikat, das erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="40e5e-109">Use **Add-AzureRmServiceFabricClusterCertificate** to add a secondary cluster certificate, either from an existing Azure key vault or creating a new Azure key vault using an existing certificate provided or from a new self-signed certificate created.</span></span> <span data-ttu-id="40e5e-110">Wenn vorhanden, wird der sekundäre Cluster überschrieben.</span><span class="sxs-lookup"><span data-stu-id="40e5e-110">It will override the secondary cluster if there is any.</span></span>

## <span data-ttu-id="40e5e-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="40e5e-111">EXAMPLES</span></span>

### <span data-ttu-id="40e5e-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="40e5e-112">Example 1</span></span>
```
Add-AzureRmServiceFabricClusterCertificate -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' 
-SecretIdentifier 'https://contoso03vault.vault.azure.net/secrets/contoso03vaultrg/7f7de9131c034172b9df37ccc549524f'
```

<span data-ttu-id="40e5e-113">Mit diesem Befehl wird ein Zertifikat im vorhandenen Azure Key Vault als sekundäres Cluster Zertifikat hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="40e5e-113">This command will add a certificate in the existing Azure key vault as a secondary cluster certificate.</span></span>

### <span data-ttu-id="40e5e-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="40e5e-114">Example 2</span></span>
```
PS c:\> $pwd = ConvertTo-SecureString -String "123" -AsPlainText -Force
PS c:\> add-AzureRmServiceFabricClusterCertificate -ResourceGroupName 'Group2' -Name 'Contoso02SFCluster'  -CertificateSubjectName 'Contoso.com' 
-CertificateOutputFolder 'c:\test' -CertificatePassword $pwd
```

<span data-ttu-id="40e5e-115">Mit diesem Befehl wird im Azure Key Vault ein selbstsigniertes Zertifikat erstellt und der Cluster so aktualisiert, dass es als sekundäres Cluster Zertifikat verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="40e5e-115">This command will create a self-signed certificate in the Azure key vault and upgrade the cluster to use it as a secondary cluster certificate.</span></span>

## <span data-ttu-id="40e5e-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="40e5e-116">PARAMETERS</span></span>

### <span data-ttu-id="40e5e-117">-Certificatedatei</span><span class="sxs-lookup"><span data-stu-id="40e5e-117">-CertificateFile</span></span>
<span data-ttu-id="40e5e-118">Der vorhandene Zertifikat Dateipfad.</span><span class="sxs-lookup"><span data-stu-id="40e5e-118">The existing certificate file path.</span></span>

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

### <span data-ttu-id="40e5e-119">-CertificateOutputFolder</span><span class="sxs-lookup"><span data-stu-id="40e5e-119">-CertificateOutputFolder</span></span>
<span data-ttu-id="40e5e-120">Der Ordner des neuen Zertifikats, das erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="40e5e-120">The folder of the new certificate to be created.</span></span>

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

### <span data-ttu-id="40e5e-121">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="40e5e-121">-CertificatePassword</span></span>
<span data-ttu-id="40e5e-122">Das Kennwort der Zertifikatsdatei.</span><span class="sxs-lookup"><span data-stu-id="40e5e-122">The password of the certificate file.</span></span>

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

### <span data-ttu-id="40e5e-123">-CertificateSubjectName</span><span class="sxs-lookup"><span data-stu-id="40e5e-123">-CertificateSubjectName</span></span>
<span data-ttu-id="40e5e-124">Der DNS-Name des zu erstellenden Zertifikats.</span><span class="sxs-lookup"><span data-stu-id="40e5e-124">The Dns name of the certificate to be created.</span></span>

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

### <span data-ttu-id="40e5e-125">-Keyvaultname</span><span class="sxs-lookup"><span data-stu-id="40e5e-125">-KeyVaultName</span></span>
<span data-ttu-id="40e5e-126">Azure Key Vault-Name.</span><span class="sxs-lookup"><span data-stu-id="40e5e-126">Azure key vault name.</span></span>

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

### <span data-ttu-id="40e5e-127">-KeyVaultResouceGroupName</span><span class="sxs-lookup"><span data-stu-id="40e5e-127">-KeyVaultResouceGroupName</span></span>
<span data-ttu-id="40e5e-128">Azure Key Vault-Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="40e5e-128">Azure key vault resource group name.</span></span>

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

### <span data-ttu-id="40e5e-129">-Name</span><span class="sxs-lookup"><span data-stu-id="40e5e-129">-Name</span></span>
<span data-ttu-id="40e5e-130">Geben Sie den Namen des Clusters an.</span><span class="sxs-lookup"><span data-stu-id="40e5e-130">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="40e5e-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40e5e-131">-ResourceGroupName</span></span>
<span data-ttu-id="40e5e-132">Gibt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="40e5e-132">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="40e5e-133">-SecretIdentifier</span><span class="sxs-lookup"><span data-stu-id="40e5e-133">-SecretIdentifier</span></span>
<span data-ttu-id="40e5e-134">Die vorhandene Azure Key Vault Secret-URL.</span><span class="sxs-lookup"><span data-stu-id="40e5e-134">The existing Azure key vault secret Url.</span></span>

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

### <span data-ttu-id="40e5e-135">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="40e5e-135">-Confirm</span></span>
<span data-ttu-id="40e5e-136">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="40e5e-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="40e5e-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="40e5e-137">-WhatIf</span></span>
<span data-ttu-id="40e5e-138">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="40e5e-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="40e5e-139">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="40e5e-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="40e5e-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40e5e-140">-DefaultProfile</span></span>
<span data-ttu-id="40e5e-141">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="40e5e-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="40e5e-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40e5e-142">CommonParameters</span></span>
<span data-ttu-id="40e5e-143">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="40e5e-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40e5e-144">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="40e5e-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40e5e-145">Eingaben</span><span class="sxs-lookup"><span data-stu-id="40e5e-145">INPUTS</span></span>

### <span data-ttu-id="40e5e-146">System. String</span><span class="sxs-lookup"><span data-stu-id="40e5e-146">System.String</span></span>

## <span data-ttu-id="40e5e-147">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="40e5e-147">OUTPUTS</span></span>

### <span data-ttu-id="40e5e-148">Microsoft. Azure. Commands. ServiceFabric. Models. PsCluster</span><span class="sxs-lookup"><span data-stu-id="40e5e-148">Microsoft.Azure.Commands.ServiceFabric.Models.PsCluster</span></span>

## <span data-ttu-id="40e5e-149">Notizen</span><span class="sxs-lookup"><span data-stu-id="40e5e-149">NOTES</span></span>

## <span data-ttu-id="40e5e-150">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="40e5e-150">RELATED LINKS</span></span>

[<span data-ttu-id="40e5e-151">Remove-AzureRmServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="40e5e-151">Remove-AzureRmServiceFabricClusterCertificate</span></span>](./Remove-AzureRmServiceFabricClusterCertificate.md)

[<span data-ttu-id="40e5e-152">Neu – AzureRmServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="40e5e-152">New-AzureRmServiceFabricCluster</span></span>](./New-AzureRmServiceFabricCluster.md)

[<span data-ttu-id="40e5e-153">Add-AzureRmServiceFabricApplicationCertificate</span><span class="sxs-lookup"><span data-stu-id="40e5e-153">Add-AzureRmServiceFabricApplicationCertificate</span></span>](./Add-AzureRmServiceFabricApplicationCertificate.md)
