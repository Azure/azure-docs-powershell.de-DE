---
title: Anmelden mit Azure PowerShell
description: Es wird beschrieben, wie Sie sich mit Azure PowerShell als Benutzer, per Dienstprinzipal oder mit verwalteten Identitäten für Azure-Ressourcen anmelden.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 06/18/2020
ms.openlocfilehash: f82a9e373806f2f071ae59f6aee7e0a0bd4ea13d
ms.sourcegitcommit: 747769a143ddebff39e78c2cc62a182401adddb9
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/23/2020
ms.locfileid: "85268193"
---
# <a name="sign-in-with-azure-powershell"></a><span data-ttu-id="fa547-103">Anmelden mit Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="fa547-103">Sign in with Azure PowerShell</span></span>

<span data-ttu-id="fa547-104">Azure PowerShell unterstützt mehrere Authentifizierungsmethoden.</span><span class="sxs-lookup"><span data-stu-id="fa547-104">Azure PowerShell supports several authentication methods.</span></span> <span data-ttu-id="fa547-105">Den einfachsten Einstieg ermöglicht der [Azure Cloud Shell](/azure/cloud-shell/overview)-Dienst, der Sie automatisch anmeldet.</span><span class="sxs-lookup"><span data-stu-id="fa547-105">The easiest way to get started is with [Azure Cloud Shell](/azure/cloud-shell/overview), which automatically logs you in.</span></span> <span data-ttu-id="fa547-106">Bei einer lokalen Installation können Sie sich interaktiv über Ihren Browser anmelden.</span><span class="sxs-lookup"><span data-stu-id="fa547-106">With a local install, you can sign in interactively through your browser.</span></span> <span data-ttu-id="fa547-107">Beim Schreiben von Skripts für die Automatisierung besteht der empfohlene Ansatz darin, einen [Dienstprinzipal](create-azure-service-principal-azureps.md) mit den erforderlichen Berechtigungen zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="fa547-107">When writing scripts for automation, the recommended approach is to use a [service principal](create-azure-service-principal-azureps.md) with the necessary permissions.</span></span> <span data-ttu-id="fa547-108">Indem Sie die Anmeldeberechtigungen für Ihren Anwendungsfall so weit wie möglich einschränken, tragen Sie zur Sicherheit Ihrer Azure-Ressourcen bei.</span><span class="sxs-lookup"><span data-stu-id="fa547-108">When you restrict sign-in permissions as much as possible for your use case, you help keep your Azure resources secure.</span></span>

<span data-ttu-id="fa547-109">Nach der Anmeldung werden Befehle für Ihr Standardabonnement ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="fa547-109">After signing in, commands are run against your default subscription.</span></span> <span data-ttu-id="fa547-110">Verwenden Sie das Cmdlet [Set-AzContext](/powershell/module/az.accounts/set-azcontext), um Ihr aktives Abonnement für eine Sitzung zu ändern.</span><span class="sxs-lookup"><span data-stu-id="fa547-110">To change your active subscription for a session, use the [Set-AzContext](/powershell/module/az.accounts/set-azcontext) cmdlet.</span></span> <span data-ttu-id="fa547-111">Verwenden Sie [Set-AzDefault](/powershell/module/az.accounts/set-azdefault), um das Standardabonnement zu ändern, das beim Anmelden mit Azure PowerShell verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="fa547-111">To change the default subscription used when logging in with Azure PowerShell, use [Set-AzDefault](/powershell/module/az.accounts/set-azdefault).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="fa547-112">Ihre Anmeldeinformationen werden in mehreren PowerShell-Sitzungen gemeinsam verwendet, solange Sie angemeldet bleiben.</span><span class="sxs-lookup"><span data-stu-id="fa547-112">Your credentials are shared among multiple PowerShell sessions as long as you remain signed in.</span></span>
> <span data-ttu-id="fa547-113">Weitere Informationen finden Sie im Artikel zu [beständigen Anmeldeinformationen](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="fa547-113">For more information, see the article on [Persistent Credentials](context-persistence.md).</span></span>

## <a name="sign-in-interactively"></a><span data-ttu-id="fa547-114">Interaktives Anmelden</span><span class="sxs-lookup"><span data-stu-id="fa547-114">Sign in interactively</span></span>

<span data-ttu-id="fa547-115">Verwenden Sie für die interaktive Anmeldung das Cmdlet [Connect-AzAccount](/powershell/module/az.accounts/connect-azaccount).</span><span class="sxs-lookup"><span data-stu-id="fa547-115">To sign in interactively, use the [Connect-AzAccount](/powershell/module/az.accounts/connect-azaccount) cmdlet.</span></span>

```azurepowershell-interactive
Connect-AzAccount
```

<span data-ttu-id="fa547-116">Bei der Ausführung über PowerShell ab Version 6 zeigt dieses Cmdlet eine Tokenzeichenfolge an.</span><span class="sxs-lookup"><span data-stu-id="fa547-116">When run from PowerShell version 6 and higher, this cmdlet presents a token string.</span></span> <span data-ttu-id="fa547-117">Kopieren Sie diese Zeichenfolge, und fügen Sie sie in [microsoft.com/devicelogin](https://microsoft.com/devicelogin) in einem Webbrowser ein, um sich anzumelden.</span><span class="sxs-lookup"><span data-stu-id="fa547-117">To sign in, copy this string and paste it into [microsoft.com/devicelogin](https://microsoft.com/devicelogin) in a web browser.</span></span> <span data-ttu-id="fa547-118">Ihre PowerShell-Sitzung wird für die Verbindungsherstellung mit Azure authentifiziert.</span><span class="sxs-lookup"><span data-stu-id="fa547-118">Your PowerShell session will be authenticated to connect to Azure.</span></span> <span data-ttu-id="fa547-119">Sie können den `UseDeviceAuthentication`-Parameter angeben, um eine Tokenzeichenfolge in Windows PowerShell zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="fa547-119">You can specify the `UseDeviceAuthentication` parameter to receive a token string on Windows PowerShell.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="fa547-120">Die Autorisierung mit Anmeldeinformationen (Benutzername/Kennwort) wurde in Azure PowerShell aufgrund von Änderungen in Active Directory-Autorisierungsimplementierungen und Sicherheitsbedenken entfernt.</span><span class="sxs-lookup"><span data-stu-id="fa547-120">Username/password credential authorization has been removed in Azure PowerShell due to changes in Active Directory authorization implementations and security concerns.</span></span> <span data-ttu-id="fa547-121">Wenn Sie die Autorisierung mit Anmeldeinformationen zu Automatisierungszwecken verwenden, [erstellen Sie stattdessen einen Dienstprinzipal](create-azure-service-principal-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="fa547-121">If you use credential authorization for automation purposes, instead [create a service principal](create-azure-service-principal-azureps.md).</span></span>

<span data-ttu-id="fa547-122">Verwenden Sie das Cmdlet [Get-AzContext](/powershell/module/az.accounts/get-azcontext), um Ihre Mandanten-ID in einer Variablen zu speichern, die in den nächsten beiden Abschnitten dieses Artikels verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="fa547-122">Use the [Get-AzContext](/powershell/module/az.accounts/get-azcontext) cmdlet to store your tenant ID in a variable to be used in the next two sections of this article.</span></span>

```azurepowershell-interactive
$tenantId = (Get-AzContext).Tenant.Id
```

## <a name="sign-in-with-a-service-principal"></a><span data-ttu-id="fa547-123">Anmelden mit einem Dienstprinzipal<a name="sp-signin"/></span><span class="sxs-lookup"><span data-stu-id="fa547-123">Sign in with a service principal <a name="sp-signin"/></span></span>

<span data-ttu-id="fa547-124">Dienstprinzipale sind nicht interaktive Azure-Konten.</span><span class="sxs-lookup"><span data-stu-id="fa547-124">Service principals are non-interactive Azure accounts.</span></span> <span data-ttu-id="fa547-125">Wie bei anderen Benutzerkonten auch, werden die Berechtigungen mit Azure Active Directory verwaltet.</span><span class="sxs-lookup"><span data-stu-id="fa547-125">Like other user accounts, their permissions are managed with Azure Active Directory.</span></span> <span data-ttu-id="fa547-126">Indem für einen Dienstprinzipal nur die benötigten Berechtigungen gewährt werden, bleibt die Sicherheit Ihrer Automatisierungsskripts gewahrt.</span><span class="sxs-lookup"><span data-stu-id="fa547-126">By granting a service principal only the permissions it needs, your automation scripts stay secure.</span></span>

<span data-ttu-id="fa547-127">Informationen zur Erstellung eines Dienstprinzipals für die Verwendung mit PowerShell finden Sie unter [Erstellen eines Azure-Dienstprinzipals mit Azure PowerShell](create-azure-service-principal-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="fa547-127">To learn how to create a service principal for use with Azure PowerShell, see [Create an Azure service principal with Azure PowerShell](create-azure-service-principal-azureps.md).</span></span>

<span data-ttu-id="fa547-128">Verwenden Sie für die Anmeldung mit einem Dienstprinzipal das Cmdlet `Connect-AzAccount` mit dem Argument `-ServicePrincipal`.</span><span class="sxs-lookup"><span data-stu-id="fa547-128">To sign in with a service principal, use the `-ServicePrincipal` argument with the `Connect-AzAccount` cmdlet.</span></span> <span data-ttu-id="fa547-129">Sie benötigen auch die Anwendungs-ID und die Anmeldeinformationen des Dienstprinzipals sowie die dem Dienstprinzipal zugeordnete Mandanten-ID.</span><span class="sxs-lookup"><span data-stu-id="fa547-129">You'll also need the service principal's application ID, sign-in credentials, and the tenant ID associate with the service principal.</span></span> <span data-ttu-id="fa547-130">Wie Sie sich mit einem Dienstprinzipal anmelden, hängt davon ab, ob er für die kennwortbasierte oder die zertifikatbasierte Authentifizierung konfiguriert wurde.</span><span class="sxs-lookup"><span data-stu-id="fa547-130">How you sign in with a service principal depends on whether it's configured for password-based or certificate-based authentication.</span></span>

### <a name="password-based-authentication"></a><span data-ttu-id="fa547-131">Kennwortbasierte Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="fa547-131">Password-based authentication</span></span>

<span data-ttu-id="fa547-132">Erstellen Sie einen Dienstprinzipal für die Verwendung in den Beispielen in diesem Abschnitt.</span><span class="sxs-lookup"><span data-stu-id="fa547-132">Create a service principal to be used in the examples in this section.</span></span> <span data-ttu-id="fa547-133">Weitere Informationen zum Erstellen von Dienstprinzipalen finden Sie unter [Erstellen eines Azure-Dienstprinzipals mit Azure PowerShell](/powershell/azure/create-azure-service-principal-azureps).</span><span class="sxs-lookup"><span data-stu-id="fa547-133">For more information on creating service principals, see [Create an Azure service principal with Azure PowerShell](/powershell/azure/create-azure-service-principal-azureps).</span></span>

```azurepowershell-interactive
$sp = New-AzADServicePrincipal -DisplayName ServicePrincipalName
```

<span data-ttu-id="fa547-134">Verwenden Sie das Cmdlet [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential), um die Anmeldeinformationen des Dienstprinzipals als entsprechendes Objekt abzurufen.</span><span class="sxs-lookup"><span data-stu-id="fa547-134">To get the service principal's credentials as the appropriate object, use the [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential) cmdlet.</span></span> <span data-ttu-id="fa547-135">Mit diesem Cmdlet wird eine Eingabeaufforderung für Benutzername und Kennwort angezeigt.</span><span class="sxs-lookup"><span data-stu-id="fa547-135">This cmdlet presents a prompt for a username and password.</span></span> <span data-ttu-id="fa547-136">Verwenden Sie die `applicationID` des Dienstprinzipals für den Benutzernamen, und konvertieren Sie dessen `secret` in Nur-Text für das Kennwort.</span><span class="sxs-lookup"><span data-stu-id="fa547-136">Use the service principal's `applicationID` for the username and convert its `secret` to plain text for the password.</span></span>

```azurepowershell-interactive
# Retrieve the plain text password for use with `Get-Credential` in the next command.
$sp.secret | ConvertFrom-SecureString -AsPlainText

$pscredential = Get-Credential -UserName $sp.ApplicationId
Connect-AzAccount -ServicePrincipal -Credential $pscredential -Tenant $tenantId
```

<span data-ttu-id="fa547-137">Für Automatisierungsszenarien müssen Sie Anmeldeinformationen aus der `applicationId` und dem `secret` eines Dienstprinzipals erstellen:</span><span class="sxs-lookup"><span data-stu-id="fa547-137">For automation scenarios, you need to create credentials from a service principal's `applicationId` and `secret`:</span></span>

```azurepowershell-interactive
$pscredential = New-Object -TypeName System.Management.Automation.PSCredential($sp.ApplicationId, $sp.Secret)
Connect-AzAccount -ServicePrincipal -Credential $pscredential -Tenant $tenantId
```

<span data-ttu-id="fa547-138">Achten Sie darauf, gute Methoden für die Kennwortspeicherung zu verwenden, wenn Sie Dienstprinzipalverbindungen automatisieren.</span><span class="sxs-lookup"><span data-stu-id="fa547-138">Make sure that you use good password storage practices when automating service principal connections.</span></span>

### <a name="certificate-based-authentication"></a><span data-ttu-id="fa547-139">Zertifikatbasierte Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="fa547-139">Certificate-based authentication</span></span>

<span data-ttu-id="fa547-140">Zertifikatbasierte Authentifizierung erfordert, dass Azure PowerShell Informationen von einem lokalen Zertifikatsspeicher basierend auf einem Fingerabdruck des Zertifikats abrufen kann.</span><span class="sxs-lookup"><span data-stu-id="fa547-140">Certificate-based authentication requires that Azure PowerShell can retrieve information from a local certificate store based on a certificate thumbprint.</span></span>

```azurepowershell-interactive
Connect-AzAccount -ApplicationId $appId -Tenant $tenantId -CertificateThumbprint <thumbprint>
```

<span data-ttu-id="fa547-141">Wenn Sie einen Dienstprinzipal anstelle einer registrierten Anwendung verwenden, fügen Sie das Argument `-ServicePrincipal` hinzu, und geben Sie die Anwendungs-ID des Dienstprinzipals als Wert für den Parameter `-ApplicationId` an.</span><span class="sxs-lookup"><span data-stu-id="fa547-141">When using a service principal instead of a registered application, add the `-ServicePrincipal` argument and provide the service principal's Application ID as the `-ApplicationId` parameter's value.</span></span>

```azurepowershell-interactive
Connect-AzAccount -ServicePrincipal -ApplicationId $servicePrincipalId -Tenant $tenantId -CertificateThumbprint <thumbprint>
```

<span data-ttu-id="fa547-142">In PowerShell 5.1 kann der Zertifikatspeicher mit den [PKI](/powershell/module/pkiclient)-Modul verwaltet und überprüft werden.</span><span class="sxs-lookup"><span data-stu-id="fa547-142">In PowerShell 5.1, the certificate store can be managed and inspected with the [PKI](/powershell/module/pkiclient) module.</span></span> <span data-ttu-id="fa547-143">Für PowerShell Core 6.x und höher ist der Prozess komplizierter.</span><span class="sxs-lookup"><span data-stu-id="fa547-143">For PowerShell Core 6.x and later, the process is more complicated.</span></span> <span data-ttu-id="fa547-144">Die folgenden Skripts zeigen, wie ein vorhandenes Zertifikat in den für PowerShell zugänglichen Zertifikatspeicher importiert wird.</span><span class="sxs-lookup"><span data-stu-id="fa547-144">The following scripts show you how to import an existing certificate into the certificate store accessible by PowerShell.</span></span>

#### <a name="import-a-certificate-in-powershell-51"></a><span data-ttu-id="fa547-145">Importieren eines Zertifikats in PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="fa547-145">Import a certificate in PowerShell 5.1</span></span>

```azurepowershell-interactive
# Import a PFX
$credentials = Get-Credential -Message "Provide PFX private key password"
Import-PfxCertificate -FilePath <path to certificate> -Password $credentials.Password -CertStoreLocation cert:\CurrentUser\My
```

#### <a name="import-a-certificate-in-powershell-core-6x-and-later"></a><span data-ttu-id="fa547-146">Importieren eines Zertifikats in PowerShell Core 6.x und höher</span><span class="sxs-lookup"><span data-stu-id="fa547-146">Import a certificate in PowerShell Core 6.x and later</span></span>

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

## <a name="sign-in-using-a-managed-identity"></a><span data-ttu-id="fa547-147">Anmelden mit einer verwalteten Identität</span><span class="sxs-lookup"><span data-stu-id="fa547-147">Sign in using a managed identity</span></span>

<span data-ttu-id="fa547-148">Verwaltete Identitäten sind ein Feature von Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="fa547-148">Managed identities are a feature of Azure Active Directory.</span></span> <span data-ttu-id="fa547-149">Bei verwalteten Identitäten handelt es sich um Dienstprinzipale, die den in Azure ausgeführten Ressourcen zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="fa547-149">Managed identities are service principals assigned to resources that run in Azure.</span></span> <span data-ttu-id="fa547-150">Sie können den Dienstprinzipal einer verwalteten Identität für die Anmeldung verwenden und ein App-exklusives Zugriffstoken für den Zugriff auf andere Ressourcen beziehen.</span><span class="sxs-lookup"><span data-stu-id="fa547-150">You can use a managed identity service principal for sign-in, and acquire an app-only access token to access other resources.</span></span> <span data-ttu-id="fa547-151">Verwaltete Identitäten stehen nur für Ressourcen zur Verfügung, die in einer Azure-Cloud ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="fa547-151">Managed identities are only available on resources running in an Azure cloud.</span></span>

<span data-ttu-id="fa547-152">In diesem Beispiel wird mithilfe der verwalteten Identität der Hostumgebung eine Verbindung hergestellt.</span><span class="sxs-lookup"><span data-stu-id="fa547-152">This example connects using the managed identity of the host environment.</span></span> <span data-ttu-id="fa547-153">Beispiel: Bei der Ausführung auf einem virtuellen Computer (VirtualMachine) mit einer zugewiesenen verwalteten Dienstidentität wird dadurch dem Code die Anmeldung mithilfe dieser zugewiesenen Identität ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="fa547-153">For example, if executed on a VirtualMachine with an assigned Managed Service Identity, this allows the code to sign in using that assigned identity.</span></span>

```azurepowershell-interactive
 Connect-AzAccount -Identity
```

## <a name="sign-in-with-a-non-default-tenant-or-as-a-cloud-solution-provider-csp"></a><span data-ttu-id="fa547-154">Anmelden mit einem anderen Mandanten als dem Standardmandanten oder als Cloudlösungsanbieter (Cloud Solution Provider, CSP)</span><span class="sxs-lookup"><span data-stu-id="fa547-154">Sign in with a non-default tenant or as a Cloud Solution Provider (CSP)</span></span>

<span data-ttu-id="fa547-155">Wenn Ihr Konto mehr als einem Mandanten zugeordnet ist, muss bei der Verbindungsherstellung für die Anmeldung der Parameter `-Tenant` verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fa547-155">If your account is associated with more than one tenant, sign-in requires the `-Tenant` parameter to be specified when connecting.</span></span> <span data-ttu-id="fa547-156">Dieser Parameter funktioniert mit jedem Anmeldeverfahren.</span><span class="sxs-lookup"><span data-stu-id="fa547-156">This parameter works with any sign-in method.</span></span> <span data-ttu-id="fa547-157">Beim Anmelden kann dieser Parameterwert entweder die Azure-Objekt-ID des Mandanten (Mandanten-ID) oder der vollqualifizierte Domänenname des Mandanten sein.</span><span class="sxs-lookup"><span data-stu-id="fa547-157">When logging in, this parameter value can either be the Azure object ID of the tenant (Tenant ID) or the fully qualified domain name of the tenant.</span></span>

<span data-ttu-id="fa547-158">Wenn Sie ein [Cloudlösungsanbieter (Cloud Solution Provider, CSP)](https://azure.microsoft.com/offers/ms-azr-0145p/) sind, **muss** der Wert `-Tenant` eine Mandanten-ID sein.</span><span class="sxs-lookup"><span data-stu-id="fa547-158">If you're a [Cloud Solution Provider (CSP)](https://azure.microsoft.com/offers/ms-azr-0145p/), the `-Tenant` value **must** be a tenant ID.</span></span>

```azurepowershell-interactive
Connect-AzAccount -Tenant 'xxxx-xxxx-xxxx-xxxx'
```

## <a name="sign-in-to-another-cloud"></a><span data-ttu-id="fa547-159">Anmelden bei einer anderen Cloud</span><span class="sxs-lookup"><span data-stu-id="fa547-159">Sign in to another Cloud</span></span>

<span data-ttu-id="fa547-160">Azure-Clouddienste verfügen über Umgebungen, die jeweils mit den regionalen Gesetzen zum Umgang mit Daten konform sind.</span><span class="sxs-lookup"><span data-stu-id="fa547-160">Azure cloud services offer environments compliant with regional data-handling laws.</span></span> <span data-ttu-id="fa547-161">Legen Sie die Umgebung für Konten in einer regionalen Cloud fest, wenn Sie sich mit dem Argument `-Environment` anmelden.</span><span class="sxs-lookup"><span data-stu-id="fa547-161">For accounts in a regional cloud, set the environment when you sign in with the `-Environment` argument.</span></span> <span data-ttu-id="fa547-162">Dieser Parameter funktioniert mit jedem Anmeldeverfahren.</span><span class="sxs-lookup"><span data-stu-id="fa547-162">This parameter works with any sign-in method.</span></span> <span data-ttu-id="fa547-163">Beispiel für den Fall, dass sich Ihr Konto in der Cloud in China befindet:</span><span class="sxs-lookup"><span data-stu-id="fa547-163">For example, if your account is in the China cloud:</span></span>

```azurepowershell-interactive
Connect-AzAccount -Environment AzureChinaCloud
```

<span data-ttu-id="fa547-164">Mit dem folgenden Befehl wird eine Liste mit den verfügbaren Umgebungen abgerufen:</span><span class="sxs-lookup"><span data-stu-id="fa547-164">The following command gets a list of available environments:</span></span>

```azurepowershell-interactive
Get-AzEnvironment | Select-Object -Property Name
```
