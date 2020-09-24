---
title: Anmelden mit Azure PowerShell
description: Es wird beschrieben, wie Sie sich mit Azure PowerShell als Benutzer, per Dienstprinzipal oder mit verwalteten Identitäten für Azure-Ressourcen anmelden.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 7/7/2020
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 8f18af8ed67ecf2aefd353208c07bf812df732d9
ms.sourcegitcommit: 15f21c40dcb7610e2fbaaabf264ad925e4224500
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/22/2020
ms.locfileid: "90928339"
---
# <a name="sign-in-with-azure-powershell"></a>Anmelden mit Azure PowerShell

Azure PowerShell unterstützt mehrere Authentifizierungsmethoden. Den einfachsten Einstieg ermöglicht der [Azure Cloud Shell](/azure/cloud-shell/overview)-Dienst, der Sie automatisch anmeldet. Bei einer lokalen Installation können Sie sich interaktiv über Ihren Browser anmelden. Beim Schreiben von Skripts für die Automatisierung besteht der empfohlene Ansatz darin, einen [Dienstprinzipal](create-azure-service-principal-azureps.md) mit den erforderlichen Berechtigungen zu verwenden. Indem Sie die Anmeldeberechtigungen für Ihren Anwendungsfall so weit wie möglich einschränken, tragen Sie zur Sicherheit Ihrer Azure-Ressourcen bei.

Zunächst sind Sie beim ersten Abonnement angemeldet, das von Azure zurückgegeben wird, wenn Sie Zugriff auf mehrere Abonnements haben. Befehle werden für dieses Abonnement standardmäßig ausgeführt. Verwenden Sie das Cmdlet [Set-AzContext](/powershell/module/az.accounts/set-azcontext), um Ihr aktives Abonnement für eine Sitzung zu ändern. Um Ihr aktives Abonnement zu ändern und es zwischen Sitzungen auf demselben System beizubehalten, verwenden Sie das Cmdlet [Select-AzContext](/powershell/module/az.accounts/select-azcontext).

> [!IMPORTANT]
> Ihre Anmeldeinformationen werden in mehreren PowerShell-Sitzungen gemeinsam verwendet, solange Sie angemeldet bleiben.
> Weitere Informationen finden Sie im Artikel zu [beständigen Anmeldeinformationen](context-persistence.md).

## <a name="sign-in-interactively"></a>Interaktives Anmelden

Verwenden Sie für die interaktive Anmeldung das Cmdlet [Connect-AzAccount](/powershell/module/az.accounts/connect-azaccount).

```azurepowershell-interactive
Connect-AzAccount
```

Bei der Ausführung über PowerShell ab Version 6 zeigt dieses Cmdlet eine Tokenzeichenfolge an. Kopieren Sie diese Zeichenfolge, und fügen Sie sie in [microsoft.com/devicelogin](https://microsoft.com/devicelogin) in einem Webbrowser ein, um sich anzumelden. Ihre PowerShell-Sitzung wird für die Verbindungsherstellung mit Azure authentifiziert. Sie können den `UseDeviceAuthentication`-Parameter angeben, um eine Tokenzeichenfolge in Windows PowerShell zu erhalten.

> [!IMPORTANT]
> Die Autorisierung mit Anmeldeinformationen (Benutzername/Kennwort) wurde in Azure PowerShell aufgrund von Änderungen in Active Directory-Autorisierungsimplementierungen und Sicherheitsbedenken entfernt. Wenn Sie die Autorisierung mit Anmeldeinformationen zu Automatisierungszwecken verwenden, [erstellen Sie stattdessen einen Dienstprinzipal](create-azure-service-principal-azureps.md).

Verwenden Sie das Cmdlet [Get-AzContext](/powershell/module/az.accounts/get-azcontext), um Ihre Mandanten-ID in einer Variablen zu speichern, die in den nächsten beiden Abschnitten dieses Artikels verwendet werden soll.

```azurepowershell-interactive
$tenantId = (Get-AzContext).Tenant.Id
```

## <a name="sign-in-with-a-service-principal"></a>Anmelden mit einem Dienstprinzipal<a name="sp-signin"/>

Dienstprinzipale sind nicht interaktive Azure-Konten. Wie bei anderen Benutzerkonten auch, werden die Berechtigungen mit Azure Active Directory verwaltet. Indem für einen Dienstprinzipal nur die benötigten Berechtigungen gewährt werden, bleibt die Sicherheit Ihrer Automatisierungsskripts gewahrt.

Informationen zur Erstellung eines Dienstprinzipals für die Verwendung mit PowerShell finden Sie unter [Erstellen eines Azure-Dienstprinzipals mit Azure PowerShell](create-azure-service-principal-azureps.md).

Verwenden Sie für die Anmeldung mit einem Dienstprinzipal das Cmdlet `Connect-AzAccount` mit dem Argument `-ServicePrincipal`. Sie benötigen auch die Anwendungs-ID und die Anmeldeinformationen des Dienstprinzipals sowie die dem Dienstprinzipal zugeordnete Mandanten-ID. Wie Sie sich mit einem Dienstprinzipal anmelden, hängt davon ab, ob er für die kennwortbasierte oder die zertifikatbasierte Authentifizierung konfiguriert wurde.

### <a name="password-based-authentication"></a>Kennwortbasierte Authentifizierung

Erstellen Sie einen Dienstprinzipal für die Verwendung in den Beispielen in diesem Abschnitt. Weitere Informationen zum Erstellen von Dienstprinzipalen finden Sie unter [Erstellen eines Azure-Dienstprinzipals mit Azure PowerShell](/powershell/azure/create-azure-service-principal-azureps).

```azurepowershell-interactive
$sp = New-AzADServicePrincipal -DisplayName ServicePrincipalName
```

Verwenden Sie das Cmdlet [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential), um die Anmeldeinformationen des Dienstprinzipals als entsprechendes Objekt abzurufen. Mit diesem Cmdlet wird eine Eingabeaufforderung für Benutzername und Kennwort angezeigt. Verwenden Sie die `applicationID` des Dienstprinzipals für den Benutzernamen, und konvertieren Sie dessen `secret` in Nur-Text für das Kennwort.

```azurepowershell-interactive
# Retrieve the plain text password for use with `Get-Credential` in the next command.
$sp.secret | ConvertFrom-SecureString -AsPlainText

$pscredential = Get-Credential -UserName $sp.ApplicationId
Connect-AzAccount -ServicePrincipal -Credential $pscredential -Tenant $tenantId
```

Für Automatisierungsszenarien müssen Sie Anmeldeinformationen aus der `applicationId` und dem `secret` eines Dienstprinzipals erstellen:

```azurepowershell-interactive
$pscredential = New-Object -TypeName System.Management.Automation.PSCredential($sp.ApplicationId, $sp.Secret)
Connect-AzAccount -ServicePrincipal -Credential $pscredential -Tenant $tenantId
```

Achten Sie darauf, gute Methoden für die Kennwortspeicherung zu verwenden, wenn Sie Dienstprinzipalverbindungen automatisieren.

### <a name="certificate-based-authentication"></a>Zertifikatbasierte Authentifizierung

Zertifikatbasierte Authentifizierung erfordert, dass Azure PowerShell Informationen von einem lokalen Zertifikatsspeicher basierend auf einem Fingerabdruck des Zertifikats abrufen kann.

```azurepowershell-interactive
Connect-AzAccount -ApplicationId $appId -Tenant $tenantId -CertificateThumbprint <thumbprint>
```

Wenn Sie einen Dienstprinzipal anstelle einer registrierten Anwendung verwenden, fügen Sie das Argument `-ServicePrincipal` hinzu, und geben Sie die Anwendungs-ID des Dienstprinzipals als Wert für den Parameter `-ApplicationId` an.

```azurepowershell-interactive
Connect-AzAccount -ServicePrincipal -ApplicationId $servicePrincipalId -Tenant $tenantId -CertificateThumbprint <thumbprint>
```

In PowerShell 5.1 kann der Zertifikatspeicher mit den [PKI](/powershell/module/pkiclient)-Modul verwaltet und überprüft werden. Für PowerShell Core 6.x und höher ist der Prozess komplizierter. Die folgenden Skripts zeigen, wie ein vorhandenes Zertifikat in den für PowerShell zugänglichen Zertifikatspeicher importiert wird.

#### <a name="import-a-certificate-in-powershell-51"></a>Importieren eines Zertifikats in PowerShell 5.1

```azurepowershell-interactive
# Import a PFX
$credentials = Get-Credential -Message "Provide PFX private key password"
Import-PfxCertificate -FilePath <path to certificate> -Password $credentials.Password -CertStoreLocation cert:\CurrentUser\My
```

#### <a name="import-a-certificate-in-powershell-core-6x-and-later"></a>Importieren eines Zertifikats in PowerShell Core 6.x und höher

```azurepowershell-interactive
# Import a PFX
$storeName = [System.Security.Cryptography.X509Certificates.StoreName]::My
$storeLocation = [System.Security.Cryptography.X509Certificates.StoreLocation]::CurrentUser
$store = [System.Security.Cryptography.X509Certificates.X509Store]::new($storeName, $storeLocation)
$certPath = <path to certificate>
$credentials = Get-Credential -Message "Provide PFX private key password"
$flag = [System.Security.Cryptography.X509Certificates.X509KeyStorageFlags]::Exportable
$certificate = [System.Security.Cryptography.X509Certificates.X509Certificate2]::new($certPath, $credentials.Password, $flag)
$store.Open([System.Security.Cryptography.X509Certificates.OpenFlags]::ReadWrite)
$store.Add($Certificate)
$store.Close()
```

## <a name="sign-in-using-a-managed-identity"></a>Anmelden mit einer verwalteten Identität

Verwaltete Identitäten sind ein Feature von Azure Active Directory. Bei verwalteten Identitäten handelt es sich um Dienstprinzipale, die den in Azure ausgeführten Ressourcen zugewiesen sind. Sie können den Dienstprinzipal einer verwalteten Identität für die Anmeldung verwenden und ein App-exklusives Zugriffstoken für den Zugriff auf andere Ressourcen beziehen. Verwaltete Identitäten stehen nur für Ressourcen zur Verfügung, die in einer Azure-Cloud ausgeführt werden.

In diesem Beispiel wird mithilfe der verwalteten Identität der Hostumgebung eine Verbindung hergestellt. Beispiel: Bei der Ausführung auf einem virtuellen Computer (VirtualMachine) mit einer zugewiesenen verwalteten Dienstidentität wird dadurch dem Code die Anmeldung mithilfe dieser zugewiesenen Identität ermöglicht.

```azurepowershell-interactive
 Connect-AzAccount -Identity
```

## <a name="sign-in-with-a-non-default-tenant-or-as-a-cloud-solution-provider-csp"></a>Anmelden mit einem anderen Mandanten als dem Standardmandanten oder als Cloudlösungsanbieter (Cloud Solution Provider, CSP)

Wenn Ihr Konto mehr als einem Mandanten zugeordnet ist, muss bei der Verbindungsherstellung für die Anmeldung der Parameter `-Tenant` verwendet werden. Dieser Parameter funktioniert mit jedem Anmeldeverfahren. Beim Anmelden kann dieser Parameterwert entweder die Azure-Objekt-ID des Mandanten (Mandanten-ID) oder der vollqualifizierte Domänenname des Mandanten sein.

Wenn Sie ein [Cloudlösungsanbieter (Cloud Solution Provider, CSP)](https://azure.microsoft.com/offers/ms-azr-0145p/) sind, **muss** der Wert `-Tenant` eine Mandanten-ID sein.

```azurepowershell-interactive
Connect-AzAccount -Tenant 'xxxx-xxxx-xxxx-xxxx'
```

## <a name="sign-in-to-another-cloud"></a>Anmelden bei einer anderen Cloud

Azure-Clouddienste verfügen über Umgebungen, die jeweils mit den regionalen Gesetzen zum Umgang mit Daten konform sind. Legen Sie die Umgebung für Konten in einer regionalen Cloud fest, wenn Sie sich mit dem Argument `-Environment` anmelden. Dieser Parameter funktioniert mit jedem Anmeldeverfahren. Beispiel für den Fall, dass sich Ihr Konto in der Cloud in China befindet:

```azurepowershell-interactive
Connect-AzAccount -Environment AzureChinaCloud
```

Mit dem folgenden Befehl wird eine Liste mit den verfügbaren Umgebungen abgerufen:

```azurepowershell-interactive
Get-AzEnvironment | Select-Object -Property Name
```
