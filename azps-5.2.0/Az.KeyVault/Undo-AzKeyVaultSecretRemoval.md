---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/undo-azkeyvaultsecretremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultSecretRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultSecretRemoval.md
ms.openlocfilehash: 1eca5a380dc71a5bd801c21bb7e7f556fcff0d35
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98295259"
---
# <span data-ttu-id="29b55-101">Undo-AzKeyVaultSecretRemoval</span><span class="sxs-lookup"><span data-stu-id="29b55-101">Undo-AzKeyVaultSecretRemoval</span></span>

## <span data-ttu-id="29b55-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="29b55-102">SYNOPSIS</span></span>
<span data-ttu-id="29b55-103">Stellt einen gelöschten geheimen Schlüssel in einem Schlüsseltresor in einen aktiven Zustand wiederher.</span><span class="sxs-lookup"><span data-stu-id="29b55-103">Recovers a deleted secret in a key vault into an active state.</span></span>

## <span data-ttu-id="29b55-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="29b55-104">SYNTAX</span></span>

### <span data-ttu-id="29b55-105">Standard (Standard)</span><span class="sxs-lookup"><span data-stu-id="29b55-105">Default (Default)</span></span>
```
Undo-AzKeyVaultSecretRemoval [-VaultName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="29b55-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="29b55-106">InputObject</span></span>
```
Undo-AzKeyVaultSecretRemoval [-InputObject] <PSDeletedKeyVaultSecretIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="29b55-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="29b55-107">DESCRIPTION</span></span>
<span data-ttu-id="29b55-108">Das **Cmdlet "Undo-AzKeyVaultSecretRemoval"** stellt einen zuvor gelöschten Geheimschlüssel wieder sicher.</span><span class="sxs-lookup"><span data-stu-id="29b55-108">The **Undo-AzKeyVaultSecretRemoval** cmdlet will recover a previously deleted secret.</span></span>
<span data-ttu-id="29b55-109">Das wiederhergestellte Geheime ist aktiv und kann für alle normalen geheimen Vorgänge verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="29b55-109">The recovered secret will be active and can be used for all normal secret operations.</span></span>
<span data-ttu-id="29b55-110">Der Aufrufer muss über die Berechtigung "Wiederherstellen" verfügen, um diesen Vorgang ausführen zu können.</span><span class="sxs-lookup"><span data-stu-id="29b55-110">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="29b55-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="29b55-111">EXAMPLES</span></span>

### <span data-ttu-id="29b55-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="29b55-112">Example 1</span></span>
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

<span data-ttu-id="29b55-113">Mit diesem Befehl wird der zuvor gelöschte geheime "MySecret" in einen aktiven und verwendbaren Zustand wiederhergestellt.</span><span class="sxs-lookup"><span data-stu-id="29b55-113">This command will recover the secret 'MySecret' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="29b55-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="29b55-114">PARAMETERS</span></span>

### <span data-ttu-id="29b55-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29b55-115">-DefaultProfile</span></span>
<span data-ttu-id="29b55-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="29b55-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="29b55-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="29b55-117">-InputObject</span></span>
<span data-ttu-id="29b55-118">Gelöschtes geheimes Objekt</span><span class="sxs-lookup"><span data-stu-id="29b55-118">Deleted secret object</span></span>

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

### <span data-ttu-id="29b55-119">-Name</span><span class="sxs-lookup"><span data-stu-id="29b55-119">-Name</span></span>
<span data-ttu-id="29b55-120">Geheimer Name.</span><span class="sxs-lookup"><span data-stu-id="29b55-120">Secret name.</span></span>
<span data-ttu-id="29b55-121">Das Cmdlet erstellt den FQDN eines Geheimen aus dem Namen des Tresors, die aktuell ausgewählte Umgebung und den geheimen Namen.</span><span class="sxs-lookup"><span data-stu-id="29b55-121">Cmdlet constructs the FQDN of a secret from vault name, currently selected environment and secret name.</span></span>

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

### <span data-ttu-id="29b55-122">-VaultName</span><span class="sxs-lookup"><span data-stu-id="29b55-122">-VaultName</span></span>
<span data-ttu-id="29b55-123">Name des Tresors.</span><span class="sxs-lookup"><span data-stu-id="29b55-123">Vault name.</span></span>
<span data-ttu-id="29b55-124">Das Cmdlet erstellt den FQDN eines Tresors basierend auf dem Namen und der aktuell ausgewählten Umgebung.</span><span class="sxs-lookup"><span data-stu-id="29b55-124">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="29b55-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="29b55-125">-Confirm</span></span>
<span data-ttu-id="29b55-126">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="29b55-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="29b55-127">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="29b55-127">-WhatIf</span></span>
<span data-ttu-id="29b55-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="29b55-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="29b55-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="29b55-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="29b55-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29b55-130">CommonParameters</span></span>
<span data-ttu-id="29b55-131">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="29b55-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29b55-132">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="29b55-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29b55-133">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="29b55-133">INPUTS</span></span>

### <span data-ttu-id="29b55-134">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecretIdentityItem</span><span class="sxs-lookup"><span data-stu-id="29b55-134">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecretIdentityItem</span></span>

## <span data-ttu-id="29b55-135">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="29b55-135">OUTPUTS</span></span>

### <span data-ttu-id="29b55-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="29b55-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret</span></span>

## <span data-ttu-id="29b55-137">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="29b55-137">NOTES</span></span>

## <span data-ttu-id="29b55-138">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="29b55-138">RELATED LINKS</span></span>

[<span data-ttu-id="29b55-139">Remove-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="29b55-139">Remove-AzKeyVaultSecret</span></span>](./Remove-AzKeyVaultSecret.md)

[<span data-ttu-id="29b55-140">Add-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="29b55-140">Add-AzKeyVaultSecret</span></span>](./Add-AzKeyVaultSecret.md)

[<span data-ttu-id="29b55-141">Get-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="29b55-141">Get-AzKeyVaultSecret</span></span>](./Get-AzKeyVaultSecret.md)
