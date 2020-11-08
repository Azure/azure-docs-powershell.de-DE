---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/undo-azkeyvaultsecretremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultSecretRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultSecretRemoval.md
ms.openlocfilehash: 1eca5a380dc71a5bd801c21bb7e7f556fcff0d35
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94175487"
---
# <span data-ttu-id="57cc2-101">Undo-AzKeyVaultSecretRemoval</span><span class="sxs-lookup"><span data-stu-id="57cc2-101">Undo-AzKeyVaultSecretRemoval</span></span>

## <span data-ttu-id="57cc2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="57cc2-102">SYNOPSIS</span></span>
<span data-ttu-id="57cc2-103">Stellt ein gelöschtes Geheimnis in einem schlüsseltresor in einen aktiven Zustand.</span><span class="sxs-lookup"><span data-stu-id="57cc2-103">Recovers a deleted secret in a key vault into an active state.</span></span>

## <span data-ttu-id="57cc2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="57cc2-104">SYNTAX</span></span>

### <span data-ttu-id="57cc2-105">Standard (Standard)</span><span class="sxs-lookup"><span data-stu-id="57cc2-105">Default (Default)</span></span>
```
Undo-AzKeyVaultSecretRemoval [-VaultName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="57cc2-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="57cc2-106">InputObject</span></span>
```
Undo-AzKeyVaultSecretRemoval [-InputObject] <PSDeletedKeyVaultSecretIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="57cc2-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="57cc2-107">DESCRIPTION</span></span>
<span data-ttu-id="57cc2-108">Mit dem Cmdlet **"Undo-AzKeyVaultSecretRemoval"** wird ein zuvor gelöschter Schlüssel wiederhergestellt.</span><span class="sxs-lookup"><span data-stu-id="57cc2-108">The **Undo-AzKeyVaultSecretRemoval** cmdlet will recover a previously deleted secret.</span></span>
<span data-ttu-id="57cc2-109">Der wiederhergestellte Schlüssel ist aktiv und kann für alle normalen geheimen Vorgänge verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="57cc2-109">The recovered secret will be active and can be used for all normal secret operations.</span></span>
<span data-ttu-id="57cc2-110">Der Aufrufer muss über die Berechtigung "Wiederherstellen" verfügen, um diesen Vorgang ausführen zu können.</span><span class="sxs-lookup"><span data-stu-id="57cc2-110">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="57cc2-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="57cc2-111">EXAMPLES</span></span>

### <span data-ttu-id="57cc2-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="57cc2-112">Example 1</span></span>
```powershell
PS C:\> Undo-AzKeyVaultSecretRemoval -VaultName 'MyKeyVault' -Name 'MySecret'

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

<span data-ttu-id="57cc2-113">Mit diesem Befehl wird der zuvor gelöschte Geheimtipp "MySecret" in einen aktiven und nutzbaren Zustand zurückgestellt.</span><span class="sxs-lookup"><span data-stu-id="57cc2-113">This command will recover the secret 'MySecret' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="57cc2-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="57cc2-114">PARAMETERS</span></span>

### <span data-ttu-id="57cc2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57cc2-115">-DefaultProfile</span></span>
<span data-ttu-id="57cc2-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="57cc2-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="57cc2-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="57cc2-117">-InputObject</span></span>
<span data-ttu-id="57cc2-118">Geheimes Objekt gelöscht</span><span class="sxs-lookup"><span data-stu-id="57cc2-118">Deleted secret object</span></span>

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

### <span data-ttu-id="57cc2-119">-Name</span><span class="sxs-lookup"><span data-stu-id="57cc2-119">-Name</span></span>
<span data-ttu-id="57cc2-120">Geheimer Name.</span><span class="sxs-lookup"><span data-stu-id="57cc2-120">Secret name.</span></span>
<span data-ttu-id="57cc2-121">Cmdlet erstellt den FQDN eines geheimen Schlüssels aus Vault-Name, aktuell ausgewählter Umgebung und geheimem Namen.</span><span class="sxs-lookup"><span data-stu-id="57cc2-121">Cmdlet constructs the FQDN of a secret from vault name, currently selected environment and secret name.</span></span>

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

### <span data-ttu-id="57cc2-122">-Vaultname</span><span class="sxs-lookup"><span data-stu-id="57cc2-122">-VaultName</span></span>
<span data-ttu-id="57cc2-123">Vault-Name.</span><span class="sxs-lookup"><span data-stu-id="57cc2-123">Vault name.</span></span>
<span data-ttu-id="57cc2-124">Cmdlet erstellt den FQDN eines Tresors basierend auf dem Namen und der aktuell ausgewählten Umgebung.</span><span class="sxs-lookup"><span data-stu-id="57cc2-124">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="57cc2-125">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="57cc2-125">-Confirm</span></span>
<span data-ttu-id="57cc2-126">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="57cc2-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="57cc2-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="57cc2-127">-WhatIf</span></span>
<span data-ttu-id="57cc2-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="57cc2-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="57cc2-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="57cc2-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="57cc2-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57cc2-130">CommonParameters</span></span>
<span data-ttu-id="57cc2-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57cc2-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57cc2-132">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="57cc2-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57cc2-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="57cc2-133">INPUTS</span></span>

### <span data-ttu-id="57cc2-134">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecretIdentityItem</span><span class="sxs-lookup"><span data-stu-id="57cc2-134">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecretIdentityItem</span></span>

## <span data-ttu-id="57cc2-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="57cc2-135">OUTPUTS</span></span>

### <span data-ttu-id="57cc2-136">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="57cc2-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret</span></span>

## <span data-ttu-id="57cc2-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="57cc2-137">NOTES</span></span>

## <span data-ttu-id="57cc2-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="57cc2-138">RELATED LINKS</span></span>

[<span data-ttu-id="57cc2-139">Remove-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="57cc2-139">Remove-AzKeyVaultSecret</span></span>](./Remove-AzKeyVaultSecret.md)

[<span data-ttu-id="57cc2-140">Add-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="57cc2-140">Add-AzKeyVaultSecret</span></span>](./Add-AzKeyVaultSecret.md)

[<span data-ttu-id="57cc2-141">Get-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="57cc2-141">Get-AzKeyVaultSecret</span></span>](./Get-AzKeyVaultSecret.md)
