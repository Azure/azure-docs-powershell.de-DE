---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/new-azservicefabriccluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricCluster.md
ms.openlocfilehash: b603087063a763d63f986afa7568160a6623a22b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101920923"
---
# <span data-ttu-id="d564a-101">New-AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="d564a-101">New-AzServiceFabricCluster</span></span>

## <span data-ttu-id="d564a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d564a-102">SYNOPSIS</span></span>

<span data-ttu-id="d564a-103">Dieser Befehl verwendet Zertifikate, die Sie bereitstellen, oder systemgenerierte selbst signierte Zertifikate, um einen neuen Service Fabric-Cluster zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="d564a-103">This command uses certificates that you provide or system generated self-signed certificates to set up a new service fabric cluster.</span></span> <span data-ttu-id="d564a-104">Sie kann eine Standardvorlage oder eine benutzerdefinierte Vorlage verwenden, die Sie bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="d564a-104">It can use a default template or a custom template that you provide.</span></span> <span data-ttu-id="d564a-105">Sie haben die Möglichkeit, einen Ordner anzugeben, in den die selbst signierten Zertifikate exportiert oder später aus dem Schlüsseltresor abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="d564a-105">You have the option of specifying a folder to export the self-signed certificates to or fetching them later from the key vault.</span></span>

## <span data-ttu-id="d564a-106">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d564a-106">SYNTAX</span></span>

### <span data-ttu-id="d564a-107">ByDefaultArmTemplate (Standard)</span><span class="sxs-lookup"><span data-stu-id="d564a-107">ByDefaultArmTemplate (Default)</span></span>
```
New-AzServiceFabricCluster [-ResourceGroupName] <String> [-CertificateOutputFolder <String>]
 [-CertificatePassword <SecureString>] [-KeyVaultResourceGroupName <String>] [-KeyVaultName <String>]
 -Location <String> [-Name <String>] [-VmUserName <String>] [-ClusterSize <Int32>]
 [-CertificateSubjectName <String>] -VmPassword <SecureString> [-OS <OperatingSystem>] [-VmSku <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d564a-108">ByExistingKeyVault</span><span class="sxs-lookup"><span data-stu-id="d564a-108">ByExistingKeyVault</span></span>
```
New-AzServiceFabricCluster [-ResourceGroupName] <String> -TemplateFile <String> -ParameterFile <String>
 [-CertificateCommonName <String>] [-CertificateIssuerThumbprint <String>] [-VmPassword <SecureString>]
 -SecretIdentifier <String> [-Thumbprint <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d564a-109">ByNewPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="d564a-109">ByNewPfxAndVaultName</span></span>
```
New-AzServiceFabricCluster [-ResourceGroupName] <String> -TemplateFile <String> -ParameterFile <String>
 [-CertificateOutputFolder <String>] [-CertificatePassword <SecureString>]
 [-KeyVaultResourceGroupName <String>] [-KeyVaultName <String>] [-CertificateSubjectName <String>]
 [-VmPassword <SecureString>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d564a-110">ByExistingPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="d564a-110">ByExistingPfxAndVaultName</span></span>
```
New-AzServiceFabricCluster [-ResourceGroupName] <String> -TemplateFile <String> -ParameterFile <String>
 -CertificateFile <String> [-CertificatePassword <SecureString>] [-SecondaryCertificateFile <String>]
 [-SecondaryCertificatePassword <SecureString>] [-KeyVaultResourceGroupName <String>] [-KeyVaultName <String>]
 [-CertificateCommonName <String>] [-CertificateIssuerThumbprint <String>] [-VmPassword <SecureString>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d564a-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d564a-111">DESCRIPTION</span></span>

<span data-ttu-id="d564a-112">Der **Befehl New-AzServiceFabricCluster** verwendet Zertifikate, die Sie bereitstellen, oder systemgenerierte selbst signierte Zertifikate, um einen neuen Service Fabric-Cluster zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="d564a-112">The **New-AzServiceFabricCluster** command uses certificates that you provide or system generated self-signed certificates to set up a new service fabric cluster.</span></span> <span data-ttu-id="d564a-113">Die verwendete Vorlage kann eine Standardvorlage oder eine benutzerdefinierte Vorlage sein, die Sie bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="d564a-113">The template used can be a default template or a custom template that you provide.</span></span> <span data-ttu-id="d564a-114">Sie haben die Möglichkeit, einen Ordner anzugeben, um die selbst signierten Zertifikate zu exportieren oder sie später aus dem Schlüsseltresor abgeholt zu haben.</span><span class="sxs-lookup"><span data-stu-id="d564a-114">You have the option of specifying a folder to export the self-signed certificates or fetching them later from the key vault.</span></span>
<span data-ttu-id="d564a-115">Wenn Sie eine benutzerdefinierte Vorlage und Parameterdatei angeben, müssen Sie die Zertifikatinformationen in der Parameterdatei nicht angeben, das System füllt diese Parameter auf.</span><span class="sxs-lookup"><span data-stu-id="d564a-115">If you are specifying a custom template and parameter file, you don't need to provide the certificate information in the parameter file, the system will populate these parameters.</span></span>
<span data-ttu-id="d564a-116">Die vier Optionen sind unten beschrieben.</span><span class="sxs-lookup"><span data-stu-id="d564a-116">The four options are detailed below.</span></span> <span data-ttu-id="d564a-117">Scrollen Sie nach unten, um Erläuterungen zu den einzelnen Parametern zu finden.</span><span class="sxs-lookup"><span data-stu-id="d564a-117">Scroll down for explanations of each of the parameters.</span></span>

## <span data-ttu-id="d564a-118">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d564a-118">EXAMPLES</span></span>

### <span data-ttu-id="d564a-119">Beispiel 1: Geben Sie nur die Clustergröße, den Namen des #A0 und das Betriebssystem an, um einen Cluster bereitstellen zu können.</span><span class="sxs-lookup"><span data-stu-id="d564a-119">Example 1: Specify only the cluster size, the cert subject name, and the OS to deploy a cluster</span></span>

```powershell
$password = "Password#1234" | ConvertTo-SecureString -AsPlainText -Force
$resourceGroupName = "quickstart-sf-group"
$azureRegion = "southcentralus"
$clusterDnsName = "{0}.{1}.cloudapp.azure.com" -f $resourceGroupName, $azureRegion
$localCertificateFolder = "c:\certs"

Write-Output "Create cluster in '$azureRegion' with cert subject name '$clusterDnsName' and cert output path '$localCertificateFolder'"

New-AzServiceFabricCluster -ResourceGroupName $resourceGroupName -Location $azureRegion -ClusterSize 5 -VmPassword $password -CertificateSubjectName $clusterDnsName -CertificateOutputFolder $localCertificateFolder -CertificatePassword $pass -OS WindowsServer2016Datacenter
```

<span data-ttu-id="d564a-120">Dieser Befehl gibt nur die Clustergröße, den Namen des #A0 und das Betriebssystem an, um einen Cluster bereitstellen zu können.</span><span class="sxs-lookup"><span data-stu-id="d564a-120">This command specifies only the cluster size, the cert subject name, and the OS to deploy a cluster.</span></span>

### <span data-ttu-id="d564a-121">Beispiel 2: Angeben einer vorhandenen Zertifikatressource in einem Schlüsseltresor und einer benutzerdefinierten Vorlage zum Bereitstellen eines Clusters</span><span class="sxs-lookup"><span data-stu-id="d564a-121">Example 2: Specify an existing Certificate resource in a key vault and a custom template to deploy a cluster</span></span>

```powershell
$resourceGroupName = "test20"
$templateParameterFile = "C:\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploytest.parameters.json"
$templateFile = "C:\azure-quickstart-templates\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploy.json"
$secretId = "https://test1.vault.azure.net:443/secrets/testcertificate4/56ec774dc61a462bbc645ffc9b4b225f"

New-AzServiceFabricCluster -ResourceGroupName $resourceGroupName -TemplateFile $templateFile -ParameterFile $templateParameterFile -SecretIdentifier $secretId
```

<span data-ttu-id="d564a-122">Dieser Befehl gibt eine vorhandene Zertifikatressource in einem Schlüsseltresor und eine benutzerdefinierte Vorlage zum Bereitstellen eines Clusters an.</span><span class="sxs-lookup"><span data-stu-id="d564a-122">This command specifies an existing Certificate resource in a key vault and a custom template to deploy a cluster.</span></span>

### <span data-ttu-id="d564a-123">Beispiel 3: Erstellen sie einen neuen Cluster mit einer benutzerdefinierten Vorlage.</span><span class="sxs-lookup"><span data-stu-id="d564a-123">Example 3: Create a new cluster using a custom template.</span></span> <span data-ttu-id="d564a-124">Angeben eines anderen Ressourcengruppennamens für den Schlüsseltresor und Hochladen eines neuen Zertifikats durch das System</span><span class="sxs-lookup"><span data-stu-id="d564a-124">Specify a different resource group name for the key vault and have the system upload a new certificate to it</span></span>

```powershell
$password = "Password#1234" | ConvertTo-SecureString -AsPlainText -Force
$resourceGroupName = "quickstart-sf-group"
$keyVaultResourceGroupName = " quickstart-kv-group"
$keyVaultName = "quickstart-kv"
$azureRegion = "southcentralus"
$clusterDnsName = "{0}.{1}.cloudapp.azure.com" -F $resourceGroupName, $azureRegion
$localCertificateFolder = "~\Documents"
$templateParameterFile = "C:\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploytest.parameters.json"
$templateFile = "C:\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploy.json"

New-AzServiceFabricCluster -ResourceGroupName $resourceGroupName -TemplateFile $templateFile -ParameterFile $templateParameterFile -CertificateOutputFolder $localCertificateFolder -CertificatePassword $password -KeyVaultResourceGroupName $keyVaultResourceGroupName  -KeyVaultName $keyVaultName -CertificateSubjectName $clusterDnsName
```

<span data-ttu-id="d564a-125">Mit diesem Befehl wird ein neuer Cluster mithilfe einer benutzerdefinierten Vorlage erstellt.</span><span class="sxs-lookup"><span data-stu-id="d564a-125">This command creates a new cluster using a custom template.</span></span> <span data-ttu-id="d564a-126">Angeben eines anderen Ressourcengruppennamens für den Schlüsseltresor und Hochladen eines neuen Zertifikats durch das System</span><span class="sxs-lookup"><span data-stu-id="d564a-126">Specify a different resource group name for the key vault and have the system upload a new certificate to it</span></span>

### <span data-ttu-id="d564a-127">Beispiel 4: Bringen Sie Ihr eigenes Zertifikat und eine benutzerdefinierte Vorlage mit, und erstellen Sie einen neuen Cluster.</span><span class="sxs-lookup"><span data-stu-id="d564a-127">Example 4: Bring your own Certificate and custom template and create a new cluster</span></span>

```powershell
$password = "Password#1234" | ConvertTo-SecureString -AsPlainText -Force
$resourceGroupName = "test20"
$keyVaultResourceGroupName = "test20kvrg"
$keyVaultName = "test20kv"
$localCertificateFile = "c:\Mycertificates\my2017Prodcert.pfx"
$templateParameterFile = "~\Documents\GitHub\azure-quickstart-templates-parms\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploytest.parameters.json"
$templateFile = "~\GitHub\azure-quickstart-templates\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploy.json"

New-AzServiceFabricCluster -ResourceGroupName $resourceGroupName -TemplateFile $templateFile -ParameterFile $templateParameterFile -CertificateFile $localCertificateFile -CertificatePassword $password -KeyVaultResourceGroupName $keyVaultResourceGroupName -KeyVaultName $keyVaultName
```

<span data-ttu-id="d564a-128">Mit diesem Befehl können Sie Ihr eigenes Zertifikat und eine benutzerdefinierte Vorlage mitbringen und einen neuen Cluster erstellen.</span><span class="sxs-lookup"><span data-stu-id="d564a-128">This command will let you bring your own Certificate and custom template and create a new cluster.</span></span>

## <span data-ttu-id="d564a-129">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="d564a-129">PARAMETERS</span></span>

### <span data-ttu-id="d564a-130">-CertificateCommonName</span><span class="sxs-lookup"><span data-stu-id="d564a-130">-CertificateCommonName</span></span>

<span data-ttu-id="d564a-131">Häufiger Name des Zertifikats</span><span class="sxs-lookup"><span data-stu-id="d564a-131">Certificate common name</span></span>

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

### <span data-ttu-id="d564a-132">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="d564a-132">-CertificateFile</span></span>

<span data-ttu-id="d564a-133">Der vorhandene Zertifikatdateipfad für das primäre Clusterzertifikat</span><span class="sxs-lookup"><span data-stu-id="d564a-133">The existing certificate file path for the primary cluster certificate</span></span>

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

### <span data-ttu-id="d564a-134">-CertificateIssuerThumbprint</span><span class="sxs-lookup"><span data-stu-id="d564a-134">-CertificateIssuerThumbprint</span></span>

<span data-ttu-id="d564a-135">Fingerabdruck des Zertifikatausstellers, getrennt durch Kommas, wenn mehr als eins</span><span class="sxs-lookup"><span data-stu-id="d564a-135">Certificate issuer thumbprint, separated by commas if more than one</span></span>

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

### <span data-ttu-id="d564a-136">-CertificateOutputFolder</span><span class="sxs-lookup"><span data-stu-id="d564a-136">-CertificateOutputFolder</span></span>

<span data-ttu-id="d564a-137">Der Ordner der neuen zertifikatdatei, die erstellt werden soll</span><span class="sxs-lookup"><span data-stu-id="d564a-137">The folder of the new certificate file to be created</span></span>

```yaml
Type: System.String
Parameter Sets: ByDefaultArmTemplate, ByNewPfxAndVaultName
Aliases: Destination

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d564a-138">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="d564a-138">-CertificatePassword</span></span>

<span data-ttu-id="d564a-139">Das Kennwort der Zertifikatdatei</span><span class="sxs-lookup"><span data-stu-id="d564a-139">The password of the certificate file</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: ByDefaultArmTemplate, ByNewPfxAndVaultName, ByExistingPfxAndVaultName
Aliases: CertPassword

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d564a-140">-CertificateSubjectName</span><span class="sxs-lookup"><span data-stu-id="d564a-140">-CertificateSubjectName</span></span>

<span data-ttu-id="d564a-141">Der Betreffname des zu erstellende Zertifikats</span><span class="sxs-lookup"><span data-stu-id="d564a-141">The subject name of the certificate to be created</span></span>

```yaml
Type: System.String
Parameter Sets: ByDefaultArmTemplate, ByNewPfxAndVaultName
Aliases: Subject

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d564a-142">-ClusterGröße</span><span class="sxs-lookup"><span data-stu-id="d564a-142">-ClusterSize</span></span>

<span data-ttu-id="d564a-143">Die Anzahl der Knoten im Cluster.</span><span class="sxs-lookup"><span data-stu-id="d564a-143">The number of nodes in the cluster.</span></span>
<span data-ttu-id="d564a-144">Standardmäßig sind 5 Knoten</span><span class="sxs-lookup"><span data-stu-id="d564a-144">Default are 5 nodes</span></span>

```yaml
Type: System.Int32
Parameter Sets: ByDefaultArmTemplate
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d564a-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d564a-145">-DefaultProfile</span></span>

<span data-ttu-id="d564a-146">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d564a-146">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d564a-147">-KeyVaultName</span><span class="sxs-lookup"><span data-stu-id="d564a-147">-KeyVaultName</span></span>

<span data-ttu-id="d564a-148">Azure Key Vault name, if not given it will be default to the resource group name</span><span class="sxs-lookup"><span data-stu-id="d564a-148">Azure key vault name, if not given it will be defaulted to the resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: ByDefaultArmTemplate, ByNewPfxAndVaultName, ByExistingPfxAndVaultName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d564a-149">-KeyVaultResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d564a-149">-KeyVaultResourceGroupName</span></span>

<span data-ttu-id="d564a-150">Der Name der Azure Key Vault-Ressourcengruppe, sofern nicht angegeben, wird standardmäßig als Ressourcengruppenname verwendet.</span><span class="sxs-lookup"><span data-stu-id="d564a-150">Azure key vault resource group name, if not given it will be defaulted to resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: ByDefaultArmTemplate, ByNewPfxAndVaultName, ByExistingPfxAndVaultName
Aliases: KeyVaultResouceGroupName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d564a-151">-Location</span><span class="sxs-lookup"><span data-stu-id="d564a-151">-Location</span></span>

<span data-ttu-id="d564a-152">Der Ressourcengruppenspeicherort</span><span class="sxs-lookup"><span data-stu-id="d564a-152">The resource group location</span></span>

```yaml
Type: System.String
Parameter Sets: ByDefaultArmTemplate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d564a-153">-Name</span><span class="sxs-lookup"><span data-stu-id="d564a-153">-Name</span></span>

<span data-ttu-id="d564a-154">Geben Sie den Namen des Clusters an, wenn er nicht angegeben wird, ist er mit dem Namen der Ressourcengruppe identisch.</span><span class="sxs-lookup"><span data-stu-id="d564a-154">Specify the name of the cluster, if not given it will be same as resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: ByDefaultArmTemplate
Aliases: ClusterName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d564a-155">-OS</span><span class="sxs-lookup"><span data-stu-id="d564a-155">-OS</span></span>

<span data-ttu-id="d564a-156">Das Betriebssystem der VMs, die den Cluster bilden.</span><span class="sxs-lookup"><span data-stu-id="d564a-156">The Operating System of the VMs that make up the cluster.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.OperatingSystem
Parameter Sets: ByDefaultArmTemplate
Aliases: VmImage
Accepted values: WindowsServer2012R2Datacenter, WindowsServer2016Datacenter, WindowsServer2016DatacenterwithContainers, UbuntuServer1604

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d564a-157">-ParameterFile</span><span class="sxs-lookup"><span data-stu-id="d564a-157">-ParameterFile</span></span>

<span data-ttu-id="d564a-158">Der Pfad zur Vorlagenparameterdatei.</span><span class="sxs-lookup"><span data-stu-id="d564a-158">The path to the template parameter file.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExistingKeyVault, ByNewPfxAndVaultName, ByExistingPfxAndVaultName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d564a-159">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d564a-159">-ResourceGroupName</span></span>

<span data-ttu-id="d564a-160">Geben Sie den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="d564a-160">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="d564a-161">-SecondaryCertificateFile</span><span class="sxs-lookup"><span data-stu-id="d564a-161">-SecondaryCertificateFile</span></span>

<span data-ttu-id="d564a-162">Der vorhandene Zertifikatdateipfad für das sekundäre Clusterzertifikat</span><span class="sxs-lookup"><span data-stu-id="d564a-162">The existing certificate file path for the secondary cluster certificate</span></span>

```yaml
Type: System.String
Parameter Sets: ByExistingPfxAndVaultName
Aliases: SecSource

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d564a-163">-SecondaryCertificatePassword</span><span class="sxs-lookup"><span data-stu-id="d564a-163">-SecondaryCertificatePassword</span></span>

<span data-ttu-id="d564a-164">Das Kennwort der Zertifikatdatei</span><span class="sxs-lookup"><span data-stu-id="d564a-164">The password of the certificate file</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: ByExistingPfxAndVaultName
Aliases: SecCertPassword

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d564a-165">-SecretIdentifier</span><span class="sxs-lookup"><span data-stu-id="d564a-165">-SecretIdentifier</span></span>

<span data-ttu-id="d564a-166">Die vorhandene geheime Azure-Schlüsseltresor-URL, z. B. https://mykv.vault.azure.net:443/secrets/mysecrets/55ec7c4dc61a462bbc645ffc9b4b225f ' '</span><span class="sxs-lookup"><span data-stu-id="d564a-166">The existing Azure key vault secret URL, for example 'https://mykv.vault.azure.net:443/secrets/mysecrets/55ec7c4dc61a462bbc645ffc9b4b225f'</span></span>

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

### <span data-ttu-id="d564a-167">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="d564a-167">-TemplateFile</span></span>

<span data-ttu-id="d564a-168">Der Pfad zur Vorlagendatei.</span><span class="sxs-lookup"><span data-stu-id="d564a-168">The path to the template file.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExistingKeyVault, ByNewPfxAndVaultName, ByExistingPfxAndVaultName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d564a-169">-Thumbprint</span><span class="sxs-lookup"><span data-stu-id="d564a-169">-Thumbprint</span></span>
<span data-ttu-id="d564a-170">Der Fingerabdruck für das Zertifikat korreliert mit dem SecretIdentifier.</span><span class="sxs-lookup"><span data-stu-id="d564a-170">The thumbprint for the certificate correspoinding to the SecretIdentifier.</span></span> <span data-ttu-id="d564a-171">Verwenden Sie dies, wenn das Zertifikat nicht verwaltet wird, da das Zertifikat im Schlüsseltresor nur als Geheimspeicher gespeichert ist und das Cmdlet den Fingerabdruck nicht erneut abspeichern kann.</span><span class="sxs-lookup"><span data-stu-id="d564a-171">Use this if the certificate is not managed as the key vault would only have the certificate stored as a secret and the cmdlet is unable to retreive the thumbprint.</span></span>

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

### <span data-ttu-id="d564a-172">-VmPassword</span><span class="sxs-lookup"><span data-stu-id="d564a-172">-VmPassword</span></span>

<span data-ttu-id="d564a-173">Das Kennwort der Vm.</span><span class="sxs-lookup"><span data-stu-id="d564a-173">The password of the Vm.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: ByDefaultArmTemplate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Security.SecureString
Parameter Sets: ByExistingKeyVault, ByNewPfxAndVaultName, ByExistingPfxAndVaultName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d564a-174">-VmSku</span><span class="sxs-lookup"><span data-stu-id="d564a-174">-VmSku</span></span>

<span data-ttu-id="d564a-175">Die Vm Sku</span><span class="sxs-lookup"><span data-stu-id="d564a-175">The Vm Sku</span></span>

```yaml
Type: System.String
Parameter Sets: ByDefaultArmTemplate
Aliases: Sku

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d564a-176">-VmUserName</span><span class="sxs-lookup"><span data-stu-id="d564a-176">-VmUserName</span></span>

<span data-ttu-id="d564a-177">Der Benutzername für die Protokollierung bei Vm</span><span class="sxs-lookup"><span data-stu-id="d564a-177">The user name for logging to Vm</span></span>

```yaml
Type: System.String
Parameter Sets: ByDefaultArmTemplate
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d564a-178">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d564a-178">-Confirm</span></span>

<span data-ttu-id="d564a-179">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d564a-179">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d564a-180">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d564a-180">-WhatIf</span></span>

<span data-ttu-id="d564a-181">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d564a-181">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d564a-182">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d564a-182">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d564a-183">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d564a-183">CommonParameters</span></span>
<span data-ttu-id="d564a-184">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d564a-184">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d564a-185">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d564a-185">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d564a-186">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d564a-186">INPUTS</span></span>

### <span data-ttu-id="d564a-187">System.String</span><span class="sxs-lookup"><span data-stu-id="d564a-187">System.String</span></span>

### <span data-ttu-id="d564a-188">System.Security.SecureString</span><span class="sxs-lookup"><span data-stu-id="d564a-188">System.Security.SecureString</span></span>

### <span data-ttu-id="d564a-189">System.Int32</span><span class="sxs-lookup"><span data-stu-id="d564a-189">System.Int32</span></span>

### <span data-ttu-id="d564a-190">Microsoft.Azure.Commands.ServiceFabric.Models.OperatingSystem</span><span class="sxs-lookup"><span data-stu-id="d564a-190">Microsoft.Azure.Commands.ServiceFabric.Models.OperatingSystem</span></span>

## <span data-ttu-id="d564a-191">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d564a-191">OUTPUTS</span></span>

### <span data-ttu-id="d564a-192">Microsoft.Azure.Commands.ServiceFabric.Models.PSDeploymentResult</span><span class="sxs-lookup"><span data-stu-id="d564a-192">Microsoft.Azure.Commands.ServiceFabric.Models.PSDeploymentResult</span></span>

## <span data-ttu-id="d564a-193">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="d564a-193">NOTES</span></span>

## <span data-ttu-id="d564a-194">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="d564a-194">RELATED LINKS</span></span>
