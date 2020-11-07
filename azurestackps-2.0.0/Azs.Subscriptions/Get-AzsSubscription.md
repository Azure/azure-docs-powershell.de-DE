---
external help file: ''
Module Name: Azs.Subscriptions
online version: https://docs.microsoft.com/powershell/module/azs.subscriptions/get-azssubscription
schema: 2.0.0
ms.openlocfilehash: 7dce95be9a936d341e0f063fd6d89701b18c2ce7
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844748"
---
# <span data-ttu-id="6a129-101">Get-AzsSubscription</span><span class="sxs-lookup"><span data-stu-id="6a129-101">Get-AzsSubscription</span></span>

## <span data-ttu-id="6a129-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6a129-102">SYNOPSIS</span></span>
<span data-ttu-id="6a129-103">Ruft Details zu bestimmten Abonnements ab.</span><span class="sxs-lookup"><span data-stu-id="6a129-103">Gets details about particular subscription.</span></span>

## <span data-ttu-id="6a129-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6a129-104">SYNTAX</span></span>

### <span data-ttu-id="6a129-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="6a129-105">List (Default)</span></span>
```
Get-AzsSubscription [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="6a129-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="6a129-106">Get</span></span>
```
Get-AzsSubscription -SubscriptionId <String[]> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="6a129-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="6a129-107">GetViaIdentity</span></span>
```
Get-AzsSubscription -InputObject <ISubscriptionIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="6a129-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6a129-108">DESCRIPTION</span></span>
<span data-ttu-id="6a129-109">Ruft Details zu bestimmten Abonnements ab.</span><span class="sxs-lookup"><span data-stu-id="6a129-109">Gets details about particular subscription.</span></span>

## <span data-ttu-id="6a129-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6a129-110">EXAMPLES</span></span>

### <span data-ttu-id="6a129-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="6a129-111">Example 1</span></span>
```powershell
PS C:\> Get-AzsSubscription | fl *

DisplayName    : Test User
Id             : /subscriptions/97d84f7a-bef7-4f2d-b651-c553be472311
OfferId        : /delegatedProviders/default/offers/TestOffer-590376ac-c8dd-4b3d-9674-b5b8fcde095b
State          : Enabled
SubscriptionId : 97d84f7a-bef7-4f2d-b651-c553be472311
TenantId       : 6ca57aaf-0074-498a-9c96-2b097515e8cb

DisplayName    : cnur
Id             : /subscriptions/ed3e275b-87d1-4e94-9962-b3700287bdbc
OfferId        : /delegatedProviders/default/offers/cnur4866tenantsubsvcoffer843
State          : Enabled
SubscriptionId : ed3e275b-87d1-4e94-9962-b3700287bdbc
TenantId       : 6ca57aaf-0074-498a-9c96-2b097515e8cb
```

<span data-ttu-id="6a129-112">Rufen Sie die Liste der Abonnements ab.</span><span class="sxs-lookup"><span data-stu-id="6a129-112">Get the list of subscriptions.</span></span>

## <span data-ttu-id="6a129-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="6a129-113">PARAMETERS</span></span>

### <span data-ttu-id="6a129-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a129-114">-DefaultProfile</span></span>
<span data-ttu-id="6a129-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="6a129-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6a129-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="6a129-116">-InputObject</span></span>
<span data-ttu-id="6a129-117">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="6a129-117">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Subscription.Models.ISubscriptionIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="6a129-118">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="6a129-118">-SubscriptionId</span></span>
<span data-ttu-id="6a129-119">Die ID des Abonnements.</span><span class="sxs-lookup"><span data-stu-id="6a129-119">Id of the subscription.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="6a129-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a129-120">CommonParameters</span></span>
<span data-ttu-id="6a129-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6a129-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a129-122">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6a129-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a129-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6a129-123">INPUTS</span></span>

### <span data-ttu-id="6a129-124">Microsoft. Azure. PowerShell. Cmdlets. Subscription. Models. ISubscriptionIdentity</span><span class="sxs-lookup"><span data-stu-id="6a129-124">Microsoft.Azure.PowerShell.Cmdlets.Subscription.Models.ISubscriptionIdentity</span></span>

## <span data-ttu-id="6a129-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6a129-125">OUTPUTS</span></span>

### <span data-ttu-id="6a129-126">Microsoft. Azure. PowerShell. Cmdlets. Subscription. Models. Api20151101. ISubscription</span><span class="sxs-lookup"><span data-stu-id="6a129-126">Microsoft.Azure.PowerShell.Cmdlets.Subscription.Models.Api20151101.ISubscription</span></span>



## <span data-ttu-id="6a129-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="6a129-127">NOTES</span></span>

<span data-ttu-id="6a129-128">Komplexe Parametereigenschaften Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="6a129-128">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="6a129-129">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="6a129-129">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="6a129-130">Inputobject <ISubscriptionIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="6a129-130">INPUTOBJECT <ISubscriptionIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="6a129-131">`[DelegatedProviderId <String>]`: ID des Delegierten Anbieters.</span><span class="sxs-lookup"><span data-stu-id="6a129-131">`[DelegatedProviderId <String>]`: Id of the delegated provider.</span></span>
  - <span data-ttu-id="6a129-132">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="6a129-132">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="6a129-133">`[OfferName <String>]`: Name des Angebots.</span><span class="sxs-lookup"><span data-stu-id="6a129-133">`[OfferName <String>]`: Name of the offer.</span></span>
  - <span data-ttu-id="6a129-134">`[SubscriptionId <String>]`: ID des Abonnements.</span><span class="sxs-lookup"><span data-stu-id="6a129-134">`[SubscriptionId <String>]`: Id of the subscription.</span></span>

## <span data-ttu-id="6a129-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6a129-135">RELATED LINKS</span></span>

