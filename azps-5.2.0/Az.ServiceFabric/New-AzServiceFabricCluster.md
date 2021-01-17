---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/new-azservicefabriccluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricCluster.md
ms.openlocfilehash: 9e5ba2d2ee228da30a887c0c7b318dd9d270d763
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98291088"
---
# <span data-ttu-id="826d3-101">New-AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="826d3-101">New-AzServiceFabricCluster</span></span>

## <span data-ttu-id="826d3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="826d3-102">SYNOPSIS</span></span>

<span data-ttu-id="826d3-103">Dieser Befehl verwendet Zertifikate, die Sie bereitstellen, oder vom System generierte selbst signierte Zertifikate zum Einrichten eines neuen Service Fabric Cluster.</span><span class="sxs-lookup"><span data-stu-id="826d3-103">This command uses certificates that you provide or system generated self-signed certificates to set up a new service fabric cluster.</span></span> <span data-ttu-id="826d3-104">Sie kann eine Standardvorlage oder eine benutzerdefinierte Vorlage verwenden, die Sie bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="826d3-104">It can use a default template or a custom template that you provide.</span></span> <span data-ttu-id="826d3-105">Sie können einen Ordner angeben, in den die selbst signierten Zertifikate exportiert werden sollen, oder sie später aus dem Schlüsseltresor abrufen.</span><span class="sxs-lookup"><span data-stu-id="826d3-105">You have the option of specifying a folder to export the self-signed certificates to or fetching them later from the key vault.</span></span>

## <span data-ttu-id="826d3-106">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="826d3-106">SYNTAX</span></span>

### <span data-ttu-id="826d3-107">ByDefaultArmTemplate (Standard)</span><span class="sxs-lookup"><span data-stu-id="826d3-107">ByDefaultArmTemplate (Default)</span></span>
```
New-AzServiceFabricCluster [-ResourceGroupName] <String> [-CertificateOutputFolder <String>]
 [-CertificatePassword <SecureString>] [-KeyVaultResourceGroupName <String>] [-KeyVaultName <String>]
 -Location <String> [-Name <String>] [-VmUserName <String>] [-ClusterSize <Int32>]
 [-CertificateSubjectName <String>] -VmPassword <SecureString> [-OS <OperatingSystem>] [-VmSku <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="826d3-108">ByExistingKeyVault</span><span class="sxs-lookup"><span data-stu-id="826d3-108">ByExistingKeyVault</span></span>
```
New-AzServiceFabricCluster [-ResourceGroupName] <String> -TemplateFile <String> -ParameterFile <String>
 [-CertificateCommonName <String>] [-CertificateIssuerThumbprint <String>] [-VmPassword <SecureString>]
 -SecretIdentifier <String> [-Thumbprint <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="826d3-109">ByNewPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="826d3-109">ByNewPfxAndVaultName</span></span>
```
New-AzServiceFabricCluster [-ResourceGroupName] <String> -TemplateFile <String> -ParameterFile <String>
 [-CertificateOutputFolder <String>] [-CertificatePassword <SecureString>]
 [-KeyVaultResourceGroupName <String>] [-KeyVaultName <String>] [-CertificateSubjectName <String>]
 [-VmPassword <SecureString>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="826d3-110">ByExistingPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="826d3-110">ByExistingPfxAndVaultName</span></span>
```
New-AzServiceFabricCluster [-ResourceGroupName] <String> -TemplateFile <String> -ParameterFile <String>
 -CertificateFile <String> [-CertificatePassword <SecureString>] [-SecondaryCertificateFile <String>]
 [-SecondaryCertificatePassword <SecureString>] [-KeyVaultResourceGroupName <String>] [-KeyVaultName <String>]
 [-CertificateCommonName <String>] [-CertificateIssuerThumbprint <String>] [-VmPassword <SecureString>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="826d3-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="826d3-111">DESCRIPTION</span></span>

<span data-ttu-id="826d3-112">Der **Befehl "New-AzServiceFabricCluster"** verwendet Zertifikate, die Sie bereitstellen, oder vom System generierte selbst signierte Zertifikate zum Einrichten eines neuen Service Fabric Cluster.</span><span class="sxs-lookup"><span data-stu-id="826d3-112">The **New-AzServiceFabricCluster** command uses certificates that you provide or system generated self-signed certificates to set up a new service fabric cluster.</span></span> <span data-ttu-id="826d3-113">Die verwendete Vorlage kann eine Standardvorlage oder eine benutzerdefinierte Vorlage sein, die Sie bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="826d3-113">The template used can be a default template or a custom template that you provide.</span></span> <span data-ttu-id="826d3-114">Sie können einen Ordner zum Exportieren der selbst signierten Zertifikate angeben oder sie später aus dem Schlüsseltresor abrufen.</span><span class="sxs-lookup"><span data-stu-id="826d3-114">You have the option of specifying a folder to export the self-signed certificates or fetching them later from the key vault.</span></span>
<span data-ttu-id="826d3-115">Wenn Sie eine benutzerdefinierte Vorlagen- und Parameterdatei angeben, müssen Sie die Zertifikatinformationen in der Parameterdatei nicht angeben, das System füllt diese Parameter aus.</span><span class="sxs-lookup"><span data-stu-id="826d3-115">If you are specifying a custom template and parameter file, you don't need to provide the certificate information in the parameter file, the system will populate these parameters.</span></span>
<span data-ttu-id="826d3-116">Die vier Optionen sind nachfolgend ausführlich beschrieben.</span><span class="sxs-lookup"><span data-stu-id="826d3-116">The four options are detailed below.</span></span> <span data-ttu-id="826d3-117">Scrollen Sie nach unten, um Erläuterungen zu den einzelnen Parametern zu finden.</span><span class="sxs-lookup"><span data-stu-id="826d3-117">Scroll down for explanations of each of the parameters.</span></span>

## <span data-ttu-id="826d3-118">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="826d3-118">EXAMPLES</span></span>

### <span data-ttu-id="826d3-119">Beispiel 1: Angeben nur der Clustergröße, des Namens des Zertifikatsubjekts und des Betriebssystems zum Bereitstellen eines Clusters</span><span class="sxs-lookup"><span data-stu-id="826d3-119">Example 1: Specify only the cluster size, the cert subject name, and the OS to deploy a cluster</span></span>

```powershell
$password = "Password#1234" | ConvertTo-SecureString -AsPlainText -Force
$resourceGroupName = "quickstart-sf-group"
$azureRegion = "southcentralus"
$clusterDnsName = "{0}.{1}.cloudapp.azure.com" -f $resourceGroupName, $azureRegion
$localCertificateFolder = "c:\certs"

Write-Output "Create cluster in '$azureRegion' with cert subject name '$clusterDnsName' and cert output path '$localCertificateFolder'"

New-AzServiceFabricCluster -ResourceGroupName $resourceGroupName -Location $azureRegion -ClusterSize 5 -VmPassword $password -CertificateSubjectName $clusterDnsName -CertificateOutputFolder $localCertificateFolder -CertificatePassword $pass -OS WindowsServer2016Datacenter
```

<span data-ttu-id="826d3-120">Dieser Befehl gibt nur die Clustergröße, den Namen des Zertifikatbezeichners und das Betriebssystem zum Bereitstellen eines Clusters an.</span><span class="sxs-lookup"><span data-stu-id="826d3-120">This command specifies only the cluster size, the cert subject name, and the OS to deploy a cluster.</span></span>

### <span data-ttu-id="826d3-121">Beispiel 2: Angeben einer vorhandenen Zertifikatressource in einem Schlüsseltresor und einer benutzerdefinierten Vorlage zum Bereitstellen eines Cluster</span><span class="sxs-lookup"><span data-stu-id="826d3-121">Example 2: Specify an existing Certificate resource in a key vault and a custom template to deploy a cluster</span></span>

```powershell
$resourceGroupName = "test20"
$templateParameterFile = "C:\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploytest.parameters.json"
$templateFile = "C:\azure-quickstart-templates\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploy.json"
$secretId = "https://test1.vault.azure.net:443/secrets/testcertificate4/56ec774dc61a462bbc645ffc9b4b225f"

New-AzServiceFabricCluster -ResourceGroupName $resourceGroupName -TemplateFile $templateFile -ParameterFile $templateParameterFile -SecretIdentifier $secretId
```

<span data-ttu-id="826d3-122">Dieser Befehl gibt eine vorhandene Zertifikatressource in einem Schlüsseltresor und eine benutzerdefinierte Vorlage zum Bereitstellen eines Cluster an.</span><span class="sxs-lookup"><span data-stu-id="826d3-122">This command specifies an existing Certificate resource in a key vault and a custom template to deploy a cluster.</span></span>

### <span data-ttu-id="826d3-123">Beispiel 3: Erstellen eines neuen Clusters mithilfe einer benutzerdefinierten Vorlage</span><span class="sxs-lookup"><span data-stu-id="826d3-123">Example 3: Create a new cluster using a custom template.</span></span> <span data-ttu-id="826d3-124">Geben Sie einen anderen Ressourcengruppennamen für den Schlüsseltresor an, und legen Sie fest, dass das System ein neues Zertifikat in den Tresor hochladet.</span><span class="sxs-lookup"><span data-stu-id="826d3-124">Specify a different resource group name for the key vault and have the system upload a new certificate to it</span></span>

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

<span data-ttu-id="826d3-125">Mit diesem Befehl wird ein neuer Cluster mithilfe einer benutzerdefinierten Vorlage erstellt.</span><span class="sxs-lookup"><span data-stu-id="826d3-125">This command creates a new cluster using a custom template.</span></span> <span data-ttu-id="826d3-126">Geben Sie einen anderen Ressourcengruppennamen für den Schlüsseltresor an, und legen Sie fest, dass das System ein neues Zertifikat in den Tresor hochladet.</span><span class="sxs-lookup"><span data-stu-id="826d3-126">Specify a different resource group name for the key vault and have the system upload a new certificate to it</span></span>

### <span data-ttu-id="826d3-127">Beispiel 4: Ein eigenes Zertifikat und eine benutzerdefinierte Vorlage mitbringen und einen neuen Cluster erstellen</span><span class="sxs-lookup"><span data-stu-id="826d3-127">Example 4: Bring your own Certificate and custom template and create a new cluster</span></span>

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

<span data-ttu-id="826d3-128">Mit diesem Befehl können Sie Ihr eigenes Zertifikat und eine benutzerdefinierte Vorlage zusammenbringen und einen neuen Cluster erstellen.</span><span class="sxs-lookup"><span data-stu-id="826d3-128">This command will let you bring your own Certificate and custom template and create a new cluster.</span></span>

## <span data-ttu-id="826d3-129">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="826d3-129">PARAMETERS</span></span>

### <span data-ttu-id="826d3-130">-CertificateCommonName</span><span class="sxs-lookup"><span data-stu-id="826d3-130">-CertificateCommonName</span></span>

<span data-ttu-id="826d3-131">Häufig verwendeter Zertifikatname</span><span class="sxs-lookup"><span data-stu-id="826d3-131">Certificate common name</span></span>

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

### <span data-ttu-id="826d3-132">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="826d3-132">-CertificateFile</span></span>

<span data-ttu-id="826d3-133">Der vorhandene Zertifikatdateipfad für das primäre Clusterzertifikat</span><span class="sxs-lookup"><span data-stu-id="826d3-133">The existing certificate file path for the primary cluster certificate</span></span>

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

### <span data-ttu-id="826d3-134">-CertificateIssuerThumbprint</span><span class="sxs-lookup"><span data-stu-id="826d3-134">-CertificateIssuerThumbprint</span></span>

<span data-ttu-id="826d3-135">Aussteller des Zertifikats mit Fingerabdruck, durch Kommas getrennt, wenn mehrere</span><span class="sxs-lookup"><span data-stu-id="826d3-135">Certificate issuer thumbprint, separated by commas if more than one</span></span>

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

### <span data-ttu-id="826d3-136">-CertificateOutputFolder</span><span class="sxs-lookup"><span data-stu-id="826d3-136">-CertificateOutputFolder</span></span>

<span data-ttu-id="826d3-137">Der Ordner der neuen zu erstellende Zertifikatdatei</span><span class="sxs-lookup"><span data-stu-id="826d3-137">The folder of the new certificate file to be created</span></span>

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

### <span data-ttu-id="826d3-138">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="826d3-138">-CertificatePassword</span></span>

<span data-ttu-id="826d3-139">Das Kennwort der Zertifikatdatei</span><span class="sxs-lookup"><span data-stu-id="826d3-139">The password of the certificate file</span></span>

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

### <span data-ttu-id="826d3-140">-CertificateSubjectName</span><span class="sxs-lookup"><span data-stu-id="826d3-140">-CertificateSubjectName</span></span>

<span data-ttu-id="826d3-141">Der Betreffname des zu erstellende Zertifikats</span><span class="sxs-lookup"><span data-stu-id="826d3-141">The subject name of the certificate to be created</span></span>

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

### <span data-ttu-id="826d3-142">-ClusterSize</span><span class="sxs-lookup"><span data-stu-id="826d3-142">-ClusterSize</span></span>

<span data-ttu-id="826d3-143">Die Anzahl der Knoten im Cluster.</span><span class="sxs-lookup"><span data-stu-id="826d3-143">The number of nodes in the cluster.</span></span>
<span data-ttu-id="826d3-144">Der Standardwert ist 5 Knoten</span><span class="sxs-lookup"><span data-stu-id="826d3-144">Default are 5 nodes</span></span>

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

### <span data-ttu-id="826d3-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="826d3-145">-DefaultProfile</span></span>

<span data-ttu-id="826d3-146">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="826d3-146">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="826d3-147">-KeyVaultName</span><span class="sxs-lookup"><span data-stu-id="826d3-147">-KeyVaultName</span></span>

<span data-ttu-id="826d3-148">Der Name des Azure-Schlüsseltresor, wenn er nicht angegeben wird, wird standardmäßig auf den Namen der Ressourcengruppe festgelegt.</span><span class="sxs-lookup"><span data-stu-id="826d3-148">Azure key vault name, if not given it will be defaulted to the resource group name</span></span>

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

### <span data-ttu-id="826d3-149">-KeyVaultResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="826d3-149">-KeyVaultResourceGroupName</span></span>

<span data-ttu-id="826d3-150">Der Name der Azure-Schlüsseltresor-Ressourcengruppe, wenn dieser nicht angegeben wird, wird standardmäßig auf "Ressourcengruppenname" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="826d3-150">Azure key vault resource group name, if not given it will be defaulted to resource group name</span></span>

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

### <span data-ttu-id="826d3-151">-Location</span><span class="sxs-lookup"><span data-stu-id="826d3-151">-Location</span></span>

<span data-ttu-id="826d3-152">Speicherort der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="826d3-152">The resource group location</span></span>

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

### <span data-ttu-id="826d3-153">-Name</span><span class="sxs-lookup"><span data-stu-id="826d3-153">-Name</span></span>

<span data-ttu-id="826d3-154">Geben Sie den Namen des Clusters an, wenn er nicht angegeben wird, ist er mit dem Namen der Ressourcengruppe identisch.</span><span class="sxs-lookup"><span data-stu-id="826d3-154">Specify the name of the cluster, if not given it will be same as resource group name</span></span>

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

### <span data-ttu-id="826d3-155">-OS</span><span class="sxs-lookup"><span data-stu-id="826d3-155">-OS</span></span>

<span data-ttu-id="826d3-156">Das Betriebssystem der VMs, aus der der Cluster (Cluster) wird.</span><span class="sxs-lookup"><span data-stu-id="826d3-156">The Operating System of the VMs that make up the cluster.</span></span>

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

### <span data-ttu-id="826d3-157">-ParameterFile</span><span class="sxs-lookup"><span data-stu-id="826d3-157">-ParameterFile</span></span>

<span data-ttu-id="826d3-158">Der Pfad zur Parameterdatei der Vorlage.</span><span class="sxs-lookup"><span data-stu-id="826d3-158">The path to the template parameter file.</span></span>

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

### <span data-ttu-id="826d3-159">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="826d3-159">-ResourceGroupName</span></span>

<span data-ttu-id="826d3-160">Geben Sie den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="826d3-160">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="826d3-161">-SecondaryCertificateFile</span><span class="sxs-lookup"><span data-stu-id="826d3-161">-SecondaryCertificateFile</span></span>

<span data-ttu-id="826d3-162">Der vorhandene Zertifikatdateipfad für das Zertifikat des sekundären Clusters</span><span class="sxs-lookup"><span data-stu-id="826d3-162">The existing certificate file path for the secondary cluster certificate</span></span>

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

### <span data-ttu-id="826d3-163">-SecondaryCertificatePassword</span><span class="sxs-lookup"><span data-stu-id="826d3-163">-SecondaryCertificatePassword</span></span>

<span data-ttu-id="826d3-164">Das Kennwort der Zertifikatdatei</span><span class="sxs-lookup"><span data-stu-id="826d3-164">The password of the certificate file</span></span>

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

### <span data-ttu-id="826d3-165">-SecretIdentifier</span><span class="sxs-lookup"><span data-stu-id="826d3-165">-SecretIdentifier</span></span>

<span data-ttu-id="826d3-166">Die vorhandene geheime Azure Key Vault-URL, z. B. https://mykv.vault.azure.net:443/secrets/mysecrets/55ec7c4dc61a462bbc645ffc9b4b225f ' '</span><span class="sxs-lookup"><span data-stu-id="826d3-166">The existing Azure key vault secret URL, for example 'https://mykv.vault.azure.net:443/secrets/mysecrets/55ec7c4dc61a462bbc645ffc9b4b225f'</span></span>

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

### <span data-ttu-id="826d3-167">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="826d3-167">-TemplateFile</span></span>

<span data-ttu-id="826d3-168">Der Pfad zur Vorlagendatei.</span><span class="sxs-lookup"><span data-stu-id="826d3-168">The path to the template file.</span></span>

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

### <span data-ttu-id="826d3-169">-Thumbprint</span><span class="sxs-lookup"><span data-stu-id="826d3-169">-Thumbprint</span></span>
<span data-ttu-id="826d3-170">Der Fingerabdruck für das Zertifikat, das dem SecretIdentifier-Konto korreliert.</span><span class="sxs-lookup"><span data-stu-id="826d3-170">The thumbprint for the certificate correspoinding to the SecretIdentifier.</span></span> <span data-ttu-id="826d3-171">Verwenden Sie diese Informationen, wenn das Zertifikat nicht verwaltet wird, da der Schlüsseltresor nur das Zertifikat als geheimes Zertifikat speichern würde und das Cmdlet den Fingerdruck nicht erneut abspeichern kann.</span><span class="sxs-lookup"><span data-stu-id="826d3-171">Use this if the certificate is not managed as the key vault would only have the certificate stored as a secret and the cmdlet is unable to retreive the thumbprint.</span></span>

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

### <span data-ttu-id="826d3-172">-VmPassword</span><span class="sxs-lookup"><span data-stu-id="826d3-172">-VmPassword</span></span>

<span data-ttu-id="826d3-173">Das Kennwort der Vm.</span><span class="sxs-lookup"><span data-stu-id="826d3-173">The password of the Vm.</span></span>

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

### <span data-ttu-id="826d3-174">-VmSku</span><span class="sxs-lookup"><span data-stu-id="826d3-174">-VmSku</span></span>

<span data-ttu-id="826d3-175">Die Vm-SKU</span><span class="sxs-lookup"><span data-stu-id="826d3-175">The Vm Sku</span></span>

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

### <span data-ttu-id="826d3-176">-VmUserName</span><span class="sxs-lookup"><span data-stu-id="826d3-176">-VmUserName</span></span>

<span data-ttu-id="826d3-177">Der Benutzername für die Protokollierung bei Vm</span><span class="sxs-lookup"><span data-stu-id="826d3-177">The user name for logging to Vm</span></span>

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

### <span data-ttu-id="826d3-178">-Confirm</span><span class="sxs-lookup"><span data-stu-id="826d3-178">-Confirm</span></span>

<span data-ttu-id="826d3-179">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="826d3-179">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="826d3-180">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="826d3-180">-WhatIf</span></span>

<span data-ttu-id="826d3-181">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="826d3-181">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="826d3-182">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="826d3-182">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="826d3-183">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="826d3-183">CommonParameters</span></span>
<span data-ttu-id="826d3-184">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="826d3-184">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="826d3-185">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="826d3-185">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="826d3-186">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="826d3-186">INPUTS</span></span>

### <span data-ttu-id="826d3-187">System.String</span><span class="sxs-lookup"><span data-stu-id="826d3-187">System.String</span></span>

### <span data-ttu-id="826d3-188">System.Security.SecureString</span><span class="sxs-lookup"><span data-stu-id="826d3-188">System.Security.SecureString</span></span>

### <span data-ttu-id="826d3-189">System.Int32</span><span class="sxs-lookup"><span data-stu-id="826d3-189">System.Int32</span></span>

### <span data-ttu-id="826d3-190">Microsoft.Azure.Commands.ServiceFabric.Models.OperatingSystem</span><span class="sxs-lookup"><span data-stu-id="826d3-190">Microsoft.Azure.Commands.ServiceFabric.Models.OperatingSystem</span></span>

## <span data-ttu-id="826d3-191">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="826d3-191">OUTPUTS</span></span>

### <span data-ttu-id="826d3-192">Microsoft.Azure.Commands.ServiceFabric.Models.PSDEploymentResult</span><span class="sxs-lookup"><span data-stu-id="826d3-192">Microsoft.Azure.Commands.ServiceFabric.Models.PSDeploymentResult</span></span>

## <span data-ttu-id="826d3-193">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="826d3-193">NOTES</span></span>

## <span data-ttu-id="826d3-194">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="826d3-194">RELATED LINKS</span></span>
