---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 817BF177-519F-47BA-86CF-4591FB402E2Dl
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultKey.md
ms.openlocfilehash: e78b6729061efe5a83f31bd25b9e542c09627ca3
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98472355"
---
# <span data-ttu-id="5d50d-101">Remove-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="5d50d-101">Remove-AzKeyVaultKey</span></span>

## <span data-ttu-id="5d50d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5d50d-102">SYNOPSIS</span></span>
<span data-ttu-id="5d50d-103">Löscht einen Schlüssel in einem Schlüsseltresor.</span><span class="sxs-lookup"><span data-stu-id="5d50d-103">Deletes a key in a key vault.</span></span>

## <span data-ttu-id="5d50d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5d50d-104">SYNTAX</span></span>

### <span data-ttu-id="5d50d-105">ByVaultName (Standard)</span><span class="sxs-lookup"><span data-stu-id="5d50d-105">ByVaultName (Default)</span></span>
```
Remove-AzKeyVaultKey [-VaultName] <String> [-Name] <String> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5d50d-106">HsmByVaultName</span><span class="sxs-lookup"><span data-stu-id="5d50d-106">HsmByVaultName</span></span>
```
Remove-AzKeyVaultKey -HsmName <String> [-Name] <String> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5d50d-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="5d50d-107">ByInputObject</span></span>
```
Remove-AzKeyVaultKey [-InputObject] <PSKeyVaultKeyIdentityItem> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5d50d-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5d50d-108">DESCRIPTION</span></span>
<span data-ttu-id="5d50d-109">Das Remove-AzKeyVaultKey cmdlet löscht einen Schlüssel in einem Schlüsseltresor.</span><span class="sxs-lookup"><span data-stu-id="5d50d-109">The Remove-AzKeyVaultKey cmdlet deletes a key in a key vault.</span></span>
<span data-ttu-id="5d50d-110">Wenn der Schlüssel versehentlich gelöscht wurde, kann der Schlüssel mithilfe von Undo-AzKeyVaultKeyRemoval einem Benutzer mit speziellen "Wiederherstellen"-Berechtigungen wiederhergestellt werden.</span><span class="sxs-lookup"><span data-stu-id="5d50d-110">If the key was accidentally deleted the key can be recovered using Undo-AzKeyVaultKeyRemoval by a user with special 'recover' permissions.</span></span>
<span data-ttu-id="5d50d-111">Dieses Cmdlet hat den Wert "High" für die **"ConfirmImpact"-Eigenschaft.**</span><span class="sxs-lookup"><span data-stu-id="5d50d-111">This cmdlet has a value of high for the **ConfirmImpact** property.</span></span>

## <span data-ttu-id="5d50d-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="5d50d-112">EXAMPLES</span></span>

### <span data-ttu-id="5d50d-113">Beispiel 1: Entfernen eines Schlüssels aus einem Schlüsseltresor</span><span class="sxs-lookup"><span data-stu-id="5d50d-113">Example 1: Remove a key from a key vault</span></span>
```powershell
PS C:\> Remove-AzKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware' -PassThru

Vault Name           : contoso
Name                 : key2
Id                   : https://contoso.vault.azure.net:443/keys/itsoftware/fdad15793ba0437e960497908ef9eb32
Deleted Date         : 5/24/2018 11:28:25 PM
Scheduled Purge Date : 8/22/2018 11:28:25 PM
Enabled              : False
Expires              : 10/11/2018 11:32:49 PM
Not Before           : 4/11/2018 11:22:49 PM
Created              : 4/12/2018 10:16:38 PM
Updated              : 4/12/2018 10:16:38 PM
Purge Disabled       : False
Tags                 :
```

<span data-ttu-id="5d50d-114">Mit diesem Befehl wird der Schlüssel "ITSoftware" aus dem Schlüsseltresor "Contoso" entfernt.</span><span class="sxs-lookup"><span data-stu-id="5d50d-114">This command removes the key named ITSoftware from the key vault named Contoso.</span></span>

### <span data-ttu-id="5d50d-115">Beispiel 2: Entfernen eines Schlüssels ohne Benutzerbestätigung</span><span class="sxs-lookup"><span data-stu-id="5d50d-115">Example 2: Remove a key without user confirmation</span></span>
```powershell
PS C:\> Remove-AzKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware' -Force
```

<span data-ttu-id="5d50d-116">Mit diesem Befehl wird der Schlüssel "ITSoftware" aus dem Schlüsseltresor "Contoso" entfernt.</span><span class="sxs-lookup"><span data-stu-id="5d50d-116">This command removes the key named ITSoftware from the key vault named Contoso.</span></span>
<span data-ttu-id="5d50d-117">Der Befehl gibt den Parameter *"Force"* an, daher fordert Sie das Cmdlet nicht zur Bestätigung auf.</span><span class="sxs-lookup"><span data-stu-id="5d50d-117">The command specifies the *Force* parameter, and, therefore, the cmdlet does not prompt you for confirmation.</span></span>

### <span data-ttu-id="5d50d-118">Beispiel 3: Endgültiges Löschen eines gelöschten Schlüssels aus dem Schlüsseltresor</span><span class="sxs-lookup"><span data-stu-id="5d50d-118">Example 3: Purge a deleted key from the key vault permanently</span></span>
```powershell
PS C:\> Remove-AzKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware' -InRemovedState
```

<span data-ttu-id="5d50d-119">Mit diesem Befehl wird der Schlüssel "ITSoftware" aus dem Schlüsseltresor "Contoso" dauerhaft entfernt.</span><span class="sxs-lookup"><span data-stu-id="5d50d-119">This command removes the key named ITSoftware from the key vault named Contoso permanently.</span></span>
<span data-ttu-id="5d50d-120">Zum Ausführen dieses Cmdlets ist die Berechtigung "Löschen" erforderlich, die zuvor und explizit dem Benutzer für diesen Schlüsseltresor gewährt worden sein muss.</span><span class="sxs-lookup"><span data-stu-id="5d50d-120">Executing this cmdlet requires the 'purge' permission, which must have been previously and explicitly granted to the user for this key vault.</span></span>

### <span data-ttu-id="5d50d-121">Beispiel 4: Entfernen von Schlüsseln mithilfe des Pipelineoperators</span><span class="sxs-lookup"><span data-stu-id="5d50d-121">Example 4: Remove keys by using the pipeline operator</span></span>
```powershell
PS C:\> Get-AzKeyVaultKey -VaultName 'Contoso' | Where-Object {$_.Attributes.Enabled -eq $False} | Remove-AzKeyVaultKey
```

<span data-ttu-id="5d50d-122">Dieser Befehl ruft alle Schlüssel im Schlüsseltresor "Contoso" ab und übergibt sie mithilfe des Pipelineoperators an das **Where-Object-Cmdlet.**</span><span class="sxs-lookup"><span data-stu-id="5d50d-122">This command gets all the keys in the key vault named Contoso, and passes them to the **Where-Object** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="5d50d-123">Dieses Cmdlet übergibt die Schlüssel mit dem Wert $False für das Attribut **"Enabled"** an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5d50d-123">That cmdlet passes the keys that have a value of $False for the **Enabled** attribute to the current cmdlet.</span></span>
<span data-ttu-id="5d50d-124">Mit diesem Cmdlet werden diese Schlüssel entfernt.</span><span class="sxs-lookup"><span data-stu-id="5d50d-124">That cmdlet removes those keys.</span></span>

## <span data-ttu-id="5d50d-125">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5d50d-125">PARAMETERS</span></span>

### <span data-ttu-id="5d50d-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d50d-126">-DefaultProfile</span></span>
<span data-ttu-id="5d50d-127">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="5d50d-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5d50d-128">-Force</span><span class="sxs-lookup"><span data-stu-id="5d50d-128">-Force</span></span>
<span data-ttu-id="5d50d-129">Erzwingt die Ausführung des Befehls ohne Benutzerbestätigung.</span><span class="sxs-lookup"><span data-stu-id="5d50d-129">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="5d50d-130">-HsmName</span><span class="sxs-lookup"><span data-stu-id="5d50d-130">-HsmName</span></span>
<span data-ttu-id="5d50d-131">HSM-Name.</span><span class="sxs-lookup"><span data-stu-id="5d50d-131">HSM name.</span></span> <span data-ttu-id="5d50d-132">Das Cmdlet erstellt den FQDN eines verwalteten HSM basierend auf dem Namen und der aktuell ausgewählten Umgebung.</span><span class="sxs-lookup"><span data-stu-id="5d50d-132">Cmdlet constructs the FQDN of a managed HSM based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: HsmByVaultName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d50d-133">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5d50d-133">-InputObject</span></span>
<span data-ttu-id="5d50d-134">KeyBundle-Objekt</span><span class="sxs-lookup"><span data-stu-id="5d50d-134">KeyBundle Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5d50d-135">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="5d50d-135">-InRemovedState</span></span>
<span data-ttu-id="5d50d-136">Entfernen Sie den zuvor gelöschten Schlüssel dauerhaft.</span><span class="sxs-lookup"><span data-stu-id="5d50d-136">Remove the previously deleted key permanently.</span></span>

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

### <span data-ttu-id="5d50d-137">-Name</span><span class="sxs-lookup"><span data-stu-id="5d50d-137">-Name</span></span>
<span data-ttu-id="5d50d-138">Gibt den Namen des zu entfernenden Schlüssels an.</span><span class="sxs-lookup"><span data-stu-id="5d50d-138">Specifies the name of the key to remove.</span></span>
<span data-ttu-id="5d50d-139">Dieses Cmdlet erstellt den vollqualifizierten Domänennamen (Fully Qualified Domain Name, FQDN) eines Schlüssels basierend auf dem Namen, den dieser Parameter angibt, dem Namen des Schlüsseltresor und Ihrer aktuellen Umgebung.</span><span class="sxs-lookup"><span data-stu-id="5d50d-139">This cmdlet constructs the fully qualified domain name (FQDN) of a key based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVaultName, HsmByVaultName
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d50d-140">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5d50d-140">-PassThru</span></span>
<span data-ttu-id="5d50d-141">Gibt an, dass dieses Cmdlet ein **Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey-Objekt** zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="5d50d-141">Indicates that this cmdlet returns a **Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey** object.</span></span>
<span data-ttu-id="5d50d-142">Standardmäßig generiert dieses Cmdlet keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="5d50d-142">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="5d50d-143">-VaultName</span><span class="sxs-lookup"><span data-stu-id="5d50d-143">-VaultName</span></span>
<span data-ttu-id="5d50d-144">Gibt den Namen des Schlüsseltresor an, aus dem der Schlüssel entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="5d50d-144">Specifies the name of the key vault from which to remove the key.</span></span>
<span data-ttu-id="5d50d-145">Dieses Cmdlet erstellt den FQDN eines Schlüsseltresor basierend auf dem Namen, den dieser Parameter angibt, und Ihrer aktuellen Umgebung.</span><span class="sxs-lookup"><span data-stu-id="5d50d-145">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVaultName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d50d-146">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5d50d-146">-Confirm</span></span>
<span data-ttu-id="5d50d-147">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5d50d-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5d50d-148">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="5d50d-148">-WhatIf</span></span>
<span data-ttu-id="5d50d-149">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5d50d-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5d50d-150">Das Cmdlet wird nicht ausgeführt. Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5d50d-150">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5d50d-151">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5d50d-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5d50d-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d50d-152">CommonParameters</span></span>
<span data-ttu-id="5d50d-153">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5d50d-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d50d-154">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5d50d-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d50d-155">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="5d50d-155">INPUTS</span></span>

### <span data-ttu-id="5d50d-156">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="5d50d-156">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span></span>

## <span data-ttu-id="5d50d-157">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="5d50d-157">OUTPUTS</span></span>

### <span data-ttu-id="5d50d-158">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="5d50d-158">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKey</span></span>

## <span data-ttu-id="5d50d-159">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="5d50d-159">NOTES</span></span>

## <span data-ttu-id="5d50d-160">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="5d50d-160">RELATED LINKS</span></span>

[<span data-ttu-id="5d50d-161">Add-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="5d50d-161">Add-AzKeyVaultKey</span></span>](./Add-AzKeyVaultKey.md)

[<span data-ttu-id="5d50d-162">Get-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="5d50d-162">Get-AzKeyVaultKey</span></span>](./Get-AzKeyVaultKey.md)

[<span data-ttu-id="5d50d-163">Set-AzKeyVaultKeyAttribute</span><span class="sxs-lookup"><span data-stu-id="5d50d-163">Set-AzKeyVaultKeyAttribute</span></span>](./Set-AzKeyVaultKeyAttribute.md)

[<span data-ttu-id="5d50d-164">Undo-AzKeyVaultKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="5d50d-164">Undo-AzKeyVaultKeyRemoval</span></span>](./Undo-AzKeyVaultKeyRemoval.md)

