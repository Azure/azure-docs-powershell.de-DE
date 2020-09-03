---
title: Anmelden mit Azure PowerShell
description: Es wird beschrieben, wie Sie sich mit Azure PowerShell als Benutzer, per Dienstprinzipal oder mit verwalteten Identitäten für Azure-Ressourcen anmelden.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 7/7/2020
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 8f18af8ed67ecf2aefd353208c07bf812df732d9
ms.sourcegitcommit: 8b3126b5c79f453464d90669f0046ba86b7a3424
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/01/2020
ms.locfileid: "89239893"
---
# <a name="sign-in-with-azure-powershell"></a><span data-ttu-id="76b8e-103">Anmelden mit Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="76b8e-103">Sign in with Azure PowerShell</span></span>

<span data-ttu-id="76b8e-104">Azure PowerShell unterstützt mehrere Authentifizierungsmethoden.</span><span class="sxs-lookup"><span data-stu-id="76b8e-104">Azure PowerShell supports several authentication methods.</span></span> <span data-ttu-id="76b8e-105">Den einfachsten Einstieg ermöglicht der [Azure Cloud Shell](/azure/cloud-shell/overview)-Dienst, der Sie automatisch anmeldet.</span><span class="sxs-lookup"><span data-stu-id="76b8e-105">The easiest way to get started is with [Azure Cloud Shell](/azure/cloud-shell/overview), which automatically logs you in.</span></span> <span data-ttu-id="76b8e-106">Bei einer lokalen Installation können Sie sich interaktiv über Ihren Browser anmelden.</span><span class="sxs-lookup"><span data-stu-id="76b8e-106">With a local install, you can sign in interactively through your browser.</span></span> <span data-ttu-id="76b8e-107">Beim Schreiben von Skripts für die Automatisierung besteht der empfohlene Ansatz darin, einen [Dienstprinzipal](create-azure-service-principal-azureps.md) mit den erforderlichen Berechtigungen zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="76b8e-107">When writing scripts for automation, the recommended approach is to use a [service principal](create-azure-service-principal-azureps.md) with the necessary permissions.</span></span> <span data-ttu-id="76b8e-108">Indem Sie die Anmeldeberechtigungen für Ihren Anwendungsfall so weit wie möglich einschränken, tragen Sie zur Sicherheit Ihrer Azure-Ressourcen bei.</span><span class="sxs-lookup"><span data-stu-id="76b8e-108">When you restrict sign-in permissions as much as possible for your use case, you help keep your Azure resources secure.</span></span>

<span data-ttu-id="76b8e-109">Zunächst sind Sie beim ersten Abonnement angemeldet, das von Azure zurückgegeben wird, wenn Sie Zugriff auf mehrere Abonnements haben.</span><span class="sxs-lookup"><span data-stu-id="76b8e-109">Initially, you're signed into the first subscription Azure returns if you have access to more than one subscription.</span></span> <span data-ttu-id="76b8e-110">Befehle werden für dieses Abonnement standardmäßig ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="76b8e-110">Commands are run against this subscription by default.</span></span> <span data-ttu-id="76b8e-111">Verwenden Sie das Cmdlet [Set-AzContext](/powershell/module/az.accounts/set-azcontext), um Ihr aktives Abonnement für eine Sitzung zu ändern.</span><span class="sxs-lookup"><span data-stu-id="76b8e-111">To change your active subscription for a session, use the [Set-AzContext](/powershell/module/az.accounts/set-azcontext) cmdlet.</span></span> <span data-ttu-id="76b8e-112">Um Ihr aktives Abonnement zu ändern und es zwischen Sitzungen auf demselben System beizubehalten, verwenden Sie das Cmdlet [Select-AzContext](/powershell/module/az.accounts/select-azcontext).</span><span class="sxs-lookup"><span data-stu-id="76b8e-112">To change your active subscription and have it persist between sessions on the same system, use the [Select-AzContext](/powershell/module/az.accounts/select-azcontext) cmdlet.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="76b8e-113">Ihre Anmeldeinformationen werden in mehreren PowerShell-Sitzungen gemeinsam verwendet, solange Sie angemeldet bleiben.</span><span class="sxs-lookup"><span data-stu-id="76b8e-113">Your credentials are shared among multiple PowerShell sessions as long as you remain signed in.</span></span>
> <span data-ttu-id="76b8e-114">Weitere Informationen finden Sie im Artikel zu [beständigen Anmeldeinformationen](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="76b8e-114">For more information, see the article on [Persistent Credentials](context-persistence.md).</span></span>

## <a name="sign-in-interactively"></a><span data-ttu-id="76b8e-115">Interaktives Anmelden</span><span class="sxs-lookup"><span data-stu-id="76b8e-115">Sign in interactively</span></span>

<span data-ttu-id="76b8e-116">Verwenden Sie für die interaktive Anmeldung das Cmdlet [Connect-AzAccount](/powershell/module/az.accounts/connect-azaccount).</span><span class="sxs-lookup"><span data-stu-id="76b8e-116">To sign in interactively, use the [Connect-AzAccount](/powershell/module/az.accounts/connect-azaccount) cmdlet.</span></span>

```azurepowershell-interactive
Connect-AzAccount
```

<span data-ttu-id="76b8e-117">Bei der Ausführung über PowerShell ab Version 6 zeigt dieses Cmdlet eine Tokenzeichenfolge an.</span><span class="sxs-lookup"><span data-stu-id="76b8e-117">When run from PowerShell version 6 and higher, this cmdlet presents a token string.</span></span> <span data-ttu-id="76b8e-118">Kopieren Sie diese Zeichenfolge, und fügen Sie sie in [microsoft.com/devicelogin](https://microsoft.com/devicelogin) in einem Webbrowser ein, um sich anzumelden.</span><span class="sxs-lookup"><span data-stu-id="76b8e-118">To sign in, copy this string and paste it into [microsoft.com/devicelogin](https://microsoft.com/devicelogin) in a web browser.</span></span> <span data-ttu-id="76b8e-119">Ihre PowerShell-Sitzung wird für die Verbindungsherstellung mit Azure authentifiziert.</span><span class="sxs-lookup"><span data-stu-id="76b8e-119">Your PowerShell session will be authenticated to connect to Azure.</span></span> <span data-ttu-id="76b8e-120">Sie können den `UseDeviceAuthentication`-Parameter angeben, um eine Tokenzeichenfolge in Windows PowerShell zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="76b8e-120">You can specify the `UseDeviceAuthentication` parameter to receive a token string on Windows PowerShell.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="76b8e-121">Die Autorisierung mit Anmeldeinformationen (Benutzername/Kennwort) wurde in Azure PowerShell aufgrund von Änderungen in Active Directory-Autorisierungsimplementierungen und Sicherheitsbedenken entfernt.</span><span class="sxs-lookup"><span data-stu-id="76b8e-121">Username/password credential authorization has been removed in Azure PowerShell due to changes in Active Directory authorization implementations and security concerns.</span></span> <span data-ttu-id="76b8e-122">Wenn Sie die Autorisierung mit Anmeldeinformationen zu Automatisierungszwecken verwenden, [erstellen Sie stattdessen einen Dienstprinzipal](create-azure-service-principal-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="76b8e-122">If you use credential authorization for automation purposes, instead [create a service principal](create-azure-service-principal-azureps.md).</span></span>

<span data-ttu-id="76b8e-123">Verwenden Sie das Cmdlet [Get-AzContext](/powershell/module/az.accounts/get-azcontext), um Ihre Mandanten-ID in einer Variablen zu speichern, die in den nächsten beiden Abschnitten dieses Artikels verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="76b8e-123">Use the [Get-AzContext](/powershell/module/az.accounts/get-azcontext) cmdlet to store your tenant ID in a variable to be used in the next two sections of this article.</span></span>

```azurepowershell-interactive
$tenantId = (Get-AzContext).Tenant.Id
```

## <a name="sign-in-with-a-service-principal"></a><span data-ttu-id="76b8e-124">Anmelden mit einem Dienstprinzipal<a name="sp-signin"/></span><span class="sxs-lookup"><span data-stu-id="76b8e-124">Sign in with a service principal <a name="sp-signin"/></span></span>

<span data-ttu-id="76b8e-125">Dienstprinzipale sind nicht interaktive Azure-Konten.</span><span class="sxs-lookup"><span data-stu-id="76b8e-125">Service principals are non-interactive Azure accounts.</span></span> <span data-ttu-id="76b8e-126">Wie bei anderen Benutzerkonten auch, werden die Berechtigungen mit Azure Active Directory verwaltet.</span><span class="sxs-lookup"><span data-stu-id="76b8e-126">Like other user accounts, their permissions are managed with Azure Active Directory.</span></span> <span data-ttu-id="76b8e-127">Indem für einen Dienstprinzipal nur die benötigten Berechtigungen gewährt werden, bleibt die Sicherheit Ihrer Automatisierungsskripts gewahrt.</span><span class="sxs-lookup"><span data-stu-id="76b8e-127">By granting a service principal only the permissions it needs, your automation scripts stay secure.</span></span>

<span data-ttu-id="76b8e-128">Informationen zur Erstellung eines Dienstprinzipals für die Verwendung mit PowerShell finden Sie unter [Erstellen eines Azure-Dienstprinzipals mit Azure PowerShell](create-azure-service-principal-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="76b8e-128">To learn how to create a service principal for use with Azure PowerShell, see [Create an Azure service principal with Azure PowerShell](create-azure-service-principal-azureps.md).</span></span>

<span data-ttu-id="76b8e-129">Verwenden Sie für die Anmeldung mit einem Dienstprinzipal das Cmdlet `Connect-AzAccount` mit dem Argument `-ServicePrincipal`.</span><span class="sxs-lookup"><span data-stu-id="76b8e-129">To sign in with a service principal, use the `-ServicePrincipal` argument with the `Connect-AzAccount` cmdlet.</span></span> <span data-ttu-id="76b8e-130">Sie benötigen auch die Anwendungs-ID und die Anmeldeinformationen des Dienstprinzipals sowie die dem Dienstprinzipal zugeordnete Mandanten-ID.</span><span class="sxs-lookup"><span data-stu-id="76b8e-130">You'll also need the service principal's application ID, sign-in credentials, and the tenant ID associate with the service principal.</span></span> <span data-ttu-id="76b8e-131">Wie Sie sich mit einem Dienstprinzipal anmelden, hängt davon ab, ob er für die kennwortbasierte oder die zertifikatbasierte Authentifizierung konfiguriert wurde.</span><span class="sxs-lookup"><span data-stu-id="76b8e-131">How you sign in with a service principal depends on whether it's configured for password-based or certificate-based authentication.</span></span>

### <a name="password-based-authentication"></a><span data-ttu-id="76b8e-132">Kennwortbasierte Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="76b8e-132">Password-based authentication</span></span>

<span data-ttu-id="76b8e-133">Erstellen Sie einen Dienstprinzipal für die Verwendung in den Beispielen in diesem Abschnitt.</span><span class="sxs-lookup"><span data-stu-id="76b8e-133">Create a service principal to be used in the examples in this section.</span></span> <span data-ttu-id="76b8e-134">Weitere Informationen zum Erstellen von Dienstprinzipalen finden Sie unter [Erstellen eines Azure-Dienstprinzipals mit Azure PowerShell](/powershell/azure/create-azure-service-principal-azureps).</span><span class="sxs-lookup"><span data-stu-id="76b8e-134">For more information on creating service principals, see [Create an Azure service principal with Azure PowerShell](/powershell/azure/create-azure-service-principal-azureps).</span></span>

```azurepowershell-interactive
$sp = New-AzADServicePrincipal -DisplayName ServicePrincipalName
```

<span data-ttu-id="76b8e-135">Verwenden Sie das Cmdlet [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential), um die Anmeldeinformationen des Dienstprinzipals als entsprechendes Objekt abzurufen.</span><span class="sxs-lookup"><span data-stu-id="76b8e-135">To get the service principal's credentials as the appropriate object, use the [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential) cmdlet.</span></span> <span data-ttu-id="76b8e-136">Mit diesem Cmdlet wird eine Eingabeaufforderung für Benutzername und Kennwort angezeigt.</span><span class="sxs-lookup"><span data-stu-id="76b8e-136">This cmdlet presents a prompt for a username and password.</span></span> <span data-ttu-id="76b8e-137">Verwenden Sie die `applicationID` des Dienstprinzipals für den Benutzernamen, und konvertieren Sie dessen `secret` in Nur-Text für das Kennwort.</span><span class="sxs-lookup"><span data-stu-id="76b8e-137">Use the service principal's `applicationID` for the username and convert its `secret` to plain text for the password.</span></span>

```azurepowershell-interactive
# Retrieve the plain text password for use with `Get-Credential` in the next command.
$sp.secret | ConvertFrom-SecureString -AsPlainText

$pscredential = Get-Credential -UserName $sp.ApplicationId
Connect-AzAccount -ServicePrincipal -Credential $pscredential -Tenant $tenantId
```

<span data-ttu-id="76b8e-138">Für Automatisierungsszenarien müssen Sie Anmeldeinformationen aus der `applicationId` und dem `secret` eines Dienstprinzipals erstellen:</span><span class="sxs-lookup"><span data-stu-id="76b8e-138">For automation scenarios, you need to create credentials from a service principal's `applicationId` and `secret`:</span></span>

```azurepowershell-interactive
$pscredential = New-Object -TypeName System.Management.Automation.PSCredential($sp.ApplicationId, $sp.Secret)
Connect-AzAccount -ServicePrincipal -Credential $pscredential -Tenant $tenantId
```

<span data-ttu-id="76b8e-139">Achten Sie darauf, gute Methoden für die Kennwortspeicherung zu verwenden, wenn Sie Dienstprinzipalverbindungen automatisieren.</span><span class="sxs-lookup"><span data-stu-id="76b8e-139">Make sure that you use good password storage practices when automating service principal connections.</span></span>

### <a name="certificate-based-authentication"></a><span data-ttu-id="76b8e-140">Zertifikatbasierte Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="76b8e-140">Certificate-based authentication</span></span>

<span data-ttu-id="76b8e-141">Zertifikatbasierte Authentifizierung erfordert, dass Azure PowerShell Informationen von einem lokalen Zertifikatsspeicher basierend auf einem Fingerabdruck des Zertifikats abrufen kann.</span><span class="sxs-lookup"><span data-stu-id="76b8e-141">Certificate-based authentication requires that Azure PowerShell can retrieve information from a local certificate store based on a certificate thumbprint.</span></span>

```azurepowershell-interactive
Connect-AzAccount -ApplicationId $appId -Tenant $tenantId -CertificateThumbprint <thumbprint>
```

<span data-ttu-id="76b8e-142">Wenn Sie einen Dienstprinzipal anstelle einer registrierten Anwendung verwenden, fügen Sie das Argument `-ServicePrincipal` hinzu, und geben Sie die Anwendungs-ID des Dienstprinzipals als Wert für den Parameter `-ApplicationId` an.</span><span class="sxs-lookup"><span data-stu-id="76b8e-142">When using a service principal instead of a registered application, add the `-ServicePrincipal` argument and provide the service principal's Application ID as the `-ApplicationId` parameter's value.</span></span>

```azurepowershell-interactive
Connect-AzAccount -ServicePrincipal -ApplicationId $servicePrincipalId -Tenant $tenantId -CertificateThumbprint <thumbprint>
```

<span data-ttu-id="76b8e-143">In PowerShell 5.1 kann der Zertifikatspeicher mit den [PKI](/powershell/module/pkiclient)-Modul verwaltet und überprüft werden.</span><span class="sxs-lookup"><span data-stu-id="76b8e-143">In PowerShell 5.1, the certificate store can be managed and inspected with the [PKI](/powershell/module/pkiclient) module.</span></span> <span data-ttu-id="76b8e-144">Für PowerShell Core 6.x und höher ist der Prozess komplizierter.</span><span class="sxs-lookup"><span data-stu-id="76b8e-144">For PowerShell Core 6.x and later, the process is more complicated.</span></span> <span data-ttu-id="76b8e-145">Die folgenden Skripts zeigen, wie ein vorhandenes Zertifikat in den für PowerShell zugänglichen Zertifikatspeicher importiert wird.</span><span class="sxs-lookup"><span data-stu-id="76b8e-145">The following scripts show you how to import an existing certificate into the certificate store accessible by PowerShell.</span></span>

#### <a name="import-a-certificate-in-powershell-51"></a><span data-ttu-id="76b8e-146">Importieren eines Zertifikats in PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="76b8e-146">Import a certificate in PowerShell 5.1</span></span>

```azurepowershell-interactive
# Import a PFX
$credentials = Get-Credential -Message "Provide PFX private key password"
Import-PfxCertificate -FilePath <path to certificate> -Password $credentials.Password -CertStoreLocation cert:\CurrentUser\My
```

#### <a name="import-a-certificate-in-powershell-core-6x-and-later"></a><span data-ttu-id="76b8e-147">Importieren eines Zertifikats in PowerShell Core 6.x und höher</span><span class="sxs-lookup"><span data-stu-id="76b8e-147">Import a certificate in PowerShell Core 6.x and later</span></span>

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

## <a name="sign-in-using-a-managed-identity"></a><span data-ttu-id="76b8e-148">Anmelden mit einer verwalteten Identität</span><span class="sxs-lookup"><span data-stu-id="76b8e-148">Sign in using a managed identity</span></span>

<span data-ttu-id="76b8e-149">Verwaltete Identitäten sind ein Feature von Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="76b8e-149">Managed identities are a feature of Azure Active Directory.</span></span> <span data-ttu-id="76b8e-150">Bei verwalteten Identitäten handelt es sich um Dienstprinzipale, die den in Azure ausgeführten Ressourcen zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="76b8e-150">Managed identities are service principals assigned to resources that run in Azure.</span></span> <span data-ttu-id="76b8e-151">Sie können den Dienstprinzipal einer verwalteten Identität für die Anmeldung verwenden und ein App-exklusives Zugriffstoken für den Zugriff auf andere Ressourcen beziehen.</span><span class="sxs-lookup"><span data-stu-id="76b8e-151">You can use a managed identity service principal for sign-in, and acquire an app-only access token to access other resources.</span></span> <span data-ttu-id="76b8e-152">Verwaltete Identitäten stehen nur für Ressourcen zur Verfügung, die in einer Azure-Cloud ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="76b8e-152">Managed identities are only available on resources running in an Azure cloud.</span></span>

<span data-ttu-id="76b8e-153">In diesem Beispiel wird mithilfe der verwalteten Identität der Hostumgebung eine Verbindung hergestellt.</span><span class="sxs-lookup"><span data-stu-id="76b8e-153">This example connects using the managed identity of the host environment.</span></span> <span data-ttu-id="76b8e-154">Beispiel: Bei der Ausführung auf einem virtuellen Computer (VirtualMachine) mit einer zugewiesenen verwalteten Dienstidentität wird dadurch dem Code die Anmeldung mithilfe dieser zugewiesenen Identität ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="76b8e-154">For example, if executed on a VirtualMachine with an assigned Managed Service Identity, this allows the code to sign in using that assigned identity.</span></span>

```azurepowershell-interactive
 Connect-AzAccount -Identity
```

## <a name="sign-in-with-a-non-default-tenant-or-as-a-cloud-solution-provider-csp"></a><span data-ttu-id="76b8e-155">Anmelden mit einem anderen Mandanten als dem Standardmandanten oder als Cloudlösungsanbieter (Cloud Solution Provider, CSP)</span><span class="sxs-lookup"><span data-stu-id="76b8e-155">Sign in with a non-default tenant or as a Cloud Solution Provider (CSP)</span></span>

<span data-ttu-id="76b8e-156">Wenn Ihr Konto mehr als einem Mandanten zugeordnet ist, muss bei der Verbindungsherstellung für die Anmeldung der Parameter `-Tenant` verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="76b8e-156">If your account is associated with more than one tenant, sign-in requires the `-Tenant` parameter to be specified when connecting.</span></span> <span data-ttu-id="76b8e-157">Dieser Parameter funktioniert mit jedem Anmeldeverfahren.</span><span class="sxs-lookup"><span data-stu-id="76b8e-157">This parameter works with any sign-in method.</span></span> <span data-ttu-id="76b8e-158">Beim Anmelden kann dieser Parameterwert entweder die Azure-Objekt-ID des Mandanten (Mandanten-ID) oder der vollqualifizierte Domänenname des Mandanten sein.</span><span class="sxs-lookup"><span data-stu-id="76b8e-158">When logging in, this parameter value can either be the Azure object ID of the tenant (Tenant ID) or the fully qualified domain name of the tenant.</span></span>

<span data-ttu-id="76b8e-159">Wenn Sie ein [Cloudlösungsanbieter (Cloud Solution Provider, CSP)](https://azure.microsoft.com/offers/ms-azr-0145p/) sind, **muss** der Wert `-Tenant` eine Mandanten-ID sein.</span><span class="sxs-lookup"><span data-stu-id="76b8e-159">If you're a [Cloud Solution Provider (CSP)](https://azure.microsoft.com/offers/ms-azr-0145p/), the `-Tenant` value **must** be a tenant ID.</span></span>

```azurepowershell-interactive
Connect-AzAccount -Tenant 'xxxx-xxxx-xxxx-xxxx'
```

## <a name="sign-in-to-another-cloud"></a><span data-ttu-id="76b8e-160">Anmelden bei einer anderen Cloud</span><span class="sxs-lookup"><span data-stu-id="76b8e-160">Sign in to another Cloud</span></span>

<span data-ttu-id="76b8e-161">Azure-Clouddienste verfügen über Umgebungen, die jeweils mit den regionalen Gesetzen zum Umgang mit Daten konform sind.</span><span class="sxs-lookup"><span data-stu-id="76b8e-161">Azure cloud services offer environments compliant with regional data-handling laws.</span></span> <span data-ttu-id="76b8e-162">Legen Sie die Umgebung für Konten in einer regionalen Cloud fest, wenn Sie sich mit dem Argument `-Environment` anmelden.</span><span class="sxs-lookup"><span data-stu-id="76b8e-162">For accounts in a regional cloud, set the environment when you sign in with the `-Environment` argument.</span></span> <span data-ttu-id="76b8e-163">Dieser Parameter funktioniert mit jedem Anmeldeverfahren.</span><span class="sxs-lookup"><span data-stu-id="76b8e-163">This parameter works with any sign-in method.</span></span> <span data-ttu-id="76b8e-164">Beispiel für den Fall, dass sich Ihr Konto in der Cloud in China befindet:</span><span class="sxs-lookup"><span data-stu-id="76b8e-164">For example, if your account is in the China cloud:</span></span>

```azurepowershell-interactive
Connect-AzAccount -Environment AzureChinaCloud
```

<span data-ttu-id="76b8e-165">Mit dem folgenden Befehl wird eine Liste mit den verfügbaren Umgebungen abgerufen:</span><span class="sxs-lookup"><span data-stu-id="76b8e-165">The following command gets a list of available environments:</span></span>

```azurepowershell-interactive
Get-AzEnvironment | Select-Object -Property Name
```
