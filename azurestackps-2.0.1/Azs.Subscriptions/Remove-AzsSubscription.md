---
external help file: ''
Module Name: Azs.Subscriptions
online version: https://docs.microsoft.com/powershell/module/azs.subscriptions/remove-azssubscription
schema: 2.0.0
ms.openlocfilehash: b6fddf677cd619dad577b7bca8286671b85d0791
ms.sourcegitcommit: 5523170e571fbd1dc93bd0fa4223aba3b324d3b0
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2020
ms.locfileid: "94005596"
---
# <span data-ttu-id="96381-101">Remove-AzsSubscription</span><span class="sxs-lookup"><span data-stu-id="96381-101">Remove-AzsSubscription</span></span>

## <span data-ttu-id="96381-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="96381-102">SYNOPSIS</span></span>


## <span data-ttu-id="96381-103">Syntax</span><span class="sxs-lookup"><span data-stu-id="96381-103">SYNTAX</span></span>

### <span data-ttu-id="96381-104">Löschen (Standard)</span><span class="sxs-lookup"><span data-stu-id="96381-104">Delete (Default)</span></span>
```
Remove-AzsSubscription -SubscriptionId <String> [-DefaultProfile <PSObject>] [-Force] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="96381-105">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="96381-105">DeleteViaIdentity</span></span>
```
Remove-AzsSubscription -InputObject <ISubscriptionIdentity> [-DefaultProfile <PSObject>] [-Force] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="96381-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="96381-106">DESCRIPTION</span></span>


## <span data-ttu-id="96381-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="96381-107">EXAMPLES</span></span>

### <span data-ttu-id="96381-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="96381-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzsSubscription -SubscriptionId d387f779-85d8-40b6-8607-8306295ebff9

```

<span data-ttu-id="96381-109">Löschen Sie das angegebene-Abonnement.</span><span class="sxs-lookup"><span data-stu-id="96381-109">Delete the specifed subscription.</span></span>

## <span data-ttu-id="96381-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="96381-110">PARAMETERS</span></span>

### <span data-ttu-id="96381-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96381-111">-DefaultProfile</span></span>


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

### <span data-ttu-id="96381-112">-Force</span><span class="sxs-lookup"><span data-stu-id="96381-112">-Force</span></span>


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

### <span data-ttu-id="96381-113">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="96381-113">-InputObject</span></span>
<span data-ttu-id="96381-114">Informationen zum Erstellen finden Sie unter Abschnitt "Notizen" für Inputobject-Eigenschaften und Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="96381-114">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Subscription.Models.ISubscriptionIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="96381-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="96381-115">-PassThru</span></span>


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

### <span data-ttu-id="96381-116">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="96381-116">-SubscriptionId</span></span>


```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="96381-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="96381-117">-Confirm</span></span>
<span data-ttu-id="96381-118">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="96381-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="96381-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="96381-119">-WhatIf</span></span>
<span data-ttu-id="96381-120">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="96381-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="96381-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="96381-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="96381-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96381-122">CommonParameters</span></span>
<span data-ttu-id="96381-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="96381-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96381-124">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="96381-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96381-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="96381-125">INPUTS</span></span>

### <span data-ttu-id="96381-126">Microsoft. Azure. PowerShell. Cmdlets. Subscription. Models. ISubscriptionIdentity</span><span class="sxs-lookup"><span data-stu-id="96381-126">Microsoft.Azure.PowerShell.Cmdlets.Subscription.Models.ISubscriptionIdentity</span></span>

## <span data-ttu-id="96381-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="96381-127">OUTPUTS</span></span>

### <span data-ttu-id="96381-128">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="96381-128">System.Boolean</span></span>



## <span data-ttu-id="96381-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="96381-129">NOTES</span></span>

<span data-ttu-id="96381-130">Komplexe Parametereigenschaften Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="96381-130">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="96381-131">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="96381-131">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="96381-132">Inputobject <ISubscriptionIdentity> :</span><span class="sxs-lookup"><span data-stu-id="96381-132">INPUTOBJECT <ISubscriptionIdentity>:</span></span> 
  - <span data-ttu-id="96381-133">`[DelegatedProviderId <String>]`: ID des Delegierten Anbieters.</span><span class="sxs-lookup"><span data-stu-id="96381-133">`[DelegatedProviderId <String>]`: Id of the delegated provider.</span></span>
  - <span data-ttu-id="96381-134">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="96381-134">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="96381-135">`[OfferName <String>]`: Name des Angebots.</span><span class="sxs-lookup"><span data-stu-id="96381-135">`[OfferName <String>]`: Name of the offer.</span></span>
  - <span data-ttu-id="96381-136">`[SubscriptionId <String>]`: ID des Abonnements.</span><span class="sxs-lookup"><span data-stu-id="96381-136">`[SubscriptionId <String>]`: Id of the subscription.</span></span>

## <span data-ttu-id="96381-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="96381-137">RELATED LINKS</span></span>

