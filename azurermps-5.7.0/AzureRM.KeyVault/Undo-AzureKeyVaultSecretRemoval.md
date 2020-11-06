---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/undo-azurekeyvaultsecretremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Undo-AzureKeyVaultSecretRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Undo-AzureKeyVaultSecretRemoval.md
ms.openlocfilehash: 07c62b1b106453cf9b19610867be39458943bcab
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498934"
---
# <span data-ttu-id="e5701-101">Undo-AzureKeyVaultSecretRemoval</span><span class="sxs-lookup"><span data-stu-id="e5701-101">Undo-AzureKeyVaultSecretRemoval</span></span>

## <span data-ttu-id="e5701-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e5701-102">SYNOPSIS</span></span>
<span data-ttu-id="e5701-103">Stellt ein gelöschtes Geheimnis in einem schlüsseltresor in einen aktiven Zustand.</span><span class="sxs-lookup"><span data-stu-id="e5701-103">Recovers a deleted secret in a key vault into an active state.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e5701-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e5701-104">SYNTAX</span></span>

### <span data-ttu-id="e5701-105">Standard (Standard)</span><span class="sxs-lookup"><span data-stu-id="e5701-105">Default (Default)</span></span>
```
Undo-AzureKeyVaultSecretRemoval [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e5701-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="e5701-106">InputObject</span></span>
```
Undo-AzureKeyVaultSecretRemoval [-InputObject] <PSDeletedKeyVaultSecretIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e5701-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e5701-107">DESCRIPTION</span></span>
<span data-ttu-id="e5701-108">Mit dem Cmdlet **"Undo-AzureKeyVaultSecretRemoval"** wird ein zuvor gelöschter Schlüssel wiederhergestellt.</span><span class="sxs-lookup"><span data-stu-id="e5701-108">The **Undo-AzureKeyVaultSecretRemoval** cmdlet will recover a previously deleted secret.</span></span>
<span data-ttu-id="e5701-109">Der wiederhergestellte Schlüssel ist aktiv und kann für alle normalen geheimen Vorgänge verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e5701-109">The recovered secret will be active and can be used for all normal secret operations.</span></span>
<span data-ttu-id="e5701-110">Der Aufrufer muss über die Berechtigung "Wiederherstellen" verfügen, um diesen Vorgang ausführen zu können.</span><span class="sxs-lookup"><span data-stu-id="e5701-110">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="e5701-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e5701-111">EXAMPLES</span></span>

### <span data-ttu-id="e5701-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e5701-112">Example 1</span></span>
```
PS C:\> Undo-AzureKeyVaultSecretRemoval -VaultName 'MyKeyVault' -Name 'MySecret'
```

<span data-ttu-id="e5701-113">Mit diesem Befehl wird der zuvor gelöschte Geheimtipp "MySecret" in einen aktiven und nutzbaren Zustand zurückgestellt.</span><span class="sxs-lookup"><span data-stu-id="e5701-113">This command will recover the secret 'MySecret' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="e5701-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="e5701-114">PARAMETERS</span></span>

### <span data-ttu-id="e5701-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5701-115">-DefaultProfile</span></span>
<span data-ttu-id="e5701-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="e5701-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5701-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="e5701-117">-InputObject</span></span>
<span data-ttu-id="e5701-118">Geheimes Objekt gelöscht</span><span class="sxs-lookup"><span data-stu-id="e5701-118">Deleted secret object</span></span>

```yaml
Type: PSDeletedKeyVaultSecretIdentityItem
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e5701-119">-Name</span><span class="sxs-lookup"><span data-stu-id="e5701-119">-Name</span></span>
<span data-ttu-id="e5701-120">Geheimer Name.</span><span class="sxs-lookup"><span data-stu-id="e5701-120">Secret name.</span></span>
<span data-ttu-id="e5701-121">Cmdlet erstellt den FQDN eines geheimen Schlüssels aus Vault-Name, aktuell ausgewählter Umgebung und geheimem Namen.</span><span class="sxs-lookup"><span data-stu-id="e5701-121">Cmdlet constructs the FQDN of a secret from vault name, currently selected environment and secret name.</span></span>

```yaml
Type: String
Parameter Sets: Default
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5701-122">-Vaultname</span><span class="sxs-lookup"><span data-stu-id="e5701-122">-VaultName</span></span>
<span data-ttu-id="e5701-123">Vault-Name.</span><span class="sxs-lookup"><span data-stu-id="e5701-123">Vault name.</span></span>
<span data-ttu-id="e5701-124">Cmdlet erstellt den FQDN eines Tresors basierend auf dem Namen und der aktuell ausgewählten Umgebung.</span><span class="sxs-lookup"><span data-stu-id="e5701-124">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: String
Parameter Sets: Default
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5701-125">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e5701-125">-Confirm</span></span>
<span data-ttu-id="e5701-126">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e5701-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5701-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e5701-127">-WhatIf</span></span>
<span data-ttu-id="e5701-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e5701-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e5701-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e5701-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5701-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5701-130">CommonParameters</span></span>
<span data-ttu-id="e5701-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5701-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5701-132">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e5701-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5701-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e5701-133">INPUTS</span></span>

### <span data-ttu-id="e5701-134">System. String</span><span class="sxs-lookup"><span data-stu-id="e5701-134">System.String</span></span>

## <span data-ttu-id="e5701-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e5701-135">OUTPUTS</span></span>

### <span data-ttu-id="e5701-136">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="e5701-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret</span></span>

## <span data-ttu-id="e5701-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="e5701-137">NOTES</span></span>

## <span data-ttu-id="e5701-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e5701-138">RELATED LINKS</span></span>

[<span data-ttu-id="e5701-139">Remove-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="e5701-139">Remove-AzureKeyVaultSecret</span></span>](./Remove-AzureKeyVaultSecret.md)

[<span data-ttu-id="e5701-140">Add-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="e5701-140">Add-AzureKeyVaultSecret</span></span>](./Add-AzureKeyVaultSecret.md)

[<span data-ttu-id="e5701-141">Get-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="e5701-141">Get-AzureKeyVaultSecret</span></span>](./Get-AzureKeyVaultSecret.md)
