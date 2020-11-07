---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 7A929BA8-02D9-4BBE-AFF3-B8781F8DDAD9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/remove-azurermkeyvault
schema: 2.0.0
ms.openlocfilehash: 2365a58093be3193c7ac285d6dd38fbaf769ccd4
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848208"
---
# <span data-ttu-id="80b3b-101">Remove-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="80b3b-101">Remove-AzureRmKeyVault</span></span>

## <span data-ttu-id="80b3b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="80b3b-102">SYNOPSIS</span></span>
<span data-ttu-id="80b3b-103">Löscht einen schlüsseltresor.</span><span class="sxs-lookup"><span data-stu-id="80b3b-103">Deletes a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="80b3b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="80b3b-104">SYNTAX</span></span>

### <span data-ttu-id="80b3b-105">ByAvailableVault</span><span class="sxs-lookup"><span data-stu-id="80b3b-105">ByAvailableVault</span></span>
```
Remove-AzureRmKeyVault [-VaultName] <String> [[-ResourceGroupName] <String>] [[-Location] <String>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="80b3b-106">ByDeletedVault</span><span class="sxs-lookup"><span data-stu-id="80b3b-106">ByDeletedVault</span></span>
```
Remove-AzureRmKeyVault [-VaultName] <String> [-Location] <String> [-Force] [-InRemovedState] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="80b3b-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="80b3b-107">DESCRIPTION</span></span>
<span data-ttu-id="80b3b-108">Das Cmdlet **Remove-AzureRmKeyVault** löscht den angegebenen schlüsseltresor.</span><span class="sxs-lookup"><span data-stu-id="80b3b-108">The **Remove-AzureRmKeyVault** cmdlet deletes the specified key vault.</span></span>
<span data-ttu-id="80b3b-109">Außerdem werden alle Schlüssel und Geheimnisse gelöscht, die in dieser Instanz enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="80b3b-109">It also deletes all keys and secrets contained in that instance.</span></span>

<span data-ttu-id="80b3b-110">Beachten Sie, dass Sie eine bessere Leistung erzielen sollten, wenn Sie die Ressourcengruppe für dieses Cmdlet optional angeben.</span><span class="sxs-lookup"><span data-stu-id="80b3b-110">Note that although specifying the resource group is optional for this cmdlet, you should so for better performance.</span></span>

## <span data-ttu-id="80b3b-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="80b3b-111">EXAMPLES</span></span>

### <span data-ttu-id="80b3b-112">Beispiel 1: Entfernen eines Schlüsseldepots</span><span class="sxs-lookup"><span data-stu-id="80b3b-112">Example 1: Remove a key vault</span></span>
```
PS C:\>Remove-AzureRmKeyVault -VaultName "Contoso03Vault"
```

<span data-ttu-id="80b3b-113">Mit diesem Befehl wird der schlüsseltresor mit dem Namen Contoso03Vault aus Ihrem aktuellen Abonnement entfernt.</span><span class="sxs-lookup"><span data-stu-id="80b3b-113">This command removes the key vault named Contoso03Vault from your current subscription.</span></span>

### <span data-ttu-id="80b3b-114">Beispiel 2: Entfernen eines Schlüsseldepots aus einer angegebenen Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="80b3b-114">Example 2: Remove a key vault from a specified resource group</span></span>
```
PS C:\>Remove-AzureRmKeyVault -VaultName "Contoso03Vault" -ResourceGroupName "Group14"
```

<span data-ttu-id="80b3b-115">Mit diesem Befehl wird der schlüsseltresor mit dem Namen Contoso03Vault aus der benannten Ressourcengruppe entfernt.</span><span class="sxs-lookup"><span data-stu-id="80b3b-115">This command removes the key vault named Contoso03Vault from the named resource group.</span></span>
<span data-ttu-id="80b3b-116">Wenn Sie den Namen der Ressourcengruppe nicht angeben, sucht das Cmdlet nach dem benannten schlüsseltresor, der in Ihrem aktuellen Abonnement gelöscht werden soll.</span><span class="sxs-lookup"><span data-stu-id="80b3b-116">If you do not specify the resource group name, the cmdlet searches for the named key vault to delete in your current subscription.</span></span>

## <span data-ttu-id="80b3b-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="80b3b-117">PARAMETERS</span></span>

### <span data-ttu-id="80b3b-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="80b3b-118">-AsJob</span></span>
<span data-ttu-id="80b3b-119">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="80b3b-119">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80b3b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80b3b-120">-DefaultProfile</span></span>
<span data-ttu-id="80b3b-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="80b3b-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="80b3b-122">-Force</span><span class="sxs-lookup"><span data-stu-id="80b3b-122">-Force</span></span>
<span data-ttu-id="80b3b-123">Gibt an, dass das Cmdlet Sie nicht zur Bestätigung auffordert.</span><span class="sxs-lookup"><span data-stu-id="80b3b-123">Indicates that the cmdlet does not prompt you for confirmation.</span></span>
<span data-ttu-id="80b3b-124">Standardmäßig werden Sie von diesem Cmdlet aufgefordert, zu bestätigen, dass Sie den schlüsseltresor löschen möchten.</span><span class="sxs-lookup"><span data-stu-id="80b3b-124">By default, this cmdlet prompts you to confirm that you want to delete the key vault.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80b3b-125">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="80b3b-125">-InRemovedState</span></span>
<span data-ttu-id="80b3b-126">Entfernen Sie den zuvor gelöschten Tresor endgültig.</span><span class="sxs-lookup"><span data-stu-id="80b3b-126">Remove the previously deleted vault permanently.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByDeletedVault
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80b3b-127">-Standort</span><span class="sxs-lookup"><span data-stu-id="80b3b-127">-Location</span></span>
<span data-ttu-id="80b3b-128">Der Speicherort des gelöschten Tresors.</span><span class="sxs-lookup"><span data-stu-id="80b3b-128">The location of the deleted vault.</span></span>

```yaml
Type: String
Parameter Sets: ByAvailableVault
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByDeletedVault
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80b3b-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="80b3b-129">-ResourceGroupName</span></span>
<span data-ttu-id="80b3b-130">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="80b3b-130">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: ByAvailableVault
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80b3b-131">-Vaultname</span><span class="sxs-lookup"><span data-stu-id="80b3b-131">-VaultName</span></span>
<span data-ttu-id="80b3b-132">Gibt den Namen des zu entfernenden Schlüsseldepots an.</span><span class="sxs-lookup"><span data-stu-id="80b3b-132">Specifies the name of the key vault to remove.</span></span>

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

### <span data-ttu-id="80b3b-133">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="80b3b-133">-Confirm</span></span>
<span data-ttu-id="80b3b-134">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="80b3b-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80b3b-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="80b3b-135">-WhatIf</span></span>
<span data-ttu-id="80b3b-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="80b3b-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="80b3b-137">Das Cmdlet wird nicht ausgeführt. Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="80b3b-137">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="80b3b-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="80b3b-138">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80b3b-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80b3b-139">CommonParameters</span></span>
<span data-ttu-id="80b3b-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="80b3b-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80b3b-141">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="80b3b-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80b3b-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="80b3b-142">INPUTS</span></span>

## <span data-ttu-id="80b3b-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="80b3b-143">OUTPUTS</span></span>

## <span data-ttu-id="80b3b-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="80b3b-144">NOTES</span></span>

## <span data-ttu-id="80b3b-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="80b3b-145">RELATED LINKS</span></span>

[<span data-ttu-id="80b3b-146">Get-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="80b3b-146">Get-AzureRmKeyVault</span></span>](./Get-AzureRmKeyVault.md)

[<span data-ttu-id="80b3b-147">Neu – AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="80b3b-147">New-AzureRmKeyVault</span></span>](./New-AzureRmKeyVault.md)
