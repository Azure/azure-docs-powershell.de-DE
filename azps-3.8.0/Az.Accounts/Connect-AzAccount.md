---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/connect-azaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Connect-AzAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Connect-AzAccount.md
ms.openlocfilehash: 32a5c4ac20d584c26d95724a3f4ab4630504fb6d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94003237"
---
# <span data-ttu-id="b18b0-101">Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="b18b0-101">Connect-AzAccount</span></span>

## <span data-ttu-id="b18b0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b18b0-102">SYNOPSIS</span></span>
<span data-ttu-id="b18b0-103">Stellen Sie eine Verbindung mit Azure mit einem authentifizierten Konto für die Verwendung mit Cmdlets aus den AZ PowerShell-Modulen her.</span><span class="sxs-lookup"><span data-stu-id="b18b0-103">Connect to Azure with an authenticated account for use with cmdlets from the Az PowerShell modules.</span></span>

## <span data-ttu-id="b18b0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b18b0-104">SYNTAX</span></span>

### <span data-ttu-id="b18b0-105">UserWithSubscriptionId (Standard)</span><span class="sxs-lookup"><span data-stu-id="b18b0-105">UserWithSubscriptionId (Default)</span></span>

```
Connect-AzAccount [-Environment <String>] [-Tenant <String>] [-Subscription <String>]
 [-ContextName <String>] [-SkipContextPopulation] [-UseDeviceAuthentication] [-Force]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b18b0-106">ServicePrincipalWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b18b0-106">ServicePrincipalWithSubscriptionId</span></span>

```
Connect-AzAccount [-Environment <String>] -Credential <PSCredential> -ServicePrincipal
 -Tenant <String> [-Subscription <String>] [-ContextName <String>] [-SkipContextPopulation] [-Force]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b18b0-107">UserWithCredential</span><span class="sxs-lookup"><span data-stu-id="b18b0-107">UserWithCredential</span></span>

```
Connect-AzAccount [-Environment <String>] -Credential <PSCredential> [-Tenant <String>]
 [-Subscription <String>] [-ContextName <String>] [-SkipContextPopulation] [-Force]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b18b0-108">ServicePrincipalCertificateWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b18b0-108">ServicePrincipalCertificateWithSubscriptionId</span></span>

```
Connect-AzAccount [-Environment <String>] -CertificateThumbprint <String> -ApplicationId <String>
 [-ServicePrincipal] -Tenant <String> [-Subscription <String>] [-ContextName <String>]
 [-SkipContextPopulation] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b18b0-109">AccessTokenWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b18b0-109">AccessTokenWithSubscriptionId</span></span>

```
Connect-AzAccount [-Environment <String>] [-Tenant <String>] -AccessToken <String>
 [-GraphAccessToken <String>] [-KeyVaultAccessToken <String>] -AccountId <String>
 [-Subscription <String>] [-ContextName <String>] [-SkipValidation] [-SkipContextPopulation]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b18b0-110">ManagedServiceLogin</span><span class="sxs-lookup"><span data-stu-id="b18b0-110">ManagedServiceLogin</span></span>

```
Connect-AzAccount [-Environment <String>] [-Tenant <String>] [-AccountId <String>] -Identity
 [-ManagedServicePort <Int32>] [-ManagedServiceHostName <String>]
 [-ManagedServiceSecret <SecureString>] [-Subscription <String>] [-ContextName <String>]
 [-SkipContextPopulation] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b18b0-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b18b0-111">DESCRIPTION</span></span>

<span data-ttu-id="b18b0-112">Das `Connect-AzAccount` Cmdlet stellt eine Verbindung zu Azure mit einem authentifizierten Konto für die Verwendung mit Cmdlets aus den AZ PowerShell-Modulen her.</span><span class="sxs-lookup"><span data-stu-id="b18b0-112">The `Connect-AzAccount` cmdlet connects to Azure with an authenticated account for use with cmdlets from the Az PowerShell modules.</span></span> <span data-ttu-id="b18b0-113">Sie können dieses authentifizierte Konto nur mit Azure-Ressourcen-Manager-Anforderungen verwenden.</span><span class="sxs-lookup"><span data-stu-id="b18b0-113">You can use this authenticated account only with Azure Resource Manager requests.</span></span> <span data-ttu-id="b18b0-114">Verwenden Sie zum Hinzufügen eines authentifizierten Kontos zur Verwendung mit der Dienstverwaltung das `Add-AzureAccount` Cmdlet aus dem Azure PowerShell-Modul.</span><span class="sxs-lookup"><span data-stu-id="b18b0-114">To add an authenticated account for use with Service Management, use the `Add-AzureAccount` cmdlet from the Azure PowerShell module.</span></span> <span data-ttu-id="b18b0-115">Wenn für den aktuellen Benutzer kein Kontext gefunden wird, wird die Kontextliste des Benutzers mit einem Kontext für jedes der ersten 25 Abonnements aufgefüllt.</span><span class="sxs-lookup"><span data-stu-id="b18b0-115">If no context is found for the current user, the user's context list is populated with a context for each of their first 25 subscriptions.</span></span>
<span data-ttu-id="b18b0-116">Die Liste der für den Benutzer erstellten Kontexte kann durch Ausführen gefunden werden `Get-AzContext -ListAvailable` .</span><span class="sxs-lookup"><span data-stu-id="b18b0-116">The list of contexts created for the user can be found by running `Get-AzContext -ListAvailable`.</span></span> <span data-ttu-id="b18b0-117">Um diesen Kontext zu überspringen, geben Sie den **SkipContextPopulation** -Schalterparameter an.</span><span class="sxs-lookup"><span data-stu-id="b18b0-117">To skip this context population, specify the **SkipContextPopulation** switch parameter.</span></span> <span data-ttu-id="b18b0-118">Nachdem Sie dieses Cmdlet ausgeführt haben, können Sie die Verbindung mit einem Azure-Konto mithilfe von beenden `Disconnect-AzAccount` .</span><span class="sxs-lookup"><span data-stu-id="b18b0-118">After executing this cmdlet, you can disconnect from an Azure account using `Disconnect-AzAccount`.</span></span>

## <span data-ttu-id="b18b0-119">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b18b0-119">EXAMPLES</span></span>

### <span data-ttu-id="b18b0-120">Beispiel 1: Herstellen einer Verbindung mit einem Azure-Konto</span><span class="sxs-lookup"><span data-stu-id="b18b0-120">Example 1: Connect to an Azure account</span></span>

<span data-ttu-id="b18b0-121">In diesem Beispiel wird eine Verbindung mit einem Azure-Konto hergestellt.</span><span class="sxs-lookup"><span data-stu-id="b18b0-121">This example connects to an Azure account.</span></span> <span data-ttu-id="b18b0-122">Sie müssen ein Microsoft-Konto oder Organisations-ID-Anmeldeinformationen angeben.</span><span class="sxs-lookup"><span data-stu-id="b18b0-122">You must provide a Microsoft account or organizational ID credentials.</span></span> <span data-ttu-id="b18b0-123">Wenn die mehrstufige Authentifizierung für Ihre Anmeldeinformationen aktiviert ist, müssen Sie sich mit der interaktiven Option anmelden oder die Dienstprinzipal Authentifizierung verwenden.</span><span class="sxs-lookup"><span data-stu-id="b18b0-123">If multi-factor authentication is enabled for your credentials, you must log in using the interactive option or use service principal authentication.</span></span>

```powershell
Connect-AzAccount
```

```Output
Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

### <span data-ttu-id="b18b0-124">Beispiel 2: (nur Windows PowerShell 5,1) Herstellen einer Verbindung mit Azure mithilfe der Organisations-ID-Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="b18b0-124">Example 2: (Windows PowerShell 5.1 only) Connect to Azure using organizational ID credentials</span></span>

<span data-ttu-id="b18b0-125">Dieses Szenario funktioniert nur in Windows PowerShell 5,1.</span><span class="sxs-lookup"><span data-stu-id="b18b0-125">This scenario works only in Windows PowerShell 5.1.</span></span> <span data-ttu-id="b18b0-126">Der erste Befehl fordert Benutzeranmeldeinformationen an und speichert Sie in der `$Credential` Variablen.</span><span class="sxs-lookup"><span data-stu-id="b18b0-126">The first command prompts for user credentials and stores them in the `$Credential` variable.</span></span> <span data-ttu-id="b18b0-127">Der zweite Befehl stellt eine Verbindung mit einem Azure-Konto unter Verwendung der in gespeicherten Anmeldeinformationen her `$Credential` .</span><span class="sxs-lookup"><span data-stu-id="b18b0-127">The second command connects to an Azure account using the credentials stored in `$Credential`.</span></span> <span data-ttu-id="b18b0-128">Dieses Konto authentifiziert sich bei Azure mithilfe der Anmeldeinformationen für die Organisations-ID.</span><span class="sxs-lookup"><span data-stu-id="b18b0-128">This account authenticates with Azure using organizational ID credentials.</span></span>

```powershell
$Credential = Get-Credential
Connect-AzAccount -Credential $Credential
```

```Output
Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

### <span data-ttu-id="b18b0-129">Beispiel 3: Herstellen einer Verbindung mit Azure mithilfe eines Dienstprinzipal Kontos</span><span class="sxs-lookup"><span data-stu-id="b18b0-129">Example 3: Connect to Azure using a service principal account</span></span>

<span data-ttu-id="b18b0-130">Der erste Befehl fordert die Anmeldeinformationen des Dienst Prinzipals an und speichert Sie in der `$Credential` Variablen.</span><span class="sxs-lookup"><span data-stu-id="b18b0-130">The first command prompts for service principal credentials and stores them in the `$Credential` variable.</span></span> <span data-ttu-id="b18b0-131">Geben Sie die Anwendungs-ID für den Benutzernamen und den Dienstprinzipal Schlüssel als Kennwort ein, wenn Sie dazu aufgefordert werden.</span><span class="sxs-lookup"><span data-stu-id="b18b0-131">Enter your application ID for the username and service principal secret as the password when prompted.</span></span> <span data-ttu-id="b18b0-132">Der zweite Befehl verbindet den angegebenen Azure-Mandanten mit den Dienstprinzipal Anmeldeinformationen, die in der Variablen gespeichert sind `$Credential` .</span><span class="sxs-lookup"><span data-stu-id="b18b0-132">The second command connects the specified Azure tenant using the service principal credentials stored in the `$Credential` variable.</span></span> <span data-ttu-id="b18b0-133">Der **ServicePrincipal** -Parameter "Switch" gibt an, dass sich das Konto als Dienstprinzipal authentifiziert.</span><span class="sxs-lookup"><span data-stu-id="b18b0-133">The **ServicePrincipal** switch parameter indicates that the account authenticates as a service principal.</span></span>

```powershell
$Credential = Get-Credential
Connect-AzAccount -Credential $Credential -Tenant 'xxxx-xxxx-xxxx-xxxx' -ServicePrincipal
```

```Output
Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
xxxx-xxxx-xxxx-xxxx    Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

### <span data-ttu-id="b18b0-134">Beispiel 4: Verwenden einer interaktiven Anmeldung zum Herstellen einer Verbindung mit einem bestimmten Mandanten und einem Abonnement</span><span class="sxs-lookup"><span data-stu-id="b18b0-134">Example 4: Use an interactive login to connect to a specific tenant and subscription</span></span>

<span data-ttu-id="b18b0-135">In diesem Beispiel wird eine Verbindung mit einem Azure-Konto mit dem angegebenen Mandanten und Abonnement hergestellt.</span><span class="sxs-lookup"><span data-stu-id="b18b0-135">This example connects to an Azure account with the specified tenant and subscription.</span></span>

```powershell
Connect-AzAccount -Tenant 'xxxx-xxxx-xxxx-xxxx' -SubscriptionId 'yyyy-yyyy-yyyy-yyyy'
```

```Output
Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

### <span data-ttu-id="b18b0-136">Beispiel 5: Herstellen einer Verbindung mit einer verwalteten Dienstidentität</span><span class="sxs-lookup"><span data-stu-id="b18b0-136">Example 5: Connect using a Managed Service Identity</span></span>

<span data-ttu-id="b18b0-137">In diesem Beispiel wird die Verbindung mit der Managed Service Identity (MSI) der Hostumgebung hergestellt.</span><span class="sxs-lookup"><span data-stu-id="b18b0-137">This example connects using the Managed Service Identity (MSI) of the host environment.</span></span> <span data-ttu-id="b18b0-138">Sie können sich beispielsweise von einem virtuellen Computer mit einer zugewiesenen MSI-Nummer bei Azure anmelden.</span><span class="sxs-lookup"><span data-stu-id="b18b0-138">For example, you sign into Azure from a virtual machine that has an assigned MSI.</span></span>

```powershell
Connect-AzAccount -Identity
```

```Output
Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
MSI@50342              Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

### <span data-ttu-id="b18b0-139">Beispiel 6: Herstellen einer Verbindung mit der Anmelde-und ClientID der Managed Service Identity</span><span class="sxs-lookup"><span data-stu-id="b18b0-139">Example 6: Connect using Managed Service Identity login and ClientId</span></span>

<span data-ttu-id="b18b0-140">In diesem Beispiel wird eine Verbindung mit der verwalteten Dienstidentität von **myUserAssignedIdentity** hergestellt.</span><span class="sxs-lookup"><span data-stu-id="b18b0-140">This example connects using the Managed Service Identity of **myUserAssignedIdentity**.</span></span> <span data-ttu-id="b18b0-141">Sie fügt dem virtuellen Computer die dem Benutzer zugewiesene Identität hinzu und stellt dann eine Verbindung mit dem ClientID der Benutzer zugewiesenen Identität her.</span><span class="sxs-lookup"><span data-stu-id="b18b0-141">It adds the user assigned identity to the virtual machine, then connects using the ClientId of the user assigned identity.</span></span> <span data-ttu-id="b18b0-142">Weitere Informationen finden Sie unter [Konfigurieren von verwalteten Identitäten für Azure-Ressourcen auf einem Azure-VM](/azure/active-directory/managed-identities-azure-resources/qs-configure-powershell-windows-vm).</span><span class="sxs-lookup"><span data-stu-id="b18b0-142">For more information, see [Configure managed identities for Azure resources on an Azure VM](/azure/active-directory/managed-identities-azure-resources/qs-configure-powershell-windows-vm).</span></span>

```powershell
$identity = Get-AzUserAssignedIdentity -ResourceGroupName 'myResourceGroup' -Name 'myUserAssignedIdentity'
Get-AzVM -ResourceGroupName contoso -Name testvm | Update-AzVM -IdentityType UserAssigned -IdentityId $identity.Id
Connect-AzAccount -Identity -AccountId $identity.ClientId # Run on the virtual machine
```

```Output
Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
yyyy-yyyy-yyyy-yyyy    Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

### <span data-ttu-id="b18b0-143">Beispiel 7: Herstellen einer Verbindung mit Zertifikaten</span><span class="sxs-lookup"><span data-stu-id="b18b0-143">Example 7: Connect using certificates</span></span>

<span data-ttu-id="b18b0-144">In diesem Beispiel wird eine Verbindung mit einem Azure-Konto mithilfe der zertifikatbasierten Dienstprinzipal Authentifizierung hergestellt.</span><span class="sxs-lookup"><span data-stu-id="b18b0-144">This example connects to an Azure account using certificate-based service principal authentication.</span></span>
<span data-ttu-id="b18b0-145">Der für die Authentifizierung verwendete Dienstprinzipal muss mit dem angegebenen Zertifikat erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="b18b0-145">The service principal used for authentication must be created with the specified certificate.</span></span> <span data-ttu-id="b18b0-146">Weitere Informationen zum Erstellen von selbstsignierten Zertifikaten und Zuweisen von Berechtigungen finden Sie unter [Verwenden von Azure PowerShell zum Erstellen eines Dienst Prinzipals mit einem Zertifikat](/azure/active-directory/develop/howto-authenticate-service-principal-powershell)</span><span class="sxs-lookup"><span data-stu-id="b18b0-146">For more information on creating a self-signed certificates and assigning them permissions, see [Use Azure PowerShell to create a service principal with a certificate](/azure/active-directory/develop/howto-authenticate-service-principal-powershell)</span></span>

```powershell
$Thumbprint = '0SZTNJ34TCCMUJ5MJZGR8XQD3S0RVHJBA33Z8ZXV'
$TenantId = '4cd76576-b611-43d0-8f2b-adcb139531bf'
$ApplicationId = '3794a65a-e4e4-493d-ac1d-f04308d712dd'
Connect-AzAccount -CertificateThumbprint $Thumbprint -ApplicationId $ApplicationId -Tenant $TenantId -ServicePrincipal
```

```Output
Account             SubscriptionName TenantId            Environment
-------             ---------------- --------            -----------
xxxx-xxxx-xxxx-xxxx Subscription1    xxxx-xxxx-xxxx-xxxx AzureCloud

Account          : 3794a65a-e4e4-493d-ac1d-f04308d712dd
SubscriptionName : MyTestSubscription
SubscriptionId   : 85f0f653-1f86-4d2c-a9f1-042efc00085c
TenantId         : 4cd76576-b611-43d0-8f2b-adcb139531bf
Environment      : AzureCloud
```

## <span data-ttu-id="b18b0-147">Parameter</span><span class="sxs-lookup"><span data-stu-id="b18b0-147">PARAMETERS</span></span>

### <span data-ttu-id="b18b0-148">-Access Token</span><span class="sxs-lookup"><span data-stu-id="b18b0-148">-AccessToken</span></span>

<span data-ttu-id="b18b0-149">Gibt ein Zugriffstoken an.</span><span class="sxs-lookup"><span data-stu-id="b18b0-149">Specifies an access token.</span></span>

> [!CAUTION]
> <span data-ttu-id="b18b0-150">Zugriffstoken sind eine Art von Anmeldeinformationen.</span><span class="sxs-lookup"><span data-stu-id="b18b0-150">Access tokens are a type of credential.</span></span> <span data-ttu-id="b18b0-151">Sie sollten die entsprechenden Sicherheitsvorkehrungen treffen, um diese vertraulich zu behandeln.</span><span class="sxs-lookup"><span data-stu-id="b18b0-151">You should take the appropriate security precautions to keep them confidential.</span></span> <span data-ttu-id="b18b0-152">Zugriffstokens auch Timeout und können verhindern, dass lange ausgeführte Aufgaben abgeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="b18b0-152">Access tokens also timeout and may prevent long running tasks from completing.</span></span>

```yaml
Type: System.String
Parameter Sets: AccessTokenWithSubscriptionId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b18b0-153">-Konto-Nr</span><span class="sxs-lookup"><span data-stu-id="b18b0-153">-AccountId</span></span>

<span data-ttu-id="b18b0-154">Konto-ID für Zugriffstoken in **Access Token** -Parametersatz.</span><span class="sxs-lookup"><span data-stu-id="b18b0-154">Account ID for access token in **AccessToken** parameter set.</span></span> <span data-ttu-id="b18b0-155">Konto-ID für verwalteten Dienst in **ManagedService** -Parametersatz.</span><span class="sxs-lookup"><span data-stu-id="b18b0-155">Account ID for managed service in **ManagedService** parameter set.</span></span> <span data-ttu-id="b18b0-156">Kann eine Ressourcen-ID des verwalteten Diensts oder die zugehörige Client-ID sein.</span><span class="sxs-lookup"><span data-stu-id="b18b0-156">Can be a managed service resource ID, or the associated client ID.</span></span>
<span data-ttu-id="b18b0-157">Wenn Sie die dem System zugewiesene Identität verwenden möchten, lassen Sie dieses Feld leer.</span><span class="sxs-lookup"><span data-stu-id="b18b0-157">To use the system assigned identity, leave this field blank.</span></span>

```yaml
Type: System.String
Parameter Sets: AccessTokenWithSubscriptionId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ManagedServiceLogin
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b18b0-158">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="b18b0-158">-ApplicationId</span></span>

<span data-ttu-id="b18b0-159">Anwendungs-ID des Dienst Prinzipals.</span><span class="sxs-lookup"><span data-stu-id="b18b0-159">Application ID of the service principal.</span></span>

```yaml
Type: System.String
Parameter Sets: ServicePrincipalCertificateWithSubscriptionId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b18b0-160">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="b18b0-160">-CertificateThumbprint</span></span>

<span data-ttu-id="b18b0-161">Zertifikat Hash oder Fingerabdruck</span><span class="sxs-lookup"><span data-stu-id="b18b0-161">Certificate Hash or Thumbprint.</span></span>

```yaml
Type: System.String
Parameter Sets: ServicePrincipalCertificateWithSubscriptionId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b18b0-162">-Contextname</span><span class="sxs-lookup"><span data-stu-id="b18b0-162">-ContextName</span></span>

<span data-ttu-id="b18b0-163">Der Name des standardmäßigen Azure-Kontexts für diesen Anmeldenamen.</span><span class="sxs-lookup"><span data-stu-id="b18b0-163">Name of the default Azure context for this login.</span></span> <span data-ttu-id="b18b0-164">Weitere Informationen zu Azure-Kontexten finden Sie unter [Azure PowerShell-Kontextobjekte](/powershell/azure/context-persistence).</span><span class="sxs-lookup"><span data-stu-id="b18b0-164">For more information about Azure contexts, see [Azure PowerShell context objects](/powershell/azure/context-persistence).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b18b0-165">– Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="b18b0-165">-Credential</span></span>

<span data-ttu-id="b18b0-166">Gibt ein **PSCredential** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="b18b0-166">Specifies a **PSCredential** object.</span></span> <span data-ttu-id="b18b0-167">Wenn Sie weitere Informationen zum **PSCredential** -Objekt wünschen, geben Sie `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="b18b0-167">For more information about the **PSCredential** object, type `Get-Help Get-Credential`.</span></span> <span data-ttu-id="b18b0-168">Das **PSCredential** -Objekt enthält die Benutzer-ID und das Kennwort für die Anmeldeinformationen für die Organisations-ID oder die Anwendungs-ID und den Schlüssel für die Anmeldeinformationen des Dienst Prinzipals.</span><span class="sxs-lookup"><span data-stu-id="b18b0-168">The **PSCredential** object provides the user ID and password for organizational ID credentials, or the application ID and secret for service principal credentials.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: ServicePrincipalWithSubscriptionId, UserWithCredential
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b18b0-169">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b18b0-169">-DefaultProfile</span></span>

<span data-ttu-id="b18b0-170">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b18b0-170">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b18b0-171">-Umgebung</span><span class="sxs-lookup"><span data-stu-id="b18b0-171">-Environment</span></span>

<span data-ttu-id="b18b0-172">Umgebung, die das Azure-Konto enthält.</span><span class="sxs-lookup"><span data-stu-id="b18b0-172">Environment containing the Azure account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: EnvironmentName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b18b0-173">-Force</span><span class="sxs-lookup"><span data-stu-id="b18b0-173">-Force</span></span>

<span data-ttu-id="b18b0-174">Überschreiben Sie den vorhandenen Kontext mit demselben Namen ohne Aufforderung.</span><span class="sxs-lookup"><span data-stu-id="b18b0-174">Overwrite the existing context with the same name without prompting.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b18b0-175">-GraphAccessToken</span><span class="sxs-lookup"><span data-stu-id="b18b0-175">-GraphAccessToken</span></span>

<span data-ttu-id="b18b0-176">Access Token for Graph-Dienst.</span><span class="sxs-lookup"><span data-stu-id="b18b0-176">AccessToken for Graph Service.</span></span>

```yaml
Type: System.String
Parameter Sets: AccessTokenWithSubscriptionId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b18b0-177">-Identity</span><span class="sxs-lookup"><span data-stu-id="b18b0-177">-Identity</span></span>

<span data-ttu-id="b18b0-178">Melden Sie sich mit einer verwalteten Dienstidentität an.</span><span class="sxs-lookup"><span data-stu-id="b18b0-178">Login using a Managed Service Identity.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ManagedServiceLogin
Aliases: MSI, ManagedService

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b18b0-179">-KeyVaultAccessToken</span><span class="sxs-lookup"><span data-stu-id="b18b0-179">-KeyVaultAccessToken</span></span>

<span data-ttu-id="b18b0-180">Access Token für keyvault-Dienst.</span><span class="sxs-lookup"><span data-stu-id="b18b0-180">AccessToken for KeyVault Service.</span></span>

```yaml
Type: System.String
Parameter Sets: AccessTokenWithSubscriptionId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b18b0-181">-ManagedServiceHostName</span><span class="sxs-lookup"><span data-stu-id="b18b0-181">-ManagedServiceHostName</span></span>

<span data-ttu-id="b18b0-182">Hostname für den verwalteten Dienst</span><span class="sxs-lookup"><span data-stu-id="b18b0-182">Host name for the managed service.</span></span>

```yaml
Type: System.String
Parameter Sets: ManagedServiceLogin
Aliases:

Required: False
Position: Named
Default value: localhost
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b18b0-183">-ManagedServicePort</span><span class="sxs-lookup"><span data-stu-id="b18b0-183">-ManagedServicePort</span></span>

<span data-ttu-id="b18b0-184">Port Nummer für den verwalteten Dienst</span><span class="sxs-lookup"><span data-stu-id="b18b0-184">Port number for the managed service.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ManagedServiceLogin
Aliases:

Required: False
Position: Named
Default value: 50342
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b18b0-185">-ManagedServiceSecret</span><span class="sxs-lookup"><span data-stu-id="b18b0-185">-ManagedServiceSecret</span></span>

<span data-ttu-id="b18b0-186">Token für die Anmeldung des verwalteten Diensts.</span><span class="sxs-lookup"><span data-stu-id="b18b0-186">Token for the managed service login.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: ManagedServiceLogin
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b18b0-187">-Scope</span><span class="sxs-lookup"><span data-stu-id="b18b0-187">-Scope</span></span>

<span data-ttu-id="b18b0-188">Bestimmt den Bereich von Kontextänderungen, beispielsweise, ob Änderungen nur für den aktuellen Prozess oder für alle von diesem Benutzer gestarteten Sitzungen gelten.</span><span class="sxs-lookup"><span data-stu-id="b18b0-188">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Common.ContextModificationScope
Parameter Sets: (All)
Aliases:
Accepted values: Process, CurrentUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b18b0-189">-ServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="b18b0-189">-ServicePrincipal</span></span>

<span data-ttu-id="b18b0-190">Gibt an, dass sich dieses Konto durch die Bereitstellung von Dienstprinzipal Anmeldeinformationen authentifiziert.</span><span class="sxs-lookup"><span data-stu-id="b18b0-190">Indicates that this account authenticates by providing service principal credentials.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ServicePrincipalWithSubscriptionId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ServicePrincipalCertificateWithSubscriptionId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b18b0-191">-SkipContextPopulation</span><span class="sxs-lookup"><span data-stu-id="b18b0-191">-SkipContextPopulation</span></span>

<span data-ttu-id="b18b0-192">Überspringt die Kontext Auffüllung, wenn keine Zusammenhänge gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="b18b0-192">Skips context population if no contexts are found.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b18b0-193">-SkipValidation</span><span class="sxs-lookup"><span data-stu-id="b18b0-193">-SkipValidation</span></span>

<span data-ttu-id="b18b0-194">Überprüfung für Zugriffstoken überspringen.</span><span class="sxs-lookup"><span data-stu-id="b18b0-194">Skip validation for access token.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AccessTokenWithSubscriptionId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b18b0-195">-Abonnement</span><span class="sxs-lookup"><span data-stu-id="b18b0-195">-Subscription</span></span>

<span data-ttu-id="b18b0-196">Name oder ID des Abonnements.</span><span class="sxs-lookup"><span data-stu-id="b18b0-196">Subscription Name or ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SubscriptionName, SubscriptionId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b18b0-197">-Mandant</span><span class="sxs-lookup"><span data-stu-id="b18b0-197">-Tenant</span></span>

<span data-ttu-id="b18b0-198">Optionaler Mandantenname oder ID.</span><span class="sxs-lookup"><span data-stu-id="b18b0-198">Optional tenant name or ID.</span></span>

> [!NOTE]
> <span data-ttu-id="b18b0-199">Aufgrund von Einschränkungen der aktuellen API müssen Sie beim Herstellen einer Verbindung mit einem Business-to-Business (B2B)-Konto eine Mandanten-ID anstelle eines Mandantennamens verwenden.</span><span class="sxs-lookup"><span data-stu-id="b18b0-199">Due to limitations of the current API, you must use a tenant ID instead of a tenant name when connecting with a business-to-business (B2B) account.</span></span>

```yaml
Type: System.String
Parameter Sets: UserWithSubscriptionId, UserWithCredential, AccessTokenWithSubscriptionId, ManagedServiceLogin
Aliases: Domain, TenantId

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ServicePrincipalWithSubscriptionId, ServicePrincipalCertificateWithSubscriptionId
Aliases: Domain, TenantId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b18b0-200">-UseDeviceAuthentication</span><span class="sxs-lookup"><span data-stu-id="b18b0-200">-UseDeviceAuthentication</span></span>

<span data-ttu-id="b18b0-201">Verwenden Sie die Gerätecode Authentifizierung anstelle eines Browsersteuerelements.</span><span class="sxs-lookup"><span data-stu-id="b18b0-201">Use device code authentication instead of a browser control.</span></span> <span data-ttu-id="b18b0-202">Dies ist der Standard Authentifizierungstyp für PowerShell ab Version 6.</span><span class="sxs-lookup"><span data-stu-id="b18b0-202">This is the default authentication type for PowerShell version 6 and higher.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: UserWithSubscriptionId
Aliases: DeviceCode, DeviceAuth, Device

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b18b0-203">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b18b0-203">-Confirm</span></span>

<span data-ttu-id="b18b0-204">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b18b0-204">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b18b0-205">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b18b0-205">-WhatIf</span></span>

<span data-ttu-id="b18b0-206">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b18b0-206">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b18b0-207">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b18b0-207">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b18b0-208">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b18b0-208">CommonParameters</span></span>

<span data-ttu-id="b18b0-209">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b18b0-209">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b18b0-210">Weitere Informationen finden Sie unter [about_CommonParameters](/powershell/module/microsoft.powershell.core/about/about_commonparameters).</span><span class="sxs-lookup"><span data-stu-id="b18b0-210">For more information, see [about_CommonParameters](/powershell/module/microsoft.powershell.core/about/about_commonparameters).</span></span>
<span data-ttu-id="b18b0-211">(http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b18b0-211">(http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b18b0-212">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b18b0-212">INPUTS</span></span>

### <span data-ttu-id="b18b0-213">System. String</span><span class="sxs-lookup"><span data-stu-id="b18b0-213">System.String</span></span>

## <span data-ttu-id="b18b0-214">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b18b0-214">OUTPUTS</span></span>

### <span data-ttu-id="b18b0-215">Microsoft. Azure. Commands. profile. Models. Core. PSAzureProfile</span><span class="sxs-lookup"><span data-stu-id="b18b0-215">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureProfile</span></span>

## <span data-ttu-id="b18b0-216">Notizen</span><span class="sxs-lookup"><span data-stu-id="b18b0-216">NOTES</span></span>

## <span data-ttu-id="b18b0-217">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b18b0-217">RELATED LINKS</span></span>
