---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/undo-azkeyvaultkeyremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultKeyRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultKeyRemoval.md
ms.openlocfilehash: c2b4fec2524ed3ddac62cf687af33ba3f76f13e8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93846048"
---
# <span data-ttu-id="18d07-101">Undo-AzKeyVaultKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="18d07-101">Undo-AzKeyVaultKeyRemoval</span></span>

## <span data-ttu-id="18d07-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="18d07-102">SYNOPSIS</span></span>
<span data-ttu-id="18d07-103">Stellt einen gelöschten Schlüssel in einem schlüsseltresor in einen aktiven Zustand.</span><span class="sxs-lookup"><span data-stu-id="18d07-103">Recovers a deleted key in a key vault into an active state.</span></span>

## <span data-ttu-id="18d07-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="18d07-104">SYNTAX</span></span>

### <span data-ttu-id="18d07-105">Standard (Standard)</span><span class="sxs-lookup"><span data-stu-id="18d07-105">Default (Default)</span></span>
```
Undo-AzKeyVaultKeyRemoval [-VaultName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="18d07-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="18d07-106">InputObject</span></span>
```
Undo-AzKeyVaultKeyRemoval [-InputObject] <PSDeletedKeyVaultKeyIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="18d07-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="18d07-107">DESCRIPTION</span></span>
<span data-ttu-id="18d07-108">Mit dem Cmdlet **"Undo-AzKeyVaultKeyRemoval"** wird ein zuvor gelöschter Schlüssel wiederhergestellt.</span><span class="sxs-lookup"><span data-stu-id="18d07-108">The **Undo-AzKeyVaultKeyRemoval** cmdlet will recover a previously deleted key.</span></span>
<span data-ttu-id="18d07-109">Der wiederhergestellte Schlüssel ist aktiv und kann für alle normalen Schlüsselvorgänge verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="18d07-109">The recovered key will be active and can be used for all normal key operations.</span></span>
<span data-ttu-id="18d07-110">Der Aufrufer muss über die Berechtigung "Wiederherstellen" verfügen, um diesen Vorgang ausführen zu können.</span><span class="sxs-lookup"><span data-stu-id="18d07-110">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="18d07-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="18d07-111">EXAMPLES</span></span>

### <span data-ttu-id="18d07-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="18d07-112">Example 1</span></span>
```powershell
PS C:\> Undo-AzKeyVaultKeyRemoval -VaultName 'MyKeyVault' -Name 'MyKey'

Vault Name     : MyKeyVault
Name           : MyKey
Version        : 1af807cc331a49d0b52b7c75e1b2366e
Id             : https://mykeybault.vault.azure.net:443/keys/mykey/1af807cc331a49d0b52b7c75e1b2366e
Enabled        : True
Expires        :
Not Before     :
Created        : 5/24/2018 8:32:27 PM
Updated        : 5/24/2018 8:32:27 PM
Purge Disabled : False
Tags           :
```

<span data-ttu-id="18d07-113">Mit diesem Befehl wird der zuvor gelöschte Schlüssel "MyKey" wieder in einen aktiven und nutzbaren Zustand versetzt.</span><span class="sxs-lookup"><span data-stu-id="18d07-113">This command will recover the key 'MyKey' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="18d07-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="18d07-114">PARAMETERS</span></span>

### <span data-ttu-id="18d07-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18d07-115">-DefaultProfile</span></span>
<span data-ttu-id="18d07-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="18d07-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="18d07-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="18d07-117">-InputObject</span></span>
<span data-ttu-id="18d07-118">Gelöschtes Schlüsselobjekt</span><span class="sxs-lookup"><span data-stu-id="18d07-118">Deleted key object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKeyIdentityItem
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="18d07-119">-Name</span><span class="sxs-lookup"><span data-stu-id="18d07-119">-Name</span></span>
<span data-ttu-id="18d07-120">Schlüsselname.</span><span class="sxs-lookup"><span data-stu-id="18d07-120">Key name.</span></span>
<span data-ttu-id="18d07-121">Cmdlet erstellt den FQDN eines Schlüssels aus Vault-Name, aktuell ausgewählter Umgebung und Schlüsselname.</span><span class="sxs-lookup"><span data-stu-id="18d07-121">Cmdlet constructs the FQDN of a key from vault name, currently selected environment and key name.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18d07-122">-Vaultname</span><span class="sxs-lookup"><span data-stu-id="18d07-122">-VaultName</span></span>
<span data-ttu-id="18d07-123">Vault-Name.</span><span class="sxs-lookup"><span data-stu-id="18d07-123">Vault name.</span></span>
<span data-ttu-id="18d07-124">Cmdlet erstellt den FQDN eines Tresors basierend auf dem Namen und der aktuell ausgewählten Umgebung.</span><span class="sxs-lookup"><span data-stu-id="18d07-124">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18d07-125">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="18d07-125">-Confirm</span></span>
<span data-ttu-id="18d07-126">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="18d07-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="18d07-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="18d07-127">-WhatIf</span></span>
<span data-ttu-id="18d07-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="18d07-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="18d07-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="18d07-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="18d07-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18d07-130">CommonParameters</span></span>
<span data-ttu-id="18d07-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="18d07-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18d07-132">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="18d07-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18d07-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="18d07-133">INPUTS</span></span>

### <span data-ttu-id="18d07-134">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="18d07-134">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKeyIdentityItem</span></span>

## <span data-ttu-id="18d07-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="18d07-135">OUTPUTS</span></span>

### <span data-ttu-id="18d07-136">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="18d07-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

## <span data-ttu-id="18d07-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="18d07-137">NOTES</span></span>

## <span data-ttu-id="18d07-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="18d07-138">RELATED LINKS</span></span>

[<span data-ttu-id="18d07-139">Remove-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="18d07-139">Remove-AzKeyVaultKey</span></span>](./Remove-AzKeyVaultKey.md)

[<span data-ttu-id="18d07-140">Add-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="18d07-140">Add-AzKeyVaultKey</span></span>](./Add-AzKeyVaultKey.md)

[<span data-ttu-id="18d07-141">Get-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="18d07-141">Get-AzKeyVaultKey</span></span>](./Get-AzKeyVaultKey.md)

