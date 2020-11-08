---
external help file: ''
Module Name: Az.AppConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.appconfiguration/get-azappconfigurationstore
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Get-AzAppConfigurationStore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Get-AzAppConfigurationStore.md
ms.openlocfilehash: 88847cbb128f5545a235eb2c5c02043231ff1078
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94008191"
---
# <span data-ttu-id="36792-101">Get-AzAppConfigurationStore</span><span class="sxs-lookup"><span data-stu-id="36792-101">Get-AzAppConfigurationStore</span></span>

## <span data-ttu-id="36792-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="36792-102">SYNOPSIS</span></span>
<span data-ttu-id="36792-103">Abrufen oder Auflisten von App-Konfigurations speichern.</span><span class="sxs-lookup"><span data-stu-id="36792-103">Get or list app configuration stores.</span></span>

## <span data-ttu-id="36792-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="36792-104">SYNTAX</span></span>

### <span data-ttu-id="36792-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="36792-105">List (Default)</span></span>
```
Get-AzAppConfigurationStore [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="36792-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="36792-106">Get</span></span>
```
Get-AzAppConfigurationStore -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="36792-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="36792-107">GetViaIdentity</span></span>
```
Get-AzAppConfigurationStore -InputObject <IAppConfigurationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="36792-108">List1</span><span class="sxs-lookup"><span data-stu-id="36792-108">List1</span></span>
```
Get-AzAppConfigurationStore -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="36792-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="36792-109">DESCRIPTION</span></span>
<span data-ttu-id="36792-110">Abrufen oder Auflisten von App-Konfigurations speichern.</span><span class="sxs-lookup"><span data-stu-id="36792-110">Get or list app configuration stores.</span></span>

## <span data-ttu-id="36792-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="36792-111">EXAMPLES</span></span>

### <span data-ttu-id="36792-112">Beispiel 1: Auflisten aller App-Konfigurationsspeicher unter einem Abonnement</span><span class="sxs-lookup"><span data-stu-id="36792-112">Example 1: List all app configuration stores under a subscription</span></span>
```powershell
PS C:\> Get-AzAppConfigurationStore

Location Name               Type
-------- ----               ----
eastus   appconfig-test01   Microsoft.AppConfiguration/configurationStores
eastus   contoso-app-config Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="36792-113">Dieser Befehl listet alle App-Konfigurationsspeicher unter einem Abonnement auf.</span><span class="sxs-lookup"><span data-stu-id="36792-113">This command lists all app configuration stores under a subscription.</span></span>

### <span data-ttu-id="36792-114">Beispiel 2: Auflisten aller App-Konfigurationsspeicher unter einer Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="36792-114">Example 2: List all app configuration stores under a resource group</span></span>
```powershell
PS C:\> Get-AzAppConfigurationStore -ResourceGroupName azpwsh-manual-test

Location Name             Type
-------- ----             ----
eastus   appconfig-test01 Microsoft.AppConfiguration/configurationStores
eastus   appconfig-test02 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="36792-115">Dieser Befehl listet alle App-Konfigurationsspeicher unter einer Ressourcengruppe auf.</span><span class="sxs-lookup"><span data-stu-id="36792-115">This command lists all app configuration stores under a resource group.</span></span>

### <span data-ttu-id="36792-116">Beispiel 3: Abrufen eines App-Konfigurationsspeichers nach Name</span><span class="sxs-lookup"><span data-stu-id="36792-116">Example 3: Get an app configuration store by name</span></span>
```powershell
PS C:\> Get-AzAppConfigurationStore -ResourceGroupName azpwsh-manual-test -Name appconfig-test01

Location Name             Type
-------- ----             ----
eastus   appconfig-test01 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="36792-117">Mit diesem Befehl wird ein App-Konfigurationsspeicher nach Namen abgerufen.</span><span class="sxs-lookup"><span data-stu-id="36792-117">This command gets an app configuration store by name.</span></span>

### <span data-ttu-id="36792-118">Beispiel 4: Abrufen eines App-Konfigurationsspeichers nach Pipeline</span><span class="sxs-lookup"><span data-stu-id="36792-118">Example 4: Get an app configuration store by pipeline</span></span>
```powershell
PS C:\> Get-AzAppConfigurationStore -ResourceGroupName azpwsh-manual-test -Name appconfig-test01 | Get-AzAppConfigurationStore

Location Name             Type
-------- ----             ----
eastus   appconfig-test01 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="36792-119">Mit diesem Befehl wird ein App-Konfigurationsspeicher nach Pipeline abgerufen.</span><span class="sxs-lookup"><span data-stu-id="36792-119">This command gets an app configuration store by pipeline.</span></span>

## <span data-ttu-id="36792-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="36792-120">PARAMETERS</span></span>

### <span data-ttu-id="36792-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36792-121">-DefaultProfile</span></span>
<span data-ttu-id="36792-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="36792-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="36792-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="36792-123">-InputObject</span></span>
<span data-ttu-id="36792-124">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="36792-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="36792-125">-Name</span><span class="sxs-lookup"><span data-stu-id="36792-125">-Name</span></span>
<span data-ttu-id="36792-126">Der Name des Konfigurationsspeichers.</span><span class="sxs-lookup"><span data-stu-id="36792-126">The name of the configuration store.</span></span>

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

### <span data-ttu-id="36792-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36792-127">-ResourceGroupName</span></span>
<span data-ttu-id="36792-128">Der Name der Ressourcengruppe, zu der die Container Registrierung gehört.</span><span class="sxs-lookup"><span data-stu-id="36792-128">The name of the resource group to which the container registry belongs.</span></span>

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

### <span data-ttu-id="36792-129">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="36792-129">-SubscriptionId</span></span>
<span data-ttu-id="36792-130">Die Microsoft Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="36792-130">The Microsoft Azure subscription ID.</span></span>

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

### <span data-ttu-id="36792-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36792-131">CommonParameters</span></span>
<span data-ttu-id="36792-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36792-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36792-133">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="36792-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36792-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="36792-134">INPUTS</span></span>

### <span data-ttu-id="36792-135">Microsoft. Azure. PowerShell. Cmdlets. AppConfiguration. Models. IAppConfigurationIdentity</span><span class="sxs-lookup"><span data-stu-id="36792-135">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.IAppConfigurationIdentity</span></span>

## <span data-ttu-id="36792-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="36792-136">OUTPUTS</span></span>

### <span data-ttu-id="36792-137">Microsoft. Azure. PowerShell. Cmdlets. AppConfiguration. Models. Api20200601. IConfigurationStore</span><span class="sxs-lookup"><span data-stu-id="36792-137">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.Api20200601.IConfigurationStore</span></span>

## <span data-ttu-id="36792-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="36792-138">NOTES</span></span>

<span data-ttu-id="36792-139">Aliase</span><span class="sxs-lookup"><span data-stu-id="36792-139">ALIASES</span></span>

<span data-ttu-id="36792-140">komplexe Parameter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="36792-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="36792-141">Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="36792-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="36792-142">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="36792-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="36792-143">Inputobject <IAppConfigurationIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="36792-143">INPUTOBJECT <IAppConfigurationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="36792-144">`[ConfigStoreName <String>]`: Der Name des Konfigurationsspeichers.</span><span class="sxs-lookup"><span data-stu-id="36792-144">`[ConfigStoreName <String>]`: The name of the configuration store.</span></span>
  - <span data-ttu-id="36792-145">`[GroupName <String>]`: Der Name der privaten Link Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="36792-145">`[GroupName <String>]`: The name of the private link resource group.</span></span>
  - <span data-ttu-id="36792-146">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="36792-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="36792-147">`[PrivateEndpointConnectionName <String>]`: Privater Endpunkt-Verbindungsname</span><span class="sxs-lookup"><span data-stu-id="36792-147">`[PrivateEndpointConnectionName <String>]`: Private endpoint connection name</span></span>
  - <span data-ttu-id="36792-148">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe, zu der die Container Registrierung gehört.</span><span class="sxs-lookup"><span data-stu-id="36792-148">`[ResourceGroupName <String>]`: The name of the resource group to which the container registry belongs.</span></span>
  - <span data-ttu-id="36792-149">`[SubscriptionId <String>]`: Die Microsoft Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="36792-149">`[SubscriptionId <String>]`: The Microsoft Azure subscription ID.</span></span>

## <span data-ttu-id="36792-150">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="36792-150">RELATED LINKS</span></span>

