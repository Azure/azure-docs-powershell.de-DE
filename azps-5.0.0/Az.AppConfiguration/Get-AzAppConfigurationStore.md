---
external help file: ''
Module Name: Az.AppConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.appconfiguration/get-azappconfigurationstore
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Get-AzAppConfigurationStore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Get-AzAppConfigurationStore.md
ms.openlocfilehash: 88847cbb128f5545a235eb2c5c02043231ff1078
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94303850"
---
# <span data-ttu-id="43fec-101">Get-AzAppConfigurationStore</span><span class="sxs-lookup"><span data-stu-id="43fec-101">Get-AzAppConfigurationStore</span></span>

## <span data-ttu-id="43fec-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="43fec-102">SYNOPSIS</span></span>
<span data-ttu-id="43fec-103">Abrufen oder Auflisten von App-Konfigurations speichern.</span><span class="sxs-lookup"><span data-stu-id="43fec-103">Get or list app configuration stores.</span></span>

## <span data-ttu-id="43fec-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="43fec-104">SYNTAX</span></span>

### <span data-ttu-id="43fec-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="43fec-105">List (Default)</span></span>
```
Get-AzAppConfigurationStore [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="43fec-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="43fec-106">Get</span></span>
```
Get-AzAppConfigurationStore -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="43fec-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="43fec-107">GetViaIdentity</span></span>
```
Get-AzAppConfigurationStore -InputObject <IAppConfigurationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="43fec-108">List1</span><span class="sxs-lookup"><span data-stu-id="43fec-108">List1</span></span>
```
Get-AzAppConfigurationStore -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="43fec-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="43fec-109">DESCRIPTION</span></span>
<span data-ttu-id="43fec-110">Abrufen oder Auflisten von App-Konfigurations speichern.</span><span class="sxs-lookup"><span data-stu-id="43fec-110">Get or list app configuration stores.</span></span>

## <span data-ttu-id="43fec-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="43fec-111">EXAMPLES</span></span>

### <span data-ttu-id="43fec-112">Beispiel 1: Auflisten aller App-Konfigurationsspeicher unter einem Abonnement</span><span class="sxs-lookup"><span data-stu-id="43fec-112">Example 1: List all app configuration stores under a subscription</span></span>
```powershell
PS C:\> Get-AzAppConfigurationStore

Location Name               Type
-------- ----               ----
eastus   appconfig-test01   Microsoft.AppConfiguration/configurationStores
eastus   contoso-app-config Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="43fec-113">Dieser Befehl listet alle App-Konfigurationsspeicher unter einem Abonnement auf.</span><span class="sxs-lookup"><span data-stu-id="43fec-113">This command lists all app configuration stores under a subscription.</span></span>

### <span data-ttu-id="43fec-114">Beispiel 2: Auflisten aller App-Konfigurationsspeicher unter einer Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="43fec-114">Example 2: List all app configuration stores under a resource group</span></span>
```powershell
PS C:\> Get-AzAppConfigurationStore -ResourceGroupName azpwsh-manual-test

Location Name             Type
-------- ----             ----
eastus   appconfig-test01 Microsoft.AppConfiguration/configurationStores
eastus   appconfig-test02 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="43fec-115">Dieser Befehl listet alle App-Konfigurationsspeicher unter einer Ressourcengruppe auf.</span><span class="sxs-lookup"><span data-stu-id="43fec-115">This command lists all app configuration stores under a resource group.</span></span>

### <span data-ttu-id="43fec-116">Beispiel 3: Abrufen eines App-Konfigurationsspeichers nach Name</span><span class="sxs-lookup"><span data-stu-id="43fec-116">Example 3: Get an app configuration store by name</span></span>
```powershell
PS C:\> Get-AzAppConfigurationStore -ResourceGroupName azpwsh-manual-test -Name appconfig-test01

Location Name             Type
-------- ----             ----
eastus   appconfig-test01 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="43fec-117">Mit diesem Befehl wird ein App-Konfigurationsspeicher nach Namen abgerufen.</span><span class="sxs-lookup"><span data-stu-id="43fec-117">This command gets an app configuration store by name.</span></span>

### <span data-ttu-id="43fec-118">Beispiel 4: Abrufen eines App-Konfigurationsspeichers nach Pipeline</span><span class="sxs-lookup"><span data-stu-id="43fec-118">Example 4: Get an app configuration store by pipeline</span></span>
```powershell
PS C:\> Get-AzAppConfigurationStore -ResourceGroupName azpwsh-manual-test -Name appconfig-test01 | Get-AzAppConfigurationStore

Location Name             Type
-------- ----             ----
eastus   appconfig-test01 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="43fec-119">Mit diesem Befehl wird ein App-Konfigurationsspeicher nach Pipeline abgerufen.</span><span class="sxs-lookup"><span data-stu-id="43fec-119">This command gets an app configuration store by pipeline.</span></span>

## <span data-ttu-id="43fec-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="43fec-120">PARAMETERS</span></span>

### <span data-ttu-id="43fec-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43fec-121">-DefaultProfile</span></span>
<span data-ttu-id="43fec-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="43fec-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="43fec-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="43fec-123">-InputObject</span></span>
<span data-ttu-id="43fec-124">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="43fec-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="43fec-125">-Name</span><span class="sxs-lookup"><span data-stu-id="43fec-125">-Name</span></span>
<span data-ttu-id="43fec-126">Der Name des Konfigurationsspeichers.</span><span class="sxs-lookup"><span data-stu-id="43fec-126">The name of the configuration store.</span></span>

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

### <span data-ttu-id="43fec-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43fec-127">-ResourceGroupName</span></span>
<span data-ttu-id="43fec-128">Der Name der Ressourcengruppe, zu der die Container Registrierung gehört.</span><span class="sxs-lookup"><span data-stu-id="43fec-128">The name of the resource group to which the container registry belongs.</span></span>

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

### <span data-ttu-id="43fec-129">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="43fec-129">-SubscriptionId</span></span>
<span data-ttu-id="43fec-130">Die Microsoft Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="43fec-130">The Microsoft Azure subscription ID.</span></span>

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

### <span data-ttu-id="43fec-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43fec-131">CommonParameters</span></span>
<span data-ttu-id="43fec-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43fec-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43fec-133">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="43fec-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43fec-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="43fec-134">INPUTS</span></span>

### <span data-ttu-id="43fec-135">Microsoft. Azure. PowerShell. Cmdlets. AppConfiguration. Models. IAppConfigurationIdentity</span><span class="sxs-lookup"><span data-stu-id="43fec-135">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.IAppConfigurationIdentity</span></span>

## <span data-ttu-id="43fec-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="43fec-136">OUTPUTS</span></span>

### <span data-ttu-id="43fec-137">Microsoft. Azure. PowerShell. Cmdlets. AppConfiguration. Models. Api20200601. IConfigurationStore</span><span class="sxs-lookup"><span data-stu-id="43fec-137">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.Api20200601.IConfigurationStore</span></span>

## <span data-ttu-id="43fec-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="43fec-138">NOTES</span></span>

<span data-ttu-id="43fec-139">Aliase</span><span class="sxs-lookup"><span data-stu-id="43fec-139">ALIASES</span></span>

<span data-ttu-id="43fec-140">komplexe Parameter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="43fec-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="43fec-141">Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="43fec-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="43fec-142">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="43fec-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="43fec-143">Inputobject <IAppConfigurationIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="43fec-143">INPUTOBJECT <IAppConfigurationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="43fec-144">`[ConfigStoreName <String>]`: Der Name des Konfigurationsspeichers.</span><span class="sxs-lookup"><span data-stu-id="43fec-144">`[ConfigStoreName <String>]`: The name of the configuration store.</span></span>
  - <span data-ttu-id="43fec-145">`[GroupName <String>]`: Der Name der privaten Link Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="43fec-145">`[GroupName <String>]`: The name of the private link resource group.</span></span>
  - <span data-ttu-id="43fec-146">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="43fec-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="43fec-147">`[PrivateEndpointConnectionName <String>]`: Privater Endpunkt-Verbindungsname</span><span class="sxs-lookup"><span data-stu-id="43fec-147">`[PrivateEndpointConnectionName <String>]`: Private endpoint connection name</span></span>
  - <span data-ttu-id="43fec-148">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe, zu der die Container Registrierung gehört.</span><span class="sxs-lookup"><span data-stu-id="43fec-148">`[ResourceGroupName <String>]`: The name of the resource group to which the container registry belongs.</span></span>
  - <span data-ttu-id="43fec-149">`[SubscriptionId <String>]`: Die Microsoft Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="43fec-149">`[SubscriptionId <String>]`: The Microsoft Azure subscription ID.</span></span>

## <span data-ttu-id="43fec-150">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="43fec-150">RELATED LINKS</span></span>

