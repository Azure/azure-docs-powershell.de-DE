---
external help file: ''
Module Name: Az.Databricks
online version: https://docs.microsoft.com/powershell/module/az.databricks/update-azdatabricksworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Update-AzDatabricksWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Update-AzDatabricksWorkspace.md
ms.openlocfilehash: 10a3a4d77cd6156bc2d6abe64a60773582ec50b2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101923707"
---
# <span data-ttu-id="05bf1-101">Update-AzDatabricksWorkspace</span><span class="sxs-lookup"><span data-stu-id="05bf1-101">Update-AzDatabricksWorkspace</span></span>

## <span data-ttu-id="05bf1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="05bf1-102">SYNOPSIS</span></span>
<span data-ttu-id="05bf1-103">Aktualisiert einen Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="05bf1-103">Updates a workspace.</span></span>

## <span data-ttu-id="05bf1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="05bf1-104">SYNTAX</span></span>

### <span data-ttu-id="05bf1-105">UpdateExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="05bf1-105">UpdateExpanded (Default)</span></span>
```
Update-AzDatabricksWorkspace -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-EncryptionKeyName <String>] [-EncryptionKeySource <KeySource>] [-EncryptionKeyVaultUri <String>]
 [-EncryptionKeyVersion <String>] [-PrepareEncryption] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="05bf1-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="05bf1-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzDatabricksWorkspace -InputObject <IDatabricksIdentity> [-EncryptionKeyName <String>]
 [-EncryptionKeySource <KeySource>] [-EncryptionKeyVaultUri <String>] [-EncryptionKeyVersion <String>]
 [-PrepareEncryption] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="05bf1-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="05bf1-107">DESCRIPTION</span></span>
<span data-ttu-id="05bf1-108">Aktualisiert einen Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="05bf1-108">Updates a workspace.</span></span>

## <span data-ttu-id="05bf1-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="05bf1-109">EXAMPLES</span></span>

### <span data-ttu-id="05bf1-110">Beispiel 1: Aktualisiert die Tags eines Databricks-Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="05bf1-110">Example 1: Updates the tags of a Databricks workspace</span></span>
```powershell
PS C:\> $dbr = Get-AzDatabricksWorkspace -ResourceGroupName databricks-rg-952d47 -Name workspaceopsc46 -Tag @{'key'=1}
PS C:\> Update-AzDatabricksWorkspace -InputObject $dbr -Tag @{key="value"}

Name            Location Managed Resource Group ID
----            -------- -------------------------
workspaceopsc46 eastus   /subscriptions/0140911e-1040-48da-8bc9-b99fb3dd88a6/resourceGroups/databricks-rg-workspaceopsc46-wfgp3ayhu6jkn
```

<span data-ttu-id="05bf1-111">Mit diesem Befehl werden die Tags eines Databricks-Arbeitsbereichs aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="05bf1-111">This command updates the tags of a Databricks workspace.</span></span>

### <span data-ttu-id="05bf1-112">Beispiel 2: Aktivieren der Verschlüsselung in einem Databricks-Arbeitsbereich</span><span class="sxs-lookup"><span data-stu-id="05bf1-112">Example 2: Enable encryption on a Databricks workspace</span></span>
```powershell
PS C:\> Update-AzDatabricksWorkspace -ResourceGroupName databricks-rg-952d47 -Name workspaceypae6l -PrepareEncryption
PS C:\> Update-AzDatabricksWorkspace -ResourceGroupName databricks-rg-952d47 -Name workspaceypae6l -EncryptionKeySource 'Microsoft.KeyVault' -EncryptionKeyVaultUri https://keyvalult-j3kube.vault.azure.net/ -EncryptionKeyName key-p3bjsf -EncryptionKeyVersion 853999da89714fb4a1408681945135fd

Name            Location       Managed Resource Group ID
----            --------       -------------------------
workspaceypae6l East US 2 EUAP /subscriptions/0140911e-1040-48da-8bc9-b99fb3dd88a6/resourceGroups/databricks-rg-workspaceypae6l-wzefrgv2b075t
```

<span data-ttu-id="05bf1-113">Zum Aktivieren der Verschlüsselung in einem Databricks-Arbeitsbereich sind drei Schritte erforderlich:</span><span class="sxs-lookup"><span data-stu-id="05bf1-113">Enabling encryption on a Databricks workspace takes three steps:</span></span>
1.
<span data-ttu-id="05bf1-114">Aktualisieren Sie den Arbeitsbereich `-PrepareEncryption` mit (wenn er nicht erstellt wurde).</span><span class="sxs-lookup"><span data-stu-id="05bf1-114">Update the workspace with `-PrepareEncryption` (if it was not created so).</span></span>
1.
<span data-ttu-id="05bf1-115">Suchen `StorageAccountIdentityPrincipalId` Sie in der Ausgabe des letzten Schritts.</span><span class="sxs-lookup"><span data-stu-id="05bf1-115">Find `StorageAccountIdentityPrincipalId` in the output of the last step.</span></span>
<span data-ttu-id="05bf1-116">Erteilen Sie dem Prinzipal schlüsselberechtigungen.</span><span class="sxs-lookup"><span data-stu-id="05bf1-116">Grant key permissions to the principal.</span></span>
1.
<span data-ttu-id="05bf1-117">Aktualisieren Sie den Arbeitsbereich erneut, um Informationen zum Verschlüsselungsschlüssel einfüllen zu können:</span><span class="sxs-lookup"><span data-stu-id="05bf1-117">Update the workspace again to fill in information about the encryption key:</span></span>
    - `-EncryptionKeySource`
    - `-EncryptionKeyVaultUri`
    - `-EncryptionKeyName`
    - `-EncryptionKeyVersion`

### <span data-ttu-id="05bf1-118">Beispiel 3: Deaktivieren der Verschlüsselung in einem Databricks-Arbeitsbereich</span><span class="sxs-lookup"><span data-stu-id="05bf1-118">Example 3: Disable encryption on a Databricks workspace</span></span>
```powershell
PS C:\> Update-AzDatabricksWorkspace -ResourceGroupName databricks-rg-952d47 -Name workspaceypae6l -EncryptionKeySource 'Default'
```

<span data-ttu-id="05bf1-119">Um die Verschlüsselung zu deaktivieren, legen Sie einfach `-EncryptionKeySource` auf . `'Default'`</span><span class="sxs-lookup"><span data-stu-id="05bf1-119">To disable encryption, simply set `-EncryptionKeySource` to `'Default'`.</span></span>

## <span data-ttu-id="05bf1-120">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="05bf1-120">PARAMETERS</span></span>

### <span data-ttu-id="05bf1-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="05bf1-121">-AsJob</span></span>
<span data-ttu-id="05bf1-122">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="05bf1-122">Run the command as a job</span></span>

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

### <span data-ttu-id="05bf1-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05bf1-123">-DefaultProfile</span></span>
<span data-ttu-id="05bf1-124">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="05bf1-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="05bf1-125">-EncryptionKeyName</span><span class="sxs-lookup"><span data-stu-id="05bf1-125">-EncryptionKeyName</span></span>
<span data-ttu-id="05bf1-126">Der Name des Schlüsseltresorschlüssels.</span><span class="sxs-lookup"><span data-stu-id="05bf1-126">The name of Key Vault key.</span></span>

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

### <span data-ttu-id="05bf1-127">-EncryptionKeySource</span><span class="sxs-lookup"><span data-stu-id="05bf1-127">-EncryptionKeySource</span></span>
<span data-ttu-id="05bf1-128">Der VerschlüsselungsschlüsselSource (Anbieter).</span><span class="sxs-lookup"><span data-stu-id="05bf1-128">The encryption keySource (provider).</span></span>
<span data-ttu-id="05bf1-129">Mögliche Werte (Groß-/Kleinschreibung): Standard, Microsoft.Keyvault</span><span class="sxs-lookup"><span data-stu-id="05bf1-129">Possible values (case-insensitive): Default, Microsoft.Keyvault</span></span>

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

### <span data-ttu-id="05bf1-130">-EncryptionKeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="05bf1-130">-EncryptionKeyVaultUri</span></span>
<span data-ttu-id="05bf1-131">Der URI (DNS-Name) des Schlüsseltresor.</span><span class="sxs-lookup"><span data-stu-id="05bf1-131">The URI (DNS name) of the Key Vault.</span></span>

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

### <span data-ttu-id="05bf1-132">-EncryptionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="05bf1-132">-EncryptionKeyVersion</span></span>
<span data-ttu-id="05bf1-133">Die Version von KeyVault Key.</span><span class="sxs-lookup"><span data-stu-id="05bf1-133">The version of KeyVault key.</span></span>

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

### <span data-ttu-id="05bf1-134">-InputObject</span><span class="sxs-lookup"><span data-stu-id="05bf1-134">-InputObject</span></span>
<span data-ttu-id="05bf1-135">Identitätsparameter.</span><span class="sxs-lookup"><span data-stu-id="05bf1-135">Identity parameter.</span></span>
<span data-ttu-id="05bf1-136">Informationen zum Erstellen finden Sie im Abschnitt NOTIZEN zu INPUTOBJECT-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="05bf1-136">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="05bf1-137">-Name</span><span class="sxs-lookup"><span data-stu-id="05bf1-137">-Name</span></span>
<span data-ttu-id="05bf1-138">Der Name des Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="05bf1-138">The name of the workspace.</span></span>

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

### <span data-ttu-id="05bf1-139">-NoWait</span><span class="sxs-lookup"><span data-stu-id="05bf1-139">-NoWait</span></span>
<span data-ttu-id="05bf1-140">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="05bf1-140">Run the command asynchronously</span></span>

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

### <span data-ttu-id="05bf1-141">-PrepareEncryption</span><span class="sxs-lookup"><span data-stu-id="05bf1-141">-PrepareEncryption</span></span>
<span data-ttu-id="05bf1-142">Bereiten Sie den Arbeitsbereich für die Verschlüsselung vor.</span><span class="sxs-lookup"><span data-stu-id="05bf1-142">Prepare the workspace for encryption.</span></span>
<span data-ttu-id="05bf1-143">Aktiviert die verwaltete Identität für verwaltete Speicherkonto.</span><span class="sxs-lookup"><span data-stu-id="05bf1-143">Enables the Managed Identity for managed storage account.</span></span>

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

### <span data-ttu-id="05bf1-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05bf1-144">-ResourceGroupName</span></span>
<span data-ttu-id="05bf1-145">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="05bf1-145">The name of the resource group.</span></span>
<span data-ttu-id="05bf1-146">Der Name ist groß- und kleinschreibungsunabhängiger.</span><span class="sxs-lookup"><span data-stu-id="05bf1-146">The name is case insensitive.</span></span>

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

### <span data-ttu-id="05bf1-147">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="05bf1-147">-SubscriptionId</span></span>
<span data-ttu-id="05bf1-148">Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="05bf1-148">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="05bf1-149">-Tag</span><span class="sxs-lookup"><span data-stu-id="05bf1-149">-Tag</span></span>
<span data-ttu-id="05bf1-150">Ressourcentags.</span><span class="sxs-lookup"><span data-stu-id="05bf1-150">Resource tags.</span></span>

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

### <span data-ttu-id="05bf1-151">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="05bf1-151">-Confirm</span></span>
<span data-ttu-id="05bf1-152">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="05bf1-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="05bf1-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="05bf1-153">-WhatIf</span></span>
<span data-ttu-id="05bf1-154">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="05bf1-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="05bf1-155">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="05bf1-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="05bf1-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05bf1-156">CommonParameters</span></span>
<span data-ttu-id="05bf1-157">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="05bf1-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05bf1-158">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="05bf1-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05bf1-159">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="05bf1-159">INPUTS</span></span>

### <span data-ttu-id="05bf1-160">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity</span><span class="sxs-lookup"><span data-stu-id="05bf1-160">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity</span></span>

## <span data-ttu-id="05bf1-161">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="05bf1-161">OUTPUTS</span></span>

### <span data-ttu-id="05bf1-162">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.Api20180401.IWorkspace</span><span class="sxs-lookup"><span data-stu-id="05bf1-162">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.Api20180401.IWorkspace</span></span>

## <span data-ttu-id="05bf1-163">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="05bf1-163">NOTES</span></span>

<span data-ttu-id="05bf1-164">ALIASE</span><span class="sxs-lookup"><span data-stu-id="05bf1-164">ALIASES</span></span>

<span data-ttu-id="05bf1-165">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="05bf1-165">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="05bf1-166">Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="05bf1-166">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="05bf1-167">Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="05bf1-167">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="05bf1-168">INPUTOBJECT <IDatabricksIdentity> : Identitätsparameter.</span><span class="sxs-lookup"><span data-stu-id="05bf1-168">INPUTOBJECT <IDatabricksIdentity>: Identity parameter.</span></span>
  - <span data-ttu-id="05bf1-169">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="05bf1-169">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="05bf1-170">`[PeeringName <String>]`: Der Name des Arbeitsbereichs vNet-Peering.</span><span class="sxs-lookup"><span data-stu-id="05bf1-170">`[PeeringName <String>]`: The name of the workspace vNet peering.</span></span>
  - <span data-ttu-id="05bf1-171">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="05bf1-171">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="05bf1-172">Der Name ist groß- und kleinschreibungsunabhängiger.</span><span class="sxs-lookup"><span data-stu-id="05bf1-172">The name is case insensitive.</span></span>
  - <span data-ttu-id="05bf1-173">`[SubscriptionId <String>]`: Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="05bf1-173">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="05bf1-174">`[WorkspaceName <String>]`: Der Name des Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="05bf1-174">`[WorkspaceName <String>]`: The name of the workspace.</span></span>

## <span data-ttu-id="05bf1-175">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="05bf1-175">RELATED LINKS</span></span>

