---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: 32BC6CE6-60EF-4A46-912B-8FE4FCCDF7CC
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2b91906a25d2f2d7c40f96ed07a4fd7463722023
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005743"
---
# <span data-ttu-id="25f5c-101">Get-AzureSubscription</span><span class="sxs-lookup"><span data-stu-id="25f5c-101">Get-AzureSubscription</span></span>

## <span data-ttu-id="25f5c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="25f5c-102">SYNOPSIS</span></span>
<span data-ttu-id="25f5c-103">Ruft Azure-Abonnements in Azure-Konto ab.</span><span class="sxs-lookup"><span data-stu-id="25f5c-103">Gets  Azure subscriptions in Azure account.</span></span>

## <span data-ttu-id="25f5c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="25f5c-104">SYNTAX</span></span>

### <span data-ttu-id="25f5c-105">ByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="25f5c-105">ByName (Default)</span></span>
```
Get-AzureSubscription [-SubscriptionName <String>] [-ExtendedDetails] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="25f5c-106">ById</span><span class="sxs-lookup"><span data-stu-id="25f5c-106">ById</span></span>
```
Get-AzureSubscription [-SubscriptionId <String>] [-ExtendedDetails] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="25f5c-107">Standard</span><span class="sxs-lookup"><span data-stu-id="25f5c-107">Default</span></span>
```
Get-AzureSubscription [-Default] [-ExtendedDetails] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="25f5c-108">Aktuellen</span><span class="sxs-lookup"><span data-stu-id="25f5c-108">Current</span></span>
```
Get-AzureSubscription [-Current] [-ExtendedDetails] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="25f5c-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="25f5c-109">DESCRIPTION</span></span>
<span data-ttu-id="25f5c-110">Das Cmdlet " **Get-AzureSubscription** " Ruft die Abonnements in Ihrem Azure-Konto ab.</span><span class="sxs-lookup"><span data-stu-id="25f5c-110">The **Get-AzureSubscription** cmdlet gets the subscriptions in your Azure account.</span></span>
<span data-ttu-id="25f5c-111">Sie können dieses Cmdlet verwenden, um Informationen zum Abonnement abzurufen und das Abonnement an andere Cmdlets zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="25f5c-111">You can use this cmdlet to get information about the subscription and to pipe the subscription to other cmdlets.</span></span>

<span data-ttu-id="25f5c-112">Für **Get-AzureSubscription** ist der Zugriff auf Ihre Azure-Konten erforderlich.</span><span class="sxs-lookup"><span data-stu-id="25f5c-112">**Get-AzureSubscription** requires access to your Azure accounts.</span></span>
<span data-ttu-id="25f5c-113">Bevor Sie **Get-AzureSubscription** ausführen, müssen Sie das **Add-AzureAccount-** Cmdlet oder die Cmdlets ausführen, die eine Datei für die Veröffentlichungseinstellungen herunterladen und installieren ( **Get-AzurePublishSettingsFile** , **Import-AzurePublishSettingsFile**.</span><span class="sxs-lookup"><span data-stu-id="25f5c-113">Before you run **Get-AzureSubscription** , you must run the **Add-AzureAccount** cmdlet or the cmdlets that download and install a publish settings file ( **Get-AzurePublishSettingsFile** , **Import-AzurePublishSettingsFile**.</span></span>

<span data-ttu-id="25f5c-114">In diesem Thema wird das Cmdlet in der 0.8.10-Version des Microsoft Azure PowerShell-Moduls beschrieben.</span><span class="sxs-lookup"><span data-stu-id="25f5c-114">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="25f5c-115">Wenn Sie die Version des verwendeten Moduls abrufen möchten, geben Sie in der Azure PowerShell-Konsole `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="25f5c-115">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

## <span data-ttu-id="25f5c-116">Beispiele</span><span class="sxs-lookup"><span data-stu-id="25f5c-116">EXAMPLES</span></span>

### <span data-ttu-id="25f5c-117">Beispiel 1: Abrufen aller Abonnements</span><span class="sxs-lookup"><span data-stu-id="25f5c-117">Example 1: Get all subscriptions</span></span>
```
C:\PS>Get-AzureSubscription
```

<span data-ttu-id="25f5c-118">Dieser Befehl ruft alle Abonnements im Konto ab.</span><span class="sxs-lookup"><span data-stu-id="25f5c-118">This command gets all subscriptions in the account.</span></span>

### <span data-ttu-id="25f5c-119">Beispiel 2: Abrufen eines Abonnements nach Name</span><span class="sxs-lookup"><span data-stu-id="25f5c-119">Example 2: Get a subscription by name</span></span>
```
C:\PS>Get-AzureSubscription -SubscriptionName "MyProdSubscription"
```

<span data-ttu-id="25f5c-120">Dieser Befehl ruft nur das "MyProdSubsciption"-Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="25f5c-120">This command gets only the "MyProdSubsciption" subscription.</span></span>

### <span data-ttu-id="25f5c-121">Beispiel 3: Abrufen des Standardabonnements</span><span class="sxs-lookup"><span data-stu-id="25f5c-121">Example 3: Get the default subscription</span></span>
```
C:\PS>(Get-AzureSubscription -Default).SubscriptionName
```

<span data-ttu-id="25f5c-122">Dieser Befehl ruft nur den Namen des Standardabonnements ab.</span><span class="sxs-lookup"><span data-stu-id="25f5c-122">This command gets only the name of the default subscription.</span></span>
<span data-ttu-id="25f5c-123">Der Befehl ruft zuerst das Abonnement ab und verwendet dann die dot-Methode, um die **subscriptionname** -Eigenschaft des Abonnements abzurufen.</span><span class="sxs-lookup"><span data-stu-id="25f5c-123">The command first gets the subscription and then uses the dot method to get the **SubscriptionName** property of the subscription.</span></span>

### <span data-ttu-id="25f5c-124">Beispiel 4: Abrufen ausgewählter Abonnementeigenschaften</span><span class="sxs-lookup"><span data-stu-id="25f5c-124">Example 4: Get selected subscription properties</span></span>
```
C:\PS>Get-AzureSubscription -Current | Format-List -Property SubscriptionName, Certificate
```

<span data-ttu-id="25f5c-125">Dieser Befehl gibt eine Liste mit dem Namen und dem Zertifikat des aktuellen Abonnements zurück.</span><span class="sxs-lookup"><span data-stu-id="25f5c-125">This command returns a list with the name and certificate of the current subscription.</span></span>
<span data-ttu-id="25f5c-126">Es wird ein Befehl " **Get-AzureSubscription** " verwendet, um das aktuelle Abonnement abzurufen.</span><span class="sxs-lookup"><span data-stu-id="25f5c-126">It uses a **Get-AzureSubscription** command to get the current subscription.</span></span>
<span data-ttu-id="25f5c-127">Anschließend wird das Abonnement an einen Befehl **Format-List** Weiterleitung, in dem die ausgewählten Eigenschaften in einer Liste angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="25f5c-127">Then it pipes the subscription to a **Format-List** command that displays the selected properties in a list.</span></span>

### <span data-ttu-id="25f5c-128">Beispiel 5: Verwenden einer alternativen Abonnement Datendatei</span><span class="sxs-lookup"><span data-stu-id="25f5c-128">Example 5: Use an alternate subscription data file</span></span>
```
C:\PS>Get-AzureSubscription -SubscriptionDataFile "C:\Temp\MySubscriptions.xml"
```

<span data-ttu-id="25f5c-129">Dieser Befehl ruft Abonnements aus der Datendatei des C:\Temp\MySubscriptions.xml-Abonnements ab.</span><span class="sxs-lookup"><span data-stu-id="25f5c-129">This command gets subscriptions from  the C:\Temp\MySubscriptions.xml subscription data file.</span></span>
<span data-ttu-id="25f5c-130">Verwenden Sie den **SubscriptionDataFile** -Parameter, wenn Sie beim Ausführen der Cmdlets **Add-AzureAccount** oder **Import-PublishSettingsFile** eine Alternative Abonnementdaten Datei angegeben haben.</span><span class="sxs-lookup"><span data-stu-id="25f5c-130">Use the **SubscriptionDataFile** parameter if you specified an alternate subscription data file when you ran the **Add-AzureAccount** or **Import-PublishSettingsFile** cmdlets.</span></span>

## <span data-ttu-id="25f5c-131">Parameter</span><span class="sxs-lookup"><span data-stu-id="25f5c-131">PARAMETERS</span></span>

### <span data-ttu-id="25f5c-132">-Current</span><span class="sxs-lookup"><span data-stu-id="25f5c-132">-Current</span></span>
<span data-ttu-id="25f5c-133">Ruft nur das aktuelle Abonnement ab, also das Abonnement, das als "aktuell" festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="25f5c-133">Gets only the current subscription, that is, the subscription designated as "current."</span></span> <span data-ttu-id="25f5c-134">Standardmäßig ruft **Get-AzureSubscription** alle Abonnements in ihren Azure-Konten ab.</span><span class="sxs-lookup"><span data-stu-id="25f5c-134">By default, **Get-AzureSubscription** gets all subscriptions in your Azure accounts.</span></span>
<span data-ttu-id="25f5c-135">Wenn Sie ein Abonnement als "aktuell" festlegen möchten, verwenden Sie den **aktuellen** Parameter des Cmdlets **Select-AzureSubscription** .</span><span class="sxs-lookup"><span data-stu-id="25f5c-135">To designate a subscription as "current," use the **Current** parameter of the **Select-AzureSubscription** cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Current
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25f5c-136">– Standard</span><span class="sxs-lookup"><span data-stu-id="25f5c-136">-Default</span></span>
<span data-ttu-id="25f5c-137">Ruft nur das Standardabonnement ab, also das Abonnement, das als "Standard" festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="25f5c-137">Gets only the default subscription, that is, the subscription designated as "default."</span></span> <span data-ttu-id="25f5c-138">Standardmäßig ruft **Get-AzureSubscription** alle Abonnements in ihren Azure-Konten ab.</span><span class="sxs-lookup"><span data-stu-id="25f5c-138">By default, **Get-AzureSubscription** gets all subscriptions in your Azure accounts.</span></span>
<span data-ttu-id="25f5c-139">Wenn Sie ein Abonnement als "Standard" festlegen möchten, verwenden Sie den **Standard** Parameter des Cmdlets **Select-AzureSubscription** .</span><span class="sxs-lookup"><span data-stu-id="25f5c-139">To designate a subscription as "default," use the **Default** parameter of the **Select-AzureSubscription** cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Default
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25f5c-140">-ExtendedDetails</span><span class="sxs-lookup"><span data-stu-id="25f5c-140">-ExtendedDetails</span></span>
<span data-ttu-id="25f5c-141">Gibt Kontingentinformationen für das Abonnement zusätzlich zu den Standardeinstellungen zurück.</span><span class="sxs-lookup"><span data-stu-id="25f5c-141">Returns quota information for the subscription, in addition to the standard settings.</span></span>

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

### <span data-ttu-id="25f5c-142">-Profil</span><span class="sxs-lookup"><span data-stu-id="25f5c-142">-Profile</span></span>
<span data-ttu-id="25f5c-143">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="25f5c-143">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="25f5c-144">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="25f5c-144">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="25f5c-145">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="25f5c-145">-SubscriptionId</span></span>
```yaml
Type: String
Parameter Sets: ById
Aliases: Id

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25f5c-146">-Abonnementname</span><span class="sxs-lookup"><span data-stu-id="25f5c-146">-SubscriptionName</span></span>
<span data-ttu-id="25f5c-147">Ruft nur das angegebene Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="25f5c-147">Gets only the specified subscription.</span></span>
<span data-ttu-id="25f5c-148">Geben Sie den Namen des Abonnements ein.</span><span class="sxs-lookup"><span data-stu-id="25f5c-148">Enter the subscription name.</span></span>
<span data-ttu-id="25f5c-149">Bei dem Wert wird die Groß-/Kleinschreibung beachtet.</span><span class="sxs-lookup"><span data-stu-id="25f5c-149">The value is case-sensitive.</span></span>
<span data-ttu-id="25f5c-150">Platzhalterzeichen werden nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="25f5c-150">Wildcard characters are not supported.</span></span>
<span data-ttu-id="25f5c-151">Standardmäßig ruft **Get-AzureSubscription** alle Abonnements in ihren Azure-Konten ab.</span><span class="sxs-lookup"><span data-stu-id="25f5c-151">By default, **Get-AzureSubscription** gets all subscriptions in your Azure accounts.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: Name

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25f5c-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25f5c-152">CommonParameters</span></span>
<span data-ttu-id="25f5c-153">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25f5c-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25f5c-154">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="25f5c-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25f5c-155">Eingaben</span><span class="sxs-lookup"><span data-stu-id="25f5c-155">INPUTS</span></span>

### <span data-ttu-id="25f5c-156">Keine</span><span class="sxs-lookup"><span data-stu-id="25f5c-156">None</span></span>
<span data-ttu-id="25f5c-157">Sie können die Eingabe an die **subscriptionname** -Eigenschaft nach Name, aber nicht nach Wert überleiten.</span><span class="sxs-lookup"><span data-stu-id="25f5c-157">You can pipe input to the **SubscriptionName** property by name, but not by value.</span></span>

## <span data-ttu-id="25f5c-158">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="25f5c-158">OUTPUTS</span></span>

### <span data-ttu-id="25f5c-159">Microsoft. WindowsAzure. Commands. Utilities. Common. WindowsAzureSubscription</span><span class="sxs-lookup"><span data-stu-id="25f5c-159">Microsoft.WindowsAzure.Commands.Utilities.Common.WindowsAzureSubscription</span></span>

## <span data-ttu-id="25f5c-160">Notizen</span><span class="sxs-lookup"><span data-stu-id="25f5c-160">NOTES</span></span>
* <span data-ttu-id="25f5c-161">Get-AzureSubscription ruft Daten aus der Abonnement Datendatei ab, die von den Cmdlets **Add-AzureAccount** und **Import-PublishSettingsFile** erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="25f5c-161">Get-AzureSubscription gets data from the subscription data file that the **Add-AzureAccount** and **Import-PublishSettingsFile** cmdlets create.</span></span>

## <span data-ttu-id="25f5c-162">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="25f5c-162">RELATED LINKS</span></span>

[<span data-ttu-id="25f5c-163">Add-AzureAccount</span><span class="sxs-lookup"><span data-stu-id="25f5c-163">Add-AzureAccount</span></span>](./Add-AzureAccount.md)

[<span data-ttu-id="25f5c-164">Get-AzurePublishSettingsFile</span><span class="sxs-lookup"><span data-stu-id="25f5c-164">Get-AzurePublishSettingsFile</span></span>](./Get-AzurePublishSettingsFile.md)

[<span data-ttu-id="25f5c-165">Importieren-AzurePublishSettingsFile</span><span class="sxs-lookup"><span data-stu-id="25f5c-165">Import-AzurePublishSettingsFile</span></span>](./Import-AzurePublishSettingsFile.md)

[<span data-ttu-id="25f5c-166">Remove-AzureSubscription</span><span class="sxs-lookup"><span data-stu-id="25f5c-166">Remove-AzureSubscription</span></span>](./Remove-AzureSubscription.md)

[<span data-ttu-id="25f5c-167">Satz-AzureSubscription</span><span class="sxs-lookup"><span data-stu-id="25f5c-167">Set-AzureSubscription</span></span>](./Set-AzureSubscription.md)


