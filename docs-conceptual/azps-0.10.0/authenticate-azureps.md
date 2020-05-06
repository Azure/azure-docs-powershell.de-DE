---
title: Anmelden mit Azure PowerShell
description: Es wird beschrieben, wie Sie sich mit Azure PowerShell als Benutzer, per Dienstprinzipal oder mit verwalteten Identitäten für Azure-Ressourcen anmelden.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/04/2019
ms.openlocfilehash: 0de487cc34593ceac05aa2077358d692470dc23e
ms.sourcegitcommit: d661f38bec34e65bf73913db59028e11fd78b131
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/05/2020
ms.locfileid: "81445797"
---
# <a name="sign-in-with-azure-powershell"></a><span data-ttu-id="57271-103">Anmelden mit Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="57271-103">Sign in with Azure PowerShell</span></span>

<span data-ttu-id="57271-104">Azure PowerShell unterstützt mehrere Authentifizierungsmethoden.</span><span class="sxs-lookup"><span data-stu-id="57271-104">Azure PowerShell supports several authentication methods.</span></span> <span data-ttu-id="57271-105">Den einfachsten Einstieg ermöglicht der [Azure Cloud Shell](/azure/cloud-shell/overview)-Dienst, der Sie automatisch anmeldet.</span><span class="sxs-lookup"><span data-stu-id="57271-105">The easiest way to get started is with [Azure Cloud Shell](/azure/cloud-shell/overview), which automatically logs you in.</span></span> <span data-ttu-id="57271-106">Bei einer lokalen Installation können Sie sich interaktiv über Ihren Browser anmelden.</span><span class="sxs-lookup"><span data-stu-id="57271-106">With a local install, you can sign in interactively through your browser.</span></span> <span data-ttu-id="57271-107">Beim Schreiben von Skripts für die Automatisierung besteht der empfohlene Ansatz darin, einen [Dienstprinzipal](create-azure-service-principal-azureps.md) mit den erforderlichen Berechtigungen zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="57271-107">When writing scripts for automation, the recommended approach is to use a [service principal](create-azure-service-principal-azureps.md) with the necessary permissions.</span></span> <span data-ttu-id="57271-108">Indem Sie die Anmeldeberechtigungen für Ihren Anwendungsfall so weit wie möglich einschränken, tragen Sie zur Sicherheit Ihrer Azure-Ressourcen bei.</span><span class="sxs-lookup"><span data-stu-id="57271-108">When you restrict sign-in permissions as much as possible for your use case, you help keep your Azure resources secure.</span></span>

<span data-ttu-id="57271-109">Nach der Anmeldung werden Befehle für Ihr Standardabonnement ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="57271-109">After signing in, commands are run against your default subscription.</span></span> <span data-ttu-id="57271-110">Verwenden Sie das Cmdlet [Set-AzContext](/powershell/module/az.accounts/set-azcontext), um Ihr aktives Abonnement für eine Sitzung zu ändern.</span><span class="sxs-lookup"><span data-stu-id="57271-110">To change your active subscription for a session, use the [Set-AzContext](/powershell/module/az.accounts/set-azcontext) cmdlet.</span></span> <span data-ttu-id="57271-111">Verwenden Sie [Set-AzDefault](/powershell/module/az.accounts/set-azdefault), um das Standardabonnement zu ändern, das beim Anmelden mit Azure PowerShell verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="57271-111">To change the default subscription used when logging in with Azure PowerShell, use [Set-AzDefault](/powershell/module/az.accounts/set-azdefault).</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="57271-112">Ihre Anmeldeinformationen werden in mehreren PowerShell-Sitzungen gemeinsam verwendet, solange Sie angemeldet bleiben.</span><span class="sxs-lookup"><span data-stu-id="57271-112">Your credentials are shared among multiple PowerShell sessions as long as you remain signed in.</span></span>
> <span data-ttu-id="57271-113">Weitere Informationen finden Sie im Artikel zu [beständigen Anmeldeinformationen](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="57271-113">For more information, see the article on [Persistent Credentials](context-persistence.md).</span></span>

## <a name="sign-in-interactively"></a><span data-ttu-id="57271-114">Interaktives Anmelden</span><span class="sxs-lookup"><span data-stu-id="57271-114">Sign in interactively</span></span>

<span data-ttu-id="57271-115">Verwenden Sie für die interaktive Anmeldung das Cmdlet [Connect-AzAccount](/powershell/module/az.accounts/connect-azaccount).</span><span class="sxs-lookup"><span data-stu-id="57271-115">To sign in interactively, use the [Connect-AzAccount](/powershell/module/az.accounts/connect-azaccount) cmdlet.</span></span>

```azurepowershell-interactive
Connect-AzAccount
```

<span data-ttu-id="57271-116">Bei der Ausführung wird von diesem Cmdlet eine Tokenzeichenfolge bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="57271-116">When run, this cmdlet will present a token string.</span></span> <span data-ttu-id="57271-117">Kopieren Sie diese Zeichenfolge, und fügen Sie sie in einem Browser unter https://microsoft.com/devicelogin ein, um sich anzumelden.</span><span class="sxs-lookup"><span data-stu-id="57271-117">To sign in, copy this string and paste it into https://microsoft.com/devicelogin in a browser.</span></span> <span data-ttu-id="57271-118">Ihre PowerShell-Sitzung wird für die Verbindungsherstellung mit Azure authentifiziert.</span><span class="sxs-lookup"><span data-stu-id="57271-118">Your PowerShell session will be authenticated to connect to Azure.</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="57271-119">Die Autorisierung mit Anmeldeinformationen (Benutzername/Kennwort) wurde in Azure PowerShell aufgrund von Änderungen in Active Directory-Autorisierungsimplementierungen und Sicherheitsbedenken entfernt.</span><span class="sxs-lookup"><span data-stu-id="57271-119">Username/password credential authorization has been removed in Azure PowerShell due to changes in Active Directory authorization implementations and security concerns.</span></span>
> <span data-ttu-id="57271-120">Wenn Sie die Autorisierung mit Anmeldeinformationen zu Automatisierungszwecken verwenden, [erstellen Sie stattdessen einen Dienstprinzipal](create-azure-service-principal-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="57271-120">If you use credential authorization for automation purposes, instead [create a service principal](create-azure-service-principal-azureps.md).</span></span>

## <a name="sign-in-with-a-service-principal"></a><span data-ttu-id="57271-121">Anmelden mit einem Dienstprinzipal<a name="sp-signin"/></span><span class="sxs-lookup"><span data-stu-id="57271-121">Sign in with a service principal <a name="sp-signin"/></span></span>

<span data-ttu-id="57271-122">Dienstprinzipale sind nicht interaktive Azure-Konten.</span><span class="sxs-lookup"><span data-stu-id="57271-122">Service principals are non-interactive Azure accounts.</span></span> <span data-ttu-id="57271-123">Wie bei anderen Benutzerkonten auch, werden die Berechtigungen mit Azure Active Directory verwaltet.</span><span class="sxs-lookup"><span data-stu-id="57271-123">Like other user accounts, their permissions are managed with Azure Active Directory.</span></span> <span data-ttu-id="57271-124">Indem für einen Dienstprinzipal nur die benötigten Berechtigungen gewährt werden, bleibt die Sicherheit Ihrer Automatisierungsskripts gewahrt.</span><span class="sxs-lookup"><span data-stu-id="57271-124">By granting a service principal only the permissions it needs, your automation scripts stay secure.</span></span>

<span data-ttu-id="57271-125">Informationen zur Erstellung eines Dienstprinzipals für die Verwendung mit PowerShell finden Sie unter [Erstellen eines Azure-Dienstprinzipals mit Azure PowerShell](create-azure-service-principal-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="57271-125">To learn how to create a service principal for use with Azure PowerShell, see [Create an Azure service principal with Azure PowerShell](create-azure-service-principal-azureps.md).</span></span>

<span data-ttu-id="57271-126">Verwenden Sie für die Anmeldung mit einem Dienstprinzipal das Cmdlet `-ServicePrincipal` mit dem Argument `Connect-AzAccount`.</span><span class="sxs-lookup"><span data-stu-id="57271-126">To sign in with a service principal, use the `-ServicePrincipal` argument with the `Connect-AzAccount` cmdlet.</span></span> <span data-ttu-id="57271-127">Sie benötigen auch die Anwendungs-ID und die Anmeldeinformationen des Dienstprinzipals sowie die dem Dienstprinzipal zugeordnete Mandanten-ID.</span><span class="sxs-lookup"><span data-stu-id="57271-127">You'll also need the service principal's application ID, sign-in credentials, and the tenant ID associate with the service principal.</span></span> <span data-ttu-id="57271-128">Wie Sie sich mit einem Dienstprinzipal anmelden, hängt davon ab, ob er für die kennwortbasierte oder die zertifikatbasierte Authentifizierung konfiguriert wurde.</span><span class="sxs-lookup"><span data-stu-id="57271-128">How you sign in with a service principal will depend on whether it's configured for password-based or certificate-based authentication.</span></span>

### <a name="password-based-authentication"></a><span data-ttu-id="57271-129">Kennwortbasierte Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="57271-129">Password-based authentication</span></span>

<span data-ttu-id="57271-130">Verwenden Sie das Cmdlet [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential), um die Anmeldeinformationen des Dienstprinzipals als entsprechendes Objekt abzurufen.</span><span class="sxs-lookup"><span data-stu-id="57271-130">To get the service principal's credentials as the appropriate object, use the [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential) cmdlet.</span></span> <span data-ttu-id="57271-131">Mit diesem Cmdlet wird eine Eingabeaufforderung für Benutzername und Kennwort angezeigt.</span><span class="sxs-lookup"><span data-stu-id="57271-131">This cmdlet will present a prompt for a username and password.</span></span> <span data-ttu-id="57271-132">Verwenden Sie die Dienstprinzipal-ID als Benutzernamen.</span><span class="sxs-lookup"><span data-stu-id="57271-132">Use the service principal ID for the username.</span></span>

```azurepowershell-interactive
$pscredential = Get-Credential
Connect-AzAccount -ServicePrincipal -Credential $pscredential -Tenant $tenantId
```

<span data-ttu-id="57271-133">Für Automatisierungsszenarien müssen Sie Anmeldeinformationen aus einem Benutzernamen und einer sicheren Zeichenfolge erstellen:</span><span class="sxs-lookup"><span data-stu-id="57271-133">For automation scenarios, you need to create credentials from a user name and secure string:</span></span>

```azurepowershell-interactive
$passwd = ConvertTo-SecureString <use a secure password here> -AsPlainText -Force
$pscredential = New-Object System.Management.Automation.PSCredential('service principal name/id', $passwd)
Connect-AzAccount -ServicePrincipal -Credential $pscredential -Tenant $tenantId
```

<span data-ttu-id="57271-134">Achten Sie darauf, gute Methoden für die Kennwortspeicherung zu verwenden, wenn Sie Dienstprinzipalverbindungen automatisieren.</span><span class="sxs-lookup"><span data-stu-id="57271-134">Make sure that you use good password storage practices when automating service principal connections.</span></span>

### <a name="certificate-based-authentication"></a><span data-ttu-id="57271-135">Zertifikatbasierte Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="57271-135">Certificate-based authentication</span></span>

<span data-ttu-id="57271-136">Zertifikatbasierte Authentifizierung erfordert, dass Azure PowerShell Informationen von einem lokalen Zertifikatsspeicher basierend auf einem Fingerabdruck des Zertifikats abrufen kann.</span><span class="sxs-lookup"><span data-stu-id="57271-136">Certificate-based authentication requires that Azure PowerShell can retrieve information from a local certificate store based on a certificate thumbprint.</span></span>

```azurepowershell-interactive
Connect-AzAccount -ApplicationId $appId -Tenant $tenantId -CertificateThumbprint <thumbprint>
```

<span data-ttu-id="57271-137">Wenn Sie einen Dienstprinzipal anstelle einer registrierten Anwendung verwenden, fügen Sie das Argument `-ServicePrincipal` hinzu, und geben Sie die Anwendungs-ID des Dienstprinzipals als Wert für den Parameter `-ApplicationId` an.</span><span class="sxs-lookup"><span data-stu-id="57271-137">When using a service principal instead of a registered application, add the `-ServicePrincipal` argument and provide the service principal's Application ID as the `-ApplicationId` parameter's value.</span></span>

```azurepowershell-interactive
Connect-AzAccount -ServicePrincipal -ApplicationId $servicePrincipalId -Tenant $tenantId -CertificateThumbprint <thumbprint>
```

<span data-ttu-id="57271-138">In PowerShell 5.1 kann der Zertifikatspeicher mit den [PKI](/powershell/module/pkiclient)-Modul verwaltet und überprüft werden.</span><span class="sxs-lookup"><span data-stu-id="57271-138">In PowerShell 5.1, the certificate store can be managed and inspected with the [PKI](/powershell/module/pkiclient) module.</span></span> <span data-ttu-id="57271-139">Für PowerShell Core 6.x und höher ist der Prozess komplizierter.</span><span class="sxs-lookup"><span data-stu-id="57271-139">For PowerShell Core 6.x and later, the process is more complicated.</span></span> <span data-ttu-id="57271-140">Die folgenden Skripts zeigen, wie ein vorhandenes Zertifikat in den für PowerShell zugänglichen Zertifikatspeicher importiert wird.</span><span class="sxs-lookup"><span data-stu-id="57271-140">The following scripts show you how to import an existing certificate into the certificate store accessible by PowerShell.</span></span>

#### <a name="import-a-certificate-in-powershell-51"></a><span data-ttu-id="57271-141">Importieren eines Zertifikats in PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="57271-141">Import a certificate in PowerShell 5.1</span></span>

```azurepowershell-interactive
# Import a PFX
$credentials = Get-Credential -Message "Provide PFX private key password"
Import-PfxCertificate -FilePath <path to certificate> -Password $credentials.Password -CertStoreLocation cert:\CurrentUser\My
```

#### <a name="import-a-certificate-in-powershell-core-6x-and-later"></a><span data-ttu-id="57271-142">Importieren eines Zertifikats in PowerShell Core 6.x und höher</span><span class="sxs-lookup"><span data-stu-id="57271-142">Import a certificate in PowerShell Core 6.x and later</span></span>

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

## <a name="sign-in-using-a-managed-identity"></a><span data-ttu-id="57271-143">Anmelden mit einer verwalteten Identität</span><span class="sxs-lookup"><span data-stu-id="57271-143">Sign in using a managed identity</span></span>

<span data-ttu-id="57271-144">Verwaltete Identitäten sind ein Feature von Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="57271-144">Managed identities are a feature of Azure Active Directory.</span></span> <span data-ttu-id="57271-145">Bei verwalteten Identitäten handelt es sich um Dienstprinzipale, die den in Azure ausgeführten Ressourcen zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="57271-145">Managed identities are service principals assigned to resources that run in Azure.</span></span> <span data-ttu-id="57271-146">Sie können den Dienstprinzipal einer verwalteten Identität für die Anmeldung verwenden und ein App-exklusives Zugriffstoken für den Zugriff auf andere Ressourcen beziehen.</span><span class="sxs-lookup"><span data-stu-id="57271-146">You can use a managed identity service principal for sign-in, and acquire an app-only access token to access other resources.</span></span> <span data-ttu-id="57271-147">Verwaltete Identitäten stehen nur für Ressourcen zur Verfügung, die in einer Azure-Cloud ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="57271-147">Managed identities are only available on resources running in an Azure cloud.</span></span>

<span data-ttu-id="57271-148">Dieser Befehl stellt mithilfe der verwalteten Identität der Hostumgebung eine Verbindung her.</span><span class="sxs-lookup"><span data-stu-id="57271-148">This command connects using the managed identity of the host environment.</span></span> <span data-ttu-id="57271-149">Beispiel: Bei der Ausführung auf einem virtuellen Computer (VirtualMachine) mit einer zugewiesenen verwalteten Dienstidentität wird dadurch dem Code die Anmeldung mithilfe dieser zugewiesenen Identität ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="57271-149">For example, if executed on a VirtualMachine with an assigned Managed Service Identity, this allows the code to sign in using that assigned identity.</span></span>

```azurepowershell-interactive
 Connect-AzAccount -Identity 
```

## <a name="sign-in-with-a-non-default-tenant-or-as-a-cloud-solution-provider-csp"></a><span data-ttu-id="57271-150">Anmelden mit einem anderen Mandanten als dem Standardmandanten oder als Cloudlösungsanbieter (Cloud Solution Provider, CSP)</span><span class="sxs-lookup"><span data-stu-id="57271-150">Sign in with a non-default tenant or as a Cloud Solution Provider (CSP)</span></span>

<span data-ttu-id="57271-151">Wenn Ihr Konto mehr als einem Mandanten zugeordnet ist, muss bei der Verbindungsherstellung für die Anmeldung der Parameter `-Tenant` verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="57271-151">If your account is associated with more than one tenant, sign-in requires the use of the `-Tenant` parameter when connecting.</span></span> <span data-ttu-id="57271-152">Dieser Parameter funktioniert mit jedem Anmeldeverfahren.</span><span class="sxs-lookup"><span data-stu-id="57271-152">This parameter will work with any sign-in method.</span></span> <span data-ttu-id="57271-153">Beim Anmelden kann dieser Parameterwert entweder die Azure-Objekt-ID des Mandanten (Mandanten-ID) oder der vollqualifizierte Domänenname des Mandanten sein.</span><span class="sxs-lookup"><span data-stu-id="57271-153">When logging in, this parameter value can either be the Azure object ID of the tenant (Tenant ID) or the fully qualified domain name of the tenant.</span></span>

<span data-ttu-id="57271-154">Wenn Sie ein [Cloudlösungsanbieter (Cloud Solution Provider, CSP)](https://azure.microsoft.com/offers/ms-azr-0145p/) sind, `-Tenant`muss**der Wert** eine Mandanten-ID sein.</span><span class="sxs-lookup"><span data-stu-id="57271-154">If you're a [Cloud Solution Provider (CSP)](https://azure.microsoft.com/offers/ms-azr-0145p/), the `-Tenant` value **must** be a tenant ID.</span></span>

```azurepowershell-interactive
Connect-AzAccount -Tenant 'xxxx-xxxx-xxxx-xxxx'
```

## <a name="sign-in-to-another-cloud"></a><span data-ttu-id="57271-155">Anmelden bei einer anderen Cloud</span><span class="sxs-lookup"><span data-stu-id="57271-155">Sign in to another Cloud</span></span>

<span data-ttu-id="57271-156">Azure-Clouddienste verfügen über Umgebungen, die jeweils mit den regionalen Gesetzen zum Umgang mit Daten konform sind.</span><span class="sxs-lookup"><span data-stu-id="57271-156">Azure cloud services offer environments compliant with regional data-handling laws.</span></span>
<span data-ttu-id="57271-157">Legen Sie die Umgebung für Konten in einer regionalen Cloud fest, wenn Sie sich mit dem Argument `-Environment` anmelden.</span><span class="sxs-lookup"><span data-stu-id="57271-157">For accounts in a regional cloud, set the environment when you sign in with the `-Environment` argument.</span></span>
<span data-ttu-id="57271-158">Dieser Parameter funktioniert mit jedem Anmeldeverfahren.</span><span class="sxs-lookup"><span data-stu-id="57271-158">This parameter will work with any sign-in method.</span></span> <span data-ttu-id="57271-159">Beispiel für den Fall, dass sich Ihr Konto in der Cloud in China befindet:</span><span class="sxs-lookup"><span data-stu-id="57271-159">For example, if your account is in the China cloud:</span></span>

```azurepowershell-interactive
Connect-AzAccount -Environment AzureChinaCloud
```

<span data-ttu-id="57271-160">Mit dem folgenden Befehl wird eine Liste mit den verfügbaren Umgebungen abgerufen:</span><span class="sxs-lookup"><span data-stu-id="57271-160">The following command gets a list of available environments:</span></span>

```azurepowershell-interactive
Get-AzEnvironment | Select-Object Name
```
