---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicefabric/new-azurermservicefabriccluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/New-AzureRmServiceFabricCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/New-AzureRmServiceFabricCluster.md
ms.openlocfilehash: 5da8d1f48a50cafc970278d59b99750f283a9414
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500393"
---
# <span data-ttu-id="fd032-101">New-AzureRmServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="fd032-101">New-AzureRmServiceFabricCluster</span></span>

## <span data-ttu-id="fd032-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="fd032-102">SYNOPSIS</span></span>
<span data-ttu-id="fd032-103">Dieser Befehl verwendet von Ihnen bereitgestellte Zertifikate oder vom System generierte selbstsignierte Zertifikate, um einen neuen Service Fabric-Cluster einzurichten.</span><span class="sxs-lookup"><span data-stu-id="fd032-103">This command uses certificates that you provide or system generated self-signed certificates to set up a new service fabric cluster.</span></span> <span data-ttu-id="fd032-104">Sie kann eine Standardvorlage oder eine von Ihnen bereitgestellte benutzerdefinierte Vorlage verwenden.</span><span class="sxs-lookup"><span data-stu-id="fd032-104">It can use a default template or a custom template that you provide.</span></span> <span data-ttu-id="fd032-105">Sie haben die Möglichkeit, einen Ordner anzugeben, um die selbstsignierten Zertifikate zu exportieren oder später aus dem schlüsseltresor abzurufen.</span><span class="sxs-lookup"><span data-stu-id="fd032-105">You have the option of specifying a folder to export the self-signed certificates to or fetching them later from the key vault.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fd032-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="fd032-106">SYNTAX</span></span>

### <span data-ttu-id="fd032-107">ByDefaultArmTemplate (Standard)</span><span class="sxs-lookup"><span data-stu-id="fd032-107">ByDefaultArmTemplate (Default)</span></span>
```
New-AzureRmServiceFabricCluster [-ResourceGroupName] <String> [-CertificateOutputFolder <String>]
 [-CertificatePassword <SecureString>] [-KeyVaultResouceGroupName <String>] [-KeyVaultName <String>]
 -Location <String> [-Name <String>] [-VmUserName <String>] [-ClusterSize <Int32>]
 [-CertificateSubjectName <String>] -VmPassword <SecureString> [-OS <OperatingSystem>] [-VmSku <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd032-108">ByExistingKeyVault</span><span class="sxs-lookup"><span data-stu-id="fd032-108">ByExistingKeyVault</span></span>
```
New-AzureRmServiceFabricCluster [-ResourceGroupName] <String> -TemplateFile <String> -ParameterFile <String>
 [-VmPassword <SecureString>] -SecretIdentifier <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd032-109">ByNewPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="fd032-109">ByNewPfxAndVaultName</span></span>
```
New-AzureRmServiceFabricCluster [-ResourceGroupName] <String> -TemplateFile <String> -ParameterFile <String>
 [-CertificateOutputFolder <String>] [-CertificatePassword <SecureString>] [-KeyVaultResouceGroupName <String>]
 [-KeyVaultName <String>] [-CertificateSubjectName <String>] [-VmPassword <SecureString>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd032-110">ByExistingPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="fd032-110">ByExistingPfxAndVaultName</span></span>
```
New-AzureRmServiceFabricCluster [-ResourceGroupName] <String> -TemplateFile <String> -ParameterFile <String>
 -CertificateFile <String> [-CertificatePassword <SecureString>] [-SecondaryCertificateFile <String>]
 [-SecondaryCertificatePassword <SecureString>] [-KeyVaultResouceGroupName <String>] [-KeyVaultName <String>]
 [-VmPassword <SecureString>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fd032-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fd032-111">DESCRIPTION</span></span>
<span data-ttu-id="fd032-112">Der Befehl **New-AzureRmServiceFabricCluster** verwendet von Ihnen bereitgestellte Zertifikate oder vom System generierte selbstsignierte Zertifikate, um einen neuen Service Fabric-Cluster einzurichten.</span><span class="sxs-lookup"><span data-stu-id="fd032-112">The **New-AzureRmServiceFabricCluster** command uses certificates that you provide or system generated self-signed certificates to set up a new service fabric cluster.</span></span> <span data-ttu-id="fd032-113">Die verwendete Vorlage kann eine Standardvorlage oder eine von Ihnen bereitgestellte benutzerdefinierte Vorlage sein.</span><span class="sxs-lookup"><span data-stu-id="fd032-113">The template used can be a default template or a custom template that you provide.</span></span> <span data-ttu-id="fd032-114">Sie haben die Möglichkeit, einen Ordner anzugeben, um die selbstsignierten Zertifikate zu exportieren oder später aus dem schlüsseltresor abzurufen.</span><span class="sxs-lookup"><span data-stu-id="fd032-114">You have the option of specifying a folder to export the self-signed certificates or fetching them later from the key vault.</span></span>

<span data-ttu-id="fd032-115">Wenn Sie eine benutzerdefinierte Vorlage und eine Parameterdatei angeben, müssen Sie die Zertifikatinformationen nicht in der Parameterdatei angeben, das System füllt diese Parameter.</span><span class="sxs-lookup"><span data-stu-id="fd032-115">If you are specifying a custom template and parameter file, you don't need to provide the certificate information in the parameter file, the system will populate these parameters.</span></span>

<span data-ttu-id="fd032-116">Die vier Optionen sind im folgenden aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="fd032-116">The four options are detailed below.</span></span> <span data-ttu-id="fd032-117">Scrollen Sie nach unten, um Erläuterungen zu den einzelnen Parametern zu haben.</span><span class="sxs-lookup"><span data-stu-id="fd032-117">Scroll down for explanations of each of the parameters.</span></span>

## <span data-ttu-id="fd032-118">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fd032-118">EXAMPLES</span></span>

### <span data-ttu-id="fd032-119">Beispiel 1: Geben Sie nur die Clustergröße, den Zertifikatantragstellernamen und das Betriebssystem für die Bereitstellungeines Clusters an.</span><span class="sxs-lookup"><span data-stu-id="fd032-119">Example 1: Specify only the cluster size, the cert subject name, and the OS to deploy a cluster.</span></span>
```
$pass="Password#1234" | ConvertTo-SecureString -AsPlainText -Force
$RGname="test01"
$clusterloc="SouthCentralUS"
$subname="{0}.{1}.cloudapp.azure.com" -f $RGname, $clusterloc
$pfxfolder="~\Documents"

Write-Output "Create cluster in '$clusterloc' with cert subject name '$subname' and cert output path '$pfxfolder'"

New-AzureRmServiceFabricCluster -ResourceGroupName $RGname -Location $clusterloc -ClusterSize 3 -VmPassword $pass -CertificateSubjectName $subname -CertificateOutputFolder $pfxfolder -CertificatePassword $pass -OS WindowsServer2016Datacenter
```

<span data-ttu-id="fd032-120">Dieser Befehl gibt nur die Clustergröße, den Zertifikatantragstellernamen und das Betriebssystem für die Bereitstellungeines Clusters an.</span><span class="sxs-lookup"><span data-stu-id="fd032-120">This command specifies only the cluster size, the cert subject name, and the OS to deploy a cluster.</span></span>

### <span data-ttu-id="fd032-121">Beispiel 2: Angeben einer vorhandenen Zertifikat Ressource in einem schlüsseltresor und einer benutzerdefinierten Vorlage zum Bereitstellen eines Clusters</span><span class="sxs-lookup"><span data-stu-id="fd032-121">Example 2: Specify an existing Certificate resource in a key vault and a custom template to deploy a cluster</span></span>
```
$RGname="test20"
$templateParmfile="C:\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploytest.parameters.json"
$templateFile="C:\azure-quickstart-templates\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploy.json"
$secretId="https://test1.vault.azure.net:443/secrets/testcertificate4/56ec774dc61a462bbc645ffc9b4b225f"

New-AzureRmServiceFabricCluster -ResourceGroupName $RGname -TemplateFile $templateFile -ParameterFile $templateParmfile -SecretIdentifier $secretId
```

<span data-ttu-id="fd032-122">Mit diesem Befehl wird eine vorhandene Zertifikat Ressource in einem schlüsseltresor und eine benutzerdefinierte Vorlage zum Bereitstellen eines Clusters angegeben.</span><span class="sxs-lookup"><span data-stu-id="fd032-122">This command specifies an existing Certificate resource in a key vault and a custom template to deploy a cluster.</span></span>

### <span data-ttu-id="fd032-123">Beispiel 3: Erstellen eines neuen Clusters mit einer benutzerdefinierten Vorlage</span><span class="sxs-lookup"><span data-stu-id="fd032-123">Example 3: Create a new cluster using a custom template.</span></span> <span data-ttu-id="fd032-124">Geben Sie einen anderen Ressourcengruppennamen für den schlüsseltresor an, und lassen Sie das System ein neues Zertifikat hochladen.</span><span class="sxs-lookup"><span data-stu-id="fd032-124">Specify a different resource group name for the key vault and have the system upload a new certificate to it</span></span>
```
$pass="Password#1234" | ConvertTo-SecureString -AsPlainText -Force
$RGname="test20"
$keyVaultRG="test20kvrg"
$keyVault="test20kv"
$clusterloc="SouthCentralUS"
$subname="{0}.{1}.$clusterloc.cloudapp.azure.com" -f $RGName, $clusterloc
$pfxfolder="~\Documents"
$templateParmfile="C:\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploytest.parameters.json"
$templateFile="C:\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploy.json"

New-AzureRmServiceFabricCluster -ResourceGroupName $RGname -TemplateFile $templateFile -ParameterFile $templateParmfile -CertificateOutputFolder $pfxfolder -CertificatePassword $pass -KeyVaultResouceGroupName $keyVaultRG  -KeyVaultName $keyVault -CertificateSubjectName $subname
```

<span data-ttu-id="fd032-125">Dieser Befehl erstellt einen neuen Cluster unter Verwendung einer benutzerdefinierten Vorlage.</span><span class="sxs-lookup"><span data-stu-id="fd032-125">This command creates a new cluster using a custom template.</span></span> <span data-ttu-id="fd032-126">Geben Sie einen anderen Ressourcengruppennamen für den schlüsseltresor an, und lassen Sie das System ein neues Zertifikat hochladen.</span><span class="sxs-lookup"><span data-stu-id="fd032-126">Specify a different resource group name for the key vault and have the system upload a new certificate to it</span></span>

### <span data-ttu-id="fd032-127">Beispiel 4: Erstellen eines eigenen Zertifikats und einer benutzerdefinierten Vorlage und Erstellen eines neuen Clusters</span><span class="sxs-lookup"><span data-stu-id="fd032-127">Example 4: Bring your own Certificate and custom template and create a new cluster</span></span>
```
$pass="Password#1234" | ConvertTo-SecureString -AsPlainText -Force
$RGname="test20"
$keyVaultRG="test20kvrg"
$keyVault="test20kv"
$pfxsourcefile="c:\Mycertificates\my2017Prodcert.pfx"
$templateParmfile="~\Documents\GitHub\azure-quickstart-templates-parms\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploytest.parameters.json"
$templateFile="~\GitHub\azure-quickstart-templates\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploy.json"

New-AzureRmServiceFabricCluster -ResourceGroupName $RGname -TemplateFile $templateFile -ParameterFile $templateParmfile -CertificateFile $pfxsourcefile -CertificatePassword $pass -KeyVaultResouceGroupName $keyVaultRG -KeyVaultName $keyVault
```

<span data-ttu-id="fd032-128">Mit diesem Befehl können Sie ein eigenes Zertifikat und eine benutzerdefinierte Vorlage erstellen und einen neuen Cluster erstellen.</span><span class="sxs-lookup"><span data-stu-id="fd032-128">This command will let you bring your own Certificate and custom template and create a new cluster.</span></span>

## <span data-ttu-id="fd032-129">Parameter</span><span class="sxs-lookup"><span data-stu-id="fd032-129">PARAMETERS</span></span>

### <span data-ttu-id="fd032-130">-Certificatedatei</span><span class="sxs-lookup"><span data-stu-id="fd032-130">-CertificateFile</span></span>
<span data-ttu-id="fd032-131">Der vorhandene Zertifikats Dateipfad für das primäre Cluster Zertifikat.</span><span class="sxs-lookup"><span data-stu-id="fd032-131">The existing certificate file path for the primary cluster certificate.</span></span>

```yaml
Type: String
Parameter Sets: ByExistingPfxAndVaultName
Aliases: Source

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fd032-132">-CertificateOutputFolder</span><span class="sxs-lookup"><span data-stu-id="fd032-132">-CertificateOutputFolder</span></span>
<span data-ttu-id="fd032-133">Der Ordner der neuen Zertifikatsdatei, die erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="fd032-133">The folder of the new certificate file to be created.</span></span>

```yaml
Type: String
Parameter Sets: ByDefaultArmTemplate, ByNewPfxAndVaultName
Aliases: Destination

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fd032-134">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="fd032-134">-CertificatePassword</span></span>
<span data-ttu-id="fd032-135">Das Kennwort der Zertifikatsdatei.</span><span class="sxs-lookup"><span data-stu-id="fd032-135">The password of the certificate file.</span></span>

```yaml
Type: SecureString
Parameter Sets: ByDefaultArmTemplate, ByNewPfxAndVaultName, ByExistingPfxAndVaultName
Aliases: CertPassword

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fd032-136">-CertificateSubjectName</span><span class="sxs-lookup"><span data-stu-id="fd032-136">-CertificateSubjectName</span></span>
<span data-ttu-id="fd032-137">Der Name des Antragstellers des zu erstellenden Zertifikats.</span><span class="sxs-lookup"><span data-stu-id="fd032-137">The subject name of the certificate to be created.</span></span>

```yaml
Type: String
Parameter Sets: ByDefaultArmTemplate, ByNewPfxAndVaultName
Aliases: Subject

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fd032-138">-Clusterisieren</span><span class="sxs-lookup"><span data-stu-id="fd032-138">-ClusterSize</span></span>
<span data-ttu-id="fd032-139">Die Anzahl der Knoten im Cluster.</span><span class="sxs-lookup"><span data-stu-id="fd032-139">The number of nodes in the cluster.</span></span> <span data-ttu-id="fd032-140">Standard sind fünf Knoten.</span><span class="sxs-lookup"><span data-stu-id="fd032-140">Default are 5 nodes.</span></span>

```yaml
Type: Int32
Parameter Sets: ByDefaultArmTemplate
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fd032-141">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd032-141">-DefaultProfile</span></span>
<span data-ttu-id="fd032-142">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="fd032-142">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd032-143">-Keyvaultname</span><span class="sxs-lookup"><span data-stu-id="fd032-143">-KeyVaultName</span></span>
<span data-ttu-id="fd032-144">Azure Key Vault-Name.</span><span class="sxs-lookup"><span data-stu-id="fd032-144">Azure key vault name.</span></span> <span data-ttu-id="fd032-145">Wenn nicht angegeben, wird der Name der Ressourcengruppe standardmäßig verwendet.</span><span class="sxs-lookup"><span data-stu-id="fd032-145">If not given, it will be defaulted to the resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByDefaultArmTemplate, ByNewPfxAndVaultName, ByExistingPfxAndVaultName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fd032-146">-KeyVaultResouceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd032-146">-KeyVaultResouceGroupName</span></span>
<span data-ttu-id="fd032-147">Azure Key Vault-Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="fd032-147">Azure key vault resource group name.</span></span> <span data-ttu-id="fd032-148">Wenn nicht angegeben, wird der Name der Ressourcengruppe standardmäßig verwendet.</span><span class="sxs-lookup"><span data-stu-id="fd032-148">If not given, it will be defaulted to resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByDefaultArmTemplate, ByNewPfxAndVaultName, ByExistingPfxAndVaultName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fd032-149">-Standort</span><span class="sxs-lookup"><span data-stu-id="fd032-149">-Location</span></span>
<span data-ttu-id="fd032-150">Der Speicherort der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="fd032-150">The resource group location.</span></span>

```yaml
Type: String
Parameter Sets: ByDefaultArmTemplate
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fd032-151">-Name</span><span class="sxs-lookup"><span data-stu-id="fd032-151">-Name</span></span>
<span data-ttu-id="fd032-152">Geben Sie den Namen des Clusters an.</span><span class="sxs-lookup"><span data-stu-id="fd032-152">Specify the name of the cluster.</span></span> <span data-ttu-id="fd032-153">Wenn Sie nicht angegeben wird, ist Sie mit dem Namen der Ressourcengruppe identisch.</span><span class="sxs-lookup"><span data-stu-id="fd032-153">If not given, it will be same as resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByDefaultArmTemplate
Aliases: ClusterName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fd032-154">-OS</span><span class="sxs-lookup"><span data-stu-id="fd032-154">-OS</span></span>
<span data-ttu-id="fd032-155">Das Betriebs System der VMS, aus denen sich der Cluster zusammensetzen soll</span><span class="sxs-lookup"><span data-stu-id="fd032-155">The Operating System of the VMs that make up the cluster.</span></span>

```yaml
Type: OperatingSystem
Parameter Sets: ByDefaultArmTemplate
Aliases: VmImage
Accepted values: WindowsServer2012R2Datacenter, WindowsServer2016Datacenter, WindowsServer2016DatacenterwithContainers, UbuntuServer1604

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd032-156">-Parameterdatei</span><span class="sxs-lookup"><span data-stu-id="fd032-156">-ParameterFile</span></span>
<span data-ttu-id="fd032-157">Der Pfad zur Vorlagenparameter Datei.</span><span class="sxs-lookup"><span data-stu-id="fd032-157">The path to the template parameter file.</span></span>

```yaml
Type: String
Parameter Sets: ByExistingKeyVault, ByNewPfxAndVaultName, ByExistingPfxAndVaultName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fd032-158">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd032-158">-ResourceGroupName</span></span>
<span data-ttu-id="fd032-159">Geben Sie den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="fd032-159">Specify the name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd032-160">-SecondaryCertificateFile</span><span class="sxs-lookup"><span data-stu-id="fd032-160">-SecondaryCertificateFile</span></span>
<span data-ttu-id="fd032-161">Der vorhandene Zertifikats Dateipfad für das sekundäre Cluster Zertifikat.</span><span class="sxs-lookup"><span data-stu-id="fd032-161">The existing certificate file path for the secondary cluster certificate.</span></span>

```yaml
Type: String
Parameter Sets: ByExistingPfxAndVaultName
Aliases: SecSource

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fd032-162">-SecondaryCertificatePassword</span><span class="sxs-lookup"><span data-stu-id="fd032-162">-SecondaryCertificatePassword</span></span>
<span data-ttu-id="fd032-163">Das Kennwort der Zertifikatsdatei.</span><span class="sxs-lookup"><span data-stu-id="fd032-163">The password of the certificate file.</span></span>

```yaml
Type: SecureString
Parameter Sets: ByExistingPfxAndVaultName
Aliases: SecCertPassword

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fd032-164">-SecretIdentifier</span><span class="sxs-lookup"><span data-stu-id="fd032-164">-SecretIdentifier</span></span>
<span data-ttu-id="fd032-165">Die vorhandene Azure Key Vault Secret-URL, beispielsweise: " https://mykv.vault.azure.net:443/secrets/mysecrets/55ec7c4dc61a462bbc645ffc9b4b225f '.</span><span class="sxs-lookup"><span data-stu-id="fd032-165">The existing Azure key vault secret URL, for example: 'https://mykv.vault.azure.net:443/secrets/mysecrets/55ec7c4dc61a462bbc645ffc9b4b225f'.</span></span>

```yaml
Type: String
Parameter Sets: ByExistingKeyVault
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fd032-166">-Vorlagendatei</span><span class="sxs-lookup"><span data-stu-id="fd032-166">-TemplateFile</span></span>
<span data-ttu-id="fd032-167">Der Pfad zur Vorlagendatei.</span><span class="sxs-lookup"><span data-stu-id="fd032-167">The path to the template file.</span></span>

```yaml
Type: String
Parameter Sets: ByExistingKeyVault, ByNewPfxAndVaultName, ByExistingPfxAndVaultName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fd032-168">-VmPassword</span><span class="sxs-lookup"><span data-stu-id="fd032-168">-VmPassword</span></span>
<span data-ttu-id="fd032-169">Das Kennwort des VM.</span><span class="sxs-lookup"><span data-stu-id="fd032-169">The password of the Vm.</span></span>

```yaml
Type: SecureString
Parameter Sets: ByDefaultArmTemplate
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: SecureString
Parameter Sets: ByExistingKeyVault, ByNewPfxAndVaultName, ByExistingPfxAndVaultName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd032-170">-VmSku</span><span class="sxs-lookup"><span data-stu-id="fd032-170">-VmSku</span></span>
<span data-ttu-id="fd032-171">Die VM-SKU.</span><span class="sxs-lookup"><span data-stu-id="fd032-171">The Vm Sku.</span></span>

```yaml
Type: String
Parameter Sets: ByDefaultArmTemplate
Aliases: Sku

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd032-172">-VmUserName</span><span class="sxs-lookup"><span data-stu-id="fd032-172">-VmUserName</span></span>
<span data-ttu-id="fd032-173">Der Benutzername für die Anmeldung bei VM.</span><span class="sxs-lookup"><span data-stu-id="fd032-173">The user name for logging to Vm.</span></span>

```yaml
Type: String
Parameter Sets: ByDefaultArmTemplate
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fd032-174">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="fd032-174">-Confirm</span></span>
<span data-ttu-id="fd032-175">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="fd032-175">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd032-176">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fd032-176">-WhatIf</span></span>
<span data-ttu-id="fd032-177">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fd032-177">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fd032-178">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="fd032-178">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd032-179">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd032-179">CommonParameters</span></span>
<span data-ttu-id="fd032-180">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd032-180">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd032-181">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fd032-181">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd032-182">Eingaben</span><span class="sxs-lookup"><span data-stu-id="fd032-182">INPUTS</span></span>

### <span data-ttu-id="fd032-183">System. String</span><span class="sxs-lookup"><span data-stu-id="fd032-183">System.String</span></span>
<span data-ttu-id="fd032-184">System. Security. SecureString System. Int32 Microsoft. Azure. Commands. ServiceFabric. Models. OperatingSystem</span><span class="sxs-lookup"><span data-stu-id="fd032-184">System.Security.SecureString System.Int32 Microsoft.Azure.Commands.ServiceFabric.Models.OperatingSystem</span></span>

## <span data-ttu-id="fd032-185">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="fd032-185">OUTPUTS</span></span>

### <span data-ttu-id="fd032-186">Microsoft.Azure.Commands.ServiceFabric.Models.PSDeploymentResult</span><span class="sxs-lookup"><span data-stu-id="fd032-186">Microsoft.Azure.Commands.ServiceFabric.Models.PSDeploymentResult</span></span>

## <span data-ttu-id="fd032-187">Notizen</span><span class="sxs-lookup"><span data-stu-id="fd032-187">NOTES</span></span>

## <span data-ttu-id="fd032-188">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="fd032-188">RELATED LINKS</span></span>

