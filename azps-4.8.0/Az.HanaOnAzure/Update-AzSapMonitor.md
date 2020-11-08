---
external help file: ''
Module Name: Az.HanaOnAzure
online version: https://docs.microsoft.com/en-us/powershell/module/az.hanaonazure/update-azsapmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Update-AzSapMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Update-AzSapMonitor.md
ms.openlocfilehash: 9d87cfff428a5c3c176bea4deff95d0c652dc45a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94166459"
---
# <span data-ttu-id="9d6ad-101">Update-AzSapMonitor</span><span class="sxs-lookup"><span data-stu-id="9d6ad-101">Update-AzSapMonitor</span></span>

## <span data-ttu-id="9d6ad-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9d6ad-102">SYNOPSIS</span></span>
<span data-ttu-id="9d6ad-103">Patches das Feld "Tags" eines SAP-Monitors für das angegebene Abonnement, die Ressourcengruppe und den Namen des Monitors.</span><span class="sxs-lookup"><span data-stu-id="9d6ad-103">Patches the Tags field of a SAP monitor for the specified subscription, resource group, and monitor name.</span></span>

## <span data-ttu-id="9d6ad-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9d6ad-104">SYNTAX</span></span>

### <span data-ttu-id="9d6ad-105">UpdateExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="9d6ad-105">UpdateExpanded (Default)</span></span>
```
Update-AzSapMonitor -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="9d6ad-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="9d6ad-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzSapMonitor -InputObject <IHanaOnAzureIdentity> [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="9d6ad-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9d6ad-107">DESCRIPTION</span></span>
<span data-ttu-id="9d6ad-108">Patches das Feld "Tags" eines SAP-Monitors für das angegebene Abonnement, die Ressourcengruppe und den Namen des Monitors.</span><span class="sxs-lookup"><span data-stu-id="9d6ad-108">Patches the Tags field of a SAP monitor for the specified subscription, resource group, and monitor name.</span></span>

## <span data-ttu-id="9d6ad-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9d6ad-109">EXAMPLES</span></span>

### <span data-ttu-id="9d6ad-110">Beispiel 1: Aktualisieren eines SAP-Monitors nach Name</span><span class="sxs-lookup"><span data-stu-id="9d6ad-110">Example 1: Update a SAP monitor by name</span></span>
```powershell
PS C:\> Update-AzSapMonitor -ResourceGroupName nancyc-hn1 -Name ps-spamonitor-t01 -Tag @{'key'=1;'key2'=2; 'key3'=3}

Location Name              Type
-------- ----              ----
westus2  ps-spamonitor-t01 Microsoft.HanaOnAzure/sapMonitors
```

<span data-ttu-id="9d6ad-111">Mit diesen Befehlen wird ein SAP-Monitor nach Name aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="9d6ad-111">This commands updates a SAP monitor by name.</span></span>

### <span data-ttu-id="9d6ad-112">Beispiel 2: Aktualisieren eines SAP-Monitors nach Objekt</span><span class="sxs-lookup"><span data-stu-id="9d6ad-112">Example 2: Update a SAP monitor by object</span></span>
```powershell
PS C:\> $sap = Get-AzSapMonitor -ResourceGroupName nancyc-hn1 -Name ps-sapmonitor-t01
PS C:\> Update-AzSapMonitor -InputObject $sap -Tag @{'key'=1;'key2'=2; 'key3'=3}

Location Name              Type
-------- ----              ----
westus2  ps-sapmonitor-t01 Microsoft.HanaOnAzure/sapMonitors
```

<span data-ttu-id="9d6ad-113">Mit diesen Befehlen wird ein SAP-Monitor nach Objekt aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="9d6ad-113">This commands updates a SAP monitor by object.</span></span>

## <span data-ttu-id="9d6ad-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="9d6ad-114">PARAMETERS</span></span>

### <span data-ttu-id="9d6ad-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d6ad-115">-DefaultProfile</span></span>
<span data-ttu-id="9d6ad-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="9d6ad-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9d6ad-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="9d6ad-117">-InputObject</span></span>
<span data-ttu-id="9d6ad-118">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="9d6ad-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.IHanaOnAzureIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9d6ad-119">-Name</span><span class="sxs-lookup"><span data-stu-id="9d6ad-119">-Name</span></span>
<span data-ttu-id="9d6ad-120">Der Name der SAP-Monitor Ressource.</span><span class="sxs-lookup"><span data-stu-id="9d6ad-120">Name of the SAP monitor resource.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: SapMonitorName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d6ad-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9d6ad-121">-ResourceGroupName</span></span>
<span data-ttu-id="9d6ad-122">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="9d6ad-122">Name of the resource group.</span></span>

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

### <span data-ttu-id="9d6ad-123">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="9d6ad-123">-SubscriptionId</span></span>
<span data-ttu-id="9d6ad-124">Abonnement-ID, die das Microsoft Azure-Abonnement eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="9d6ad-124">Subscription ID which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="9d6ad-125">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="9d6ad-125">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="9d6ad-126">-Tag</span><span class="sxs-lookup"><span data-stu-id="9d6ad-126">-Tag</span></span>
<span data-ttu-id="9d6ad-127">Tags-Feld der Ressource.</span><span class="sxs-lookup"><span data-stu-id="9d6ad-127">Tags field of the resource.</span></span>

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

### <span data-ttu-id="9d6ad-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="9d6ad-128">-Confirm</span></span>
<span data-ttu-id="9d6ad-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9d6ad-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9d6ad-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9d6ad-130">-WhatIf</span></span>
<span data-ttu-id="9d6ad-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9d6ad-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9d6ad-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9d6ad-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9d6ad-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d6ad-133">CommonParameters</span></span>
<span data-ttu-id="9d6ad-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d6ad-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d6ad-135">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9d6ad-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d6ad-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9d6ad-136">INPUTS</span></span>

### <span data-ttu-id="9d6ad-137">Microsoft. Azure. PowerShell. Cmdlets. HanaOnAzure. Models. IHanaOnAzureIdentity</span><span class="sxs-lookup"><span data-stu-id="9d6ad-137">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.IHanaOnAzureIdentity</span></span>

## <span data-ttu-id="9d6ad-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9d6ad-138">OUTPUTS</span></span>

### <span data-ttu-id="9d6ad-139">Microsoft. Azure. PowerShell. Cmdlets. HanaOnAzure. Models. Api20200207Preview. ISapMonitor</span><span class="sxs-lookup"><span data-stu-id="9d6ad-139">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.Api20200207Preview.ISapMonitor</span></span>

## <span data-ttu-id="9d6ad-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="9d6ad-140">NOTES</span></span>

<span data-ttu-id="9d6ad-141">Aliase</span><span class="sxs-lookup"><span data-stu-id="9d6ad-141">ALIASES</span></span>

<span data-ttu-id="9d6ad-142">komplexe Parameter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="9d6ad-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="9d6ad-143">Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="9d6ad-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="9d6ad-144">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="9d6ad-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="9d6ad-145">Inputobject <IHanaOnAzureIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="9d6ad-145">INPUTOBJECT <IHanaOnAzureIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="9d6ad-146">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="9d6ad-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="9d6ad-147">`[Location <String>]`: Der Speicherort des gelöschten Tresors.</span><span class="sxs-lookup"><span data-stu-id="9d6ad-147">`[Location <String>]`: The location of the deleted vault.</span></span>
  - <span data-ttu-id="9d6ad-148">`[OperationKind <AccessPolicyUpdateKind?>]`: Name des Vorgangs</span><span class="sxs-lookup"><span data-stu-id="9d6ad-148">`[OperationKind <AccessPolicyUpdateKind?>]`: Name of the operation</span></span>
  - <span data-ttu-id="9d6ad-149">`[ProviderInstanceName <String>]`: Name der Anbieterinstanz.</span><span class="sxs-lookup"><span data-stu-id="9d6ad-149">`[ProviderInstanceName <String>]`: Name of the provider instance.</span></span>
  - <span data-ttu-id="9d6ad-150">`[ResourceGroupName <String>]`: Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="9d6ad-150">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="9d6ad-151">`[ResourceName <String>]`: Der Name der Identitäts Ressource.</span><span class="sxs-lookup"><span data-stu-id="9d6ad-151">`[ResourceName <String>]`: The name of the identity resource.</span></span>
  - <span data-ttu-id="9d6ad-152">`[SapMonitorName <String>]`: Name der SAP-Monitor Ressource.</span><span class="sxs-lookup"><span data-stu-id="9d6ad-152">`[SapMonitorName <String>]`: Name of the SAP monitor resource.</span></span>
  - <span data-ttu-id="9d6ad-153">`[Scope <String>]`: Der Ressourcenanbieter Bereich der Ressource.</span><span class="sxs-lookup"><span data-stu-id="9d6ad-153">`[Scope <String>]`: The resource provider scope of the resource.</span></span> <span data-ttu-id="9d6ad-154">Übergeordnete Ressource, die durch verwaltete Identitäten erweitert wird.</span><span class="sxs-lookup"><span data-stu-id="9d6ad-154">Parent resource being extended by Managed Identities.</span></span>
  - <span data-ttu-id="9d6ad-155">`[SubscriptionId <String>]`: Abonnement-ID, die das Microsoft Azure-Abonnement eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="9d6ad-155">`[SubscriptionId <String>]`: Subscription ID which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="9d6ad-156">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="9d6ad-156">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="9d6ad-157">`[VaultName <String>]`: Name des Tresors</span><span class="sxs-lookup"><span data-stu-id="9d6ad-157">`[VaultName <String>]`: Name of the vault</span></span>

## <span data-ttu-id="9d6ad-158">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9d6ad-158">RELATED LINKS</span></span>

