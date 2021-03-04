---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/update-azstorageencryptionscope
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageEncryptionScope.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageEncryptionScope.md
ms.openlocfilehash: 153165406fd02561dbece79e18558065ff34c8f9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101929248"
---
# <span data-ttu-id="39c53-101">Update-AzStorageEncryptionScope</span><span class="sxs-lookup"><span data-stu-id="39c53-101">Update-AzStorageEncryptionScope</span></span>

## <span data-ttu-id="39c53-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="39c53-102">SYNOPSIS</span></span>
<span data-ttu-id="39c53-103">Ändern Sie einen Verschlüsselungsbereich für ein Speicherkonto.</span><span class="sxs-lookup"><span data-stu-id="39c53-103">Modify an encryption scope for a Storage account.</span></span>

## <span data-ttu-id="39c53-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="39c53-104">SYNTAX</span></span>

### <span data-ttu-id="39c53-105">AccountName (Standard)</span><span class="sxs-lookup"><span data-stu-id="39c53-105">AccountName (Default)</span></span>
```
Update-AzStorageEncryptionScope [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -EncryptionScopeName <String> [-StorageEncryption] [-State <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="39c53-106">AccountNameKeyVault</span><span class="sxs-lookup"><span data-stu-id="39c53-106">AccountNameKeyVault</span></span>
```
Update-AzStorageEncryptionScope [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -EncryptionScopeName <String> [-KeyvaultEncryption] -KeyUri <String> [-State <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="39c53-107">AccountObject</span><span class="sxs-lookup"><span data-stu-id="39c53-107">AccountObject</span></span>
```
Update-AzStorageEncryptionScope -StorageAccount <PSStorageAccount> -EncryptionScopeName <String>
 [-StorageEncryption] [-State <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="39c53-108">AccountObjectKeyVault</span><span class="sxs-lookup"><span data-stu-id="39c53-108">AccountObjectKeyVault</span></span>
```
Update-AzStorageEncryptionScope -StorageAccount <PSStorageAccount> -EncryptionScopeName <String>
 [-KeyvaultEncryption] -KeyUri <String> [-State <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="39c53-109">EncryptionScopeObject</span><span class="sxs-lookup"><span data-stu-id="39c53-109">EncryptionScopeObject</span></span>
```
Update-AzStorageEncryptionScope -InputObject <PSEncryptionScope> [-StorageEncryption] [-State <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="39c53-110">EncryptionScopeObjectKeyVault</span><span class="sxs-lookup"><span data-stu-id="39c53-110">EncryptionScopeObjectKeyVault</span></span>
```
Update-AzStorageEncryptionScope -InputObject <PSEncryptionScope> [-KeyvaultEncryption] -KeyUri <String>
 [-State <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="39c53-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="39c53-111">DESCRIPTION</span></span>
<span data-ttu-id="39c53-112">Das **Cmdlet Update-AzStorageEncryptionScope** ändert einen Verschlüsselungsbereich für ein Speicherkonto.</span><span class="sxs-lookup"><span data-stu-id="39c53-112">The **Update-AzStorageEncryptionScope** cmdlet modifies an encryption scope for a Storage account.</span></span>

## <span data-ttu-id="39c53-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="39c53-113">EXAMPLES</span></span>

### <span data-ttu-id="39c53-114">Beispiel 1: Deaktivieren eines Verschlüsselungsbereichs</span><span class="sxs-lookup"><span data-stu-id="39c53-114">Example 1: Disable an encryption scope</span></span>
```
PS C:\> Update-AzStorageEncryptionScope -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount"  -EncryptionScopeName testscope -State Disabled 

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name      State    Source            KeyVaultKeyUri RequireInfrastructureEncryption                                         
----      -----    ------            -------------- -------------------------------                                         
testscope Disabled Microsoft.Storage
```

<span data-ttu-id="39c53-115">Mit diesem Befehl wird ein Verschlüsselungsbereich deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="39c53-115">This command disables an encryption scope.</span></span>

### <span data-ttu-id="39c53-116">Beispiel 2: Aktivieren eines Verschlüsselungsbereichs</span><span class="sxs-lookup"><span data-stu-id="39c53-116">Example 2: Enable an encryption scope</span></span>
```
PS C:\> Update-AzStorageEncryptionScope -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount"  -EncryptionScopeName testscope -State Enabled 

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name      State    Source            KeyVaultKeyUri RequireInfrastructureEncryption                                                                           
----      -----    ------            -------------- -------------------------------                                                                          
testscope Enabled  Microsoft.Storage
```

<span data-ttu-id="39c53-117">Dieser Befehl aktiviert einen Verschlüsselungsbereich.</span><span class="sxs-lookup"><span data-stu-id="39c53-117">This command enables an encryption scope.</span></span>

### <span data-ttu-id="39c53-118">Beispiel 3: Aktualisieren eines Verschlüsselungsbereichs für die Verwendung der Speicherverschlüsselung</span><span class="sxs-lookup"><span data-stu-id="39c53-118">Example 3: Update an encryption scope to use Storage Encryption</span></span>
```
PS C:\> Update-AzStorageEncryptionScope -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount"  -EncryptionScopeName testscope -StorageEncryption

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name      State    Source            KeyVaultKeyUri RequireInfrastructureEncryption                                          
----      -----    ------            -------------- -------------------------------                                         
testscope Enabled  Microsoft.Storage
```

<span data-ttu-id="39c53-119">Mit diesem Befehl wird ein Verschlüsselungsbereich aktualisiert, um die Speicherverschlüsselung zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="39c53-119">This command updates an encryption scope to use Storage Encryption.</span></span>

### <span data-ttu-id="39c53-120">Beispiel 4: Aktualisieren eines Verschlüsselungsbereichs für die Verwendung der Keyvault-Verschlüsselung</span><span class="sxs-lookup"><span data-stu-id="39c53-120">Example 4: Update an encryption scope to use Keyvault Encryption</span></span>
```
PS C:\> Update-AzStorageEncryptionScope -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -EncryptionScopeName testscope -KeyvaultEncryption -KeyUri "https://keyvalutname.vault.azure.net:443/keys/keyname/34a0ba563b4243d9a0ef2b1d3c0c7d57"

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name      State    Source             KeyVaultKeyUri                                                                          RequireInfrastructureEncryption 
----      -----    ------             --------------                                                                          -------------------------------
testscope Enabled  Microsoft.Keyvault https://keyvalutname.vault.azure.net:443/keys/keyname/34a0ba563b4243d9a0ef2b1d3c0c7d57   
```

<span data-ttu-id="39c53-121">Mit diesem Befehl wird ein Verschlüsselungsbereich für die Verwendung der Keyvault-Verschlüsselung aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="39c53-121">This command updtaes an encryption scope to use Keyvault Encryption.</span></span>
<span data-ttu-id="39c53-122">Die Identität des Speicherkontos muss über die Berechtigungen "Get,wrapkey", "Unwrapkey" für den Keyvault-Schlüssel verfügen.</span><span class="sxs-lookup"><span data-stu-id="39c53-122">The Storage account Identity need have get,wrapkey,unwrapkey permissions to the keyvault key.</span></span>

## <span data-ttu-id="39c53-123">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="39c53-123">PARAMETERS</span></span>

### <span data-ttu-id="39c53-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39c53-124">-DefaultProfile</span></span>
<span data-ttu-id="39c53-125">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="39c53-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="39c53-126">-EncryptionScopeName</span><span class="sxs-lookup"><span data-stu-id="39c53-126">-EncryptionScopeName</span></span>
<span data-ttu-id="39c53-127">Azure Storage EncryptionScope Name</span><span class="sxs-lookup"><span data-stu-id="39c53-127">Azure Storage EncryptionScope name</span></span>

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

### <span data-ttu-id="39c53-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="39c53-128">-InputObject</span></span>
<span data-ttu-id="39c53-129">EncryptionScope-Objekt</span><span class="sxs-lookup"><span data-stu-id="39c53-129">EncryptionScope object</span></span>

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

### <span data-ttu-id="39c53-130">-KeyUri</span><span class="sxs-lookup"><span data-stu-id="39c53-130">-KeyUri</span></span>
<span data-ttu-id="39c53-131">Der wichtigste URI</span><span class="sxs-lookup"><span data-stu-id="39c53-131">The key Uri</span></span>

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

### <span data-ttu-id="39c53-132">-KeyvaultEncryption</span><span class="sxs-lookup"><span data-stu-id="39c53-132">-KeyvaultEncryption</span></span>
<span data-ttu-id="39c53-133">Erstellen des Verschlüsselungsbereichs mit keySource als Microsoft.Keyvault</span><span class="sxs-lookup"><span data-stu-id="39c53-133">Create encryption scope with keySource as Microsoft.Keyvault</span></span>

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

### <span data-ttu-id="39c53-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="39c53-134">-ResourceGroupName</span></span>
<span data-ttu-id="39c53-135">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="39c53-135">Resource Group Name.</span></span>

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

### <span data-ttu-id="39c53-136">-State</span><span class="sxs-lookup"><span data-stu-id="39c53-136">-State</span></span>
<span data-ttu-id="39c53-137">Update encryption scope State, Possible values include: 'Enabled', 'Disabled'.</span><span class="sxs-lookup"><span data-stu-id="39c53-137">Update encryption scope State, Possible values include: 'Enabled', 'Disabled'.</span></span>

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

### <span data-ttu-id="39c53-138">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="39c53-138">-StorageAccount</span></span>
<span data-ttu-id="39c53-139">Speicherkontoobjekt</span><span class="sxs-lookup"><span data-stu-id="39c53-139">Storage account object</span></span>

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

### <span data-ttu-id="39c53-140">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="39c53-140">-StorageAccountName</span></span>
<span data-ttu-id="39c53-141">Speicherkontoname.</span><span class="sxs-lookup"><span data-stu-id="39c53-141">Storage Account Name.</span></span>

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

### <span data-ttu-id="39c53-142">-StorageEncryption</span><span class="sxs-lookup"><span data-stu-id="39c53-142">-StorageEncryption</span></span>
<span data-ttu-id="39c53-143">Erstellen Sie den Verschlüsselungsbereich mit keySource als Microsoft.Storage.</span><span class="sxs-lookup"><span data-stu-id="39c53-143">Create encryption scope with keySource as Microsoft.Storage.</span></span>

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

### <span data-ttu-id="39c53-144">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="39c53-144">-Confirm</span></span>
<span data-ttu-id="39c53-145">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="39c53-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="39c53-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="39c53-146">-WhatIf</span></span>
<span data-ttu-id="39c53-147">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="39c53-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="39c53-148">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="39c53-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="39c53-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39c53-149">CommonParameters</span></span>
<span data-ttu-id="39c53-150">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="39c53-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39c53-151">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="39c53-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39c53-152">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="39c53-152">INPUTS</span></span>

### <span data-ttu-id="39c53-153">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="39c53-153">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="39c53-154">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="39c53-154">OUTPUTS</span></span>

### <span data-ttu-id="39c53-155">Microsoft.Azure.Commands.Management.Storage.Models.PSEncryptionScope</span><span class="sxs-lookup"><span data-stu-id="39c53-155">Microsoft.Azure.Commands.Management.Storage.Models.PSEncryptionScope</span></span>

## <span data-ttu-id="39c53-156">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="39c53-156">NOTES</span></span>

## <span data-ttu-id="39c53-157">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="39c53-157">RELATED LINKS</span></span>
