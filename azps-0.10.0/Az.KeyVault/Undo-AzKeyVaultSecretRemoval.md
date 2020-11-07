---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/undo-AzKeyvaultsecretremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Undo-AzKeyVaultSecretRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Undo-AzKeyVaultSecretRemoval.md
ms.openlocfilehash: e65bef4119c51b989287bbf0db2e7587fef50271
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843835"
---
# <span data-ttu-id="dd87d-101">Undo-AzKeyVaultSecretRemoval</span><span class="sxs-lookup"><span data-stu-id="dd87d-101">Undo-AzKeyVaultSecretRemoval</span></span>

## <span data-ttu-id="dd87d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="dd87d-102">SYNOPSIS</span></span>
<span data-ttu-id="dd87d-103">Stellt ein gelöschtes Geheimnis in einem schlüsseltresor in einen aktiven Zustand.</span><span class="sxs-lookup"><span data-stu-id="dd87d-103">Recovers a deleted secret in a key vault into an active state.</span></span>

## <span data-ttu-id="dd87d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="dd87d-104">SYNTAX</span></span>

```
Undo-AzKeyVaultSecretRemoval [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dd87d-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="dd87d-105">DESCRIPTION</span></span>
<span data-ttu-id="dd87d-106">Mit dem Cmdlet **"Undo-AzKeyVaultSecretRemoval"** wird ein zuvor gelöschter Schlüssel wiederhergestellt.</span><span class="sxs-lookup"><span data-stu-id="dd87d-106">The **Undo-AzKeyVaultSecretRemoval** cmdlet will recover a previously deleted secret.</span></span>
<span data-ttu-id="dd87d-107">Der wiederhergestellte Schlüssel ist aktiv und kann für alle normalen geheimen Vorgänge verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="dd87d-107">The recovered secret will be active and can be used for all normal secret operations.</span></span>
<span data-ttu-id="dd87d-108">Der Aufrufer muss über die Berechtigung "Wiederherstellen" verfügen, um diesen Vorgang ausführen zu können.</span><span class="sxs-lookup"><span data-stu-id="dd87d-108">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="dd87d-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="dd87d-109">EXAMPLES</span></span>

### <span data-ttu-id="dd87d-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="dd87d-110">Example 1</span></span>
```
PS C:\> Undo-AzKeyVaultSecretRemoval -VaultName 'MyKeyVault' -Name 'MySecret'
```

<span data-ttu-id="dd87d-111">Mit diesem Befehl wird der zuvor gelöschte Geheimtipp "MySecret" in einen aktiven und nutzbaren Zustand zurückgestellt.</span><span class="sxs-lookup"><span data-stu-id="dd87d-111">This command will recover the secret 'MySecret' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="dd87d-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="dd87d-112">PARAMETERS</span></span>

### <span data-ttu-id="dd87d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd87d-113">-DefaultProfile</span></span>
<span data-ttu-id="dd87d-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="dd87d-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dd87d-115">-Name</span><span class="sxs-lookup"><span data-stu-id="dd87d-115">-Name</span></span>
<span data-ttu-id="dd87d-116">Geheimer Name.</span><span class="sxs-lookup"><span data-stu-id="dd87d-116">Secret name.</span></span>
<span data-ttu-id="dd87d-117">Cmdlet erstellt den FQDN eines geheimen Schlüssels aus Vault-Name, aktuell ausgewählter Umgebung und geheimem Namen.</span><span class="sxs-lookup"><span data-stu-id="dd87d-117">Cmdlet constructs the FQDN of a secret from vault name, currently selected environment and secret name.</span></span>

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

### <span data-ttu-id="dd87d-118">-Vaultname</span><span class="sxs-lookup"><span data-stu-id="dd87d-118">-VaultName</span></span>
<span data-ttu-id="dd87d-119">Vault-Name.</span><span class="sxs-lookup"><span data-stu-id="dd87d-119">Vault name.</span></span>
<span data-ttu-id="dd87d-120">Cmdlet erstellt den FQDN eines Tresors basierend auf dem Namen und der aktuell ausgewählten Umgebung.</span><span class="sxs-lookup"><span data-stu-id="dd87d-120">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="dd87d-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="dd87d-121">-Confirm</span></span>
<span data-ttu-id="dd87d-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="dd87d-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dd87d-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dd87d-123">-WhatIf</span></span>
<span data-ttu-id="dd87d-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="dd87d-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dd87d-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="dd87d-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dd87d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd87d-126">CommonParameters</span></span>
<span data-ttu-id="dd87d-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd87d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd87d-128">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dd87d-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd87d-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="dd87d-129">INPUTS</span></span>

### <span data-ttu-id="dd87d-130">System. String</span><span class="sxs-lookup"><span data-stu-id="dd87d-130">System.String</span></span>

## <span data-ttu-id="dd87d-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="dd87d-131">OUTPUTS</span></span>

### <span data-ttu-id="dd87d-132">Microsoft. Azure. Commands. keyvault. Models. Secret</span><span class="sxs-lookup"><span data-stu-id="dd87d-132">Microsoft.Azure.Commands.KeyVault.Models.Secret</span></span>

## <span data-ttu-id="dd87d-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="dd87d-133">NOTES</span></span>

## <span data-ttu-id="dd87d-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="dd87d-134">RELATED LINKS</span></span>

[<span data-ttu-id="dd87d-135">Remove-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="dd87d-135">Remove-AzKeyVaultSecret</span></span>](./Remove-AzKeyVaultSecret.md)

[<span data-ttu-id="dd87d-136">Add-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="dd87d-136">Add-AzKeyVaultSecret</span></span>](./Add-AzKeyVaultSecret.md)

[<span data-ttu-id="dd87d-137">Get-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="dd87d-137">Get-AzKeyVaultSecret</span></span>](./Get-AzKeyVaultSecret.md)
