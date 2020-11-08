---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 7A929BA8-02D9-4BBE-AFF3-B8781F8DDAD9
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVault.md
ms.openlocfilehash: 69a1155b99d054699c41cc0b26cd78ef4445f931
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94175508"
---
# <span data-ttu-id="05b49-101">Remove-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="05b49-101">Remove-AzKeyVault</span></span>

## <span data-ttu-id="05b49-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="05b49-102">SYNOPSIS</span></span>
<span data-ttu-id="05b49-103">Löscht einen schlüsseltresor.</span><span class="sxs-lookup"><span data-stu-id="05b49-103">Deletes a key vault.</span></span>

## <span data-ttu-id="05b49-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="05b49-104">SYNTAX</span></span>

### <span data-ttu-id="05b49-105">ByAvailableVault (Standard)</span><span class="sxs-lookup"><span data-stu-id="05b49-105">ByAvailableVault (Default)</span></span>
```
Remove-AzKeyVault [-VaultName] <String> [[-ResourceGroupName] <String>] [[-Location] <String>] [-Force]
 [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="05b49-106">ByDeletedVault</span><span class="sxs-lookup"><span data-stu-id="05b49-106">ByDeletedVault</span></span>
```
Remove-AzKeyVault [-VaultName] <String> [-Location] <String> [-InRemovedState] [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="05b49-107">InputObjectByAvailableVault</span><span class="sxs-lookup"><span data-stu-id="05b49-107">InputObjectByAvailableVault</span></span>
```
Remove-AzKeyVault [-InputObject] <PSKeyVault> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="05b49-108">InputObjectByDeletedVault</span><span class="sxs-lookup"><span data-stu-id="05b49-108">InputObjectByDeletedVault</span></span>
```
Remove-AzKeyVault [-InputObject] <PSKeyVault> [-InRemovedState] [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="05b49-109">ResourceIdByAvailableVault</span><span class="sxs-lookup"><span data-stu-id="05b49-109">ResourceIdByAvailableVault</span></span>
```
Remove-AzKeyVault [-ResourceId] <String> [[-Location] <String>] [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="05b49-110">ResourceIdByDeletedVault</span><span class="sxs-lookup"><span data-stu-id="05b49-110">ResourceIdByDeletedVault</span></span>
```
Remove-AzKeyVault [-ResourceId] <String> [-Location] <String> [-InRemovedState] [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="05b49-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="05b49-111">DESCRIPTION</span></span>
<span data-ttu-id="05b49-112">Das Cmdlet **Remove-AzKeyVault** löscht den angegebenen schlüsseltresor.</span><span class="sxs-lookup"><span data-stu-id="05b49-112">The **Remove-AzKeyVault** cmdlet deletes the specified key vault.</span></span>
<span data-ttu-id="05b49-113">Außerdem werden alle Schlüssel und Geheimnisse gelöscht, die in dieser Instanz enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="05b49-113">It also deletes all keys and secrets contained in that instance.</span></span>
<span data-ttu-id="05b49-114">Beachten Sie, dass Sie eine bessere Leistung erzielen sollten, wenn Sie die Ressourcengruppe für dieses Cmdlet optional angeben.</span><span class="sxs-lookup"><span data-stu-id="05b49-114">Note that although specifying the resource group is optional for this cmdlet, you should so for better performance.</span></span>

## <span data-ttu-id="05b49-115">Beispiele</span><span class="sxs-lookup"><span data-stu-id="05b49-115">EXAMPLES</span></span>

### <span data-ttu-id="05b49-116">Beispiel 1: Entfernen eines Schlüsseldepots</span><span class="sxs-lookup"><span data-stu-id="05b49-116">Example 1: Remove a key vault</span></span>
```powershell
PS C:\> Remove-AzKeyVault -VaultName "Contoso03Vault" -PassThru

True
```

<span data-ttu-id="05b49-117">Mit diesem Befehl wird der schlüsseltresor mit dem Namen Contoso03Vault aus Ihrem aktuellen Abonnement entfernt.</span><span class="sxs-lookup"><span data-stu-id="05b49-117">This command removes the key vault named Contoso03Vault from your current subscription.</span></span>

### <span data-ttu-id="05b49-118">Beispiel 2: Entfernen eines Schlüsseldepots aus einer angegebenen Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="05b49-118">Example 2: Remove a key vault from a specified resource group</span></span>
```powershell
PS C:\> Remove-AzKeyVault -Name "Contoso03Vault" -ResourceGroupName "Group14" -PassThru

True
```

<span data-ttu-id="05b49-119">Mit diesem Befehl wird der schlüsseltresor mit dem Namen Contoso03Vault aus der benannten Ressourcengruppe entfernt.</span><span class="sxs-lookup"><span data-stu-id="05b49-119">This command removes the key vault named Contoso03Vault from the named resource group.</span></span>
<span data-ttu-id="05b49-120">Wenn Sie den Namen der Ressourcengruppe nicht angeben, sucht das Cmdlet nach dem benannten schlüsseltresor, der in Ihrem aktuellen Abonnement gelöscht werden soll.</span><span class="sxs-lookup"><span data-stu-id="05b49-120">If you do not specify the resource group name, the cmdlet searches for the named key vault to delete in your current subscription.</span></span>

### <span data-ttu-id="05b49-121">Beispiel 3: Entfernen eines verwalteten HSM</span><span class="sxs-lookup"><span data-stu-id="05b49-121">Example 3: Remove a managed hsm</span></span>
```powershell
PS C:\>  Remove-AzKeyVault -Name "testManagedHsm" -Hsm -PassThru

True
```

<span data-ttu-id="05b49-122">Dieser Befehl entfernt das verwaltete HSM mit dem Namen testManagedHsm aus Ihrem aktuellen Abonnement.</span><span class="sxs-lookup"><span data-stu-id="05b49-122">This command removes the managed hsm named testManagedHsm from your current subscription.</span></span>

## <span data-ttu-id="05b49-123">Parameter</span><span class="sxs-lookup"><span data-stu-id="05b49-123">PARAMETERS</span></span>

### <span data-ttu-id="05b49-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="05b49-124">-AsJob</span></span>
<span data-ttu-id="05b49-125">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="05b49-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="05b49-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05b49-126">-DefaultProfile</span></span>
<span data-ttu-id="05b49-127">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="05b49-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="05b49-128">-Force</span><span class="sxs-lookup"><span data-stu-id="05b49-128">-Force</span></span>
<span data-ttu-id="05b49-129">Gibt an, dass das Cmdlet Sie nicht zur Bestätigung auffordert.</span><span class="sxs-lookup"><span data-stu-id="05b49-129">Indicates that the cmdlet does not prompt you for confirmation.</span></span>
<span data-ttu-id="05b49-130">Standardmäßig werden Sie von diesem Cmdlet aufgefordert, zu bestätigen, dass Sie den schlüsseltresor löschen möchten.</span><span class="sxs-lookup"><span data-stu-id="05b49-130">By default, this cmdlet prompts you to confirm that you want to delete the key vault.</span></span>

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

### <span data-ttu-id="05b49-131">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="05b49-131">-InputObject</span></span>
<span data-ttu-id="05b49-132">Zentrales Vault-Objekt, das gelöscht werden soll</span><span class="sxs-lookup"><span data-stu-id="05b49-132">Key Vault object to be deleted.</span></span>

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

### <span data-ttu-id="05b49-133">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="05b49-133">-InRemovedState</span></span>
<span data-ttu-id="05b49-134">Entfernen Sie den zuvor gelöschten Tresor endgültig.</span><span class="sxs-lookup"><span data-stu-id="05b49-134">Remove the previously deleted vault permanently.</span></span>

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

### <span data-ttu-id="05b49-135">-Standort</span><span class="sxs-lookup"><span data-stu-id="05b49-135">-Location</span></span>
<span data-ttu-id="05b49-136">Der Speicherort des gelöschten Tresors.</span><span class="sxs-lookup"><span data-stu-id="05b49-136">The location of the deleted vault.</span></span>

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

### <span data-ttu-id="05b49-137">-PassThru</span><span class="sxs-lookup"><span data-stu-id="05b49-137">-PassThru</span></span>
<span data-ttu-id="05b49-138">Dieses Cmdlet gibt standardmäßig kein Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="05b49-138">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="05b49-139">Wenn dieser Schalter angegeben wird, wird true zurückgegeben, wenn er erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="05b49-139">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="05b49-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05b49-140">-ResourceGroupName</span></span>
<span data-ttu-id="05b49-141">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="05b49-141">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="05b49-142">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="05b49-142">-ResourceId</span></span>
<span data-ttu-id="05b49-143">Keyvault-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="05b49-143">KeyVault Resource Id.</span></span>

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

### <span data-ttu-id="05b49-144">-Vaultname</span><span class="sxs-lookup"><span data-stu-id="05b49-144">-VaultName</span></span>
<span data-ttu-id="05b49-145">Gibt den Namen des zu entfernenden Schlüsseldepots an.</span><span class="sxs-lookup"><span data-stu-id="05b49-145">Specifies the name of the key vault to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAvailableVault, ByDeletedVault
Aliases: Name

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05b49-146">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="05b49-146">-Confirm</span></span>
<span data-ttu-id="05b49-147">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="05b49-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="05b49-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="05b49-148">-WhatIf</span></span>
<span data-ttu-id="05b49-149">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="05b49-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="05b49-150">Das Cmdlet wird nicht ausgeführt. Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="05b49-150">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="05b49-151">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="05b49-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="05b49-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05b49-152">CommonParameters</span></span>
<span data-ttu-id="05b49-153">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="05b49-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05b49-154">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="05b49-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05b49-155">Eingaben</span><span class="sxs-lookup"><span data-stu-id="05b49-155">INPUTS</span></span>

### <span data-ttu-id="05b49-156">Microsoft. Azure. Commands. keyvault. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="05b49-156">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="05b49-157">System. String</span><span class="sxs-lookup"><span data-stu-id="05b49-157">System.String</span></span>

## <span data-ttu-id="05b49-158">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="05b49-158">OUTPUTS</span></span>

### <span data-ttu-id="05b49-159">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="05b49-159">System.Boolean</span></span>

## <span data-ttu-id="05b49-160">Notizen</span><span class="sxs-lookup"><span data-stu-id="05b49-160">NOTES</span></span>

## <span data-ttu-id="05b49-161">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="05b49-161">RELATED LINKS</span></span>

[<span data-ttu-id="05b49-162">Get-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="05b49-162">Get-AzKeyVault</span></span>](./Get-AzKeyVault.md)

[<span data-ttu-id="05b49-163">Neu – AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="05b49-163">New-AzKeyVault</span></span>](./New-AzKeyVault.md)
