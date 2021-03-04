---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/new-azstorageencryptionscope
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageEncryptionScope.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageEncryptionScope.md
ms.openlocfilehash: ab2750bff8ccc3f53761671455bc50fe3ec154d5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101944507"
---
# <span data-ttu-id="57391-101">New-AzStorageEncryptionScope</span><span class="sxs-lookup"><span data-stu-id="57391-101">New-AzStorageEncryptionScope</span></span>

## <span data-ttu-id="57391-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="57391-102">SYNOPSIS</span></span>
<span data-ttu-id="57391-103">Erstellt einen Verschlüsselungsbereich für ein Speicherkonto.</span><span class="sxs-lookup"><span data-stu-id="57391-103">Creates an encryption scope for a Storage account.</span></span>

## <span data-ttu-id="57391-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="57391-104">SYNTAX</span></span>

### <span data-ttu-id="57391-105">AccountName (Standard)</span><span class="sxs-lookup"><span data-stu-id="57391-105">AccountName (Default)</span></span>
```
New-AzStorageEncryptionScope [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -EncryptionScopeName <String> [-StorageEncryption] [-RequireInfrastructureEncryption]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="57391-106">AccountNameKeyVault</span><span class="sxs-lookup"><span data-stu-id="57391-106">AccountNameKeyVault</span></span>
```
New-AzStorageEncryptionScope [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -EncryptionScopeName <String> [-KeyvaultEncryption] -KeyUri <String> [-RequireInfrastructureEncryption]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="57391-107">AccountObject</span><span class="sxs-lookup"><span data-stu-id="57391-107">AccountObject</span></span>
```
New-AzStorageEncryptionScope -StorageAccount <PSStorageAccount> -EncryptionScopeName <String>
 [-StorageEncryption] [-RequireInfrastructureEncryption] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="57391-108">AccountObjectKeyVault</span><span class="sxs-lookup"><span data-stu-id="57391-108">AccountObjectKeyVault</span></span>
```
New-AzStorageEncryptionScope -StorageAccount <PSStorageAccount> -EncryptionScopeName <String>
 [-KeyvaultEncryption] -KeyUri <String> [-RequireInfrastructureEncryption]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="57391-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="57391-109">DESCRIPTION</span></span>
<span data-ttu-id="57391-110">Das **Cmdlet New-AzStorageEncryptionScope** erstellt einen Verschlüsselungsbereich für ein Speicherkonto.</span><span class="sxs-lookup"><span data-stu-id="57391-110">The **New-AzStorageEncryptionScope** cmdlet creates an encryption scope for a Storage account.</span></span>

## <span data-ttu-id="57391-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="57391-111">EXAMPLES</span></span>

### <span data-ttu-id="57391-112">Beispiel 1: Erstellen eines Verschlüsselungsbereichs mit Speicherverschlüsselung</span><span class="sxs-lookup"><span data-stu-id="57391-112">Example 1: Create an encryption scope with Storage Encryption</span></span>
```
PS C:\> New-AzStorageEncryptionScope -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount"  -EncryptionScopeName testscope -StorageEncryption

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name      State    Source            KeyVaultKeyUri RequireInfrastructureEncryption                                         
----      -----    ------            -------------- -------------------------------                                         
testscope Enabled  Microsoft.Storage
```

<span data-ttu-id="57391-113">Mit diesem Befehl wird ein Verschlüsselungsbereich mit Speicherverschlüsselung erstellt.</span><span class="sxs-lookup"><span data-stu-id="57391-113">This command creates an encryption scope with Storage Encryption.</span></span>

### <span data-ttu-id="57391-114">Beispiel 2: Erstellen eines Verschlüsselungsbereichs mit Keyvault Encryption und RequireInfrastructureEncryption</span><span class="sxs-lookup"><span data-stu-id="57391-114">Example 2: Create an encryption scope with Keyvault Encryption, and RequireInfrastructureEncryption</span></span>
```
PS C:\> New-AzStorageEncryptionScope -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" `
    -EncryptionScopeName testscope -KeyvaultEncryption -KeyUri "https://keyvalutname.vault.azure.net:443/keys/keyname/34a0ba563b4243d9a0ef2b1d3c0c7d57" `
    -RequireInfrastructureEncryption 

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name         State   Source           KeyVaultKeyUri                                                                          RequireInfrastructureEncryption                                       
----         -----   ------             --------------                                                                        -------------------------------                                     
testscope Enabled  Microsoft.Keyvault https://keyvalutname.vault.azure.net:443/keys/keyname/34a0ba563b4243d9a0ef2b1d3c0c7d57  True 
```

<span data-ttu-id="57391-115">Mit diesem Befehl wird ein Verschlüsselungsbereich mit Keyvault Encryption und RequireInfrastructureEncryption erstellt.</span><span class="sxs-lookup"><span data-stu-id="57391-115">This command creates an encryption scope with Keyvault Encryption and RequireInfrastructureEncryption.</span></span>
<span data-ttu-id="57391-116">Die Identität des Speicherkontos muss über die Berechtigungen "Get,wrapkey", "Unwrapkey" für den Keyvault-Schlüssel verfügen.</span><span class="sxs-lookup"><span data-stu-id="57391-116">The Storage account Identity need have get,wrapkey,unwrapkey permissions to the keyvault key.</span></span>

## <span data-ttu-id="57391-117">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="57391-117">PARAMETERS</span></span>

### <span data-ttu-id="57391-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57391-118">-DefaultProfile</span></span>
<span data-ttu-id="57391-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="57391-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="57391-120">-EncryptionScopeName</span><span class="sxs-lookup"><span data-stu-id="57391-120">-EncryptionScopeName</span></span>
<span data-ttu-id="57391-121">Azure Storage EncryptionScope Name</span><span class="sxs-lookup"><span data-stu-id="57391-121">Azure Storage EncryptionScope name</span></span>

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

### <span data-ttu-id="57391-122">-KeyUri</span><span class="sxs-lookup"><span data-stu-id="57391-122">-KeyUri</span></span>
<span data-ttu-id="57391-123">Der wichtigste URI</span><span class="sxs-lookup"><span data-stu-id="57391-123">The key Uri</span></span>

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

### <span data-ttu-id="57391-124">-KeyvaultEncryption</span><span class="sxs-lookup"><span data-stu-id="57391-124">-KeyvaultEncryption</span></span>
<span data-ttu-id="57391-125">Erstellen des Verschlüsselungsbereichs mit keySource als Microsoft.Keyvault</span><span class="sxs-lookup"><span data-stu-id="57391-125">Create encryption scope with keySource as Microsoft.Keyvault</span></span>

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

### <span data-ttu-id="57391-126">-RequireInfrastructureEncryption</span><span class="sxs-lookup"><span data-stu-id="57391-126">-RequireInfrastructureEncryption</span></span>
<span data-ttu-id="57391-127">Der Verschlüsselungsbereich verwendet eine sekundäre Verschlüsselungsebene mit plattform verwalteten Schlüsseln für ruhende Daten.</span><span class="sxs-lookup"><span data-stu-id="57391-127">The encryption scope will apply a secondary layer of encryption with platform managed keys for data at rest.</span></span>

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

### <span data-ttu-id="57391-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="57391-128">-ResourceGroupName</span></span>
<span data-ttu-id="57391-129">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="57391-129">Resource Group Name.</span></span>

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

### <span data-ttu-id="57391-130">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="57391-130">-StorageAccount</span></span>
<span data-ttu-id="57391-131">Speicherkontoobjekt</span><span class="sxs-lookup"><span data-stu-id="57391-131">Storage account object</span></span>

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

### <span data-ttu-id="57391-132">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="57391-132">-StorageAccountName</span></span>
<span data-ttu-id="57391-133">Speicherkontoname.</span><span class="sxs-lookup"><span data-stu-id="57391-133">Storage Account Name.</span></span>

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

### <span data-ttu-id="57391-134">-StorageEncryption</span><span class="sxs-lookup"><span data-stu-id="57391-134">-StorageEncryption</span></span>
<span data-ttu-id="57391-135">Erstellen Sie den Verschlüsselungsbereich mit keySource als Microsoft.Storage.</span><span class="sxs-lookup"><span data-stu-id="57391-135">Create encryption scope with keySource as Microsoft.Storage.</span></span>

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

### <span data-ttu-id="57391-136">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="57391-136">-Confirm</span></span>
<span data-ttu-id="57391-137">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="57391-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="57391-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="57391-138">-WhatIf</span></span>
<span data-ttu-id="57391-139">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="57391-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="57391-140">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="57391-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="57391-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57391-141">CommonParameters</span></span>
<span data-ttu-id="57391-142">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57391-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57391-143">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="57391-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57391-144">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="57391-144">INPUTS</span></span>

### <span data-ttu-id="57391-145">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="57391-145">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="57391-146">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="57391-146">OUTPUTS</span></span>

### <span data-ttu-id="57391-147">Microsoft.Azure.Commands.Management.Storage.Models.PSEncryptionScope</span><span class="sxs-lookup"><span data-stu-id="57391-147">Microsoft.Azure.Commands.Management.Storage.Models.PSEncryptionScope</span></span>

## <span data-ttu-id="57391-148">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="57391-148">NOTES</span></span>

## <span data-ttu-id="57391-149">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="57391-149">RELATED LINKS</span></span>
