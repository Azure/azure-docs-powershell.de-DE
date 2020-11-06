---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
ms.assetid: 4D7EEDD7-89D4-4B1E-A9A1-B301E759CE72
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Set-AzureRmStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Set-AzureRmStorageAccount.md
ms.openlocfilehash: 860e87063810251075341cd1eddd013870734384
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93480750"
---
# <span data-ttu-id="502e9-101">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="502e9-101">Set-AzureRmStorageAccount</span></span>

## <span data-ttu-id="502e9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="502e9-102">SYNOPSIS</span></span>
<span data-ttu-id="502e9-103">Ändert ein Speicherkonto.</span><span class="sxs-lookup"><span data-stu-id="502e9-103">Modifies a Storage account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="502e9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="502e9-104">SYNTAX</span></span>

### <span data-ttu-id="502e9-105">StorageEncryption (Standard)</span><span class="sxs-lookup"><span data-stu-id="502e9-105">StorageEncryption (Default)</span></span>
```
Set-AzureRmStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-Force] [[-SkuName] <String>]
 [[-AccessTier] <String>] [[-CustomDomainName] <String>] [[-UseSubDomain] <Boolean>]
 [[-EnableEncryptionService] <EncryptionSupportServiceEnum>]
 [[-DisableEncryptionService] <EncryptionSupportServiceEnum>] [[-Tag] <Hashtable>]
 [-EnableHttpsTrafficOnly <Boolean>] [-StorageEncryption] [-AssignIdentity]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="502e9-106">KeyvaultEncryption</span><span class="sxs-lookup"><span data-stu-id="502e9-106">KeyvaultEncryption</span></span>
```
Set-AzureRmStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-Force] [[-SkuName] <String>]
 [[-AccessTier] <String>] [[-CustomDomainName] <String>] [[-UseSubDomain] <Boolean>]
 [[-EnableEncryptionService] <EncryptionSupportServiceEnum>]
 [[-DisableEncryptionService] <EncryptionSupportServiceEnum>] [[-Tag] <Hashtable>]
 [-EnableHttpsTrafficOnly <Boolean>] [-KeyvaultEncryption] -KeyName <String> -KeyVersion <String>
 -KeyVaultUri <String> [-AssignIdentity] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="502e9-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="502e9-107">DESCRIPTION</span></span>
<span data-ttu-id="502e9-108">Das Cmdlet " **Satz-AzureRmStorageAccount** " ändert ein Azure Storage-Konto.</span><span class="sxs-lookup"><span data-stu-id="502e9-108">The **Set-AzureRmStorageAccount** cmdlet modifies an Azure Storage account.</span></span>
<span data-ttu-id="502e9-109">Sie können dieses Cmdlet verwenden, um den Kontotyp zu ändern, eine Kundendomäne zu aktualisieren oder Tags für ein Speicherkonto einzurichten.</span><span class="sxs-lookup"><span data-stu-id="502e9-109">You can use this cmdlet to modify the account type, update a customer domain, or set tags on a Storage account.</span></span>

## <span data-ttu-id="502e9-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="502e9-110">EXAMPLES</span></span>

### <span data-ttu-id="502e9-111">Beispiel 1: Einrichten des Speicher Kontotyps</span><span class="sxs-lookup"><span data-stu-id="502e9-111">Example 1: Set the Storage account type</span></span>
```
PS C:\>Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -Type "Standard_RAGRS"
```

<span data-ttu-id="502e9-112">Dieser Befehl legt den Typ des speicherkontos auf Standard_RAGRS fest.</span><span class="sxs-lookup"><span data-stu-id="502e9-112">This command sets the Storage account type to Standard_RAGRS.</span></span>

### <span data-ttu-id="502e9-113">Beispiel 2: Einrichten einer benutzerdefinierten Domäne für ein Speicherkonto</span><span class="sxs-lookup"><span data-stu-id="502e9-113">Example 2: Set a custom domain for a Storage account</span></span>
```
PS C:\>Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -CustomDomainName "www.contoso.com" -UseSubDomain $True
```

<span data-ttu-id="502e9-114">Mit diesem Befehl wird eine benutzerdefinierte Domäne für ein Speicherkonto festgelegt.</span><span class="sxs-lookup"><span data-stu-id="502e9-114">This command sets a custom domain for a Storage account.</span></span>

### <span data-ttu-id="502e9-115">Beispiel 3: Aktivieren der Verschlüsselung für BLOB-und Dateidienste</span><span class="sxs-lookup"><span data-stu-id="502e9-115">Example 3: Enable encryption on Blob and File Services</span></span>
```
PS C:\>Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -EnableEncryptionService "Blob,File"
```

<span data-ttu-id="502e9-116">Mit diesem Befehl wird die Speicherdienst Verschlüsselung für BLOB und Datei für ein Speicherkonto aktiviert.</span><span class="sxs-lookup"><span data-stu-id="502e9-116">This command enables Storage Service encryption on Blob and File for a Storage account.</span></span>

### <span data-ttu-id="502e9-117">Beispiel 4: Einrichten des Zugriffsstufen Werts</span><span class="sxs-lookup"><span data-stu-id="502e9-117">Example 4: Set the access tier value</span></span>
```
PS C:\>Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -AccessTier Cool
```

<span data-ttu-id="502e9-118">Mit dem Befehl wird der Wert der Access-Ebene auf "cool" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="502e9-118">The command sets the Access Tier value to be cool.</span></span>

### <span data-ttu-id="502e9-119">Beispiel 4: Einrichten der benutzerdefinierten Domäne und der Tags</span><span class="sxs-lookup"><span data-stu-id="502e9-119">Example 4: Set the custom domain and tags</span></span>
```
PS C:\>Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -CustomDomainName "www.domainname.com" -UseSubDomain $true -Tag @{tag0="value0";tag1="value1";tag2="value2"}
```

<span data-ttu-id="502e9-120">Mit dem Befehl wird der Wert der Access-Ebene auf "cool" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="502e9-120">The command sets the Access Tier value to be cool.</span></span>

### <span data-ttu-id="502e9-121">Beispiel 5: Aktivieren der Verschlüsselung für BLOB-Dienste mit keyvault</span><span class="sxs-lookup"><span data-stu-id="502e9-121">Example 5: Enable encryption on Blob Services with Keyvault</span></span>
```
PS C:\>Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -AssignIdentity
PS C:\>$account = Get-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount"

PS C:\>$keyVault = New-AzureRmKeyVault -VaultName "MyKeyVault" -ResourceGroupName "MyResourceGroup" -Location "EastUS2"
PS C:\>$key = Add-AzureKeyVaultKey -VaultName "MyKeyVault" -Name "MyKey" -Destination 'Software'
PS C:\>Set-AzureRmKeyVaultAccessPolicy -VaultName "MyKeyVault" -ObjectId $account.Identity.PrincipalId -PermissionsToKeys wrapkey,unwrapkey

PS C:\>Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -EnableEncryptionService "Blob" -KeyvaultEncryption -KeyName $key.Name -KeyVersion $key.Version -KeyVaultUri $keyVault.VaultUri
```

<span data-ttu-id="502e9-122">Mit diesem Befehl wird die Speicherdienst Verschlüsselung für BLOB mit einem neu erstellten keyvault aktiviert.</span><span class="sxs-lookup"><span data-stu-id="502e9-122">This command enables Storage Service encryption on Blob with a new created Keyvault.</span></span>

### <span data-ttu-id="502e9-123">Beispiel 6: Deaktivieren Sie die Verschlüsselung für Dateidienste, wobei keySource auf "Microsoft. Storage" gesetzt ist.</span><span class="sxs-lookup"><span data-stu-id="502e9-123">Example 6: Disable encryption on File Services with KeySource set to "Microsoft.Storage"</span></span>
```
PS C:\>Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -DisableEncryptionService File  -StorageEncryption
```

<span data-ttu-id="502e9-124">Mit diesem Befehl wird die Verschlüsselung für Dateidienste deaktiviert, wobei keySource auf "Microsoft. Storage" gesetzt ist.</span><span class="sxs-lookup"><span data-stu-id="502e9-124">This command disables encryption on File Services with KeySource set to "Microsoft.Storage"</span></span>

## <span data-ttu-id="502e9-125">Parameter</span><span class="sxs-lookup"><span data-stu-id="502e9-125">PARAMETERS</span></span>

### <span data-ttu-id="502e9-126">-AccessTier</span><span class="sxs-lookup"><span data-stu-id="502e9-126">-AccessTier</span></span>
<span data-ttu-id="502e9-127">Gibt die Zugriffsebene des speicherkontos an, das von diesem Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="502e9-127">Specifies the access tier of the Storage account that this cmdlet modifies.</span></span>
<span data-ttu-id="502e9-128">Die akzeptablen Werte für diesen Parameter sind: heiß und cool.</span><span class="sxs-lookup"><span data-stu-id="502e9-128">The acceptable values for this parameter are: Hot and Cool.</span></span>

<span data-ttu-id="502e9-129">Wenn Sie die Zugriffsebene ändern, kann dies zu zusätzlichen Gebühren führen.</span><span class="sxs-lookup"><span data-stu-id="502e9-129">If you change the access tier, it may result in additional charges.</span></span>
<span data-ttu-id="502e9-130">Weitere Informationen finden Sie unter Azure-BLOB-Speicher: heiße und kühle Speicherebenen https://go.microsoft.com/fwlink/?LinkId=786482 ( https://go.microsoft.com/fwlink/?LinkId=786482) .</span><span class="sxs-lookup"><span data-stu-id="502e9-130">For more information, see Azure Blob Storage: Hot and cool storage tiershttps://go.microsoft.com/fwlink/?LinkId=786482 (https://go.microsoft.com/fwlink/?LinkId=786482).</span></span>
<span data-ttu-id="502e9-131">Wenn die Art des speicherkontos Speicher ist, geben Sie diesen Parameter nicht an.</span><span class="sxs-lookup"><span data-stu-id="502e9-131">If the kind of Storage account is Storage, do not specify this parameter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="502e9-132">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="502e9-132">-AssignIdentity</span></span>
<span data-ttu-id="502e9-133">Generieren und Zuweisen einer neuen Speicherkonto Identität für dieses Speicherkonto für die Verwendung mit Schlüssel Verwaltungsdiensten wie Azure keyvault</span><span class="sxs-lookup"><span data-stu-id="502e9-133">Generate and assign a new Storage Account Identity for this storage account for use with key management services like Azure KeyVault.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="502e9-134">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="502e9-134">-CustomDomainName</span></span>
<span data-ttu-id="502e9-135">Gibt den Namen der benutzerdefinierten Domäne an.</span><span class="sxs-lookup"><span data-stu-id="502e9-135">Specifies the name of the custom domain.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="502e9-136">-DisableEncryptionService</span><span class="sxs-lookup"><span data-stu-id="502e9-136">-DisableEncryptionService</span></span>
<span data-ttu-id="502e9-137">Gibt an, ob dieses Cmdlet die Speicherdienst Verschlüsselung für den Speicherdienst deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="502e9-137">Indicates whether this cmdlet disables Storage Service encryption on the Storage Service.</span></span>
<span data-ttu-id="502e9-138">Azure-BLOB-und Azure-Dateidienste werden unterstützt.</span><span class="sxs-lookup"><span data-stu-id="502e9-138">Azure Blob and Azure File Services are supported.</span></span>

```yaml
Type: EncryptionSupportServiceEnum
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="502e9-139">-EnableEncryptionService</span><span class="sxs-lookup"><span data-stu-id="502e9-139">-EnableEncryptionService</span></span>
<span data-ttu-id="502e9-140">Gibt an, ob dieses Cmdlet Speicherdienst Verschlüsselung für den Speicherdienst aktiviert.</span><span class="sxs-lookup"><span data-stu-id="502e9-140">Indicates whether this cmdlet enables Storage Service encryption on the Storage Service.</span></span>
<span data-ttu-id="502e9-141">Azure-BLOB-und Azure-Dateidienste werden unterstützt.</span><span class="sxs-lookup"><span data-stu-id="502e9-141">Azure Blob and Azure File Services are supported.</span></span>

```yaml
Type: EncryptionSupportServiceEnum
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="502e9-142">-EnableHttpsTrafficOnly</span><span class="sxs-lookup"><span data-stu-id="502e9-142">-EnableHttpsTrafficOnly</span></span>
<span data-ttu-id="502e9-143">Gibt an, ob das Speicherkonto nur HTTPS-Datenverkehr aktiviert.</span><span class="sxs-lookup"><span data-stu-id="502e9-143">Indicates whether or not the Storage Account only enable https traffic.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="502e9-144">-Force</span><span class="sxs-lookup"><span data-stu-id="502e9-144">-Force</span></span>
<span data-ttu-id="502e9-145">Wenn Sie die Zugriffsebene ändern, kann dies zu zusätzlichen Gebühren führen.</span><span class="sxs-lookup"><span data-stu-id="502e9-145">If you change the access tier, it may result in additional charges.</span></span>
<span data-ttu-id="502e9-146">Weitere Informationen finden Sie unter Azure-BLOB-Speicher: heiße und kühle Speicherebenen https://go.microsoft.com/fwlink/?LinkId=786482 ( https://go.microsoft.com/fwlink/?LinkId=786482) .</span><span class="sxs-lookup"><span data-stu-id="502e9-146">For more information, see Azure Blob Storage: Hot and cool storage tiershttps://go.microsoft.com/fwlink/?LinkId=786482 (https://go.microsoft.com/fwlink/?LinkId=786482).</span></span>
<span data-ttu-id="502e9-147">Wenn die Art des speicherkontos Speicher ist, geben Sie diesen Parameter nicht an.</span><span class="sxs-lookup"><span data-stu-id="502e9-147">If the kind of Storage account is Storage, do not specify this parameter.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="502e9-148">-Information</span><span class="sxs-lookup"><span data-stu-id="502e9-148">-InformationAction</span></span>
<span data-ttu-id="502e9-149">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="502e9-149">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="502e9-150">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="502e9-150">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="502e9-151">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="502e9-151">Continue</span></span>
- <span data-ttu-id="502e9-152">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="502e9-152">Ignore</span></span>
- <span data-ttu-id="502e9-153">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="502e9-153">Inquire</span></span>
- <span data-ttu-id="502e9-154">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="502e9-154">SilentlyContinue</span></span>
- <span data-ttu-id="502e9-155">Beenden</span><span class="sxs-lookup"><span data-stu-id="502e9-155">Stop</span></span>
- <span data-ttu-id="502e9-156">Anhalten</span><span class="sxs-lookup"><span data-stu-id="502e9-156">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="502e9-157">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="502e9-157">-InformationVariable</span></span>
<span data-ttu-id="502e9-158">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="502e9-158">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="502e9-159">-KeyName</span><span class="sxs-lookup"><span data-stu-id="502e9-159">-KeyName</span></span>
<span data-ttu-id="502e9-160">Speicherkonto Verschlüsselung keyvault-keyvault-keyName</span><span class="sxs-lookup"><span data-stu-id="502e9-160">Storage Account encryption keySource KeyVault KeyName</span></span>

```yaml
Type: String
Parameter Sets: KeyvaultEncryption
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="502e9-161">-KeyvaultEncryption</span><span class="sxs-lookup"><span data-stu-id="502e9-161">-KeyvaultEncryption</span></span>
<span data-ttu-id="502e9-162">Gibt an, ob die Schlüsselquelle für die Speicherkonto Verschlüsselung auf Microsoft. keyvault festgesetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="502e9-162">Whether to set Storage Account Encryption KeySource to Microsoft.Keyvault or not.</span></span>
<span data-ttu-id="502e9-163">Wenn Sie keyName, keyversion und KeyvaultUri angeben, wird die Schlüsselquelle für die Speicherkonto Verschlüsselung ebenfalls auf Microsoft festgelegt. keyvault-Wetter dieser Parameter ist festgelegt oder nicht.</span><span class="sxs-lookup"><span data-stu-id="502e9-163">If you specify KeyName, KeyVersion and KeyvaultUri, Storage Account encryption keySource will also be set to Microsoft.Keyvault weather this parameter is set or not.</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: KeyvaultEncryption
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="502e9-164">-KeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="502e9-164">-KeyVaultUri</span></span>
<span data-ttu-id="502e9-165">Speicherkonto Verschlüsselung keyvault KeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="502e9-165">Storage Account encryption keySource KeyVault KeyVaultUri</span></span>

```yaml
Type: String
Parameter Sets: KeyvaultEncryption
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="502e9-166">-Keyversion</span><span class="sxs-lookup"><span data-stu-id="502e9-166">-KeyVersion</span></span>
<span data-ttu-id="502e9-167">Speicherkonto Verschlüsselung keyvault keyvault-keyversion</span><span class="sxs-lookup"><span data-stu-id="502e9-167">Storage Account encryption keySource KeyVault KeyVersion</span></span>

```yaml
Type: String
Parameter Sets: KeyvaultEncryption
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="502e9-168">-Name</span><span class="sxs-lookup"><span data-stu-id="502e9-168">-Name</span></span>
<span data-ttu-id="502e9-169">Gibt den Namen des zu ändernden speicherkontos an.</span><span class="sxs-lookup"><span data-stu-id="502e9-169">Specifies the name of the Storage account to Modify.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="502e9-170">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="502e9-170">-ResourceGroupName</span></span>
<span data-ttu-id="502e9-171">Gibt den Namen der Ressourcengruppe an, in der das Speicherkonto geändert werden soll.</span><span class="sxs-lookup"><span data-stu-id="502e9-171">Specifies the name of the resource group in which to modify the Storage account.</span></span>

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

### <span data-ttu-id="502e9-172">-SkuName</span><span class="sxs-lookup"><span data-stu-id="502e9-172">-SkuName</span></span>
<span data-ttu-id="502e9-173">Gibt den SKU-Namen des speicherkontos an.</span><span class="sxs-lookup"><span data-stu-id="502e9-173">Specifies the SKU name of the storage account.</span></span>
<span data-ttu-id="502e9-174">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="502e9-174">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="502e9-175">Standard_LRS.</span><span class="sxs-lookup"><span data-stu-id="502e9-175">Standard_LRS.</span></span>
<span data-ttu-id="502e9-176">Lokal redundanter Speicherplatz.</span><span class="sxs-lookup"><span data-stu-id="502e9-176">Locally-redundant storage.</span></span>
- <span data-ttu-id="502e9-177">Standard_ZRS.</span><span class="sxs-lookup"><span data-stu-id="502e9-177">Standard_ZRS.</span></span>
<span data-ttu-id="502e9-178">Zone – redundanter Speicher.</span><span class="sxs-lookup"><span data-stu-id="502e9-178">Zone-redundant storage.</span></span>
- <span data-ttu-id="502e9-179">Standard_GRS.</span><span class="sxs-lookup"><span data-stu-id="502e9-179">Standard_GRS.</span></span>
<span data-ttu-id="502e9-180">Geo-redundanter Speicher.</span><span class="sxs-lookup"><span data-stu-id="502e9-180">Geo-redundant storage.</span></span>
- <span data-ttu-id="502e9-181">Standard_RAGRS.</span><span class="sxs-lookup"><span data-stu-id="502e9-181">Standard_RAGRS.</span></span>
<span data-ttu-id="502e9-182">Lesezugriff Geo-redundanter Speicher.</span><span class="sxs-lookup"><span data-stu-id="502e9-182">Read access geo-redundant storage.</span></span>
- <span data-ttu-id="502e9-183">Premium_LRS.</span><span class="sxs-lookup"><span data-stu-id="502e9-183">Premium_LRS.</span></span>
<span data-ttu-id="502e9-184">Premium-lokal redundanter Speicherplatz.</span><span class="sxs-lookup"><span data-stu-id="502e9-184">Premium locally-redundant storage.</span></span>

<span data-ttu-id="502e9-185">Standard_ZRS-und Premium_LRS Typen können nicht in andere Kontotypen geändert werden.</span><span class="sxs-lookup"><span data-stu-id="502e9-185">You cannot change Standard_ZRS and Premium_LRS types to other account types.</span></span>
<span data-ttu-id="502e9-186">Sie können andere Kontotypen nicht in Standard_ZRS oder Premium_LRS ändern.</span><span class="sxs-lookup"><span data-stu-id="502e9-186">You cannot change other account types to Standard_ZRS or Premium_LRS.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: StorageAccountType, AccountType, Type

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="502e9-187">-StorageEncryption</span><span class="sxs-lookup"><span data-stu-id="502e9-187">-StorageEncryption</span></span>
<span data-ttu-id="502e9-188">Gibt an, ob die Schlüsselquelle für die Speicherkonto Verschlüsselung auf Microsoft. Storage festgesetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="502e9-188">Whether to set Storage Account Encryption KeySource to Microsoft.Storage or not.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: StorageEncryption
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="502e9-189">-Tag</span><span class="sxs-lookup"><span data-stu-id="502e9-189">-Tag</span></span>
<span data-ttu-id="502e9-190">Wenn Sie einen Wert von BlobStorage für den Parameter *Art* des New-AzureRmStorageAccount-Cmdlets angeben, müssen Sie einen Wert für den *AccessTier* -Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="502e9-190">If you specify a value of BlobStorage for the *Kind* parameter of the New-AzureRmStorageAccount cmdlet, you must specify a value for the *AccessTier* parameter.</span></span>

<span data-ttu-id="502e9-191">Wenn Sie einen Wert für Storage für diesen *Art* -Parameter angeben, geben Sie den *AccessTier* -Parameter nicht an.</span><span class="sxs-lookup"><span data-stu-id="502e9-191">If you specify a value of Storage for this *Kind* parameter, do not specify the *AccessTier* parameter.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="502e9-192">-UseSubDomain</span><span class="sxs-lookup"><span data-stu-id="502e9-192">-UseSubDomain</span></span>
<span data-ttu-id="502e9-193">Gibt an, ob die indirekte CNAME-Validierung aktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="502e9-193">Indicates whether to enable indirect CName validation.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="502e9-194">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="502e9-194">-Confirm</span></span>
<span data-ttu-id="502e9-195">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="502e9-195">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="502e9-196">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="502e9-196">-WhatIf</span></span>
<span data-ttu-id="502e9-197">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="502e9-197">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="502e9-198">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="502e9-198">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="502e9-199">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="502e9-199">CommonParameters</span></span>
<span data-ttu-id="502e9-200">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="502e9-200">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="502e9-201">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="502e9-201">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="502e9-202">Eingaben</span><span class="sxs-lookup"><span data-stu-id="502e9-202">INPUTS</span></span>

### <span data-ttu-id="502e9-203">Keine</span><span class="sxs-lookup"><span data-stu-id="502e9-203">None</span></span>
<span data-ttu-id="502e9-204">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="502e9-204">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="502e9-205">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="502e9-205">OUTPUTS</span></span>

## <span data-ttu-id="502e9-206">Notizen</span><span class="sxs-lookup"><span data-stu-id="502e9-206">NOTES</span></span>

## <span data-ttu-id="502e9-207">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="502e9-207">RELATED LINKS</span></span>

[<span data-ttu-id="502e9-208">Get-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="502e9-208">Get-AzureRmStorageAccount</span></span>](./Get-AzureRmStorageAccount.md)

[<span data-ttu-id="502e9-209">Neu – AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="502e9-209">New-AzureRmStorageAccount</span></span>](./New-AzureRmStorageAccount.md)

[<span data-ttu-id="502e9-210">Remove-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="502e9-210">Remove-AzureRmStorageAccount</span></span>](./Remove-AzureRmStorageAccount.md)
