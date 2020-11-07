---
external help file: ''
Module Name: Azs.Subscriptions
online version: https://docs.microsoft.com/powershell/module/azs.subscriptions/get-azsdelegatedprovideroffer
schema: 2.0.0
ms.openlocfilehash: 118834c020a198d355d3f3b9e6dc17699f88e0cc
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844760"
---
# <span data-ttu-id="fea58-101">Get-AzsDelegatedProviderOffer</span><span class="sxs-lookup"><span data-stu-id="fea58-101">Get-AzsDelegatedProviderOffer</span></span>

## <span data-ttu-id="fea58-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="fea58-102">SYNOPSIS</span></span>
<span data-ttu-id="fea58-103">Rufen Sie das angegebene Angebot für den Delegierten Anbieter ab.</span><span class="sxs-lookup"><span data-stu-id="fea58-103">Get the specified offer for the delegated provider.</span></span>

## <span data-ttu-id="fea58-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="fea58-104">SYNTAX</span></span>

### <span data-ttu-id="fea58-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="fea58-105">List (Default)</span></span>
```
Get-AzsDelegatedProviderOffer -DelegatedProviderId <String> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="fea58-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="fea58-106">Get</span></span>
```
Get-AzsDelegatedProviderOffer -DelegatedProviderId <String> -OfferName <String> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="fea58-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="fea58-107">GetViaIdentity</span></span>
```
Get-AzsDelegatedProviderOffer -InputObject <ISubscriptionIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="fea58-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fea58-108">DESCRIPTION</span></span>
<span data-ttu-id="fea58-109">Rufen Sie das angegebene Angebot für den Delegierten Anbieter ab.</span><span class="sxs-lookup"><span data-stu-id="fea58-109">Get the specified offer for the delegated provider.</span></span>

## <span data-ttu-id="fea58-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fea58-110">EXAMPLES</span></span>

### <span data-ttu-id="fea58-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="fea58-111">Example 1</span></span>
```powershell
PS C:\> Get-AzsDelegatedProviderOffer -DelegatedProviderId 4b763321-23f5-4a45-a44d-9ccfdd705a3d

{{ Add output here }}
```

<span data-ttu-id="fea58-112">Abrufen der Liste der Angebote für den angegebenen Delegierten Anbieter</span><span class="sxs-lookup"><span data-stu-id="fea58-112">Get the list of offers for the specified delegated provider</span></span>

## <span data-ttu-id="fea58-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="fea58-113">PARAMETERS</span></span>

### <span data-ttu-id="fea58-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fea58-114">-DefaultProfile</span></span>
<span data-ttu-id="fea58-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="fea58-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fea58-116">-DelegatedProviderId</span><span class="sxs-lookup"><span data-stu-id="fea58-116">-DelegatedProviderId</span></span>
<span data-ttu-id="fea58-117">Die ID des Delegierten Anbieters.</span><span class="sxs-lookup"><span data-stu-id="fea58-117">Id of the delegated provider.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="fea58-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="fea58-118">-InputObject</span></span>
<span data-ttu-id="fea58-119">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="fea58-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="fea58-120">-Angebotname</span><span class="sxs-lookup"><span data-stu-id="fea58-120">-OfferName</span></span>
<span data-ttu-id="fea58-121">Name des Angebots.</span><span class="sxs-lookup"><span data-stu-id="fea58-121">Name of the offer.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="fea58-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fea58-122">CommonParameters</span></span>
<span data-ttu-id="fea58-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fea58-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fea58-124">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fea58-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fea58-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="fea58-125">INPUTS</span></span>

### <span data-ttu-id="fea58-126">Microsoft. Azure. PowerShell. Cmdlets. Subscription. Models. ISubscriptionIdentity</span><span class="sxs-lookup"><span data-stu-id="fea58-126">Microsoft.Azure.PowerShell.Cmdlets.Subscription.Models.ISubscriptionIdentity</span></span>

## <span data-ttu-id="fea58-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="fea58-127">OUTPUTS</span></span>

### <span data-ttu-id="fea58-128">Microsoft. Azure. PowerShell. Cmdlets. Subscription. Models. Api20151101. IOffer</span><span class="sxs-lookup"><span data-stu-id="fea58-128">Microsoft.Azure.PowerShell.Cmdlets.Subscription.Models.Api20151101.IOffer</span></span>



## <span data-ttu-id="fea58-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="fea58-129">NOTES</span></span>

<span data-ttu-id="fea58-130">Komplexe Parametereigenschaften Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="fea58-130">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="fea58-131">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="fea58-131">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="fea58-132">Inputobject <ISubscriptionIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="fea58-132">INPUTOBJECT <ISubscriptionIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="fea58-133">`[DelegatedProviderId <String>]`: ID des Delegierten Anbieters.</span><span class="sxs-lookup"><span data-stu-id="fea58-133">`[DelegatedProviderId <String>]`: Id of the delegated provider.</span></span>
  - <span data-ttu-id="fea58-134">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="fea58-134">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="fea58-135">`[OfferName <String>]`: Name des Angebots.</span><span class="sxs-lookup"><span data-stu-id="fea58-135">`[OfferName <String>]`: Name of the offer.</span></span>
  - <span data-ttu-id="fea58-136">`[SubscriptionId <String>]`: ID des Abonnements.</span><span class="sxs-lookup"><span data-stu-id="fea58-136">`[SubscriptionId <String>]`: Id of the subscription.</span></span>

## <span data-ttu-id="fea58-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="fea58-137">RELATED LINKS</span></span>

