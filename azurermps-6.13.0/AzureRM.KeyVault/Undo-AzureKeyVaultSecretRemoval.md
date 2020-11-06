---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/undo-azurekeyvaultsecretremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Undo-AzureKeyVaultSecretRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Undo-AzureKeyVaultSecretRemoval.md
ms.openlocfilehash: ecc22deb6be4f8fe85b66454091f6bfbd01d3a80
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496034"
---
# <span data-ttu-id="bf012-101">Undo-AzureKeyVaultSecretRemoval</span><span class="sxs-lookup"><span data-stu-id="bf012-101">Undo-AzureKeyVaultSecretRemoval</span></span>

## <span data-ttu-id="bf012-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="bf012-102">SYNOPSIS</span></span>
<span data-ttu-id="bf012-103">Stellt ein gelöschtes Geheimnis in einem schlüsseltresor in einen aktiven Zustand.</span><span class="sxs-lookup"><span data-stu-id="bf012-103">Recovers a deleted secret in a key vault into an active state.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bf012-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="bf012-104">SYNTAX</span></span>

### <span data-ttu-id="bf012-105">Standard (Standard)</span><span class="sxs-lookup"><span data-stu-id="bf012-105">Default (Default)</span></span>
```
Undo-AzureKeyVaultSecretRemoval [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bf012-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="bf012-106">InputObject</span></span>
```
Undo-AzureKeyVaultSecretRemoval [-InputObject] <PSDeletedKeyVaultSecretIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bf012-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bf012-107">DESCRIPTION</span></span>
<span data-ttu-id="bf012-108">Mit dem Cmdlet **"Undo-AzureKeyVaultSecretRemoval"** wird ein zuvor gelöschter Schlüssel wiederhergestellt.</span><span class="sxs-lookup"><span data-stu-id="bf012-108">The **Undo-AzureKeyVaultSecretRemoval** cmdlet will recover a previously deleted secret.</span></span>
<span data-ttu-id="bf012-109">Der wiederhergestellte Schlüssel ist aktiv und kann für alle normalen geheimen Vorgänge verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="bf012-109">The recovered secret will be active and can be used for all normal secret operations.</span></span>
<span data-ttu-id="bf012-110">Der Aufrufer muss über die Berechtigung "Wiederherstellen" verfügen, um diesen Vorgang ausführen zu können.</span><span class="sxs-lookup"><span data-stu-id="bf012-110">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="bf012-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="bf012-111">EXAMPLES</span></span>

### <span data-ttu-id="bf012-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="bf012-112">Example 1</span></span>
```powershell
PS C:\> Undo-AzureKeyVaultSecretRemoval -VaultName 'MyKeyVault' -Name 'MySecret'

Vault Name   : MyKeyVault
Name         : MySecret
Version      : f622abc7b1394092812f1eb0f85dc91c
Id           : https://mykeyvault.vault.azure.net:443/secrets/mysecret/f622abc7b1394092812f1eb0f85dc91c
Enabled      : True
Expires      :
Not Before   :
Created      : 4/19/2018 5:56:02 PM
Updated      : 4/26/2018 7:48:40 PM
Content Type :
Tags         :
```

<span data-ttu-id="bf012-113">Mit diesem Befehl wird der zuvor gelöschte Geheimtipp "MySecret" in einen aktiven und nutzbaren Zustand zurückgestellt.</span><span class="sxs-lookup"><span data-stu-id="bf012-113">This command will recover the secret 'MySecret' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="bf012-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="bf012-114">PARAMETERS</span></span>

### <span data-ttu-id="bf012-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf012-115">-DefaultProfile</span></span>
<span data-ttu-id="bf012-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="bf012-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bf012-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="bf012-117">-InputObject</span></span>
<span data-ttu-id="bf012-118">Geheimes Objekt gelöscht</span><span class="sxs-lookup"><span data-stu-id="bf012-118">Deleted secret object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecretIdentityItem
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bf012-119">-Name</span><span class="sxs-lookup"><span data-stu-id="bf012-119">-Name</span></span>
<span data-ttu-id="bf012-120">Geheimer Name.</span><span class="sxs-lookup"><span data-stu-id="bf012-120">Secret name.</span></span>
<span data-ttu-id="bf012-121">Cmdlet erstellt den FQDN eines geheimen Schlüssels aus Vault-Name, aktuell ausgewählter Umgebung und geheimem Namen.</span><span class="sxs-lookup"><span data-stu-id="bf012-121">Cmdlet constructs the FQDN of a secret from vault name, currently selected environment and secret name.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf012-122">-Vaultname</span><span class="sxs-lookup"><span data-stu-id="bf012-122">-VaultName</span></span>
<span data-ttu-id="bf012-123">Vault-Name.</span><span class="sxs-lookup"><span data-stu-id="bf012-123">Vault name.</span></span>
<span data-ttu-id="bf012-124">Cmdlet erstellt den FQDN eines Tresors basierend auf dem Namen und der aktuell ausgewählten Umgebung.</span><span class="sxs-lookup"><span data-stu-id="bf012-124">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="bf012-125">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="bf012-125">-Confirm</span></span>
<span data-ttu-id="bf012-126">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="bf012-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bf012-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bf012-127">-WhatIf</span></span>
<span data-ttu-id="bf012-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="bf012-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bf012-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="bf012-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bf012-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf012-130">CommonParameters</span></span>
<span data-ttu-id="bf012-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bf012-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf012-132">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bf012-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf012-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="bf012-133">INPUTS</span></span>

### <span data-ttu-id="bf012-134">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecretIdentityItem</span><span class="sxs-lookup"><span data-stu-id="bf012-134">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecretIdentityItem</span></span>
<span data-ttu-id="bf012-135">Parameter: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="bf012-135">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="bf012-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="bf012-136">OUTPUTS</span></span>

### <span data-ttu-id="bf012-137">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="bf012-137">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret</span></span>

## <span data-ttu-id="bf012-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="bf012-138">NOTES</span></span>

## <span data-ttu-id="bf012-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="bf012-139">RELATED LINKS</span></span>

[<span data-ttu-id="bf012-140">Remove-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="bf012-140">Remove-AzureKeyVaultSecret</span></span>](./Remove-AzureKeyVaultSecret.md)

[<span data-ttu-id="bf012-141">Add-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="bf012-141">Add-AzureKeyVaultSecret</span></span>](./Add-AzureKeyVaultSecret.md)

[<span data-ttu-id="bf012-142">Get-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="bf012-142">Get-AzureKeyVaultSecret</span></span>](./Get-AzureKeyVaultSecret.md)
