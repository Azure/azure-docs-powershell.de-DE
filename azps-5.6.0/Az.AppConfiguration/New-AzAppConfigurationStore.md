---
external help file: ''
Module Name: Az.AppConfiguration
online version: https://docs.microsoft.com/powershell/module/az.appconfiguration/new-azappconfigurationstore
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/New-AzAppConfigurationStore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/New-AzAppConfigurationStore.md
ms.openlocfilehash: 9373a154e6bc717c22705961fb5232814ac3d2c0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101936368"
---
# <span data-ttu-id="8a4f6-101">New-AzAppConfigurationStore</span><span class="sxs-lookup"><span data-stu-id="8a4f6-101">New-AzAppConfigurationStore</span></span>

## <span data-ttu-id="8a4f6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8a4f6-102">SYNOPSIS</span></span>
<span data-ttu-id="8a4f6-103">Erstellt einen Konfigurationsspeicher mit den angegebenen Parametern.</span><span class="sxs-lookup"><span data-stu-id="8a4f6-103">Creates a configuration store with the specified parameters.</span></span>

## <span data-ttu-id="8a4f6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8a4f6-104">SYNTAX</span></span>

```
New-AzAppConfigurationStore -Name <String> -ResourceGroupName <String> -Location <String> -Sku <String>
 [-SubscriptionId <String>] [-IdentityType <IdentityType>] [-Tag <Hashtable>]
 [-UserAssignedIdentity <String[]>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="8a4f6-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8a4f6-105">DESCRIPTION</span></span>
<span data-ttu-id="8a4f6-106">Erstellt einen Konfigurationsspeicher mit den angegebenen Parametern.</span><span class="sxs-lookup"><span data-stu-id="8a4f6-106">Creates a configuration store with the specified parameters.</span></span>

## <span data-ttu-id="8a4f6-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="8a4f6-107">EXAMPLES</span></span>

### <span data-ttu-id="8a4f6-108">Beispiel 1: Erstellen eines App-Konfigurationsspeichers</span><span class="sxs-lookup"><span data-stu-id="8a4f6-108">Example 1: Create an app configuration store</span></span>
```powershell
PS C:\> New-AzAppConfigurationStore -Name appconfig-test03 -ResourceGroupName azpwsh-manual-test -Location eastus -Sku free

Location Name             Type
-------- ----             ----
eastus   appconfig-test03 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="8a4f6-109">Mit diesem Befehl wird ein App-Konfigurationsspeicher erstellt.</span><span class="sxs-lookup"><span data-stu-id="8a4f6-109">This command creates an app configuration store.</span></span>

### <span data-ttu-id="8a4f6-110">Beispiel 2: Erstellen einer App-Konfiguration mit dem Auf "UserAssigned" festgelegten IdentityType</span><span class="sxs-lookup"><span data-stu-id="8a4f6-110">Example 2: Create an app configuration with the IdentityType set to "UserAssigned"</span></span>
```powershell
PS C:\> $assignedIdentity = New-AzUserAssignedIdentity -ResourceGroupName azpwsh-manual-test -Name assignedIdentity
PS C:\> New-AzAppConfigurationStore -Name appconfig-test10 -ResourceGroupName azpwsh-manual-test -Location eastus -Sku standard -IdentityType "UserAssigned" -UserAssignedIdentity $assignedIdentity.Id

Location Name             Type
-------- ----             ----
eastus   appconfig-test03 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="8a4f6-111">Mit diesem Befehl wird eine App-Konfiguration erstellt und ihr eine vom Benutzer zugewiesene verwaltete Identität zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="8a4f6-111">This command creates an app configuration and assign a user-assigned managed identity to it.</span></span>
<span data-ttu-id="8a4f6-112">Im Beispiel für finden Sie die folgenden Schritte zum Aktivieren `Update-AzAppConfigurationStore` von CMK (cusomer managed key).</span><span class="sxs-lookup"><span data-stu-id="8a4f6-112">See the example of `Update-AzAppConfigurationStore` for the following steps to enable CMK (cusomer managed key).</span></span>

### <span data-ttu-id="8a4f6-113">Beispiel 3: Erstellen einer App-Konfiguration mit dem Auf "SystemAssigned" festgelegten IdentityType</span><span class="sxs-lookup"><span data-stu-id="8a4f6-113">Example 3: Create an app configuration with the IdentityType set to "SystemAssigned"</span></span> 
```powershell
PS C:\> New-AzAppConfigurationStore -Name appconfig-test11 -ResourceGroupName azpwsh-manual-test -Location eastus -Sku standard -IdentityType "SystemAssigned"

Location Name             Type
-------- ----             ----
eastus   appconfig-test11 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="8a4f6-114">Mit diesem Befehl wird eine App-Konfiguration erstellt und die der Ressource zugeordnete vom System zugewiesene verwaltete Identität aktiviert.</span><span class="sxs-lookup"><span data-stu-id="8a4f6-114">This command creates an app configuration and enables the system-assigned managed identity associated with the resource.</span></span>
<span data-ttu-id="8a4f6-115">Im Beispiel für finden Sie die folgenden Schritte zum Aktivieren `Update-AzAppConfigurationStore` von CMK (cusomer managed key).</span><span class="sxs-lookup"><span data-stu-id="8a4f6-115">See the example of `Update-AzAppConfigurationStore` for the following steps to enable CMK (cusomer managed key).</span></span>

### <span data-ttu-id="8a4f6-116">Beispiel 4: Erstellen einer App-Konfiguration mit dem Auf "SystemAssigned, UserAssigned" festgelegten IdentityType</span><span class="sxs-lookup"><span data-stu-id="8a4f6-116">Example 4: Create an app configuration with the IdentityType set to "SystemAssigned, UserAssigned"</span></span>
```powershell
PS C:\> $assignedIdentity = New-AzUserAssignedIdentity -ResourceGroupName azpwsh-manual-test -Name assignedIdentity
PS C:\> New-AzAppConfigurationStore -Name appconfig-test10 -ResourceGroupName azpwsh-manual-test -Location eastus -Sku standard -IdentityType "SystemAssigned, UserAssigned" -UserAssignedIdentity $assignedIdentity.Id

Location Name             Type
-------- ----             ----
eastus   appconfig-test10 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="8a4f6-117">Sie können die vom System zugewiesene verwaltete Identität aktivieren und benutzer zugewiesene Identitäten gleichzeitig vergeben.</span><span class="sxs-lookup"><span data-stu-id="8a4f6-117">You can enable system-assigned managed identity and give user-assigned identities at the same time.</span></span>
<span data-ttu-id="8a4f6-118">Im Beispiel für finden Sie die folgenden Schritte zum Aktivieren `Update-AzAppConfigurationStore` von CMK (cusomer managed key).</span><span class="sxs-lookup"><span data-stu-id="8a4f6-118">See the example of `Update-AzAppConfigurationStore` for the following steps to enable CMK (cusomer managed key).</span></span>

## <span data-ttu-id="8a4f6-119">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="8a4f6-119">PARAMETERS</span></span>

### <span data-ttu-id="8a4f6-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8a4f6-120">-AsJob</span></span>
<span data-ttu-id="8a4f6-121">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="8a4f6-121">Run the command as a job</span></span>

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

### <span data-ttu-id="8a4f6-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a4f6-122">-DefaultProfile</span></span>
<span data-ttu-id="8a4f6-123">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8a4f6-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8a4f6-124">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="8a4f6-124">-IdentityType</span></span>
<span data-ttu-id="8a4f6-125">Der Typ der verwendeten verwalteten Identität.</span><span class="sxs-lookup"><span data-stu-id="8a4f6-125">The type of managed identity used.</span></span>
<span data-ttu-id="8a4f6-126">Der Typ "SystemAssignedAndUserAssigned" enthält sowohl eine implizit erstellte Identität als auch eine Gruppe von vom Benutzer zugewiesenen Identitäten.</span><span class="sxs-lookup"><span data-stu-id="8a4f6-126">The type 'SystemAssignedAndUserAssigned' includes both an implicitly created identity and a set of user-assigned identities.</span></span>
<span data-ttu-id="8a4f6-127">Der Typ "Keine" entfernt alle Identitäten.</span><span class="sxs-lookup"><span data-stu-id="8a4f6-127">The type 'None' will remove any identities.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Support.IdentityType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a4f6-128">-Location</span><span class="sxs-lookup"><span data-stu-id="8a4f6-128">-Location</span></span>
<span data-ttu-id="8a4f6-129">Der Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="8a4f6-129">The location of the resource.</span></span>
<span data-ttu-id="8a4f6-130">Dies kann nach dem Erstellen der Ressource nicht geändert werden.</span><span class="sxs-lookup"><span data-stu-id="8a4f6-130">This cannot be changed after the resource is created.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a4f6-131">-Name</span><span class="sxs-lookup"><span data-stu-id="8a4f6-131">-Name</span></span>
<span data-ttu-id="8a4f6-132">Der Name des Konfigurationsspeichers.</span><span class="sxs-lookup"><span data-stu-id="8a4f6-132">The name of the configuration store.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a4f6-133">-NoWait</span><span class="sxs-lookup"><span data-stu-id="8a4f6-133">-NoWait</span></span>
<span data-ttu-id="8a4f6-134">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="8a4f6-134">Run the command asynchronously</span></span>

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

### <span data-ttu-id="8a4f6-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8a4f6-135">-ResourceGroupName</span></span>
<span data-ttu-id="8a4f6-136">Der Name der Ressourcengruppe, zu der die Containerregistrierung gehört.</span><span class="sxs-lookup"><span data-stu-id="8a4f6-136">The name of the resource group to which the container registry belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a4f6-137">-Sku</span><span class="sxs-lookup"><span data-stu-id="8a4f6-137">-Sku</span></span>
<span data-ttu-id="8a4f6-138">Der SKU-Name des Konfigurationsspeichers.</span><span class="sxs-lookup"><span data-stu-id="8a4f6-138">The SKU name of the configuration store.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a4f6-139">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8a4f6-139">-SubscriptionId</span></span>
<span data-ttu-id="8a4f6-140">Die Microsoft Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="8a4f6-140">The Microsoft Azure subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a4f6-141">-Tag</span><span class="sxs-lookup"><span data-stu-id="8a4f6-141">-Tag</span></span>
<span data-ttu-id="8a4f6-142">Die Tags der Ressource.</span><span class="sxs-lookup"><span data-stu-id="8a4f6-142">The tags of the resource.</span></span>

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

### <span data-ttu-id="8a4f6-143">-UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="8a4f6-143">-UserAssignedIdentity</span></span>
<span data-ttu-id="8a4f6-144">Die Liste der benutzer zugewiesenen Identitäten, die der Ressource zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="8a4f6-144">The list of user-assigned identities associated with the resource.</span></span>
<span data-ttu-id="8a4f6-145">Die vom Benutzer zugewiesenen Identitätswörterbuchschlüssel werden ARM Ressourcen-IDs im Formular "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}" angezeigt.</span><span class="sxs-lookup"><span data-stu-id="8a4f6-145">The user-assigned identity dictionary keys will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}'.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a4f6-146">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="8a4f6-146">-Confirm</span></span>
<span data-ttu-id="8a4f6-147">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8a4f6-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8a4f6-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8a4f6-148">-WhatIf</span></span>
<span data-ttu-id="8a4f6-149">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8a4f6-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8a4f6-150">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8a4f6-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8a4f6-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a4f6-151">CommonParameters</span></span>
<span data-ttu-id="8a4f6-152">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8a4f6-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a4f6-153">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8a4f6-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a4f6-154">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="8a4f6-154">INPUTS</span></span>

## <span data-ttu-id="8a4f6-155">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="8a4f6-155">OUTPUTS</span></span>

### <span data-ttu-id="8a4f6-156">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.Api20200601.IConfigurationStore</span><span class="sxs-lookup"><span data-stu-id="8a4f6-156">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.Api20200601.IConfigurationStore</span></span>

## <span data-ttu-id="8a4f6-157">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="8a4f6-157">NOTES</span></span>

<span data-ttu-id="8a4f6-158">ALIASE</span><span class="sxs-lookup"><span data-stu-id="8a4f6-158">ALIASES</span></span>

## <span data-ttu-id="8a4f6-159">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="8a4f6-159">RELATED LINKS</span></span>



[<span data-ttu-id="8a4f6-160">New-AzUserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="8a4f6-160">New-AzUserAssignedIdentity</span></span>](https://docs.microsoft.com/powershell/module/az.managedserviceidentity/new-azuserassignedidentity?view=azps-4.4.0)

