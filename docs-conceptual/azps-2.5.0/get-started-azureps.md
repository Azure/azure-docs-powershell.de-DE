---
title: Erste Schritte mit Azure PowerShell
description: ''
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: get-started-article
ms.date: 01/14/2019
ms.openlocfilehash: c60036ba8be6282007aa34a0bb9c0d9e33197072
ms.sourcegitcommit: 6c0d296bfec7c1c35a1d15074ca5eacda6684ea4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/30/2019
ms.locfileid: "68657670"
---
# <a name="get-started-with-azure-powershell"></a><span data-ttu-id="55baa-102">Erste Schritte mit Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="55baa-102">Get started with Azure PowerShell</span></span>

<span data-ttu-id="55baa-103">Azure PowerShell ist für die Verwaltung von Azure-Ressourcen über die Befehlszeile optimiert.</span><span class="sxs-lookup"><span data-stu-id="55baa-103">Azure PowerShell is designed for managing and administering Azure resources from the command line.</span></span> <span data-ttu-id="55baa-104">Verwenden Sie Azure PowerShell, wenn Sie automatisierte Tools erstellen möchten, die das Azure Resource Manager-Modell nutzen.</span><span class="sxs-lookup"><span data-stu-id="55baa-104">Use Azure PowerShell when you want to build automated tools that use the Azure Resource Manager model.</span></span>
<span data-ttu-id="55baa-105">Sie können Azure PowerShell mit [Azure Cloud Shell](/azure/cloud-shell/overview) in Ihrem Browser verwenden oder auf dem lokalen Computer installieren.</span><span class="sxs-lookup"><span data-stu-id="55baa-105">Try it out in your browser with [Azure Cloud Shell](/azure/cloud-shell/overview), or install on your local machine.</span></span>

<span data-ttu-id="55baa-106">Dieser Artikel unterstützt Sie bei den ersten Schritten mit Azure PowerShell und enthält Informationen zu den wichtigsten Konzepten.</span><span class="sxs-lookup"><span data-stu-id="55baa-106">This article helps you get started with Azure PowerShell and teaches the core concepts behind it.</span></span>

## <a name="install-or-run-in-azure-cloud-shell"></a><span data-ttu-id="55baa-107">Installieren oder Ausführen in Azure Cloud Shell</span><span class="sxs-lookup"><span data-stu-id="55baa-107">Install or run in Azure Cloud Shell</span></span>

<span data-ttu-id="55baa-108">Für die ersten Schritte mit Azure PowerShell ist es am einfachsten Azure PowerShell in einer Azure Cloud Shell-Umgebung auszuprobieren.</span><span class="sxs-lookup"><span data-stu-id="55baa-108">The easiest way to get started with Azure PowerShell is by trying it out in an Azure Cloud Shell environment.</span></span>
<span data-ttu-id="55baa-109">Informationen zum Einrichten und Ausführen von Azure PowerShell mit Cloud Shell finden Sie unter [Schnellstart für PowerShell in Azure Cloud Shell](/azure/cloud-shell/quickstart-powershell).</span><span class="sxs-lookup"><span data-stu-id="55baa-109">To get up and running with Cloud Shell, see [Quickstart for PowerShell in Azure Cloud Shell](/azure/cloud-shell/quickstart-powershell).</span></span>
<span data-ttu-id="55baa-110">Cloud Shell führt PowerShell 6 in einem Linux-Container aus. Windows-spezifische Funktionen sind daher nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="55baa-110">Cloud Shell runs PowerShell 6 on a Linux container, so Windows-specific functionality isn't available.</span></span>

<span data-ttu-id="55baa-111">Wenn Sie Azure PowerShell auf Ihrem lokalen Computer installieren möchten, folgen Sie den Anweisungen unter [Install the Azure PowerShell module](install-az-ps.md) (Installieren des Azure PowerShell-Moduls).</span><span class="sxs-lookup"><span data-stu-id="55baa-111">When you're ready to install Azure PowerShell on your local machine, follow the instructions in [Install the Azure PowerShell module](install-az-ps.md).</span></span>

## <a name="sign-in-to-azure"></a><span data-ttu-id="55baa-112">Anmelden bei Azure</span><span class="sxs-lookup"><span data-stu-id="55baa-112">Sign in to Azure</span></span>

<span data-ttu-id="55baa-113">Melden Sie sich interaktiv mit dem Cmdlet `Connect-AzAccount` an.</span><span class="sxs-lookup"><span data-stu-id="55baa-113">Sign in interactively with the `Connect-AzAccount` cmdlet.</span></span> <span data-ttu-id="55baa-114">Überspringen Sie diesen Schritt, wenn Sie Cloud Shell verwenden: Ihre Azure Cloud Shell-Sitzung ist bereits für die Umgebung, das Abonnement und den Mandanten authentifiziert, über die die Cloud Shell-Sitzung gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="55baa-114">Skip this step if you use Cloud Shell: Your Azure Cloud Shell session is already authenticated for the environment, subscription, and tenant that launched the Cloud Shell session.</span></span>

```azurepowershell-interactive
Connect-AzAccount
```

<span data-ttu-id="55baa-115">Wenn Sie sich in einer Region außerhalb der USA befinden, verwenden Sie den Parameter `-Environment` für die Anmeldung.</span><span class="sxs-lookup"><span data-stu-id="55baa-115">If you're in a non-US region, use the `-Environment` parameter to sign in.</span></span> <span data-ttu-id="55baa-116">Rufen Sie den Namen der Umgebung für Ihre Region mithilfe des Cmdlets [Get-AzEnvironment](/powershell/module/Az.Accounts/Get-AzEnvironment) ab.</span><span class="sxs-lookup"><span data-stu-id="55baa-116">Get the name of the environment for your region by using the [Get-AzEnvironment](/powershell/module/Az.Accounts/Get-AzEnvironment) cmdlet.</span></span> <span data-ttu-id="55baa-117">Geben Sie beispielsweise Folgendes ein, um sich bei Azure China 21Vianet anzumelden:</span><span class="sxs-lookup"><span data-stu-id="55baa-117">For example, to sign in to Azure China 21Vianet:</span></span>

```azurepowershell-interactive
Connect-AzAccount -Environment AzureChinaCloud
```

<span data-ttu-id="55baa-118">Sie erhalten ein Token für die Verwendung unter https://microsoft.com/devicelogin.</span><span class="sxs-lookup"><span data-stu-id="55baa-118">You'll get a token to use on https://microsoft.com/devicelogin.</span></span> <span data-ttu-id="55baa-119">Öffnen Sie diese Seite in Ihrem Browser, und geben Sie das Token ein. Melden Sie sich dann mit den Anmeldeinformationen für Ihr Azure-Konto an, und autorisieren Sie Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="55baa-119">Open this page in your browser and enter the token, then sign in with your Azure account credentials and authorize Azure PowerShell.</span></span> 

<span data-ttu-id="55baa-120">Nach der Anmeldung sehen Sie Informationen, die angeben, welches Ihrer Azure-Abonnements aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="55baa-120">After signing in, you'll see information indicating which of your Azure subscriptions is active.</span></span> <span data-ttu-id="55baa-121">Wenn Sie mehrere Azure-Abonnements in Ihrem Konto haben und ein anderes auswählen möchten, rufen Sie Ihre verfügbaren Abonnements mit [Get-AzSubscription](/powershell/module/az.accounts/get-azsubscription)ab, und verwenden Sie das Cmdlet [Set-AzContext](/powershell/module/az.accounts/set-azcontext) mit Ihrer Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="55baa-121">If you have multiple Azure subscriptions in your account and want to select a different one, get your available subscriptions with [Get-AzSubscription](/powershell/module/az.accounts/get-azsubscription) and use the [Set-AzContext](/powershell/module/az.accounts/set-azcontext) cmdlet with your subscription ID.</span></span>
<span data-ttu-id="55baa-122">Weitere Informationen zum Verwalten Ihrer Azure-Abonnements in Azure PowerShell finden Sie unter [Verwenden mehrerer Azure-Abonnements](manage-subscriptions-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="55baa-122">For more information about managing your Azure subscriptions in Azure PowerShell, see [Use multiple Azure subscriptions](manage-subscriptions-azureps.md).</span></span>

<span data-ttu-id="55baa-123">Nach der Anmeldung können Sie mithilfe der Azure PowerShell-Cmdlets auf Ressourcen in Ihrem Abonnement zugreifen und diese verwalten.</span><span class="sxs-lookup"><span data-stu-id="55baa-123">Once signed in, use the Azure PowerShell cmdlets to access and manage resources in your subscription.</span></span> <span data-ttu-id="55baa-124">Weitere Informationen zum Anmeldeprozess und zu den Authentifizierungsmethoden finden Sie unter [Sign in with Azure PowerShell](authenticate-azureps.md) (Anmelden mit Azure PowerShell).</span><span class="sxs-lookup"><span data-stu-id="55baa-124">To learn more about the sign-in process and authentication methods, see [Sign in with Azure PowerShell](authenticate-azureps.md).</span></span>

## <a name="find-commands"></a><span data-ttu-id="55baa-125">Suchen nach Befehlen</span><span class="sxs-lookup"><span data-stu-id="55baa-125">Find commands</span></span>

<span data-ttu-id="55baa-126">Azure PowerShell-Cmdlets entsprechen der standardmäßigen Benennungskonvention für PowerShell: `VERB-NOUN`.</span><span class="sxs-lookup"><span data-stu-id="55baa-126">Azure PowerShell cmdlets follow a standard naming convention for PowerShell, `VERB-NOUN`.</span></span> <span data-ttu-id="55baa-127">Das Verb beschreibt die Aktion (beispielsweise `New`, `Get`, `Set` und `Remove`), und das Nomen beschreibt den Ressourcentyp (beispielsweise `AzVM`, `AzKeyVaultCertificate`, `AzFirewall` und `AzVirtualNetworkGateway`).</span><span class="sxs-lookup"><span data-stu-id="55baa-127">The verb describes the action (examples include `New`, `Get`, `Set`, `Remove`) and the noun describes the resource type (examples include `AzVM`, `AzKeyVaultCertificate`, `AzFirewall`, `AzVirtualNetworkGateway`).</span></span> <span data-ttu-id="55baa-128">Nomen in Azure PowerShell beginnen immer mit dem Präfix `Az`.</span><span class="sxs-lookup"><span data-stu-id="55baa-128">Nouns in Azure PowerShell always start with the prefix `Az`.</span></span> <span data-ttu-id="55baa-129">Die vollständige Liste der Standardverben finden Sie unter [Approved verbs for PowerShell Commands](/powershell/developer/cmdlet/approved-verbs-for-windows-powershell-commands) (Genehmigte Verben für PowerShell-Befehle).</span><span class="sxs-lookup"><span data-stu-id="55baa-129">For the full list of standard verbs, see [Approved verbs for PowerShell Commands](/powershell/developer/cmdlet/approved-verbs-for-windows-powershell-commands).</span></span>

<span data-ttu-id="55baa-130">Wenn Ihnen die verfügbaren Nomen, Verben und Azure PowerShell-Module bekannt sind, können Sie mühelos mit dem Cmdlet [Get-Command](/powershell/module/microsoft.powershell.core/get-command) nach Befehlen suchen.</span><span class="sxs-lookup"><span data-stu-id="55baa-130">Knowing the nouns, verbs, and the Azure PowerShell modules available help you find commands with the [Get-Command](/powershell/module/microsoft.powershell.core/get-command) cmdlet.</span></span> <span data-ttu-id="55baa-131">Für die Suche nach allen VM-bezogenen Befehlen mit dem Verb `Get` geben Sie beispielsweise Folgendes ein:</span><span class="sxs-lookup"><span data-stu-id="55baa-131">For example, to find all VM-related commands that use the `Get` verb:</span></span>

```powershell-interactive
Get-Command -Verb Get -Noun AzVM* -Module Az.Compute
```

<span data-ttu-id="55baa-132">Um Ihnen die Suche nach häufig verwendeten Befehlen zu erleichtern, sind in der folgenden Tabelle der Ressourcentyp, das entsprechende Azure PowerShell-Modul und das mit `Get-Command` zu verwendende Nomenpräfix aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="55baa-132">To help you find common commands, this table lists the resource type, corresponding Azure PowerShell module, and noun prefix to use with `Get-Command`:</span></span>

| <span data-ttu-id="55baa-133">Ressourcentyp</span><span class="sxs-lookup"><span data-stu-id="55baa-133">Resource type</span></span> | <span data-ttu-id="55baa-134">Azure PowerShell-Modul</span><span class="sxs-lookup"><span data-stu-id="55baa-134">Azure PowerShell module</span></span> | <span data-ttu-id="55baa-135">Nomenpräfix</span><span class="sxs-lookup"><span data-stu-id="55baa-135">Noun prefix</span></span> |
|---------------|-------------------------|----------------|
| [<span data-ttu-id="55baa-136">Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="55baa-136">Resource group</span></span>](/azure/azure-resource-manager/resource-group-overview) | [<span data-ttu-id="55baa-137">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="55baa-137">Az.Resources</span></span>](/powershell/module/az.resources#resources) | `AzResourceGroup` |
| [<span data-ttu-id="55baa-138">Virtuelle Computer</span><span class="sxs-lookup"><span data-stu-id="55baa-138">Virtual machines</span></span>](/azure/virtual-machines) | [<span data-ttu-id="55baa-139">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="55baa-139">Az.Compute</span></span>](/powershell/module/az.compute#virtual_machines) | `AzVM` |
| [<span data-ttu-id="55baa-140">Speicherkonten</span><span class="sxs-lookup"><span data-stu-id="55baa-140">Storage accounts</span></span>](/azure/storage/common/storage-introduction) | [<span data-ttu-id="55baa-141">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="55baa-141">Az.Storage</span></span>](/powershell/module/az.storage/) | `AzStorageAccount` |
| [<span data-ttu-id="55baa-142">Schlüsseltresor</span><span class="sxs-lookup"><span data-stu-id="55baa-142">Key Vault</span></span>](/azure/key-vault/key-vault-whatis) | [<span data-ttu-id="55baa-143">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="55baa-143">Az.KeyVault</span></span>](/powershell/module/az.keyvault) | `AzKeyVault` |
| [<span data-ttu-id="55baa-144">Webanwendungen</span><span class="sxs-lookup"><span data-stu-id="55baa-144">Web applications</span></span>](/azure/app-service) | [<span data-ttu-id="55baa-145">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="55baa-145">Az.Websites</span></span>](/powershell/module/az.websites) | `AzWebApp` |
| [<span data-ttu-id="55baa-146">SQL-Datenbanken</span><span class="sxs-lookup"><span data-stu-id="55baa-146">SQL databases</span></span>](/azure/sql-database) | [<span data-ttu-id="55baa-147">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="55baa-147">Az.Sql</span></span>](/powershell/module/az.sql) | `AzSqlDatabase` |

<span data-ttu-id="55baa-148">Eine vollständige Liste der Module in Azure PowerShell finden Sie unter [Azure PowerShell modules list](https://github.com/Azure/azure-powershell/blob/master/documentation/azure-powershell-modules.md) (Liste der Azure PowerShell-Module) auf GitHub.</span><span class="sxs-lookup"><span data-stu-id="55baa-148">For a full list of the modules in Azure PowerShell, see the [Azure PowerShell modules list](https://github.com/Azure/azure-powershell/blob/master/documentation/azure-powershell-modules.md) hosted on GitHub.</span></span>

## <a name="learn-azure-powershell-basics-with-quickstarts-and-tutorials"></a><span data-ttu-id="55baa-149">Kennenlernen von Azure PowerShell mit Schnellstarts und Tutorials</span><span class="sxs-lookup"><span data-stu-id="55baa-149">Learn Azure PowerShell basics with quickstarts and tutorials</span></span>

<span data-ttu-id="55baa-150">Für die ersten Schritte mit Azure PowerShell können Sie ein ausführliches Tutorial zum Einrichten von VMs und Abfragen dieser VMs nutzen.</span><span class="sxs-lookup"><span data-stu-id="55baa-150">To get started with Azure PowerShell, try an in-depth tutorial for setting up virtual machines and learning how to query them.</span></span>

> [!div class="nextstepaction"]
> <span data-ttu-id="55baa-151">[Create virtual machines with Azure PowerShell](azureps-vm-tutorial.yml) (Erstellen von VMs mit Azure PowerShell)</span><span class="sxs-lookup"><span data-stu-id="55baa-151">[Create virtual machines with Azure PowerShell](azureps-vm-tutorial.yml)</span></span>

<span data-ttu-id="55baa-152">Zudem stehen Ihnen Azure PowerShell-Schnellstarts für andere beliebte Azure-Dienste zur Verfügung:</span><span class="sxs-lookup"><span data-stu-id="55baa-152">There are also Azure PowerShell quickstarts for other popular Azure services:</span></span>

* [<span data-ttu-id="55baa-153">Erstellen eines Speicherkontos</span><span class="sxs-lookup"><span data-stu-id="55baa-153">Create a storage account</span></span>](/azure/storage/common/storage-quickstart-create-account?tabs=azure-powershell)
* [<span data-ttu-id="55baa-154">Übertragen von Objekten nach/aus Azure Blob Storage</span><span class="sxs-lookup"><span data-stu-id="55baa-154">Transfer objects to/from Azure Blob storage</span></span>](/azure/storage/blobs/storage-quickstart-blobs-powershell)
* [<span data-ttu-id="55baa-155">Erstellen und Abrufen von Geheimnissen in Azure Key Vault</span><span class="sxs-lookup"><span data-stu-id="55baa-155">Create and retrieve secrets from Azure Key Vault</span></span>](/azure/key-vault/quick-create-powershell)
* [<span data-ttu-id="55baa-156">Erstellen einer Azure SQL-Datenbank und Firewall</span><span class="sxs-lookup"><span data-stu-id="55baa-156">Create an Azure SQL database and firewall</span></span>](/azure/sql-database/scripts/sql-database-create-and-configure-database-powershell)
* [<span data-ttu-id="55baa-157">Ausführen eines Containers in Azure Container Instances</span><span class="sxs-lookup"><span data-stu-id="55baa-157">Run a container in Azure Container Instances</span></span>](/azure/container-instances/container-instances-quickstart-powershell)
* [<span data-ttu-id="55baa-158">Erstellen einer VM-Skalierungsgruppe (VMSS)</span><span class="sxs-lookup"><span data-stu-id="55baa-158">Create a Virtual Machine Scale Set (VMSS)</span></span>](/azure/virtual-machine-scale-sets/quick-create-powershell)
* [<span data-ttu-id="55baa-159">Erstellen einer Load Balancer Standard-Instanz</span><span class="sxs-lookup"><span data-stu-id="55baa-159">Create a standard load balancer</span></span>](/azure/load-balancer/quickstart-create-standard-load-balancer-powershell)

## <a name="next-steps"></a><span data-ttu-id="55baa-160">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="55baa-160">Next steps</span></span>

* [<span data-ttu-id="55baa-161">Anmelden mit Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="55baa-161">Sign in with Azure PowerShell</span></span>](authenticate-azureps.md)
* [<span data-ttu-id="55baa-162">Verwalten von Azure-Abonnements mit Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="55baa-162">Manage Azure subscriptions with Azure PowerShell</span></span>](manage-subscriptions-azureps.md)
* <span data-ttu-id="55baa-163">[Create service principals with Azure PowerShell](create-azure-service-principal-azureps.md) (Erstellen von Dienstprinzipalen mit Azure PowerShell)</span><span class="sxs-lookup"><span data-stu-id="55baa-163">[Create service principals with Azure PowerShell](create-azure-service-principal-azureps.md)</span></span>
* <span data-ttu-id="55baa-164">Hilfe aus der Community:</span><span class="sxs-lookup"><span data-stu-id="55baa-164">Get help from the community:</span></span>
  * [<span data-ttu-id="55baa-165">Azure-Forum auf MSDN</span><span class="sxs-lookup"><span data-stu-id="55baa-165">Azure forum on MSDN</span></span>](http://go.microsoft.com/fwlink/p/?LinkId=320212)
  * [<span data-ttu-id="55baa-166">Stack Overflow</span><span class="sxs-lookup"><span data-stu-id="55baa-166">Stack Overflow</span></span>](http://go.microsoft.com/fwlink/?LinkId=320213)
