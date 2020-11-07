---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 7A929BA8-02D9-4BBE-AFF3-B8781F8DDAD9
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVault.md
ms.openlocfilehash: 8332f4a5b14668a767ddf77e974a25a14ac884ce
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93650882"
---
# <span data-ttu-id="007de-101">Remove-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="007de-101">Remove-AzKeyVault</span></span>

## <span data-ttu-id="007de-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="007de-102">SYNOPSIS</span></span>
<span data-ttu-id="007de-103">Löscht einen schlüsseltresor.</span><span class="sxs-lookup"><span data-stu-id="007de-103">Deletes a key vault.</span></span>

## <span data-ttu-id="007de-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="007de-104">SYNTAX</span></span>

### <span data-ttu-id="007de-105">ByAvailableVault (Standard)</span><span class="sxs-lookup"><span data-stu-id="007de-105">ByAvailableVault (Default)</span></span>
```
Remove-AzKeyVault [-VaultName] <String> [[-ResourceGroupName] <String>] [[-Location] <String>] [-Force]
 [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="007de-106">ByDeletedVault</span><span class="sxs-lookup"><span data-stu-id="007de-106">ByDeletedVault</span></span>
```
Remove-AzKeyVault [-VaultName] <String> [-Location] <String> [-InRemovedState] [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="007de-107">InputObjectByAvailableVault</span><span class="sxs-lookup"><span data-stu-id="007de-107">InputObjectByAvailableVault</span></span>
```
Remove-AzKeyVault [-InputObject] <PSKeyVault> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="007de-108">InputObjectByDeletedVault</span><span class="sxs-lookup"><span data-stu-id="007de-108">InputObjectByDeletedVault</span></span>
```
Remove-AzKeyVault [-InputObject] <PSKeyVault> [-InRemovedState] [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="007de-109">ResourceIdByAvailableVault</span><span class="sxs-lookup"><span data-stu-id="007de-109">ResourceIdByAvailableVault</span></span>
```
Remove-AzKeyVault [-ResourceId] <String> [[-Location] <String>] [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="007de-110">ResourceIdByDeletedVault</span><span class="sxs-lookup"><span data-stu-id="007de-110">ResourceIdByDeletedVault</span></span>
```
Remove-AzKeyVault [-ResourceId] <String> [-Location] <String> [-InRemovedState] [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="007de-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="007de-111">DESCRIPTION</span></span>
<span data-ttu-id="007de-112">Das Cmdlet **Remove-AzKeyVault** löscht den angegebenen schlüsseltresor.</span><span class="sxs-lookup"><span data-stu-id="007de-112">The **Remove-AzKeyVault** cmdlet deletes the specified key vault.</span></span>
<span data-ttu-id="007de-113">Außerdem werden alle Schlüssel und Geheimnisse gelöscht, die in dieser Instanz enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="007de-113">It also deletes all keys and secrets contained in that instance.</span></span>
<span data-ttu-id="007de-114">Beachten Sie, dass Sie eine bessere Leistung erzielen sollten, wenn Sie die Ressourcengruppe für dieses Cmdlet optional angeben.</span><span class="sxs-lookup"><span data-stu-id="007de-114">Note that although specifying the resource group is optional for this cmdlet, you should so for better performance.</span></span>

## <span data-ttu-id="007de-115">Beispiele</span><span class="sxs-lookup"><span data-stu-id="007de-115">EXAMPLES</span></span>

### <span data-ttu-id="007de-116">Beispiel 1: Entfernen eines Schlüsseldepots</span><span class="sxs-lookup"><span data-stu-id="007de-116">Example 1: Remove a key vault</span></span>
```powershell
PS C:\> Remove-AzKeyVault -VaultName "Contoso03Vault" -PassThru

True
```

<span data-ttu-id="007de-117">Mit diesem Befehl wird der schlüsseltresor mit dem Namen Contoso03Vault aus Ihrem aktuellen Abonnement entfernt.</span><span class="sxs-lookup"><span data-stu-id="007de-117">This command removes the key vault named Contoso03Vault from your current subscription.</span></span>

### <span data-ttu-id="007de-118">Beispiel 2: Entfernen eines Schlüsseldepots aus einer angegebenen Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="007de-118">Example 2: Remove a key vault from a specified resource group</span></span>
```powershell
PS C:\> Remove-AzKeyVault -VaultName "Contoso03Vault" -ResourceGroupName "Group14" -PassThru

True
```

<span data-ttu-id="007de-119">Mit diesem Befehl wird der schlüsseltresor mit dem Namen Contoso03Vault aus der benannten Ressourcengruppe entfernt.</span><span class="sxs-lookup"><span data-stu-id="007de-119">This command removes the key vault named Contoso03Vault from the named resource group.</span></span>
<span data-ttu-id="007de-120">Wenn Sie den Namen der Ressourcengruppe nicht angeben, sucht das Cmdlet nach dem benannten schlüsseltresor, der in Ihrem aktuellen Abonnement gelöscht werden soll.</span><span class="sxs-lookup"><span data-stu-id="007de-120">If you do not specify the resource group name, the cmdlet searches for the named key vault to delete in your current subscription.</span></span>

## <span data-ttu-id="007de-121">Parameter</span><span class="sxs-lookup"><span data-stu-id="007de-121">PARAMETERS</span></span>

### <span data-ttu-id="007de-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="007de-122">-AsJob</span></span>
<span data-ttu-id="007de-123">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="007de-123">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="007de-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="007de-124">-DefaultProfile</span></span>
<span data-ttu-id="007de-125">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="007de-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="007de-126">-Force</span><span class="sxs-lookup"><span data-stu-id="007de-126">-Force</span></span>
<span data-ttu-id="007de-127">Gibt an, dass das Cmdlet Sie nicht zur Bestätigung auffordert.</span><span class="sxs-lookup"><span data-stu-id="007de-127">Indicates that the cmdlet does not prompt you for confirmation.</span></span>
<span data-ttu-id="007de-128">Standardmäßig werden Sie von diesem Cmdlet aufgefordert, zu bestätigen, dass Sie den schlüsseltresor löschen möchten.</span><span class="sxs-lookup"><span data-stu-id="007de-128">By default, this cmdlet prompts you to confirm that you want to delete the key vault.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="007de-129">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="007de-129">-InputObject</span></span>
<span data-ttu-id="007de-130">Zentrales Vault-Objekt, das gelöscht werden soll</span><span class="sxs-lookup"><span data-stu-id="007de-130">Key Vault object to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault
Parameter Sets: InputObjectByAvailableVault, InputObjectByDeletedVault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="007de-131">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="007de-131">-InRemovedState</span></span>
<span data-ttu-id="007de-132">Entfernen Sie den zuvor gelöschten Tresor endgültig.</span><span class="sxs-lookup"><span data-stu-id="007de-132">Remove the previously deleted vault permanently.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByDeletedVault, InputObjectByDeletedVault, ResourceIdByDeletedVault
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="007de-133">-Standort</span><span class="sxs-lookup"><span data-stu-id="007de-133">-Location</span></span>
<span data-ttu-id="007de-134">Der Speicherort des gelöschten Tresors.</span><span class="sxs-lookup"><span data-stu-id="007de-134">The location of the deleted vault.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAvailableVault, ResourceIdByAvailableVault
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByDeletedVault, ResourceIdByDeletedVault
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="007de-135">-PassThru</span><span class="sxs-lookup"><span data-stu-id="007de-135">-PassThru</span></span>
<span data-ttu-id="007de-136">Dieses Cmdlet gibt standardmäßig kein Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="007de-136">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="007de-137">Wenn dieser Schalter angegeben wird, wird true zurückgegeben, wenn er erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="007de-137">If this switch is specified, it returns true if successful.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="007de-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="007de-138">-ResourceGroupName</span></span>
<span data-ttu-id="007de-139">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="007de-139">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAvailableVault
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="007de-140">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="007de-140">-ResourceId</span></span>
<span data-ttu-id="007de-141">Keyvault-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="007de-141">KeyVault Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdByAvailableVault, ResourceIdByDeletedVault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="007de-142">-Vaultname</span><span class="sxs-lookup"><span data-stu-id="007de-142">-VaultName</span></span>
<span data-ttu-id="007de-143">Gibt den Namen des zu entfernenden Schlüsseldepots an.</span><span class="sxs-lookup"><span data-stu-id="007de-143">Specifies the name of the key vault to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAvailableVault, ByDeletedVault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="007de-144">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="007de-144">-Confirm</span></span>
<span data-ttu-id="007de-145">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="007de-145">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="007de-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="007de-146">-WhatIf</span></span>
<span data-ttu-id="007de-147">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="007de-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="007de-148">Das Cmdlet wird nicht ausgeführt. Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="007de-148">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="007de-149">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="007de-149">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="007de-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="007de-150">CommonParameters</span></span>
<span data-ttu-id="007de-151">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="007de-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="007de-152">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="007de-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="007de-153">Eingaben</span><span class="sxs-lookup"><span data-stu-id="007de-153">INPUTS</span></span>

### <span data-ttu-id="007de-154">Microsoft. Azure. Commands. keyvault. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="007de-154">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="007de-155">System. String</span><span class="sxs-lookup"><span data-stu-id="007de-155">System.String</span></span>

## <span data-ttu-id="007de-156">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="007de-156">OUTPUTS</span></span>

### <span data-ttu-id="007de-157">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="007de-157">System.Boolean</span></span>

## <span data-ttu-id="007de-158">Notizen</span><span class="sxs-lookup"><span data-stu-id="007de-158">NOTES</span></span>

## <span data-ttu-id="007de-159">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="007de-159">RELATED LINKS</span></span>

[<span data-ttu-id="007de-160">Get-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="007de-160">Get-AzKeyVault</span></span>](./Get-AzKeyVault.md)

[<span data-ttu-id="007de-161">Neu – AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="007de-161">New-AzKeyVault</span></span>](./New-AzKeyVault.md)
