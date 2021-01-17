---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstorageencryptionscope
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageEncryptionScope.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageEncryptionScope.md
ms.openlocfilehash: 011bdd96d69ae73ca62145b85f6e636751f8eb9f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98460252"
---
# <span data-ttu-id="9e3e4-101">New-AzStorageEncryptionScope</span><span class="sxs-lookup"><span data-stu-id="9e3e4-101">New-AzStorageEncryptionScope</span></span>

## <span data-ttu-id="9e3e4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9e3e4-102">SYNOPSIS</span></span>
<span data-ttu-id="9e3e4-103">Erstellt einen Verschlüsselungsbereich für ein Speicherkonto.</span><span class="sxs-lookup"><span data-stu-id="9e3e4-103">Creates an encryption scope for a Storage account.</span></span>

## <span data-ttu-id="9e3e4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9e3e4-104">SYNTAX</span></span>

### <span data-ttu-id="9e3e4-105">AccountName (Standard)</span><span class="sxs-lookup"><span data-stu-id="9e3e4-105">AccountName (Default)</span></span>
```
New-AzStorageEncryptionScope [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -EncryptionScopeName <String> [-StorageEncryption] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9e3e4-106">AccountNameKeyVault</span><span class="sxs-lookup"><span data-stu-id="9e3e4-106">AccountNameKeyVault</span></span>
```
New-AzStorageEncryptionScope [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -EncryptionScopeName <String> [-KeyvaultEncryption] -KeyUri <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9e3e4-107">AccountObject</span><span class="sxs-lookup"><span data-stu-id="9e3e4-107">AccountObject</span></span>
```
New-AzStorageEncryptionScope -StorageAccount <PSStorageAccount> -EncryptionScopeName <String>
 [-StorageEncryption] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9e3e4-108">AccountObjectKeyVault</span><span class="sxs-lookup"><span data-stu-id="9e3e4-108">AccountObjectKeyVault</span></span>
```
New-AzStorageEncryptionScope -StorageAccount <PSStorageAccount> -EncryptionScopeName <String>
 [-KeyvaultEncryption] -KeyUri <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9e3e4-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9e3e4-109">DESCRIPTION</span></span>
<span data-ttu-id="9e3e4-110">Das **Cmdlet "New-AzStorageEncryptionScope"** erstellt einen Verschlüsselungsbereich für ein Speicherkonto.</span><span class="sxs-lookup"><span data-stu-id="9e3e4-110">The **New-AzStorageEncryptionScope** cmdlet creates an encryption scope for a Storage account.</span></span>

## <span data-ttu-id="9e3e4-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="9e3e4-111">EXAMPLES</span></span>

### <span data-ttu-id="9e3e4-112">Beispiel 1: Erstellen eines Verschlüsselungsbereichs mit Speicherverschlüsselung</span><span class="sxs-lookup"><span data-stu-id="9e3e4-112">Example 1: Create an encryption scope with Storage Encryption</span></span>
```
PS C:\> New-AzStorageEncryptionScope -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount"  -EncryptionScopeName testscope -StorageEncryption

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name      State    Source            KeyVaultKeyUri                                         
----      -----    ------            --------------                                         
testscope Enabled  Microsoft.Storage
```

<span data-ttu-id="9e3e4-113">Dieser Befehl erstellt einen Verschlüsselungsbereich mit Speicherverschlüsselung.</span><span class="sxs-lookup"><span data-stu-id="9e3e4-113">This command creates an encryption scope with Storage Encryption.</span></span>

### <span data-ttu-id="9e3e4-114">Beispiel 2: Erstellen eines Verschlüsselungsbereichs mit der Schlüsselvaultverschlüsselung</span><span class="sxs-lookup"><span data-stu-id="9e3e4-114">Example 2: Create an encryption scope with Keyvault Encryption</span></span>
```
PS C:\> New-AzStorageEncryptionScope -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -EncryptionScopeName testscope -KeyvaultEncryption -KeyUri "https://keyvalutname.vault.azure.net:443/keys/keyname/34a0ba563b4243d9a0ef2b1d3c0c7d57"

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name      State    Source             KeyVaultKeyUri                                         
----      -----    ------             --------------                                         
testscope Enabled  Microsoft.Keyvault https://keyvalutname.vault.azure.net:443/keys/keyname/34a0ba563b4243d9a0ef2b1d3c0c7d57
```

<span data-ttu-id="9e3e4-115">Dieser Befehl erstellt einen Verschlüsselungsbereich mit Keyvault Encryption.</span><span class="sxs-lookup"><span data-stu-id="9e3e4-115">This command creates an encryption scope with Keyvault Encryption.</span></span>
<span data-ttu-id="9e3e4-116">Die Speicherkontoidentität muss die Berechtigungen "get,wrapkey", "unwrapkey" und "keyvault" besitzen.</span><span class="sxs-lookup"><span data-stu-id="9e3e4-116">The Storage account Identity need have get,wrapkey,unwrapkey permissions to the keyvault key.</span></span>

## <span data-ttu-id="9e3e4-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9e3e4-117">PARAMETERS</span></span>

### <span data-ttu-id="9e3e4-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e3e4-118">-DefaultProfile</span></span>
<span data-ttu-id="9e3e4-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9e3e4-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9e3e4-120">-EncryptionScopeName</span><span class="sxs-lookup"><span data-stu-id="9e3e4-120">-EncryptionScopeName</span></span>
<span data-ttu-id="9e3e4-121">Azure Storage EncryptionScope-Name</span><span class="sxs-lookup"><span data-stu-id="9e3e4-121">Azure Storage EncryptionScope name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e3e4-122">-KeyUri</span><span class="sxs-lookup"><span data-stu-id="9e3e4-122">-KeyUri</span></span>
<span data-ttu-id="9e3e4-123">Der Schlüssel-URI</span><span class="sxs-lookup"><span data-stu-id="9e3e4-123">The key Uri</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNameKeyVault, AccountObjectKeyVault
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e3e4-124">-KeyvaultEncryption</span><span class="sxs-lookup"><span data-stu-id="9e3e4-124">-KeyvaultEncryption</span></span>
<span data-ttu-id="9e3e4-125">Erstellen des Verschlüsselungsbereichs mit keySource als Microsoft.Keyvault</span><span class="sxs-lookup"><span data-stu-id="9e3e4-125">Create encryption scope with keySource as Microsoft.Keyvault</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AccountNameKeyVault, AccountObjectKeyVault
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e3e4-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e3e4-126">-ResourceGroupName</span></span>
<span data-ttu-id="9e3e4-127">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="9e3e4-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="9e3e4-128">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="9e3e4-128">-StorageAccount</span></span>
<span data-ttu-id="9e3e4-129">Speicherkontoobjekt</span><span class="sxs-lookup"><span data-stu-id="9e3e4-129">Storage account object</span></span>

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

### <span data-ttu-id="9e3e4-130">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="9e3e4-130">-StorageAccountName</span></span>
<span data-ttu-id="9e3e4-131">Speicherkontoname.</span><span class="sxs-lookup"><span data-stu-id="9e3e4-131">Storage Account Name.</span></span>

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

### <span data-ttu-id="9e3e4-132">-StorageEncryption</span><span class="sxs-lookup"><span data-stu-id="9e3e4-132">-StorageEncryption</span></span>
<span data-ttu-id="9e3e4-133">Erstellen Sie einen Verschlüsselungsbereich mit "keySource" als "Microsoft.Storage".</span><span class="sxs-lookup"><span data-stu-id="9e3e4-133">Create encryption scope with keySource as Microsoft.Storage.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AccountName, AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e3e4-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9e3e4-134">-Confirm</span></span>
<span data-ttu-id="9e3e4-135">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9e3e4-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9e3e4-136">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="9e3e4-136">-WhatIf</span></span>
<span data-ttu-id="9e3e4-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9e3e4-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9e3e4-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9e3e4-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9e3e4-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e3e4-139">CommonParameters</span></span>
<span data-ttu-id="9e3e4-140">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e3e4-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e3e4-141">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9e3e4-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e3e4-142">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="9e3e4-142">INPUTS</span></span>

### <span data-ttu-id="9e3e4-143">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="9e3e4-143">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="9e3e4-144">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="9e3e4-144">OUTPUTS</span></span>

### <span data-ttu-id="9e3e4-145">Microsoft.Azure.Commands.Management.Storage.Models.PSEncryptionScope</span><span class="sxs-lookup"><span data-stu-id="9e3e4-145">Microsoft.Azure.Commands.Management.Storage.Models.PSEncryptionScope</span></span>

## <span data-ttu-id="9e3e4-146">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="9e3e4-146">NOTES</span></span>

## <span data-ttu-id="9e3e4-147">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="9e3e4-147">RELATED LINKS</span></span>
