---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 7A929BA8-02D9-4BBE-AFF3-B8781F8DDAD9
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVault.md
ms.openlocfilehash: 69a1155b99d054699c41cc0b26cd78ef4445f931
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98472469"
---
# <span data-ttu-id="dca86-101">Remove-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="dca86-101">Remove-AzKeyVault</span></span>

## <span data-ttu-id="dca86-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dca86-102">SYNOPSIS</span></span>
<span data-ttu-id="dca86-103">Löscht einen Schlüsseltresor.</span><span class="sxs-lookup"><span data-stu-id="dca86-103">Deletes a key vault.</span></span>

## <span data-ttu-id="dca86-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="dca86-104">SYNTAX</span></span>

### <span data-ttu-id="dca86-105">ByAvailableVault (Standard)</span><span class="sxs-lookup"><span data-stu-id="dca86-105">ByAvailableVault (Default)</span></span>
```
Remove-AzKeyVault [-VaultName] <String> [[-ResourceGroupName] <String>] [[-Location] <String>] [-Force]
 [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dca86-106">ByDeletedVault</span><span class="sxs-lookup"><span data-stu-id="dca86-106">ByDeletedVault</span></span>
```
Remove-AzKeyVault [-VaultName] <String> [-Location] <String> [-InRemovedState] [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dca86-107">InputObjectByAvailableVault</span><span class="sxs-lookup"><span data-stu-id="dca86-107">InputObjectByAvailableVault</span></span>
```
Remove-AzKeyVault [-InputObject] <PSKeyVault> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dca86-108">InputObjectByDeletedVault</span><span class="sxs-lookup"><span data-stu-id="dca86-108">InputObjectByDeletedVault</span></span>
```
Remove-AzKeyVault [-InputObject] <PSKeyVault> [-InRemovedState] [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dca86-109">ResourceIdByAvailableVault</span><span class="sxs-lookup"><span data-stu-id="dca86-109">ResourceIdByAvailableVault</span></span>
```
Remove-AzKeyVault [-ResourceId] <String> [[-Location] <String>] [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dca86-110">ResourceIdByDeletedVault</span><span class="sxs-lookup"><span data-stu-id="dca86-110">ResourceIdByDeletedVault</span></span>
```
Remove-AzKeyVault [-ResourceId] <String> [-Location] <String> [-InRemovedState] [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dca86-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="dca86-111">DESCRIPTION</span></span>
<span data-ttu-id="dca86-112">Das **Cmdlet "Remove-AzKeyVault"** löscht den angegebenen Schlüsseltresor.</span><span class="sxs-lookup"><span data-stu-id="dca86-112">The **Remove-AzKeyVault** cmdlet deletes the specified key vault.</span></span>
<span data-ttu-id="dca86-113">Außerdem werden alle schlüssel- und geheimen Schlüssel gelöscht, die in dieser Instanz enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="dca86-113">It also deletes all keys and secrets contained in that instance.</span></span>
<span data-ttu-id="dca86-114">Beachten Sie: Obwohl die Angabe der Ressourcengruppe für dieses Cmdlet optional ist, sollten Sie dies für eine bessere Leistung tun.</span><span class="sxs-lookup"><span data-stu-id="dca86-114">Note that although specifying the resource group is optional for this cmdlet, you should so for better performance.</span></span>

## <span data-ttu-id="dca86-115">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="dca86-115">EXAMPLES</span></span>

### <span data-ttu-id="dca86-116">Beispiel 1: Entfernen eines Schlüsseltresor</span><span class="sxs-lookup"><span data-stu-id="dca86-116">Example 1: Remove a key vault</span></span>
```powershell
PS C:\> Remove-AzKeyVault -VaultName "Contoso03Vault" -PassThru

True
```

<span data-ttu-id="dca86-117">Mit diesem Befehl wird der Schlüsseltresor "Contoso03Vault" aus Ihrem aktuellen Abonnement entfernt.</span><span class="sxs-lookup"><span data-stu-id="dca86-117">This command removes the key vault named Contoso03Vault from your current subscription.</span></span>

### <span data-ttu-id="dca86-118">Beispiel 2: Entfernen eines Schlüsseltresor aus einer bestimmten Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="dca86-118">Example 2: Remove a key vault from a specified resource group</span></span>
```powershell
PS C:\> Remove-AzKeyVault -Name "Contoso03Vault" -ResourceGroupName "Group14" -PassThru

True
```

<span data-ttu-id="dca86-119">Mit diesem Befehl wird der Schlüsseltresor "Contoso03Vault" aus der benannten Ressourcengruppe entfernt.</span><span class="sxs-lookup"><span data-stu-id="dca86-119">This command removes the key vault named Contoso03Vault from the named resource group.</span></span>
<span data-ttu-id="dca86-120">Wenn Sie den Namen der Ressourcengruppe nicht angeben, sucht das Cmdlet nach dem benannten Schlüsseltresor, der in Ihrem aktuellen Abonnement gelöscht werden soll.</span><span class="sxs-lookup"><span data-stu-id="dca86-120">If you do not specify the resource group name, the cmdlet searches for the named key vault to delete in your current subscription.</span></span>

### <span data-ttu-id="dca86-121">Beispiel 3: Entfernen eines verwalteten HSM</span><span class="sxs-lookup"><span data-stu-id="dca86-121">Example 3: Remove a managed hsm</span></span>
```powershell
PS C:\>  Remove-AzKeyVault -Name "testManagedHsm" -Hsm -PassThru

True
```

<span data-ttu-id="dca86-122">Mit diesem Befehl wird der verwaltete hsm namens "testManagedHsm" aus Ihrem aktuellen Abonnement entfernt.</span><span class="sxs-lookup"><span data-stu-id="dca86-122">This command removes the managed hsm named testManagedHsm from your current subscription.</span></span>

## <span data-ttu-id="dca86-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dca86-123">PARAMETERS</span></span>

### <span data-ttu-id="dca86-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dca86-124">-AsJob</span></span>
<span data-ttu-id="dca86-125">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="dca86-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="dca86-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dca86-126">-DefaultProfile</span></span>
<span data-ttu-id="dca86-127">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="dca86-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dca86-128">-Force</span><span class="sxs-lookup"><span data-stu-id="dca86-128">-Force</span></span>
<span data-ttu-id="dca86-129">Zeigt an, dass sie vom Cmdlet nicht zur Bestätigung aufgefordert werden.</span><span class="sxs-lookup"><span data-stu-id="dca86-129">Indicates that the cmdlet does not prompt you for confirmation.</span></span>
<span data-ttu-id="dca86-130">Standardmäßig werden Sie von diesem Cmdlet aufgefordert zu bestätigen, dass Sie den Schlüsseltresor löschen möchten.</span><span class="sxs-lookup"><span data-stu-id="dca86-130">By default, this cmdlet prompts you to confirm that you want to delete the key vault.</span></span>

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

### <span data-ttu-id="dca86-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dca86-131">-InputObject</span></span>
<span data-ttu-id="dca86-132">Key Vault-Objekt, das gelöscht werden soll.</span><span class="sxs-lookup"><span data-stu-id="dca86-132">Key Vault object to be deleted.</span></span>

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

### <span data-ttu-id="dca86-133">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="dca86-133">-InRemovedState</span></span>
<span data-ttu-id="dca86-134">Entfernen Sie den zuvor gelöschten Tresor dauerhaft.</span><span class="sxs-lookup"><span data-stu-id="dca86-134">Remove the previously deleted vault permanently.</span></span>

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

### <span data-ttu-id="dca86-135">-Location</span><span class="sxs-lookup"><span data-stu-id="dca86-135">-Location</span></span>
<span data-ttu-id="dca86-136">Der Speicherort des gelöschten Tresors.</span><span class="sxs-lookup"><span data-stu-id="dca86-136">The location of the deleted vault.</span></span>

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

### <span data-ttu-id="dca86-137">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dca86-137">-PassThru</span></span>
<span data-ttu-id="dca86-138">Dieses Cmdlet gibt standardmäßig kein Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="dca86-138">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="dca86-139">Wenn dieser Schalter angegeben ist, wird "true" zurückgegeben, wenn er erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="dca86-139">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="dca86-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dca86-140">-ResourceGroupName</span></span>
<span data-ttu-id="dca86-141">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="dca86-141">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="dca86-142">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dca86-142">-ResourceId</span></span>
<span data-ttu-id="dca86-143">KeyVault-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="dca86-143">KeyVault Resource Id.</span></span>

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

### <span data-ttu-id="dca86-144">-VaultName</span><span class="sxs-lookup"><span data-stu-id="dca86-144">-VaultName</span></span>
<span data-ttu-id="dca86-145">Gibt den Namen des zu entfernenden Schlüsseltresor an.</span><span class="sxs-lookup"><span data-stu-id="dca86-145">Specifies the name of the key vault to remove.</span></span>

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

### <span data-ttu-id="dca86-146">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dca86-146">-Confirm</span></span>
<span data-ttu-id="dca86-147">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="dca86-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dca86-148">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="dca86-148">-WhatIf</span></span>
<span data-ttu-id="dca86-149">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="dca86-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dca86-150">Das Cmdlet wird nicht ausgeführt. Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="dca86-150">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dca86-151">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="dca86-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dca86-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dca86-152">CommonParameters</span></span>
<span data-ttu-id="dca86-153">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dca86-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dca86-154">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="dca86-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dca86-155">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="dca86-155">INPUTS</span></span>

### <span data-ttu-id="dca86-156">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="dca86-156">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="dca86-157">System.String</span><span class="sxs-lookup"><span data-stu-id="dca86-157">System.String</span></span>

## <span data-ttu-id="dca86-158">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="dca86-158">OUTPUTS</span></span>

### <span data-ttu-id="dca86-159">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="dca86-159">System.Boolean</span></span>

## <span data-ttu-id="dca86-160">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="dca86-160">NOTES</span></span>

## <span data-ttu-id="dca86-161">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="dca86-161">RELATED LINKS</span></span>

[<span data-ttu-id="dca86-162">Get-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="dca86-162">Get-AzKeyVault</span></span>](./Get-AzKeyVault.md)

[<span data-ttu-id="dca86-163">New-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="dca86-163">New-AzKeyVault</span></span>](./New-AzKeyVault.md)
