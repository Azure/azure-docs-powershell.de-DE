---
external help file: ''
Module Name: Az.AppConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.appconfiguration/new-azappconfigurationstorekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/New-AzAppConfigurationStoreKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/New-AzAppConfigurationStoreKey.md
ms.openlocfilehash: 922bc6f596611638c0ea7d27304e6ea3f0d62eeb
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94173947"
---
# <span data-ttu-id="c81ba-101">New-AzAppConfigurationStoreKey</span><span class="sxs-lookup"><span data-stu-id="c81ba-101">New-AzAppConfigurationStoreKey</span></span>

## <span data-ttu-id="c81ba-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c81ba-102">SYNOPSIS</span></span>
<span data-ttu-id="c81ba-103">Generiert eine Zugriffstaste für den angegebenen Konfigurationsspeicher erneut.</span><span class="sxs-lookup"><span data-stu-id="c81ba-103">Regenerates an access key for the specified configuration store.</span></span>

## <span data-ttu-id="c81ba-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c81ba-104">SYNTAX</span></span>

### <span data-ttu-id="c81ba-105">RegenerateExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="c81ba-105">RegenerateExpanded (Default)</span></span>
```
New-AzAppConfigurationStoreKey -Name <String> -ResourceGroupName <String> -Id <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="c81ba-106">RegenerateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="c81ba-106">RegenerateViaIdentityExpanded</span></span>
```
New-AzAppConfigurationStoreKey -InputObject <IAppConfigurationIdentity> -Id <String>
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c81ba-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c81ba-107">DESCRIPTION</span></span>
<span data-ttu-id="c81ba-108">Generiert eine Zugriffstaste für den angegebenen Konfigurationsspeicher erneut.</span><span class="sxs-lookup"><span data-stu-id="c81ba-108">Regenerates an access key for the specified configuration store.</span></span>

## <span data-ttu-id="c81ba-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c81ba-109">EXAMPLES</span></span>

### <span data-ttu-id="c81ba-110">Beispiel 1: Erneutes Generieren des Schlüssels eines App-Konfigurationsspeichers</span><span class="sxs-lookup"><span data-stu-id="c81ba-110">Example 1: Regenerate key of an app configuration store</span></span>
```powershell
PS C:\> $keys= Get-AzAppConfigurationStoreKey -Name appconfig-test01 -ResourceGroupName azpwsh-manual-test
PS C:\> New-AzAppConfigurationStoreKey -Name appconfig-test01 -ResourceGroupName azpwsh-manual-test -Id $keys[0].id

ConnectionString                                                                                                                     LastModified        Name      ReadOnly Value
----------------                                                                                                                     ------------        ----      -------- -----
Endpoint=https://appconfig-test01.azconfig.io;Id=09pv-l0-s0:opFCQMC6+9485xJgN5Ws;Secret=GcoE9e9t7GLRNJ910M46IrbHO/Vg0tt4HujRdsaCoTY= 5/8/2020 5:47:15 AM Secondary False    GcoE9e9t7GLRNJ910M46IrbHO/Vg0tt4HujRdsaCoTY=
```

<span data-ttu-id="c81ba-111">Mit diesem Befehl wird der Schlüssel eines App-Konfigurationsspeichers neu generiert.</span><span class="sxs-lookup"><span data-stu-id="c81ba-111">This command regenerate key of an app configuration store.</span></span>

### <span data-ttu-id="c81ba-112">Beispiel 2: Erneutes Generieren des Schlüssels eines App-Konfigurationsspeichers nach Objekt</span><span class="sxs-lookup"><span data-stu-id="c81ba-112">Example 2: Regenerate key of an app configuration store by object</span></span>
```powershell
PS C:\> $app= New-AzAppConfigurationStore -Name appconfig-test10 -ResourceGroupName azpwsh-manual-test
PS C:\> $keys= Get-AzAppConfigurationStoreKey -Name appconfig-test01 -ResourceGroupName azpwsh-manual-test
PS C:\> New-AzAppConfigurationStoreKey -InputObject $app -Id $keys[0].id
ConnectionString                                                                                                                     LastModified        Name      ReadOnly Value
----------------                                                                                                                     ------------        ----      -------- -----
Endpoint=https://appconfig-test01.azconfig.io;Id=09pv-l0-s0:opFCQMC6+9485xJgN5Ws;Secret=GcoE9e9t7GLRNJ910M46IrbHO/Vg0tt4HujRdsaCoTY= 5/8/2020 5:47:15 AM Secondary False    GcoE9e9t7GLRNJ910M46IrbHO/Vg0tt4HujRdsaCoTY=
```

<span data-ttu-id="c81ba-113">Mit diesem Befehl wird der Schlüssel eines App-Konfigurationsspeichers nach Objekt neu generiert.</span><span class="sxs-lookup"><span data-stu-id="c81ba-113">This command regenerate key of an app configuration store by object.</span></span>

## <span data-ttu-id="c81ba-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="c81ba-114">PARAMETERS</span></span>

### <span data-ttu-id="c81ba-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c81ba-115">-DefaultProfile</span></span>
<span data-ttu-id="c81ba-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c81ba-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c81ba-117">-ID</span><span class="sxs-lookup"><span data-stu-id="c81ba-117">-Id</span></span>
<span data-ttu-id="c81ba-118">Die ID des Schlüssels, der neu generiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="c81ba-118">The id of the key to regenerate.</span></span>

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

### <span data-ttu-id="c81ba-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="c81ba-119">-InputObject</span></span>
<span data-ttu-id="c81ba-120">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="c81ba-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="c81ba-121">-Name</span><span class="sxs-lookup"><span data-stu-id="c81ba-121">-Name</span></span>
<span data-ttu-id="c81ba-122">Der Name des Konfigurationsspeichers.</span><span class="sxs-lookup"><span data-stu-id="c81ba-122">The name of the configuration store.</span></span>

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

### <span data-ttu-id="c81ba-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c81ba-123">-ResourceGroupName</span></span>
<span data-ttu-id="c81ba-124">Der Name der Ressourcengruppe, zu der die Container Registrierung gehört.</span><span class="sxs-lookup"><span data-stu-id="c81ba-124">The name of the resource group to which the container registry belongs.</span></span>

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

### <span data-ttu-id="c81ba-125">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="c81ba-125">-SubscriptionId</span></span>
<span data-ttu-id="c81ba-126">Die Microsoft Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="c81ba-126">The Microsoft Azure subscription ID.</span></span>

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

### <span data-ttu-id="c81ba-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c81ba-127">-Confirm</span></span>
<span data-ttu-id="c81ba-128">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c81ba-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c81ba-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c81ba-129">-WhatIf</span></span>
<span data-ttu-id="c81ba-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c81ba-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c81ba-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c81ba-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c81ba-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c81ba-132">CommonParameters</span></span>
<span data-ttu-id="c81ba-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c81ba-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c81ba-134">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c81ba-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c81ba-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c81ba-135">INPUTS</span></span>

### <span data-ttu-id="c81ba-136">Microsoft. Azure. PowerShell. Cmdlets. AppConfiguration. Models. IAppConfigurationIdentity</span><span class="sxs-lookup"><span data-stu-id="c81ba-136">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.IAppConfigurationIdentity</span></span>

## <span data-ttu-id="c81ba-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c81ba-137">OUTPUTS</span></span>

### <span data-ttu-id="c81ba-138">Microsoft. Azure. PowerShell. Cmdlets. AppConfiguration. Models. Api20200601. IApiKey</span><span class="sxs-lookup"><span data-stu-id="c81ba-138">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.Api20200601.IApiKey</span></span>

## <span data-ttu-id="c81ba-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="c81ba-139">NOTES</span></span>

<span data-ttu-id="c81ba-140">Aliase</span><span class="sxs-lookup"><span data-stu-id="c81ba-140">ALIASES</span></span>

<span data-ttu-id="c81ba-141">komplexe Parameter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c81ba-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="c81ba-142">Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="c81ba-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c81ba-143">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="c81ba-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="c81ba-144">Inputobject <IAppConfigurationIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="c81ba-144">INPUTOBJECT <IAppConfigurationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="c81ba-145">`[ConfigStoreName <String>]`: Der Name des Konfigurationsspeichers.</span><span class="sxs-lookup"><span data-stu-id="c81ba-145">`[ConfigStoreName <String>]`: The name of the configuration store.</span></span>
  - <span data-ttu-id="c81ba-146">`[GroupName <String>]`: Der Name der privaten Link Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="c81ba-146">`[GroupName <String>]`: The name of the private link resource group.</span></span>
  - <span data-ttu-id="c81ba-147">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="c81ba-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="c81ba-148">`[PrivateEndpointConnectionName <String>]`: Privater Endpunkt-Verbindungsname</span><span class="sxs-lookup"><span data-stu-id="c81ba-148">`[PrivateEndpointConnectionName <String>]`: Private endpoint connection name</span></span>
  - <span data-ttu-id="c81ba-149">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe, zu der die Container Registrierung gehört.</span><span class="sxs-lookup"><span data-stu-id="c81ba-149">`[ResourceGroupName <String>]`: The name of the resource group to which the container registry belongs.</span></span>
  - <span data-ttu-id="c81ba-150">`[SubscriptionId <String>]`: Die Microsoft Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="c81ba-150">`[SubscriptionId <String>]`: The Microsoft Azure subscription ID.</span></span>

## <span data-ttu-id="c81ba-151">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c81ba-151">RELATED LINKS</span></span>

