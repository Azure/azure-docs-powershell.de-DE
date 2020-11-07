---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/undo-azurermkeyvaultremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Undo-AzureRmKeyVaultRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Undo-AzureRmKeyVaultRemoval.md
ms.openlocfilehash: 83737a7643c78ef4ec41d84e153690b3a53a8d5f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664655"
---
# <span data-ttu-id="044f8-101">Undo-AzureRmKeyVaultRemoval</span><span class="sxs-lookup"><span data-stu-id="044f8-101">Undo-AzureRmKeyVaultRemoval</span></span>

## <span data-ttu-id="044f8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="044f8-102">SYNOPSIS</span></span>
<span data-ttu-id="044f8-103">Stellt einen gelöschten schlüsseltresor in einen aktiven Zustand.</span><span class="sxs-lookup"><span data-stu-id="044f8-103">Recovers a deleted key vault into an active state.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="044f8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="044f8-104">SYNTAX</span></span>

### <span data-ttu-id="044f8-105">Standard (Standard)</span><span class="sxs-lookup"><span data-stu-id="044f8-105">Default (Default)</span></span>
```
Undo-AzureRmKeyVaultRemoval [-VaultName] <String> [-ResourceGroupName] <String> [-Location] <String>
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="044f8-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="044f8-106">InputObject</span></span>
```
Undo-AzureRmKeyVaultRemoval [-InputObject] <PSDeletedKeyVault> [-ResourceGroupName] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="044f8-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="044f8-107">DESCRIPTION</span></span>
<span data-ttu-id="044f8-108">Mit dem Cmdlet **"Undo-AzureRmKeyVaultRemoval"** wird ein zuvor gelöschter schlüsseltresor wiederhergestellt.</span><span class="sxs-lookup"><span data-stu-id="044f8-108">The **Undo-AzureRmKeyVaultRemoval** cmdlet will recover a previously deleted key vault.</span></span> <span data-ttu-id="044f8-109">Der wiederhergestellte Tresor wird nach der Wiederherstellung aktiviert.</span><span class="sxs-lookup"><span data-stu-id="044f8-109">The recovered vault will be active after recovery</span></span>

## <span data-ttu-id="044f8-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="044f8-110">EXAMPLES</span></span>

### <span data-ttu-id="044f8-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="044f8-111">Example 1</span></span>
```
PS C:\> Undo-AzureRmKeyVaultRemoval -VaultName 'MyKeyVault' -ResourceGroupName 'MyResourceGroup' -Location 'eastus2' -Tag @{"x"= "y"}
```

<span data-ttu-id="044f8-112">Mit diesem Befehl wird der schlüsseltresor "MyKeyVault" wiederhergestellt, der zuvor aus der eastus2-Region und der Ressourcengruppe "myresourcegroup" gelöscht wurde, in einen aktiven und nutzbaren Zustand.</span><span class="sxs-lookup"><span data-stu-id="044f8-112">This command will recover the key vault 'MyKeyVault' that was previously deleted from eastus2 region and 'MyResourceGroup' resource group, into an active and usable state.</span></span> <span data-ttu-id="044f8-113">Außerdem werden die Tags durch eine neue Kategorie ersetzt.</span><span class="sxs-lookup"><span data-stu-id="044f8-113">It also replaces the tags with new tag.</span></span>

## <span data-ttu-id="044f8-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="044f8-114">PARAMETERS</span></span>

### <span data-ttu-id="044f8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="044f8-115">-DefaultProfile</span></span>
<span data-ttu-id="044f8-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="044f8-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="044f8-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="044f8-117">-InputObject</span></span>
<span data-ttu-id="044f8-118">Vault-Objekt gelöscht</span><span class="sxs-lookup"><span data-stu-id="044f8-118">Deleted vault object</span></span>

```yaml
Type: PSDeletedKeyVault
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="044f8-119">-Standort</span><span class="sxs-lookup"><span data-stu-id="044f8-119">-Location</span></span>
<span data-ttu-id="044f8-120">Gibt den ursprünglichen Azure-Bereich für gelöschte Vaults an.</span><span class="sxs-lookup"><span data-stu-id="044f8-120">Specifies the deleted vault original Azure region.</span></span>

```yaml
Type: String
Parameter Sets: Default
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="044f8-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="044f8-121">-ResourceGroupName</span></span>
<span data-ttu-id="044f8-122">Gibt den Namen einer vorhandenen Ressourcengruppe an, in der der schlüsseltresor erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="044f8-122">Specifies the name of an existing resource group in which to create the key vault.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="044f8-123">-Tag</span><span class="sxs-lookup"><span data-stu-id="044f8-123">-Tag</span></span>
<span data-ttu-id="044f8-124">Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="044f8-124">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="044f8-125">Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="044f8-125">For example:</span></span>

<span data-ttu-id="044f8-126">@ {KEY0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="044f8-126">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="044f8-127">-Vaultname</span><span class="sxs-lookup"><span data-stu-id="044f8-127">-VaultName</span></span>
<span data-ttu-id="044f8-128">Vault-Name.</span><span class="sxs-lookup"><span data-stu-id="044f8-128">Vault name.</span></span>
<span data-ttu-id="044f8-129">Cmdlet erstellt den FQDN eines Tresors basierend auf dem Namen und der aktuell ausgewählten Umgebung.</span><span class="sxs-lookup"><span data-stu-id="044f8-129">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="044f8-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="044f8-130">-Confirm</span></span>
<span data-ttu-id="044f8-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="044f8-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="044f8-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="044f8-132">-WhatIf</span></span>
<span data-ttu-id="044f8-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="044f8-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="044f8-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="044f8-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="044f8-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="044f8-135">CommonParameters</span></span>
<span data-ttu-id="044f8-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="044f8-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="044f8-137">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="044f8-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="044f8-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="044f8-138">INPUTS</span></span>

### <span data-ttu-id="044f8-139">System. String</span><span class="sxs-lookup"><span data-stu-id="044f8-139">System.String</span></span>
<span data-ttu-id="044f8-140">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="044f8-140">System.Collections.Hashtable</span></span>

## <span data-ttu-id="044f8-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="044f8-141">OUTPUTS</span></span>

### <span data-ttu-id="044f8-142">Microsoft. Azure. Commands. keyvault. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="044f8-142">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="044f8-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="044f8-143">NOTES</span></span>

## <span data-ttu-id="044f8-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="044f8-144">RELATED LINKS</span></span>

[<span data-ttu-id="044f8-145">Remove-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="044f8-145">Remove-AzureRmKeyVault</span></span>](./Remove-AzureRmKeyVault.md)

[<span data-ttu-id="044f8-146">Neu – AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="044f8-146">New-AzureRmKeyVault</span></span>](./New-AzureRmKeyVault.md)

[<span data-ttu-id="044f8-147">Get-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="044f8-147">Get-AzureRmKeyVault</span></span>](./Get-AzureRmKeyVault.md)
