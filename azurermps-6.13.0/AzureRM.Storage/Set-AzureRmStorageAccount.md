---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
ms.assetid: 4D7EEDD7-89D4-4B1E-A9A1-B301E759CE72
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/set-azurermstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Set-AzureRmStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Set-AzureRmStorageAccount.md
ms.openlocfilehash: c182ee26f66cf20ab50bd778e398061ff39c60c0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498146"
---
# <span data-ttu-id="f23da-101">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f23da-101">Set-AzureRmStorageAccount</span></span>

## <span data-ttu-id="f23da-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f23da-102">SYNOPSIS</span></span>
<span data-ttu-id="f23da-103">Ändert ein Speicherkonto.</span><span class="sxs-lookup"><span data-stu-id="f23da-103">Modifies a Storage account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f23da-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f23da-104">SYNTAX</span></span>

### <span data-ttu-id="f23da-105">StorageEncryption (Standard)</span><span class="sxs-lookup"><span data-stu-id="f23da-105">StorageEncryption (Default)</span></span>
```
Set-AzureRmStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-Force] [-SkuName <String>]
 [-AccessTier <String>] [-CustomDomainName <String>] [-UseSubDomain <Boolean>] [-Tag <Hashtable>]
 [-EnableHttpsTrafficOnly <Boolean>] [-StorageEncryption] [-AssignIdentity]
 [-NetworkRuleSet <PSNetworkRuleSet>] [-UpgradeToStorageV2] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f23da-106">KeyvaultEncryption</span><span class="sxs-lookup"><span data-stu-id="f23da-106">KeyvaultEncryption</span></span>
```
Set-AzureRmStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-Force] [-SkuName <String>]
 [-AccessTier <String>] [-CustomDomainName <String>] [-UseSubDomain <Boolean>] [-Tag <Hashtable>]
 [-EnableHttpsTrafficOnly <Boolean>] [-KeyvaultEncryption] -KeyName <String> -KeyVersion <String>
 -KeyVaultUri <String> [-AssignIdentity] [-NetworkRuleSet <PSNetworkRuleSet>] [-UpgradeToStorageV2] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f23da-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f23da-107">DESCRIPTION</span></span>
<span data-ttu-id="f23da-108">Das Cmdlet " **Satz-AzureRmStorageAccount** " ändert ein Azure Storage-Konto.</span><span class="sxs-lookup"><span data-stu-id="f23da-108">The **Set-AzureRmStorageAccount** cmdlet modifies an Azure Storage account.</span></span>
<span data-ttu-id="f23da-109">Sie können dieses Cmdlet verwenden, um den Kontotyp zu ändern, eine Kundendomäne zu aktualisieren oder Tags für ein Speicherkonto einzurichten.</span><span class="sxs-lookup"><span data-stu-id="f23da-109">You can use this cmdlet to modify the account type, update a customer domain, or set tags on a Storage account.</span></span>

## <span data-ttu-id="f23da-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f23da-110">EXAMPLES</span></span>

### <span data-ttu-id="f23da-111">Beispiel 1: Einrichten des Speicher Kontotyps</span><span class="sxs-lookup"><span data-stu-id="f23da-111">Example 1: Set the Storage account type</span></span>
```
PS C:\>Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Type "Standard_RAGRS"
```

<span data-ttu-id="f23da-112">Dieser Befehl legt den Typ des speicherkontos auf Standard_RAGRS fest.</span><span class="sxs-lookup"><span data-stu-id="f23da-112">This command sets the Storage account type to Standard_RAGRS.</span></span>

### <span data-ttu-id="f23da-113">Beispiel 2: Einrichten einer benutzerdefinierten Domäne für ein Speicherkonto</span><span class="sxs-lookup"><span data-stu-id="f23da-113">Example 2: Set a custom domain for a Storage account</span></span>
```
PS C:\>Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -CustomDomainName "www.contoso.com" -UseSubDomain $True
```

<span data-ttu-id="f23da-114">Mit diesem Befehl wird eine benutzerdefinierte Domäne für ein Speicherkonto festgelegt.</span><span class="sxs-lookup"><span data-stu-id="f23da-114">This command sets a custom domain for a Storage account.</span></span>

### <span data-ttu-id="f23da-115">Beispiel 3: Einrichten des Zugriffsstufen Werts</span><span class="sxs-lookup"><span data-stu-id="f23da-115">Example 3: Set the access tier value</span></span>
```
PS C:\>Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -AccessTier Cool
```

<span data-ttu-id="f23da-116">Mit dem Befehl wird der Wert der Access-Ebene auf "cool" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="f23da-116">The command sets the Access Tier value to be cool.</span></span>

### <span data-ttu-id="f23da-117">Beispiel 4: Einrichten der benutzerdefinierten Domäne und der Tags</span><span class="sxs-lookup"><span data-stu-id="f23da-117">Example 4: Set the custom domain and tags</span></span>
```
PS C:\>Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -CustomDomainName "www.domainname.com" -UseSubDomain $true -Tag @{tag0="value0";tag1="value1";tag2="value2"}
```

<span data-ttu-id="f23da-118">Der Befehl legt die benutzerdefinierte Domäne und die Tags für ein Speicherkonto fest.</span><span class="sxs-lookup"><span data-stu-id="f23da-118">The command sets the custom domain and tags for a Storage account.</span></span>

### <span data-ttu-id="f23da-119">Beispiel 5: Konfigurieren der Schlüsselquelle für Verschlüsselung auf keyvault</span><span class="sxs-lookup"><span data-stu-id="f23da-119">Example 5: Set Encryption KeySource to Keyvault</span></span>
```
PS C:\>Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -AssignIdentity
PS C:\>$account = Get-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount"

PS C:\>$keyVault = New-AzureRmKeyVault -VaultName "MyKeyVault" -ResourceGroupName "MyResourceGroup" -Location "EastUS2"
PS C:\>$key = Add-AzureKeyVaultKey -VaultName "MyKeyVault" -Name "MyKey" -Destination 'Software'
PS C:\>Set-AzureRmKeyVaultAccessPolicy -VaultName "MyKeyVault" -ObjectId $account.Identity.PrincipalId -PermissionsToKeys wrapkey,unwrapkey,get

PS C:\>Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -KeyvaultEncryption -KeyName $key.Name -KeyVersion $key.Version -KeyVaultUri $keyVault.VaultUri
```

<span data-ttu-id="f23da-120">Mit diesem Befehl wird die Verschlüsselungs-keySource mit einem neu erstellten keyvault gesetzt.</span><span class="sxs-lookup"><span data-stu-id="f23da-120">This command set Encryption KeySource with a new created Keyvault.</span></span>

### <span data-ttu-id="f23da-121">Beispiel 6: Verschlüsselungs-keySource auf "Microsoft. Storage" setzen</span><span class="sxs-lookup"><span data-stu-id="f23da-121">Example 6: Set Encryption KeySource to "Microsoft.Storage"</span></span>
```
PS C:\>Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -StorageEncryption
```

<span data-ttu-id="f23da-122">Mit diesem Befehl wird die Verschlüsselungs-keySource auf "Microsoft. Storage" gesetzt.</span><span class="sxs-lookup"><span data-stu-id="f23da-122">This command set Encryption KeySource to "Microsoft.Storage"</span></span>

### <span data-ttu-id="f23da-123">Beispiel 7: Festlegen der NetworkRuleSet-Eigenschaft eines speicherkontos mit JSON</span><span class="sxs-lookup"><span data-stu-id="f23da-123">Example 7: Set NetworkRuleSet property of a Storage account with JSON</span></span>
```
PS C:\>Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -NetworkRuleSet (@{bypass="Logging,Metrics";
    ipRules=(@{IPAddressOrRange="20.11.0.0/16";Action="allow"},
            @{IPAddressOrRange="10.0.0.0/7";Action="allow"});
    virtualNetworkRules=(@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1";Action="allow"},
                        @{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet2/subnets/subnet2";Action="allow"});
    defaultAction="allow"})
```

<span data-ttu-id="f23da-124">Dieser Befehl legt die NetworkRuleSet-Eigenschaft eines speicherkontos mit JSON fest.</span><span class="sxs-lookup"><span data-stu-id="f23da-124">This command sets NetworkRuleSet property of a Storage account with JSON</span></span>

### <span data-ttu-id="f23da-125">Beispiel 8: Abrufen der NetworkRuleSet-Eigenschaft von einem Speicherkonto und festlegen auf ein anderes Speicherkonto</span><span class="sxs-lookup"><span data-stu-id="f23da-125">Example 8: Get NetworkRuleSet property from a Storage account, and set it to another Storage account</span></span>
```
PS C:\> $networkRuleSet = (Get-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount").NetworkRuleSet 
PS C:\> Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount2" -NetworkRuleSet $networkRuleSet
```

<span data-ttu-id="f23da-126">Dieser erste Befehl ruft die NetworkRuleSet-Eigenschaft von einem Speicherkonto ab, und der zweite Befehl legt Sie auf ein anderes Speicherkonto fest.</span><span class="sxs-lookup"><span data-stu-id="f23da-126">This first command gets NetworkRuleSet property from a Storage account, and the second command sets it to another Storage account</span></span> 

### <span data-ttu-id="f23da-127">Beispiel 9: Upgraden eines speicherkontos mit der Art "Speicher" oder "BlobStorage" auf "StorageV2" Art Storage-Konto</span><span class="sxs-lookup"><span data-stu-id="f23da-127">Example 9: Upgrade a Storage account with Kind "Storage" or "BlobStorage" to "StorageV2" kind Storage account</span></span>
```
PS C:\> Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -UpgradeToStorageV2
```

<span data-ttu-id="f23da-128">Mit dem Befehl wird ein Speicherkonto mit der Art "Speicher" oder "BlobStorage" auf "StorageV2"-Speicherkonto aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="f23da-128">The command upgrade a Storage account with Kind "Storage" or "BlobStorage" to "StorageV2" kind Storage account.</span></span>

## <span data-ttu-id="f23da-129">Parameter</span><span class="sxs-lookup"><span data-stu-id="f23da-129">PARAMETERS</span></span>

### <span data-ttu-id="f23da-130">-AccessTier</span><span class="sxs-lookup"><span data-stu-id="f23da-130">-AccessTier</span></span>
<span data-ttu-id="f23da-131">Gibt die Zugriffsebene des speicherkontos an, das von diesem Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="f23da-131">Specifies the access tier of the Storage account that this cmdlet modifies.</span></span>
<span data-ttu-id="f23da-132">Die akzeptablen Werte für diesen Parameter sind: heiß und cool.</span><span class="sxs-lookup"><span data-stu-id="f23da-132">The acceptable values for this parameter are: Hot and Cool.</span></span>
<span data-ttu-id="f23da-133">Wenn Sie die Zugriffsebene ändern, kann dies zu zusätzlichen Gebühren führen.</span><span class="sxs-lookup"><span data-stu-id="f23da-133">If you change the access tier, it may result in additional charges.</span></span> <span data-ttu-id="f23da-134">Weitere Informationen finden Sie unter [Azure-BLOB-Speicher: heiße und kühle Speicherebenen](https://go.microsoft.com/fwlink/?LinkId=786482).</span><span class="sxs-lookup"><span data-stu-id="f23da-134">For more information, see [Azure Blob Storage: Hot and cool storage tiers](https://go.microsoft.com/fwlink/?LinkId=786482).</span></span>
<span data-ttu-id="f23da-135">Wenn das Speicherkonto eine Art StorageV2 oder BlobStorage hat, können Sie den *AccessTier* -Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="f23da-135">If the Storage account has Kind as StorageV2 or BlobStorage, you can specify the *AccessTier* parameter.</span></span> <span data-ttu-id="f23da-136">Wenn das Speicherkonto eine Art Speicher ist, geben Sie den *AccessTier* -Parameter nicht an.</span><span class="sxs-lookup"><span data-stu-id="f23da-136">If the Storage account has Kind as Storage, do not specify the *AccessTier* parameter.</span></span>

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

### <span data-ttu-id="f23da-137">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f23da-137">-AsJob</span></span>
<span data-ttu-id="f23da-138">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="f23da-138">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f23da-139">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="f23da-139">-AssignIdentity</span></span>
<span data-ttu-id="f23da-140">Generieren und Zuweisen einer neuen Speicherkonto Identität für dieses Speicherkonto für die Verwendung mit Schlüssel Verwaltungsdiensten wie Azure keyvault</span><span class="sxs-lookup"><span data-stu-id="f23da-140">Generate and assign a new Storage account Identity for this Storage account for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="f23da-141">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="f23da-141">-CustomDomainName</span></span>
<span data-ttu-id="f23da-142">Gibt den Namen der benutzerdefinierten Domäne an.</span><span class="sxs-lookup"><span data-stu-id="f23da-142">Specifies the name of the custom domain.</span></span>

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

### <span data-ttu-id="f23da-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f23da-143">-DefaultProfile</span></span>
<span data-ttu-id="f23da-144">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f23da-144">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f23da-145">-EnableHttpsTrafficOnly</span><span class="sxs-lookup"><span data-stu-id="f23da-145">-EnableHttpsTrafficOnly</span></span>
<span data-ttu-id="f23da-146">Gibt an, ob das Speicherkonto nur HTTPS-Datenverkehr aktiviert.</span><span class="sxs-lookup"><span data-stu-id="f23da-146">Indicates whether or not the Storage account only enables HTTPS traffic.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f23da-147">-Force</span><span class="sxs-lookup"><span data-stu-id="f23da-147">-Force</span></span>
<span data-ttu-id="f23da-148">Erzwingt, dass die Änderung in das Speicherkonto geschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="f23da-148">Forces the change to be written to the Storage account.</span></span>

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

### <span data-ttu-id="f23da-149">-KeyName</span><span class="sxs-lookup"><span data-stu-id="f23da-149">-KeyName</span></span>
<span data-ttu-id="f23da-150">Wenn Sie-KeyvaultEncryption verwenden, um die Verschlüsselung mit Key Vault zu aktivieren, geben Sie die KeyName-Eigenschaft mit dieser Option an.</span><span class="sxs-lookup"><span data-stu-id="f23da-150">If using -KeyvaultEncryption to enable encryption with Key Vault, specify the Keyname property with this option.</span></span>

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

### <span data-ttu-id="f23da-151">-KeyvaultEncryption</span><span class="sxs-lookup"><span data-stu-id="f23da-151">-KeyvaultEncryption</span></span>
<span data-ttu-id="f23da-152">Gibt an, ob Sie Microsoft keyvault für die Verschlüsselungsschlüssel verwenden möchten, wenn Sie die Speicherdienst Verschlüsselung verwenden.</span><span class="sxs-lookup"><span data-stu-id="f23da-152">Indicates whether or not to use Microsoft KeyVault for the encryption keys when using Storage Service Encryption.</span></span> <span data-ttu-id="f23da-153">Wenn keyName, keyversion und KeyVaultUri eingestellt sind, wird keySource auf Microsoft. keyvault festgesetzt, ob dieser Parameter festgesetzt ist oder nicht.</span><span class="sxs-lookup"><span data-stu-id="f23da-153">If KeyName, KeyVersion, and KeyVaultUri are all set, KeySource will be set to Microsoft.Keyvault whether this parameter is set or not.</span></span> 

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

### <span data-ttu-id="f23da-154">-KeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="f23da-154">-KeyVaultUri</span></span>
<span data-ttu-id="f23da-155">Verwenden Sie bei Verwendung der Schlüssel Vault-Verschlüsselung durch Angabe des-KeyvaultEncryption-Parameters diese Option, um den URI für den schlüsseltresor anzugeben.</span><span class="sxs-lookup"><span data-stu-id="f23da-155">When using Key Vault Encryption by specifying the -KeyvaultEncryption parameter, use this option to specify the URI to the Key Vault.</span></span>

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

### <span data-ttu-id="f23da-156">-Keyversion</span><span class="sxs-lookup"><span data-stu-id="f23da-156">-KeyVersion</span></span>
<span data-ttu-id="f23da-157">Verwenden Sie bei Verwendung der Schlüssel Vault-Verschlüsselung durch Angabe des-KeyvaultEncryption-Parameters diese Option, um den URI für die Schlüssel Version anzugeben.</span><span class="sxs-lookup"><span data-stu-id="f23da-157">When using Key Vault Encryption by specifying the -KeyvaultEncryption parameter, use this option to specify the URI to the Key Version.</span></span>

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

### <span data-ttu-id="f23da-158">-Name</span><span class="sxs-lookup"><span data-stu-id="f23da-158">-Name</span></span>
<span data-ttu-id="f23da-159">Gibt den Namen des zu ändernden speicherkontos an.</span><span class="sxs-lookup"><span data-stu-id="f23da-159">Specifies the name of the Storage account to modify.</span></span>

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

### <span data-ttu-id="f23da-160">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="f23da-160">-NetworkRuleSet</span></span>
<span data-ttu-id="f23da-161">NetworkRuleSet wird verwendet, um eine Reihe von Konfigurationsregeln für Firewalls und virtuelle Netzwerke zu definieren sowie Werte für Netzwerkeigenschaften festzulegen, beispielsweise Dienste, die die Regeln umgehen dürfen, und die Behandlung von Anforderungen, die keiner der definierten Regeln entsprechen.</span><span class="sxs-lookup"><span data-stu-id="f23da-161">NetworkRuleSet is used to define a set of configuration rules for firewalls and virtual networks, as well as to set values for network properties such as services allowed to bypass the rules and how to handle requests that don't match any of the defined rules.</span></span>

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

### <span data-ttu-id="f23da-162">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f23da-162">-ResourceGroupName</span></span>
<span data-ttu-id="f23da-163">Gibt den Namen der Ressourcengruppe an, in der das Speicherkonto geändert werden soll.</span><span class="sxs-lookup"><span data-stu-id="f23da-163">Specifies the name of the resource group in which to modify the Storage account.</span></span>

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

### <span data-ttu-id="f23da-164">-SkuName</span><span class="sxs-lookup"><span data-stu-id="f23da-164">-SkuName</span></span>
<span data-ttu-id="f23da-165">Gibt den SKU-Namen des speicherkontos an.</span><span class="sxs-lookup"><span data-stu-id="f23da-165">Specifies the SKU name of the Storage account.</span></span>
<span data-ttu-id="f23da-166">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="f23da-166">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="f23da-167">Standard_LRS-lokal redundanter Speicherplatz.</span><span class="sxs-lookup"><span data-stu-id="f23da-167">Standard_LRS - Locally-redundant storage.</span></span>
- <span data-ttu-id="f23da-168">Standard_ZRS Zone – redundanter Speicherplatz.</span><span class="sxs-lookup"><span data-stu-id="f23da-168">Standard_ZRS - Zone-redundant storage.</span></span>
- <span data-ttu-id="f23da-169">Standard_GRS-Geo-redundanter Speicher.</span><span class="sxs-lookup"><span data-stu-id="f23da-169">Standard_GRS - Geo-redundant storage.</span></span>
- <span data-ttu-id="f23da-170">Standard_RAGRS Lesezugriff Geo-redundanter Speicher.</span><span class="sxs-lookup"><span data-stu-id="f23da-170">Standard_RAGRS - Read access geo-redundant storage.</span></span>
- <span data-ttu-id="f23da-171">Premium_LRS-Premium-lokal redundanter Speicherplatz.</span><span class="sxs-lookup"><span data-stu-id="f23da-171">Premium_LRS - Premium locally-redundant storage.</span></span>
<span data-ttu-id="f23da-172">Standard_ZRS-und Premium_LRS Typen können nicht in andere Kontotypen geändert werden.</span><span class="sxs-lookup"><span data-stu-id="f23da-172">You cannot change Standard_ZRS and Premium_LRS types to other account types.</span></span>
<span data-ttu-id="f23da-173">Sie können andere Kontotypen nicht in Standard_ZRS oder Premium_LRS ändern.</span><span class="sxs-lookup"><span data-stu-id="f23da-173">You cannot change other account types to Standard_ZRS or Premium_LRS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountType, AccountType, Type
Accepted values: Standard_LRS, Standard_ZRS, Standard_GRS, Standard_RAGRS, Premium_LRS

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f23da-174">-StorageEncryption</span><span class="sxs-lookup"><span data-stu-id="f23da-174">-StorageEncryption</span></span>
<span data-ttu-id="f23da-175">Gibt an, ob die Speicherkonto Verschlüsselung für die Verwendung von Microsoft-verwalteten Schlüsseln festgesetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="f23da-175">Indicates whether or not to set the Storage account encryption to use Microsoft-managed keys.</span></span>

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

### <span data-ttu-id="f23da-176">-Tag</span><span class="sxs-lookup"><span data-stu-id="f23da-176">-Tag</span></span>
<span data-ttu-id="f23da-177">Schlüssel-Wert-Paare in Form einer Hashtabelle, die als Tags auf dem Server definiert ist.</span><span class="sxs-lookup"><span data-stu-id="f23da-177">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="f23da-178">Beispiel: @ {Key0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="f23da-178">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="f23da-179">-UpgradeToStorageV2</span><span class="sxs-lookup"><span data-stu-id="f23da-179">-UpgradeToStorageV2</span></span>
<span data-ttu-id="f23da-180">Upgrade des speicherkontos Art von Speicher-oder BlobStorage auf StorageV2.</span><span class="sxs-lookup"><span data-stu-id="f23da-180">Upgrade Storage account Kind from  Storage or BlobStorage to StorageV2.</span></span>

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

### <span data-ttu-id="f23da-181">-UseSubDomain</span><span class="sxs-lookup"><span data-stu-id="f23da-181">-UseSubDomain</span></span>
<span data-ttu-id="f23da-182">Gibt an, ob die indirekte CNAME-Validierung aktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="f23da-182">Indicates whether to enable indirect CName validation.</span></span>

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

### <span data-ttu-id="f23da-183">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f23da-183">-Confirm</span></span>
<span data-ttu-id="f23da-184">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f23da-184">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f23da-185">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f23da-185">-WhatIf</span></span>
<span data-ttu-id="f23da-186">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f23da-186">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f23da-187">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f23da-187">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f23da-188">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f23da-188">CommonParameters</span></span>
<span data-ttu-id="f23da-189">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f23da-189">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f23da-190">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f23da-190">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f23da-191">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f23da-191">INPUTS</span></span>

### <span data-ttu-id="f23da-192">System. String</span><span class="sxs-lookup"><span data-stu-id="f23da-192">System.String</span></span>

### <span data-ttu-id="f23da-193">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="f23da-193">System.Collections.Hashtable</span></span>

### <span data-ttu-id="f23da-194">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f23da-194">System.Boolean</span></span>

## <span data-ttu-id="f23da-195">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f23da-195">OUTPUTS</span></span>

### <span data-ttu-id="f23da-196">Microsoft. Azure. Commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f23da-196">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="f23da-197">Notizen</span><span class="sxs-lookup"><span data-stu-id="f23da-197">NOTES</span></span>

## <span data-ttu-id="f23da-198">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f23da-198">RELATED LINKS</span></span>

[<span data-ttu-id="f23da-199">Get-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f23da-199">Get-AzureRmStorageAccount</span></span>](./Get-AzureRmStorageAccount.md)

[<span data-ttu-id="f23da-200">Neu – AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f23da-200">New-AzureRmStorageAccount</span></span>](./New-AzureRmStorageAccount.md)

[<span data-ttu-id="f23da-201">Remove-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f23da-201">Remove-AzureRmStorageAccount</span></span>](./Remove-AzureRmStorageAccount.md)
