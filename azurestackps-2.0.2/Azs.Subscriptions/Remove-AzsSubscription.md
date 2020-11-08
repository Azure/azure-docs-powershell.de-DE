---
external help file: ''
Module Name: Azs.Subscriptions
online version: https://docs.microsoft.com/powershell/module/azs.subscriptions/remove-azssubscription
schema: 2.0.0
ms.openlocfilehash: b6fddf677cd619dad577b7bca8286671b85d0791
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94007227"
---
# <span data-ttu-id="c6049-101">Remove-AzsSubscription</span><span class="sxs-lookup"><span data-stu-id="c6049-101">Remove-AzsSubscription</span></span>

## <span data-ttu-id="c6049-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c6049-102">SYNOPSIS</span></span>


## <span data-ttu-id="c6049-103">Syntax</span><span class="sxs-lookup"><span data-stu-id="c6049-103">SYNTAX</span></span>

### <span data-ttu-id="c6049-104">Löschen (Standard)</span><span class="sxs-lookup"><span data-stu-id="c6049-104">Delete (Default)</span></span>
```
Remove-AzsSubscription -SubscriptionId <String> [-DefaultProfile <PSObject>] [-Force] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="c6049-105">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="c6049-105">DeleteViaIdentity</span></span>
```
Remove-AzsSubscription -InputObject <ISubscriptionIdentity> [-DefaultProfile <PSObject>] [-Force] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c6049-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c6049-106">DESCRIPTION</span></span>


## <span data-ttu-id="c6049-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c6049-107">EXAMPLES</span></span>

### <span data-ttu-id="c6049-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c6049-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzsSubscription -SubscriptionId d387f779-85d8-40b6-8607-8306295ebff9

```

<span data-ttu-id="c6049-109">Löschen Sie das angegebene-Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c6049-109">Delete the specifed subscription.</span></span>

## <span data-ttu-id="c6049-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="c6049-110">PARAMETERS</span></span>

### <span data-ttu-id="c6049-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6049-111">-DefaultProfile</span></span>


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

### <span data-ttu-id="c6049-112">-Force</span><span class="sxs-lookup"><span data-stu-id="c6049-112">-Force</span></span>


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

### <span data-ttu-id="c6049-113">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="c6049-113">-InputObject</span></span>
<span data-ttu-id="c6049-114">Informationen zum Erstellen finden Sie unter Abschnitt "Notizen" für Inputobject-Eigenschaften und Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="c6049-114">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="c6049-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c6049-115">-PassThru</span></span>


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

### <span data-ttu-id="c6049-116">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="c6049-116">-SubscriptionId</span></span>


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

### <span data-ttu-id="c6049-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c6049-117">-Confirm</span></span>
<span data-ttu-id="c6049-118">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c6049-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c6049-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c6049-119">-WhatIf</span></span>
<span data-ttu-id="c6049-120">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c6049-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c6049-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c6049-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c6049-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6049-122">CommonParameters</span></span>
<span data-ttu-id="c6049-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c6049-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6049-124">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c6049-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6049-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c6049-125">INPUTS</span></span>

### <span data-ttu-id="c6049-126">Microsoft. Azure. PowerShell. Cmdlets. Subscription. Models. ISubscriptionIdentity</span><span class="sxs-lookup"><span data-stu-id="c6049-126">Microsoft.Azure.PowerShell.Cmdlets.Subscription.Models.ISubscriptionIdentity</span></span>

## <span data-ttu-id="c6049-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c6049-127">OUTPUTS</span></span>

### <span data-ttu-id="c6049-128">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c6049-128">System.Boolean</span></span>



## <span data-ttu-id="c6049-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="c6049-129">NOTES</span></span>

<span data-ttu-id="c6049-130">Komplexe Parametereigenschaften Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="c6049-130">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c6049-131">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="c6049-131">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="c6049-132">Inputobject <ISubscriptionIdentity> :</span><span class="sxs-lookup"><span data-stu-id="c6049-132">INPUTOBJECT <ISubscriptionIdentity>:</span></span> 
  - <span data-ttu-id="c6049-133">`[DelegatedProviderId <String>]`: ID des Delegierten Anbieters.</span><span class="sxs-lookup"><span data-stu-id="c6049-133">`[DelegatedProviderId <String>]`: Id of the delegated provider.</span></span>
  - <span data-ttu-id="c6049-134">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="c6049-134">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="c6049-135">`[OfferName <String>]`: Name des Angebots.</span><span class="sxs-lookup"><span data-stu-id="c6049-135">`[OfferName <String>]`: Name of the offer.</span></span>
  - <span data-ttu-id="c6049-136">`[SubscriptionId <String>]`: ID des Abonnements.</span><span class="sxs-lookup"><span data-stu-id="c6049-136">`[SubscriptionId <String>]`: Id of the subscription.</span></span>

## <span data-ttu-id="c6049-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c6049-137">RELATED LINKS</span></span>

