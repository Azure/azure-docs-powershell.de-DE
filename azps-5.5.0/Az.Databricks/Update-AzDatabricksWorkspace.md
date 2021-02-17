---
external help file: ''
Module Name: Az.Databricks
online version: https://docs.microsoft.com/en-us/powershell/module/az.databricks/update-azdatabricksworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Update-AzDatabricksWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Update-AzDatabricksWorkspace.md
ms.openlocfilehash: 0d213dd18ea2423c90dec6446e4551cbcd8d161a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100165273"
---
# <span data-ttu-id="7927f-101">Update-AzDatabricksWorkspace</span><span class="sxs-lookup"><span data-stu-id="7927f-101">Update-AzDatabricksWorkspace</span></span>

## <span data-ttu-id="7927f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7927f-102">SYNOPSIS</span></span>
<span data-ttu-id="7927f-103">Aktualisiert einen Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="7927f-103">Updates a workspace.</span></span>

## <span data-ttu-id="7927f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7927f-104">SYNTAX</span></span>

### <span data-ttu-id="7927f-105">UpdateExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="7927f-105">UpdateExpanded (Default)</span></span>
```
Update-AzDatabricksWorkspace -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-EncryptionKeyName <String>] [-EncryptionKeySource <KeySource>] [-EncryptionKeyVaultUri <String>]
 [-EncryptionKeyVersion <String>] [-PrepareEncryption] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="7927f-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="7927f-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzDatabricksWorkspace -InputObject <IDatabricksIdentity> [-EncryptionKeyName <String>]
 [-EncryptionKeySource <KeySource>] [-EncryptionKeyVaultUri <String>] [-EncryptionKeyVersion <String>]
 [-PrepareEncryption] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="7927f-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7927f-107">DESCRIPTION</span></span>
<span data-ttu-id="7927f-108">Aktualisiert einen Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="7927f-108">Updates a workspace.</span></span>

## <span data-ttu-id="7927f-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="7927f-109">EXAMPLES</span></span>

### <span data-ttu-id="7927f-110">Beispiel 1: Aktualisiert die Tags eines Datenarbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="7927f-110">Example 1: Updates the tags of a Databricks workspace</span></span>
```powershell
PS C:\> $dbr = Get-AzDatabricksWorkspace -ResourceGroupName databricks-rg-952d47 -Name workspaceopsc46 -Tag @{'key'=1}
PS C:\> Update-AzDatabricksWorkspace -InputObject $dbr -Tag @{key="value"}

Name            Location Managed Resource Group ID
----            -------- -------------------------
workspaceopsc46 eastus   /subscriptions/0140911e-1040-48da-8bc9-b99fb3dd88a6/resourceGroups/databricks-rg-workspaceopsc46-wfgp3ayhu6jkn
```

<span data-ttu-id="7927f-111">Mit diesem Befehl werden die Tags eines Datenarbeitsbereichs aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="7927f-111">This command updates the tags of a Databricks workspace.</span></span>

### <span data-ttu-id="7927f-112">Beispiel 2: Aktivieren der Verschlüsselung für einen Datenarbeitsbereich</span><span class="sxs-lookup"><span data-stu-id="7927f-112">Example 2: Enable encryption on a Databricks workspace</span></span>
```powershell
PS C:\> Update-AzDatabricksWorkspace -ResourceGroupName databricks-rg-952d47 -Name workspaceypae6l -PrepareEncryption
PS C:\> Update-AzDatabricksWorkspace -ResourceGroupName databricks-rg-952d47 -Name workspaceypae6l -EncryptionKeySource 'Microsoft.KeyVault' -EncryptionKeyVaultUri https://keyvalult-j3kube.vault.azure.net/ -EncryptionKeyName key-p3bjsf -EncryptionKeyVersion 853999da89714fb4a1408681945135fd

Name            Location       Managed Resource Group ID
----            --------       -------------------------
workspaceypae6l East US 2 EUAP /subscriptions/0140911e-1040-48da-8bc9-b99fb3dd88a6/resourceGroups/databricks-rg-workspaceypae6l-wzefrgv2b075t
```

<span data-ttu-id="7927f-113">Zum Aktivieren der Verschlüsselung für einen Datenarbeitsbereich sind drei Schritte erforderlich:</span><span class="sxs-lookup"><span data-stu-id="7927f-113">Enabling encryption on a Databricks workspace takes three steps:</span></span>
1.
<span data-ttu-id="7927f-114">Aktualisieren Des Arbeitsbereichs mit (sofern nicht `-PrepareEncryption` erstellt).</span><span class="sxs-lookup"><span data-stu-id="7927f-114">Update the workspace with `-PrepareEncryption` (if it was not created so).</span></span>
1.
<span data-ttu-id="7927f-115">Suchen `StorageAccountIdentityPrincipalId` Sie in der Ausgabe des letzten Schritts.</span><span class="sxs-lookup"><span data-stu-id="7927f-115">Find `StorageAccountIdentityPrincipalId` in the output of the last step.</span></span>
<span data-ttu-id="7927f-116">Erteilen von Schlüsselberechtigungen für den Prinzipal</span><span class="sxs-lookup"><span data-stu-id="7927f-116">Grant key permissions to the principal.</span></span>
1.
<span data-ttu-id="7927f-117">Aktualisieren Sie den Arbeitsbereich erneut, um Informationen zum Verschlüsselungsschlüssel einfüllen:</span><span class="sxs-lookup"><span data-stu-id="7927f-117">Update the workspace again to fill in information about the encryption key:</span></span>
    - `-EncryptionKeySource`
    - `-EncryptionKeyVaultUri`
    - `-EncryptionKeyName`
    - `-EncryptionKeyVersion`

### <span data-ttu-id="7927f-118">Beispiel 3: Deaktivieren der Verschlüsselung für einen Datenarbeitsbereich</span><span class="sxs-lookup"><span data-stu-id="7927f-118">Example 3: Disable encryption on a Databricks workspace</span></span>
```powershell
PS C:\> Update-AzDatabricksWorkspace -ResourceGroupName databricks-rg-952d47 -Name workspaceypae6l -EncryptionKeySource 'Default'
```

<span data-ttu-id="7927f-119">Um die Verschlüsselung zu deaktivieren, legen Sie einfach auf `-EncryptionKeySource` `'Default'` "</span><span class="sxs-lookup"><span data-stu-id="7927f-119">To disable encryption, simply set `-EncryptionKeySource` to `'Default'`.</span></span>

## <span data-ttu-id="7927f-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7927f-120">PARAMETERS</span></span>

### <span data-ttu-id="7927f-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7927f-121">-AsJob</span></span>
<span data-ttu-id="7927f-122">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="7927f-122">Run the command as a job</span></span>

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

### <span data-ttu-id="7927f-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7927f-123">-DefaultProfile</span></span>
<span data-ttu-id="7927f-124">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7927f-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7927f-125">-EncryptionKeyName</span><span class="sxs-lookup"><span data-stu-id="7927f-125">-EncryptionKeyName</span></span>
<span data-ttu-id="7927f-126">Der Name des Schlüssels des Tresorschlüssels.</span><span class="sxs-lookup"><span data-stu-id="7927f-126">The name of Key Vault key.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7927f-127">-EncryptionKeySource</span><span class="sxs-lookup"><span data-stu-id="7927f-127">-EncryptionKeySource</span></span>
<span data-ttu-id="7927f-128">Die Verschlüsselungsschlüsselquelle (Anbieter).</span><span class="sxs-lookup"><span data-stu-id="7927f-128">The encryption keySource (provider).</span></span>
<span data-ttu-id="7927f-129">Mögliche Werte (ohne Schreibung): Standard, Microsoft.Keyvault</span><span class="sxs-lookup"><span data-stu-id="7927f-129">Possible values (case-insensitive): Default, Microsoft.Keyvault</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Databricks.Support.KeySource
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7927f-130">-EncryptionKeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="7927f-130">-EncryptionKeyVaultUri</span></span>
<span data-ttu-id="7927f-131">Der URI (DNS-Name) des Schlüsseltresor.</span><span class="sxs-lookup"><span data-stu-id="7927f-131">The URI (DNS name) of the Key Vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7927f-132">-EncryptionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="7927f-132">-EncryptionKeyVersion</span></span>
<span data-ttu-id="7927f-133">Die Version des KeyVault-Schlüssels.</span><span class="sxs-lookup"><span data-stu-id="7927f-133">The version of KeyVault key.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7927f-134">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7927f-134">-InputObject</span></span>
<span data-ttu-id="7927f-135">Identitätsparameter.</span><span class="sxs-lookup"><span data-stu-id="7927f-135">Identity parameter.</span></span>
<span data-ttu-id="7927f-136">Informationen zum Erstellen finden Sie im Abschnitt NOTES zu #A0 und zum Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="7927f-136">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7927f-137">-Name</span><span class="sxs-lookup"><span data-stu-id="7927f-137">-Name</span></span>
<span data-ttu-id="7927f-138">Der Name des Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="7927f-138">The name of the workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: WorkspaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7927f-139">-NoWait</span><span class="sxs-lookup"><span data-stu-id="7927f-139">-NoWait</span></span>
<span data-ttu-id="7927f-140">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="7927f-140">Run the command asynchronously</span></span>

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

### <span data-ttu-id="7927f-141">-PrepareEncryption</span><span class="sxs-lookup"><span data-stu-id="7927f-141">-PrepareEncryption</span></span>
<span data-ttu-id="7927f-142">Bereiten Sie den Arbeitsbereich für die Verschlüsselung vor.</span><span class="sxs-lookup"><span data-stu-id="7927f-142">Prepare the workspace for encryption.</span></span>
<span data-ttu-id="7927f-143">Aktiviert die verwaltete Identität für verwaltete Speicherkonto.</span><span class="sxs-lookup"><span data-stu-id="7927f-143">Enables the Managed Identity for managed storage account.</span></span>

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

### <span data-ttu-id="7927f-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7927f-144">-ResourceGroupName</span></span>
<span data-ttu-id="7927f-145">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="7927f-145">The name of the resource group.</span></span>
<span data-ttu-id="7927f-146">Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="7927f-146">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7927f-147">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7927f-147">-SubscriptionId</span></span>
<span data-ttu-id="7927f-148">Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="7927f-148">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7927f-149">-Tag</span><span class="sxs-lookup"><span data-stu-id="7927f-149">-Tag</span></span>
<span data-ttu-id="7927f-150">Ressourcentags.</span><span class="sxs-lookup"><span data-stu-id="7927f-150">Resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7927f-151">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7927f-151">-Confirm</span></span>
<span data-ttu-id="7927f-152">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7927f-152">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7927f-153">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="7927f-153">-WhatIf</span></span>
<span data-ttu-id="7927f-154">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7927f-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7927f-155">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7927f-155">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7927f-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7927f-156">CommonParameters</span></span>
<span data-ttu-id="7927f-157">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7927f-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7927f-158">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7927f-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7927f-159">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="7927f-159">INPUTS</span></span>

### <span data-ttu-id="7927f-160">Microsoft.Azure.PowerShell.Cmdlets.Databpersonenbezogenes.Models.IDatabseriesIdentity</span><span class="sxs-lookup"><span data-stu-id="7927f-160">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity</span></span>

## <span data-ttu-id="7927f-161">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="7927f-161">OUTPUTS</span></span>

### <span data-ttu-id="7927f-162">Microsoft.Azure.PowerShell.Cmdlets.Databpersonenbezogenes.Models.Api20180401.IWorkspace</span><span class="sxs-lookup"><span data-stu-id="7927f-162">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.Api20180401.IWorkspace</span></span>

## <span data-ttu-id="7927f-163">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="7927f-163">NOTES</span></span>

<span data-ttu-id="7927f-164">ALIASE</span><span class="sxs-lookup"><span data-stu-id="7927f-164">ALIASES</span></span>

<span data-ttu-id="7927f-165">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="7927f-165">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="7927f-166">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="7927f-166">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="7927f-167">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="7927f-167">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="7927f-168">INPUTOBJECT <IDatabricksIdentity> : Identity-Parameter.</span><span class="sxs-lookup"><span data-stu-id="7927f-168">INPUTOBJECT <IDatabricksIdentity>: Identity parameter.</span></span>
  - <span data-ttu-id="7927f-169">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="7927f-169">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="7927f-170">`[PeeringName <String>]`: Der Name des vNet-Arbeitsbereichs-Peerings.</span><span class="sxs-lookup"><span data-stu-id="7927f-170">`[PeeringName <String>]`: The name of the workspace vNet peering.</span></span>
  - <span data-ttu-id="7927f-171">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="7927f-171">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="7927f-172">Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="7927f-172">The name is case insensitive.</span></span>
  - <span data-ttu-id="7927f-173">`[SubscriptionId <String>]`: Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="7927f-173">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="7927f-174">`[WorkspaceName <String>]`: Der Name des Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="7927f-174">`[WorkspaceName <String>]`: The name of the workspace.</span></span>

## <span data-ttu-id="7927f-175">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="7927f-175">RELATED LINKS</span></span>

