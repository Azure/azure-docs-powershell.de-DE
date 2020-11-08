---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: 7A45DCAD-88DC-40F0-BBF7-0F531A571CA6
online version: ''
schema: 2.0.0
ms.openlocfilehash: 48b941691366c3af821e3a4cdaa7b07c5e958e16
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005651"
---
# <span data-ttu-id="b85e8-101">Select-AzureSubscription</span><span class="sxs-lookup"><span data-stu-id="b85e8-101">Select-AzureSubscription</span></span>

## <span data-ttu-id="b85e8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b85e8-102">SYNOPSIS</span></span>
<span data-ttu-id="b85e8-103">Ändert das aktuelle und das standardmäßige Azure-Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b85e8-103">Changes the current and default Azure subscriptions.</span></span>

## <span data-ttu-id="b85e8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b85e8-104">SYNTAX</span></span>

### <span data-ttu-id="b85e8-105">SelectSubscriptionByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="b85e8-105">SelectSubscriptionByNameParameterSet (Default)</span></span>
```
Select-AzureSubscription -SubscriptionName <String> [-Account <String>] [-Current] [-PassThru]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="b85e8-106">SelectDefaultSubscriptionByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="b85e8-106">SelectDefaultSubscriptionByNameParameterSet</span></span>
```
Select-AzureSubscription -SubscriptionName <String> [-Account <String>] [-Default] [-PassThru]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="b85e8-107">SelectSubscriptionByIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b85e8-107">SelectSubscriptionByIdParameterSet</span></span>
```
Select-AzureSubscription -SubscriptionId <String> [-Account <String>] [-Current] [-PassThru]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="b85e8-108">SelectDefaultSubscriptionByIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b85e8-108">SelectDefaultSubscriptionByIdParameterSet</span></span>
```
Select-AzureSubscription -SubscriptionId <String> [-Account <String>] [-Default] [-PassThru]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="b85e8-109">NoCurrentSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="b85e8-109">NoCurrentSubscriptionParameterSet</span></span>
```
Select-AzureSubscription [-Account <String>] [-NoCurrent] [-PassThru] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="b85e8-110">NoDefaultSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="b85e8-110">NoDefaultSubscriptionParameterSet</span></span>
```
Select-AzureSubscription [-Account <String>] [-NoDefault] [-PassThru] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="b85e8-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b85e8-111">DESCRIPTION</span></span>
<span data-ttu-id="b85e8-112">Mit dem Cmdlet **Select-AzureSubscription** werden die aktuellen und die standardmäßigen Azure-Abonnements festgelegt und gelöscht.</span><span class="sxs-lookup"><span data-stu-id="b85e8-112">The **Select-AzureSubscription** cmdlet sets and clears the current and default Azure subscriptions.</span></span>

<span data-ttu-id="b85e8-113">Das "aktuelle Abonnement" ist das Abonnement, das standardmäßig in der aktuellen Windows PowerShell-Sitzung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b85e8-113">The "current subscription" is the subscription that is used by default in the current Windows PowerShell session.</span></span>
<span data-ttu-id="b85e8-114">Das Standardabonnement wird standardmäßig in allen Windows PowerShell-Sitzungen verwendet.</span><span class="sxs-lookup"><span data-stu-id="b85e8-114">The "default subscription" is used by default in all Windows PowerShell sessions.</span></span>
<span data-ttu-id="b85e8-115">Mit der Bezeichnung "Aktuelles Abonnement" können Sie ein anderes Abonnement angeben, das standardmäßig für die aktuelle Sitzung verwendet werden soll, ohne das "Standardabonnement" für alle anderen Sitzungen zu ändern.</span><span class="sxs-lookup"><span data-stu-id="b85e8-115">The "current subscription" label lets you specify a different subscription to be used by default for the current session without changing the "default subscription" for all other sessions.</span></span>

<span data-ttu-id="b85e8-116">Die Abonnement Bezeichnung "Standard" wird in ihrer Abonnementdaten Datei gespeichert.</span><span class="sxs-lookup"><span data-stu-id="b85e8-116">The "default" subscription designation is saved in your subscription data file.</span></span>
<span data-ttu-id="b85e8-117">Die sitzungsspezifische Bezeichnung "aktuell" wird nicht gespeichert.</span><span class="sxs-lookup"><span data-stu-id="b85e8-117">The session-specific "current" designation is not saved.</span></span>

<span data-ttu-id="b85e8-118">In diesem Thema wird das Cmdlet in der 0.8.10-Version des Microsoft Azure PowerShell-Moduls beschrieben.</span><span class="sxs-lookup"><span data-stu-id="b85e8-118">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="b85e8-119">Wenn Sie die Version des verwendeten Moduls abrufen möchten, geben Sie in der Azure PowerShell-Konsole `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="b85e8-119">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

## <span data-ttu-id="b85e8-120">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b85e8-120">EXAMPLES</span></span>

### <span data-ttu-id="b85e8-121">Beispiel 1: Einrichten des aktuellen Abonnements</span><span class="sxs-lookup"><span data-stu-id="b85e8-121">Example 1: Set the current subscription</span></span>
```
C:\PS> Select-AzureSubscription -Current -SubscriptionName ContosoEngineering
```

<span data-ttu-id="b85e8-122">Mit diesem Befehl wird "ContosoEngineering" zum aktuellen Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b85e8-122">This command makes "ContosoEngineering" the current subscription.</span></span>

### <span data-ttu-id="b85e8-123">Beispiel 2: Festlegen des Standardabonnements</span><span class="sxs-lookup"><span data-stu-id="b85e8-123">Example 2: Set the default subscription</span></span>
```
C:\PS> Select-AzureSubscription -Default -SubscriptionName ContosoFinance -SubscriptionDataFile "C:\subs\MySubscriptions.xml"
```

<span data-ttu-id="b85e8-124">Mit diesem Befehl wird das Standardabonnement auf "ContosoFinance" geändert.</span><span class="sxs-lookup"><span data-stu-id="b85e8-124">This command changes the default subscription to "ContosoFinance."</span></span> <span data-ttu-id="b85e8-125">Die Einstellung wird in der Subscriptions.xml-Abonnement Datendatei anstelle der Standarddaten Datei für das Abonnement gespeichert.</span><span class="sxs-lookup"><span data-stu-id="b85e8-125">It saves the setting in the Subscriptions.xml subscription data file, instead of the default subscription data file.</span></span>

## <span data-ttu-id="b85e8-126">Parameter</span><span class="sxs-lookup"><span data-stu-id="b85e8-126">PARAMETERS</span></span>

### <span data-ttu-id="b85e8-127">-Konto</span><span class="sxs-lookup"><span data-stu-id="b85e8-127">-Account</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b85e8-128">-Current</span><span class="sxs-lookup"><span data-stu-id="b85e8-128">-Current</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: SelectSubscriptionByNameParameterSet, SelectSubscriptionByIdParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b85e8-129">– Standard</span><span class="sxs-lookup"><span data-stu-id="b85e8-129">-Default</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: SelectDefaultSubscriptionByNameParameterSet, SelectDefaultSubscriptionByIdParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b85e8-130">-Nocurrent</span><span class="sxs-lookup"><span data-stu-id="b85e8-130">-NoCurrent</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: NoCurrentSubscriptionParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b85e8-131">-NODEFAULT</span><span class="sxs-lookup"><span data-stu-id="b85e8-131">-NoDefault</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: NoDefaultSubscriptionParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b85e8-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b85e8-132">-PassThru</span></span>
<span data-ttu-id="b85e8-133">Gibt $true zurück, wenn der Befehl erfolgreich ist, und $false, wenn ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="b85e8-133">Returns $True if the command succeeds and $False if it fails.</span></span>
<span data-ttu-id="b85e8-134">Standardmäßig gibt dieses Cmdlet keine Ausgabe zurück.</span><span class="sxs-lookup"><span data-stu-id="b85e8-134">By default, this cmdlet does not return any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b85e8-135">-Profil</span><span class="sxs-lookup"><span data-stu-id="b85e8-135">-Profile</span></span>
<span data-ttu-id="b85e8-136">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="b85e8-136">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="b85e8-137">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="b85e8-137">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b85e8-138">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="b85e8-138">-SubscriptionId</span></span>
```yaml
Type: String
Parameter Sets: SelectSubscriptionByIdParameterSet, SelectDefaultSubscriptionByIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b85e8-139">-Abonnementname</span><span class="sxs-lookup"><span data-stu-id="b85e8-139">-SubscriptionName</span></span>
```yaml
Type: String
Parameter Sets: SelectSubscriptionByNameParameterSet, SelectDefaultSubscriptionByNameParameterSet
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b85e8-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b85e8-140">CommonParameters</span></span>
<span data-ttu-id="b85e8-141">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b85e8-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b85e8-142">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b85e8-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b85e8-143">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b85e8-143">INPUTS</span></span>

### <span data-ttu-id="b85e8-144">Keine</span><span class="sxs-lookup"><span data-stu-id="b85e8-144">None</span></span>
<span data-ttu-id="b85e8-145">Sie können die Eingabe an dieses Cmdlet nach Eigenschaftsname, aber nicht nach Wert übergeben.</span><span class="sxs-lookup"><span data-stu-id="b85e8-145">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="b85e8-146">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b85e8-146">OUTPUTS</span></span>

### <span data-ttu-id="b85e8-147">None oder System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b85e8-147">None or System.Boolean</span></span>
<span data-ttu-id="b85e8-148">Wenn Sie den Parameter *passthru* verwenden, gibt dieses Cmdlet einen booleschen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="b85e8-148">If you use the *PassThru* parameter, this cmdlet returns a Boolean value.</span></span>
<span data-ttu-id="b85e8-149">Standardmäßig wird keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="b85e8-149">By default, it does not generate any output.</span></span>

## <span data-ttu-id="b85e8-150">Notizen</span><span class="sxs-lookup"><span data-stu-id="b85e8-150">NOTES</span></span>

## <span data-ttu-id="b85e8-151">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b85e8-151">RELATED LINKS</span></span>

[<span data-ttu-id="b85e8-152">Get-AzureSubscription</span><span class="sxs-lookup"><span data-stu-id="b85e8-152">Get-AzureSubscription</span></span>](./Get-AzureSubscription.md)

[<span data-ttu-id="b85e8-153">Remove-AzureSubscription</span><span class="sxs-lookup"><span data-stu-id="b85e8-153">Remove-AzureSubscription</span></span>](./Remove-AzureSubscription.md)

[<span data-ttu-id="b85e8-154">Satz-AzureSubscription</span><span class="sxs-lookup"><span data-stu-id="b85e8-154">Set-AzureSubscription</span></span>](./Set-AzureSubscription.md)


