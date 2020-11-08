---
external help file: ''
Module Name: Az.AppConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.appconfiguration/new-azappconfigurationstore
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/New-AzAppConfigurationStore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/New-AzAppConfigurationStore.md
ms.openlocfilehash: 20f3985553a3fc7a993480bdf154a7f8e6776bf6
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94173941"
---
# <span data-ttu-id="76090-101">New-AzAppConfigurationStore</span><span class="sxs-lookup"><span data-stu-id="76090-101">New-AzAppConfigurationStore</span></span>

## <span data-ttu-id="76090-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="76090-102">SYNOPSIS</span></span>
<span data-ttu-id="76090-103">Erstellt einen Konfigurationsspeicher mit den angegebenen Parametern.</span><span class="sxs-lookup"><span data-stu-id="76090-103">Creates a configuration store with the specified parameters.</span></span>

## <span data-ttu-id="76090-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="76090-104">SYNTAX</span></span>

```
New-AzAppConfigurationStore -Name <String> -ResourceGroupName <String> -Location <String> -Sku <String>
 [-SubscriptionId <String>] [-IdentityType <IdentityType>] [-Tag <Hashtable>]
 [-UserAssignedIdentity <String[]>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="76090-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="76090-105">DESCRIPTION</span></span>
<span data-ttu-id="76090-106">Erstellt einen Konfigurationsspeicher mit den angegebenen Parametern.</span><span class="sxs-lookup"><span data-stu-id="76090-106">Creates a configuration store with the specified parameters.</span></span>

## <span data-ttu-id="76090-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="76090-107">EXAMPLES</span></span>

### <span data-ttu-id="76090-108">Beispiel 1: Erstellen eines App-Konfigurationsspeichers</span><span class="sxs-lookup"><span data-stu-id="76090-108">Example 1: Create an app configuration store</span></span>
```powershell
PS C:\> New-AzAppConfigurationStore -Name appconfig-test03 -ResourceGroupName azpwsh-manual-test -Location eastus -Sku free

Location Name             Type
-------- ----             ----
eastus   appconfig-test03 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="76090-109">Dieser Befehl erstellt einen app-Konfigurationsspeicher.</span><span class="sxs-lookup"><span data-stu-id="76090-109">This command creates an app configuration store.</span></span>

### <span data-ttu-id="76090-110">Beispiel 2: Erstellen einer APP-Konfiguration mit dem IdentityType auf "UserAssigned"</span><span class="sxs-lookup"><span data-stu-id="76090-110">Example 2: Create an app configuration with the IdentityType set to "UserAssigned"</span></span>
```powershell
PS C:\> $assignedIdentity = New-AzUserAssignedIdentity -ResourceGroupName azpwsh-manual-test -Name assignedIdentity
PS C:\> New-AzAppConfigurationStore -Name appconfig-test10 -ResourceGroupName azpwsh-manual-test -Location eastus -Sku standard -IdentityType "UserAssigned" -UserAssignedIdentity $assignedIdentity.Id

Location Name             Type
-------- ----             ----
eastus   appconfig-test03 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="76090-111">Dieser Befehl erstellt eine APP-Konfiguration und weist ihr eine vom Benutzer zugewiesene verwaltete Identität zu.</span><span class="sxs-lookup"><span data-stu-id="76090-111">This command creates an app configuration and assign a user-assigned managed identity to it.</span></span>
<span data-ttu-id="76090-112">Lesen Sie das Beispiel `Update-AzAppConfigurationStore` für die folgenden Schritte zum Aktivieren von CMK (Cusomer-verwalteter Schlüssel).</span><span class="sxs-lookup"><span data-stu-id="76090-112">See the example of `Update-AzAppConfigurationStore` for the following steps to enable CMK (cusomer managed key).</span></span>

### <span data-ttu-id="76090-113">Beispiel 3: Erstellen einer APP-Konfiguration, wobei die IdentityType auf "SystemAssigned" gesetzt ist</span><span class="sxs-lookup"><span data-stu-id="76090-113">Example 3: Create an app configuration with the IdentityType set to "SystemAssigned"</span></span> 
```powershell
PS C:\> New-AzAppConfigurationStore -Name appconfig-test11 -ResourceGroupName azpwsh-manual-test -Location eastus -Sku standard -IdentityType "SystemAssigned"

Location Name             Type
-------- ----             ----
eastus   appconfig-test11 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="76090-114">Mit diesem Befehl wird eine APP-Konfiguration erstellt und die der Ressource zugeordnete, vom System zugewiesene verwaltete Identität aktiviert.</span><span class="sxs-lookup"><span data-stu-id="76090-114">This command creates an app configuration and enables the system-assigned managed identity associated with the resource.</span></span>
<span data-ttu-id="76090-115">Lesen Sie das Beispiel `Update-AzAppConfigurationStore` für die folgenden Schritte zum Aktivieren von CMK (Cusomer-verwalteter Schlüssel).</span><span class="sxs-lookup"><span data-stu-id="76090-115">See the example of `Update-AzAppConfigurationStore` for the following steps to enable CMK (cusomer managed key).</span></span>

### <span data-ttu-id="76090-116">Beispiel 4: Erstellen einer APP-Konfiguration mit dem IdentityType auf "SystemAssigned, UserAssigned"</span><span class="sxs-lookup"><span data-stu-id="76090-116">Example 4: Create an app configuration with the IdentityType set to "SystemAssigned, UserAssigned"</span></span>
```powershell
PS C:\> $assignedIdentity = New-AzUserAssignedIdentity -ResourceGroupName azpwsh-manual-test -Name assignedIdentity
PS C:\> New-AzAppConfigurationStore -Name appconfig-test10 -ResourceGroupName azpwsh-manual-test -Location eastus -Sku standard -IdentityType "SystemAssigned, UserAssigned" -UserAssignedIdentity $assignedIdentity.Id

Location Name             Type
-------- ----             ----
eastus   appconfig-test10 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="76090-117">Sie können die vom System zugewiesene verwaltete Identität aktivieren und Benutzern zugewiesene Identitäten gleichzeitig zuweisen.</span><span class="sxs-lookup"><span data-stu-id="76090-117">You can enable system-assigned managed identity and give user-assigned identities at the same time.</span></span>
<span data-ttu-id="76090-118">Lesen Sie das Beispiel `Update-AzAppConfigurationStore` für die folgenden Schritte zum Aktivieren von CMK (Cusomer-verwalteter Schlüssel).</span><span class="sxs-lookup"><span data-stu-id="76090-118">See the example of `Update-AzAppConfigurationStore` for the following steps to enable CMK (cusomer managed key).</span></span>

## <span data-ttu-id="76090-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="76090-119">PARAMETERS</span></span>

### <span data-ttu-id="76090-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="76090-120">-AsJob</span></span>
<span data-ttu-id="76090-121">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="76090-121">Run the command as a job</span></span>

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

### <span data-ttu-id="76090-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76090-122">-DefaultProfile</span></span>
<span data-ttu-id="76090-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="76090-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="76090-124">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="76090-124">-IdentityType</span></span>
<span data-ttu-id="76090-125">Der Typ der verwendeten verwalteten Identität.</span><span class="sxs-lookup"><span data-stu-id="76090-125">The type of managed identity used.</span></span>
<span data-ttu-id="76090-126">Der Typ "SystemAssignedAndUserAssigned" umfasst sowohl eine implizit erstellte Identität als auch eine Reihe von vom Benutzer zugewiesenen Identitäten.</span><span class="sxs-lookup"><span data-stu-id="76090-126">The type 'SystemAssignedAndUserAssigned' includes both an implicitly created identity and a set of user-assigned identities.</span></span>
<span data-ttu-id="76090-127">Der Typ "None" entfernt alle Identitäten.</span><span class="sxs-lookup"><span data-stu-id="76090-127">The type 'None' will remove any identities.</span></span>

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

### <span data-ttu-id="76090-128">-Standort</span><span class="sxs-lookup"><span data-stu-id="76090-128">-Location</span></span>
<span data-ttu-id="76090-129">Der Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="76090-129">The location of the resource.</span></span>
<span data-ttu-id="76090-130">Dies kann nach der Erstellung der Ressource nicht mehr geändert werden.</span><span class="sxs-lookup"><span data-stu-id="76090-130">This cannot be changed after the resource is created.</span></span>

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

### <span data-ttu-id="76090-131">-Name</span><span class="sxs-lookup"><span data-stu-id="76090-131">-Name</span></span>
<span data-ttu-id="76090-132">Der Name des Konfigurationsspeichers.</span><span class="sxs-lookup"><span data-stu-id="76090-132">The name of the configuration store.</span></span>

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

### <span data-ttu-id="76090-133">-Nowait</span><span class="sxs-lookup"><span data-stu-id="76090-133">-NoWait</span></span>
<span data-ttu-id="76090-134">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="76090-134">Run the command asynchronously</span></span>

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

### <span data-ttu-id="76090-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76090-135">-ResourceGroupName</span></span>
<span data-ttu-id="76090-136">Der Name der Ressourcengruppe, zu der die Container Registrierung gehört.</span><span class="sxs-lookup"><span data-stu-id="76090-136">The name of the resource group to which the container registry belongs.</span></span>

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

### <span data-ttu-id="76090-137">-SKU</span><span class="sxs-lookup"><span data-stu-id="76090-137">-Sku</span></span>
<span data-ttu-id="76090-138">Der SKU-Name des Konfigurationsspeichers.</span><span class="sxs-lookup"><span data-stu-id="76090-138">The SKU name of the configuration store.</span></span>

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

### <span data-ttu-id="76090-139">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="76090-139">-SubscriptionId</span></span>
<span data-ttu-id="76090-140">Die Microsoft Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="76090-140">The Microsoft Azure subscription ID.</span></span>

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

### <span data-ttu-id="76090-141">-Tag</span><span class="sxs-lookup"><span data-stu-id="76090-141">-Tag</span></span>
<span data-ttu-id="76090-142">Die Tags der Ressource.</span><span class="sxs-lookup"><span data-stu-id="76090-142">The tags of the resource.</span></span>

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

### <span data-ttu-id="76090-143">-UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="76090-143">-UserAssignedIdentity</span></span>
<span data-ttu-id="76090-144">Die Liste der Benutzer zugewiesenen Identitäten, die der Ressource zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="76090-144">The list of user-assigned identities associated with the resource.</span></span>
<span data-ttu-id="76090-145">Die vom Benutzer zugewiesenen ID-Wörterbuchschlüssel sind arm-Ressourcen-IDs in der Form: "/Subscriptions/{SubscriptionId}/resourceGroups/{resourceGroupName}/Providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}".</span><span class="sxs-lookup"><span data-stu-id="76090-145">The user-assigned identity dictionary keys will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}'.</span></span>

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

### <span data-ttu-id="76090-146">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="76090-146">-Confirm</span></span>
<span data-ttu-id="76090-147">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="76090-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="76090-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="76090-148">-WhatIf</span></span>
<span data-ttu-id="76090-149">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="76090-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="76090-150">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="76090-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="76090-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76090-151">CommonParameters</span></span>
<span data-ttu-id="76090-152">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76090-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76090-153">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="76090-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76090-154">Eingaben</span><span class="sxs-lookup"><span data-stu-id="76090-154">INPUTS</span></span>

## <span data-ttu-id="76090-155">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="76090-155">OUTPUTS</span></span>

### <span data-ttu-id="76090-156">Microsoft. Azure. PowerShell. Cmdlets. AppConfiguration. Models. Api20200601. IConfigurationStore</span><span class="sxs-lookup"><span data-stu-id="76090-156">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.Api20200601.IConfigurationStore</span></span>

## <span data-ttu-id="76090-157">Notizen</span><span class="sxs-lookup"><span data-stu-id="76090-157">NOTES</span></span>

<span data-ttu-id="76090-158">Aliase</span><span class="sxs-lookup"><span data-stu-id="76090-158">ALIASES</span></span>

## <span data-ttu-id="76090-159">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="76090-159">RELATED LINKS</span></span>



[<span data-ttu-id="76090-160">Neu – AzUserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="76090-160">New-AzUserAssignedIdentity</span></span>](https://docs.microsoft.com/en-us/powershell/module/az.managedserviceidentity/new-azuserassignedidentity?view=azps-4.4.0)

