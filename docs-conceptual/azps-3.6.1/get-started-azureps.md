---
title: Erste Schritte mit Azure PowerShell
description: ''
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: get-started-article
ms.date: 01/17/2020
ms.openlocfilehash: 718f0dc0f1ef9b0c2aa3d0630ca099fa5cec7ec0
ms.sourcegitcommit: f6fa6543be1e0f6330b1598f01528b2928cc426c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/10/2020
ms.locfileid: "79035871"
---
# <a name="get-started-with-azure-powershell"></a><span data-ttu-id="884c8-102">Erste Schritte mit Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="884c8-102">Get started with Azure PowerShell</span></span>

<span data-ttu-id="884c8-103">Azure PowerShell ist für die Verwaltung von Azure-Ressourcen über die Befehlszeile optimiert.</span><span class="sxs-lookup"><span data-stu-id="884c8-103">Azure PowerShell is designed for managing and administering Azure resources from the command line.</span></span> <span data-ttu-id="884c8-104">Verwenden Sie Azure PowerShell, wenn Sie automatisierte Tools erstellen möchten, die das Azure Resource Manager-Modell nutzen.</span><span class="sxs-lookup"><span data-stu-id="884c8-104">Use Azure PowerShell when you want to build automated tools that use the Azure Resource Manager model.</span></span>
<span data-ttu-id="884c8-105">Sie können Azure PowerShell mit [Azure Cloud Shell](/azure/cloud-shell/overview) in Ihrem Browser verwenden oder auf dem lokalen Computer installieren.</span><span class="sxs-lookup"><span data-stu-id="884c8-105">Try it out in your browser with [Azure Cloud Shell](/azure/cloud-shell/overview), or install on your local machine.</span></span>

<span data-ttu-id="884c8-106">Dieser Artikel unterstützt Sie bei den ersten Schritten mit Azure PowerShell und enthält Informationen zu den wichtigsten Konzepten.</span><span class="sxs-lookup"><span data-stu-id="884c8-106">This article helps you get started with Azure PowerShell and teaches the core concepts behind it.</span></span>

## <a name="install-or-run-in-azure-cloud-shell"></a><span data-ttu-id="884c8-107">Installieren oder Ausführen in Azure Cloud Shell</span><span class="sxs-lookup"><span data-stu-id="884c8-107">Install or run in Azure Cloud Shell</span></span>

<span data-ttu-id="884c8-108">Für die ersten Schritte mit Azure PowerShell ist es am einfachsten Azure PowerShell in einer Azure Cloud Shell-Umgebung auszuprobieren.</span><span class="sxs-lookup"><span data-stu-id="884c8-108">The easiest way to get started with Azure PowerShell is by trying it out in an Azure Cloud Shell environment.</span></span>
<span data-ttu-id="884c8-109">Informationen zum Einrichten und Ausführen von Azure PowerShell mit Cloud Shell finden Sie unter [Schnellstart für PowerShell in Azure Cloud Shell](/azure/cloud-shell/quickstart-powershell).</span><span class="sxs-lookup"><span data-stu-id="884c8-109">To get up and running with Cloud Shell, see [Quickstart for PowerShell in Azure Cloud Shell](/azure/cloud-shell/quickstart-powershell).</span></span>
<span data-ttu-id="884c8-110">Cloud Shell führt PowerShell 6 in einem Linux-Container aus. Windows-spezifische Funktionen sind daher nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="884c8-110">Cloud Shell runs PowerShell 6 on a Linux container, so Windows-specific functionality isn't available.</span></span>

<span data-ttu-id="884c8-111">Wenn Sie Azure PowerShell auf Ihrem lokalen Computer installieren möchten, folgen Sie den Anweisungen unter [Install the Azure PowerShell module](install-az-ps.md) (Installieren des Azure PowerShell-Moduls).</span><span class="sxs-lookup"><span data-stu-id="884c8-111">When you're ready to install Azure PowerShell on your local machine, follow the instructions in [Install the Azure PowerShell module](install-az-ps.md).</span></span>

## <a name="sign-in-to-azure"></a><span data-ttu-id="884c8-112">Anmelden bei Azure</span><span class="sxs-lookup"><span data-stu-id="884c8-112">Sign in to Azure</span></span>

<span data-ttu-id="884c8-113">Melden Sie sich interaktiv mit dem Cmdlet `Connect-AzAccount` an.</span><span class="sxs-lookup"><span data-stu-id="884c8-113">Sign in interactively with the `Connect-AzAccount` cmdlet.</span></span> <span data-ttu-id="884c8-114">Überspringen Sie diesen Schritt, wenn Sie Cloud Shell verwenden: Ihre Azure Cloud Shell-Sitzung ist bereits für die Umgebung, das Abonnement und den Mandanten authentifiziert, über die die Cloud Shell-Sitzung gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="884c8-114">Skip this step if you use Cloud Shell: Your Azure Cloud Shell session is already authenticated for the environment, subscription, and tenant that launched the Cloud Shell session.</span></span>

```azurepowershell-interactive
Connect-AzAccount
```

<span data-ttu-id="884c8-115">Wenn Sie sich in einer Region außerhalb der USA befinden, verwenden Sie den Parameter `-Environment` für die Anmeldung.</span><span class="sxs-lookup"><span data-stu-id="884c8-115">If you're in a non-US region, use the `-Environment` parameter to sign in.</span></span> <span data-ttu-id="884c8-116">Rufen Sie den Namen der Umgebung für Ihre Region mithilfe des Cmdlets [Get-AzEnvironment](/powershell/module/Az.Accounts/Get-AzEnvironment) ab.</span><span class="sxs-lookup"><span data-stu-id="884c8-116">Get the name of the environment for your region by using the [Get-AzEnvironment](/powershell/module/Az.Accounts/Get-AzEnvironment) cmdlet.</span></span> <span data-ttu-id="884c8-117">Geben Sie beispielsweise Folgendes ein, um sich bei Azure China 21Vianet anzumelden:</span><span class="sxs-lookup"><span data-stu-id="884c8-117">For example, to sign in to Azure China 21Vianet:</span></span>

```azurepowershell-interactive
Connect-AzAccount -Environment AzureChinaCloud
```

<span data-ttu-id="884c8-118">In PowerShell 5.1-Umgebungen wird ein Anmeldedialogfeld angezeigt, in dem Sie den Benutzernamen und das Kennwort für Ihr Azure-Konto eingeben.</span><span class="sxs-lookup"><span data-stu-id="884c8-118">In PowerShell 5.1 environments, you'll get a sign-in dialog to provide a username and password for your Azure account.</span></span> <span data-ttu-id="884c8-119">In jeder anderen Version von PowerShell erhalten Sie ein Token für die Verwendung unter [https://microsoft.com/devicelogin ].</span><span class="sxs-lookup"><span data-stu-id="884c8-119">On every other version of PowerShell, you'll get a token to use on [https://microsoft.com/devicelogin].</span></span>
<span data-ttu-id="884c8-120">Öffnen Sie diese Seite in Ihrem Browser, und geben Sie das Token ein. Melden Sie sich dann mit den Anmeldeinformationen für Ihr Azure-Konto an, und autorisieren Sie Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="884c8-120">Open this page in your browser and enter the token, then sign in with your Azure account credentials and authorize Azure PowerShell.</span></span>

<span data-ttu-id="884c8-121">Nach der Anmeldung sehen Sie Informationen, die angeben, welches Ihrer Azure-Abonnements aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="884c8-121">After signing in, you'll see information indicating which of your Azure subscriptions is active.</span></span> <span data-ttu-id="884c8-122">Wenn Sie mehrere Azure-Abonnements in Ihrem Konto haben und ein anderes auswählen möchten, rufen Sie Ihre verfügbaren Abonnements mit [Get-AzSubscription](/powershell/module/az.accounts/get-azsubscription)ab, und verwenden Sie das Cmdlet [Set-AzContext](/powershell/module/az.accounts/set-azcontext) mit Ihrer Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="884c8-122">If you have multiple Azure subscriptions in your account and want to select a different one, get your available subscriptions with [Get-AzSubscription](/powershell/module/az.accounts/get-azsubscription) and use the [Set-AzContext](/powershell/module/az.accounts/set-azcontext) cmdlet with your subscription ID.</span></span>
<span data-ttu-id="884c8-123">Weitere Informationen zum Verwalten Ihrer Azure-Abonnements in Azure PowerShell finden Sie unter [Verwenden mehrerer Azure-Abonnements](manage-subscriptions-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="884c8-123">For more information about managing your Azure subscriptions in Azure PowerShell, see [Use multiple Azure subscriptions](manage-subscriptions-azureps.md).</span></span>

<span data-ttu-id="884c8-124">Nach der Anmeldung können Sie mithilfe der Azure PowerShell-Cmdlets auf Ressourcen in Ihrem Abonnement zugreifen und diese verwalten.</span><span class="sxs-lookup"><span data-stu-id="884c8-124">Once signed in, use the Azure PowerShell cmdlets to access and manage resources in your subscription.</span></span> <span data-ttu-id="884c8-125">Weitere Informationen zum Anmeldeprozess und zu den Authentifizierungsmethoden finden Sie unter [Sign in with Azure PowerShell](authenticate-azureps.md) (Anmelden mit Azure PowerShell).</span><span class="sxs-lookup"><span data-stu-id="884c8-125">To learn more about the sign-in process and authentication methods, see [Sign in with Azure PowerShell](authenticate-azureps.md).</span></span>

## <a name="find-commands"></a><span data-ttu-id="884c8-126">Suchen nach Befehlen</span><span class="sxs-lookup"><span data-stu-id="884c8-126">Find commands</span></span>

<span data-ttu-id="884c8-127">Azure PowerShell-Cmdlets entsprechen der standardmäßigen Benennungskonvention für PowerShell: `VERB-NOUN`.</span><span class="sxs-lookup"><span data-stu-id="884c8-127">Azure PowerShell cmdlets follow a standard naming convention for PowerShell, `VERB-NOUN`.</span></span> <span data-ttu-id="884c8-128">Das Verb beschreibt die Aktion (beispielsweise `New`, `Get`, `Set` und `Remove`), und das Nomen beschreibt den Ressourcentyp (beispielsweise `AzVM`, `AzKeyVaultCertificate`, `AzFirewall` und `AzVirtualNetworkGateway`).</span><span class="sxs-lookup"><span data-stu-id="884c8-128">The verb describes the action (examples include `New`, `Get`, `Set`, `Remove`) and the noun describes the resource type (examples include `AzVM`, `AzKeyVaultCertificate`, `AzFirewall`, `AzVirtualNetworkGateway`).</span></span> <span data-ttu-id="884c8-129">Nomen in Azure PowerShell beginnen immer mit dem Präfix `Az`.</span><span class="sxs-lookup"><span data-stu-id="884c8-129">Nouns in Azure PowerShell always start with the prefix `Az`.</span></span> <span data-ttu-id="884c8-130">Die vollständige Liste der Standardverben finden Sie unter [Approved verbs for PowerShell Commands](/powershell/scripting/developer/cmdlet/approved-verbs-for-windows-powershell-commands) (Genehmigte Verben für PowerShell-Befehle).</span><span class="sxs-lookup"><span data-stu-id="884c8-130">For the full list of standard verbs, see [Approved verbs for PowerShell Commands](/powershell/scripting/developer/cmdlet/approved-verbs-for-windows-powershell-commands).</span></span>

<span data-ttu-id="884c8-131">Wenn Ihnen die verfügbaren Nomen, Verben und Azure PowerShell-Module bekannt sind, können Sie mühelos mit dem Cmdlet [Get-Command](/powershell/module/microsoft.powershell.core/get-command) nach Befehlen suchen.</span><span class="sxs-lookup"><span data-stu-id="884c8-131">Knowing the nouns, verbs, and the Azure PowerShell modules available help you find commands with the [Get-Command](/powershell/module/microsoft.powershell.core/get-command) cmdlet.</span></span> <span data-ttu-id="884c8-132">Für die Suche nach allen VM-bezogenen Befehlen mit dem Verb `Get` geben Sie beispielsweise Folgendes ein:</span><span class="sxs-lookup"><span data-stu-id="884c8-132">For example, to find all VM-related commands that use the `Get` verb:</span></span>

```powershell-interactive
Get-Command -Verb Get -Noun AzVM* -Module Az.Compute
```

<span data-ttu-id="884c8-133">Um Ihnen die Suche nach häufig verwendeten Befehlen zu erleichtern, sind in der folgenden Tabelle der Ressourcentyp, das entsprechende Azure PowerShell-Modul und das mit `Get-Command` zu verwendende Nomenpräfix aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="884c8-133">To help you find common commands, this table lists the resource type, corresponding Azure PowerShell module, and noun prefix to use with `Get-Command`:</span></span>

| <span data-ttu-id="884c8-134">Ressourcentyp</span><span class="sxs-lookup"><span data-stu-id="884c8-134">Resource type</span></span> | <span data-ttu-id="884c8-135">Azure PowerShell-Modul</span><span class="sxs-lookup"><span data-stu-id="884c8-135">Azure PowerShell module</span></span> | <span data-ttu-id="884c8-136">Nomenpräfix</span><span class="sxs-lookup"><span data-stu-id="884c8-136">Noun prefix</span></span> |
|---------------|-------------------------|----------------|
| [<span data-ttu-id="884c8-137">Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="884c8-137">Resource group</span></span>](/azure/azure-resource-manager/resource-group-overview) | [<span data-ttu-id="884c8-138">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="884c8-138">Az.Resources</span></span>](/powershell/module/az.resources#resources) | `AzResourceGroup` |
| [<span data-ttu-id="884c8-139">Virtuelle Computer</span><span class="sxs-lookup"><span data-stu-id="884c8-139">Virtual machines</span></span>](/azure/virtual-machines) | [<span data-ttu-id="884c8-140">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="884c8-140">Az.Compute</span></span>](/powershell/module/az.compute#virtual_machines) | `AzVM` |
| [<span data-ttu-id="884c8-141">Speicherkonten</span><span class="sxs-lookup"><span data-stu-id="884c8-141">Storage accounts</span></span>](/azure/storage/common/storage-introduction) | [<span data-ttu-id="884c8-142">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="884c8-142">Az.Storage</span></span>](/powershell/module/az.storage/) | `AzStorageAccount` |
| [<span data-ttu-id="884c8-143">Schlüsseltresor</span><span class="sxs-lookup"><span data-stu-id="884c8-143">Key Vault</span></span>](/azure/key-vault/key-vault-whatis) | [<span data-ttu-id="884c8-144">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="884c8-144">Az.KeyVault</span></span>](/powershell/module/az.keyvault) | `AzKeyVault` |
| [<span data-ttu-id="884c8-145">Webanwendungen</span><span class="sxs-lookup"><span data-stu-id="884c8-145">Web applications</span></span>](/azure/app-service) | [<span data-ttu-id="884c8-146">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="884c8-146">Az.Websites</span></span>](/powershell/module/az.websites) | `AzWebApp` |
| [<span data-ttu-id="884c8-147">SQL-Datenbanken</span><span class="sxs-lookup"><span data-stu-id="884c8-147">SQL databases</span></span>](/azure/sql-database) | [<span data-ttu-id="884c8-148">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="884c8-148">Az.Sql</span></span>](/powershell/module/az.sql) | `AzSqlDatabase` |

<span data-ttu-id="884c8-149">Eine vollständige Liste der Module in Azure PowerShell finden Sie unter [Azure PowerShell modules list](https://github.com/Azure/azure-powershell/blob/master/documentation/azure-powershell-modules.md) (Liste der Azure PowerShell-Module) auf GitHub.</span><span class="sxs-lookup"><span data-stu-id="884c8-149">For a full list of the modules in Azure PowerShell, see the [Azure PowerShell modules list](https://github.com/Azure/azure-powershell/blob/master/documentation/azure-powershell-modules.md) hosted on GitHub.</span></span>

## <a name="learn-azure-powershell-basics-with-quickstarts-and-tutorials"></a><span data-ttu-id="884c8-150">Kennenlernen von Azure PowerShell mit Schnellstarts und Tutorials</span><span class="sxs-lookup"><span data-stu-id="884c8-150">Learn Azure PowerShell basics with quickstarts and tutorials</span></span>

<span data-ttu-id="884c8-151">Für die ersten Schritte mit Azure PowerShell können Sie ein ausführliches Tutorial zum Einrichten von VMs und Abfragen dieser VMs nutzen.</span><span class="sxs-lookup"><span data-stu-id="884c8-151">To get started with Azure PowerShell, try an in-depth tutorial for setting up virtual machines and learning how to query them.</span></span>

> [!div class="nextstepaction"]
> <span data-ttu-id="884c8-152">[Create virtual machines with Azure PowerShell](azureps-vm-tutorial.yml) (Erstellen von VMs mit Azure PowerShell)</span><span class="sxs-lookup"><span data-stu-id="884c8-152">[Create virtual machines with Azure PowerShell](azureps-vm-tutorial.yml)</span></span>

<span data-ttu-id="884c8-153">Zudem stehen Ihnen Azure PowerShell-Schnellstarts für andere beliebte Azure-Dienste zur Verfügung:</span><span class="sxs-lookup"><span data-stu-id="884c8-153">There are also Azure PowerShell quickstarts for other popular Azure services:</span></span>

* [<span data-ttu-id="884c8-154">Erstellen eines Speicherkontos</span><span class="sxs-lookup"><span data-stu-id="884c8-154">Create a storage account</span></span>](/azure/storage/common/storage-quickstart-create-account?tabs=azure-powershell)
* [<span data-ttu-id="884c8-155">Übertragen von Objekten nach/aus Azure Blob Storage</span><span class="sxs-lookup"><span data-stu-id="884c8-155">Transfer objects to/from Azure Blob storage</span></span>](/azure/storage/blobs/storage-quickstart-blobs-powershell)
* [<span data-ttu-id="884c8-156">Erstellen und Abrufen von Geheimnissen in Azure Key Vault</span><span class="sxs-lookup"><span data-stu-id="884c8-156">Create and retrieve secrets from Azure Key Vault</span></span>](/azure/key-vault/quick-create-powershell)
* [<span data-ttu-id="884c8-157">Erstellen einer Azure SQL-Datenbank und Firewall</span><span class="sxs-lookup"><span data-stu-id="884c8-157">Create an Azure SQL database and firewall</span></span>](/azure/sql-database/scripts/sql-database-create-and-configure-database-powershell)
* [<span data-ttu-id="884c8-158">Ausführen eines Containers in Azure Container Instances</span><span class="sxs-lookup"><span data-stu-id="884c8-158">Run a container in Azure Container Instances</span></span>](/azure/container-instances/container-instances-quickstart-powershell)
* [<span data-ttu-id="884c8-159">Erstellen einer VM-Skalierungsgruppe (VMSS)</span><span class="sxs-lookup"><span data-stu-id="884c8-159">Create a Virtual Machine Scale Set (VMSS)</span></span>](/azure/virtual-machine-scale-sets/quick-create-powershell)
* [<span data-ttu-id="884c8-160">Erstellen einer Load Balancer Standard-Instanz</span><span class="sxs-lookup"><span data-stu-id="884c8-160">Create a standard load balancer</span></span>](/azure/load-balancer/quickstart-create-standard-load-balancer-powershell)

## <a name="next-steps"></a><span data-ttu-id="884c8-161">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="884c8-161">Next steps</span></span>

* [<span data-ttu-id="884c8-162">Anmelden mit Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="884c8-162">Sign in with Azure PowerShell</span></span>](authenticate-azureps.md)
* [<span data-ttu-id="884c8-163">Verwalten von Azure-Abonnements mit Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="884c8-163">Manage Azure subscriptions with Azure PowerShell</span></span>](manage-subscriptions-azureps.md)
* <span data-ttu-id="884c8-164">[Create service principals with Azure PowerShell](create-azure-service-principal-azureps.md) (Erstellen von Dienstprinzipalen mit Azure PowerShell)</span><span class="sxs-lookup"><span data-stu-id="884c8-164">[Create service principals with Azure PowerShell](create-azure-service-principal-azureps.md)</span></span>
* <span data-ttu-id="884c8-165">Hilfe aus der Community:</span><span class="sxs-lookup"><span data-stu-id="884c8-165">Get help from the community:</span></span>
  * [<span data-ttu-id="884c8-166">Azure-Forum auf MSDN</span><span class="sxs-lookup"><span data-stu-id="884c8-166">Azure forum on MSDN</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=320212)
  * [<span data-ttu-id="884c8-167">Stack Overflow</span><span class="sxs-lookup"><span data-stu-id="884c8-167">Stack Overflow</span></span>](https://go.microsoft.com/fwlink/?LinkId=320213)
