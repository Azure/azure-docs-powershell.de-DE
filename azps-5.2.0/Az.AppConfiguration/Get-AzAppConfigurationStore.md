---
external help file: ''
Module Name: Az.AppConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.appconfiguration/get-azappconfigurationstore
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Get-AzAppConfigurationStore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Get-AzAppConfigurationStore.md
ms.openlocfilehash: 88847cbb128f5545a235eb2c5c02043231ff1078
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98289540"
---
# <span data-ttu-id="36b03-101">Get-AzAppConfigurationStore</span><span class="sxs-lookup"><span data-stu-id="36b03-101">Get-AzAppConfigurationStore</span></span>

## <span data-ttu-id="36b03-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="36b03-102">SYNOPSIS</span></span>
<span data-ttu-id="36b03-103">Laden Sie Konfigurationsspeicher für Apps herunter, oder listen Sie sie auf.</span><span class="sxs-lookup"><span data-stu-id="36b03-103">Get or list app configuration stores.</span></span>

## <span data-ttu-id="36b03-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="36b03-104">SYNTAX</span></span>

### <span data-ttu-id="36b03-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="36b03-105">List (Default)</span></span>
```
Get-AzAppConfigurationStore [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="36b03-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="36b03-106">Get</span></span>
```
Get-AzAppConfigurationStore -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="36b03-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="36b03-107">GetViaIdentity</span></span>
```
Get-AzAppConfigurationStore -InputObject <IAppConfigurationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="36b03-108">Liste1</span><span class="sxs-lookup"><span data-stu-id="36b03-108">List1</span></span>
```
Get-AzAppConfigurationStore -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="36b03-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="36b03-109">DESCRIPTION</span></span>
<span data-ttu-id="36b03-110">Laden Sie Konfigurationsspeicher für Apps herunter, oder listen Sie sie auf.</span><span class="sxs-lookup"><span data-stu-id="36b03-110">Get or list app configuration stores.</span></span>

## <span data-ttu-id="36b03-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="36b03-111">EXAMPLES</span></span>

### <span data-ttu-id="36b03-112">Beispiel 1: Auflisten aller App-Konfigurationsspeicher unter einem Abonnement</span><span class="sxs-lookup"><span data-stu-id="36b03-112">Example 1: List all app configuration stores under a subscription</span></span>
```powershell
PS C:\> Get-AzAppConfigurationStore

Location Name               Type
-------- ----               ----
eastus   appconfig-test01   Microsoft.AppConfiguration/configurationStores
eastus   contoso-app-config Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="36b03-113">Mit diesem Befehl werden alle App-Konfigurationsspeicher unter einem Abonnement aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="36b03-113">This command lists all app configuration stores under a subscription.</span></span>

### <span data-ttu-id="36b03-114">Beispiel 2: Auflisten aller App-Konfigurationsspeicher unter einer Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="36b03-114">Example 2: List all app configuration stores under a resource group</span></span>
```powershell
PS C:\> Get-AzAppConfigurationStore -ResourceGroupName azpwsh-manual-test

Location Name             Type
-------- ----             ----
eastus   appconfig-test01 Microsoft.AppConfiguration/configurationStores
eastus   appconfig-test02 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="36b03-115">Mit diesem Befehl werden alle App-Konfigurationsspeicher unter einer Ressourcengruppe aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="36b03-115">This command lists all app configuration stores under a resource group.</span></span>

### <span data-ttu-id="36b03-116">Beispiel 3: Erstellen eines App-Konfigurationsspeichers nach Name</span><span class="sxs-lookup"><span data-stu-id="36b03-116">Example 3: Get an app configuration store by name</span></span>
```powershell
PS C:\> Get-AzAppConfigurationStore -ResourceGroupName azpwsh-manual-test -Name appconfig-test01

Location Name             Type
-------- ----             ----
eastus   appconfig-test01 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="36b03-117">Dieser Befehl ruft einen App-Konfigurationsspeicher nach Name ab.</span><span class="sxs-lookup"><span data-stu-id="36b03-117">This command gets an app configuration store by name.</span></span>

### <span data-ttu-id="36b03-118">Beispiel 4: Herunterladen eines App-Konfigurationsspeichers per Pipeline</span><span class="sxs-lookup"><span data-stu-id="36b03-118">Example 4: Get an app configuration store by pipeline</span></span>
```powershell
PS C:\> Get-AzAppConfigurationStore -ResourceGroupName azpwsh-manual-test -Name appconfig-test01 | Get-AzAppConfigurationStore

Location Name             Type
-------- ----             ----
eastus   appconfig-test01 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="36b03-119">Dieser Befehl ruft einen App-Konfigurationsspeicher per Pipeline ab.</span><span class="sxs-lookup"><span data-stu-id="36b03-119">This command gets an app configuration store by pipeline.</span></span>

## <span data-ttu-id="36b03-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="36b03-120">PARAMETERS</span></span>

### <span data-ttu-id="36b03-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36b03-121">-DefaultProfile</span></span>
<span data-ttu-id="36b03-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="36b03-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="36b03-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="36b03-123">-InputObject</span></span>
<span data-ttu-id="36b03-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="36b03-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.IAppConfigurationIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="36b03-125">-Name</span><span class="sxs-lookup"><span data-stu-id="36b03-125">-Name</span></span>
<span data-ttu-id="36b03-126">Der Name des Konfigurationsspeichers.</span><span class="sxs-lookup"><span data-stu-id="36b03-126">The name of the configuration store.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36b03-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36b03-127">-ResourceGroupName</span></span>
<span data-ttu-id="36b03-128">Der Name der Ressourcengruppe, zu der die Containerregistrierung gehört.</span><span class="sxs-lookup"><span data-stu-id="36b03-128">The name of the resource group to which the container registry belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36b03-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="36b03-129">-SubscriptionId</span></span>
<span data-ttu-id="36b03-130">Die Microsoft Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="36b03-130">The Microsoft Azure subscription ID.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36b03-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36b03-131">CommonParameters</span></span>
<span data-ttu-id="36b03-132">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36b03-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36b03-133">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="36b03-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36b03-134">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="36b03-134">INPUTS</span></span>

### <span data-ttu-id="36b03-135">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.IAppConfigurationIdentity</span><span class="sxs-lookup"><span data-stu-id="36b03-135">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.IAppConfigurationIdentity</span></span>

## <span data-ttu-id="36b03-136">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="36b03-136">OUTPUTS</span></span>

### <span data-ttu-id="36b03-137">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.Api20200601.IConfigurationStore</span><span class="sxs-lookup"><span data-stu-id="36b03-137">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.Api20200601.IConfigurationStore</span></span>

## <span data-ttu-id="36b03-138">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="36b03-138">NOTES</span></span>

<span data-ttu-id="36b03-139">ALIASE</span><span class="sxs-lookup"><span data-stu-id="36b03-139">ALIASES</span></span>

<span data-ttu-id="36b03-140">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="36b03-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="36b03-141">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="36b03-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="36b03-142">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="36b03-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="36b03-143">INPUTOBJECT <IAppConfigurationIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="36b03-143">INPUTOBJECT <IAppConfigurationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="36b03-144">`[ConfigStoreName <String>]`: Der Name des Konfigurationsspeichers.</span><span class="sxs-lookup"><span data-stu-id="36b03-144">`[ConfigStoreName <String>]`: The name of the configuration store.</span></span>
  - <span data-ttu-id="36b03-145">`[GroupName <String>]`: Der Name der Ressourcengruppe für private Verknüpfungen.</span><span class="sxs-lookup"><span data-stu-id="36b03-145">`[GroupName <String>]`: The name of the private link resource group.</span></span>
  - <span data-ttu-id="36b03-146">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="36b03-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="36b03-147">`[PrivateEndpointConnectionName <String>]`: Name der Verbindung für den privaten Endpunkt</span><span class="sxs-lookup"><span data-stu-id="36b03-147">`[PrivateEndpointConnectionName <String>]`: Private endpoint connection name</span></span>
  - <span data-ttu-id="36b03-148">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe, zu der die Containerregistrierung gehört.</span><span class="sxs-lookup"><span data-stu-id="36b03-148">`[ResourceGroupName <String>]`: The name of the resource group to which the container registry belongs.</span></span>
  - <span data-ttu-id="36b03-149">`[SubscriptionId <String>]`: Die Microsoft Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="36b03-149">`[SubscriptionId <String>]`: The Microsoft Azure subscription ID.</span></span>

## <span data-ttu-id="36b03-150">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="36b03-150">RELATED LINKS</span></span>

