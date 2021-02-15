---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/undo-azkeyvaultkeyremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultKeyRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultKeyRemoval.md
ms.openlocfilehash: d6637b8c180dd2ef25bdba5326f0a42a364bc8ab
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100152684"
---
# <span data-ttu-id="f17f0-101">Undo-AzKeyVaultKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="f17f0-101">Undo-AzKeyVaultKeyRemoval</span></span>

## <span data-ttu-id="f17f0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f17f0-102">SYNOPSIS</span></span>
<span data-ttu-id="f17f0-103">Stellt einen gelöschten Schlüssel in einem Schlüsseltresor in einen aktiven Zustand wiederher.</span><span class="sxs-lookup"><span data-stu-id="f17f0-103">Recovers a deleted key in a key vault into an active state.</span></span>

## <span data-ttu-id="f17f0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f17f0-104">SYNTAX</span></span>

### <span data-ttu-id="f17f0-105">Standard (Standard)</span><span class="sxs-lookup"><span data-stu-id="f17f0-105">Default (Default)</span></span>
```
Undo-AzKeyVaultKeyRemoval [-VaultName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f17f0-106">HsmInteractive</span><span class="sxs-lookup"><span data-stu-id="f17f0-106">HsmInteractive</span></span>
```
Undo-AzKeyVaultKeyRemoval -HsmName <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f17f0-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="f17f0-107">InputObject</span></span>
```
Undo-AzKeyVaultKeyRemoval [-InputObject] <PSDeletedKeyVaultKeyIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f17f0-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f17f0-108">DESCRIPTION</span></span>
<span data-ttu-id="f17f0-109">Das **Cmdlet "Undo-AzKeyVaultKeyRemoval"** stellt einen zuvor gelöschten Schlüssel wiederher.</span><span class="sxs-lookup"><span data-stu-id="f17f0-109">The **Undo-AzKeyVaultKeyRemoval** cmdlet will recover a previously deleted key.</span></span>
<span data-ttu-id="f17f0-110">Der wiederhergestellte Schlüssel ist aktiv und kann für alle normalen Schlüsselvorgänge verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f17f0-110">The recovered key will be active and can be used for all normal key operations.</span></span>
<span data-ttu-id="f17f0-111">Der Aufrufer muss über die Berechtigung "Wiederherstellen" verfügen, um diesen Vorgang ausführen zu können.</span><span class="sxs-lookup"><span data-stu-id="f17f0-111">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="f17f0-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f17f0-112">EXAMPLES</span></span>

### <span data-ttu-id="f17f0-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f17f0-113">Example 1</span></span>
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

<span data-ttu-id="f17f0-114">Mit diesem Befehl wird der zuvor gelöschte Schlüssel "MyKey" in einen aktiven und verwendbaren Zustand wiederhergestellt.</span><span class="sxs-lookup"><span data-stu-id="f17f0-114">This command will recover the key 'MyKey' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="f17f0-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f17f0-115">PARAMETERS</span></span>

### <span data-ttu-id="f17f0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f17f0-116">-DefaultProfile</span></span>
<span data-ttu-id="f17f0-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="f17f0-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f17f0-118">-HsmName</span><span class="sxs-lookup"><span data-stu-id="f17f0-118">-HsmName</span></span>
<span data-ttu-id="f17f0-119">HSM-Name.</span><span class="sxs-lookup"><span data-stu-id="f17f0-119">HSM name.</span></span> <span data-ttu-id="f17f0-120">Das Cmdlet erstellt den FQDN eines verwalteten HSM basierend auf dem Namen und der aktuell ausgewählten Umgebung.</span><span class="sxs-lookup"><span data-stu-id="f17f0-120">Cmdlet constructs the FQDN of a managed HSM based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: HsmInteractive
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f17f0-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f17f0-121">-InputObject</span></span>
<span data-ttu-id="f17f0-122">Gelöschtes Schlüsselobjekt</span><span class="sxs-lookup"><span data-stu-id="f17f0-122">Deleted key object</span></span>

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

### <span data-ttu-id="f17f0-123">-Name</span><span class="sxs-lookup"><span data-stu-id="f17f0-123">-Name</span></span>
<span data-ttu-id="f17f0-124">Schlüsselname.</span><span class="sxs-lookup"><span data-stu-id="f17f0-124">Key name.</span></span>
<span data-ttu-id="f17f0-125">Das Cmdlet erstellt den FQDN eines Schlüssels aus dem Namen des Tresors, der aktuell ausgewählte Umgebung und schlüsselname.</span><span class="sxs-lookup"><span data-stu-id="f17f0-125">Cmdlet constructs the FQDN of a key from vault name, currently selected environment and key name.</span></span>

```yaml
Type: System.String
Parameter Sets: Default, HsmInteractive
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f17f0-126">-VaultName</span><span class="sxs-lookup"><span data-stu-id="f17f0-126">-VaultName</span></span>
<span data-ttu-id="f17f0-127">Name des Tresors.</span><span class="sxs-lookup"><span data-stu-id="f17f0-127">Vault name.</span></span>
<span data-ttu-id="f17f0-128">Das Cmdlet erstellt den FQDN eines Tresors basierend auf dem Namen und der aktuell ausgewählten Umgebung.</span><span class="sxs-lookup"><span data-stu-id="f17f0-128">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="f17f0-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f17f0-129">-Confirm</span></span>
<span data-ttu-id="f17f0-130">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f17f0-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f17f0-131">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="f17f0-131">-WhatIf</span></span>
<span data-ttu-id="f17f0-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f17f0-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f17f0-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f17f0-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f17f0-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f17f0-134">CommonParameters</span></span>
<span data-ttu-id="f17f0-135">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f17f0-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f17f0-136">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f17f0-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f17f0-137">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f17f0-137">INPUTS</span></span>

### <span data-ttu-id="f17f0-138">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="f17f0-138">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKeyIdentityItem</span></span>

## <span data-ttu-id="f17f0-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f17f0-139">OUTPUTS</span></span>

### <span data-ttu-id="f17f0-140">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="f17f0-140">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

## <span data-ttu-id="f17f0-141">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="f17f0-141">NOTES</span></span>

## <span data-ttu-id="f17f0-142">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="f17f0-142">RELATED LINKS</span></span>

[<span data-ttu-id="f17f0-143">Remove-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="f17f0-143">Remove-AzKeyVaultKey</span></span>](./Remove-AzKeyVaultKey.md)

[<span data-ttu-id="f17f0-144">Add-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="f17f0-144">Add-AzKeyVaultKey</span></span>](./Add-AzKeyVaultKey.md)

[<span data-ttu-id="f17f0-145">Get-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="f17f0-145">Get-AzKeyVaultKey</span></span>](./Get-AzKeyVaultKey.md)

