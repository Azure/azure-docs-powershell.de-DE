---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/connect-azaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Connect-AzAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Connect-AzAccount.md
ms.openlocfilehash: 87e8615e7862e8b3314c9dace4849621a8ed4c78
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841103"
---
# <span data-ttu-id="d8cd8-101">Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="d8cd8-101">Connect-AzAccount</span></span>

## <span data-ttu-id="d8cd8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d8cd8-102">SYNOPSIS</span></span>
<span data-ttu-id="d8cd8-103">Herstellen einer Verbindung mit Azure mit einem authentifizierten Konto für die Verwendung mit Azure Resource Manager-Cmdlet-Anforderungen.</span><span class="sxs-lookup"><span data-stu-id="d8cd8-103">Connect to Azure with an authenticated account for use with Azure Resource Manager cmdlet requests.</span></span>

## <span data-ttu-id="d8cd8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d8cd8-104">SYNTAX</span></span>

### <span data-ttu-id="d8cd8-105">UserWithSubscriptionId (Standard)</span><span class="sxs-lookup"><span data-stu-id="d8cd8-105">UserWithSubscriptionId (Default)</span></span>
```
Connect-AzAccount [-Environment <String>] [-Tenant <String>] [-Subscription <String>] [-ContextName <String>]
 [-SkipContextPopulation] [-UseDeviceAuthentication] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d8cd8-106">ServicePrincipalWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d8cd8-106">ServicePrincipalWithSubscriptionId</span></span>
```
Connect-AzAccount [-Environment <String>] -Credential <PSCredential> [-ServicePrincipal] -Tenant <String>
 [-Subscription <String>] [-ContextName <String>] [-SkipContextPopulation] [-Force]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d8cd8-107">UserWithCredential</span><span class="sxs-lookup"><span data-stu-id="d8cd8-107">UserWithCredential</span></span>
```
Connect-AzAccount [-Environment <String>] -Credential <PSCredential> [-Tenant <String>]
 [-Subscription <String>] [-ContextName <String>] [-SkipContextPopulation] [-Force]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d8cd8-108">ServicePrincipalCertificateWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d8cd8-108">ServicePrincipalCertificateWithSubscriptionId</span></span>
```
Connect-AzAccount [-Environment <String>] -CertificateThumbprint <String> -ApplicationId <String>
 [-ServicePrincipal] -Tenant <String> [-Subscription <String>] [-ContextName <String>] [-SkipContextPopulation]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d8cd8-109">AccessTokenWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d8cd8-109">AccessTokenWithSubscriptionId</span></span>
```
Connect-AzAccount [-Environment <String>] [-Tenant <String>] -AccessToken <String> [-GraphAccessToken <String>]
 [-KeyVaultAccessToken <String>] -AccountId <String> [-Subscription <String>] [-ContextName <String>]
 [-SkipValidation] [-SkipContextPopulation] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d8cd8-110">ManagedServiceLogin</span><span class="sxs-lookup"><span data-stu-id="d8cd8-110">ManagedServiceLogin</span></span>
```
Connect-AzAccount [-Environment <String>] [-Tenant <String>] [-AccountId <String>] [-Identity]
 [-ManagedServicePort <Int32>] [-ManagedServiceHostName <String>] [-ManagedServiceSecret <SecureString>]
 [-Subscription <String>] [-ContextName <String>] [-SkipContextPopulation] [-Force]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d8cd8-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d8cd8-111">DESCRIPTION</span></span>
<span data-ttu-id="d8cd8-112">Das Connect-AzAccount-Cmdlet stellt eine Verbindung zu Azure mit einem authentifizierten Konto für die Verwendung mit Azure Resource Manager-Cmdlet-Anforderungen her.</span><span class="sxs-lookup"><span data-stu-id="d8cd8-112">The Connect-AzAccount cmdlet connects to Azure with an authenticated account for use with Azure Resource Manager cmdlet requests.</span></span>
<span data-ttu-id="d8cd8-113">Sie können dieses authentifizierte Konto nur mit Azure Resource Manager-Cmdlets verwenden.</span><span class="sxs-lookup"><span data-stu-id="d8cd8-113">You can use this authenticated account only with Azure Resource Manager cmdlets.</span></span>
<span data-ttu-id="d8cd8-114">Verwenden Sie zum Hinzufügen eines authentifizierten Kontos zur Verwendung mit Dienst Verwaltungs-Cmdlets das Add-AzAccount oder das Import-AzPublishSettingsFile-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d8cd8-114">To add an authenticated account for use with Service Management cmdlets, use the Add-AzAccount or the Import-AzPublishSettingsFile cmdlet.</span></span>
<span data-ttu-id="d8cd8-115">Wenn für den aktuellen Benutzer kein Kontext gefunden wird, füllt dieser Befehl die Kontextliste des Benutzers mit einem Kontext für jedes Ihrer (ersten 25) Abonnements auf.</span><span class="sxs-lookup"><span data-stu-id="d8cd8-115">If no context is found for the current user, this command will populate the user's context list with a context for each of their (first 25) subscriptions.</span></span> <span data-ttu-id="d8cd8-116">Die Liste der für den Benutzer erstellten Kontexte kann durch Ausführen von "Get-AzContext-ListAvailable" gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="d8cd8-116">The list of contexts created for the user can be found by running "Get-AzContext -ListAvailable".</span></span> <span data-ttu-id="d8cd8-117">Um diesen Kontext zu überspringen, können Sie diesen Befehl mit dem Switch-Parameter "-SkipContextPopulation" ausführen.</span><span class="sxs-lookup"><span data-stu-id="d8cd8-117">To skip this context population, you can run this command with the "-SkipContextPopulation" switch parameter.</span></span>
<span data-ttu-id="d8cd8-118">Nachdem Sie dieses Cmdlet ausgeführt haben, können Sie die Verbindung mit einem Azure-Konto mithilfe von Disconnect-AzAccount trennen.</span><span class="sxs-lookup"><span data-stu-id="d8cd8-118">After executing this cmdlet, you can disconnect from an Azure account using Disconnect-AzAccount.</span></span>

## <span data-ttu-id="d8cd8-119">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d8cd8-119">EXAMPLES</span></span>

### <span data-ttu-id="d8cd8-120">Beispiel 1: Verwenden einer interaktiven Anmeldung zum Herstellen einer Verbindung mit einem Azure-Konto</span><span class="sxs-lookup"><span data-stu-id="d8cd8-120">Example 1: Use an interactive login to connect to an Azure account</span></span>
```powershell
PS C:\> Connect-AzAccount

Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

<span data-ttu-id="d8cd8-121">Dieser Befehl stellt eine Verbindung mit einem Azure-Konto her.</span><span class="sxs-lookup"><span data-stu-id="d8cd8-121">This command connects to an Azure account.</span></span>
<span data-ttu-id="d8cd8-122">Zum Ausführen von Azure Resource Manager-Cmdlets mit diesem Konto müssen Sie an der Eingabeaufforderung Microsoft-Konto-oder Organisations-ID-Anmeldeinformationen angeben.</span><span class="sxs-lookup"><span data-stu-id="d8cd8-122">To run Azure Resource Manager cmdlets with this account, you must provide Microsoft account or organizational ID credentials at the prompt.</span></span>
<span data-ttu-id="d8cd8-123">Wenn die mehrstufige Authentifizierung für Ihre Anmeldeinformationen aktiviert ist, müssen Sie sich mit der interaktiven Option anmelden oder die Dienstprinzipal Authentifizierung verwenden.</span><span class="sxs-lookup"><span data-stu-id="d8cd8-123">If multi-factor authentication is enabled for your credentials, you must log in using the interactive option or use service principal authentication.</span></span>

### <span data-ttu-id="d8cd8-124">Beispiel 2: (nur Windows PowerShell 5,1) Herstellen einer Verbindung mit einem Azure-Konto mithilfe der Organisations-ID-Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="d8cd8-124">Example 2: (Windows PowerShell 5.1 only) Connect to an Azure account using organizational ID credentials</span></span>
```powershell
PS C:\> $Credential = Get-Credential
PS C:\> Connect-AzAccount -Credential $Credential

Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

<span data-ttu-id="d8cd8-125">Dieses Szenario funktioniert nur in Windows PowerShell 5,1.</span><span class="sxs-lookup"><span data-stu-id="d8cd8-125">This scenario works only in Windows PowerShell 5.1.</span></span> <span data-ttu-id="d8cd8-126">Mit dem ersten Befehl werden Benutzeranmeldeinformationen (Benutzername und Kennwort) aufgefordert, und Sie werden dann in der $Credential-Variablen gespeichert.</span><span class="sxs-lookup"><span data-stu-id="d8cd8-126">The first command will prompt for user credentials (username and password), and then stores them in the $Credential variable.</span></span>
<span data-ttu-id="d8cd8-127">Der zweite Befehl stellt mithilfe der in $Credential gespeicherten Anmeldeinformationen eine Verbindung mit einem Azure-Konto her.</span><span class="sxs-lookup"><span data-stu-id="d8cd8-127">The second command connects to an Azure account using the credentials stored in $Credential.</span></span>
<span data-ttu-id="d8cd8-128">Dieses Konto authentifiziert sich beim Azure Resource Manager mit den Anmeldeinformationen für die Organisations-ID.</span><span class="sxs-lookup"><span data-stu-id="d8cd8-128">This account authenticates with Azure Resource Manager using organizational ID credentials.</span></span>
<span data-ttu-id="d8cd8-129">Sie können keine mehrstufigen Authentifizierungs-oder Microsoft-Kontoanmeldeinformationen verwenden, um Azure Resource Manager-Cmdlets mit diesem Konto auszuführen.</span><span class="sxs-lookup"><span data-stu-id="d8cd8-129">You cannot use multi-factor authentication or Microsoft account credentials to run Azure Resource Manager cmdlets with this account.</span></span>

### <span data-ttu-id="d8cd8-130">Beispiel 3: Herstellen einer Verbindung mit einem Azure-Dienstprinzipal Konto</span><span class="sxs-lookup"><span data-stu-id="d8cd8-130">Example 3: Connect to an Azure service principal account</span></span>
```powershell
PS C:\> $Credential = Get-Credential
PS C:\> Connect-AzAccount -Credential $Credential -Tenant "xxxx-xxxx-xxxx-xxxx" -ServicePrincipal

Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
xxxx-xxxx-xxxx-xxxx    Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

<span data-ttu-id="d8cd8-131">Der erste Befehl ruft die Anmeldeinformationen des Dienst Prinzipals ab (Anwendungs-ID und Dienstprinzipal Schlüssel) und speichert Sie dann in der $Credential-Variablen.</span><span class="sxs-lookup"><span data-stu-id="d8cd8-131">The first command gets the service principal credentials (application id and service principal secret), and then stores them in the $Credential variable.</span></span>
<span data-ttu-id="d8cd8-132">Der zweite Befehl stellt eine Verbindung mit Azure mithilfe der Dienstprinzipal Anmeldeinformationen her, die in $Credential für den angegebenen Mandanten gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="d8cd8-132">The second command connect to Azure using the service principal credentials stored in $Credential for the specified Tenant.</span></span>
<span data-ttu-id="d8cd8-133">Der ServicePrincipal-Parameter "Switch" gibt an, dass sich das Konto als Dienstprinzipal authentifiziert.</span><span class="sxs-lookup"><span data-stu-id="d8cd8-133">The ServicePrincipal switch parameter indicates that the account authenticates as a service principal.</span></span>

### <span data-ttu-id="d8cd8-134">Beispiel 4: Verwenden einer interaktiven Anmeldung zum Herstellen einer Verbindung mit einem Konto für einen bestimmten Mandanten und ein Abonnement</span><span class="sxs-lookup"><span data-stu-id="d8cd8-134">Example 4: Use an interactive login to connect to an account for a specific tenant and subscription</span></span>
```powershell
PS C:\> Connect-AzAccount -Tenant "xxxx-xxxx-xxxx-xxxx" -SubscriptionId "yyyy-yyyy-yyyy-yyyy"

Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

<span data-ttu-id="d8cd8-135">Dieser Befehl stellt eine Verbindung mit einem Azure-Konto her und konfiguriert AzureRM PowerShell so, dass Cmdlets für den angegebenen Mandanten und das Abonnement standardmäßig ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="d8cd8-135">This command connects to an Azure account and configured AzureRM PowerShell to run cmdlets for the specified tenant and subscription by default.</span></span>

### <span data-ttu-id="d8cd8-136">Beispiel 5: Hinzufügen eines Kontos mit der Anmeldung für die verwaltete Dienstidentität</span><span class="sxs-lookup"><span data-stu-id="d8cd8-136">Example 5: Add an Account Using Managed Service Identity Login</span></span>
```powershell
PS C:\> Connect-AzAccount -Identity

Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
MSI@50342              Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

<span data-ttu-id="d8cd8-137">Dieser Befehl stellt eine Verbindung mit der verwalteten Dienstidentität der Hostumgebung her (Wenn beispielsweise auf einem VirtualMachine mit einer zugewiesenen verwalteten Dienstidentität ausgeführt wird, kann der Code mit dieser zugewiesenen Identität angemeldet werden)</span><span class="sxs-lookup"><span data-stu-id="d8cd8-137">This command connects using the managed service identity of the host environment (for example, if executed on a VirtualMachine with an assigned Managed Service Identity, this will allow the code to login using that assigned identity)</span></span>

### <span data-ttu-id="d8cd8-138">Beispiel 6: Hinzufügen eines Kontos mit der Anmeldung für die verwaltete Dienstidentität und ClientID</span><span class="sxs-lookup"><span data-stu-id="d8cd8-138">Example 6: Add an Account Using Managed Service Identity Login and ClientId</span></span>
```powershell
PS C:\> $identity = Get-AzUserAssignedIdentity -ResourceGroupName "myResourceGroup" -Name "myUserAssignedIdentity"
PS C:\> Get-AzVM -ResourceGroupName contoso -Name testvm | Update-AzVM -IdentityType UserAssigned -IdentityId $identity.Id
PS C:\> Connect-AzAccount -Identity -AccountId $identity.ClientId # Run on the "testvm" virtual machine

Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
yyyy-yyyy-yyyy-yyyy    Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

<span data-ttu-id="d8cd8-139">Dieser Befehl stellt eine Verbindung mit der verwalteten Dienstidentität von "myUserAssignedIdentity" her, indem die dem virtuellen Computer zugewiesene Identität des Benutzers hinzugefügt und dann eine Verbindung mit dem ClientID der Benutzer zugewiesenen Identität hergestellt wird.</span><span class="sxs-lookup"><span data-stu-id="d8cd8-139">This command connects using the managed service identity of "myUserAssignedIdentity" by adding the User Assigned Identity to the Virtual Machine, then connecting using the ClientId of the User Assigned Identity.</span></span>
<span data-ttu-id="d8cd8-140">Weitere Informationen zum Konfigurieren von verwalteten Identitäten finden Sie hier: https://docs.microsoft.com/en-us/azure/active-directory/managed-identities-azure-resources/qs-configure-powershell-windows-vm .</span><span class="sxs-lookup"><span data-stu-id="d8cd8-140">More information about configuring Managed Identities can be found here: https://docs.microsoft.com/en-us/azure/active-directory/managed-identities-azure-resources/qs-configure-powershell-windows-vm.</span></span>

### <span data-ttu-id="d8cd8-141">Beispiel 7: Hinzufügen eines Kontos mit der Anmeldung für die verwaltete Dienstidentität und ClientID</span><span class="sxs-lookup"><span data-stu-id="d8cd8-141">Example 7: Add an Account Using Managed Service Identity Login and ClientId</span></span>
```powershell
PS C:\> $identity = Get-AzUserAssignedIdentity -ResourceGroupName "myResourceGroup" -Name "myUserAssignedIdentity"
PS C:\> Get-AzVM -ResourceGroupName contoso -Name testvm | Update-AzVM -IdentityType UserAssigned -IdentityId $identity.Id
PS C:\> Connect-AzAccount -Identity -AccountId $identity.Id # Run on the "testvm" virtual machine

Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
yyyy-yyyy-yyyy-yyyy    Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

<span data-ttu-id="d8cd8-142">Dieser Befehl stellt eine Verbindung mit der verwalteten Dienstidentität von "myUserAssignedIdentity" her, indem die dem virtuellen Computer zugewiesene Identität des Benutzers hinzugefügt und dann eine Verbindung mit der ID der Benutzer zugewiesenen Identität hergestellt wird.</span><span class="sxs-lookup"><span data-stu-id="d8cd8-142">This command connects using the managed service identity of "myUserAssignedIdentity" by adding the User Assigned Identity to the Virtual Machine, then connecting using the Id of the User Assigned Identity.</span></span>
<span data-ttu-id="d8cd8-143">Weitere Informationen zum Konfigurieren von verwalteten Identitäten finden Sie hier: https://docs.microsoft.com/en-us/azure/active-directory/managed-identities-azure-resources/qs-configure-powershell-windows-vm .</span><span class="sxs-lookup"><span data-stu-id="d8cd8-143">More information about configuring Managed Identities can be found here: https://docs.microsoft.com/en-us/azure/active-directory/managed-identities-azure-resources/qs-configure-powershell-windows-vm.</span></span>

### <span data-ttu-id="d8cd8-144">Beispiel 8: Hinzufügen eines Kontos mithilfe von Zertifikaten</span><span class="sxs-lookup"><span data-stu-id="d8cd8-144">Example 8: Add an account using certificates</span></span>
```powershell
# For more information on creating a self-signed certificate
# and giving it proper permissions, please see the following:
# https://docs.microsoft.com/en-us/azure/active-directory/develop/howto-authenticate-service-principal-powershell
PS C:\> $Thumbprint = "0SZTNJ34TCCMUJ5MJZGR8XQD3S0RVHJBA33Z8ZXV"
PS C:\> $TenantId = "4cd76576-b611-43d0-8f2b-adcb139531bf"
PS C:\> $ApplicationId = "3794a65a-e4e4-493d-ac1d-f04308d712dd"
PS C:\> Connect-AzAccount -CertificateThumbprint $Thumbprint -ApplicationId $ApplicationId -Tenant $TenantId -ServicePrincipal

Account             SubscriptionName TenantId            Environment
-------             ---------------- --------            -----------
xxxx-xxxx-xxxx-xxxx Subscription1    xxxx-xxxx-xxxx-xxxx AzureCloud

Account          : 3794a65a-e4e4-493d-ac1d-f04308d712dd
SubscriptionName : MyTestSubscription
SubscriptionId   : 85f0f653-1f86-4d2c-a9f1-042efc00085c
TenantId         : 4cd76576-b611-43d0-8f2b-adcb139531bf
Environment      : AzureCloud
```

<span data-ttu-id="d8cd8-145">Dieser Befehl stellt mithilfe der zertifikatbasierten Dienstprinzipal Authentifizierung eine Verbindung mit einem Azure-Konto her.</span><span class="sxs-lookup"><span data-stu-id="d8cd8-145">This command connects to an Azure account using certificate-based service principal authentication.</span></span> <span data-ttu-id="d8cd8-146">Der für die Authentifizierung verwendete Dienstprinzipal sollte mit dem angegebenen Zertifikat erstellt worden sein.</span><span class="sxs-lookup"><span data-stu-id="d8cd8-146">The service principal used for authentication should have been created with the given certificate.</span></span>

### <span data-ttu-id="d8cd8-147">Beispiel 9: Hinzufügen eines Kontos mithilfe der Access Token-Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="d8cd8-147">Example 9: Add an account using AccessToken authentication</span></span>
```powershell
PS C:\> $url = "https://login.windows.net/<TenantId>/oauth2/token"
PS C:\> $body = "grant_type=refresh_token&refresh_token=<refreshtoken>" # Refresh token obtained from ~/.azure/TokenCache.dat
PS C:\> $response = Invoke-RestMethod $url -Method POST -Body $body
PS C:\> $AccessToken = $response.access_token
PS C:\> $body1 = $body + "&resource=https%3A%2F%2Fvault.azure.net"
PS C:\> $response = Invoke-RestMethod $url -Method POST -Body $body1
PS C:\> $body2 = $body + "&resource=https%3A%2F%2Fgraph.windows.net"
PS C:\> $GraphAccessToken = $response.access_token
PS C:\> Connect-AzAccount -AccountId "azureuser@contoso.com" -AccessToken $AccessToken -KeyVaultAccessToken $KeyVaultAccessToken -GraphAccessToken $GraphAccessToken -Tenant "xxxx-xxxx-xxxx-xxxx" -SubscriptionId "yyyy-yyyy-yyyy-yyyy"

Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

<span data-ttu-id="d8cd8-148">Dieser Befehl stellt eine Verbindung mit einem Azure-Konto her, das in "Konto-Nr" angegeben ist, wobei Access Token und KeyVaultAccessToken bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="d8cd8-148">This command connects to an Azure account specified in "AccountId" using the AccessToken and KeyVaultAccessToken provided.</span></span>

## <span data-ttu-id="d8cd8-149">Parameter</span><span class="sxs-lookup"><span data-stu-id="d8cd8-149">PARAMETERS</span></span>

### <span data-ttu-id="d8cd8-150">-Access Token</span><span class="sxs-lookup"><span data-stu-id="d8cd8-150">-AccessToken</span></span>
<span data-ttu-id="d8cd8-151">Gibt ein Zugriffstoken an.</span><span class="sxs-lookup"><span data-stu-id="d8cd8-151">Specifies an access token.</span></span>

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

### <span data-ttu-id="d8cd8-152">-Konto-Nr</span><span class="sxs-lookup"><span data-stu-id="d8cd8-152">-AccountId</span></span>
<span data-ttu-id="d8cd8-153">Konto-ID für Zugriffstoken in Access Token-Parametersatz.</span><span class="sxs-lookup"><span data-stu-id="d8cd8-153">Account Id for access token in AccessToken parameter set.</span></span> <span data-ttu-id="d8cd8-154">Konto-ID für verwalteten Dienst in ManagedService-Parametersatz.</span><span class="sxs-lookup"><span data-stu-id="d8cd8-154">Account Id for managed service in ManagedService parameter set.</span></span> <span data-ttu-id="d8cd8-155">Kann eine Ressourcen-ID des verwalteten Diensts oder die zugehörige Client-ID sein. Wenn Sie die SystemAssigned-Identität verwenden möchten, lassen Sie dieses Feld leer.</span><span class="sxs-lookup"><span data-stu-id="d8cd8-155">Can be a managed service resource Id, or the associated client id. To use the SystemAssigned identity, leave this field blank.</span></span>

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

### <span data-ttu-id="d8cd8-156">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="d8cd8-156">-ApplicationId</span></span>
<span data-ttu-id="d8cd8-157">SPN</span><span class="sxs-lookup"><span data-stu-id="d8cd8-157">SPN</span></span>

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

### <span data-ttu-id="d8cd8-158">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="d8cd8-158">-CertificateThumbprint</span></span>
<span data-ttu-id="d8cd8-159">Zertifikat Hash (Fingerabdruck)</span><span class="sxs-lookup"><span data-stu-id="d8cd8-159">Certificate Hash (Thumbprint)</span></span>

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

### <span data-ttu-id="d8cd8-160">-Contextname</span><span class="sxs-lookup"><span data-stu-id="d8cd8-160">-ContextName</span></span>
<span data-ttu-id="d8cd8-161">Der Name des Standardkontexts aus dieser Anmeldung.</span><span class="sxs-lookup"><span data-stu-id="d8cd8-161">Name of the default context from this login.</span></span>  <span data-ttu-id="d8cd8-162">Nachdem Sie sich angemeldet haben, können Sie diesen Kontext mit diesem Namen auswählen.</span><span class="sxs-lookup"><span data-stu-id="d8cd8-162">You will be able to select this context by this name after login.</span></span>

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

### <span data-ttu-id="d8cd8-163">– Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="d8cd8-163">-Credential</span></span>
<span data-ttu-id="d8cd8-164">Gibt ein PSCredential-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="d8cd8-164">Specifies a PSCredential object.</span></span>
<span data-ttu-id="d8cd8-165">Wenn Sie weitere Informationen zum PSCredential-Objekt wünschen, geben Sie Get-Help Get-Credential ein.</span><span class="sxs-lookup"><span data-stu-id="d8cd8-165">For more information about the PSCredential object, type Get-Help Get-Credential.</span></span>
<span data-ttu-id="d8cd8-166">Das PSCredential-Objekt enthält die Benutzer-ID und das Kennwort für die Anmeldeinformationen für die Organisations-ID oder die Anwendungs-ID und den Schlüssel für die Anmeldeinformationen des Dienst Prinzipals.</span><span class="sxs-lookup"><span data-stu-id="d8cd8-166">The PSCredential object provides the user ID and password for organizational ID credentials, or the application ID and secret for service principal credentials.</span></span>

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

### <span data-ttu-id="d8cd8-167">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8cd8-167">-DefaultProfile</span></span>
<span data-ttu-id="d8cd8-168">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d8cd8-168">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d8cd8-169">-Umgebung</span><span class="sxs-lookup"><span data-stu-id="d8cd8-169">-Environment</span></span>
<span data-ttu-id="d8cd8-170">Umgebung mit dem Konto, bei dem Sie sich anmelden können</span><span class="sxs-lookup"><span data-stu-id="d8cd8-170">Environment containing the account to log into</span></span>

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

### <span data-ttu-id="d8cd8-171">-Force</span><span class="sxs-lookup"><span data-stu-id="d8cd8-171">-Force</span></span>
<span data-ttu-id="d8cd8-172">Überschreiben Sie den vorhandenen Kontext mit dem gleichen Namen (sofern vorhanden).</span><span class="sxs-lookup"><span data-stu-id="d8cd8-172">Overwrite the existing context with the same name, if any.</span></span>

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

### <span data-ttu-id="d8cd8-173">-GraphAccessToken</span><span class="sxs-lookup"><span data-stu-id="d8cd8-173">-GraphAccessToken</span></span>
<span data-ttu-id="d8cd8-174">Access Token for Graph-Dienst</span><span class="sxs-lookup"><span data-stu-id="d8cd8-174">AccessToken for Graph Service</span></span>

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

### <span data-ttu-id="d8cd8-175">-Identity</span><span class="sxs-lookup"><span data-stu-id="d8cd8-175">-Identity</span></span>
<span data-ttu-id="d8cd8-176">Melden Sie sich mit der verwalteten Dienstidentität in der aktuellen Umgebung an.</span><span class="sxs-lookup"><span data-stu-id="d8cd8-176">Login using managed service identity in the current environment.</span></span>

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

### <span data-ttu-id="d8cd8-177">-KeyVaultAccessToken</span><span class="sxs-lookup"><span data-stu-id="d8cd8-177">-KeyVaultAccessToken</span></span>
<span data-ttu-id="d8cd8-178">Access Token für keyvault-Dienst</span><span class="sxs-lookup"><span data-stu-id="d8cd8-178">AccessToken for KeyVault Service</span></span>

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

### <span data-ttu-id="d8cd8-179">-ManagedServiceHostName</span><span class="sxs-lookup"><span data-stu-id="d8cd8-179">-ManagedServiceHostName</span></span>
<span data-ttu-id="d8cd8-180">Hostname für Managed Service-Anmeldung</span><span class="sxs-lookup"><span data-stu-id="d8cd8-180">Host name for managed service login</span></span>

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

### <span data-ttu-id="d8cd8-181">-ManagedServicePort</span><span class="sxs-lookup"><span data-stu-id="d8cd8-181">-ManagedServicePort</span></span>
<span data-ttu-id="d8cd8-182">Port Nummer für die Anmeldung des verwalteten Diensts</span><span class="sxs-lookup"><span data-stu-id="d8cd8-182">Port number for managed service login</span></span>

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

### <span data-ttu-id="d8cd8-183">-ManagedServiceSecret</span><span class="sxs-lookup"><span data-stu-id="d8cd8-183">-ManagedServiceSecret</span></span>
<span data-ttu-id="d8cd8-184">Secret, wird für einige Arten von Managed-Service-Anmeldungen verwendet.</span><span class="sxs-lookup"><span data-stu-id="d8cd8-184">Secret, used for some kinds of managed service login.</span></span>

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

### <span data-ttu-id="d8cd8-185">-Scope</span><span class="sxs-lookup"><span data-stu-id="d8cd8-185">-Scope</span></span>
<span data-ttu-id="d8cd8-186">Bestimmt den Bereich von Kontextänderungen, beispielsweise, ob Änderungen nur für den aktuellen Prozess oder für alle von diesem Benutzer gestarteten Sitzungen gelten.</span><span class="sxs-lookup"><span data-stu-id="d8cd8-186">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="d8cd8-187">-ServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="d8cd8-187">-ServicePrincipal</span></span>
<span data-ttu-id="d8cd8-188">Gibt an, dass sich dieses Konto durch die Bereitstellung von Dienstprinzipal Anmeldeinformationen authentifiziert.</span><span class="sxs-lookup"><span data-stu-id="d8cd8-188">Indicates that this account authenticates by providing service principal credentials.</span></span>

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

### <span data-ttu-id="d8cd8-189">-SkipContextPopulation</span><span class="sxs-lookup"><span data-stu-id="d8cd8-189">-SkipContextPopulation</span></span>
<span data-ttu-id="d8cd8-190">Überspringt die Kontext Auffüllung, wenn keine Zusammenhänge gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="d8cd8-190">Skips context population if no contexts are found.</span></span>

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

### <span data-ttu-id="d8cd8-191">-SkipValidation</span><span class="sxs-lookup"><span data-stu-id="d8cd8-191">-SkipValidation</span></span>
<span data-ttu-id="d8cd8-192">Überprüfung für Zugriffstoken überspringen</span><span class="sxs-lookup"><span data-stu-id="d8cd8-192">Skip validation for access token</span></span>

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

### <span data-ttu-id="d8cd8-193">-Abonnement</span><span class="sxs-lookup"><span data-stu-id="d8cd8-193">-Subscription</span></span>
<span data-ttu-id="d8cd8-194">Name oder ID des Abonnements</span><span class="sxs-lookup"><span data-stu-id="d8cd8-194">Subscription Name or ID</span></span>

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

### <span data-ttu-id="d8cd8-195">-Mandant</span><span class="sxs-lookup"><span data-stu-id="d8cd8-195">-Tenant</span></span>
<span data-ttu-id="d8cd8-196">Optionaler Mandantenname oder ID</span><span class="sxs-lookup"><span data-stu-id="d8cd8-196">Optional tenant name or ID</span></span>

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

### <span data-ttu-id="d8cd8-197">-UseDeviceAuthentication</span><span class="sxs-lookup"><span data-stu-id="d8cd8-197">-UseDeviceAuthentication</span></span>
<span data-ttu-id="d8cd8-198">Verwenden der Gerätecode Authentifizierung anstelle eines Browsersteuerelements</span><span class="sxs-lookup"><span data-stu-id="d8cd8-198">Use device code authentication instead of a browser control</span></span>

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

### <span data-ttu-id="d8cd8-199">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d8cd8-199">-Confirm</span></span>
<span data-ttu-id="d8cd8-200">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d8cd8-200">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d8cd8-201">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d8cd8-201">-WhatIf</span></span>
<span data-ttu-id="d8cd8-202">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d8cd8-202">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d8cd8-203">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d8cd8-203">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d8cd8-204">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8cd8-204">CommonParameters</span></span>
<span data-ttu-id="d8cd8-205">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8cd8-205">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8cd8-206">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d8cd8-206">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8cd8-207">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d8cd8-207">INPUTS</span></span>

### <span data-ttu-id="d8cd8-208">System. String</span><span class="sxs-lookup"><span data-stu-id="d8cd8-208">System.String</span></span>

## <span data-ttu-id="d8cd8-209">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d8cd8-209">OUTPUTS</span></span>

### <span data-ttu-id="d8cd8-210">Microsoft. Azure. Commands. profile. Models. Core. PSAzureProfile</span><span class="sxs-lookup"><span data-stu-id="d8cd8-210">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureProfile</span></span>

## <span data-ttu-id="d8cd8-211">Notizen</span><span class="sxs-lookup"><span data-stu-id="d8cd8-211">NOTES</span></span>

## <span data-ttu-id="d8cd8-212">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d8cd8-212">RELATED LINKS</span></span>
