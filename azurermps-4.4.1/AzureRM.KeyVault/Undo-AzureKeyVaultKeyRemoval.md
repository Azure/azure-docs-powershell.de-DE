---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://msdn.microsoft.com/en-us/library/dn868052.aspx
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Undo-AzureKeyVaultKeyRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Undo-AzureKeyVaultKeyRemoval.md
ms.openlocfilehash: df29d88fbac1a8d2dc382522e24ff143cf075573
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504085"
---
# <span data-ttu-id="4c93e-101">Undo-AzureKeyVaultKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="4c93e-101">Undo-AzureKeyVaultKeyRemoval</span></span>

## <span data-ttu-id="4c93e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4c93e-102">SYNOPSIS</span></span>
<span data-ttu-id="4c93e-103">Stellt einen gelöschten Schlüssel in einem schlüsseltresor in einen aktiven Zustand.</span><span class="sxs-lookup"><span data-stu-id="4c93e-103">Recovers a deleted key in a key vault into an active state.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4c93e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4c93e-104">SYNTAX</span></span>

```
Undo-AzureKeyVaultKeyRemoval [-VaultName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4c93e-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4c93e-105">DESCRIPTION</span></span>
<span data-ttu-id="4c93e-106">Mit dem Cmdlet **"Undo-AzureKeyVaultKeyRemoval"** wird ein zuvor gelöschter Schlüssel wiederhergestellt.</span><span class="sxs-lookup"><span data-stu-id="4c93e-106">The **Undo-AzureKeyVaultKeyRemoval** cmdlet will recover a previously deleted key.</span></span>
<span data-ttu-id="4c93e-107">Der wiederhergestellte Schlüssel ist aktiv und kann für alle normalen Schlüsselvorgänge verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4c93e-107">The recovered key will be active and can be used for all normal key operations.</span></span>
<span data-ttu-id="4c93e-108">Der Aufrufer muss über die Berechtigung "Wiederherstellen" verfügen, um diesen Vorgang ausführen zu können.</span><span class="sxs-lookup"><span data-stu-id="4c93e-108">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="4c93e-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4c93e-109">EXAMPLES</span></span>

### <span data-ttu-id="4c93e-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="4c93e-110">Example 1</span></span>
```
PS C:\>Undo-AzureKeyVaultKeyRemoval -VaultName 'MyKeyVault' -Name 'MyKey'
```

<span data-ttu-id="4c93e-111">Mit diesem Befehl wird der zuvor gelöschte Schlüssel "MyKey" wieder in einen aktiven und nutzbaren Zustand versetzt.</span><span class="sxs-lookup"><span data-stu-id="4c93e-111">This command will recover the key 'MyKey' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="4c93e-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="4c93e-112">PARAMETERS</span></span>

### <span data-ttu-id="4c93e-113">-Name</span><span class="sxs-lookup"><span data-stu-id="4c93e-113">-Name</span></span>
<span data-ttu-id="4c93e-114">Schlüsselname.</span><span class="sxs-lookup"><span data-stu-id="4c93e-114">Key name.</span></span>
<span data-ttu-id="4c93e-115">Cmdlet erstellt den FQDN eines Schlüssels aus Vault-Name, aktuell ausgewählter Umgebung und Schlüsselname.</span><span class="sxs-lookup"><span data-stu-id="4c93e-115">Cmdlet constructs the FQDN of a key from vault name, currently selected environment and key name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c93e-116">-Vaultname</span><span class="sxs-lookup"><span data-stu-id="4c93e-116">-VaultName</span></span>
<span data-ttu-id="4c93e-117">Vault-Name.</span><span class="sxs-lookup"><span data-stu-id="4c93e-117">Vault name.</span></span>
<span data-ttu-id="4c93e-118">Cmdlet erstellt den FQDN eines Tresors basierend auf dem Namen und der aktuell ausgewählten Umgebung.</span><span class="sxs-lookup"><span data-stu-id="4c93e-118">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="4c93e-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="4c93e-119">-Confirm</span></span>
<span data-ttu-id="4c93e-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4c93e-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4c93e-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4c93e-121">-WhatIf</span></span>
<span data-ttu-id="4c93e-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4c93e-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4c93e-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4c93e-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4c93e-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c93e-124">-DefaultProfile</span></span>
<span data-ttu-id="4c93e-125">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4c93e-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4c93e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c93e-126">CommonParameters</span></span>
<span data-ttu-id="4c93e-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4c93e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c93e-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4c93e-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c93e-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4c93e-129">INPUTS</span></span>

### <span data-ttu-id="4c93e-130">System. String</span><span class="sxs-lookup"><span data-stu-id="4c93e-130">System.String</span></span>

## <span data-ttu-id="4c93e-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4c93e-131">OUTPUTS</span></span>

### <span data-ttu-id="4c93e-132">Microsoft. Azure. Commands. keyvault. Models. keybundle</span><span class="sxs-lookup"><span data-stu-id="4c93e-132">Microsoft.Azure.Commands.KeyVault.Models.KeyBundle</span></span>

## <span data-ttu-id="4c93e-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="4c93e-133">NOTES</span></span>

## <span data-ttu-id="4c93e-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4c93e-134">RELATED LINKS</span></span>

[<span data-ttu-id="4c93e-135">Remove-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="4c93e-135">Remove-AzureKeyVaultKey</span></span>](./Remove-AzureKeyVaultKey.md)

[<span data-ttu-id="4c93e-136">Add-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="4c93e-136">Add-AzureKeyVaultKey</span></span>](./Add-AzureKeyVaultKey.md)

[<span data-ttu-id="4c93e-137">Get-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="4c93e-137">Get-AzureKeyVaultKey</span></span>](./Get-AzureKeyVaultKey.md)

