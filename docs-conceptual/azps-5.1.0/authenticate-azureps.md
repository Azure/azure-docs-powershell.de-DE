---
title: Anmelden mit Azure PowerShell
description: Es wird beschrieben, wie Sie sich mit Azure PowerShell als Benutzer, per Dienstprinzipal oder mit verwalteten Identitäten für Azure-Ressourcen anmelden.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 11/23/2020
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: 46e5e84b6718cc7a700ef2df4e82647e8cb60941
ms.sourcegitcommit: 25eca7b5f5480758aa2cd830458900cf91cf673c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/24/2020
ms.locfileid: "95515108"
---
# <a name="sign-in-with-azure-powershell"></a><span data-ttu-id="41658-103">Anmelden mit Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="41658-103">Sign in with Azure PowerShell</span></span>

<span data-ttu-id="41658-104">Azure PowerShell unterstützt mehrere Authentifizierungsmethoden.</span><span class="sxs-lookup"><span data-stu-id="41658-104">Azure PowerShell supports several authentication methods.</span></span> <span data-ttu-id="41658-105">Den einfachsten Einstieg ermöglicht der [Azure Cloud Shell](/azure/cloud-shell/overview)-Dienst, der Sie automatisch anmeldet.</span><span class="sxs-lookup"><span data-stu-id="41658-105">The easiest way to get started is with [Azure Cloud Shell](/azure/cloud-shell/overview), which automatically logs you in.</span></span> <span data-ttu-id="41658-106">Bei einer lokalen Installation können Sie sich interaktiv über Ihren Browser anmelden.</span><span class="sxs-lookup"><span data-stu-id="41658-106">With a local install, you can sign in interactively through your browser.</span></span> <span data-ttu-id="41658-107">Beim Schreiben von Skripts für die Automatisierung besteht der empfohlene Ansatz darin, einen [Dienstprinzipal](create-azure-service-principal-azureps.md) mit den erforderlichen Berechtigungen zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="41658-107">When writing scripts for automation, the recommended approach is to use a [service principal](create-azure-service-principal-azureps.md) with the necessary permissions.</span></span> <span data-ttu-id="41658-108">Indem Sie die Anmeldeberechtigungen für Ihren Anwendungsfall so weit wie möglich einschränken, tragen Sie zur Sicherheit Ihrer Azure-Ressourcen bei.</span><span class="sxs-lookup"><span data-stu-id="41658-108">When you restrict sign-in permissions as much as possible for your use case, you help keep your Azure resources secure.</span></span>

<span data-ttu-id="41658-109">Zunächst sind Sie beim ersten Abonnement angemeldet, das von Azure zurückgegeben wird, wenn Sie Zugriff auf mehrere Abonnements haben.</span><span class="sxs-lookup"><span data-stu-id="41658-109">Initially, you're signed into the first subscription Azure returns if you have access to more than one subscription.</span></span> <span data-ttu-id="41658-110">Befehle werden für dieses Abonnement standardmäßig ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="41658-110">Commands are run against this subscription by default.</span></span> <span data-ttu-id="41658-111">Verwenden Sie das Cmdlet [Set-AzContext](/powershell/module/az.accounts/set-azcontext), um Ihr aktives Abonnement für eine Sitzung zu ändern.</span><span class="sxs-lookup"><span data-stu-id="41658-111">To change your active subscription for a session, use the [Set-AzContext](/powershell/module/az.accounts/set-azcontext) cmdlet.</span></span> <span data-ttu-id="41658-112">Um Ihr aktives Abonnement zu ändern und es zwischen Sitzungen auf demselben System beizubehalten, verwenden Sie das Cmdlet [Select-AzContext](/powershell/module/az.accounts/select-azcontext).</span><span class="sxs-lookup"><span data-stu-id="41658-112">To change your active subscription and have it persist between sessions on the same system, use the [Select-AzContext](/powershell/module/az.accounts/select-azcontext) cmdlet.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="41658-113">Ihre Anmeldeinformationen werden in mehreren PowerShell-Sitzungen gemeinsam verwendet, solange Sie angemeldet bleiben.</span><span class="sxs-lookup"><span data-stu-id="41658-113">Your credentials are shared among multiple PowerShell sessions as long as you remain signed in.</span></span>
> <span data-ttu-id="41658-114">Weitere Informationen finden Sie im Artikel zu [beständigen Anmeldeinformationen](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="41658-114">For more information, see the article on [Persistent Credentials](context-persistence.md).</span></span>

## <a name="sign-in-interactively"></a><span data-ttu-id="41658-115">Interaktives Anmelden</span><span class="sxs-lookup"><span data-stu-id="41658-115">Sign in interactively</span></span>

<span data-ttu-id="41658-116">Verwenden Sie für die interaktive Anmeldung das Cmdlet [Connect-AzAccount](/powershell/module/az.accounts/connect-azaccount).</span><span class="sxs-lookup"><span data-stu-id="41658-116">To sign in interactively, use the [Connect-AzAccount](/powershell/module/az.accounts/connect-azaccount) cmdlet.</span></span>

```azurepowershell-interactive
Connect-AzAccount
```

<span data-ttu-id="41658-117">Ab Version 5.0.0 des Az-PowerShell-Moduls zeigt dieses Cmdlet standardmäßig eine browserbasierte interaktive Anmeldeaufforderung an.</span><span class="sxs-lookup"><span data-stu-id="41658-117">Beginning with Az PowerShell module version 5.0.0, this cmdlet presents an interactive browser based login prompt by default.</span></span> <span data-ttu-id="41658-118">Sie können den Parameter `UseDeviceAuthentication` angeben, um eine Tokenzeichenfolge zu erhalten. Dies war zuvor die Standardeinstellung für PowerShell-Version 6 und höhere Versionen.</span><span class="sxs-lookup"><span data-stu-id="41658-118">You can specify the `UseDeviceAuthentication` parameter to receive a token string which was previously the default for PowerShell version 6 and higher.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="41658-119">Die Autorisierung mit Anmeldeinformationen (Benutzername/Kennwort) wurde in Azure PowerShell aufgrund von Änderungen in Active Directory-Autorisierungsimplementierungen und Sicherheitsbedenken entfernt.</span><span class="sxs-lookup"><span data-stu-id="41658-119">Username/password credential authorization has been removed in Azure PowerShell due to changes in Active Directory authorization implementations and security concerns.</span></span> <span data-ttu-id="41658-120">Wenn Sie die Autorisierung mit Anmeldeinformationen zu Automatisierungszwecken verwenden, [erstellen Sie stattdessen einen Dienstprinzipal](create-azure-service-principal-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="41658-120">If you use credential authorization for automation purposes, instead [create a service principal](create-azure-service-principal-azureps.md).</span></span>

<span data-ttu-id="41658-121">Verwenden Sie das Cmdlet [Get-AzContext](/powershell/module/az.accounts/get-azcontext), um Ihre Mandanten-ID in einer Variablen zu speichern, die in den nächsten beiden Abschnitten dieses Artikels verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="41658-121">Use the [Get-AzContext](/powershell/module/az.accounts/get-azcontext) cmdlet to store your tenant ID in a variable to be used in the next two sections of this article.</span></span>

```azurepowershell-interactive
$tenantId = (Get-AzContext).Tenant.Id
```

## <a name="sign-in-with-a-service-principal"></a><span data-ttu-id="41658-122">Anmelden mit einem Dienstprinzipal<a name="sp-signin"/></span><span class="sxs-lookup"><span data-stu-id="41658-122">Sign in with a service principal <a name="sp-signin"/></span></span>

<span data-ttu-id="41658-123">Dienstprinzipale sind nicht interaktive Azure-Konten.</span><span class="sxs-lookup"><span data-stu-id="41658-123">Service principals are non-interactive Azure accounts.</span></span> <span data-ttu-id="41658-124">Wie bei anderen Benutzerkonten auch, werden die Berechtigungen mit Azure Active Directory verwaltet.</span><span class="sxs-lookup"><span data-stu-id="41658-124">Like other user accounts, their permissions are managed with Azure Active Directory.</span></span> <span data-ttu-id="41658-125">Indem für einen Dienstprinzipal nur die benötigten Berechtigungen gewährt werden, bleibt die Sicherheit Ihrer Automatisierungsskripts gewahrt.</span><span class="sxs-lookup"><span data-stu-id="41658-125">By granting a service principal only the permissions it needs, your automation scripts stay secure.</span></span>

<span data-ttu-id="41658-126">Informationen zur Erstellung eines Dienstprinzipals für die Verwendung mit PowerShell finden Sie unter [Erstellen eines Azure-Dienstprinzipals mit Azure PowerShell](create-azure-service-principal-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="41658-126">To learn how to create a service principal for use with Azure PowerShell, see [Create an Azure service principal with Azure PowerShell](create-azure-service-principal-azureps.md).</span></span>

<span data-ttu-id="41658-127">Verwenden Sie für die Anmeldung mit einem Dienstprinzipal das Cmdlet `Connect-AzAccount` mit dem Argument `-ServicePrincipal`.</span><span class="sxs-lookup"><span data-stu-id="41658-127">To sign in with a service principal, use the `-ServicePrincipal` argument with the `Connect-AzAccount` cmdlet.</span></span> <span data-ttu-id="41658-128">Sie benötigen auch die Anwendungs-ID und die Anmeldeinformationen des Dienstprinzipals sowie die dem Dienstprinzipal zugeordnete Mandanten-ID.</span><span class="sxs-lookup"><span data-stu-id="41658-128">You'll also need the service principal's application ID, sign-in credentials, and the tenant ID associate with the service principal.</span></span> <span data-ttu-id="41658-129">Wie Sie sich mit einem Dienstprinzipal anmelden, hängt davon ab, ob er für die kennwortbasierte oder die zertifikatbasierte Authentifizierung konfiguriert wurde.</span><span class="sxs-lookup"><span data-stu-id="41658-129">How you sign in with a service principal depends on whether it's configured for password-based or certificate-based authentication.</span></span>

### <a name="password-based-authentication"></a><span data-ttu-id="41658-130">Kennwortbasierte Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="41658-130">Password-based authentication</span></span>

<span data-ttu-id="41658-131">Erstellen Sie einen Dienstprinzipal für die Verwendung in den Beispielen in diesem Abschnitt.</span><span class="sxs-lookup"><span data-stu-id="41658-131">Create a service principal to be used in the examples in this section.</span></span> <span data-ttu-id="41658-132">Weitere Informationen zum Erstellen von Dienstprinzipalen finden Sie unter [Erstellen eines Azure-Dienstprinzipals mit Azure PowerShell](/powershell/azure/create-azure-service-principal-azureps).</span><span class="sxs-lookup"><span data-stu-id="41658-132">For more information on creating service principals, see [Create an Azure service principal with Azure PowerShell](/powershell/azure/create-azure-service-principal-azureps).</span></span>

```azurepowershell-interactive
$sp = New-AzADServicePrincipal -DisplayName ServicePrincipalName
```

<span data-ttu-id="41658-133">Verwenden Sie das Cmdlet [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential), um die Anmeldeinformationen des Dienstprinzipals als entsprechendes Objekt abzurufen.</span><span class="sxs-lookup"><span data-stu-id="41658-133">To get the service principal's credentials as the appropriate object, use the [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential) cmdlet.</span></span> <span data-ttu-id="41658-134">Mit diesem Cmdlet wird eine Eingabeaufforderung für Benutzername und Kennwort angezeigt.</span><span class="sxs-lookup"><span data-stu-id="41658-134">This cmdlet presents a prompt for a username and password.</span></span> <span data-ttu-id="41658-135">Verwenden Sie die `applicationID` des Dienstprinzipals für den Benutzernamen, und konvertieren Sie dessen `secret` in Nur-Text für das Kennwort.</span><span class="sxs-lookup"><span data-stu-id="41658-135">Use the service principal's `applicationID` for the username and convert its `secret` to plain text for the password.</span></span>

```azurepowershell-interactive
# Retrieve the plain text password for use with `Get-Credential` in the next command.
$sp.secret | ConvertFrom-SecureString -AsPlainText

$pscredential = Get-Credential -UserName $sp.ApplicationId
Connect-AzAccount -ServicePrincipal -Credential $pscredential -Tenant $tenantId
```

<span data-ttu-id="41658-136">Für Automatisierungsszenarien müssen Sie Anmeldeinformationen aus der `applicationId` und dem `secret` eines Dienstprinzipals erstellen:</span><span class="sxs-lookup"><span data-stu-id="41658-136">For automation scenarios, you need to create credentials from a service principal's `applicationId` and `secret`:</span></span>

```azurepowershell-interactive
$pscredential = New-Object -TypeName System.Management.Automation.PSCredential($sp.ApplicationId, $sp.Secret)
Connect-AzAccount -ServicePrincipal -Credential $pscredential -Tenant $tenantId
```

<span data-ttu-id="41658-137">Achten Sie darauf, gute Methoden für die Kennwortspeicherung zu verwenden, wenn Sie Dienstprinzipalverbindungen automatisieren.</span><span class="sxs-lookup"><span data-stu-id="41658-137">Make sure that you use good password storage practices when automating service principal connections.</span></span>

### <a name="certificate-based-authentication"></a><span data-ttu-id="41658-138">Zertifikatbasierte Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="41658-138">Certificate-based authentication</span></span>

<span data-ttu-id="41658-139">Zertifikatbasierte Authentifizierung erfordert, dass Azure PowerShell Informationen von einem lokalen Zertifikatsspeicher basierend auf einem Fingerabdruck des Zertifikats abrufen kann.</span><span class="sxs-lookup"><span data-stu-id="41658-139">Certificate-based authentication requires that Azure PowerShell can retrieve information from a local certificate store based on a certificate thumbprint.</span></span>

```azurepowershell-interactive
Connect-AzAccount -ApplicationId $appId -Tenant $tenantId -CertificateThumbprint <thumbprint>
```

<span data-ttu-id="41658-140">Wenn Sie einen Dienstprinzipal anstelle einer registrierten Anwendung verwenden, fügen Sie das Argument `-ServicePrincipal` hinzu, und geben Sie die Anwendungs-ID des Dienstprinzipals als Wert für den Parameter `-ApplicationId` an.</span><span class="sxs-lookup"><span data-stu-id="41658-140">When using a service principal instead of a registered application, add the `-ServicePrincipal` argument and provide the service principal's Application ID as the `-ApplicationId` parameter's value.</span></span>

```azurepowershell-interactive
Connect-AzAccount -ServicePrincipal -ApplicationId $servicePrincipalId -Tenant $tenantId -CertificateThumbprint <thumbprint>
```

<span data-ttu-id="41658-141">In PowerShell 5.1 kann der Zertifikatspeicher mit den [PKI](/powershell/module/pkiclient)-Modul verwaltet und überprüft werden.</span><span class="sxs-lookup"><span data-stu-id="41658-141">In PowerShell 5.1, the certificate store can be managed and inspected with the [PKI](/powershell/module/pkiclient) module.</span></span> <span data-ttu-id="41658-142">Für PowerShell Core 6.x und höher ist der Prozess komplizierter.</span><span class="sxs-lookup"><span data-stu-id="41658-142">For PowerShell Core 6.x and later, the process is more complicated.</span></span> <span data-ttu-id="41658-143">Die folgenden Skripts zeigen, wie ein vorhandenes Zertifikat in den für PowerShell zugänglichen Zertifikatspeicher importiert wird.</span><span class="sxs-lookup"><span data-stu-id="41658-143">The following scripts show you how to import an existing certificate into the certificate store accessible by PowerShell.</span></span>

#### <a name="import-a-certificate-in-powershell-51"></a><span data-ttu-id="41658-144">Importieren eines Zertifikats in PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="41658-144">Import a certificate in PowerShell 5.1</span></span>

```azurepowershell-interactive
# Import a PFX
$credentials = Get-Credential -Message "Provide PFX private key password"
Import-PfxCertificate -FilePath <path to certificate> -Password $credentials.Password -CertStoreLocation cert:\CurrentUser\My
```

#### <a name="import-a-certificate-in-powershell-core-6x-and-later"></a><span data-ttu-id="41658-145">Importieren eines Zertifikats in PowerShell Core 6.x und höher</span><span class="sxs-lookup"><span data-stu-id="41658-145">Import a certificate in PowerShell Core 6.x and later</span></span>

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

## <a name="sign-in-using-a-managed-identity"></a><span data-ttu-id="41658-146">Anmelden mit einer verwalteten Identität</span><span class="sxs-lookup"><span data-stu-id="41658-146">Sign in using a managed identity</span></span>

<span data-ttu-id="41658-147">Verwaltete Identitäten sind ein Feature von Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="41658-147">Managed identities are a feature of Azure Active Directory.</span></span> <span data-ttu-id="41658-148">Bei verwalteten Identitäten handelt es sich um Dienstprinzipale, die den in Azure ausgeführten Ressourcen zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="41658-148">Managed identities are service principals assigned to resources that run in Azure.</span></span> <span data-ttu-id="41658-149">Sie können den Dienstprinzipal einer verwalteten Identität für die Anmeldung verwenden und ein App-exklusives Zugriffstoken für den Zugriff auf andere Ressourcen beziehen.</span><span class="sxs-lookup"><span data-stu-id="41658-149">You can use a managed identity service principal for sign-in, and acquire an app-only access token to access other resources.</span></span> <span data-ttu-id="41658-150">Verwaltete Identitäten stehen nur für Ressourcen zur Verfügung, die in einer Azure-Cloud ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="41658-150">Managed identities are only available on resources running in an Azure cloud.</span></span>

<span data-ttu-id="41658-151">In diesem Beispiel wird mithilfe der verwalteten Identität der Hostumgebung eine Verbindung hergestellt.</span><span class="sxs-lookup"><span data-stu-id="41658-151">This example connects using the managed identity of the host environment.</span></span> <span data-ttu-id="41658-152">Beispiel: Bei der Ausführung auf einem virtuellen Computer (VirtualMachine) mit einer zugewiesenen verwalteten Dienstidentität wird dadurch dem Code die Anmeldung mithilfe dieser zugewiesenen Identität ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="41658-152">For example, if executed on a VirtualMachine with an assigned Managed Service Identity, this allows the code to sign in using that assigned identity.</span></span>

```azurepowershell-interactive
 Connect-AzAccount -Identity
```

## <a name="sign-in-with-a-non-default-tenant-or-as-a-cloud-solution-provider-csp"></a><span data-ttu-id="41658-153">Anmelden mit einem anderen Mandanten als dem Standardmandanten oder als Cloudlösungsanbieter (Cloud Solution Provider, CSP)</span><span class="sxs-lookup"><span data-stu-id="41658-153">Sign in with a non-default tenant or as a Cloud Solution Provider (CSP)</span></span>

<span data-ttu-id="41658-154">Wenn Ihr Konto mehr als einem Mandanten zugeordnet ist, muss bei der Verbindungsherstellung für die Anmeldung der Parameter `-Tenant` verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="41658-154">If your account is associated with more than one tenant, sign-in requires the `-Tenant` parameter to be specified when connecting.</span></span> <span data-ttu-id="41658-155">Dieser Parameter funktioniert mit jedem Anmeldeverfahren.</span><span class="sxs-lookup"><span data-stu-id="41658-155">This parameter works with any sign-in method.</span></span> <span data-ttu-id="41658-156">Beim Anmelden kann dieser Parameterwert entweder die Azure-Objekt-ID des Mandanten (Mandanten-ID) oder der vollqualifizierte Domänenname des Mandanten sein.</span><span class="sxs-lookup"><span data-stu-id="41658-156">When logging in, this parameter value can either be the Azure object ID of the tenant (Tenant ID) or the fully qualified domain name of the tenant.</span></span>

<span data-ttu-id="41658-157">Wenn Sie ein [Cloudlösungsanbieter (Cloud Solution Provider, CSP)](https://azure.microsoft.com/offers/ms-azr-0145p/) sind, **muss** der Wert `-Tenant` eine Mandanten-ID sein.</span><span class="sxs-lookup"><span data-stu-id="41658-157">If you're a [Cloud Solution Provider (CSP)](https://azure.microsoft.com/offers/ms-azr-0145p/), the `-Tenant` value **must** be a tenant ID.</span></span>

```azurepowershell-interactive
Connect-AzAccount -Tenant 'xxxx-xxxx-xxxx-xxxx'
```

## <a name="sign-in-to-another-cloud"></a><span data-ttu-id="41658-158">Anmelden bei einer anderen Cloud</span><span class="sxs-lookup"><span data-stu-id="41658-158">Sign in to another Cloud</span></span>

<span data-ttu-id="41658-159">Azure-Clouddienste verfügen über Umgebungen, die jeweils mit den regionalen Gesetzen zum Umgang mit Daten konform sind.</span><span class="sxs-lookup"><span data-stu-id="41658-159">Azure cloud services offer environments compliant with regional data-handling laws.</span></span> <span data-ttu-id="41658-160">Legen Sie die Umgebung für Konten in einer regionalen Cloud fest, wenn Sie sich mit dem Argument `-Environment` anmelden.</span><span class="sxs-lookup"><span data-stu-id="41658-160">For accounts in a regional cloud, set the environment when you sign in with the `-Environment` argument.</span></span> <span data-ttu-id="41658-161">Dieser Parameter funktioniert mit jedem Anmeldeverfahren.</span><span class="sxs-lookup"><span data-stu-id="41658-161">This parameter works with any sign-in method.</span></span> <span data-ttu-id="41658-162">Beispiel für den Fall, dass sich Ihr Konto in der Cloud in China befindet:</span><span class="sxs-lookup"><span data-stu-id="41658-162">For example, if your account is in the China cloud:</span></span>

```azurepowershell-interactive
Connect-AzAccount -Environment AzureChinaCloud
```

<span data-ttu-id="41658-163">Mit dem folgenden Befehl wird eine Liste mit den verfügbaren Umgebungen abgerufen:</span><span class="sxs-lookup"><span data-stu-id="41658-163">The following command gets a list of available environments:</span></span>

```azurepowershell-interactive
Get-AzEnvironment | Select-Object -Property Name
```
