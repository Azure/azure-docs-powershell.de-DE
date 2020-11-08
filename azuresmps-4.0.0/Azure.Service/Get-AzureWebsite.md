---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: E4B1AA31-1185-4035-86E6-2BB2587285C6
online version: ''
schema: 2.0.0
ms.openlocfilehash: a8273613081ab6bab0c9c3481df90f5b680b3355
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006480"
---
# <span data-ttu-id="1c9ec-101">Get-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="1c9ec-101">Get-AzureWebsite</span></span>

## <span data-ttu-id="1c9ec-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1c9ec-102">SYNOPSIS</span></span>
<span data-ttu-id="1c9ec-103">Ruft Azure-Websites im aktuellen Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="1c9ec-103">Gets Azure websites in the current subscription.</span></span>

## <span data-ttu-id="1c9ec-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1c9ec-104">SYNTAX</span></span>

```
Get-AzureWebsite [-Name <String>] [-Slot <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="1c9ec-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1c9ec-105">DESCRIPTION</span></span>
<span data-ttu-id="1c9ec-106">Das Cmdlet " **Get-AzureWebsite** " Ruft Informationen zu Azure-Websites im aktuellen Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="1c9ec-106">The **Get-AzureWebsite** cmdlet gets information about Azure websites in the current subscription.</span></span>

<span data-ttu-id="1c9ec-107">Standardmäßig ruft **Get-AzureWebsite** alle Azure-Websites im aktuellen Abonnement ab und gibt ein Objekt zurück, das grundlegende Informationen zu den Websites bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="1c9ec-107">By default, **Get-AzureWebsite** gets all Azure websites in the current subscription and returns an object that provides basic information about the sites.</span></span>
<span data-ttu-id="1c9ec-108">Wenn Sie den Parameter *Name* verwenden, gibt **Get-AzureWebsite** ein Objekt mit umfangreichen Informationen zurück, einschließlich Konfigurationsdetails.</span><span class="sxs-lookup"><span data-stu-id="1c9ec-108">When you use the *Name* parameter, **Get-AzureWebsite** returns an object with extensive information, including configuration details.</span></span>

<span data-ttu-id="1c9ec-109">Das aktuelle Abonnement ist das Abonnement, das als "aktuell" festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="1c9ec-109">The current subscription is the subscription that is designated as "current."</span></span> <span data-ttu-id="1c9ec-110">Um das aktuelle Abonnement zu finden, verwenden Sie den *aktuellen* Parameter des Cmdlets [Get-AzureSubscription](https://go.microsoft.com/fwlink/?LinkID=397623) .</span><span class="sxs-lookup"><span data-stu-id="1c9ec-110">To find the current subscription, use the *Current* parameter of the [Get-AzureSubscription](https://go.microsoft.com/fwlink/?LinkID=397623) cmdlet.</span></span>
<span data-ttu-id="1c9ec-111">Wenn Sie das aktuelle Abonnement ändern möchten, verwenden Sie das Cmdlet [Select-AzureSubscription](https://go.microsoft.com/fwlink/?LinkID=397628) .</span><span class="sxs-lookup"><span data-stu-id="1c9ec-111">To change the current subscription, use the [Select-AzureSubscription](https://go.microsoft.com/fwlink/?LinkID=397628) cmdlet.</span></span>

<span data-ttu-id="1c9ec-112">In diesem Thema wird das Cmdlet in der 0.8.10-Version des Microsoft Azure PowerShell-Moduls beschrieben.</span><span class="sxs-lookup"><span data-stu-id="1c9ec-112">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="1c9ec-113">Wenn Sie die Version des verwendeten Moduls abrufen möchten, geben Sie in der Azure PowerShell-Konsole `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="1c9ec-113">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

## <span data-ttu-id="1c9ec-114">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1c9ec-114">EXAMPLES</span></span>

### <span data-ttu-id="1c9ec-115">Beispiel 1: Abrufen aller Websites im Abonnement</span><span class="sxs-lookup"><span data-stu-id="1c9ec-115">Example 1: Get all websites in the subscription</span></span>
```
PS C:\> Get-AzureWebsite
```

<span data-ttu-id="1c9ec-116">Dieser Befehl ruft alle Azure-Websites im aktuellen Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="1c9ec-116">This command gets all Azure websites in the current subscription.</span></span>

### <span data-ttu-id="1c9ec-117">Beispiel 2: Abrufen einer Website nach Namen</span><span class="sxs-lookup"><span data-stu-id="1c9ec-117">Example 2: Get a website by name</span></span>
```
PS C:\> Get-AzureWebsite -Name ContosoWeb
```

<span data-ttu-id="1c9ec-118">Dieser Befehl Ruft detaillierte Informationen zur ContosoWeb Azure-Website einschließlich Konfigurationsinformationen ab.</span><span class="sxs-lookup"><span data-stu-id="1c9ec-118">This command gets detailed information about the ContosoWeb Azure website, including configuration information.</span></span>
<span data-ttu-id="1c9ec-119">Wenn Sie den Parameter *Name* verwenden, gibt **Get-AzureWebsite** ein **SiteWithConfig** -Objekt mit erweiterten Informationen zur Website zurück.</span><span class="sxs-lookup"><span data-stu-id="1c9ec-119">When you use the *Name* parameter, **Get-AzureWebsite** returns a **SiteWithConfig** object with extended information about the website.</span></span>

### <span data-ttu-id="1c9ec-120">Beispiel 3: Abrufen detaillierter Informationen zu allen Websites</span><span class="sxs-lookup"><span data-stu-id="1c9ec-120">Example 3: Get detailed information about all websites</span></span>
```
PS C:\> Get-AzureWebsite | ForEach-Object {Get-AzureWebsite -Name $_.Name}
```

<span data-ttu-id="1c9ec-121">Dieser Befehl Ruft detaillierte Informationen zu allen Websites des Abonnements ab.</span><span class="sxs-lookup"><span data-stu-id="1c9ec-121">This command gets detailed information about all websites in the subscription.</span></span>
<span data-ttu-id="1c9ec-122">Sie verwendet einen Befehl " **Get-AzureWebsite** ", um alle Websites abzurufen, und verwendet dann das **ForEach-Object-** Cmdlet, um jede Website nach Namen abzurufen.</span><span class="sxs-lookup"><span data-stu-id="1c9ec-122">It uses a **Get-AzureWebsite** command to get all websites and then uses the **ForEach-Object** cmdlet to get each website by name.</span></span>

### <span data-ttu-id="1c9ec-123">Beispiel 4: Abrufen von Informationen zu einem Bereitstellungs Steckplatz</span><span class="sxs-lookup"><span data-stu-id="1c9ec-123">Example 4: Get information about a deployment slot</span></span>
```
PS C:\> Get-AzureWebsite -Name ContosoWeb -Slot Staging
```

<span data-ttu-id="1c9ec-124">Dieser Befehl ruft den Staging-Bereitstellungs Steckplatz der ContosoWeb-Website ab.</span><span class="sxs-lookup"><span data-stu-id="1c9ec-124">This command gets the Staging deployment slot of the ContosoWeb website.</span></span>
<span data-ttu-id="1c9ec-125">Mit Bereitstellungs Steckplätzen können Sie verschiedene Versionen ihrer Azure-Website testen, ohne Sie für die Öffentlichkeit freizugeben.</span><span class="sxs-lookup"><span data-stu-id="1c9ec-125">Deployment slots let you test different versions of your Azure website without releasing them to the public.</span></span>

### <span data-ttu-id="1c9ec-126">Beispiel 5: Abrufen von Website Instanzen</span><span class="sxs-lookup"><span data-stu-id="1c9ec-126">Example 5: Get website instances</span></span>
```
PS C:\>(Get-AzureWebsite -Name ContosoWeb).Instances

InstanceId
----------
2d8e712fb8f85d061c30fd793a534e6700a175f9a9ab12ca55cb3b0edfcc10ee
5834916b8cef49249b18187708223a33fbbc4352d33b48369f3166644bdd3445

PS C:\>(Get-AzureWebsite -Name ContosoWeb).Instances.Count
2
```

<span data-ttu-id="1c9ec-127">In den Befehlen in diesem Beispiel wird die Instances-Eigenschaft einer Azure-Website verwendet, um Informationen zu aktuell ausgeführten Website Instanzen abzurufen.</span><span class="sxs-lookup"><span data-stu-id="1c9ec-127">The commands in this example use the Instances property of an Azure website to get information about currently running website instances.</span></span>
<span data-ttu-id="1c9ec-128">Die **Instances** -Eigenschaft wurde dem **SiteWithConfig** -Objekt in Version 0.8.3 des Azure-Moduls hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="1c9ec-128">The **Instances** property was added to the **SiteWithConfig** object in version 0.8.3 of the Azure module.</span></span>

<span data-ttu-id="1c9ec-129">Der erste Befehl ruft die Instanz-IDs aller derzeit ausgeführten Instanzen einer Website ab.</span><span class="sxs-lookup"><span data-stu-id="1c9ec-129">The first command gets the instance IDs of all currently running instances of a website.</span></span>
<span data-ttu-id="1c9ec-130">Mit dem zweiten Befehl wird die Anzahl der ausgeführten Instanzen der Website abgerufen.</span><span class="sxs-lookup"><span data-stu-id="1c9ec-130">The second command gets the number of running instances of the website.</span></span>
<span data-ttu-id="1c9ec-131">Sie können die **count** -Eigenschaft für ein beliebiges Array verwenden.</span><span class="sxs-lookup"><span data-stu-id="1c9ec-131">You can use the **Count** property on any array.</span></span>

## <span data-ttu-id="1c9ec-132">Parameter</span><span class="sxs-lookup"><span data-stu-id="1c9ec-132">PARAMETERS</span></span>

### <span data-ttu-id="1c9ec-133">-Name</span><span class="sxs-lookup"><span data-stu-id="1c9ec-133">-Name</span></span>
<span data-ttu-id="1c9ec-134">Ruft detaillierte Konfigurationsinformationen zur angegebenen Website ab.</span><span class="sxs-lookup"><span data-stu-id="1c9ec-134">Gets detailed configuration information about the specified website.</span></span>
<span data-ttu-id="1c9ec-135">Geben Sie den Namen einer Website im Abonnement ein.</span><span class="sxs-lookup"><span data-stu-id="1c9ec-135">Enter the name of one website in the subscription.</span></span>
<span data-ttu-id="1c9ec-136">Standardmäßig ruft **Get-AzureWebsite** alle Websites im aktuellen Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="1c9ec-136">By default, **Get-AzureWebsite** gets all websites in the current subscription.</span></span>
<span data-ttu-id="1c9ec-137">Der *Name* -Wert unterstützt keine Platzhalterzeichen.</span><span class="sxs-lookup"><span data-stu-id="1c9ec-137">The *Name* value does not support wildcard characters.</span></span>

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

### <span data-ttu-id="1c9ec-138">-Profil</span><span class="sxs-lookup"><span data-stu-id="1c9ec-138">-Profile</span></span>
<span data-ttu-id="1c9ec-139">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="1c9ec-139">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="1c9ec-140">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="1c9ec-140">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="1c9ec-141">-Slot</span><span class="sxs-lookup"><span data-stu-id="1c9ec-141">-Slot</span></span>
<span data-ttu-id="1c9ec-142">Ruft den angegebenen Bereitstellungs Steckplatz der Website ab.</span><span class="sxs-lookup"><span data-stu-id="1c9ec-142">Gets the specified deployment slot of the website.</span></span>
<span data-ttu-id="1c9ec-143">Geben Sie den Namen des Steckplatzes ein, beispielsweise "Staging" oder "Production".</span><span class="sxs-lookup"><span data-stu-id="1c9ec-143">Enter the slot name, such as "Staging" or "Production".</span></span>
<span data-ttu-id="1c9ec-144">Weitere Informationen zu Bereitstellungs Steckplätzen finden Sie unter Bereitstellung auf Microsoft Azure-Websites https://azure.microsoft.com/en-us/documentation/articles/web-sites-staged-publishing/ .</span><span class="sxs-lookup"><span data-stu-id="1c9ec-144">For more information about deployment slots, see Staged Deployment on Microsoft Azure Web Siteshttps://azure.microsoft.com/en-us/documentation/articles/web-sites-staged-publishing/.</span></span>
<span data-ttu-id="1c9ec-145">Verwenden Sie das Cmdlet Set-AzureWebsite, um einen Bereitstellungs Steckplatz zu einer vorhandenen Azure-Website hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="1c9ec-145">To add a deployment slot to an existing Azure website, use the Set-AzureWebsite cmdlet.</span></span>

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

### <span data-ttu-id="1c9ec-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c9ec-146">CommonParameters</span></span>
<span data-ttu-id="1c9ec-147">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c9ec-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c9ec-148">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1c9ec-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c9ec-149">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1c9ec-149">INPUTS</span></span>

### <span data-ttu-id="1c9ec-150">Keine</span><span class="sxs-lookup"><span data-stu-id="1c9ec-150">None</span></span>
<span data-ttu-id="1c9ec-151">Sie können die Eingabe an dieses Cmdlet nach Eigenschaftsname, aber nicht nach Wert übergeben.</span><span class="sxs-lookup"><span data-stu-id="1c9ec-151">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="1c9ec-152">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1c9ec-152">OUTPUTS</span></span>

### <span data-ttu-id="1c9ec-153">Microsoft. WindowsAzure. Commands. Utilities. Websites. Services. webentities. Website</span><span class="sxs-lookup"><span data-stu-id="1c9ec-153">Microsoft.WindowsAzure.Commands.Utilities.Websites.Services.WebEntities.Site</span></span>
<span data-ttu-id="1c9ec-154">Standardmäßig gibt **Get-AzureWebsite** ein Array von **Website** Objekten zurück.</span><span class="sxs-lookup"><span data-stu-id="1c9ec-154">By default, **Get-AzureWebsite** returns an array of **Site** objects.</span></span>

### <span data-ttu-id="1c9ec-155">Microsoft. WindowsAzure. Commands. Utilities. Websites. Services. webentities. SiteWithConfig</span><span class="sxs-lookup"><span data-stu-id="1c9ec-155">Microsoft.WindowsAzure.Commands.Utilities.Websites.Services.WebEntities.SiteWithConfig</span></span>
<span data-ttu-id="1c9ec-156">Wenn Sie den Parameter *Name* verwenden, gibt **Get-AzureWebsite** ein **SiteWithConfig** -Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="1c9ec-156">When you use the *Name* parameter, **Get-AzureWebsite** returns a **SiteWithConfig** object.</span></span>

## <span data-ttu-id="1c9ec-157">Notizen</span><span class="sxs-lookup"><span data-stu-id="1c9ec-157">NOTES</span></span>

## <span data-ttu-id="1c9ec-158">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1c9ec-158">RELATED LINKS</span></span>

[<span data-ttu-id="1c9ec-159">Neu – AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="1c9ec-159">New-AzureWebsite</span></span>](./New-AzureWebsite.md)

[<span data-ttu-id="1c9ec-160">Remove-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="1c9ec-160">Remove-AzureWebsite</span></span>](./Remove-AzureWebsite.md)

[<span data-ttu-id="1c9ec-161">Anfang-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="1c9ec-161">Start-AzureWebsite</span></span>](./Start-AzureWebsite.md)

[<span data-ttu-id="1c9ec-162">Stopp-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="1c9ec-162">Stop-AzureWebsite</span></span>](./Stop-AzureWebsite.md)

[<span data-ttu-id="1c9ec-163">Anzeigen-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="1c9ec-163">Show-AzureWebsite</span></span>](./Show-AzureWebsite.md)


