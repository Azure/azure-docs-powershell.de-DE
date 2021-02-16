---
external help file: ''
Module Name: Az.AppConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.appconfiguration/new-azappconfigurationstorekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/New-AzAppConfigurationStoreKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/New-AzAppConfigurationStoreKey.md
ms.openlocfilehash: 922bc6f596611638c0ea7d27304e6ea3f0d62eeb
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100149532"
---
# <span data-ttu-id="ec817-101">New-AzAppConfigurationStoreKey</span><span class="sxs-lookup"><span data-stu-id="ec817-101">New-AzAppConfigurationStoreKey</span></span>

## <span data-ttu-id="ec817-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ec817-102">SYNOPSIS</span></span>
<span data-ttu-id="ec817-103">Generiert einen Zugriffsschlüssel für den angegebenen Konfigurationsspeicher erneut.</span><span class="sxs-lookup"><span data-stu-id="ec817-103">Regenerates an access key for the specified configuration store.</span></span>

## <span data-ttu-id="ec817-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ec817-104">SYNTAX</span></span>

### <span data-ttu-id="ec817-105">RegenerateExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="ec817-105">RegenerateExpanded (Default)</span></span>
```
New-AzAppConfigurationStoreKey -Name <String> -ResourceGroupName <String> -Id <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="ec817-106">RegenerateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="ec817-106">RegenerateViaIdentityExpanded</span></span>
```
New-AzAppConfigurationStoreKey -InputObject <IAppConfigurationIdentity> -Id <String>
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ec817-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ec817-107">DESCRIPTION</span></span>
<span data-ttu-id="ec817-108">Generiert einen Zugriffsschlüssel für den angegebenen Konfigurationsspeicher erneut.</span><span class="sxs-lookup"><span data-stu-id="ec817-108">Regenerates an access key for the specified configuration store.</span></span>

## <span data-ttu-id="ec817-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ec817-109">EXAMPLES</span></span>

### <span data-ttu-id="ec817-110">Beispiel 1: Neuer generierter Schlüssel eines App-Konfigurationsspeichers</span><span class="sxs-lookup"><span data-stu-id="ec817-110">Example 1: Regenerate key of an app configuration store</span></span>
```powershell
PS C:\> $keys= Get-AzAppConfigurationStoreKey -Name appconfig-test01 -ResourceGroupName azpwsh-manual-test
PS C:\> New-AzAppConfigurationStoreKey -Name appconfig-test01 -ResourceGroupName azpwsh-manual-test -Id $keys[0].id

ConnectionString                                                                                                                     LastModified        Name      ReadOnly Value
----------------                                                                                                                     ------------        ----      -------- -----
Endpoint=https://appconfig-test01.azconfig.io;Id=09pv-l0-s0:opFCQMC6+9485xJgN5Ws;Secret=GcoE9e9t7GLRNJ910M46IrbHO/Vg0tt4HujRdsaCoTY= 5/8/2020 5:47:15 AM Secondary False    GcoE9e9t7GLRNJ910M46IrbHO/Vg0tt4HujRdsaCoTY=
```

<span data-ttu-id="ec817-111">Dieser Befehl generiert den Schlüssel eines App-Konfigurationsspeichers erneut.</span><span class="sxs-lookup"><span data-stu-id="ec817-111">This command regenerate key of an app configuration store.</span></span>

### <span data-ttu-id="ec817-112">Beispiel 2: Neuer generierter Schlüssel eines App-Konfigurationsspeichers nach Objekt</span><span class="sxs-lookup"><span data-stu-id="ec817-112">Example 2: Regenerate key of an app configuration store by object</span></span>
```powershell
PS C:\> $app= New-AzAppConfigurationStore -Name appconfig-test10 -ResourceGroupName azpwsh-manual-test
PS C:\> $keys= Get-AzAppConfigurationStoreKey -Name appconfig-test01 -ResourceGroupName azpwsh-manual-test
PS C:\> New-AzAppConfigurationStoreKey -InputObject $app -Id $keys[0].id
ConnectionString                                                                                                                     LastModified        Name      ReadOnly Value
----------------                                                                                                                     ------------        ----      -------- -----
Endpoint=https://appconfig-test01.azconfig.io;Id=09pv-l0-s0:opFCQMC6+9485xJgN5Ws;Secret=GcoE9e9t7GLRNJ910M46IrbHO/Vg0tt4HujRdsaCoTY= 5/8/2020 5:47:15 AM Secondary False    GcoE9e9t7GLRNJ910M46IrbHO/Vg0tt4HujRdsaCoTY=
```

<span data-ttu-id="ec817-113">Dieser Befehl generiert den Schlüssel eines App-Konfigurationsspeichers nach Objekt erneut.</span><span class="sxs-lookup"><span data-stu-id="ec817-113">This command regenerate key of an app configuration store by object.</span></span>

## <span data-ttu-id="ec817-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ec817-114">PARAMETERS</span></span>

### <span data-ttu-id="ec817-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec817-115">-DefaultProfile</span></span>
<span data-ttu-id="ec817-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ec817-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ec817-117">-ID</span><span class="sxs-lookup"><span data-stu-id="ec817-117">-Id</span></span>
<span data-ttu-id="ec817-118">Die ID des Schlüssels, der erneut generiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="ec817-118">The id of the key to regenerate.</span></span>

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

### <span data-ttu-id="ec817-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ec817-119">-InputObject</span></span>
<span data-ttu-id="ec817-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="ec817-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.IAppConfigurationIdentity
Parameter Sets: RegenerateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ec817-121">-Name</span><span class="sxs-lookup"><span data-stu-id="ec817-121">-Name</span></span>
<span data-ttu-id="ec817-122">Der Name des Konfigurationsspeichers.</span><span class="sxs-lookup"><span data-stu-id="ec817-122">The name of the configuration store.</span></span>

```yaml
Type: System.String
Parameter Sets: RegenerateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec817-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ec817-123">-ResourceGroupName</span></span>
<span data-ttu-id="ec817-124">Der Name der Ressourcengruppe, zu der die Containerregistrierung gehört.</span><span class="sxs-lookup"><span data-stu-id="ec817-124">The name of the resource group to which the container registry belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: RegenerateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec817-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ec817-125">-SubscriptionId</span></span>
<span data-ttu-id="ec817-126">Die Microsoft Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="ec817-126">The Microsoft Azure subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: RegenerateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec817-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ec817-127">-Confirm</span></span>
<span data-ttu-id="ec817-128">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ec817-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ec817-129">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="ec817-129">-WhatIf</span></span>
<span data-ttu-id="ec817-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ec817-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ec817-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ec817-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ec817-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec817-132">CommonParameters</span></span>
<span data-ttu-id="ec817-133">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ec817-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec817-134">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ec817-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec817-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ec817-135">INPUTS</span></span>

### <span data-ttu-id="ec817-136">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.IAppConfigurationIdentity</span><span class="sxs-lookup"><span data-stu-id="ec817-136">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.IAppConfigurationIdentity</span></span>

## <span data-ttu-id="ec817-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ec817-137">OUTPUTS</span></span>

### <span data-ttu-id="ec817-138">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.Api20200601.IApiKey</span><span class="sxs-lookup"><span data-stu-id="ec817-138">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.Api20200601.IApiKey</span></span>

## <span data-ttu-id="ec817-139">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="ec817-139">NOTES</span></span>

<span data-ttu-id="ec817-140">ALIASE</span><span class="sxs-lookup"><span data-stu-id="ec817-140">ALIASES</span></span>

<span data-ttu-id="ec817-141">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="ec817-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ec817-142">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="ec817-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ec817-143">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="ec817-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ec817-144">INPUTOBJECT <IAppConfigurationIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="ec817-144">INPUTOBJECT <IAppConfigurationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="ec817-145">`[ConfigStoreName <String>]`: Der Name des Konfigurationsspeichers.</span><span class="sxs-lookup"><span data-stu-id="ec817-145">`[ConfigStoreName <String>]`: The name of the configuration store.</span></span>
  - <span data-ttu-id="ec817-146">`[GroupName <String>]`: Der Name der Ressourcengruppe für private Verknüpfungen.</span><span class="sxs-lookup"><span data-stu-id="ec817-146">`[GroupName <String>]`: The name of the private link resource group.</span></span>
  - <span data-ttu-id="ec817-147">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="ec817-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ec817-148">`[PrivateEndpointConnectionName <String>]`: Name der Verbindung für den privaten Endpunkt</span><span class="sxs-lookup"><span data-stu-id="ec817-148">`[PrivateEndpointConnectionName <String>]`: Private endpoint connection name</span></span>
  - <span data-ttu-id="ec817-149">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe, zu der die Containerregistrierung gehört.</span><span class="sxs-lookup"><span data-stu-id="ec817-149">`[ResourceGroupName <String>]`: The name of the resource group to which the container registry belongs.</span></span>
  - <span data-ttu-id="ec817-150">`[SubscriptionId <String>]`: Die Microsoft Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="ec817-150">`[SubscriptionId <String>]`: The Microsoft Azure subscription ID.</span></span>

## <span data-ttu-id="ec817-151">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="ec817-151">RELATED LINKS</span></span>

