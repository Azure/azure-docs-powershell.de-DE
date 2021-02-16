---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/undo-AzKeyvaultsecretremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Undo-AzKeyVaultSecretRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Undo-AzKeyVaultSecretRemoval.md
ms.openlocfilehash: 9c240d3902aeba38af4281ba31bacea76bad0a58
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/14/2021
ms.locfileid: "100399089"
---
# <span data-ttu-id="40837-101">Undo-AzKeyVaultSecretRemoval</span><span class="sxs-lookup"><span data-stu-id="40837-101">Undo-AzKeyVaultSecretRemoval</span></span>

## <span data-ttu-id="40837-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="40837-102">SYNOPSIS</span></span>
<span data-ttu-id="40837-103">Stellt einen gelöschten geheimen Schlüssel in einem Schlüsseltresor in einen aktiven Zustand wiederher.</span><span class="sxs-lookup"><span data-stu-id="40837-103">Recovers a deleted secret in a key vault into an active state.</span></span>

## <span data-ttu-id="40837-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="40837-104">SYNTAX</span></span>

```
Undo-AzKeyVaultSecretRemoval [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="40837-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="40837-105">DESCRIPTION</span></span>
<span data-ttu-id="40837-106">Das **Cmdlet "Undo-AzKeyVaultSecretRemoval"** stellt einen zuvor gelöschten Geheimschlüssel wieder sicher.</span><span class="sxs-lookup"><span data-stu-id="40837-106">The **Undo-AzKeyVaultSecretRemoval** cmdlet will recover a previously deleted secret.</span></span>
<span data-ttu-id="40837-107">Das wiederhergestellte Geheime ist aktiv und kann für alle normalen geheimen Vorgänge verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="40837-107">The recovered secret will be active and can be used for all normal secret operations.</span></span>
<span data-ttu-id="40837-108">Der Aufrufer muss über die Berechtigung "Wiederherstellen" verfügen, um diesen Vorgang ausführen zu können.</span><span class="sxs-lookup"><span data-stu-id="40837-108">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="40837-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="40837-109">EXAMPLES</span></span>

### <span data-ttu-id="40837-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="40837-110">Example 1</span></span>
```
PS C:\> Undo-AzKeyVaultSecretRemoval -VaultName 'MyKeyVault' -Name 'MySecret'
```

<span data-ttu-id="40837-111">Mit diesem Befehl wird der zuvor gelöschte geheime "MySecret" in einen aktiven und verwendbaren Zustand wiederhergestellt.</span><span class="sxs-lookup"><span data-stu-id="40837-111">This command will recover the secret 'MySecret' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="40837-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="40837-112">PARAMETERS</span></span>

### <span data-ttu-id="40837-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40837-113">-DefaultProfile</span></span>
<span data-ttu-id="40837-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="40837-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40837-115">-Name</span><span class="sxs-lookup"><span data-stu-id="40837-115">-Name</span></span>
<span data-ttu-id="40837-116">Geheimer Name.</span><span class="sxs-lookup"><span data-stu-id="40837-116">Secret name.</span></span>
<span data-ttu-id="40837-117">Das Cmdlet erstellt den FQDN eines Geheimen aus dem Namen des Tresors, die aktuell ausgewählte Umgebung und den geheimen Namen.</span><span class="sxs-lookup"><span data-stu-id="40837-117">Cmdlet constructs the FQDN of a secret from vault name, currently selected environment and secret name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40837-118">-VaultName</span><span class="sxs-lookup"><span data-stu-id="40837-118">-VaultName</span></span>
<span data-ttu-id="40837-119">Name des Tresors.</span><span class="sxs-lookup"><span data-stu-id="40837-119">Vault name.</span></span>
<span data-ttu-id="40837-120">Das Cmdlet erstellt den FQDN eines Tresors basierend auf dem Namen und der aktuell ausgewählten Umgebung.</span><span class="sxs-lookup"><span data-stu-id="40837-120">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40837-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="40837-121">-Confirm</span></span>
<span data-ttu-id="40837-122">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="40837-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="40837-123">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="40837-123">-WhatIf</span></span>
<span data-ttu-id="40837-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="40837-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="40837-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="40837-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="40837-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40837-126">CommonParameters</span></span>
<span data-ttu-id="40837-127">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="40837-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40837-128">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="40837-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40837-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="40837-129">INPUTS</span></span>

### <span data-ttu-id="40837-130">System.String</span><span class="sxs-lookup"><span data-stu-id="40837-130">System.String</span></span>

## <span data-ttu-id="40837-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="40837-131">OUTPUTS</span></span>

### <span data-ttu-id="40837-132">Microsoft.Azure.Commands.KeyVault.Models.Secret</span><span class="sxs-lookup"><span data-stu-id="40837-132">Microsoft.Azure.Commands.KeyVault.Models.Secret</span></span>

## <span data-ttu-id="40837-133">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="40837-133">NOTES</span></span>

## <span data-ttu-id="40837-134">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="40837-134">RELATED LINKS</span></span>

[<span data-ttu-id="40837-135">Remove-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="40837-135">Remove-AzKeyVaultSecret</span></span>](./Remove-AzKeyVaultSecret.md)


[<span data-ttu-id="40837-136">Get-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="40837-136">Get-AzKeyVaultSecret</span></span>](./Get-AzKeyVaultSecret.md)
