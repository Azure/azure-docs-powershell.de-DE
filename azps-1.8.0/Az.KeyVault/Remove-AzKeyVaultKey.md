---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 817BF177-519F-47BA-86CF-4591FB402E2Dl
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultKey.md
ms.openlocfilehash: afa9f59520cba9f90f0f5d0a2edb6564b73245bf
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/14/2021
ms.locfileid: "100399242"
---
# <span data-ttu-id="49a36-101">Remove-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="49a36-101">Remove-AzKeyVaultKey</span></span>

## <span data-ttu-id="49a36-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="49a36-102">SYNOPSIS</span></span>
<span data-ttu-id="49a36-103">Löscht einen Schlüssel in einem Schlüsseltresor.</span><span class="sxs-lookup"><span data-stu-id="49a36-103">Deletes a key in a key vault.</span></span>

## <span data-ttu-id="49a36-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="49a36-104">SYNTAX</span></span>

### <span data-ttu-id="49a36-105">ByVaultName (Standard)</span><span class="sxs-lookup"><span data-stu-id="49a36-105">ByVaultName (Default)</span></span>
```
Remove-AzKeyVaultKey [-VaultName] <String> [-Name] <String> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="49a36-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="49a36-106">ByInputObject</span></span>
```
Remove-AzKeyVaultKey [-InputObject] <PSKeyVaultKeyIdentityItem> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="49a36-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="49a36-107">DESCRIPTION</span></span>
<span data-ttu-id="49a36-108">Das Remove-AzKeyVaultKey cmdlet löscht einen Schlüssel in einem Schlüsseltresor.</span><span class="sxs-lookup"><span data-stu-id="49a36-108">The Remove-AzKeyVaultKey cmdlet deletes a key in a key vault.</span></span>
<span data-ttu-id="49a36-109">Wenn der Schlüssel versehentlich gelöscht wurde, kann der Schlüssel mithilfe von Undo-AzKeyVaultKeyRemoval einem Benutzer mit speziellen "Wiederherstellen"-Berechtigungen wiederhergestellt werden.</span><span class="sxs-lookup"><span data-stu-id="49a36-109">If the key was accidentally deleted the key can be recovered using Undo-AzKeyVaultKeyRemoval by a user with special 'recover' permissions.</span></span>
<span data-ttu-id="49a36-110">Dieses Cmdlet hat den Wert "High" für die **"ConfirmImpact"-Eigenschaft.**</span><span class="sxs-lookup"><span data-stu-id="49a36-110">This cmdlet has a value of high for the **ConfirmImpact** property.</span></span>

## <span data-ttu-id="49a36-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="49a36-111">EXAMPLES</span></span>

### <span data-ttu-id="49a36-112">Beispiel 1: Entfernen eines Schlüssels aus einem Schlüsseltresor</span><span class="sxs-lookup"><span data-stu-id="49a36-112">Example 1: Remove a key from a key vault</span></span>
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

<span data-ttu-id="49a36-113">Mit diesem Befehl wird der Schlüssel "ITSoftware" aus dem Schlüsseltresor "Contoso" entfernt.</span><span class="sxs-lookup"><span data-stu-id="49a36-113">This command removes the key named ITSoftware from the key vault named Contoso.</span></span>

### <span data-ttu-id="49a36-114">Beispiel 2: Entfernen eines Schlüssels ohne Benutzerbestätigung</span><span class="sxs-lookup"><span data-stu-id="49a36-114">Example 2: Remove a key without user confirmation</span></span>
```powershell
PS C:\> Remove-AzKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware' -Force
```

<span data-ttu-id="49a36-115">Mit diesem Befehl wird der Schlüssel "ITSoftware" aus dem Schlüsseltresor "Contoso" entfernt.</span><span class="sxs-lookup"><span data-stu-id="49a36-115">This command removes the key named ITSoftware from the key vault named Contoso.</span></span>
<span data-ttu-id="49a36-116">Der Befehl gibt den Parameter *"Force"* an, daher fordert Sie das Cmdlet nicht zur Bestätigung auf.</span><span class="sxs-lookup"><span data-stu-id="49a36-116">The command specifies the *Force* parameter, and, therefore, the cmdlet does not prompt you for confirmation.</span></span>

### <span data-ttu-id="49a36-117">Beispiel 3: Endgültiges Löschen eines gelöschten Schlüssels aus dem Schlüsseltresor</span><span class="sxs-lookup"><span data-stu-id="49a36-117">Example 3: Purge a deleted key from the key vault permanently</span></span>
```powershell
PS C:\> Remove-AzKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware' -InRemovedState
```

<span data-ttu-id="49a36-118">Mit diesem Befehl wird der Schlüssel "ITSoftware" dauerhaft aus dem Schlüsseltresor "Contoso" entfernt.</span><span class="sxs-lookup"><span data-stu-id="49a36-118">This command removes the key named ITSoftware from the key vault named Contoso permanently.</span></span>
<span data-ttu-id="49a36-119">Zum Ausführen dieses Cmdlets ist die Berechtigung zum Löschen erforderlich, die zuvor und explizit dem Benutzer für diesen Schlüsseltresor erteilt worden sein muss.</span><span class="sxs-lookup"><span data-stu-id="49a36-119">Executing this cmdlet requires the 'purge' permission, which must have been previously and explicitly granted to the user for this key vault.</span></span>

### <span data-ttu-id="49a36-120">Beispiel 4: Entfernen von Schlüsseln mithilfe des Pipelineoperators</span><span class="sxs-lookup"><span data-stu-id="49a36-120">Example 4: Remove keys by using the pipeline operator</span></span>
```powershell
PS C:\> Get-AzKeyVaultKey -VaultName 'Contoso' | Where-Object {$_.Attributes.Enabled -eq $False} | Remove-AzKeyVaultKey
```

<span data-ttu-id="49a36-121">Dieser Befehl ruft alle Schlüssel im Schlüsseltresor "Contoso" ab und übergibt sie mithilfe des Pipelineoperators an das **Where-Object-Cmdlet.**</span><span class="sxs-lookup"><span data-stu-id="49a36-121">This command gets all the keys in the key vault named Contoso, and passes them to the **Where-Object** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="49a36-122">Dieses Cmdlet übergibt die Schlüssel mit dem Wert $False für das Attribut **"Enabled"** an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="49a36-122">That cmdlet passes the keys that have a value of $False for the **Enabled** attribute to the current cmdlet.</span></span>
<span data-ttu-id="49a36-123">Mit diesem Cmdlet werden diese Tasten entfernt.</span><span class="sxs-lookup"><span data-stu-id="49a36-123">That cmdlet removes those keys.</span></span>

## <span data-ttu-id="49a36-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="49a36-124">PARAMETERS</span></span>

### <span data-ttu-id="49a36-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49a36-125">-DefaultProfile</span></span>
<span data-ttu-id="49a36-126">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="49a36-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="49a36-127">-Force</span><span class="sxs-lookup"><span data-stu-id="49a36-127">-Force</span></span>
<span data-ttu-id="49a36-128">Erzwingt die Ausführung des Befehls ohne Benutzerbestätigung.</span><span class="sxs-lookup"><span data-stu-id="49a36-128">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="49a36-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="49a36-129">-InputObject</span></span>
<span data-ttu-id="49a36-130">KeyBundle-Objekt</span><span class="sxs-lookup"><span data-stu-id="49a36-130">KeyBundle Object</span></span>

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

### <span data-ttu-id="49a36-131">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="49a36-131">-InRemovedState</span></span>
<span data-ttu-id="49a36-132">Entfernen Sie den zuvor gelöschten Schlüssel dauerhaft.</span><span class="sxs-lookup"><span data-stu-id="49a36-132">Remove the previously deleted key permanently.</span></span>

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

### <span data-ttu-id="49a36-133">-Name</span><span class="sxs-lookup"><span data-stu-id="49a36-133">-Name</span></span>
<span data-ttu-id="49a36-134">Gibt den Namen des zu entfernenden Schlüssels an.</span><span class="sxs-lookup"><span data-stu-id="49a36-134">Specifies the name of the key to remove.</span></span>
<span data-ttu-id="49a36-135">Dieses Cmdlet erstellt den vollqualifizierten Domänennamen (Fully Qualified Domain Name, FQDN) eines Schlüssels basierend auf dem Namen, den dieser Parameter angibt, dem Namen des Schlüsseltresor und Ihrer aktuellen Umgebung.</span><span class="sxs-lookup"><span data-stu-id="49a36-135">This cmdlet constructs the fully qualified domain name (FQDN) of a key based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVaultName
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49a36-136">-PassThru</span><span class="sxs-lookup"><span data-stu-id="49a36-136">-PassThru</span></span>
<span data-ttu-id="49a36-137">Gibt an, dass dieses Cmdlet ein **Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey-Objekt** zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="49a36-137">Indicates that this cmdlet returns a **Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey** object.</span></span>
<span data-ttu-id="49a36-138">Standardmäßig generiert dieses Cmdlet keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="49a36-138">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="49a36-139">-VaultName</span><span class="sxs-lookup"><span data-stu-id="49a36-139">-VaultName</span></span>
<span data-ttu-id="49a36-140">Gibt den Namen des Schlüsseltresor an, aus dem der Schlüssel entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="49a36-140">Specifies the name of the key vault from which to remove the key.</span></span>
<span data-ttu-id="49a36-141">Dieses Cmdlet erstellt den FQDN eines Schlüsseltresor basierend auf dem Namen, den dieser Parameter angibt, und Ihrer aktuellen Umgebung.</span><span class="sxs-lookup"><span data-stu-id="49a36-141">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

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

### <span data-ttu-id="49a36-142">-Confirm</span><span class="sxs-lookup"><span data-stu-id="49a36-142">-Confirm</span></span>
<span data-ttu-id="49a36-143">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="49a36-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="49a36-144">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="49a36-144">-WhatIf</span></span>
<span data-ttu-id="49a36-145">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="49a36-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="49a36-146">Das Cmdlet wird nicht ausgeführt. Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="49a36-146">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="49a36-147">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="49a36-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="49a36-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49a36-148">CommonParameters</span></span>
<span data-ttu-id="49a36-149">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49a36-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49a36-150">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="49a36-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49a36-151">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="49a36-151">INPUTS</span></span>

### <span data-ttu-id="49a36-152">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="49a36-152">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span></span>

## <span data-ttu-id="49a36-153">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="49a36-153">OUTPUTS</span></span>

### <span data-ttu-id="49a36-154">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="49a36-154">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKey</span></span>

## <span data-ttu-id="49a36-155">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="49a36-155">NOTES</span></span>

## <span data-ttu-id="49a36-156">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="49a36-156">RELATED LINKS</span></span>

[<span data-ttu-id="49a36-157">Add-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="49a36-157">Add-AzKeyVaultKey</span></span>](./Add-AzKeyVaultKey.md)

[<span data-ttu-id="49a36-158">Get-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="49a36-158">Get-AzKeyVaultKey</span></span>](./Get-AzKeyVaultKey.md)


[<span data-ttu-id="49a36-159">Undo-AzKeyVaultKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="49a36-159">Undo-AzKeyVaultKeyRemoval</span></span>](./Undo-AzKeyVaultKeyRemoval.md)

