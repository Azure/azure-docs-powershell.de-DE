---
title: Verwenden experimenteller Azure PowerShell-Module
description: Grundlegendes zur Philosophie und Verwendung experimenteller Azure PowerShell-Module.
services: azure
author: sdwheeler
ms.author: sewhee
manager: carmonm
ms.product: azure
ms.service: azure-powershell
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/05/2017
ms.openlocfilehash: c11e4503c07b0a0c4a71021bc511da723098188e
ms.sourcegitcommit: 42bfd513fe646494d3d9eb0cfc35b049f7e1fbb7
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/19/2017
---
# <a name="using-experimental-azure-powershell-modules"></a><span data-ttu-id="ae06b-103">Verwenden experimenteller Azure PowerShell-Module</span><span class="sxs-lookup"><span data-stu-id="ae06b-103">Using experimental Azure PowerShell modules</span></span>

<span data-ttu-id="ae06b-104">Das Azure PowerShell-Team experimentiert mit zahlreichen Verbesserungen für Azure-PowerShell und konzentriert sich dabei auf Azure-Entwicklertools (insbesondere Befehlszeilenschnittstellen).</span><span class="sxs-lookup"><span data-stu-id="ae06b-104">With the emphasis on developer tools (especially CLIs) in Azure, the Azure PowerShell team is experimenting with many improvements to the Azure PowerShell experience.</span></span>

## <a name="experimentation-methodology"></a><span data-ttu-id="ae06b-105">Experimentiermethodik</span><span class="sxs-lookup"><span data-stu-id="ae06b-105">Experimentation methodology</span></span>

<span data-ttu-id="ae06b-106">Zur Vereinfachung der Experimente erstellen wir neue Azure PowerShell-Module, die vorhandene Azure SDK-Funktionen auf neue, benutzerfreundlichere Weise implementieren.</span><span class="sxs-lookup"><span data-stu-id="ae06b-106">To facilitate experimentation, we are creating new Azure PowerShell modules that implement existing Azure SDK functionality in new, easier to use ways.</span></span> <span data-ttu-id="ae06b-107">In den meisten Fällen sind die Cmdlets mit bereits vorhandenen Cmdlets identisch.</span><span class="sxs-lookup"><span data-stu-id="ae06b-107">In most cases, the cmdlets exactly mirror existing cmdlets.</span></span> <span data-ttu-id="ae06b-108">Die experimentellen Cmdlets bieten jedoch eine Kurzschreibweise und intelligentere Standardwerte, die die Erstellung und Verwaltung von Azure-Ressourcen erleichtern.</span><span class="sxs-lookup"><span data-stu-id="ae06b-108">However, the experimental cmdlets provide a shorthand notation and smarter default values that make it easier to create and manage Azure resources.</span></span>

<span data-ttu-id="ae06b-109">Diese Module können parallel zu bereits vorhandenen Azure PowerShell-Modulen installiert werden.</span><span class="sxs-lookup"><span data-stu-id="ae06b-109">These modules can be installed side-by-side with existing Azure PowerShell modules.</span></span> <span data-ttu-id="ae06b-110">Die Cmdlet-Namen wurden verkürzt, um die Angabe kürzerer Namen zu ermöglichen und Namenskonflikte mit bereits vorhandenen, nicht experimentellen Cmdlets zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="ae06b-110">The cmdlet names have been shortened to provide shorter names and avoid name conflicts with existing, non-experimental cmdlets.</span></span>

<span data-ttu-id="ae06b-111">Für die experimentellen Module wird folgende Benennungskonvention verwendet: `AzureRM.*.Experiments`.</span><span class="sxs-lookup"><span data-stu-id="ae06b-111">The experimental modules use the following naming convention: `AzureRM.*.Experiments`.</span></span> <span data-ttu-id="ae06b-112">Diese Benennungskonvention kommt so ähnlich auch bei der Benennung von Vorschaumodulen zur Anwendung: `AzureRM.*.Preview`.</span><span class="sxs-lookup"><span data-stu-id="ae06b-112">This naming convention is similar to the naming of Preview modules: `AzureRM.*.Preview`.</span></span> <span data-ttu-id="ae06b-113">Vorschaumodule unterscheiden sich von experimentellen Modulen.</span><span class="sxs-lookup"><span data-stu-id="ae06b-113">Preview modules differ from experimental modules.</span></span> <span data-ttu-id="ae06b-114">Vorschaumodule implementieren neue Funktionen von Azure-Diensten, die nur als Vorschauversion angeboten werden.</span><span class="sxs-lookup"><span data-stu-id="ae06b-114">Preview modules implement new functionality of Azure services that is only available as a Preview offering.</span></span> <span data-ttu-id="ae06b-115">Vorschaumodule ersetzen vorhandene Azure PowerShell-Module und verwenden die gleichen Cmdlet- und Parameternamen.</span><span class="sxs-lookup"><span data-stu-id="ae06b-115">Preview modules replace existing Azure PowerShell modules and use the same cmdlet and parameter names.</span></span>

## <a name="how-to-install-an-experimental-module"></a><span data-ttu-id="ae06b-116">Installieren eines experimentellen Moduls</span><span class="sxs-lookup"><span data-stu-id="ae06b-116">How to install an experimental module</span></span>

<span data-ttu-id="ae06b-117">Experimentelle Module werden genau wie vorhandene Azure PowerShell-Module im PowerShell-Katalog veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="ae06b-117">Experimental modules are published to the PowerShell Gallery just like the existing Azure PowerShell modules.</span></span> <span data-ttu-id="ae06b-118">Führen Sie zum Anzeigen einer Liste der experimentellen Module den folgenden Befehl aus:</span><span class="sxs-lookup"><span data-stu-id="ae06b-118">To see a list of experimental modules, run the following command:</span></span>

```powershell
Find-Module AzureRM.*.Experiments
```

```Output
Version Name                         Repository Description
------- ----                         ---------- -----------
1.0.25  AzureRM.Compute.Experiments  PSGallery  Azure Compute experiments for VM creation
1.0.0   AzureRM.Websites.Experiments PSGallery  Create and deploy web applications using Azure App Services.
```

<span data-ttu-id="ae06b-119">Verwenden Sie zum Installieren des experimentellen Moduls die folgenden Befehle in einer PowerShell-Sitzung mit erhöhten Rechten:</span><span class="sxs-lookup"><span data-stu-id="ae06b-119">To install the experimental module, use the following commands from an elevated PowerShell session:</span></span>

```powershell
Install-Module AzureRM.Compute.Experiments
Install-Module AzureRM.Websites.Experiments
```

### <a name="documentation-and-support"></a><span data-ttu-id="ae06b-120">Dokumentation und Support</span><span class="sxs-lookup"><span data-stu-id="ae06b-120">Documentation and support</span></span>

<span data-ttu-id="ae06b-121">Die Dokumentation ist im Installationspaket enthalten und kann über das Cmdlet `Get-Help` aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="ae06b-121">Documentation is included in the install package and is accessed using the `Get-Help` cmdlet.</span></span> <span data-ttu-id="ae06b-122">Für experimentelle Module wird keine offizielle Dokumentation veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="ae06b-122">No official documentation is published for experimental modules.</span></span>

<span data-ttu-id="ae06b-123">Wir ermutigen Sie dazu, diese Module zu testen.</span><span class="sxs-lookup"><span data-stu-id="ae06b-123">We encourage you to test these modules.</span></span> <span data-ttu-id="ae06b-124">Ihr Feedback hilft uns dabei, die Benutzerfreundlichkeit zu verbessern und noch besser auf Ihre Anforderungen einzugehen.</span><span class="sxs-lookup"><span data-stu-id="ae06b-124">Your feedback allows us to improve usability and respond to your needs.</span></span> <span data-ttu-id="ae06b-125">Da es sich hierbei jedoch um experimentelle Modul handelt, ist der Support dafür eingeschränkt.</span><span class="sxs-lookup"><span data-stu-id="ae06b-125">However, being experimental, support for these modules is limited.</span></span> <span data-ttu-id="ae06b-126">Fragen oder Problemberichte können durch Erstellen eines [Problems](https://github.com/Azure/azure-powershell/issues) im GitHub-Repository übermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="ae06b-126">Questions or problem reports can be submitted by creating an [issue](https://github.com/Azure/azure-powershell/issues) in the GitHub repository.</span></span>

## <a name="experiments-and-areas-of-improvement"></a><span data-ttu-id="ae06b-127">Experimente und Verbesserungsbereiche</span><span class="sxs-lookup"><span data-stu-id="ae06b-127">Experiments and areas of improvement</span></span>

<span data-ttu-id="ae06b-128">Diese Verbesserungen wurden auf der Grundlage wichtiger Alleinstellungsmerkmale in Konkurrenzprodukten ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="ae06b-128">These improvements were selected based on key differentiators in competing products.</span></span> <span data-ttu-id="ae06b-129">Bei der Azure CLI 2.0 basieren Befehle beispielsweise ganz bewusst auf _Szenarien_ und nicht auf der _API-Oberfläche_.</span><span class="sxs-lookup"><span data-stu-id="ae06b-129">For example, Azure CLI 2.0 has made a point of basing commands on _scenarios_ rather than _API surface area_.</span></span>
<span data-ttu-id="ae06b-130">Die Azure CLI 2.0 verwendet einige intelligente Standardwerte, die Endbenutzern den Einstieg erleichtern.</span><span class="sxs-lookup"><span data-stu-id="ae06b-130">Azure CLI 2.0 use a number of smart defaults that make "getting started" scenarios easier for end users.</span></span>

### <a name="core-improvements"></a><span data-ttu-id="ae06b-131">Zentrale Verbesserungen</span><span class="sxs-lookup"><span data-stu-id="ae06b-131">Core improvements</span></span>

<span data-ttu-id="ae06b-132">Die zentralen Verbesserungen gelten als naheliegend, und zur Implementierung dieser Updates sind nicht viele Experimente erforderlich.</span><span class="sxs-lookup"><span data-stu-id="ae06b-132">The core improvements are regarded as "common sense", and little experimentation is needed to move forward in implementing these updates.</span></span>

- <span data-ttu-id="ae06b-133">Szenariobasierte Cmdlets: *Alle* Cmdlets sollten für Szenarien und nicht für den Azure REST-Dienst entwickelt werden.</span><span class="sxs-lookup"><span data-stu-id="ae06b-133">Scenario-based Cmdlets - \**All*- cmdlets should be designed around scenarios, not the Azure REST service.</span></span>

- <span data-ttu-id="ae06b-134">Kürzere Namen: Gilt für die Namen von Cmdlets (beispielsweise `New-AzureRmVM` => `New-AzVm`) und Parametern (beispielsweise `-ResourceGroupName` => `-Rg`).</span><span class="sxs-lookup"><span data-stu-id="ae06b-134">Shorter Names - Includes the names of cmdlets (for example, `New-AzureRmVM` => `New-AzVm`) and the names of parameters (for example, `-ResourceGroupName` => `-Rg`).</span></span> <span data-ttu-id="ae06b-135">Verwenden Sie Aliase, um die Kompatibilität mit älteren Cmdlets zu gewährleisten.</span><span class="sxs-lookup"><span data-stu-id="ae06b-135">Use aliases for compatibility with "old" cmdlets.</span></span> <span data-ttu-id="ae06b-136">Geben Sie _abwärtskompatible_ Parametersätze an.</span><span class="sxs-lookup"><span data-stu-id="ae06b-136">Provide _backwards compatible_ parameter sets.</span></span>

- <span data-ttu-id="ae06b-137">Intelligente Standardwerte: Erstellen Sie intelligente Standardwerte zum Ausfüllen erforderlicher Informationen.</span><span class="sxs-lookup"><span data-stu-id="ae06b-137">Smart Defaults - Create smart defaults to fill in "required" information.</span></span> <span data-ttu-id="ae06b-138">Beispiel: </span><span class="sxs-lookup"><span data-stu-id="ae06b-138">For example:</span></span>
  - <span data-ttu-id="ae06b-139">Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="ae06b-139">Resource Group</span></span>
  - <span data-ttu-id="ae06b-140">Speicherort</span><span class="sxs-lookup"><span data-stu-id="ae06b-140">Location</span></span>
  - <span data-ttu-id="ae06b-141">Abhängige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="ae06b-141">Dependent resources</span></span>

### <a name="experimental-improvements"></a><span data-ttu-id="ae06b-142">Experimentelle Verbesserungen</span><span class="sxs-lookup"><span data-stu-id="ae06b-142">Experimental improvements</span></span>

<span data-ttu-id="ae06b-143">Die experimentellen Verbesserungen stellen eine wesentliche Änderung dar, die das Team im Rahmen von Experimenten überprüfen möchte.</span><span class="sxs-lookup"><span data-stu-id="ae06b-143">The experimental improvements present a significant change that the team wants to validate via experimentation.</span></span>

- <span data-ttu-id="ae06b-144">Einfache Typen: Erstellungsszenarien sollten weniger komplexe Typen und Konfigurationsobjekte verwenden.</span><span class="sxs-lookup"><span data-stu-id="ae06b-144">Simple types - Create scenarios should move away from complex types and config objects.</span></span> <span data-ttu-id="ae06b-145">Vereinfachen Sie die Konfiguration auf maximal zwei Parameter.</span><span class="sxs-lookup"><span data-stu-id="ae06b-145">Simplify the configuration down to one or two parameters.</span></span>

- <span data-ttu-id="ae06b-146">Intelligente Erstellung: In Erstellungsszenarien mit intelligenter Erstellung gibt es _keine_ erforderlichen Parameter. Alle benötigten Informationen werden automatisch von Azure PowerShell ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="ae06b-146">"Smart Create" - All create scenarios implementing "Smart Create" would have _no_ required parameters: all necessary information would be chosen by Azure PowerShell in an opinionated fashion.</span></span>

- <span data-ttu-id="ae06b-147">„Graue“ Parameter: In vielen Fällen sind einige Parameter unter Umständen „grau“ oder nicht wirklich optimal.</span><span class="sxs-lookup"><span data-stu-id="ae06b-147">Gray Parameters - In many cases, some parameters could be "gray" or semi-optional.</span></span> <span data-ttu-id="ae06b-148">Wurde der Parameter nicht angegeben, wird der Benutzer gefragt, ob der Parameter automatisch generiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="ae06b-148">If the parameter is not specified, the user is asked if they want the parameter generated for them.</span></span> <span data-ttu-id="ae06b-149">Bei grauen Parametern ist es auch sinnvoll, einen Wert mit Zustimmung des Benutzers vom Kontext abzuleiten.</span><span class="sxs-lookup"><span data-stu-id="ae06b-149">It also makes sense for gray parameters to infer a value based on context with the user's consent.</span></span>
  <span data-ttu-id="ae06b-150">So kann es beispielsweise sinnvoll sein, wenn der graue Parameter den zuletzt verwendeten Wert vorschlägt.</span><span class="sxs-lookup"><span data-stu-id="ae06b-150">For example, it may make sense to have the gray parameter suggest the most recently used value.</span></span>

- <span data-ttu-id="ae06b-151">Schalter `-Auto`: Mit dem Schalter `-Auto` können Benutzer entscheiden, ob sie _für alles Standardwerte verwenden_ und dabei gleichzeitig die Integrität der erforderlichen Parameter im Hauptpfad bewahren möchten.</span><span class="sxs-lookup"><span data-stu-id="ae06b-151">`-Auto` Switch - The `-Auto` switch would provide an "opt-in" way for users to _default all the things_ while maintaining the integrity of required parameters in the mainline path.</span></span>

### <a name="feature-specific-switches"></a><span data-ttu-id="ae06b-152">Featurespezifische Schalter</span><span class="sxs-lookup"><span data-stu-id="ae06b-152">Feature-specific switches</span></span>

<span data-ttu-id="ae06b-153">Im Szenario „Web-App erstellen“ sind beispielsweise Schalter wie `-Git` oder `-AddRemote` denkbar, durch die einem vorhandenen Git-Repository automatisch eine Azure-Remotefunktion hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="ae06b-153">For example, the "Create web app" scenario might have a `-Git` or `-AddRemote` switch that would automatically add an "azure" remote to an existing git repository.</span></span>

- <span data-ttu-id="ae06b-154">Festlegbare Standardwerte: Benutzer sollten die Möglichkeit haben, bestimmte allgemeine Parameter wie `-ResourceGroupName` und `-Location` auf Standardwerte festzulegen.</span><span class="sxs-lookup"><span data-stu-id="ae06b-154">Settable Defaults - Users should have the ability to default certain ubiquitous parameters like `-ResourceGroupName` and `-Location`.</span></span>

- <span data-ttu-id="ae06b-155">Standardgrößen: Ressourcengrößen können für Benutzer verwirrend sein, da viele Ressourcenanbieter unterschiedliche Namen verwenden (etwa „Standard\_DS1\_v2“ oder „S1“).</span><span class="sxs-lookup"><span data-stu-id="ae06b-155">Size Defaults - Resource "sizes" can be confusing to users since many Resource Providers use different names (for example, "Standard\_DS1\_v2" or "S1").</span></span> <span data-ttu-id="ae06b-156">Die meisten Benutzer machen sich jedoch eher Gedanken über die Kosten.</span><span class="sxs-lookup"><span data-stu-id="ae06b-156">However, most users care more about cost.</span></span> <span data-ttu-id="ae06b-157">Daher ist es sinnvoll, auf der Grundlage eines Preisplans universelle Größen zu definieren.</span><span class="sxs-lookup"><span data-stu-id="ae06b-157">Therefore, it makes sense to define "universal" sizes based on a pricing schedule.</span></span> <span data-ttu-id="ae06b-158">Benutzer können sich für eine bestimmte Größe entscheiden oder Azure PowerShell die Wahl der _besten Option_ für die Ressource und das Budget überlassen.</span><span class="sxs-lookup"><span data-stu-id="ae06b-158">Users can choose a specific size or let Azure PowerShell choose the _best option_ based on the resource the budget.</span></span>

- <span data-ttu-id="ae06b-159">Ausgabeformat: Azure PowerShell gibt derzeit `PSObject`-Objekte zurück und nur wenig über die Konsole aus.</span><span class="sxs-lookup"><span data-stu-id="ae06b-159">Output Format - Azure PowerShell currently returns `PSObject`s and there is little console output.</span></span> <span data-ttu-id="ae06b-160">Azure PowerShell muss dem Benutzer ggf. Informationen zu den verwendeten intelligenten Standardwerten anzeigen.</span><span class="sxs-lookup"><span data-stu-id="ae06b-160">Azure PowerShell may need to display some information to the user regarding the "smart defaults" used.</span></span>
