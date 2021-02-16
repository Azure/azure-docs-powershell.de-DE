---
external help file: ''
Module Name: Az.AppConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.appconfiguration/remove-azappconfigurationstore
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Remove-AzAppConfigurationStore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Remove-AzAppConfigurationStore.md
ms.openlocfilehash: b0939a4baa498532a3b519875183e6d1d12945a7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100149529"
---
# <span data-ttu-id="b298c-101">Remove-AzAppConfigurationStore</span><span class="sxs-lookup"><span data-stu-id="b298c-101">Remove-AzAppConfigurationStore</span></span>

## <span data-ttu-id="b298c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b298c-102">SYNOPSIS</span></span>
<span data-ttu-id="b298c-103">Löscht einen Konfigurationsspeicher.</span><span class="sxs-lookup"><span data-stu-id="b298c-103">Deletes a configuration store.</span></span>

## <span data-ttu-id="b298c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b298c-104">SYNTAX</span></span>

### <span data-ttu-id="b298c-105">Löschen (Standard)</span><span class="sxs-lookup"><span data-stu-id="b298c-105">Delete (Default)</span></span>
```
Remove-AzAppConfigurationStore -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="b298c-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="b298c-106">DeleteViaIdentity</span></span>
```
Remove-AzAppConfigurationStore -InputObject <IAppConfigurationIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b298c-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b298c-107">DESCRIPTION</span></span>
<span data-ttu-id="b298c-108">Löscht einen Konfigurationsspeicher.</span><span class="sxs-lookup"><span data-stu-id="b298c-108">Deletes a configuration store.</span></span>

## <span data-ttu-id="b298c-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b298c-109">EXAMPLES</span></span>

### <span data-ttu-id="b298c-110">Beispiel 1: Entfernen eines App-Konfigurationsspeichers</span><span class="sxs-lookup"><span data-stu-id="b298c-110">Example 1: Remove an app configuration store</span></span>
```powershell
PS C:\> Remove-AzAppConfigurationStore -Name appconfig-test03 -ResourceGroupName lucas-manual-test

```

<span data-ttu-id="b298c-111">Mit diesem Befehl wird ein App-Konfigurationsspeicher entfernt.</span><span class="sxs-lookup"><span data-stu-id="b298c-111">This command removes an app configuration store.</span></span>

### <span data-ttu-id="b298c-112">Beispiel 2: Entfernen eines App-Konfigurationsspeichers</span><span class="sxs-lookup"><span data-stu-id="b298c-112">Example 2: Remove an app configuration store</span></span>
```powershell
PS C:\> Get-AzAppConfigurationStore -Name appconfig-test02 -ResourceGroupName lucas-manual-test | Remove-AzAppConfigurationStore

```

<span data-ttu-id="b298c-113">Mit diesem Befehl wird ein App-Konfigurationsspeicher entfernt.</span><span class="sxs-lookup"><span data-stu-id="b298c-113">This command removes an app configuration store.</span></span>

## <span data-ttu-id="b298c-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b298c-114">PARAMETERS</span></span>

### <span data-ttu-id="b298c-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b298c-115">-AsJob</span></span>
<span data-ttu-id="b298c-116">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="b298c-116">Run the command as a job</span></span>

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

### <span data-ttu-id="b298c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b298c-117">-DefaultProfile</span></span>
<span data-ttu-id="b298c-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b298c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b298c-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b298c-119">-InputObject</span></span>
<span data-ttu-id="b298c-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="b298c-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.IAppConfigurationIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b298c-121">-Name</span><span class="sxs-lookup"><span data-stu-id="b298c-121">-Name</span></span>
<span data-ttu-id="b298c-122">Der Name des Konfigurationsspeichers.</span><span class="sxs-lookup"><span data-stu-id="b298c-122">The name of the configuration store.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b298c-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="b298c-123">-NoWait</span></span>
<span data-ttu-id="b298c-124">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="b298c-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="b298c-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b298c-125">-PassThru</span></span>
<span data-ttu-id="b298c-126">Gibt "true" zurück, wenn der Befehl erfolgreich ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="b298c-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="b298c-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b298c-127">-ResourceGroupName</span></span>
<span data-ttu-id="b298c-128">Der Name der Ressourcengruppe, zu der die Containerregistrierung gehört.</span><span class="sxs-lookup"><span data-stu-id="b298c-128">The name of the resource group to which the container registry belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b298c-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b298c-129">-SubscriptionId</span></span>
<span data-ttu-id="b298c-130">Die Microsoft Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="b298c-130">The Microsoft Azure subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b298c-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b298c-131">-Confirm</span></span>
<span data-ttu-id="b298c-132">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b298c-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b298c-133">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="b298c-133">-WhatIf</span></span>
<span data-ttu-id="b298c-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b298c-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b298c-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b298c-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b298c-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b298c-136">CommonParameters</span></span>
<span data-ttu-id="b298c-137">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b298c-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b298c-138">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b298c-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b298c-139">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b298c-139">INPUTS</span></span>

### <span data-ttu-id="b298c-140">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.IAppConfigurationIdentity</span><span class="sxs-lookup"><span data-stu-id="b298c-140">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.IAppConfigurationIdentity</span></span>

## <span data-ttu-id="b298c-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b298c-141">OUTPUTS</span></span>

### <span data-ttu-id="b298c-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b298c-142">System.Boolean</span></span>

## <span data-ttu-id="b298c-143">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="b298c-143">NOTES</span></span>

<span data-ttu-id="b298c-144">ALIASE</span><span class="sxs-lookup"><span data-stu-id="b298c-144">ALIASES</span></span>

<span data-ttu-id="b298c-145">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="b298c-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b298c-146">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="b298c-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b298c-147">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="b298c-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b298c-148">INPUTOBJECT <IAppConfigurationIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="b298c-148">INPUTOBJECT <IAppConfigurationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b298c-149">`[ConfigStoreName <String>]`: Der Name des Konfigurationsspeichers.</span><span class="sxs-lookup"><span data-stu-id="b298c-149">`[ConfigStoreName <String>]`: The name of the configuration store.</span></span>
  - <span data-ttu-id="b298c-150">`[GroupName <String>]`: Der Name der Ressourcengruppe für private Verknüpfungen.</span><span class="sxs-lookup"><span data-stu-id="b298c-150">`[GroupName <String>]`: The name of the private link resource group.</span></span>
  - <span data-ttu-id="b298c-151">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="b298c-151">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b298c-152">`[PrivateEndpointConnectionName <String>]`: Name der Verbindung für den privaten Endpunkt</span><span class="sxs-lookup"><span data-stu-id="b298c-152">`[PrivateEndpointConnectionName <String>]`: Private endpoint connection name</span></span>
  - <span data-ttu-id="b298c-153">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe, zu der die Containerregistrierung gehört.</span><span class="sxs-lookup"><span data-stu-id="b298c-153">`[ResourceGroupName <String>]`: The name of the resource group to which the container registry belongs.</span></span>
  - <span data-ttu-id="b298c-154">`[SubscriptionId <String>]`: Die Microsoft Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="b298c-154">`[SubscriptionId <String>]`: The Microsoft Azure subscription ID.</span></span>

## <span data-ttu-id="b298c-155">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="b298c-155">RELATED LINKS</span></span>

