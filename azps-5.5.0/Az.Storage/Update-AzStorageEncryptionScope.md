---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/update-azstorageencryptionscope
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageEncryptionScope.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageEncryptionScope.md
ms.openlocfilehash: 6c8f07cbdb70b84d235afa7ce953da0bac477f55
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100164705"
---
# <span data-ttu-id="b2115-101">Update-AzStorageEncryptionScope</span><span class="sxs-lookup"><span data-stu-id="b2115-101">Update-AzStorageEncryptionScope</span></span>

## <span data-ttu-id="b2115-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b2115-102">SYNOPSIS</span></span>
<span data-ttu-id="b2115-103">Ändern Sie einen Verschlüsselungsbereich für ein Speicherkonto.</span><span class="sxs-lookup"><span data-stu-id="b2115-103">Modify an encryption scope for a Storage account.</span></span>

## <span data-ttu-id="b2115-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b2115-104">SYNTAX</span></span>

### <span data-ttu-id="b2115-105">AccountName (Standard)</span><span class="sxs-lookup"><span data-stu-id="b2115-105">AccountName (Default)</span></span>
```
Update-AzStorageEncryptionScope [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -EncryptionScopeName <String> [-StorageEncryption] [-State <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b2115-106">AccountNameKeyVault</span><span class="sxs-lookup"><span data-stu-id="b2115-106">AccountNameKeyVault</span></span>
```
Update-AzStorageEncryptionScope [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -EncryptionScopeName <String> [-KeyvaultEncryption] -KeyUri <String> [-State <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b2115-107">AccountObject</span><span class="sxs-lookup"><span data-stu-id="b2115-107">AccountObject</span></span>
```
Update-AzStorageEncryptionScope -StorageAccount <PSStorageAccount> -EncryptionScopeName <String>
 [-StorageEncryption] [-State <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b2115-108">AccountObjectKeyVault</span><span class="sxs-lookup"><span data-stu-id="b2115-108">AccountObjectKeyVault</span></span>
```
Update-AzStorageEncryptionScope -StorageAccount <PSStorageAccount> -EncryptionScopeName <String>
 [-KeyvaultEncryption] -KeyUri <String> [-State <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b2115-109">EncryptionScopeObject</span><span class="sxs-lookup"><span data-stu-id="b2115-109">EncryptionScopeObject</span></span>
```
Update-AzStorageEncryptionScope -InputObject <PSEncryptionScope> [-StorageEncryption] [-State <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b2115-110">EncryptionScopeObjectKeyVault</span><span class="sxs-lookup"><span data-stu-id="b2115-110">EncryptionScopeObjectKeyVault</span></span>
```
Update-AzStorageEncryptionScope -InputObject <PSEncryptionScope> [-KeyvaultEncryption] -KeyUri <String>
 [-State <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b2115-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b2115-111">DESCRIPTION</span></span>
<span data-ttu-id="b2115-112">Das **Cmdlet "Update-AzStorageEncryptionScope"** ändert einen Verschlüsselungsbereich für ein Speicherkonto.</span><span class="sxs-lookup"><span data-stu-id="b2115-112">The **Update-AzStorageEncryptionScope** cmdlet modifies an encryption scope for a Storage account.</span></span>

## <span data-ttu-id="b2115-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b2115-113">EXAMPLES</span></span>

### <span data-ttu-id="b2115-114">Beispiel 1: Deaktivieren eines Verschlüsselungsbereichs</span><span class="sxs-lookup"><span data-stu-id="b2115-114">Example 1: Disable an encryption scope</span></span>
```
PS C:\> Update-AzStorageEncryptionScope -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount"  -EncryptionScopeName testscope -State Disabled 

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name      State    Source            KeyVaultKeyUri                                                                          
----      -----    ------            --------------                                                                          
testscope Disabled Microsoft.Storage
```

<span data-ttu-id="b2115-115">Mit diesem Befehl wird ein Verschlüsselungsbereich deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="b2115-115">This command disables an encryption scope.</span></span>

### <span data-ttu-id="b2115-116">Beispiel 2: Aktivieren eines Verschlüsselungsbereichs</span><span class="sxs-lookup"><span data-stu-id="b2115-116">Example 2: Enable an encryption scope</span></span>
```
PS C:\> Update-AzStorageEncryptionScope -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount"  -EncryptionScopeName testscope -State Enabled 

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name      State    Source            KeyVaultKeyUri                                                                          
----      -----    ------            --------------                                                                          
testscope Enabled  Microsoft.Storage
```

<span data-ttu-id="b2115-117">Dieser Befehl aktiviert einen Verschlüsselungsbereich.</span><span class="sxs-lookup"><span data-stu-id="b2115-117">This command enables an encryption scope.</span></span>

### <span data-ttu-id="b2115-118">Beispiel 3: Aktualisieren eines Verschlüsselungsbereichs für die Verwendung der Speicherverschlüsselung</span><span class="sxs-lookup"><span data-stu-id="b2115-118">Example 3: Update an encryption scope to use Storage Encryption</span></span>
```
PS C:\> Update-AzStorageEncryptionScope -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount"  -EncryptionScopeName testscope -StorageEncryption

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name      State    Source            KeyVaultKeyUri                                         
----      -----    ------            --------------                                         
testscope Enabled  Microsoft.Storage
```

<span data-ttu-id="b2115-119">Mit diesem Befehl wird ein Verschlüsselungsbereich aktualisiert, um die Speicherverschlüsselung zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="b2115-119">This command updates an encryption scope to use Storage Encryption.</span></span>

### <span data-ttu-id="b2115-120">Beispiel 4: Aktualisieren eines Verschlüsselungsbereichs für die Verwendung der Schlüsselvaultverschlüsselung</span><span class="sxs-lookup"><span data-stu-id="b2115-120">Example 4: Update an encryption scope to use Keyvault Encryption</span></span>
```
PS C:\> Update-AzStorageEncryptionScope -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -EncryptionScopeName testscope -KeyvaultEncryption -KeyUri "https://keyvalutname.vault.azure.net:443/keys/keyname/34a0ba563b4243d9a0ef2b1d3c0c7d57"

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name      State    Source             KeyVaultKeyUri                                         
----      -----    ------             --------------                                         
testscope Enabled  Microsoft.Keyvault https://keyvalutname.vault.azure.net:443/keys/keyname/34a0ba563b4243d9a0ef2b1d3c0c7d57
```

<span data-ttu-id="b2115-121">Mit diesem Befehl wird ein Verschlüsselungsbereich für die Verwendung der Keyvault Encryption aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="b2115-121">This command updtaes an encryption scope to use Keyvault Encryption.</span></span>
<span data-ttu-id="b2115-122">Die Speicherkontoidentität muss die Berechtigungen "get,wrapkey", "unwrapkey" und "keyvault" besitzen.</span><span class="sxs-lookup"><span data-stu-id="b2115-122">The Storage account Identity need have get,wrapkey,unwrapkey permissions to the keyvault key.</span></span>

## <span data-ttu-id="b2115-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b2115-123">PARAMETERS</span></span>

### <span data-ttu-id="b2115-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2115-124">-DefaultProfile</span></span>
<span data-ttu-id="b2115-125">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b2115-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b2115-126">-EncryptionScopeName</span><span class="sxs-lookup"><span data-stu-id="b2115-126">-EncryptionScopeName</span></span>
<span data-ttu-id="b2115-127">Azure Storage EncryptionScope-Name</span><span class="sxs-lookup"><span data-stu-id="b2115-127">Azure Storage EncryptionScope name</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountNameKeyVault, AccountObject, AccountObjectKeyVault
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2115-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b2115-128">-InputObject</span></span>
<span data-ttu-id="b2115-129">Objekt "EncryptionScope"</span><span class="sxs-lookup"><span data-stu-id="b2115-129">EncryptionScope object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSEncryptionScope
Parameter Sets: EncryptionScopeObject, EncryptionScopeObjectKeyVault
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b2115-130">-KeyUri</span><span class="sxs-lookup"><span data-stu-id="b2115-130">-KeyUri</span></span>
<span data-ttu-id="b2115-131">Der Schlüssel-URI</span><span class="sxs-lookup"><span data-stu-id="b2115-131">The key Uri</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNameKeyVault, AccountObjectKeyVault, EncryptionScopeObjectKeyVault
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2115-132">-KeyvaultEncryption</span><span class="sxs-lookup"><span data-stu-id="b2115-132">-KeyvaultEncryption</span></span>
<span data-ttu-id="b2115-133">Erstellen eines Verschlüsselungsbereichs mit keySource als Microsoft.Keyvault</span><span class="sxs-lookup"><span data-stu-id="b2115-133">Create encryption scope with keySource as Microsoft.Keyvault</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AccountNameKeyVault, AccountObjectKeyVault, EncryptionScopeObjectKeyVault
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2115-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b2115-134">-ResourceGroupName</span></span>
<span data-ttu-id="b2115-135">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="b2115-135">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountNameKeyVault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2115-136">-State</span><span class="sxs-lookup"><span data-stu-id="b2115-136">-State</span></span>
<span data-ttu-id="b2115-137">"Status des Verschlüsselungsbereichs aktualisieren", mögliche Werte: "Enabled", "Disabled".</span><span class="sxs-lookup"><span data-stu-id="b2115-137">Update encryption scope State, Possible values include: 'Enabled', 'Disabled'.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2115-138">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="b2115-138">-StorageAccount</span></span>
<span data-ttu-id="b2115-139">Speicherkontoobjekt</span><span class="sxs-lookup"><span data-stu-id="b2115-139">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject, AccountObjectKeyVault
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b2115-140">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="b2115-140">-StorageAccountName</span></span>
<span data-ttu-id="b2115-141">Name des Speicherkontos.</span><span class="sxs-lookup"><span data-stu-id="b2115-141">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountNameKeyVault
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2115-142">-StorageEncryption</span><span class="sxs-lookup"><span data-stu-id="b2115-142">-StorageEncryption</span></span>
<span data-ttu-id="b2115-143">Erstellen Sie einen Verschlüsselungsbereich mit "keySource" als "Microsoft.Storage".</span><span class="sxs-lookup"><span data-stu-id="b2115-143">Create encryption scope with keySource as Microsoft.Storage.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AccountName, AccountObject, EncryptionScopeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2115-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b2115-144">-Confirm</span></span>
<span data-ttu-id="b2115-145">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b2115-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b2115-146">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="b2115-146">-WhatIf</span></span>
<span data-ttu-id="b2115-147">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b2115-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b2115-148">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b2115-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b2115-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2115-149">CommonParameters</span></span>
<span data-ttu-id="b2115-150">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2115-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2115-151">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b2115-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2115-152">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b2115-152">INPUTS</span></span>

### <span data-ttu-id="b2115-153">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b2115-153">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="b2115-154">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b2115-154">OUTPUTS</span></span>

### <span data-ttu-id="b2115-155">Microsoft.Azure.Commands.Management.Storage.Models.PSEncryptionScope</span><span class="sxs-lookup"><span data-stu-id="b2115-155">Microsoft.Azure.Commands.Management.Storage.Models.PSEncryptionScope</span></span>

## <span data-ttu-id="b2115-156">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="b2115-156">NOTES</span></span>

## <span data-ttu-id="b2115-157">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="b2115-157">RELATED LINKS</span></span>
