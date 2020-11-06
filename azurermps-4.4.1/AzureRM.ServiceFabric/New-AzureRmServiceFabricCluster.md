---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/New-AzureRmServiceFabricCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/New-AzureRmServiceFabricCluster.md
ms.openlocfilehash: c1f6dea6c4fb103107a052d64a82ad81eafdb8c5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504726"
---
# <span data-ttu-id="006b5-101">New-AzureRmServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="006b5-101">New-AzureRmServiceFabricCluster</span></span>

## <span data-ttu-id="006b5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="006b5-102">SYNOPSIS</span></span>
<span data-ttu-id="006b5-103">Dieser Befehl verwendet von Ihnen bereitgestellte Zertifikate oder vom System generierte selbstsignierte Zertifikate, um einen neuen Service Fabric-Cluster einzurichten.</span><span class="sxs-lookup"><span data-stu-id="006b5-103">This command uses certificates that you provide or system generated self-signed certificates to set up a new service fabric cluster.</span></span> <span data-ttu-id="006b5-104">Sie kann eine Standardvorlage oder eine von Ihnen bereitgestellte benutzerdefinierte Vorlage verwenden.</span><span class="sxs-lookup"><span data-stu-id="006b5-104">It can use a default template or a custom template that you provide.</span></span> <span data-ttu-id="006b5-105">Sie haben die Möglichkeit, einen Ordner anzugeben, um die selbstsignierten Zertifikate zu exportieren oder später aus dem schlüsseltresor abzurufen.</span><span class="sxs-lookup"><span data-stu-id="006b5-105">You have the option of specifying a folder to export the self-signed certificates to or fetching them later from the key vault.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="006b5-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="006b5-106">SYNTAX</span></span>

### <span data-ttu-id="006b5-107">ByDefaultArmTemplate (Standard)</span><span class="sxs-lookup"><span data-stu-id="006b5-107">ByDefaultArmTemplate (Default)</span></span>
```
New-AzureRmServiceFabricCluster [-ResourceGroupName] <String> [-CertificateOutputFolder <String>]
 [-CertificatePassword <SecureString>] [-KeyVaultResouceGroupName <String>] [-KeyVaultName <String>]
 -Location <String> [-Name <String>] [-VmUserName <String>] [-ClusterSize <Int32>]
 [-CertificateSubjectName <String>] -VmPassword <SecureString> [-OS <OperatingSystem>] [-VmSku <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="006b5-108">ByExistingKeyVault</span><span class="sxs-lookup"><span data-stu-id="006b5-108">ByExistingKeyVault</span></span>
```
New-AzureRmServiceFabricCluster [-ResourceGroupName] <String> -TemplateFile <String> -ParameterFile <String>
 -SecretIdentifier <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="006b5-109">ByNewPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="006b5-109">ByNewPfxAndVaultName</span></span>
```
New-AzureRmServiceFabricCluster [-ResourceGroupName] <String> -TemplateFile <String> -ParameterFile <String>
 [-CertificateOutputFolder <String>] [-CertificatePassword <SecureString>] [-KeyVaultResouceGroupName <String>]
 [-KeyVaultName <String>] [-CertificateSubjectName <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="006b5-110">ByExistingPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="006b5-110">ByExistingPfxAndVaultName</span></span>
```
New-AzureRmServiceFabricCluster [-ResourceGroupName] <String> -TemplateFile <String> -ParameterFile <String>
 -CertificateFile <String> [-CertificatePassword <SecureString>] [-SecondaryCertificateFile <String>]
 [-SecondaryCertificatePassword <SecureString>] [-KeyVaultResouceGroupName <String>] [-KeyVaultName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="006b5-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="006b5-111">DESCRIPTION</span></span>
<span data-ttu-id="006b5-112">Der Befehl **New-AzureRmServiceFabricCluster** verwendet von Ihnen bereitgestellte Zertifikate oder vom System generierte selbstsignierte Zertifikate, um einen neuen Service Fabric-Cluster einzurichten.</span><span class="sxs-lookup"><span data-stu-id="006b5-112">The **New-AzureRmServiceFabricCluster** command uses certificates that you provide or system generated self-signed certificates to set up a new service fabric cluster.</span></span> <span data-ttu-id="006b5-113">Die verwendete Vorlage kann eine Standardvorlage oder eine von Ihnen bereitgestellte benutzerdefinierte Vorlage sein.</span><span class="sxs-lookup"><span data-stu-id="006b5-113">The template used can be a default template or a custom template that you provide.</span></span> <span data-ttu-id="006b5-114">Sie haben die Möglichkeit, einen Ordner anzugeben, um die selbstsignierten Zertifikate zu exportieren oder später aus dem schlüsseltresor abzurufen.</span><span class="sxs-lookup"><span data-stu-id="006b5-114">You have the option of specifying a folder to export the self-signed certificates or fetching them later from the key vault.</span></span>

<span data-ttu-id="006b5-115">Wenn Sie eine benutzerdefinierte Vorlage und eine Parameterdatei angeben, müssen Sie die Zertifikatinformationen nicht in der Parameterdatei angeben, das System füllt diese Parameter.</span><span class="sxs-lookup"><span data-stu-id="006b5-115">If you are specifying a custom template and parameter file, you don't need to provide the certificate information in the parameter file, the system will populate these parameters.</span></span>

<span data-ttu-id="006b5-116">Die vier Optionen sind im folgenden aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="006b5-116">The four options are detailed below.</span></span> <span data-ttu-id="006b5-117">Scrollen Sie nach unten, um Erläuterungen zu den einzelnen Parametern zu haben.</span><span class="sxs-lookup"><span data-stu-id="006b5-117">Scroll down for explanations of each of the parameters.</span></span>

## <span data-ttu-id="006b5-118">Beispiele</span><span class="sxs-lookup"><span data-stu-id="006b5-118">EXAMPLES</span></span>

### <span data-ttu-id="006b5-119">Beispiel 1: Geben Sie nur die Clustergröße, den Zertifikatantragstellernamen und das Betriebssystem für die Bereitstellungeines Clusters an.</span><span class="sxs-lookup"><span data-stu-id="006b5-119">Example 1: Specify only the cluster size, the cert subject name, and the OS to deploy a cluster.</span></span>
```
$pass="Password#1234" | ConvertTo-SecureString -AsPlainText -Force
$RGname="test01"
$clusterloc="SouthCentralUS"
$subname="{0}.{1}.cloudapp.azure.com" -f $RGname, $clusterloc
$pfxfolder="~\Documents"

Write-Output "create cluster in " $clusterloc "subject name for cert " $subname "and output the cert into " $pfxfolder

New-AzureRmServiceFabricCluster -ResourceGroupName $RGname -Location $clusterloc -ClusterSize 3 -VmPassword $pwd -CertificateSubjectName $subname -CertificateOutputFolder $pfxfolder -CertificatePassword $pwd -OS WindowsServer2016Datacenter
```

<span data-ttu-id="006b5-120">Dieser Befehl gibt nur die Clustergröße, den Zertifikatantragstellernamen und das Betriebssystem für die Bereitstellungeines Clusters an.</span><span class="sxs-lookup"><span data-stu-id="006b5-120">This command specifies only the cluster size, the cert subject name, and the OS to deploy a cluster.</span></span>

### <span data-ttu-id="006b5-121">Beispiel 2: Angeben einer vorhandenen Zertifikat Ressource in einem schlüsseltresor und einer benutzerdefinierten Vorlage zum Bereitstellen eines Clusters</span><span class="sxs-lookup"><span data-stu-id="006b5-121">Example 2: Specify an existing Certificate resource in a key vault and a custom template to deploy a cluster</span></span>
```
$RGname="test20"
$templateParmfile="C:\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploytest.parameters.json"
$templateFile="C:\azure-quickstart-templates\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploy.json"
$secertId="https://test1.vault.azure.net:443/secrets/testcertificate4/56ec774dc61a462bbc645ffc9b4b225f"

New-AzureRmServiceFabricCluster -ResourceGroupName $RGname -TemplateFile $templateFile -ParameterFile $templateParmfile -SecretIdentifier $secertId
```

<span data-ttu-id="006b5-122">Mit diesem Befehl wird eine vorhandene Zertifikat Ressource in einem schlüsseltresor und eine benutzerdefinierte Vorlage zum Bereitstellen eines Clusters angegeben.</span><span class="sxs-lookup"><span data-stu-id="006b5-122">This command specifies an existing Certificate resource in a key vault and a custom template to deploy a cluster.</span></span>

### <span data-ttu-id="006b5-123">Beispiel 3: Erstellen eines neuen Clusters mit einer benutzerdefinierten Vorlage</span><span class="sxs-lookup"><span data-stu-id="006b5-123">Example 3: Create a new cluster using a custom template.</span></span> <span data-ttu-id="006b5-124">Geben Sie den anderen RG-Namen für den schlüsseltresor an, und laden Sie das Zertifikat in das System hoch.</span><span class="sxs-lookup"><span data-stu-id="006b5-124">Specify the different RG name for the key vault and have the system upload the certificate to it</span></span>
```
$pwd="Password#1234" | ConvertTo-SecureString -AsPlainText -Force
$RGname="test20"
$keyVaultRG="test20kvrg"
$keyVault="test20kv"
$clusterloc="SouthCentralUS"
$subname="{0}.{1}.$clusterloc.cloudapp.azure.com" -f $RGName, $clusterloc
$pfxfolder="~\Documents"
$templateParmfile="C:\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploytest.parameters.json"
$templateFile="C:\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploy.json"
$secertId="https://test1.vault.azure.net:443/secrets/testcertificate4/55ec7c4dc61a462bbc645ffc9b4b225f"
$thumprint="C2D7E11DD35153A702A51D10A424A3014B9B6E8B"

New-AzureRmServiceFabricCluster -ResourceGroupName $RGname -TemplateFile $templateFile -ParameterFile $templateParmfile -CertificateOutputFolder $pfxfolder -CertificatePassword $pwd -KeyVaultResouceGroupName $keyVaultRG  -KeyVaultName $keyVault -CertificateSubjectName $subname
```

<span data-ttu-id="006b5-125">Dieser Befehl erstellt einen neuen Cluster unter Verwendung einer benutzerdefinierten Vorlage.</span><span class="sxs-lookup"><span data-stu-id="006b5-125">This command creates a new cluster using a custom template.</span></span> <span data-ttu-id="006b5-126">Geben Sie den anderen RG-Namen für den schlüsseltresor an, und laden Sie das Zertifikat in das System hoch.</span><span class="sxs-lookup"><span data-stu-id="006b5-126">Specify the different RG name for the key vault and have the system upload the certificate to it.</span></span>

### <span data-ttu-id="006b5-127">Beispiel 4: Erstellen eines eigenen Zertifikats und einer benutzerdefinierten Vorlage und Erstellen eines neuen Clusters</span><span class="sxs-lookup"><span data-stu-id="006b5-127">Example 4: Bring your own Certificate and custom template and create a new cluster</span></span>
```
$certPwd="Password#1234" | ConvertTo-SecureString -AsPlainText -Force
$RGname="test20"
$keyVaultRG="test20kvrg"
$keyVault="test20kv"
$clusterloc="SouthCentralUS"
$pfxsourcefile="c:\Mycertificates\my2017Prodcert.pfx"
$templateParmfile="~\Documents\GitHub\azure-quickstart-templates-parms\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploytest.parameters.json"
$templateFile="~\GitHub\azure-quickstart-templates\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploy.json"

New-AzureRmServiceFabricCluster -ResourceGroupName $RGname -TemplateFile $templateFile -ParameterFile $templateParmfile -CertificateSourceFile $pfxsourcefile -CertificatePassword $certpwd -KeyVaultResouceGroupName $keyVaultRG -KeyVaultName $keyVault
```

<span data-ttu-id="006b5-128">Mit diesem Befehl können Sie ein eigenes Zertifikat und eine benutzerdefinierte Vorlage erstellen und einen neuen Cluster erstellen.</span><span class="sxs-lookup"><span data-stu-id="006b5-128">This command will let you bring your own Certificate and custom template and create a new cluster.</span></span>

## <span data-ttu-id="006b5-129">Parameter</span><span class="sxs-lookup"><span data-stu-id="006b5-129">PARAMETERS</span></span>

### <span data-ttu-id="006b5-130">-Certificatedatei</span><span class="sxs-lookup"><span data-stu-id="006b5-130">-CertificateFile</span></span>
<span data-ttu-id="006b5-131">Der vorhandene Zertifikats Dateipfad für das primäre Cluster Zertifikat.</span><span class="sxs-lookup"><span data-stu-id="006b5-131">The existing certificate file path for the primary cluster certificate.</span></span>

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

### <span data-ttu-id="006b5-132">-CertificateOutputFolder</span><span class="sxs-lookup"><span data-stu-id="006b5-132">-CertificateOutputFolder</span></span>
<span data-ttu-id="006b5-133">Der Ordner der neuen Zertifikatsdatei, die erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="006b5-133">The folder of the new certificate file to be created.</span></span>

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

### <span data-ttu-id="006b5-134">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="006b5-134">-CertificatePassword</span></span>
<span data-ttu-id="006b5-135">Das Kennwort der Zertifikatsdatei.</span><span class="sxs-lookup"><span data-stu-id="006b5-135">The password of the certificate file.</span></span>

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

### <span data-ttu-id="006b5-136">-CertificateSubjectName</span><span class="sxs-lookup"><span data-stu-id="006b5-136">-CertificateSubjectName</span></span>
<span data-ttu-id="006b5-137">Der Name des Antragstellers des zu erstellenden Zertifikats.</span><span class="sxs-lookup"><span data-stu-id="006b5-137">The subject name of the certificate to be created.</span></span>

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

### <span data-ttu-id="006b5-138">-Clusterisieren</span><span class="sxs-lookup"><span data-stu-id="006b5-138">-ClusterSize</span></span>
<span data-ttu-id="006b5-139">Die Anzahl der Knoten im Cluster.</span><span class="sxs-lookup"><span data-stu-id="006b5-139">The number of nodes in the cluster.</span></span> <span data-ttu-id="006b5-140">Standard sind fünf Knoten.</span><span class="sxs-lookup"><span data-stu-id="006b5-140">Default are 5 nodes.</span></span>

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

### <span data-ttu-id="006b5-141">-Keyvaultname</span><span class="sxs-lookup"><span data-stu-id="006b5-141">-KeyVaultName</span></span>
<span data-ttu-id="006b5-142">Azure Key Vault-Name.</span><span class="sxs-lookup"><span data-stu-id="006b5-142">Azure key vault name.</span></span> <span data-ttu-id="006b5-143">Wenn nicht angegeben, wird der Name der Ressourcengruppe standardmäßig verwendet.</span><span class="sxs-lookup"><span data-stu-id="006b5-143">If not given, it will be defaulted to the resource group name.</span></span>

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

### <span data-ttu-id="006b5-144">-KeyVaultResouceGroupName</span><span class="sxs-lookup"><span data-stu-id="006b5-144">-KeyVaultResouceGroupName</span></span>
<span data-ttu-id="006b5-145">Azure Key Vault-Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="006b5-145">Azure key vault resource group name.</span></span> <span data-ttu-id="006b5-146">Wenn nicht angegeben, wird der Name der Ressourcengruppe standardmäßig verwendet.</span><span class="sxs-lookup"><span data-stu-id="006b5-146">If not given, it will be defaulted to resource group name.</span></span>

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

### <span data-ttu-id="006b5-147">-Standort</span><span class="sxs-lookup"><span data-stu-id="006b5-147">-Location</span></span>
<span data-ttu-id="006b5-148">Der Speicherort der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="006b5-148">The resource group location.</span></span>

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

### <span data-ttu-id="006b5-149">-Name</span><span class="sxs-lookup"><span data-stu-id="006b5-149">-Name</span></span>
<span data-ttu-id="006b5-150">Geben Sie den Namen des Clusters an.</span><span class="sxs-lookup"><span data-stu-id="006b5-150">Specify the name of the cluster.</span></span> <span data-ttu-id="006b5-151">Wenn Sie nicht angegeben wird, ist Sie mit dem Namen der Ressourcengruppe identisch.</span><span class="sxs-lookup"><span data-stu-id="006b5-151">If not given, it will be same as resource group name.</span></span>

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

### <span data-ttu-id="006b5-152">-OS</span><span class="sxs-lookup"><span data-stu-id="006b5-152">-OS</span></span>
<span data-ttu-id="006b5-153">Das Betriebs System der VMS, aus denen sich der Cluster zusammensetzen soll</span><span class="sxs-lookup"><span data-stu-id="006b5-153">The Operating System of the VMs that make up the cluster.</span></span>

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

### <span data-ttu-id="006b5-154">-Parameterdatei</span><span class="sxs-lookup"><span data-stu-id="006b5-154">-ParameterFile</span></span>
<span data-ttu-id="006b5-155">Der Pfad zur Vorlagenparameter Datei.</span><span class="sxs-lookup"><span data-stu-id="006b5-155">The path to the template parameter file.</span></span>

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

### <span data-ttu-id="006b5-156">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="006b5-156">-ResourceGroupName</span></span>
<span data-ttu-id="006b5-157">Geben Sie den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="006b5-157">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="006b5-158">-SecondaryCertificateFile</span><span class="sxs-lookup"><span data-stu-id="006b5-158">-SecondaryCertificateFile</span></span>
<span data-ttu-id="006b5-159">Der vorhandene Zertifikats Dateipfad für das sekundäre Cluster Zertifikat.</span><span class="sxs-lookup"><span data-stu-id="006b5-159">The existing certificate file path for the secondary cluster certificate.</span></span>

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

### <span data-ttu-id="006b5-160">-SecondaryCertificatePassword</span><span class="sxs-lookup"><span data-stu-id="006b5-160">-SecondaryCertificatePassword</span></span>
<span data-ttu-id="006b5-161">Das Kennwort der Zertifikatsdatei.</span><span class="sxs-lookup"><span data-stu-id="006b5-161">The password of the certificate file.</span></span>

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

### <span data-ttu-id="006b5-162">-SecretIdentifier</span><span class="sxs-lookup"><span data-stu-id="006b5-162">-SecretIdentifier</span></span>
<span data-ttu-id="006b5-163">Die vorhandene Azure Key Vault Secret-URL, beispielsweise: " https://mykv.vault.azure.net:443/secrets/mysecrets/55ec7c4dc61a462bbc645ffc9b4b225f '.</span><span class="sxs-lookup"><span data-stu-id="006b5-163">The existing Azure key vault secret URL, for example: 'https://mykv.vault.azure.net:443/secrets/mysecrets/55ec7c4dc61a462bbc645ffc9b4b225f'.</span></span>

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

### <span data-ttu-id="006b5-164">-Vorlagendatei</span><span class="sxs-lookup"><span data-stu-id="006b5-164">-TemplateFile</span></span>
<span data-ttu-id="006b5-165">Der Pfad zur Vorlagendatei.</span><span class="sxs-lookup"><span data-stu-id="006b5-165">The path to the template file.</span></span>

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

### <span data-ttu-id="006b5-166">-VmPassword</span><span class="sxs-lookup"><span data-stu-id="006b5-166">-VmPassword</span></span>
<span data-ttu-id="006b5-167">Das Kennwort des VM.</span><span class="sxs-lookup"><span data-stu-id="006b5-167">The password of the Vm.</span></span>

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

### <span data-ttu-id="006b5-168">-VmSku</span><span class="sxs-lookup"><span data-stu-id="006b5-168">-VmSku</span></span>
<span data-ttu-id="006b5-169">Die VM-SKU.</span><span class="sxs-lookup"><span data-stu-id="006b5-169">The Vm Sku.</span></span>

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

### <span data-ttu-id="006b5-170">-VmUserName</span><span class="sxs-lookup"><span data-stu-id="006b5-170">-VmUserName</span></span>
<span data-ttu-id="006b5-171">Der Benutzername für die Anmeldung bei VM.</span><span class="sxs-lookup"><span data-stu-id="006b5-171">The user name for logging to Vm.</span></span>

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

### <span data-ttu-id="006b5-172">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="006b5-172">-Confirm</span></span>
<span data-ttu-id="006b5-173">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="006b5-173">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="006b5-174">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="006b5-174">-WhatIf</span></span>
<span data-ttu-id="006b5-175">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="006b5-175">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="006b5-176">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="006b5-176">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="006b5-177">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="006b5-177">-DefaultProfile</span></span>
<span data-ttu-id="006b5-178">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="006b5-178">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="006b5-179">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="006b5-179">CommonParameters</span></span>
<span data-ttu-id="006b5-180">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="006b5-180">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="006b5-181">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="006b5-181">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="006b5-182">Eingaben</span><span class="sxs-lookup"><span data-stu-id="006b5-182">INPUTS</span></span>

### <span data-ttu-id="006b5-183">System. String</span><span class="sxs-lookup"><span data-stu-id="006b5-183">System.String</span></span>
<span data-ttu-id="006b5-184">System. Security. SecureString System. Int32 Microsoft. Azure. Commands. ServiceFabric. Models. OperatingSystem</span><span class="sxs-lookup"><span data-stu-id="006b5-184">System.Security.SecureString System.Int32 Microsoft.Azure.Commands.ServiceFabric.Models.OperatingSystem</span></span>

## <span data-ttu-id="006b5-185">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="006b5-185">OUTPUTS</span></span>

### <span data-ttu-id="006b5-186">Microsoft.Azure.Commands.ServiceFabric.Models.PSDeploymentResult</span><span class="sxs-lookup"><span data-stu-id="006b5-186">Microsoft.Azure.Commands.ServiceFabric.Models.PSDeploymentResult</span></span>

## <span data-ttu-id="006b5-187">Notizen</span><span class="sxs-lookup"><span data-stu-id="006b5-187">NOTES</span></span>

## <span data-ttu-id="006b5-188">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="006b5-188">RELATED LINKS</span></span>

