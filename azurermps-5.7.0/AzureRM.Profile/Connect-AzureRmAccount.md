---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/add-azurermaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Connect-AzureRmAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Connect-AzureRmAccount.md
ms.openlocfilehash: 01cc9210e57edbb19caa8406e9015b36942b99d4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93476689"
---
# <span data-ttu-id="93825-101">Connect-AzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="93825-101">Connect-AzureRmAccount</span></span>

## <span data-ttu-id="93825-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="93825-102">SYNOPSIS</span></span>
<span data-ttu-id="93825-103">Herstellen einer Verbindung mit Azure mit einem authentifizierten Konto für die Verwendung mit Azure Resource Manager-Cmdlet-Anforderungen.</span><span class="sxs-lookup"><span data-stu-id="93825-103">Connect to Azure with an authenticated account for use with Azure Resource Manager cmdlet requests.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="93825-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="93825-104">SYNTAX</span></span>

### <span data-ttu-id="93825-105">UserWithSubscriptionId (Standard)</span><span class="sxs-lookup"><span data-stu-id="93825-105">UserWithSubscriptionId (Default)</span></span>
```
Connect-AzureRmAccount [-Environment <String>] [[-Credential] <PSCredential>] [-TenantId <String>]
 [-Subscription <String>] [-ContextName <String>] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="93825-106">ServicePrincipalWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="93825-106">ServicePrincipalWithSubscriptionId</span></span>
```
Connect-AzureRmAccount [-Environment <String>] [-Credential] <PSCredential> [-ServicePrincipal]
 -TenantId <String> [-Subscription <String>] [-ContextName <String>] [-Force]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="93825-107">ServicePrincipalCertificateWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="93825-107">ServicePrincipalCertificateWithSubscriptionId</span></span>
```
Connect-AzureRmAccount [-Environment <String>] -CertificateThumbprint <String> -ApplicationId <String>
 [-ServicePrincipal] -TenantId <String> [-Subscription <String>] [-ContextName <String>] [-Force]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="93825-108">AccessTokenWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="93825-108">AccessTokenWithSubscriptionId</span></span>
```
Connect-AzureRmAccount [-Environment <String>] [-TenantId <String>] -AccessToken <String>
 [-GraphAccessToken <String>] [-KeyVaultAccessToken <String>] -AccountId <String> [-Subscription <String>]
 [-ContextName <String>] [-SkipValidation] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="93825-109">ManagedServiceLogin</span><span class="sxs-lookup"><span data-stu-id="93825-109">ManagedServiceLogin</span></span>
```
Connect-AzureRmAccount [-Environment <String>] [-TenantId <String>] [-AccountId <String>] [-Identity]
 [-ManagedServicePort <Int32>] [-ManagedServiceHostName <String>] [-Subscription <String>]
 [-ContextName <String>] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="93825-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="93825-110">DESCRIPTION</span></span>
<span data-ttu-id="93825-111">Das Connect-AzureRmAccount-Cmdlet stellt eine Verbindung zu Azure mit einem authentifizierten Konto für die Verwendung mit Azure Resource Manager-Cmdlet-Anforderungen her.</span><span class="sxs-lookup"><span data-stu-id="93825-111">The Connect-AzureRmAccount cmdlet connects to Azure with an authenticated account for use with Azure Resource Manager cmdlet requests.</span></span>

<span data-ttu-id="93825-112">Sie können dieses authentifizierte Konto nur mit Azure Resource Manager-Cmdlets verwenden.</span><span class="sxs-lookup"><span data-stu-id="93825-112">You can use this authenticated account only with Azure Resource Manager cmdlets.</span></span>

<span data-ttu-id="93825-113">Verwenden Sie zum Hinzufügen eines authentifizierten Kontos zur Verwendung mit Dienst Verwaltungs-Cmdlets das Add-AzureAccount oder das Import-AzurePublishSettingsFile-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="93825-113">To add an authenticated account for use with Service Management cmdlets, use the Add-AzureAccount or the Import-AzurePublishSettingsFile cmdlet.</span></span>

<span data-ttu-id="93825-114">Nachdem Sie dieses Cmdlet ausgeführt haben, können Sie die Verbindung mit einem Azure-Konto mithilfe von Disconnect-AzureRmAccount trennen.</span><span class="sxs-lookup"><span data-stu-id="93825-114">After executing this cmdlet, you can disconnect from an Azure account using Disconnect-AzureRmAccount.</span></span>

## <span data-ttu-id="93825-115">Beispiele</span><span class="sxs-lookup"><span data-stu-id="93825-115">EXAMPLES</span></span>

### <span data-ttu-id="93825-116">Beispiel 1: Verwenden einer interaktiven Anmeldung zum Herstellen einer Verbindung mit einem Azure-Konto</span><span class="sxs-lookup"><span data-stu-id="93825-116">Example 1: Use an interactive login to connect to an Azure account</span></span>
```
PS C:\> Connect-AzureRmAccount
Account: azureuser@contoso.com
Environment: AzureCloud
Subscription: xxxx-xxxx-xxxx-xxxx
Tenant: xxxx-xxxx-xxxx-xxxx
```

<span data-ttu-id="93825-117">Dieser Befehl stellt eine Verbindung mit einem Azure-Konto her.</span><span class="sxs-lookup"><span data-stu-id="93825-117">This command connects to an Azure account.</span></span>

<span data-ttu-id="93825-118">Zum Ausführen von Azure Resource Manager-Cmdlets mit diesem Konto müssen Sie an der Eingabeaufforderung Microsoft-Konto-oder Organisations-ID-Anmeldeinformationen angeben.</span><span class="sxs-lookup"><span data-stu-id="93825-118">To run Azure Resource Manager cmdlets with this account, you must provide Microsoft account or organizational ID credentials at the prompt.</span></span>

<span data-ttu-id="93825-119">Wenn die mehrstufige Authentifizierung für Ihre Anmeldeinformationen aktiviert ist, müssen Sie sich mit der interaktiven Option anmelden oder die Dienstprinzipal Authentifizierung verwenden.</span><span class="sxs-lookup"><span data-stu-id="93825-119">If multi-factor authentication is enabled for your credentials, you must log in using the interactive option or use service principal authentication.</span></span>

### <span data-ttu-id="93825-120">Beispiel 2: Herstellen einer Verbindung mit einem Azure-Konto mithilfe der Organisations-ID-Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="93825-120">Example 2: Connect to an Azure account using organizational ID credentials</span></span>
```
PS C:\> $Credential = Get-Credential
PS C:\> Connect-AzureRmAccount -Credential $Credential
Account: azureuser@contoso.com
Environment: AzureChinaCloud
Subscription: xxxx-xxxx-xxxx-xxxx
Tenant: xxxx-xxxx-xxxx-xxxx
```

<span data-ttu-id="93825-121">Der erste Befehl ruft die Anmeldeinformationen des Benutzers ab und speichert Sie dann in der $Credential-Variablen.</span><span class="sxs-lookup"><span data-stu-id="93825-121">The first command gets the user credentials, and then stores them in the $Credential variable.</span></span>

<span data-ttu-id="93825-122">Der zweite Befehl stellt mithilfe der in $Credential gespeicherten Anmeldeinformationen eine Verbindung mit einem Azure-Konto her.</span><span class="sxs-lookup"><span data-stu-id="93825-122">The second command connects to an Azure account using the credentials stored in $Credential.</span></span>

<span data-ttu-id="93825-123">Dieses Konto authentifiziert sich beim Azure Resource Manager mit den Anmeldeinformationen für die Organisations-ID.</span><span class="sxs-lookup"><span data-stu-id="93825-123">This account authenticates with Azure Resource Manager using organizational ID credentials.</span></span>

<span data-ttu-id="93825-124">Sie können keine mehrstufigen Authentifizierungs-oder Microsoft-Kontoanmeldeinformationen verwenden, um Azure Resource Manager-Cmdlets mit diesem Konto auszuführen.</span><span class="sxs-lookup"><span data-stu-id="93825-124">You cannot use multi-factor authentication or Microsoft account credentials to run Azure Resource Manager cmdlets with this account.</span></span>

### <span data-ttu-id="93825-125">Beispiel 3: Herstellen einer Verbindung mit einem Azure-Dienstprinzipal Konto</span><span class="sxs-lookup"><span data-stu-id="93825-125">Example 3: Connect to an Azure service principal account</span></span>
```
PS C:\> $Credential = Get-Credential
PS C:\> Connect-AzureRmAccount -Credential $Credential -Tenant "xxxx-xxxx-xxxx-xxxx" -ServicePrincipal
Account: xxxx-xxxx-xxxx-xxxx
Environment: AzureCloud
Subscription: yyyy-yyyy-yyyy-yyyy
Tenant: xxxx-xxxx-xxxx-xxxx
```

<span data-ttu-id="93825-126">Der erste Befehl ruft die Anmeldeinformationen des Benutzers ab und speichert Sie dann in der $Credential-Variablen.</span><span class="sxs-lookup"><span data-stu-id="93825-126">The first command gets the user credentials, and then stores them in the $Credential variable.</span></span>

<span data-ttu-id="93825-127">Der zweite Befehl stellt eine Verbindung mit Azure mithilfe der Dienstprinzipal Anmeldeinformationen her, die in $Credential für den angegebenen Mandanten gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="93825-127">The second command connect to Azure using the service principal credentials stored in $Credential for the specified Tenant.</span></span>

<span data-ttu-id="93825-128">Der ServicePrincipal-Parameter "Switch" gibt an, dass sich das Konto als Dienstprinzipal authentifiziert.</span><span class="sxs-lookup"><span data-stu-id="93825-128">The ServicePrincipal switch parameter indicates that the account authenticates as a service principal.</span></span>

### <span data-ttu-id="93825-129">Beispiel 4: Verwenden einer interaktiven Anmeldung zum Herstellen einer Verbindung mit einem Konto für einen bestimmten Mandanten und ein Abonnement</span><span class="sxs-lookup"><span data-stu-id="93825-129">Example 4: Use an interactive login to connect to an account for a specific tenant and subscription</span></span>
```
PS C:\> Connect-AzureRmAccount -Tenant "xxxx-xxxx-xxxx-xxxx" -SubscriptionId "yyyy-yyyy-yyyy-yyyy"
Account: pfuller@contoso.com
Environment: AzureCloud
Subscription: yyyy-yyyy-yyyy-yyyy
Tenant: xxxx-xxxx-xxxx-xxxx
```

<span data-ttu-id="93825-130">Dieser Befehl stellt eine Verbindung mit einem Azure-Konto her und konfiguriert AzureRM PowerShell so, dass Cmdlets für den angegebenen Mandanten und das Abonnement standardmäßig ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="93825-130">This command connects to an Azure account and configured AzureRM PowerShell to run cmdlets for the specified tenant and subscription by default.</span></span>

### <span data-ttu-id="93825-131">Beispiel 5: Hinzufügen eines Kontos mit der Anmeldung für die verwaltete Dienstidentität</span><span class="sxs-lookup"><span data-stu-id="93825-131">Example 5: Add an Account Using Managed Service Identity Login</span></span>
```
PS C:\>Add-AzureRmAccount -MSI
Account: MSI@50342
Environment: AzureCloud
Subscription: yyyy-yyyy-yyyy-yyyy
Tenant: xxxx-xxxx-xxxx-xxxx
```

<span data-ttu-id="93825-132">Dieser Befehl meldet sich mit der verwalteten Dienstidentität der Hostumgebung an (Wenn beispielsweise auf einem VirtualMachine mit einer zugewiesenen verwalteten Dienstidentität ausgeführt wird, kann der Code mit dieser zugewiesenen Identität angemeldet werden)</span><span class="sxs-lookup"><span data-stu-id="93825-132">This command logs in using the managed service identity of the host environment (for example, if executed on a VirtualMachine with an assigned Managed Service Identity, this will allow the code to login using that assigned identity)</span></span>

## <span data-ttu-id="93825-133">Parameter</span><span class="sxs-lookup"><span data-stu-id="93825-133">PARAMETERS</span></span>

### <span data-ttu-id="93825-134">-Access Token</span><span class="sxs-lookup"><span data-stu-id="93825-134">-AccessToken</span></span>
<span data-ttu-id="93825-135">Gibt ein Zugriffstoken an.</span><span class="sxs-lookup"><span data-stu-id="93825-135">Specifies an access token.</span></span>

```yaml
Type: String
Parameter Sets: AccessTokenWithSubscriptionId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93825-136">-Konto-Nr</span><span class="sxs-lookup"><span data-stu-id="93825-136">-AccountId</span></span>
<span data-ttu-id="93825-137">Konto-ID für Zugriffstoken</span><span class="sxs-lookup"><span data-stu-id="93825-137">Account Id for access token</span></span>

```yaml
Type: String
Parameter Sets: AccessTokenWithSubscriptionId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ManagedServiceLogin
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93825-138">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="93825-138">-ApplicationId</span></span>
<span data-ttu-id="93825-139">SPN</span><span class="sxs-lookup"><span data-stu-id="93825-139">SPN</span></span>

```yaml
Type: String
Parameter Sets: ServicePrincipalCertificateWithSubscriptionId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93825-140">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="93825-140">-CertificateThumbprint</span></span>
<span data-ttu-id="93825-141">Zertifikat Hash (Fingerabdruck)</span><span class="sxs-lookup"><span data-stu-id="93825-141">Certificate Hash (Thumbprint)</span></span>

```yaml
Type: String
Parameter Sets: ServicePrincipalCertificateWithSubscriptionId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93825-142">-Contextname</span><span class="sxs-lookup"><span data-stu-id="93825-142">-ContextName</span></span>
<span data-ttu-id="93825-143">Der Name des Standardkontexts aus dieser Anmeldung.</span><span class="sxs-lookup"><span data-stu-id="93825-143">Name of the default context from this login.</span></span>  <span data-ttu-id="93825-144">Nachdem Sie sich angemeldet haben, können Sie diesen Kontext mit diesem Namen auswählen.</span><span class="sxs-lookup"><span data-stu-id="93825-144">You will be able to select this context by this name after login.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93825-145">– Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="93825-145">-Credential</span></span>
<span data-ttu-id="93825-146">Gibt ein PSCredential-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="93825-146">Specifies a PSCredential object.</span></span>
<span data-ttu-id="93825-147">Wenn Sie weitere Informationen zum PSCredential-Objekt wünschen, geben Sie Get-Help Get-Credential ein.</span><span class="sxs-lookup"><span data-stu-id="93825-147">For more information about the PSCredential object, type Get-Help Get-Credential.</span></span>

<span data-ttu-id="93825-148">Das PSCredential-Objekt enthält die Benutzer-ID und das Kennwort für die Anmeldeinformationen für die Organisations-ID oder die Anwendungs-ID und den Schlüssel für die Anmeldeinformationen des Dienst Prinzipals.</span><span class="sxs-lookup"><span data-stu-id="93825-148">The PSCredential object provides the user ID and password for organizational ID credentials, or the application ID and secret for service principal credentials.</span></span>

```yaml
Type: PSCredential
Parameter Sets: UserWithSubscriptionId
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: PSCredential
Parameter Sets: ServicePrincipalWithSubscriptionId
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93825-149">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93825-149">-DefaultProfile</span></span>
<span data-ttu-id="93825-150">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="93825-150">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93825-151">-Umgebung</span><span class="sxs-lookup"><span data-stu-id="93825-151">-Environment</span></span>
<span data-ttu-id="93825-152">Umgebung mit dem Konto, bei dem Sie sich anmelden können</span><span class="sxs-lookup"><span data-stu-id="93825-152">Environment containing the account to log into</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: EnvironmentName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93825-153">-Force</span><span class="sxs-lookup"><span data-stu-id="93825-153">-Force</span></span>
<span data-ttu-id="93825-154">Überschreiben Sie den vorhandenen Kontext mit dem gleichen Namen (sofern vorhanden).</span><span class="sxs-lookup"><span data-stu-id="93825-154">Overwrite the existing context with the same name, if any.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93825-155">-GraphAccessToken</span><span class="sxs-lookup"><span data-stu-id="93825-155">-GraphAccessToken</span></span>
<span data-ttu-id="93825-156">Access Token for Graph-Dienst</span><span class="sxs-lookup"><span data-stu-id="93825-156">AccessToken for Graph Service</span></span>

```yaml
Type: String
Parameter Sets: AccessTokenWithSubscriptionId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93825-157">-Identity</span><span class="sxs-lookup"><span data-stu-id="93825-157">-Identity</span></span>
<span data-ttu-id="93825-158">Melden Sie sich mit der verwalteten Dienstidentität in der aktuellen Umgebung an.</span><span class="sxs-lookup"><span data-stu-id="93825-158">Login using managed service identity in the current environment.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ManagedServiceLogin
Aliases: MSI, ManagedService

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93825-159">-KeyVaultAccessToken</span><span class="sxs-lookup"><span data-stu-id="93825-159">-KeyVaultAccessToken</span></span>
<span data-ttu-id="93825-160">Access Token für keyvault-Dienst</span><span class="sxs-lookup"><span data-stu-id="93825-160">AccessToken for KeyVault Service</span></span>

```yaml
Type: String
Parameter Sets: AccessTokenWithSubscriptionId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93825-161">-ManagedServiceHostName</span><span class="sxs-lookup"><span data-stu-id="93825-161">-ManagedServiceHostName</span></span>
<span data-ttu-id="93825-162">Hostname für Managed Service-Anmeldung</span><span class="sxs-lookup"><span data-stu-id="93825-162">Host name for managed service login</span></span>

```yaml
Type: String
Parameter Sets: ManagedServiceLogin
Aliases: 

Required: False
Position: Named
Default value: localhost
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93825-163">-ManagedServicePort</span><span class="sxs-lookup"><span data-stu-id="93825-163">-ManagedServicePort</span></span>
<span data-ttu-id="93825-164">Port Nummer für die Anmeldung des verwalteten Diensts</span><span class="sxs-lookup"><span data-stu-id="93825-164">Port number for managed service login</span></span>

```yaml
Type: Int32
Parameter Sets: ManagedServiceLogin
Aliases: 

Required: False
Position: Named
Default value: 50342
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93825-165">-Scope</span><span class="sxs-lookup"><span data-stu-id="93825-165">-Scope</span></span>
<span data-ttu-id="93825-166">Bestimmt den Bereich von Kontextänderungen, beispielsweise, ob Änderungen nur für den aktuellen Prozess oder für alle von diesem Benutzer gestarteten Sitzungen gelten.</span><span class="sxs-lookup"><span data-stu-id="93825-166">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

```yaml
Type: ContextModificationScope
Parameter Sets: (All)
Aliases: 
Accepted values: Process, CurrentUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93825-167">-ServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="93825-167">-ServicePrincipal</span></span>
<span data-ttu-id="93825-168">Gibt an, dass sich dieses Konto durch die Bereitstellung von Dienstprinzipal Anmeldeinformationen authentifiziert.</span><span class="sxs-lookup"><span data-stu-id="93825-168">Indicates that this account authenticates by providing service principal credentials.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ServicePrincipalWithSubscriptionId, ServicePrincipalCertificateWithSubscriptionId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93825-169">-SkipValidation</span><span class="sxs-lookup"><span data-stu-id="93825-169">-SkipValidation</span></span>
<span data-ttu-id="93825-170">Überprüfung für Zugriffstoken überspringen</span><span class="sxs-lookup"><span data-stu-id="93825-170">Skip validation for access token</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: AccessTokenWithSubscriptionId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93825-171">-Abonnement</span><span class="sxs-lookup"><span data-stu-id="93825-171">-Subscription</span></span>
<span data-ttu-id="93825-172">Name oder ID des Abonnements</span><span class="sxs-lookup"><span data-stu-id="93825-172">Subscription Name or ID</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SubscriptionName, SubscriptionId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="93825-173">-Mandanten-Nr</span><span class="sxs-lookup"><span data-stu-id="93825-173">-TenantId</span></span>
<span data-ttu-id="93825-174">Optionaler Mandantenname oder ID</span><span class="sxs-lookup"><span data-stu-id="93825-174">Optional tenant name or ID</span></span>

```yaml
Type: String
Parameter Sets: UserWithSubscriptionId, AccessTokenWithSubscriptionId, ManagedServiceLogin
Aliases: Domain

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ServicePrincipalWithSubscriptionId, ServicePrincipalCertificateWithSubscriptionId
Aliases: Domain

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93825-175">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="93825-175">-Confirm</span></span>
<span data-ttu-id="93825-176">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="93825-176">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93825-177">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="93825-177">-WhatIf</span></span>
<span data-ttu-id="93825-178">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="93825-178">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="93825-179">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="93825-179">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93825-180">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93825-180">CommonParameters</span></span>
<span data-ttu-id="93825-181">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="93825-181">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93825-182">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="93825-182">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93825-183">Eingaben</span><span class="sxs-lookup"><span data-stu-id="93825-183">INPUTS</span></span>

### <span data-ttu-id="93825-184">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="93825-184">String</span></span>
<span data-ttu-id="93825-185">Der Parameter "Abonnement-Nr" akzeptiert den Wert vom Typ "Zeichenfolge" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="93825-185">Parameter 'SubscriptionId' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="93825-186">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="93825-186">String</span></span>
<span data-ttu-id="93825-187">Der Parameter "subscriptionname" akzeptiert den Wert vom Typ "Zeichenfolge" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="93825-187">Parameter 'SubscriptionName' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="93825-188">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="93825-188">OUTPUTS</span></span>

### <span data-ttu-id="93825-189">PSAzureProfile</span><span class="sxs-lookup"><span data-stu-id="93825-189">PSAzureProfile</span></span>
<span data-ttu-id="93825-190">Informationen zu Anmeldeinformationen, Abonnements, Konten und Mandanten für den angemeldeten Benutzer.</span><span class="sxs-lookup"><span data-stu-id="93825-190">Credentials, subscription, account, and tenant information for the logged in user.</span></span>

## <span data-ttu-id="93825-191">Notizen</span><span class="sxs-lookup"><span data-stu-id="93825-191">NOTES</span></span>

## <span data-ttu-id="93825-192">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="93825-192">RELATED LINKS</span></span>

