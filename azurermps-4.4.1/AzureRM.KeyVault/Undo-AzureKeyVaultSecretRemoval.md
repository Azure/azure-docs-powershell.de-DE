---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://msdn.microsoft.com/en-us/library/dn868052.aspx
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Undo-AzureKeyVaultSecretRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Undo-AzureKeyVaultSecretRemoval.md
ms.openlocfilehash: e71fa3098003f6fb713c90903eee6e97ca4f42ae
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663928"
---
# <span data-ttu-id="ac784-101">Undo-AzureKeyVaultSecretRemoval</span><span class="sxs-lookup"><span data-stu-id="ac784-101">Undo-AzureKeyVaultSecretRemoval</span></span>

## <span data-ttu-id="ac784-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ac784-102">SYNOPSIS</span></span>
<span data-ttu-id="ac784-103">Stellt ein gelöschtes Geheimnis in einem schlüsseltresor in einen aktiven Zustand.</span><span class="sxs-lookup"><span data-stu-id="ac784-103">Recovers a deleted secret in a key vault into an active state.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ac784-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ac784-104">SYNTAX</span></span>

```
Undo-AzureKeyVaultSecretRemoval [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ac784-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ac784-105">DESCRIPTION</span></span>
<span data-ttu-id="ac784-106">Mit dem Cmdlet **"Undo-AzureKeyVaultSecretRemoval"** wird ein zuvor gelöschter Schlüssel wiederhergestellt.</span><span class="sxs-lookup"><span data-stu-id="ac784-106">The **Undo-AzureKeyVaultSecretRemoval** cmdlet will recover a previously deleted secret.</span></span>
<span data-ttu-id="ac784-107">Der wiederhergestellte Schlüssel ist aktiv und kann für alle normalen geheimen Vorgänge verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ac784-107">The recovered secret will be active and can be used for all normal secret operations.</span></span>
<span data-ttu-id="ac784-108">Der Aufrufer muss über die Berechtigung "Wiederherstellen" verfügen, um diesen Vorgang ausführen zu können.</span><span class="sxs-lookup"><span data-stu-id="ac784-108">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="ac784-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ac784-109">EXAMPLES</span></span>

### <span data-ttu-id="ac784-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ac784-110">Example 1</span></span>
```
PS C:\> Undo-AzureKeyVaultSecretRemoval -VaultName 'MyKeyVault' -Name 'MySecret'
```

<span data-ttu-id="ac784-111">Mit diesem Befehl wird der zuvor gelöschte Geheimtipp "MySecret" in einen aktiven und nutzbaren Zustand zurückgestellt.</span><span class="sxs-lookup"><span data-stu-id="ac784-111">This command will recover the secret 'MySecret' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="ac784-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="ac784-112">PARAMETERS</span></span>

### <span data-ttu-id="ac784-113">-Name</span><span class="sxs-lookup"><span data-stu-id="ac784-113">-Name</span></span>
<span data-ttu-id="ac784-114">Geheimer Name.</span><span class="sxs-lookup"><span data-stu-id="ac784-114">Secret name.</span></span>
<span data-ttu-id="ac784-115">Cmdlet erstellt den FQDN eines geheimen Schlüssels aus Vault-Name, aktuell ausgewählter Umgebung und geheimem Namen.</span><span class="sxs-lookup"><span data-stu-id="ac784-115">Cmdlet constructs the FQDN of a secret from vault name, currently selected environment and secret name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ac784-116">-Vaultname</span><span class="sxs-lookup"><span data-stu-id="ac784-116">-VaultName</span></span>
<span data-ttu-id="ac784-117">Vault-Name.</span><span class="sxs-lookup"><span data-stu-id="ac784-117">Vault name.</span></span>
<span data-ttu-id="ac784-118">Cmdlet erstellt den FQDN eines Tresors basierend auf dem Namen und der aktuell ausgewählten Umgebung.</span><span class="sxs-lookup"><span data-stu-id="ac784-118">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ac784-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ac784-119">-Confirm</span></span>
<span data-ttu-id="ac784-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ac784-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ac784-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ac784-121">-WhatIf</span></span>
<span data-ttu-id="ac784-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ac784-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ac784-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ac784-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ac784-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac784-124">-DefaultProfile</span></span>
<span data-ttu-id="ac784-125">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ac784-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ac784-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac784-126">CommonParameters</span></span>
<span data-ttu-id="ac784-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ac784-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac784-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ac784-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac784-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ac784-129">INPUTS</span></span>

### <span data-ttu-id="ac784-130">System. String</span><span class="sxs-lookup"><span data-stu-id="ac784-130">System.String</span></span>

## <span data-ttu-id="ac784-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ac784-131">OUTPUTS</span></span>

### <span data-ttu-id="ac784-132">Microsoft. Azure. Commands. keyvault. Models. Secret</span><span class="sxs-lookup"><span data-stu-id="ac784-132">Microsoft.Azure.Commands.KeyVault.Models.Secret</span></span>

## <span data-ttu-id="ac784-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="ac784-133">NOTES</span></span>

## <span data-ttu-id="ac784-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ac784-134">RELATED LINKS</span></span>

[<span data-ttu-id="ac784-135">Remove-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="ac784-135">Remove-AzureKeyVaultSecret</span></span>](./Remove-AzureKeyVaultSecret.md)

[<span data-ttu-id="ac784-136">Add-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="ac784-136">Add-AzureKeyVaultSecret</span></span>](./Add-AzureKeyVaultSecret.md)

[<span data-ttu-id="ac784-137">Get-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="ac784-137">Get-AzureKeyVaultSecret</span></span>](./Get-AzureKeyVaultSecret.md)
