---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 7A929BA8-02D9-4BBE-AFF3-B8781F8DDAD9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/remove-azurermkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureRmKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureRmKeyVault.md
ms.openlocfilehash: 0c9e37433d28a16a28ca56daf4a726347b7a9533
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663061"
---
# <span data-ttu-id="685c4-101">Remove-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="685c4-101">Remove-AzureRmKeyVault</span></span>

## <span data-ttu-id="685c4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="685c4-102">SYNOPSIS</span></span>
<span data-ttu-id="685c4-103">Löscht einen schlüsseltresor.</span><span class="sxs-lookup"><span data-stu-id="685c4-103">Deletes a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="685c4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="685c4-104">SYNTAX</span></span>

### <span data-ttu-id="685c4-105">ByAvailableVault (Standard)</span><span class="sxs-lookup"><span data-stu-id="685c4-105">ByAvailableVault (Default)</span></span>
```
Remove-AzureRmKeyVault [-VaultName] <String> [[-ResourceGroupName] <String>] [[-Location] <String>] [-Force]
 [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="685c4-106">ByDeletedVault</span><span class="sxs-lookup"><span data-stu-id="685c4-106">ByDeletedVault</span></span>
```
Remove-AzureRmKeyVault [-VaultName] <String> [-Location] <String> [-InRemovedState] [-Force] [-AsJob]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="685c4-107">InputObjectByAvailableVault</span><span class="sxs-lookup"><span data-stu-id="685c4-107">InputObjectByAvailableVault</span></span>
```
Remove-AzureRmKeyVault [-InputObject] <PSKeyVault> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="685c4-108">InputObjectByDeletedVault</span><span class="sxs-lookup"><span data-stu-id="685c4-108">InputObjectByDeletedVault</span></span>
```
Remove-AzureRmKeyVault [-InputObject] <PSKeyVault> [-InRemovedState] [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="685c4-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="685c4-109">DESCRIPTION</span></span>
<span data-ttu-id="685c4-110">Das Cmdlet **Remove-AzureRmKeyVault** löscht den angegebenen schlüsseltresor.</span><span class="sxs-lookup"><span data-stu-id="685c4-110">The **Remove-AzureRmKeyVault** cmdlet deletes the specified key vault.</span></span>
<span data-ttu-id="685c4-111">Außerdem werden alle Schlüssel und Geheimnisse gelöscht, die in dieser Instanz enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="685c4-111">It also deletes all keys and secrets contained in that instance.</span></span>

<span data-ttu-id="685c4-112">Beachten Sie, dass Sie eine bessere Leistung erzielen sollten, wenn Sie die Ressourcengruppe für dieses Cmdlet optional angeben.</span><span class="sxs-lookup"><span data-stu-id="685c4-112">Note that although specifying the resource group is optional for this cmdlet, you should so for better performance.</span></span>

## <span data-ttu-id="685c4-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="685c4-113">EXAMPLES</span></span>

### <span data-ttu-id="685c4-114">Beispiel 1: Entfernen eines Schlüsseldepots</span><span class="sxs-lookup"><span data-stu-id="685c4-114">Example 1: Remove a key vault</span></span>
```
PS C:\>Remove-AzureRmKeyVault -VaultName "Contoso03Vault"
```

<span data-ttu-id="685c4-115">Mit diesem Befehl wird der schlüsseltresor mit dem Namen Contoso03Vault aus Ihrem aktuellen Abonnement entfernt.</span><span class="sxs-lookup"><span data-stu-id="685c4-115">This command removes the key vault named Contoso03Vault from your current subscription.</span></span>

### <span data-ttu-id="685c4-116">Beispiel 2: Entfernen eines Schlüsseldepots aus einer angegebenen Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="685c4-116">Example 2: Remove a key vault from a specified resource group</span></span>
```
PS C:\>Remove-AzureRmKeyVault -VaultName "Contoso03Vault" -ResourceGroupName "Group14"
```

<span data-ttu-id="685c4-117">Mit diesem Befehl wird der schlüsseltresor mit dem Namen Contoso03Vault aus der benannten Ressourcengruppe entfernt.</span><span class="sxs-lookup"><span data-stu-id="685c4-117">This command removes the key vault named Contoso03Vault from the named resource group.</span></span>
<span data-ttu-id="685c4-118">Wenn Sie den Namen der Ressourcengruppe nicht angeben, sucht das Cmdlet nach dem benannten schlüsseltresor, der in Ihrem aktuellen Abonnement gelöscht werden soll.</span><span class="sxs-lookup"><span data-stu-id="685c4-118">If you do not specify the resource group name, the cmdlet searches for the named key vault to delete in your current subscription.</span></span>

## <span data-ttu-id="685c4-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="685c4-119">PARAMETERS</span></span>

### <span data-ttu-id="685c4-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="685c4-120">-AsJob</span></span>
<span data-ttu-id="685c4-121">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="685c4-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="685c4-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="685c4-122">-DefaultProfile</span></span>
<span data-ttu-id="685c4-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="685c4-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="685c4-124">-Force</span><span class="sxs-lookup"><span data-stu-id="685c4-124">-Force</span></span>
<span data-ttu-id="685c4-125">Gibt an, dass das Cmdlet Sie nicht zur Bestätigung auffordert.</span><span class="sxs-lookup"><span data-stu-id="685c4-125">Indicates that the cmdlet does not prompt you for confirmation.</span></span>
<span data-ttu-id="685c4-126">Standardmäßig werden Sie von diesem Cmdlet aufgefordert, zu bestätigen, dass Sie den schlüsseltresor löschen möchten.</span><span class="sxs-lookup"><span data-stu-id="685c4-126">By default, this cmdlet prompts you to confirm that you want to delete the key vault.</span></span>

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

### <span data-ttu-id="685c4-127">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="685c4-127">-InputObject</span></span>
<span data-ttu-id="685c4-128">Zentrales Vault-Objekt, das gelöscht werden soll</span><span class="sxs-lookup"><span data-stu-id="685c4-128">Key Vault object to be deleted.</span></span>

```yaml
Type: PSKeyVault
Parameter Sets: InputObjectByAvailableVault, InputObjectByDeletedVault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="685c4-129">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="685c4-129">-InRemovedState</span></span>
<span data-ttu-id="685c4-130">Entfernen Sie den zuvor gelöschten Tresor endgültig.</span><span class="sxs-lookup"><span data-stu-id="685c4-130">Remove the previously deleted vault permanently.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByDeletedVault, InputObjectByDeletedVault
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="685c4-131">-Standort</span><span class="sxs-lookup"><span data-stu-id="685c4-131">-Location</span></span>
<span data-ttu-id="685c4-132">Der Speicherort des gelöschten Tresors.</span><span class="sxs-lookup"><span data-stu-id="685c4-132">The location of the deleted vault.</span></span>

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

### <span data-ttu-id="685c4-133">-PassThru</span><span class="sxs-lookup"><span data-stu-id="685c4-133">-PassThru</span></span>
<span data-ttu-id="685c4-134">Dieses Cmdlet gibt standardmäßig kein Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="685c4-134">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="685c4-135">Wenn dieser Schalter angegeben wird, wird true zurückgegeben, wenn er erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="685c4-135">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="685c4-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="685c4-136">-ResourceGroupName</span></span>
<span data-ttu-id="685c4-137">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="685c4-137">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="685c4-138">-Vaultname</span><span class="sxs-lookup"><span data-stu-id="685c4-138">-VaultName</span></span>
<span data-ttu-id="685c4-139">Gibt den Namen des zu entfernenden Schlüsseldepots an.</span><span class="sxs-lookup"><span data-stu-id="685c4-139">Specifies the name of the key vault to remove.</span></span>

```yaml
Type: String
Parameter Sets: ByAvailableVault, ByDeletedVault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="685c4-140">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="685c4-140">-Confirm</span></span>
<span data-ttu-id="685c4-141">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="685c4-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="685c4-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="685c4-142">-WhatIf</span></span>
<span data-ttu-id="685c4-143">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="685c4-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="685c4-144">Das Cmdlet wird nicht ausgeführt. Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="685c4-144">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="685c4-145">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="685c4-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="685c4-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="685c4-146">CommonParameters</span></span>
<span data-ttu-id="685c4-147">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="685c4-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="685c4-148">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="685c4-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="685c4-149">Eingaben</span><span class="sxs-lookup"><span data-stu-id="685c4-149">INPUTS</span></span>

### <span data-ttu-id="685c4-150">Keine</span><span class="sxs-lookup"><span data-stu-id="685c4-150">None</span></span>
<span data-ttu-id="685c4-151">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="685c4-151">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="685c4-152">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="685c4-152">OUTPUTS</span></span>

### <span data-ttu-id="685c4-153">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="685c4-153">System.Boolean</span></span>

## <span data-ttu-id="685c4-154">Notizen</span><span class="sxs-lookup"><span data-stu-id="685c4-154">NOTES</span></span>

## <span data-ttu-id="685c4-155">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="685c4-155">RELATED LINKS</span></span>

[<span data-ttu-id="685c4-156">Get-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="685c4-156">Get-AzureRmKeyVault</span></span>](./Get-AzureRmKeyVault.md)

[<span data-ttu-id="685c4-157">Neu – AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="685c4-157">New-AzureRmKeyVault</span></span>](./New-AzureRmKeyVault.md)
