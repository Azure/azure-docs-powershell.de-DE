---
external help file: ''
Module Name: Azs.Network.Admin
online version: https://docs.microsoft.com/powershell/module/azs.network.admin/get-azsnetworkadminoverview
schema: 2.0.0
ms.openlocfilehash: 8559b8cdde324c3927ac835f49291441a4e58847
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/24/2020
ms.locfileid: "94005420"
---
# <span data-ttu-id="b08dc-101">Get-AzsNetworkAdminOverview</span><span class="sxs-lookup"><span data-stu-id="b08dc-101">Get-AzsNetworkAdminOverview</span></span>

## <span data-ttu-id="b08dc-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b08dc-102">SYNOPSIS</span></span>
<span data-ttu-id="b08dc-103">Verschaffen Sie sich einen Überblick über den Zustand des Netzwerkressourcen Anbieters.</span><span class="sxs-lookup"><span data-stu-id="b08dc-103">Get an overview of the state of the network resource provider.</span></span>

## <span data-ttu-id="b08dc-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b08dc-104">SYNTAX</span></span>

### <span data-ttu-id="b08dc-105">Abrufen (Standard)</span><span class="sxs-lookup"><span data-stu-id="b08dc-105">Get (Default)</span></span>
```
Get-AzsNetworkAdminOverview [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="b08dc-106">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="b08dc-106">GetViaIdentity</span></span>
```
Get-AzsNetworkAdminOverview -InputObject <INetworkAdminIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="b08dc-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b08dc-107">DESCRIPTION</span></span>
<span data-ttu-id="b08dc-108">Verschaffen Sie sich einen Überblick über den Zustand des Netzwerkressourcen Anbieters.</span><span class="sxs-lookup"><span data-stu-id="b08dc-108">Get an overview of the state of the network resource provider.</span></span>

## <span data-ttu-id="b08dc-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b08dc-109">EXAMPLES</span></span>

### <span data-ttu-id="b08dc-110">--------------------------Beispiel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="b08dc-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```powershell
Get-AzsNetworkAdminOverview
To view examples, please use the -Online parameter with Get-Help or navigate to: https://docs.microsoft.com/powershell/module/azs.network.admin/get-azsnetworkadminoverview
```



## <span data-ttu-id="b08dc-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="b08dc-111">PARAMETERS</span></span>

### <span data-ttu-id="b08dc-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b08dc-112">-DefaultProfile</span></span>
<span data-ttu-id="b08dc-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b08dc-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b08dc-114">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="b08dc-114">-InputObject</span></span>
<span data-ttu-id="b08dc-115">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="b08dc-115">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="b08dc-116">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="b08dc-116">-SubscriptionId</span></span>
<span data-ttu-id="b08dc-117">Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="b08dc-117">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="b08dc-118">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="b08dc-118">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="b08dc-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b08dc-119">CommonParameters</span></span>
<span data-ttu-id="b08dc-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b08dc-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b08dc-121">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b08dc-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b08dc-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b08dc-122">INPUTS</span></span>

### <span data-ttu-id="b08dc-123">Microsoft. Azure. PowerShell. Cmdlets. NetworkAdmin. Models. INetworkAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="b08dc-123">Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.INetworkAdminIdentity</span></span>

## <span data-ttu-id="b08dc-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b08dc-124">OUTPUTS</span></span>

### <span data-ttu-id="b08dc-125">Microsoft. Azure. PowerShell. Cmdlets. NetworkAdmin. Models. Api20150615. IAdminOverview</span><span class="sxs-lookup"><span data-stu-id="b08dc-125">Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.Api20150615.IAdminOverview</span></span>



## <span data-ttu-id="b08dc-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="b08dc-126">NOTES</span></span>

<span data-ttu-id="b08dc-127">Komplexe Parametereigenschaften Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="b08dc-127">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b08dc-128">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="b08dc-128">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="b08dc-129">Inputobject <INetworkAdminIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="b08dc-129">INPUTOBJECT <INetworkAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b08dc-130">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="b08dc-130">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b08dc-131">`[Location <String>]`: Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="b08dc-131">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="b08dc-132">`[ResourceName <String>]`: Name der Ressource.</span><span class="sxs-lookup"><span data-stu-id="b08dc-132">`[ResourceName <String>]`: Name of the resource.</span></span>
  - <span data-ttu-id="b08dc-133">`[SubscriptionId <String>]`: Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="b08dc-133">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="b08dc-134">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="b08dc-134">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="b08dc-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b08dc-135">RELATED LINKS</span></span>

