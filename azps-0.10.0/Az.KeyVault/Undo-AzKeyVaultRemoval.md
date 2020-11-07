---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/undo-azkeyvaultremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Undo-AzKeyVaultRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Undo-AzKeyVaultRemoval.md
ms.openlocfilehash: fd2483925e8ab14772a3bf34d4411748583a03c9
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842084"
---
# <span data-ttu-id="4198b-101">Undo-AzKeyVaultRemoval</span><span class="sxs-lookup"><span data-stu-id="4198b-101">Undo-AzKeyVaultRemoval</span></span>

## <span data-ttu-id="4198b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4198b-102">SYNOPSIS</span></span>
<span data-ttu-id="4198b-103">Stellt einen gelöschten schlüsseltresor in einen aktiven Zustand.</span><span class="sxs-lookup"><span data-stu-id="4198b-103">Recovers a deleted key vault into an active state.</span></span>

## <span data-ttu-id="4198b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4198b-104">SYNTAX</span></span>

```
Undo-AzKeyVaultRemoval [-VaultName] <String> [-ResourceGroupName] <String> [-Location] <String>
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4198b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4198b-105">DESCRIPTION</span></span>
<span data-ttu-id="4198b-106">Mit dem Cmdlet **"Undo-AzKeyVaultRemoval"** wird ein zuvor gelöschter schlüsseltresor wiederhergestellt.</span><span class="sxs-lookup"><span data-stu-id="4198b-106">The **Undo-AzKeyVaultRemoval** cmdlet will recover a previously deleted key vault.</span></span> <span data-ttu-id="4198b-107">Der wiederhergestellte Tresor wird nach der Wiederherstellung aktiviert.</span><span class="sxs-lookup"><span data-stu-id="4198b-107">The recovered vault will be active after recovery</span></span>

## <span data-ttu-id="4198b-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4198b-108">EXAMPLES</span></span>

### <span data-ttu-id="4198b-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="4198b-109">Example 1</span></span>
```
PS C:\> Undo-AzKeyVaultRemoval -VaultName 'MyKeyVault' -ResourceGroupName 'MyResourceGroup' -Location 'eastus2' -Tag @{"x"= "y"}
```

<span data-ttu-id="4198b-110">Mit diesem Befehl wird der schlüsseltresor "MyKeyVault" wiederhergestellt, der zuvor aus der eastus2-Region und der Ressourcengruppe "myresourcegroup" gelöscht wurde, in einen aktiven und nutzbaren Zustand.</span><span class="sxs-lookup"><span data-stu-id="4198b-110">This command will recover the key vault 'MyKeyVault' that was previously deleted from eastus2 region and 'MyResourceGroup' resource group, into an active and usable state.</span></span> <span data-ttu-id="4198b-111">Außerdem werden die Tags durch eine neue Kategorie ersetzt.</span><span class="sxs-lookup"><span data-stu-id="4198b-111">It also replaces the tags with new tag.</span></span>

## <span data-ttu-id="4198b-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="4198b-112">PARAMETERS</span></span>

### <span data-ttu-id="4198b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4198b-113">-DefaultProfile</span></span>
<span data-ttu-id="4198b-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="4198b-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4198b-115">-Standort</span><span class="sxs-lookup"><span data-stu-id="4198b-115">-Location</span></span>
<span data-ttu-id="4198b-116">Gibt den ursprünglichen Azure-Bereich für gelöschte Vaults an.</span><span class="sxs-lookup"><span data-stu-id="4198b-116">Specifies the deleted vault original Azure region.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4198b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4198b-117">-ResourceGroupName</span></span>
<span data-ttu-id="4198b-118">Gibt den Namen einer vorhandenen Ressourcengruppe an, in der der schlüsseltresor erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="4198b-118">Specifies the name of an existing resource group in which to create the key vault.</span></span>

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

### <span data-ttu-id="4198b-119">-Tag</span><span class="sxs-lookup"><span data-stu-id="4198b-119">-Tag</span></span>
<span data-ttu-id="4198b-120">Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="4198b-120">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="4198b-121">Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="4198b-121">For example:</span></span>

<span data-ttu-id="4198b-122">@ {KEY0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="4198b-122">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="4198b-123">-Vaultname</span><span class="sxs-lookup"><span data-stu-id="4198b-123">-VaultName</span></span>
<span data-ttu-id="4198b-124">Vault-Name.</span><span class="sxs-lookup"><span data-stu-id="4198b-124">Vault name.</span></span>
<span data-ttu-id="4198b-125">Cmdlet erstellt den FQDN eines Tresors basierend auf dem Namen und der aktuell ausgewählten Umgebung.</span><span class="sxs-lookup"><span data-stu-id="4198b-125">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="4198b-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="4198b-126">-Confirm</span></span>
<span data-ttu-id="4198b-127">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4198b-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4198b-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4198b-128">-WhatIf</span></span>
<span data-ttu-id="4198b-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4198b-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4198b-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4198b-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4198b-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4198b-131">CommonParameters</span></span>
<span data-ttu-id="4198b-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4198b-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4198b-133">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4198b-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4198b-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4198b-134">INPUTS</span></span>

### <span data-ttu-id="4198b-135">System. String</span><span class="sxs-lookup"><span data-stu-id="4198b-135">System.String</span></span>
<span data-ttu-id="4198b-136">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="4198b-136">System.Collections.Hashtable</span></span>

## <span data-ttu-id="4198b-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4198b-137">OUTPUTS</span></span>

### <span data-ttu-id="4198b-138">Microsoft. Azure. Commands. keyvault. Models. PSVault</span><span class="sxs-lookup"><span data-stu-id="4198b-138">Microsoft.Azure.Commands.KeyVault.Models.PSVault</span></span>

## <span data-ttu-id="4198b-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="4198b-139">NOTES</span></span>

## <span data-ttu-id="4198b-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4198b-140">RELATED LINKS</span></span>

[<span data-ttu-id="4198b-141">Remove-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="4198b-141">Remove-AzKeyVault</span></span>](./Remove-AzKeyVault.md)

[<span data-ttu-id="4198b-142">Neu – AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="4198b-142">New-AzKeyVault</span></span>](./New-AzKeyVault.md)

[<span data-ttu-id="4198b-143">Get-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="4198b-143">Get-AzKeyVault</span></span>](./Get-AzKeyVault.md)
