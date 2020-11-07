---
external help file: ''
Module Name: Azs.Network.Admin
online version: https://docs.microsoft.com/powershell/module/azs.network.admin/get-azsnetworkquota
schema: 2.0.0
ms.openlocfilehash: e9fbcb04841c08fe396cc56d92acd0abdaf94089
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842532"
---
# <span data-ttu-id="09489-101">Get-AzsNetworkQuota</span><span class="sxs-lookup"><span data-stu-id="09489-101">Get-AzsNetworkQuota</span></span>

## <span data-ttu-id="09489-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="09489-102">SYNOPSIS</span></span>
<span data-ttu-id="09489-103">Abrufen eines Kontingents anhand des Namens</span><span class="sxs-lookup"><span data-stu-id="09489-103">Get a quota by name.</span></span>

## <span data-ttu-id="09489-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="09489-104">SYNTAX</span></span>

### <span data-ttu-id="09489-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="09489-105">List (Default)</span></span>
```
Get-AzsNetworkQuota [-Location <String>] [-SubscriptionId <String[]>] [-Filter <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="09489-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="09489-106">Get</span></span>
```
Get-AzsNetworkQuota -Name <String> [-Location <String>] [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="09489-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="09489-107">GetViaIdentity</span></span>
```
Get-AzsNetworkQuota -InputObject <INetworkAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="09489-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="09489-108">DESCRIPTION</span></span>
<span data-ttu-id="09489-109">Alle Kontingente auflisten.</span><span class="sxs-lookup"><span data-stu-id="09489-109">List all quotas.</span></span>
<span data-ttu-id="09489-110">Begrenzen Sie die Liste, indem Sie einen Namen oder Filter übergeben.</span><span class="sxs-lookup"><span data-stu-id="09489-110">Limit the list by passing a name or filter.</span></span>

## <span data-ttu-id="09489-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="09489-111">EXAMPLES</span></span>

### <span data-ttu-id="09489-112">--------------------------Beispiel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="09489-112">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsNetworkQuota
```

<span data-ttu-id="09489-113">Listet alle Netzwerk Kontingente auf.</span><span class="sxs-lookup"><span data-stu-id="09489-113">Lists all the  network quotas.</span></span>

### <span data-ttu-id="09489-114">--------------------------Beispiel 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="09489-114">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsNetworkQuota -Name NetworkQuota1
```

<span data-ttu-id="09489-115">Ruft das angegebene Netzwerk Kontingent ab.</span><span class="sxs-lookup"><span data-stu-id="09489-115">Gets the specified network quota.</span></span>



## <span data-ttu-id="09489-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="09489-116">PARAMETERS</span></span>

### <span data-ttu-id="09489-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09489-117">-DefaultProfile</span></span>
<span data-ttu-id="09489-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="09489-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="09489-119">-Filter</span><span class="sxs-lookup"><span data-stu-id="09489-119">-Filter</span></span>
<span data-ttu-id="09489-120">OData-Filterparameter</span><span class="sxs-lookup"><span data-stu-id="09489-120">OData filter parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="09489-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="09489-121">-InputObject</span></span>
<span data-ttu-id="09489-122">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="09489-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.INetworkAdminIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="09489-123">-Standort</span><span class="sxs-lookup"><span data-stu-id="09489-123">-Location</span></span>
<span data-ttu-id="09489-124">Der Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="09489-124">Location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Name
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="09489-125">-Name</span><span class="sxs-lookup"><span data-stu-id="09489-125">-Name</span></span>
<span data-ttu-id="09489-126">Der Name der Ressource.</span><span class="sxs-lookup"><span data-stu-id="09489-126">Name of the resource.</span></span>

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

### <span data-ttu-id="09489-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="09489-127">-PassThru</span></span>
<span data-ttu-id="09489-128">Gibt "true" zurück, wenn der Befehl erfolgreich ist</span><span class="sxs-lookup"><span data-stu-id="09489-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="09489-129">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="09489-129">-SubscriptionId</span></span>
<span data-ttu-id="09489-130">Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="09489-130">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="09489-131">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="09489-131">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="09489-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09489-132">CommonParameters</span></span>
<span data-ttu-id="09489-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09489-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09489-134">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="09489-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09489-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="09489-135">INPUTS</span></span>

### <span data-ttu-id="09489-136">Microsoft. Azure. PowerShell. Cmdlets. NetworkAdmin. Models. INetworkAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="09489-136">Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.INetworkAdminIdentity</span></span>

## <span data-ttu-id="09489-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="09489-137">OUTPUTS</span></span>

### <span data-ttu-id="09489-138">Microsoft. Azure. PowerShell. Cmdlets. NetworkAdmin. Models. Api20150615. IQuota</span><span class="sxs-lookup"><span data-stu-id="09489-138">Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.Api20150615.IQuota</span></span>



## <span data-ttu-id="09489-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="09489-139">NOTES</span></span>

<span data-ttu-id="09489-140">Komplexe Parametereigenschaften Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="09489-140">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="09489-141">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="09489-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="09489-142">Inputobject <INetworkAdminIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="09489-142">INPUTOBJECT <INetworkAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="09489-143">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="09489-143">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="09489-144">`[Location <String>]`: Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="09489-144">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="09489-145">`[ResourceName <String>]`: Name der Ressource.</span><span class="sxs-lookup"><span data-stu-id="09489-145">`[ResourceName <String>]`: Name of the resource.</span></span>
  - <span data-ttu-id="09489-146">`[SubscriptionId <String>]`: Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="09489-146">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="09489-147">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="09489-147">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="09489-148">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="09489-148">RELATED LINKS</span></span>

