---
title: Installieren und Konfigurieren von Azure PowerShell | Microsoft-Dokumentation
description: Hier erfahren Sie, wie Sie Azure PowerShell für die erste Verwendung installieren und konfigurieren.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/27/2018
ms.openlocfilehash: dc11af0fff84899ca1b3ad3abf8760dd8c59e6f6
ms.sourcegitcommit: b02cbcd00748a4a9a4790a5fba229ce53c3bf973
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/09/2019
ms.locfileid: "68863273"
---
# <a name="install-azure-powershell-on-windows-with-powershellget"></a>Installieren von Azure PowerShell unter Windows mit PowerShellGet

[!INCLUDE [migrate-to-az](../includes/migrate-to-az.md)]

In diesem Artikel erfahren Sie, wie Sie die Azure PowerShell-Module für PowerShell 5.x für Windows mit PowerShellGet installieren. PowerShellGet und die Modulverwaltung stellen die bevorzugte Installationsmethode für Azure PowerShell dar. Sie können aber auch den Webplattform-Installer oder das MSI-Paket verwenden. Entsprechende Informationen finden Sie unter [Andere Installationsmethoden](other-install.md).

Das klassische Azure-Bereitstellungsmodell wird von dieser Version von Azure PowerShell nicht unterstützt. Befolgen Sie die Anleitung unter [Installieren des Azure PowerShell-Dienstverwaltungsmoduls](/powershell/azure/servicemanagement/install-azure-ps), um Unterstützung zu klassischen Bereitstellungen zu erhalten.

> [!IMPORTANT]
> Das AzureRM-Modul wird für macOS oder Linux nicht unterstützt. Wenn Sie Azure PowerShell-Cmdlets auf diesen Plattformen verwenden möchten, [installieren Sie das Az-Modul](/powershell/azure/install-az-ps).

## <a name="step-1-install-powershellget"></a>Schritt 1: Installieren von PowerShellGet

Für die Installation von Komponenten aus dem PowerShell-Katalog ist das PowerShellGet-Modul erforderlich. Stellen Sie sicher, dass Sie über die entsprechende Version von PowerShellGet verfügen und alle anderen Systemanforderungen erfüllt sind. Führen Sie den folgenden Befehl aus, um zu ermitteln, ob PowerShellGet auf Ihrem System installiert ist.


```powershell-interactive
Get-InstalledModule -Name PowerShellGet -ListAvailable | Select-Object -Property Name,Version,Path
```

Etwa folgende Ausgabe sollte angezeigt werden:

```Output
Name          Version Path
----          ------- ----
Name          Version Path
----          ------- ----
PowerShellGet 1.6.0   C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.6.0\PowerShellGet.psd1
PowerShellGet 1.0.0.1 C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.0.0.1\PowerShellGet.psd1
```

Sie benötigen mindestens die PowerShellGet-Version 1.1.2.0. Verwenden Sie zum Aktualisieren von PowerShellGet den folgenden Befehl:

```powershell-interactive
Install-Module PowerShellGet -Force
```

Falls PowerShellGet nicht installiert ist, lesen Sie die Informationen im Abschnitt [Installieren von PowerShellGet](#how-to-get-powershellget) dieses Artikels.

> [!NOTE]
> Für die Verwendung von PowerShellGet ist eine Ausführungsrichtlinie erforderlich, die die Ausführung von Skripts ermöglicht. Weitere Informationen zur Ausführungsrichtlinie von PowerShell finden Sie unter [About Execution Policies](/powershell/module/microsoft.powershell.core/about/about_execution_policies) (Informationen zu Ausführungsrichtlinien).
>
> [!IMPORTANT]
> Das in diesem Dokument beschriebene Modul „AzureRM“ verwendet .NET Framework. Dadurch ist es nicht mit PowerShell 6.0 kompatibel, das .NET Core verwendet. Wenn Sie PowerShell 6.0 verwenden, befolgen Sie die [Installationsanweisungen für macOS und Linux](install-azurermps-maclinux.md).

## <a name="step-2-install-azure-powershell"></a>Schritt 2: Installieren von Azure Powershell

Für die Installation von Azure PowerShell aus dem PowerShell-Katalog sind erhöhte Rechte erforderlich. Führen Sie den folgenden Befehl in einer PowerShell-Sitzung mit erhöhten Rechten aus:

```powershell-interactive
# Install the Azure Resource Manager modules from the PowerShell Gallery
Install-Module -Name AzureRM -AllowClobber
```

Standardmäßig ist der PowerShell-Katalog nicht als vertrauenswürdiges Repository für PowerShellGet konfiguriert. Bei der ersten Verwendung des PowerShell-Katalogs wird die folgende Meldung angezeigt:

```Output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"): Y
```

Antworten Sie mit „Ja“ oder „Ja zu allen“, um die Installation fortzusetzen.

> [!NOTE]
> Wenn Sie eine ältere NuGet-Version als 2.8.5.201 haben, werden Sie aufgefordert, die aktuelle NuGet-Version herunterzuladen und zu installieren.

Das AzureRM-Modul ist ein Rollupmodul für die Azure Resource Manager-Cmdlets. Bei der Installation des AzureRM-Moduls werden alle noch nicht installierten Azure PowerShell-Module aus dem PowerShell-Katalog heruntergeladen und installiert.

Wenn eine frühere Version von Azure PowerShell installiert ist, erhalten Sie möglicherweise eine Fehlermeldung. Informationen zum Beheben dieses Problem finden Sie im Abschnitt [Aktualisieren auf eine neue Version von Azure PowerShell](#update-azps) dieses Artikels.

## <a name="step-3-load-the-azurerm-module"></a>Schritt 3: Laden des AzureRM-Moduls

Nach der Installation des Moduls müssen Sie das Modul in der PowerShell-Sitzung laden. Dies muss in einer normalen PowerShell-Sitzung (ohne erhöhte Rechte) erfolgen. Module werden wie folgt mit dem Cmdlet `Import-Module` geladen:

```powershell-interactive
Import-Module -Name AzureRM
```

## <a name="next-steps"></a>Nächste Schritte

Weitere Informationen zur Verwendung von Azure PowerShell finden Sie in den folgenden Artikeln:

* [Erste Schritte mit Azure PowerShell](get-started-azureps.md)

## <a name="reporting-issues-and-feedback"></a>Melden von Problemen und Bereitstellen von Feedback

Wenn mit dem Tool Fehler auftreten, legen Sie einen Eintrag im Bereich [Probleme](https://github.com/Azure/azure-powershell/issues) unseres GitHub Repositorys an. Zum Senden von Feedback zur Befehlszeile verwenden Sie das Cmdlet `Send-Feedback`.

## <a name="frequently-asked-questions"></a>Häufig gestellte Fragen

### <a name="how-to-get-powershellget"></a>Installieren von PowerShellGet

|Betriebssystemversion|Installationsanleitung|
|---|---|
|Ich besitze Windows 10 oder Windows Server 2016.|In Windows Management Framework (WMF) 5.0 integriert (im Betriebssystem enthalten)|
|Ich möchte auf PowerShell 5 aktualisieren.|[Installieren Sie die aktuelle Version von WMF.](https://www.microsoft.com/download/details.aspx?id=54616)|
|Ich nutze eine Windows-Version mit PowerShell 3 oder PowerShell 4.|[Laden Sie die PackageManagement-Module herunter.](http://go.microsoft.com/fwlink/?LinkID=746217)|

### <a name="div-idhelpmechoosechecking-the-version-of-azure-powershell"></a><div id="helpmechoose"/>Überprüfen der Azure PowerShell-Version

Obwohl empfohlen wird, möglichst bald ein Upgrade auf die neueste Version auszuführen, werden verschiedene Azure PowerShell-Versionen unterstützt. Führen Sie zum Ermitteln der installierten Azure PowerShell-Version `Get-InstalledModule AzureRM` in der Befehlszeile aus:

```powershell-interactive
Get-InstalledModule AzureRM -AllVersions | Select-Object -Property Name,Version,Path
```

### <a name="support-for-classic-deployment-methods"></a>Unterstützung für klassische Bereitstellungsmethoden

Bei Bereitstellungen mit dem klassischen Bereitstellungsmodell können Sie die Dienstverwaltungsversion von Azure PowerShell installieren. Weitere Informationen finden Sie unter [Installing the Azure PowerShell Service Management module](/powershell/azure/servicemanagement/install-azure-ps) (Installieren des Azure PowerShell-Dienstverwaltungsmoduls). Das Azure- und das AzureRM-Modul nutzen gemeinsame Abhängigkeiten. Wenn Sie sowohl die Azure- als auch die AzureRM-Module verwenden, müssen Sie die gleiche Version der einzelnen Pakete installieren.

### <a name="div-idupdate-azpsupdating-to-a-new-version-of-azure-powershell"></a><div id="update-azps"/>Aktualisieren auf eine neue Version von Azure PowerShell

Wenn Sie eine frühere Version von Azure PowerShell installiert haben, die das Dienstverwaltungsmodul enthält, kann die folgende Fehlermeldung angezeigt werden:

```Output
PackageManagement\Install-Package : A command with name 'Get-AzureStorageContainerAcl' is already
available on this system. This module 'Azure.Storage' may override the existing commands. If you
still want to install this module 'Azure.Storage', use -AllowClobber parameter.

At C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.0.0.1\PSModule.psm1:1772 char:21
+ ...          $null = PackageManagement\Install-Package @PSBoundParameters
+                      ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : InvalidOperation: (Microsoft.Power....InstallPackage:InstallPackage) [Install-Package], Exception
    + FullyQualifiedErrorId : CommandAlreadyAvailable,Validate-ModuleCommandAlreadyAvailable,Microsoft.PowerShell.PackageManagement.Cmdlets.InstallPackage
```

Wie in der Fehlermeldung angegeben, müssen Sie den Parameter „-AllowClobber“ zum Installieren des Moduls verwenden. Verwenden Sie den folgenden Befehl:

```powershell-interactive
# Install the Azure Resource Manager modules from the PowerShell Gallery
Install-Module -Name AzureRM -AllowClobber
```

Weitere Informationen finden Sie im Hilfethema zu [Install-Module](https://msdn.microsoft.com/powershell/reference/5.1/PowerShellGet/install-module).

### <a name="installing-module-versions-side-by-side"></a>Parallele Installation von Modulversionen

Die PowerShellGet-Installationsmethode ist die einzige Methode, die die Installation mehrerer Versionen unterstützt. Beispiel: Sie besitzen Skripts, die mit einer vorherigen Version von Azure PowerShell geschrieben wurden, für deren Aktualisierung keine Zeit ist bzw. keine Ressourcen verfügbar sind. Die folgenden Befehle veranschaulichen, wie mehrere Versionen von Azure PowerShell installiert werden:

```powershell-interactive
Install-Module -Name AzureRM -RequiredVersion 3.7.0
Install-Module -Name AzureRM -RequiredVersion 2.3.0
```

Nur eine Version des Moduls kann in einer PowerShell-Sitzung geladen werden. Sie müssen ein neues PowerShell-Fenster öffnen und `Import-Module` verwenden, um eine bestimmte Version der AzureRM-Cmdlets zu importieren:

```powershell-interactive
Import-Module -Name AzureRM -RequiredVersion 2.3.0
```

> [!NOTE]
> Version 2.1.0 und Version 1.2.6 sind die ersten Modulversionen, die parallel installiert und genutzt werden können. Beim Laden einer früheren Version von Azure PowerShell werden inkompatible Versionen des **AzureRM.Profile**-Moduls geladen. Dies führt dazu, dass Sie, immer wenn Sie ein Cmdlet ausführen, zum Anmelden aufgefordert werden.

### <a name="other-installation-methods"></a>Andere Installationsmethoden

Information zum Installieren des Webplattform-Installers oder des MSI-Pakets finden Sie unter [Other installation methods](other-install.md) (Andere Installationsmethoden).
