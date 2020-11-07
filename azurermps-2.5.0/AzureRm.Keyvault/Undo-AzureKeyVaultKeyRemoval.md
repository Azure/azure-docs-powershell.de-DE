---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/undo-azurekeyvaultkeyremoval
schema: 2.0.0
ms.openlocfilehash: 831bcdb76a0f24a2935f2ffd2ed0bf7df1c10042
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849291"
---
# <span data-ttu-id="ac17a-101">Undo-AzureKeyVaultKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="ac17a-101">Undo-AzureKeyVaultKeyRemoval</span></span>

## <span data-ttu-id="ac17a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ac17a-102">SYNOPSIS</span></span>
<span data-ttu-id="ac17a-103">Stellt einen gelöschten Schlüssel in einem schlüsseltresor in einen aktiven Zustand.</span><span class="sxs-lookup"><span data-stu-id="ac17a-103">Recovers a deleted key in a key vault into an active state.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ac17a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ac17a-104">SYNTAX</span></span>

```
Undo-AzureKeyVaultKeyRemoval [-VaultName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ac17a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ac17a-105">DESCRIPTION</span></span>
<span data-ttu-id="ac17a-106">Mit dem Cmdlet **"Undo-AzureKeyVaultKeyRemoval"** wird ein zuvor gelöschter Schlüssel wiederhergestellt.</span><span class="sxs-lookup"><span data-stu-id="ac17a-106">The **Undo-AzureKeyVaultKeyRemoval** cmdlet will recover a previously deleted key.</span></span>
<span data-ttu-id="ac17a-107">Der wiederhergestellte Schlüssel ist aktiv und kann für alle normalen Schlüsselvorgänge verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ac17a-107">The recovered key will be active and can be used for all normal key operations.</span></span>
<span data-ttu-id="ac17a-108">Der Aufrufer muss über die Berechtigung "Wiederherstellen" verfügen, um diesen Vorgang ausführen zu können.</span><span class="sxs-lookup"><span data-stu-id="ac17a-108">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="ac17a-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ac17a-109">EXAMPLES</span></span>

### <span data-ttu-id="ac17a-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ac17a-110">Example 1</span></span>
```
PS C:\>Undo-AzureKeyVaultKeyRemoval -VaultName 'MyKeyVault' -Name 'MyKey'
```

<span data-ttu-id="ac17a-111">Mit diesem Befehl wird der zuvor gelöschte Schlüssel "MyKey" wieder in einen aktiven und nutzbaren Zustand versetzt.</span><span class="sxs-lookup"><span data-stu-id="ac17a-111">This command will recover the key 'MyKey' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="ac17a-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="ac17a-112">PARAMETERS</span></span>

### <span data-ttu-id="ac17a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac17a-113">-DefaultProfile</span></span>
<span data-ttu-id="ac17a-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="ac17a-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ac17a-115">-Name</span><span class="sxs-lookup"><span data-stu-id="ac17a-115">-Name</span></span>
<span data-ttu-id="ac17a-116">Schlüsselname.</span><span class="sxs-lookup"><span data-stu-id="ac17a-116">Key name.</span></span>
<span data-ttu-id="ac17a-117">Cmdlet erstellt den FQDN eines Schlüssels aus Vault-Name, aktuell ausgewählter Umgebung und Schlüsselname.</span><span class="sxs-lookup"><span data-stu-id="ac17a-117">Cmdlet constructs the FQDN of a key from vault name, currently selected environment and key name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ac17a-118">-Vaultname</span><span class="sxs-lookup"><span data-stu-id="ac17a-118">-VaultName</span></span>
<span data-ttu-id="ac17a-119">Vault-Name.</span><span class="sxs-lookup"><span data-stu-id="ac17a-119">Vault name.</span></span>
<span data-ttu-id="ac17a-120">Cmdlet erstellt den FQDN eines Tresors basierend auf dem Namen und der aktuell ausgewählten Umgebung.</span><span class="sxs-lookup"><span data-stu-id="ac17a-120">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="ac17a-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ac17a-121">-Confirm</span></span>
<span data-ttu-id="ac17a-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ac17a-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ac17a-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ac17a-123">-WhatIf</span></span>
<span data-ttu-id="ac17a-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ac17a-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ac17a-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ac17a-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ac17a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac17a-126">CommonParameters</span></span>
<span data-ttu-id="ac17a-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ac17a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac17a-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ac17a-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac17a-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ac17a-129">INPUTS</span></span>

### <span data-ttu-id="ac17a-130">System. String</span><span class="sxs-lookup"><span data-stu-id="ac17a-130">System.String</span></span>

## <span data-ttu-id="ac17a-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ac17a-131">OUTPUTS</span></span>

### <span data-ttu-id="ac17a-132">Microsoft. Azure. Commands. keyvault. Models. keybundle</span><span class="sxs-lookup"><span data-stu-id="ac17a-132">Microsoft.Azure.Commands.KeyVault.Models.KeyBundle</span></span>

## <span data-ttu-id="ac17a-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="ac17a-133">NOTES</span></span>

## <span data-ttu-id="ac17a-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ac17a-134">RELATED LINKS</span></span>

[<span data-ttu-id="ac17a-135">Remove-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="ac17a-135">Remove-AzureKeyVaultKey</span></span>](./Remove-AzureKeyVaultKey.md)

[<span data-ttu-id="ac17a-136">Add-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="ac17a-136">Add-AzureKeyVaultKey</span></span>](./Add-AzureKeyVaultKey.md)

[<span data-ttu-id="ac17a-137">Get-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="ac17a-137">Get-AzureKeyVaultKey</span></span>](./Get-AzureKeyVaultKey.md)

