---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 4D7EEDD7-89D4-4B1E-A9A1-B301E759CE72
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageAccount.md
ms.openlocfilehash: ca6bc95d0da6e9793b2bb26ab12362bb74d9212a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93995925"
---
# <span data-ttu-id="80596-101">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="80596-101">Set-AzStorageAccount</span></span>

## <span data-ttu-id="80596-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="80596-102">SYNOPSIS</span></span>
<span data-ttu-id="80596-103">Ändert ein Speicherkonto.</span><span class="sxs-lookup"><span data-stu-id="80596-103">Modifies a Storage account.</span></span>

## <span data-ttu-id="80596-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="80596-104">SYNTAX</span></span>

### <span data-ttu-id="80596-105">StorageEncryption (Standard)</span><span class="sxs-lookup"><span data-stu-id="80596-105">StorageEncryption (Default)</span></span>
```
Set-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-Force] [-SkuName <String>]
 [-AccessTier <String>] [-CustomDomainName <String>] [-UseSubDomain <Boolean>] [-Tag <Hashtable>]
 [-EnableHttpsTrafficOnly <Boolean>] [-StorageEncryption] [-AssignIdentity]
 [-NetworkRuleSet <PSNetworkRuleSet>] [-UpgradeToStorageV2]
 [-EnableAzureActiveDirectoryDomainServicesForFile <Boolean>] [-EnableLargeFileShare] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="80596-106">KeyvaultEncryption</span><span class="sxs-lookup"><span data-stu-id="80596-106">KeyvaultEncryption</span></span>
```
Set-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-Force] [-SkuName <String>]
 [-AccessTier <String>] [-CustomDomainName <String>] [-UseSubDomain <Boolean>] [-Tag <Hashtable>]
 [-EnableHttpsTrafficOnly <Boolean>] [-KeyvaultEncryption] -KeyName <String> -KeyVersion <String>
 -KeyVaultUri <String> [-AssignIdentity] [-NetworkRuleSet <PSNetworkRuleSet>] [-UpgradeToStorageV2]
 [-EnableAzureActiveDirectoryDomainServicesForFile <Boolean>] [-EnableLargeFileShare] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="80596-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="80596-107">DESCRIPTION</span></span>
<span data-ttu-id="80596-108">Das Cmdlet " **Satz-AzStorageAccount** " ändert ein Azure Storage-Konto.</span><span class="sxs-lookup"><span data-stu-id="80596-108">The **Set-AzStorageAccount** cmdlet modifies an Azure Storage account.</span></span>
<span data-ttu-id="80596-109">Sie können dieses Cmdlet verwenden, um den Kontotyp zu ändern, eine Kundendomäne zu aktualisieren oder Tags für ein Speicherkonto einzurichten.</span><span class="sxs-lookup"><span data-stu-id="80596-109">You can use this cmdlet to modify the account type, update a customer domain, or set tags on a Storage account.</span></span>

## <span data-ttu-id="80596-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="80596-110">EXAMPLES</span></span>

### <span data-ttu-id="80596-111">Beispiel 1: Einrichten des Speicher Kontotyps</span><span class="sxs-lookup"><span data-stu-id="80596-111">Example 1: Set the Storage account type</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Type "Standard_RAGRS"
```

<span data-ttu-id="80596-112">Dieser Befehl legt den Typ des speicherkontos auf Standard_RAGRS fest.</span><span class="sxs-lookup"><span data-stu-id="80596-112">This command sets the Storage account type to Standard_RAGRS.</span></span>

### <span data-ttu-id="80596-113">Beispiel 2: Einrichten einer benutzerdefinierten Domäne für ein Speicherkonto</span><span class="sxs-lookup"><span data-stu-id="80596-113">Example 2: Set a custom domain for a Storage account</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -CustomDomainName "www.contoso.com" -UseSubDomain $True
```

<span data-ttu-id="80596-114">Mit diesem Befehl wird eine benutzerdefinierte Domäne für ein Speicherkonto festgelegt.</span><span class="sxs-lookup"><span data-stu-id="80596-114">This command sets a custom domain for a Storage account.</span></span>

### <span data-ttu-id="80596-115">Beispiel 3: Einrichten des Zugriffsstufen Werts</span><span class="sxs-lookup"><span data-stu-id="80596-115">Example 3: Set the access tier value</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -AccessTier Cool
```

<span data-ttu-id="80596-116">Mit dem Befehl wird der Wert der Access-Ebene auf "cool" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="80596-116">The command sets the Access Tier value to be cool.</span></span>

### <span data-ttu-id="80596-117">Beispiel 4: Einrichten der benutzerdefinierten Domäne und der Tags</span><span class="sxs-lookup"><span data-stu-id="80596-117">Example 4: Set the custom domain and tags</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -CustomDomainName "www.domainname.com" -UseSubDomain $true -Tag @{tag0="value0";tag1="value1";tag2="value2"}
```

<span data-ttu-id="80596-118">Der Befehl legt die benutzerdefinierte Domäne und die Tags für ein Speicherkonto fest.</span><span class="sxs-lookup"><span data-stu-id="80596-118">The command sets the custom domain and tags for a Storage account.</span></span>

### <span data-ttu-id="80596-119">Beispiel 5: Konfigurieren der Schlüsselquelle für Verschlüsselung auf keyvault</span><span class="sxs-lookup"><span data-stu-id="80596-119">Example 5: Set Encryption KeySource to Keyvault</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -AssignIdentity
PS C:\>$account = Get-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount"

PS C:\>$keyVault = New-AzKeyVault -VaultName "MyKeyVault" -ResourceGroupName "MyResourceGroup" -Location "EastUS2"
PS C:\>$key = Add-AzKeyVaultKey -VaultName "MyKeyVault" -Name "MyKey" -Destination 'Software'
PS C:\>Set-AzKeyVaultAccessPolicy -VaultName "MyKeyVault" -ObjectId $account.Identity.PrincipalId -PermissionsToKeys wrapkey,unwrapkey,get

PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -KeyvaultEncryption -KeyName $key.Name -KeyVersion $key.Version -KeyVaultUri $keyVault.VaultUri
```

<span data-ttu-id="80596-120">Mit diesem Befehl wird die Verschlüsselungs-keySource mit einem neu erstellten keyvault gesetzt.</span><span class="sxs-lookup"><span data-stu-id="80596-120">This command set Encryption KeySource with a new created Keyvault.</span></span>

### <span data-ttu-id="80596-121">Beispiel 6: Verschlüsselungs-keySource auf "Microsoft. Storage" setzen</span><span class="sxs-lookup"><span data-stu-id="80596-121">Example 6: Set Encryption KeySource to "Microsoft.Storage"</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -StorageEncryption
```

<span data-ttu-id="80596-122">Mit diesem Befehl wird die Verschlüsselungs-keySource auf "Microsoft. Storage" gesetzt.</span><span class="sxs-lookup"><span data-stu-id="80596-122">This command set Encryption KeySource to "Microsoft.Storage"</span></span>

### <span data-ttu-id="80596-123">Beispiel 7: Festlegen der NetworkRuleSet-Eigenschaft eines speicherkontos mit JSON</span><span class="sxs-lookup"><span data-stu-id="80596-123">Example 7: Set NetworkRuleSet property of a Storage account with JSON</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -NetworkRuleSet (@{bypass="Logging,Metrics";
    ipRules=(@{IPAddressOrRange="20.11.0.0/16";Action="allow"},
            @{IPAddressOrRange="10.0.0.0/7";Action="allow"});
    virtualNetworkRules=(@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1";Action="allow"},
                        @{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet2/subnets/subnet2";Action="allow"});
    defaultAction="allow"})
```

<span data-ttu-id="80596-124">Dieser Befehl legt die NetworkRuleSet-Eigenschaft eines speicherkontos mit JSON fest.</span><span class="sxs-lookup"><span data-stu-id="80596-124">This command sets NetworkRuleSet property of a Storage account with JSON</span></span>

### <span data-ttu-id="80596-125">Beispiel 8: Abrufen der NetworkRuleSet-Eigenschaft von einem Speicherkonto und festlegen auf ein anderes Speicherkonto</span><span class="sxs-lookup"><span data-stu-id="80596-125">Example 8: Get NetworkRuleSet property from a Storage account, and set it to another Storage account</span></span>
```
PS C:\> $networkRuleSet = (Get-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount").NetworkRuleSet 
PS C:\> Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount2" -NetworkRuleSet $networkRuleSet
```

<span data-ttu-id="80596-126">Dieser erste Befehl ruft die NetworkRuleSet-Eigenschaft von einem Speicherkonto ab, und der zweite Befehl legt Sie auf ein anderes Speicherkonto fest.</span><span class="sxs-lookup"><span data-stu-id="80596-126">This first command gets NetworkRuleSet property from a Storage account, and the second command sets it to another Storage account</span></span> 

### <span data-ttu-id="80596-127">Beispiel 9: Upgraden eines speicherkontos mit der Art "Speicher" oder "BlobStorage" auf "StorageV2" Art Storage-Konto</span><span class="sxs-lookup"><span data-stu-id="80596-127">Example 9: Upgrade a Storage account with Kind "Storage" or "BlobStorage" to "StorageV2" kind Storage account</span></span>
```
PS C:\> Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -UpgradeToStorageV2
```

<span data-ttu-id="80596-128">Mit dem Befehl wird ein Speicherkonto mit der Art "Speicher" oder "BlobStorage" auf "StorageV2"-Speicherkonto aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="80596-128">The command upgrade a Storage account with Kind "Storage" or "BlobStorage" to "StorageV2" kind Storage account.</span></span>

### <span data-ttu-id="80596-129">Beispiel 10: Aktualisieren eines speicherkontos durch Aktivieren von Azure-Dateien Aad DS-Authentifizierung.</span><span class="sxs-lookup"><span data-stu-id="80596-129">Example 10: Update a Storage account by enable Azure Files AAD DS Authentication.</span></span>
```
PS C:\> Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -EnableAzureActiveDirectoryDomainServicesForFile $true
```

<span data-ttu-id="80596-130">Der Befehl Aktualisieren eines speicherkontos durch Aktivieren von Azure-Dateien Aad DS-Authentifizierung.</span><span class="sxs-lookup"><span data-stu-id="80596-130">The command update a Storage account by enable Azure Files AAD DS Authentication.</span></span>

## <span data-ttu-id="80596-131">Parameter</span><span class="sxs-lookup"><span data-stu-id="80596-131">PARAMETERS</span></span>

### <span data-ttu-id="80596-132">-AccessTier</span><span class="sxs-lookup"><span data-stu-id="80596-132">-AccessTier</span></span>
<span data-ttu-id="80596-133">Gibt die Zugriffsebene des speicherkontos an, das von diesem Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="80596-133">Specifies the access tier of the Storage account that this cmdlet modifies.</span></span>
<span data-ttu-id="80596-134">Die akzeptablen Werte für diesen Parameter sind: heiß und cool.</span><span class="sxs-lookup"><span data-stu-id="80596-134">The acceptable values for this parameter are: Hot and Cool.</span></span>
<span data-ttu-id="80596-135">Wenn Sie die Zugriffsebene ändern, kann dies zu zusätzlichen Gebühren führen.</span><span class="sxs-lookup"><span data-stu-id="80596-135">If you change the access tier, it may result in additional charges.</span></span> <span data-ttu-id="80596-136">Weitere Informationen finden Sie unter [Azure-BLOB-Speicher: heiße und kühle Speicherebenen](http://go.microsoft.com/fwlink/?LinkId=786482).</span><span class="sxs-lookup"><span data-stu-id="80596-136">For more information, see [Azure Blob Storage: Hot and cool storage tiers](http://go.microsoft.com/fwlink/?LinkId=786482).</span></span>
<span data-ttu-id="80596-137">Wenn das Speicherkonto eine Art StorageV2 oder BlobStorage hat, können Sie den *AccessTier* -Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="80596-137">If the Storage account has Kind as StorageV2 or BlobStorage, you can specify the *AccessTier* parameter.</span></span> <span data-ttu-id="80596-138">Wenn das Speicherkonto eine Art Speicher ist, geben Sie den *AccessTier* -Parameter nicht an.</span><span class="sxs-lookup"><span data-stu-id="80596-138">If the Storage account has Kind as Storage, do not specify the *AccessTier* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Hot, Cool

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80596-139">-AsJob</span><span class="sxs-lookup"><span data-stu-id="80596-139">-AsJob</span></span>
<span data-ttu-id="80596-140">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="80596-140">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80596-141">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="80596-141">-AssignIdentity</span></span>
<span data-ttu-id="80596-142">Generieren und Zuweisen einer neuen Speicherkonto Identität für dieses Speicherkonto für die Verwendung mit Schlüssel Verwaltungsdiensten wie Azure keyvault</span><span class="sxs-lookup"><span data-stu-id="80596-142">Generate and assign a new Storage account Identity for this Storage account for use with key management services like Azure KeyVault.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80596-143">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="80596-143">-CustomDomainName</span></span>
<span data-ttu-id="80596-144">Gibt den Namen der benutzerdefinierten Domäne an.</span><span class="sxs-lookup"><span data-stu-id="80596-144">Specifies the name of the custom domain.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80596-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80596-145">-DefaultProfile</span></span>
<span data-ttu-id="80596-146">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="80596-146">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="80596-147">-EnableAzureActiveDirectoryDomainServicesForFile</span><span class="sxs-lookup"><span data-stu-id="80596-147">-EnableAzureActiveDirectoryDomainServicesForFile</span></span>
<span data-ttu-id="80596-148">Aktivieren Sie Azure-Dateien Azure Active Directory-Domänendienst Authentifizierung für das Speicherkonto.</span><span class="sxs-lookup"><span data-stu-id="80596-148">Enable Azure Files Azure Active Directory Domain Service Authentication for the storage account.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80596-149">-EnableHttpsTrafficOnly</span><span class="sxs-lookup"><span data-stu-id="80596-149">-EnableHttpsTrafficOnly</span></span>
<span data-ttu-id="80596-150">Gibt an, ob das Speicherkonto nur HTTPS-Datenverkehr aktiviert.</span><span class="sxs-lookup"><span data-stu-id="80596-150">Indicates whether or not the Storage account only enables HTTPS traffic.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80596-151">-EnableLargeFileShare</span><span class="sxs-lookup"><span data-stu-id="80596-151">-EnableLargeFileShare</span></span>
<span data-ttu-id="80596-152">Gibt an, ob das Speicherkonto große Dateifreigaben mit mehr als 5 tib-Kapazität unterstützenkann.</span><span class="sxs-lookup"><span data-stu-id="80596-152">Indicates whether or not the storage account can support large file shares with more than 5 TiB capacity.</span></span> <span data-ttu-id="80596-153">Sobald das Konto aktiviert ist, kann das Feature nicht deaktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="80596-153">Once the account is enabled, the feature cannot be disabled.</span></span> <span data-ttu-id="80596-154">Wird derzeit nur für LRS-und ZRS-Replikationstypen unterstützt, daher sind Konto Konvertierungen in Geo-redundante Konten nicht möglich.</span><span class="sxs-lookup"><span data-stu-id="80596-154">Currently only supported for LRS and ZRS replication types, hence account conversions to geo-redundant accounts would not be possible.</span></span> <span data-ttu-id="80596-155">Weitere Informationen finden Sie unter https://go.microsoft.com/fwlink/?linkid=2086047</span><span class="sxs-lookup"><span data-stu-id="80596-155">Learn more in https://go.microsoft.com/fwlink/?linkid=2086047</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80596-156">-Force</span><span class="sxs-lookup"><span data-stu-id="80596-156">-Force</span></span>
<span data-ttu-id="80596-157">Erzwingt, dass die Änderung in das Speicherkonto geschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="80596-157">Forces the change to be written to the Storage account.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80596-158">-KeyName</span><span class="sxs-lookup"><span data-stu-id="80596-158">-KeyName</span></span>
<span data-ttu-id="80596-159">Wenn Sie-KeyvaultEncryption verwenden, um die Verschlüsselung mit Key Vault zu aktivieren, geben Sie die KeyName-Eigenschaft mit dieser Option an.</span><span class="sxs-lookup"><span data-stu-id="80596-159">If using -KeyvaultEncryption to enable encryption with Key Vault, specify the Keyname property with this option.</span></span>

```yaml
Type: System.String
Parameter Sets: KeyvaultEncryption
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80596-160">-KeyvaultEncryption</span><span class="sxs-lookup"><span data-stu-id="80596-160">-KeyvaultEncryption</span></span>
<span data-ttu-id="80596-161">Gibt an, ob Sie Microsoft keyvault für die Verschlüsselungsschlüssel verwenden möchten, wenn Sie die Speicherdienst Verschlüsselung verwenden.</span><span class="sxs-lookup"><span data-stu-id="80596-161">Indicates whether or not to use Microsoft KeyVault for the encryption keys when using Storage Service Encryption.</span></span> <span data-ttu-id="80596-162">Wenn keyName, keyversion und KeyVaultUri eingestellt sind, wird keySource auf Microsoft. keyvault festgesetzt, ob dieser Parameter festgesetzt ist oder nicht.</span><span class="sxs-lookup"><span data-stu-id="80596-162">If KeyName, KeyVersion, and KeyVaultUri are all set, KeySource will be set to Microsoft.Keyvault whether this parameter is set or not.</span></span> 

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: KeyvaultEncryption
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80596-163">-KeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="80596-163">-KeyVaultUri</span></span>
<span data-ttu-id="80596-164">Verwenden Sie bei Verwendung der Schlüssel Vault-Verschlüsselung durch Angabe des-KeyvaultEncryption-Parameters diese Option, um den URI für den schlüsseltresor anzugeben.</span><span class="sxs-lookup"><span data-stu-id="80596-164">When using Key Vault Encryption by specifying the -KeyvaultEncryption parameter, use this option to specify the URI to the Key Vault.</span></span>

```yaml
Type: System.String
Parameter Sets: KeyvaultEncryption
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80596-165">-Keyversion</span><span class="sxs-lookup"><span data-stu-id="80596-165">-KeyVersion</span></span>
<span data-ttu-id="80596-166">Verwenden Sie bei Verwendung der Schlüssel Vault-Verschlüsselung durch Angabe des-KeyvaultEncryption-Parameters diese Option, um den URI für die Schlüssel Version anzugeben.</span><span class="sxs-lookup"><span data-stu-id="80596-166">When using Key Vault Encryption by specifying the -KeyvaultEncryption parameter, use this option to specify the URI to the Key Version.</span></span>

```yaml
Type: System.String
Parameter Sets: KeyvaultEncryption
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80596-167">-Name</span><span class="sxs-lookup"><span data-stu-id="80596-167">-Name</span></span>
<span data-ttu-id="80596-168">Gibt den Namen des zu ändernden speicherkontos an.</span><span class="sxs-lookup"><span data-stu-id="80596-168">Specifies the name of the Storage account to modify.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80596-169">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="80596-169">-NetworkRuleSet</span></span>
<span data-ttu-id="80596-170">NetworkRuleSet wird verwendet, um eine Reihe von Konfigurationsregeln für Firewalls und virtuelle Netzwerke zu definieren sowie Werte für Netzwerkeigenschaften festzulegen, beispielsweise Dienste, die die Regeln umgehen dürfen, und die Behandlung von Anforderungen, die keiner der definierten Regeln entsprechen.</span><span class="sxs-lookup"><span data-stu-id="80596-170">NetworkRuleSet is used to define a set of configuration rules for firewalls and virtual networks, as well as to set values for network properties such as services allowed to bypass the rules and how to handle requests that don't match any of the defined rules.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSNetworkRuleSet
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80596-171">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="80596-171">-ResourceGroupName</span></span>
<span data-ttu-id="80596-172">Gibt den Namen der Ressourcengruppe an, in der das Speicherkonto geändert werden soll.</span><span class="sxs-lookup"><span data-stu-id="80596-172">Specifies the name of the resource group in which to modify the Storage account.</span></span>

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

### <span data-ttu-id="80596-173">-SkuName</span><span class="sxs-lookup"><span data-stu-id="80596-173">-SkuName</span></span>
<span data-ttu-id="80596-174">Gibt den SKU-Namen des speicherkontos an.</span><span class="sxs-lookup"><span data-stu-id="80596-174">Specifies the SKU name of the Storage account.</span></span>
<span data-ttu-id="80596-175">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="80596-175">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="80596-176">Standard_LRS-lokal redundanter Speicherplatz.</span><span class="sxs-lookup"><span data-stu-id="80596-176">Standard_LRS - Locally-redundant storage.</span></span>
- <span data-ttu-id="80596-177">Standard_ZRS Zone – redundanter Speicherplatz.</span><span class="sxs-lookup"><span data-stu-id="80596-177">Standard_ZRS - Zone-redundant storage.</span></span>
- <span data-ttu-id="80596-178">Standard_GRS-Geo-redundanter Speicher.</span><span class="sxs-lookup"><span data-stu-id="80596-178">Standard_GRS - Geo-redundant storage.</span></span>
- <span data-ttu-id="80596-179">Standard_RAGRS Lesezugriff Geo-redundanter Speicher.</span><span class="sxs-lookup"><span data-stu-id="80596-179">Standard_RAGRS - Read access geo-redundant storage.</span></span>
- <span data-ttu-id="80596-180">Premium_LRS-Premium-lokal redundanter Speicherplatz.</span><span class="sxs-lookup"><span data-stu-id="80596-180">Premium_LRS - Premium locally-redundant storage.</span></span>
- <span data-ttu-id="80596-181">Standard_GZRS-Geo-redundante Zone – redundanter Speicherplatz.</span><span class="sxs-lookup"><span data-stu-id="80596-181">Standard_GZRS - Geo-redundant zone-redundant storage.</span></span>
- <span data-ttu-id="80596-182">Standard_RAGZRS-Read Access Geo-redundant Zone-redundanter Speicher.</span><span class="sxs-lookup"><span data-stu-id="80596-182">Standard_RAGZRS - Read access geo-redundant zone-redundant storage.</span></span>
<span data-ttu-id="80596-183">Standard_ZRS-und Premium_LRS Typen können nicht in andere Kontotypen geändert werden.</span><span class="sxs-lookup"><span data-stu-id="80596-183">You cannot change Standard_ZRS and Premium_LRS types to other account types.</span></span>
<span data-ttu-id="80596-184">Sie können andere Kontotypen nicht in Standard_ZRS oder Premium_LRS ändern.</span><span class="sxs-lookup"><span data-stu-id="80596-184">You cannot change other account types to Standard_ZRS or Premium_LRS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountType, AccountType, Type
Accepted values: Standard_LRS, Standard_ZRS, Standard_GRS, Standard_RAGRS, Premium_LRS, Standard_GZRS, Standard_RAGZRS

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80596-185">-StorageEncryption</span><span class="sxs-lookup"><span data-stu-id="80596-185">-StorageEncryption</span></span>
<span data-ttu-id="80596-186">Gibt an, ob die Speicherkonto Verschlüsselung für die Verwendung von Microsoft-verwalteten Schlüsseln festgesetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="80596-186">Indicates whether or not to set the Storage account encryption to use Microsoft-managed keys.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: StorageEncryption
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80596-187">-Tag</span><span class="sxs-lookup"><span data-stu-id="80596-187">-Tag</span></span>
<span data-ttu-id="80596-188">Schlüssel-Wert-Paare in Form einer Hashtabelle, die als Tags auf dem Server definiert ist.</span><span class="sxs-lookup"><span data-stu-id="80596-188">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="80596-189">Beispiel: @ {Key0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="80596-189">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80596-190">-UpgradeToStorageV2</span><span class="sxs-lookup"><span data-stu-id="80596-190">-UpgradeToStorageV2</span></span>
<span data-ttu-id="80596-191">Upgrade des speicherkontos Art von Speicher-oder BlobStorage auf StorageV2.</span><span class="sxs-lookup"><span data-stu-id="80596-191">Upgrade Storage account Kind from  Storage or BlobStorage to StorageV2.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80596-192">-UseSubDomain</span><span class="sxs-lookup"><span data-stu-id="80596-192">-UseSubDomain</span></span>
<span data-ttu-id="80596-193">Gibt an, ob die indirekte CNAME-Validierung aktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="80596-193">Indicates whether to enable indirect CName validation.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80596-194">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="80596-194">-Confirm</span></span>
<span data-ttu-id="80596-195">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="80596-195">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80596-196">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="80596-196">-WhatIf</span></span>
<span data-ttu-id="80596-197">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="80596-197">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="80596-198">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="80596-198">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80596-199">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80596-199">CommonParameters</span></span>
<span data-ttu-id="80596-200">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="80596-200">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80596-201">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="80596-201">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80596-202">Eingaben</span><span class="sxs-lookup"><span data-stu-id="80596-202">INPUTS</span></span>

### <span data-ttu-id="80596-203">System. String</span><span class="sxs-lookup"><span data-stu-id="80596-203">System.String</span></span>

### <span data-ttu-id="80596-204">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="80596-204">System.Collections.Hashtable</span></span>

## <span data-ttu-id="80596-205">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="80596-205">OUTPUTS</span></span>

### <span data-ttu-id="80596-206">Microsoft. Azure. Commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="80596-206">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="80596-207">Notizen</span><span class="sxs-lookup"><span data-stu-id="80596-207">NOTES</span></span>

## <span data-ttu-id="80596-208">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="80596-208">RELATED LINKS</span></span>

[<span data-ttu-id="80596-209">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="80596-209">Get-AzStorageAccount</span></span>](./Get-AzStorageAccount.md)

[<span data-ttu-id="80596-210">Neu – AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="80596-210">New-AzStorageAccount</span></span>](./New-AzStorageAccount.md)

[<span data-ttu-id="80596-211">Remove-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="80596-211">Remove-AzStorageAccount</span></span>](./Remove-AzStorageAccount.md)
