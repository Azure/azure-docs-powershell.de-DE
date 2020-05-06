---
title: Verwalten von Azure-Abonnements mit Azure PowerShell
description: Verwalten von Azure-Abonnements mit Azure PowerShell
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 02/04/2019
ms.openlocfilehash: 778fdb463a42b609d3a94c910a2c0f9553ef4eb9
ms.sourcegitcommit: d661f38bec34e65bf73913db59028e11fd78b131
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/05/2020
ms.locfileid: "81740166"
---
# <a name="use-multiple-azure-subscriptions"></a>Verwenden mehrerer Azure-Abonnements

Die meisten Azure-Benutzer verwenden nur ein einzelnes Abonnement. Wenn Sie allerdings mehreren Organisationen angehören oder Ihre Organisation den Zugriff auf bestimmte Ressourcen über Gruppierungen aufgeteilt hat, besitzen Sie möglicherweise mehrere Abonnements in Azure. Die CLI unterstützt sowohl die globale Auswahl eines Abonnements als auch die Auswahl per Befehl.

Ausführliche Informationen zu Abonnements, der Abrechnung und der Kostenverwaltung finden Sie in der [Dokumentation zur Abrechnungs- und Kostenverwaltung in Azure](/azure/billing/).

## <a name="tenants-users-and-subscriptions"></a>Mandanten, Benutzer und Abonnements

Möglicherweise sind Sie sich nicht ganz über den Unterschied zwischen Mandanten, Benutzern und Abonnements in Azure im Klaren. Ein _Mandant_ ist die Azure Active Directory-Entität, die eine gesamte Organisation umfasst. Dieser Mandant hat mindestens ein _Abonnement_ und einen _Benutzer_. Ein Benutzer ist eine Person und nur einem einzelnen Mandanten zugeordnet: der Organisation, der er angehört. Benutzer sind Konten, die sich bei Azure anmelden, um Ressourcen zu erstellen, zu verwalten und zu verwenden.
Ein Benutzer hat möglicherweise Zugriff auf mehrere _Abonnements_. Hierbei handelt es sich um die Vereinbarungen mit Microsoft, die die Verwendung von Clouddiensten wie Azure regeln. Jede Ressource ist einem Abonnement zugeordnet.

Weitere Informationen zu den Unterschieden zwischen Mandanten, Benutzern und Abonnements finden Sie im [Microsoft Azure-Glossar](/azure/azure-glossary-cloud-terminology).  Informationen zum Hinzufügen eines neuen Abonnements zu Ihrem Azure Active Directory-Mandanten finden Sie unter [Hinzufügen eines Azure-Abonnements zu Azure Active Directory](/azure/active-directory/active-directory-how-subscriptions-associated-directory).
Informationen zum Anmelden bei einem bestimmten Mandanten finden Sie unter [Anmelden mit Azure PowerShell](/powershell/azure/authenticate-azureps).

## <a name="change-the-active-subscription"></a>Ändern des aktiven Abonnements

In Azure PowerShell ist für den Zugriff auf die Ressourcen für ein Abonnement eine Änderung des Abonnements erforderlich, das Ihrer aktuellen Azure-Sitzung zugeordnet ist.
Hierfür wird der Kontext der aktiven Sitzung geändert. Dies sind die Informationen dazu, welcher Mandant, welches Abonnement und welche Benutzer-Cmdlets für die Ausführung verwendet werden sollen.
Zum Ändern von Abonnements muss zuerst mit [Get-AzSubscription](/powershell/module/az.accounts/get-azsubscription) ein Azure PowerShell-Kontextobjekt abgerufen und anschließend der aktuelle Kontext mit [Set-AzContext](/powershell/module/az.accounts/set-azcontext) geändert werden.

Im nächsten Beispiel wird veranschaulicht, wie Sie ein Abonnement im derzeit aktiven Mandanten abrufen und als aktive Sitzung festlegen:

```powershell-interactive
$context = Get-AzSubscription -SubscriptionId ...
Set-AzContext $context
```

Weitere Informationen zu Azure PowerShell-Kontexten, z. B. zum Durchführen von Speichervorgängen und schnellen Wechseln zwischen Kontexten, um die Nutzung mehrerer Abonnements zu vereinfachen, finden Sie unter [Speichern von Benutzeranmeldeinformationen zwischen PowerShell-Sitzungen](context-persistence.md).
