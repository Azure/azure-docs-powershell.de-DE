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
ms.sourcegitcommit: 30eeeec0985f8623b1bc03f461124446b04297c2
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2020
ms.locfileid: "76256832"
---
# <a name="get-started-with-azure-powershell"></a>Erste Schritte mit Azure PowerShell

Azure PowerShell ist für die Verwaltung von Azure-Ressourcen über die Befehlszeile optimiert. Verwenden Sie Azure PowerShell, wenn Sie automatisierte Tools erstellen möchten, die das Azure Resource Manager-Modell nutzen.
Sie können Azure PowerShell mit [Azure Cloud Shell](/azure/cloud-shell/overview) in Ihrem Browser verwenden oder auf dem lokalen Computer installieren.

Dieser Artikel unterstützt Sie bei den ersten Schritten mit Azure PowerShell und enthält Informationen zu den wichtigsten Konzepten.

## <a name="install-or-run-in-azure-cloud-shell"></a>Installieren oder Ausführen in Azure Cloud Shell

Für die ersten Schritte mit Azure PowerShell ist es am einfachsten Azure PowerShell in einer Azure Cloud Shell-Umgebung auszuprobieren.
Informationen zum Einrichten und Ausführen von Azure PowerShell mit Cloud Shell finden Sie unter [Schnellstart für PowerShell in Azure Cloud Shell](/azure/cloud-shell/quickstart-powershell).
Cloud Shell führt PowerShell 6 in einem Linux-Container aus. Windows-spezifische Funktionen sind daher nicht verfügbar.

Wenn Sie Azure PowerShell auf Ihrem lokalen Computer installieren möchten, folgen Sie den Anweisungen unter [Install the Azure PowerShell module](install-az-ps.md) (Installieren des Azure PowerShell-Moduls).

## <a name="sign-in-to-azure"></a>Anmelden bei Azure

Melden Sie sich interaktiv mit dem Cmdlet `Connect-AzAccount` an. Überspringen Sie diesen Schritt, wenn Sie Cloud Shell verwenden: Ihre Azure Cloud Shell-Sitzung ist bereits für die Umgebung, das Abonnement und den Mandanten authentifiziert, über die die Cloud Shell-Sitzung gestartet wurde.

```azurepowershell-interactive
Connect-AzAccount
```

Wenn Sie sich in einer Region außerhalb der USA befinden, verwenden Sie den Parameter `-Environment` für die Anmeldung. Rufen Sie den Namen der Umgebung für Ihre Region mithilfe des Cmdlets [Get-AzEnvironment](/powershell/module/Az.Accounts/Get-AzEnvironment) ab. Geben Sie beispielsweise Folgendes ein, um sich bei Azure China 21Vianet anzumelden:

```azurepowershell-interactive
Connect-AzAccount -Environment AzureChinaCloud
```

In PowerShell 5.1-Umgebungen wird ein Anmeldedialogfeld angezeigt, in dem Sie den Benutzernamen und das Kennwort für Ihr Azure-Konto eingeben. In jeder anderen Version von PowerShell erhalten Sie ein Token für die Verwendung unter [https://microsoft.com/devicelogin ].
Öffnen Sie diese Seite in Ihrem Browser, und geben Sie das Token ein. Melden Sie sich dann mit den Anmeldeinformationen für Ihr Azure-Konto an, und autorisieren Sie Azure PowerShell.

Nach der Anmeldung sehen Sie Informationen, die angeben, welches Ihrer Azure-Abonnements aktiv ist. Wenn Sie mehrere Azure-Abonnements in Ihrem Konto haben und ein anderes auswählen möchten, rufen Sie Ihre verfügbaren Abonnements mit [Get-AzSubscription](/powershell/module/az.accounts/get-azsubscription)ab, und verwenden Sie das Cmdlet [Set-AzContext](/powershell/module/az.accounts/set-azcontext) mit Ihrer Abonnement-ID.
Weitere Informationen zum Verwalten Ihrer Azure-Abonnements in Azure PowerShell finden Sie unter [Verwenden mehrerer Azure-Abonnements](manage-subscriptions-azureps.md).

Nach der Anmeldung können Sie mithilfe der Azure PowerShell-Cmdlets auf Ressourcen in Ihrem Abonnement zugreifen und diese verwalten. Weitere Informationen zum Anmeldeprozess und zu den Authentifizierungsmethoden finden Sie unter [Sign in with Azure PowerShell](authenticate-azureps.md) (Anmelden mit Azure PowerShell).

## <a name="find-commands"></a>Suchen nach Befehlen

Azure PowerShell-Cmdlets entsprechen der standardmäßigen Benennungskonvention für PowerShell: `VERB-NOUN`. Das Verb beschreibt die Aktion (beispielsweise `New`, `Get`, `Set` und `Remove`), und das Nomen beschreibt den Ressourcentyp (beispielsweise `AzVM`, `AzKeyVaultCertificate`, `AzFirewall` und `AzVirtualNetworkGateway`). Nomen in Azure PowerShell beginnen immer mit dem Präfix `Az`. Die vollständige Liste der Standardverben finden Sie unter [Approved verbs for PowerShell Commands](/powershell/scripting/developer/cmdlet/approved-verbs-for-windows-powershell-commands) (Genehmigte Verben für PowerShell-Befehle).

Wenn Ihnen die verfügbaren Nomen, Verben und Azure PowerShell-Module bekannt sind, können Sie mühelos mit dem Cmdlet [Get-Command](/powershell/module/microsoft.powershell.core/get-command) nach Befehlen suchen. Für die Suche nach allen VM-bezogenen Befehlen mit dem Verb `Get` geben Sie beispielsweise Folgendes ein:

```powershell-interactive
Get-Command -Verb Get -Noun AzVM* -Module Az.Compute
```

Um Ihnen die Suche nach häufig verwendeten Befehlen zu erleichtern, sind in der folgenden Tabelle der Ressourcentyp, das entsprechende Azure PowerShell-Modul und das mit `Get-Command` zu verwendende Nomenpräfix aufgeführt:

| Ressourcentyp | Azure PowerShell-Modul | Nomenpräfix |
|---------------|-------------------------|----------------|
| [Ressourcengruppe](/azure/azure-resource-manager/resource-group-overview) | [Az.Resources](/powershell/module/az.resources#resources) | `AzResourceGroup` |
| [Virtuelle Computer](/azure/virtual-machines) | [Az.Compute](/powershell/module/az.compute#virtual_machines) | `AzVM` |
| [Speicherkonten](/azure/storage/common/storage-introduction) | [Az.Storage](/powershell/module/az.storage/) | `AzStorageAccount` |
| [Schlüsseltresor](/azure/key-vault/key-vault-whatis) | [Az.KeyVault](/powershell/module/az.keyvault) | `AzKeyVault` |
| [Webanwendungen](/azure/app-service) | [Az.Websites](/powershell/module/az.websites) | `AzWebApp` |
| [SQL-Datenbanken](/azure/sql-database) | [Az.Sql](/powershell/module/az.sql) | `AzSqlDatabase` |

Eine vollständige Liste der Module in Azure PowerShell finden Sie unter [Azure PowerShell modules list](https://github.com/Azure/azure-powershell/blob/master/documentation/azure-powershell-modules.md) (Liste der Azure PowerShell-Module) auf GitHub.

## <a name="learn-azure-powershell-basics-with-quickstarts-and-tutorials"></a>Kennenlernen von Azure PowerShell mit Schnellstarts und Tutorials

Für die ersten Schritte mit Azure PowerShell können Sie ein ausführliches Tutorial zum Einrichten von VMs und Abfragen dieser VMs nutzen.

> [!div class="nextstepaction"]
> [Create virtual machines with Azure PowerShell](azureps-vm-tutorial.yml) (Erstellen von VMs mit Azure PowerShell)

Zudem stehen Ihnen Azure PowerShell-Schnellstarts für andere beliebte Azure-Dienste zur Verfügung:

* [Erstellen eines Speicherkontos](/azure/storage/common/storage-quickstart-create-account?tabs=azure-powershell)
* [Übertragen von Objekten nach/aus Azure Blob Storage](/azure/storage/blobs/storage-quickstart-blobs-powershell)
* [Erstellen und Abrufen von Geheimnissen in Azure Key Vault](/azure/key-vault/quick-create-powershell)
* [Erstellen einer Azure SQL-Datenbank und Firewall](/azure/sql-database/scripts/sql-database-create-and-configure-database-powershell)
* [Ausführen eines Containers in Azure Container Instances](/azure/container-instances/container-instances-quickstart-powershell)
* [Erstellen einer VM-Skalierungsgruppe (VMSS)](/azure/virtual-machine-scale-sets/quick-create-powershell)
* [Erstellen einer Load Balancer Standard-Instanz](/azure/load-balancer/quickstart-create-standard-load-balancer-powershell)

## <a name="next-steps"></a>Nächste Schritte

* [Anmelden mit Azure PowerShell](authenticate-azureps.md)
* [Verwalten von Azure-Abonnements mit Azure PowerShell](manage-subscriptions-azureps.md)
* [Create service principals with Azure PowerShell](create-azure-service-principal-azureps.md) (Erstellen von Dienstprinzipalen mit Azure PowerShell)
* Hilfe aus der Community:
  * [Azure-Forum auf MSDN](https://go.microsoft.com/fwlink/p/?LinkId=320212)
  * [Stack Overflow](https://go.microsoft.com/fwlink/?LinkId=320213)
