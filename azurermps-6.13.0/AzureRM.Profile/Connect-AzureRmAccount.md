---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/add-azurermaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Connect-AzureRmAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Connect-AzureRmAccount.md
ms.openlocfilehash: a0f29e666a289faddbfce848b97cb0272ce67d0d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664807"
---
# <span data-ttu-id="3b106-101">Connect-AzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="3b106-101">Connect-AzureRmAccount</span></span>

## <span data-ttu-id="3b106-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3b106-102">SYNOPSIS</span></span>
<span data-ttu-id="3b106-103">Herstellen einer Verbindung mit Azure mit einem authentifizierten Konto für die Verwendung mit Azure Resource Manager-Cmdlet-Anforderungen.</span><span class="sxs-lookup"><span data-stu-id="3b106-103">Connect to Azure with an authenticated account for use with Azure Resource Manager cmdlet requests.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3b106-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3b106-104">SYNTAX</span></span>

### <span data-ttu-id="3b106-105">UserWithSubscriptionId (Standard)</span><span class="sxs-lookup"><span data-stu-id="3b106-105">UserWithSubscriptionId (Default)</span></span>
```
Connect-AzureRmAccount [-Environment <String>] [[-Credential] <PSCredential>] [-TenantId <String>]
 [-Subscription <String>] [-ContextName <String>] [-SkipContextPopulation] [-Force]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3b106-106">ServicePrincipalWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3b106-106">ServicePrincipalWithSubscriptionId</span></span>
```
Connect-AzureRmAccount [-Environment <String>] [-Credential] <PSCredential> [-ServicePrincipal]
 -TenantId <String> [-Subscription <String>] [-ContextName <String>] [-SkipContextPopulation] [-Force]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3b106-107">ServicePrincipalCertificateWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3b106-107">ServicePrincipalCertificateWithSubscriptionId</span></span>
```
Connect-AzureRmAccount [-Environment <String>] -CertificateThumbprint <String> -ApplicationId <String>
 [-ServicePrincipal] -TenantId <String> [-Subscription <String>] [-ContextName <String>]
 [-SkipContextPopulation] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3b106-108">AccessTokenWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3b106-108">AccessTokenWithSubscriptionId</span></span>
```
Connect-AzureRmAccount [-Environment <String>] [-TenantId <String>] -AccessToken <String>
 [-GraphAccessToken <String>] [-KeyVaultAccessToken <String>] -AccountId <String> [-Subscription <String>]
 [-ContextName <String>] [-SkipValidation] [-SkipContextPopulation] [-Force]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3b106-109">ManagedServiceLogin</span><span class="sxs-lookup"><span data-stu-id="3b106-109">ManagedServiceLogin</span></span>
```
Connect-AzureRmAccount [-Environment <String>] [-TenantId <String>] [-AccountId <String>] [-Identity]
 [-ManagedServicePort <Int32>] [-ManagedServiceHostName <String>] [-ManagedServiceSecret <SecureString>]
 [-Subscription <String>] [-ContextName <String>] [-SkipContextPopulation] [-Force]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3b106-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3b106-110">DESCRIPTION</span></span>
<span data-ttu-id="3b106-111">Das Connect-AzureRmAccount-Cmdlet stellt eine Verbindung zu Azure mit einem authentifizierten Konto für die Verwendung mit Azure Resource Manager-Cmdlet-Anforderungen her.</span><span class="sxs-lookup"><span data-stu-id="3b106-111">The Connect-AzureRmAccount cmdlet connects to Azure with an authenticated account for use with Azure Resource Manager cmdlet requests.</span></span>
<span data-ttu-id="3b106-112">Sie können dieses authentifizierte Konto nur mit Azure Resource Manager-Cmdlets verwenden.</span><span class="sxs-lookup"><span data-stu-id="3b106-112">You can use this authenticated account only with Azure Resource Manager cmdlets.</span></span>
<span data-ttu-id="3b106-113">Verwenden Sie zum Hinzufügen eines authentifizierten Kontos zur Verwendung mit Dienst Verwaltungs-Cmdlets das Add-AzureAccount oder das Import-AzurePublishSettingsFile-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3b106-113">To add an authenticated account for use with Service Management cmdlets, use the Add-AzureAccount or the Import-AzurePublishSettingsFile cmdlet.</span></span>
<span data-ttu-id="3b106-114">Wenn für den aktuellen Benutzer kein Kontext gefunden wird, füllt dieser Befehl die Kontextliste des Benutzers mit einem Kontext für jedes Ihrer (ersten 25) Abonnements auf.</span><span class="sxs-lookup"><span data-stu-id="3b106-114">If no context is found for the current user, this command will populate the user's context list with a context for each of their (first 25) subscriptions.</span></span> <span data-ttu-id="3b106-115">Die Liste der für den Benutzer erstellten Kontexte kann durch Ausführen von "Get-AzureRmContext-ListAvailable" gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="3b106-115">The list of contexts created for the user can be found by running "Get-AzureRmContext -ListAvailable".</span></span> <span data-ttu-id="3b106-116">Um diesen Kontext zu überspringen, können Sie diesen Befehl mit dem Switch-Parameter "-SkipContextPopulation" ausführen.</span><span class="sxs-lookup"><span data-stu-id="3b106-116">To skip this context population, you can run this command with the "-SkipContextPopulation" switch parameter.</span></span>
<span data-ttu-id="3b106-117">Nachdem Sie dieses Cmdlet ausgeführt haben, können Sie die Verbindung mit einem Azure-Konto mithilfe von Disconnect-AzureRmAccount trennen.</span><span class="sxs-lookup"><span data-stu-id="3b106-117">After executing this cmdlet, you can disconnect from an Azure account using Disconnect-AzureRmAccount.</span></span>

## <span data-ttu-id="3b106-118">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3b106-118">EXAMPLES</span></span>

### <span data-ttu-id="3b106-119">Beispiel 1: Verwenden einer interaktiven Anmeldung zum Herstellen einer Verbindung mit einem Azure-Konto</span><span class="sxs-lookup"><span data-stu-id="3b106-119">Example 1: Use an interactive login to connect to an Azure account</span></span>
```powershell
PS C:\> Connect-AzureRmAccount

Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

<span data-ttu-id="3b106-120">Dieser Befehl stellt eine Verbindung mit einem Azure-Konto her.</span><span class="sxs-lookup"><span data-stu-id="3b106-120">This command connects to an Azure account.</span></span>
<span data-ttu-id="3b106-121">Zum Ausführen von Azure Resource Manager-Cmdlets mit diesem Konto müssen Sie an der Eingabeaufforderung Microsoft-Konto-oder Organisations-ID-Anmeldeinformationen angeben.</span><span class="sxs-lookup"><span data-stu-id="3b106-121">To run Azure Resource Manager cmdlets with this account, you must provide Microsoft account or organizational ID credentials at the prompt.</span></span>
<span data-ttu-id="3b106-122">Wenn die mehrstufige Authentifizierung für Ihre Anmeldeinformationen aktiviert ist, müssen Sie sich mit der interaktiven Option anmelden oder die Dienstprinzipal Authentifizierung verwenden.</span><span class="sxs-lookup"><span data-stu-id="3b106-122">If multi-factor authentication is enabled for your credentials, you must log in using the interactive option or use service principal authentication.</span></span>

### <span data-ttu-id="3b106-123">Beispiel 2: Herstellen einer Verbindung mit einem Azure-Konto mithilfe der Organisations-ID-Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="3b106-123">Example 2: Connect to an Azure account using organizational ID credentials</span></span>
```powershell
PS C:\> $Credential = Get-Credential
PS C:\> Connect-AzureRmAccount -Credential $Credential

Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

<span data-ttu-id="3b106-124">Mit dem ersten Befehl werden Benutzeranmeldeinformationen (Benutzername und Kennwort) aufgefordert, und Sie werden dann in der $Credential-Variablen gespeichert.</span><span class="sxs-lookup"><span data-stu-id="3b106-124">The first command will prompt for user credentials (username and password), and then stores them in the $Credential variable.</span></span>
<span data-ttu-id="3b106-125">Der zweite Befehl stellt mithilfe der in $Credential gespeicherten Anmeldeinformationen eine Verbindung mit einem Azure-Konto her.</span><span class="sxs-lookup"><span data-stu-id="3b106-125">The second command connects to an Azure account using the credentials stored in $Credential.</span></span>
<span data-ttu-id="3b106-126">Dieses Konto authentifiziert sich beim Azure Resource Manager mit den Anmeldeinformationen für die Organisations-ID.</span><span class="sxs-lookup"><span data-stu-id="3b106-126">This account authenticates with Azure Resource Manager using organizational ID credentials.</span></span>
<span data-ttu-id="3b106-127">Sie können keine mehrstufigen Authentifizierungs-oder Microsoft-Kontoanmeldeinformationen verwenden, um Azure Resource Manager-Cmdlets mit diesem Konto auszuführen.</span><span class="sxs-lookup"><span data-stu-id="3b106-127">You cannot use multi-factor authentication or Microsoft account credentials to run Azure Resource Manager cmdlets with this account.</span></span>

### <span data-ttu-id="3b106-128">Beispiel 3: Herstellen einer Verbindung mit einem Azure-Dienstprinzipal Konto</span><span class="sxs-lookup"><span data-stu-id="3b106-128">Example 3: Connect to an Azure service principal account</span></span>
```powershell
PS C:\> $Credential = Get-Credential

PS C:\> Connect-AzureRmAccount -Credential $Credential -Tenant "xxxx-xxxx-xxxx-xxxx" -ServicePrincipal
Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
xxxx-xxxx-xxxx-xxxx    Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

<span data-ttu-id="3b106-129">Der erste Befehl ruft die Anmeldeinformationen des Dienst Prinzipals ab (Anwendungs-ID und Dienstprinzipal Schlüssel) und speichert Sie dann in der $Credential-Variablen.</span><span class="sxs-lookup"><span data-stu-id="3b106-129">The first command gets the service principal credentials (application id and service principal secret), and then stores them in the $Credential variable.</span></span>
<span data-ttu-id="3b106-130">Der zweite Befehl stellt eine Verbindung mit Azure mithilfe der Dienstprinzipal Anmeldeinformationen her, die in $Credential für den angegebenen Mandanten gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="3b106-130">The second command connect to Azure using the service principal credentials stored in $Credential for the specified Tenant.</span></span>
<span data-ttu-id="3b106-131">Der ServicePrincipal-Parameter "Switch" gibt an, dass sich das Konto als Dienstprinzipal authentifiziert.</span><span class="sxs-lookup"><span data-stu-id="3b106-131">The ServicePrincipal switch parameter indicates that the account authenticates as a service principal.</span></span>

### <span data-ttu-id="3b106-132">Beispiel 4: Verwenden einer interaktiven Anmeldung zum Herstellen einer Verbindung mit einem Konto für einen bestimmten Mandanten und ein Abonnement</span><span class="sxs-lookup"><span data-stu-id="3b106-132">Example 4: Use an interactive login to connect to an account for a specific tenant and subscription</span></span>
```powershell
PS C:\> Connect-AzureRmAccount -Tenant "xxxx-xxxx-xxxx-xxxx" -SubscriptionId "yyyy-yyyy-yyyy-yyyy"
Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

<span data-ttu-id="3b106-133">Dieser Befehl stellt eine Verbindung mit einem Azure-Konto her und konfiguriert AzureRM PowerShell so, dass Cmdlets für den angegebenen Mandanten und das Abonnement standardmäßig ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="3b106-133">This command connects to an Azure account and configured AzureRM PowerShell to run cmdlets for the specified tenant and subscription by default.</span></span>

### <span data-ttu-id="3b106-134">Beispiel 5: Hinzufügen eines Kontos mit der Anmeldung für die verwaltete Dienstidentität</span><span class="sxs-lookup"><span data-stu-id="3b106-134">Example 5: Add an Account Using Managed Service Identity Login</span></span>
```powershell
PS C:\> Connect-AzureRmAccount -MSI

Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
MSI@50342              Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

<span data-ttu-id="3b106-135">Dieser Befehl stellt eine Verbindung mit der verwalteten Dienstidentität der Hostumgebung her (Wenn beispielsweise auf einem VirtualMachine mit einer zugewiesenen verwalteten Dienstidentität ausgeführt wird, kann der Code mit dieser zugewiesenen Identität angemeldet werden)</span><span class="sxs-lookup"><span data-stu-id="3b106-135">This command connects using the managed service identity of the host environment (for example, if executed on a VirtualMachine with an assigned Managed Service Identity, this will allow the code to login using that assigned identity)</span></span>

### <span data-ttu-id="3b106-136">Beispiel 6: Hinzufügen eines Kontos mithilfe von Zertifikaten</span><span class="sxs-lookup"><span data-stu-id="3b106-136">Example 6: Add an account using certificates</span></span>
```powershell
# For more information on creating a self-signed certificate
# and giving it proper permissions, please see the following:
# https://docs.microsoft.com/en-us/azure/active-directory/develop/howto-authenticate-service-principal-powershell
PS C:\> $Thumbprint = "0SZTNJ34TCCMUJ5MJZGR8XQD3S0RVHJBA33Z8ZXV"
PS C:\> $TenantId = "4cd76576-b611-43d0-8f2b-adcb139531bf"
PS C:\> $ApplicationId = "3794a65a-e4e4-493d-ac1d-f04308d712dd"
PS C:\> Connect-AzureRmAccount -CertificateThumbprint $Thumbprint -ApplicationId $ApplicationId -Tenant $TenantId -ServicePrincipal

Account             SubscriptionName TenantId            Environment
-------             ---------------- --------            -----------
xxxx-xxxx-xxxx-xxxx Subscription1    xxxx-xxxx-xxxx-xxxx AzureCloud

Account          : 3794a65a-e4e4-493d-ac1d-f04308d712dd
SubscriptionName : MyTestSubscription
SubscriptionId   : 85f0f653-1f86-4d2c-a9f1-042efc00085c
TenantId         : 4cd76576-b611-43d0-8f2b-adcb139531bf
Environment      : AzureCloud
```

<span data-ttu-id="3b106-137">Dieser Befehl stellt mithilfe der zertifikatbasierten Dienstprinzipal Authentifizierung eine Verbindung mit einem Azure-Konto her.</span><span class="sxs-lookup"><span data-stu-id="3b106-137">This command connects to an Azure account using certificate-based service principal authentication.</span></span> <span data-ttu-id="3b106-138">Der für die Authentifizierung verwendete theservice-Prinzipal sollte mit dem angegebenen Zertifikat erstellt worden sein.</span><span class="sxs-lookup"><span data-stu-id="3b106-138">Theservice principal used for authentication should have been created with the given certificate.</span></span>

## <span data-ttu-id="3b106-139">Parameter</span><span class="sxs-lookup"><span data-stu-id="3b106-139">PARAMETERS</span></span>

### <span data-ttu-id="3b106-140">-Access Token</span><span class="sxs-lookup"><span data-stu-id="3b106-140">-AccessToken</span></span>
<span data-ttu-id="3b106-141">Gibt ein Zugriffstoken an.</span><span class="sxs-lookup"><span data-stu-id="3b106-141">Specifies an access token.</span></span>

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

### <span data-ttu-id="3b106-142">-Konto-Nr</span><span class="sxs-lookup"><span data-stu-id="3b106-142">-AccountId</span></span>
<span data-ttu-id="3b106-143">Konto-ID für Zugriffstoken</span><span class="sxs-lookup"><span data-stu-id="3b106-143">Account Id for access token</span></span>

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

### <span data-ttu-id="3b106-144">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="3b106-144">-ApplicationId</span></span>
<span data-ttu-id="3b106-145">SPN</span><span class="sxs-lookup"><span data-stu-id="3b106-145">SPN</span></span>

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

### <span data-ttu-id="3b106-146">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="3b106-146">-CertificateThumbprint</span></span>
<span data-ttu-id="3b106-147">Zertifikat Hash (Fingerabdruck)</span><span class="sxs-lookup"><span data-stu-id="3b106-147">Certificate Hash (Thumbprint)</span></span>

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

### <span data-ttu-id="3b106-148">-Contextname</span><span class="sxs-lookup"><span data-stu-id="3b106-148">-ContextName</span></span>
<span data-ttu-id="3b106-149">Der Name des Standardkontexts aus dieser Anmeldung.</span><span class="sxs-lookup"><span data-stu-id="3b106-149">Name of the default context from this login.</span></span>  <span data-ttu-id="3b106-150">Nachdem Sie sich angemeldet haben, können Sie diesen Kontext mit diesem Namen auswählen.</span><span class="sxs-lookup"><span data-stu-id="3b106-150">You will be able to select this context by this name after login.</span></span>

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

### <span data-ttu-id="3b106-151">– Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="3b106-151">-Credential</span></span>
<span data-ttu-id="3b106-152">Gibt ein PSCredential-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="3b106-152">Specifies a PSCredential object.</span></span>
<span data-ttu-id="3b106-153">Wenn Sie weitere Informationen zum PSCredential-Objekt wünschen, geben Sie Get-Help Get-Credential ein.</span><span class="sxs-lookup"><span data-stu-id="3b106-153">For more information about the PSCredential object, type Get-Help Get-Credential.</span></span>
<span data-ttu-id="3b106-154">Das PSCredential-Objekt enthält die Benutzer-ID und das Kennwort für die Anmeldeinformationen für die Organisations-ID oder die Anwendungs-ID und den Schlüssel für die Anmeldeinformationen des Dienst Prinzipals.</span><span class="sxs-lookup"><span data-stu-id="3b106-154">The PSCredential object provides the user ID and password for organizational ID credentials, or the application ID and secret for service principal credentials.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: UserWithSubscriptionId
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: ServicePrincipalWithSubscriptionId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b106-155">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b106-155">-DefaultProfile</span></span>
<span data-ttu-id="3b106-156">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="3b106-156">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b106-157">-Umgebung</span><span class="sxs-lookup"><span data-stu-id="3b106-157">-Environment</span></span>
<span data-ttu-id="3b106-158">Umgebung mit dem Konto, bei dem Sie sich anmelden können</span><span class="sxs-lookup"><span data-stu-id="3b106-158">Environment containing the account to log into</span></span>

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

### <span data-ttu-id="3b106-159">-Force</span><span class="sxs-lookup"><span data-stu-id="3b106-159">-Force</span></span>
<span data-ttu-id="3b106-160">Überschreiben Sie den vorhandenen Kontext mit dem gleichen Namen (sofern vorhanden).</span><span class="sxs-lookup"><span data-stu-id="3b106-160">Overwrite the existing context with the same name, if any.</span></span>

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

### <span data-ttu-id="3b106-161">-GraphAccessToken</span><span class="sxs-lookup"><span data-stu-id="3b106-161">-GraphAccessToken</span></span>
<span data-ttu-id="3b106-162">Access Token for Graph-Dienst</span><span class="sxs-lookup"><span data-stu-id="3b106-162">AccessToken for Graph Service</span></span>

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

### <span data-ttu-id="3b106-163">-Identity</span><span class="sxs-lookup"><span data-stu-id="3b106-163">-Identity</span></span>
<span data-ttu-id="3b106-164">Melden Sie sich mit der verwalteten Dienstidentität in der aktuellen Umgebung an.</span><span class="sxs-lookup"><span data-stu-id="3b106-164">Login using managed service identity in the current environment.</span></span>

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

### <span data-ttu-id="3b106-165">-KeyVaultAccessToken</span><span class="sxs-lookup"><span data-stu-id="3b106-165">-KeyVaultAccessToken</span></span>
<span data-ttu-id="3b106-166">Access Token für keyvault-Dienst</span><span class="sxs-lookup"><span data-stu-id="3b106-166">AccessToken for KeyVault Service</span></span>

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

### <span data-ttu-id="3b106-167">-ManagedServiceHostName</span><span class="sxs-lookup"><span data-stu-id="3b106-167">-ManagedServiceHostName</span></span>
<span data-ttu-id="3b106-168">Hostname für Managed Service-Anmeldung</span><span class="sxs-lookup"><span data-stu-id="3b106-168">Host name for managed service login</span></span>

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

### <span data-ttu-id="3b106-169">-ManagedServicePort</span><span class="sxs-lookup"><span data-stu-id="3b106-169">-ManagedServicePort</span></span>
<span data-ttu-id="3b106-170">Port Nummer für die Anmeldung des verwalteten Diensts</span><span class="sxs-lookup"><span data-stu-id="3b106-170">Port number for managed service login</span></span>

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

### <span data-ttu-id="3b106-171">-ManagedServiceSecret</span><span class="sxs-lookup"><span data-stu-id="3b106-171">-ManagedServiceSecret</span></span>
<span data-ttu-id="3b106-172">Secret, wird für einige Arten von Managed-Service-Anmeldungen verwendet.</span><span class="sxs-lookup"><span data-stu-id="3b106-172">Secret, used for some kinds of managed service login.</span></span>

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

### <span data-ttu-id="3b106-173">-Scope</span><span class="sxs-lookup"><span data-stu-id="3b106-173">-Scope</span></span>
<span data-ttu-id="3b106-174">Bestimmt den Bereich von Kontextänderungen, beispielsweise, ob Änderungen nur für den aktuellen Prozess oder für alle von diesem Benutzer gestarteten Sitzungen gelten.</span><span class="sxs-lookup"><span data-stu-id="3b106-174">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="3b106-175">-ServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="3b106-175">-ServicePrincipal</span></span>
<span data-ttu-id="3b106-176">Gibt an, dass sich dieses Konto durch die Bereitstellung von Dienstprinzipal Anmeldeinformationen authentifiziert.</span><span class="sxs-lookup"><span data-stu-id="3b106-176">Indicates that this account authenticates by providing service principal credentials.</span></span>

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

### <span data-ttu-id="3b106-177">-SkipContextPopulation</span><span class="sxs-lookup"><span data-stu-id="3b106-177">-SkipContextPopulation</span></span>
<span data-ttu-id="3b106-178">Überspringt die Kontext Auffüllung, wenn keine Zusammenhänge gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="3b106-178">Skips context population if no contexts are found.</span></span>

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

### <span data-ttu-id="3b106-179">-SkipValidation</span><span class="sxs-lookup"><span data-stu-id="3b106-179">-SkipValidation</span></span>
<span data-ttu-id="3b106-180">Überprüfung für Zugriffstoken überspringen</span><span class="sxs-lookup"><span data-stu-id="3b106-180">Skip validation for access token</span></span>

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

### <span data-ttu-id="3b106-181">-Abonnement</span><span class="sxs-lookup"><span data-stu-id="3b106-181">-Subscription</span></span>
<span data-ttu-id="3b106-182">Name oder ID des Abonnements</span><span class="sxs-lookup"><span data-stu-id="3b106-182">Subscription Name or ID</span></span>

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

### <span data-ttu-id="3b106-183">-Mandanten-Nr</span><span class="sxs-lookup"><span data-stu-id="3b106-183">-TenantId</span></span>
<span data-ttu-id="3b106-184">Optionaler Domänenname oder Mandanten-ID.</span><span class="sxs-lookup"><span data-stu-id="3b106-184">Optional domain name or tenant ID.</span></span> <span data-ttu-id="3b106-185">Der Domänenname funktioniert nicht in allen Anmelde Situationen.</span><span class="sxs-lookup"><span data-stu-id="3b106-185">Domain name will not work in all sign-in situations.</span></span> <span data-ttu-id="3b106-186">Für die Anmeldung im Cloud Solution Provider (CSP) ist die Mandanten-ID erforderlich.</span><span class="sxs-lookup"><span data-stu-id="3b106-186">For Cloud Solution Provider (CSP) sign-in, tenant ID is required.</span></span>

```yaml
Type: System.String
Parameter Sets: UserWithSubscriptionId, AccessTokenWithSubscriptionId, ManagedServiceLogin
Aliases: Domain

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ServicePrincipalWithSubscriptionId, ServicePrincipalCertificateWithSubscriptionId
Aliases: Domain

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b106-187">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="3b106-187">-Confirm</span></span>
<span data-ttu-id="3b106-188">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3b106-188">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3b106-189">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3b106-189">-WhatIf</span></span>
<span data-ttu-id="3b106-190">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3b106-190">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3b106-191">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3b106-191">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3b106-192">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b106-192">CommonParameters</span></span>
<span data-ttu-id="3b106-193">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3b106-193">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b106-194">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3b106-194">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b106-195">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3b106-195">INPUTS</span></span>

### <span data-ttu-id="3b106-196">System. String</span><span class="sxs-lookup"><span data-stu-id="3b106-196">System.String</span></span>
<span data-ttu-id="3b106-197">Parameter: Abonnement (ByValue)</span><span class="sxs-lookup"><span data-stu-id="3b106-197">Parameters: Subscription (ByValue)</span></span>

## <span data-ttu-id="3b106-198">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3b106-198">OUTPUTS</span></span>

### <span data-ttu-id="3b106-199">Microsoft. Azure. Commands. profile. Models. PSAzureProfile</span><span class="sxs-lookup"><span data-stu-id="3b106-199">Microsoft.Azure.Commands.Profile.Models.PSAzureProfile</span></span>

## <span data-ttu-id="3b106-200">Notizen</span><span class="sxs-lookup"><span data-stu-id="3b106-200">NOTES</span></span>

## <span data-ttu-id="3b106-201">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3b106-201">RELATED LINKS</span></span>
