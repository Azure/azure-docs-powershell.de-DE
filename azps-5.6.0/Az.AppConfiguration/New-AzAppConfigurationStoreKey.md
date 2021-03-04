---
external help file: ''
Module Name: Az.AppConfiguration
online version: https://docs.microsoft.com/powershell/module/az.appconfiguration/new-azappconfigurationstorekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/New-AzAppConfigurationStoreKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/New-AzAppConfigurationStoreKey.md
ms.openlocfilehash: b71be7ed7475f89df52c22f69b38234ba8cee132
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101936355"
---
# <span data-ttu-id="f55ef-101">New-AzAppConfigurationStoreKey</span><span class="sxs-lookup"><span data-stu-id="f55ef-101">New-AzAppConfigurationStoreKey</span></span>

## <span data-ttu-id="f55ef-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f55ef-102">SYNOPSIS</span></span>
<span data-ttu-id="f55ef-103">Regeneriert einen Zugriffsschlüssel für den angegebenen Konfigurationsspeicher.</span><span class="sxs-lookup"><span data-stu-id="f55ef-103">Regenerates an access key for the specified configuration store.</span></span>

## <span data-ttu-id="f55ef-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f55ef-104">SYNTAX</span></span>

### <span data-ttu-id="f55ef-105">RegenerateExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="f55ef-105">RegenerateExpanded (Default)</span></span>
```
New-AzAppConfigurationStoreKey -Name <String> -ResourceGroupName <String> -Id <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="f55ef-106">RegenerateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="f55ef-106">RegenerateViaIdentityExpanded</span></span>
```
New-AzAppConfigurationStoreKey -InputObject <IAppConfigurationIdentity> -Id <String>
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="f55ef-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f55ef-107">DESCRIPTION</span></span>
<span data-ttu-id="f55ef-108">Regeneriert einen Zugriffsschlüssel für den angegebenen Konfigurationsspeicher.</span><span class="sxs-lookup"><span data-stu-id="f55ef-108">Regenerates an access key for the specified configuration store.</span></span>

## <span data-ttu-id="f55ef-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f55ef-109">EXAMPLES</span></span>

### <span data-ttu-id="f55ef-110">Beispiel 1: Neuerieren des Schlüssels eines App-Konfigurationsspeichers</span><span class="sxs-lookup"><span data-stu-id="f55ef-110">Example 1: Regenerate key of an app configuration store</span></span>
```powershell
PS C:\> $keys= Get-AzAppConfigurationStoreKey -Name appconfig-test01 -ResourceGroupName azpwsh-manual-test
PS C:\> New-AzAppConfigurationStoreKey -Name appconfig-test01 -ResourceGroupName azpwsh-manual-test -Id $keys[0].id

ConnectionString                                                                                                                     LastModified        Name      ReadOnly Value
----------------                                                                                                                     ------------        ----      -------- -----
Endpoint=https://appconfig-test01.azconfig.io;Id=09pv-l0-s0:opFCQMC6+9485xJgN5Ws;Secret=GcoE9e9t7GLRNJ910M46IrbHO/Vg0tt4HujRdsaCoTY= 5/8/2020 5:47:15 AM Secondary False    GcoE9e9t7GLRNJ910M46IrbHO/Vg0tt4HujRdsaCoTY=
```

<span data-ttu-id="f55ef-111">Mit diesem Befehl wird der Schlüssel eines App-Konfigurationsspeichers neu generiert.</span><span class="sxs-lookup"><span data-stu-id="f55ef-111">This command regenerate key of an app configuration store.</span></span>

### <span data-ttu-id="f55ef-112">Beispiel 2: Neuerieren des Schlüssels eines App-Konfigurationsspeichers nach Objekt</span><span class="sxs-lookup"><span data-stu-id="f55ef-112">Example 2: Regenerate key of an app configuration store by object</span></span>
```powershell
PS C:\> $app= New-AzAppConfigurationStore -Name appconfig-test10 -ResourceGroupName azpwsh-manual-test
PS C:\> $keys= Get-AzAppConfigurationStoreKey -Name appconfig-test01 -ResourceGroupName azpwsh-manual-test
PS C:\> New-AzAppConfigurationStoreKey -InputObject $app -Id $keys[0].id
ConnectionString                                                                                                                     LastModified        Name      ReadOnly Value
----------------                                                                                                                     ------------        ----      -------- -----
Endpoint=https://appconfig-test01.azconfig.io;Id=09pv-l0-s0:opFCQMC6+9485xJgN5Ws;Secret=GcoE9e9t7GLRNJ910M46IrbHO/Vg0tt4HujRdsaCoTY= 5/8/2020 5:47:15 AM Secondary False    GcoE9e9t7GLRNJ910M46IrbHO/Vg0tt4HujRdsaCoTY=
```

<span data-ttu-id="f55ef-113">Mit diesem Befehl wird der Schlüssel eines App-Konfigurationsspeichers nach Objekt neu generiert.</span><span class="sxs-lookup"><span data-stu-id="f55ef-113">This command regenerate key of an app configuration store by object.</span></span>

## <span data-ttu-id="f55ef-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="f55ef-114">PARAMETERS</span></span>

### <span data-ttu-id="f55ef-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f55ef-115">-DefaultProfile</span></span>
<span data-ttu-id="f55ef-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f55ef-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f55ef-117">-ID</span><span class="sxs-lookup"><span data-stu-id="f55ef-117">-Id</span></span>
<span data-ttu-id="f55ef-118">Die ID des Schlüssels, der neu generiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="f55ef-118">The id of the key to regenerate.</span></span>

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

### <span data-ttu-id="f55ef-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f55ef-119">-InputObject</span></span>
<span data-ttu-id="f55ef-120">Identitätsparameter Zum Erstellen lesen Sie den Abschnitt NOTIZEN für INPUTOBJECT-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="f55ef-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="f55ef-121">-Name</span><span class="sxs-lookup"><span data-stu-id="f55ef-121">-Name</span></span>
<span data-ttu-id="f55ef-122">Der Name des Konfigurationsspeichers.</span><span class="sxs-lookup"><span data-stu-id="f55ef-122">The name of the configuration store.</span></span>

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

### <span data-ttu-id="f55ef-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f55ef-123">-ResourceGroupName</span></span>
<span data-ttu-id="f55ef-124">Der Name der Ressourcengruppe, zu der die Containerregistrierung gehört.</span><span class="sxs-lookup"><span data-stu-id="f55ef-124">The name of the resource group to which the container registry belongs.</span></span>

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

### <span data-ttu-id="f55ef-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f55ef-125">-SubscriptionId</span></span>
<span data-ttu-id="f55ef-126">Die Microsoft Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="f55ef-126">The Microsoft Azure subscription ID.</span></span>

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

### <span data-ttu-id="f55ef-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f55ef-127">-Confirm</span></span>
<span data-ttu-id="f55ef-128">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f55ef-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f55ef-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f55ef-129">-WhatIf</span></span>
<span data-ttu-id="f55ef-130">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f55ef-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f55ef-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f55ef-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f55ef-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f55ef-132">CommonParameters</span></span>
<span data-ttu-id="f55ef-133">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f55ef-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f55ef-134">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f55ef-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f55ef-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f55ef-135">INPUTS</span></span>

### <span data-ttu-id="f55ef-136">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.IAppConfigurationIdentity</span><span class="sxs-lookup"><span data-stu-id="f55ef-136">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.IAppConfigurationIdentity</span></span>

## <span data-ttu-id="f55ef-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f55ef-137">OUTPUTS</span></span>

### <span data-ttu-id="f55ef-138">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.Api20200601.IApiKey</span><span class="sxs-lookup"><span data-stu-id="f55ef-138">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.Api20200601.IApiKey</span></span>

## <span data-ttu-id="f55ef-139">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="f55ef-139">NOTES</span></span>

<span data-ttu-id="f55ef-140">ALIASE</span><span class="sxs-lookup"><span data-stu-id="f55ef-140">ALIASES</span></span>

<span data-ttu-id="f55ef-141">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="f55ef-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f55ef-142">Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="f55ef-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f55ef-143">Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="f55ef-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f55ef-144">INPUTOBJECT <IAppConfigurationIdentity> : Identitätsparameter</span><span class="sxs-lookup"><span data-stu-id="f55ef-144">INPUTOBJECT <IAppConfigurationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f55ef-145">`[ConfigStoreName <String>]`: Der Name des Konfigurationsspeichers.</span><span class="sxs-lookup"><span data-stu-id="f55ef-145">`[ConfigStoreName <String>]`: The name of the configuration store.</span></span>
  - <span data-ttu-id="f55ef-146">`[GroupName <String>]`: Der Name der Ressourcengruppe für private Verknüpfungen.</span><span class="sxs-lookup"><span data-stu-id="f55ef-146">`[GroupName <String>]`: The name of the private link resource group.</span></span>
  - <span data-ttu-id="f55ef-147">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="f55ef-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f55ef-148">`[PrivateEndpointConnectionName <String>]`: Name der Privaten Endpunktverbindung</span><span class="sxs-lookup"><span data-stu-id="f55ef-148">`[PrivateEndpointConnectionName <String>]`: Private endpoint connection name</span></span>
  - <span data-ttu-id="f55ef-149">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe, zu der die Containerregistrierung gehört.</span><span class="sxs-lookup"><span data-stu-id="f55ef-149">`[ResourceGroupName <String>]`: The name of the resource group to which the container registry belongs.</span></span>
  - <span data-ttu-id="f55ef-150">`[SubscriptionId <String>]`: Die Microsoft Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="f55ef-150">`[SubscriptionId <String>]`: The Microsoft Azure subscription ID.</span></span>

## <span data-ttu-id="f55ef-151">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="f55ef-151">RELATED LINKS</span></span>

