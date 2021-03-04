---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/powershell/module/az.accounts/connect-azaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Connect-AzAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Connect-AzAccount.md
ms.openlocfilehash: dcf4e78e9b6e467961eb05dd141396e426dfe5e7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101943227"
---
# <span data-ttu-id="16a45-101">Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="16a45-101">Connect-AzAccount</span></span>

## <span data-ttu-id="16a45-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="16a45-102">SYNOPSIS</span></span>
<span data-ttu-id="16a45-103">Stellen Sie eine Verbindung mit Azure mit einem authentifizierten Konto zur Verwendung mit Cmdlets aus den Az-PowerShell-Modulen bereit.</span><span class="sxs-lookup"><span data-stu-id="16a45-103">Connect to Azure with an authenticated account for use with cmdlets from the Az PowerShell modules.</span></span>

## <span data-ttu-id="16a45-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="16a45-104">SYNTAX</span></span>

### <span data-ttu-id="16a45-105">UserWithSubscriptionId (Standard)</span><span class="sxs-lookup"><span data-stu-id="16a45-105">UserWithSubscriptionId (Default)</span></span>
```
Connect-AzAccount [-Environment <String>] [-Tenant <String>] [-Subscription <String>] [-ContextName <String>]
 [-SkipContextPopulation] [-MaxContextPopulation <Int32>] [-UseDeviceAuthentication] [-Force]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="16a45-106">ServicePrincipalWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="16a45-106">ServicePrincipalWithSubscriptionId</span></span>
```
Connect-AzAccount [-Environment <String>] -Credential <PSCredential> [-ServicePrincipal] -Tenant <String>
 [-Subscription <String>] [-ContextName <String>] [-SkipContextPopulation] [-MaxContextPopulation <Int32>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="16a45-107">UserWithCredential</span><span class="sxs-lookup"><span data-stu-id="16a45-107">UserWithCredential</span></span>
```
Connect-AzAccount [-Environment <String>] -Credential <PSCredential> [-Tenant <String>]
 [-Subscription <String>] [-ContextName <String>] [-SkipContextPopulation] [-MaxContextPopulation <Int32>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="16a45-108">ServicePrincipalCertificateWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="16a45-108">ServicePrincipalCertificateWithSubscriptionId</span></span>
```
Connect-AzAccount [-Environment <String>] -CertificateThumbprint <String> -ApplicationId <String>
 [-ServicePrincipal] -Tenant <String> [-Subscription <String>] [-ContextName <String>] [-SkipContextPopulation]
 [-MaxContextPopulation <Int32>] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="16a45-109">AccessTokenWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="16a45-109">AccessTokenWithSubscriptionId</span></span>
```
Connect-AzAccount [-Environment <String>] [-Tenant <String>] -AccessToken <String> [-GraphAccessToken <String>]
 [-KeyVaultAccessToken <String>] -AccountId <String> [-Subscription <String>] [-ContextName <String>]
 [-SkipValidation] [-SkipContextPopulation] [-MaxContextPopulation <Int32>] [-Force]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="16a45-110">ManagedServiceLogin</span><span class="sxs-lookup"><span data-stu-id="16a45-110">ManagedServiceLogin</span></span>
```
Connect-AzAccount [-Environment <String>] [-Tenant <String>] [-AccountId <String>] [-Identity]
 [-ManagedServicePort <Int32>] [-ManagedServiceHostName <String>] [-ManagedServiceSecret <SecureString>]
 [-Subscription <String>] [-ContextName <String>] [-SkipContextPopulation] [-MaxContextPopulation <Int32>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="16a45-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="16a45-111">DESCRIPTION</span></span>

<span data-ttu-id="16a45-112">Das Cmdlet stellt eine Verbindung mit Azure mit einem authentifizierten Konto zur Verwendung mit `Connect-AzAccount` Cmdlets aus den Az-PowerShell-Modulen bereit.</span><span class="sxs-lookup"><span data-stu-id="16a45-112">The `Connect-AzAccount` cmdlet connects to Azure with an authenticated account for use with cmdlets from the Az PowerShell modules.</span></span> <span data-ttu-id="16a45-113">Sie können dieses authentifizierte Konto nur mit Azure Resource Manager-Anforderungen verwenden.</span><span class="sxs-lookup"><span data-stu-id="16a45-113">You can use this authenticated account only with Azure Resource Manager requests.</span></span> <span data-ttu-id="16a45-114">Zum Hinzufügen eines authentifizierten Kontos für die Verwendung mit der Dienstverwaltung verwenden Sie das `Add-AzureAccount` Cmdlet aus dem Azure PowerShell-Modul.</span><span class="sxs-lookup"><span data-stu-id="16a45-114">To add an authenticated account for use with Service Management, use the `Add-AzureAccount` cmdlet from the Azure PowerShell module.</span></span> <span data-ttu-id="16a45-115">Wenn für den aktuellen Benutzer kein Kontext gefunden wird, wird die Kontextliste des Benutzers mit einem Kontext für jedes seiner ersten 25 Abonnements gefüllt.</span><span class="sxs-lookup"><span data-stu-id="16a45-115">If no context is found for the current user, the user's context list is populated with a context for each of their first 25 subscriptions.</span></span>
<span data-ttu-id="16a45-116">Die Liste der kontextbezogenen Kontexte, die für den Benutzer erstellt wurden, finden Sie unter `Get-AzContext -ListAvailable` Ausführen von .</span><span class="sxs-lookup"><span data-stu-id="16a45-116">The list of contexts created for the user can be found by running `Get-AzContext -ListAvailable`.</span></span> <span data-ttu-id="16a45-117">Um diese Kontextgesamtheit zu überspringen, geben Sie den **Switchparameter SkipContextPopulation** an.</span><span class="sxs-lookup"><span data-stu-id="16a45-117">To skip this context population, specify the **SkipContextPopulation** switch parameter.</span></span> <span data-ttu-id="16a45-118">Nachdem Sie dieses Cmdlet ausgeführt haben, können Sie die Verbindung mit einem Azure-Konto mithilfe von `Disconnect-AzAccount` trennen.</span><span class="sxs-lookup"><span data-stu-id="16a45-118">After executing this cmdlet, you can disconnect from an Azure account using `Disconnect-AzAccount`.</span></span>

## <span data-ttu-id="16a45-119">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="16a45-119">EXAMPLES</span></span>

### <span data-ttu-id="16a45-120">Beispiel 1: Herstellen einer Verbindung mit einem Azure-Konto</span><span class="sxs-lookup"><span data-stu-id="16a45-120">Example 1: Connect to an Azure account</span></span>

<span data-ttu-id="16a45-121">In diesem Beispiel wird eine Verbindung mit einem Azure-Konto hergestellt.</span><span class="sxs-lookup"><span data-stu-id="16a45-121">This example connects to an Azure account.</span></span> <span data-ttu-id="16a45-122">Sie müssen anmeldeinformationen für ein Microsoft-Konto oder eine Organisations-ID angeben.</span><span class="sxs-lookup"><span data-stu-id="16a45-122">You must provide a Microsoft account or organizational ID credentials.</span></span> <span data-ttu-id="16a45-123">Wenn die mehrstufige Authentifizierung für Ihre Anmeldeinformationen aktiviert ist, müssen Sie sich mit der interaktiven Option anmelden oder die Dienstprinzipalauthentifizierung verwenden.</span><span class="sxs-lookup"><span data-stu-id="16a45-123">If multi-factor authentication is enabled for your credentials, you must log in using the interactive option or use service principal authentication.</span></span>

```powershell
Connect-AzAccount
```

```Output
Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

### <span data-ttu-id="16a45-124">Beispiel 2: (nur Windows PowerShell 5.1) Herstellen einer Verbindung mit Azure mithilfe von Organisations-ID-Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="16a45-124">Example 2: (Windows PowerShell 5.1 only) Connect to Azure using organizational ID credentials</span></span>

<span data-ttu-id="16a45-125">Dieses Szenario funktioniert nur in Windows PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="16a45-125">This scenario works only in Windows PowerShell 5.1.</span></span> <span data-ttu-id="16a45-126">Der erste Befehl fordert Benutzeranmeldeinformationen auf und speichert sie in der `$Credential` Variablen.</span><span class="sxs-lookup"><span data-stu-id="16a45-126">The first command prompts for user credentials and stores them in the `$Credential` variable.</span></span> <span data-ttu-id="16a45-127">Der zweite Befehl stellt eine Verbindung mit einem Azure-Konto mithilfe der in gespeicherten Anmeldeinformationen `$Credential` bereit.</span><span class="sxs-lookup"><span data-stu-id="16a45-127">The second command connects to an Azure account using the credentials stored in `$Credential`.</span></span> <span data-ttu-id="16a45-128">Dieses Konto authentifiziert sich bei Azure mithilfe von Organisations-ID-Anmeldeinformationen.</span><span class="sxs-lookup"><span data-stu-id="16a45-128">This account authenticates with Azure using organizational ID credentials.</span></span>

```powershell
$Credential = Get-Credential
Connect-AzAccount -Credential $Credential
```

```Output
Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

### <span data-ttu-id="16a45-129">Beispiel 3: Herstellen einer Verbindung mit Azure mithilfe eines Dienstprinzipalkontos</span><span class="sxs-lookup"><span data-stu-id="16a45-129">Example 3: Connect to Azure using a service principal account</span></span>

<span data-ttu-id="16a45-130">Der erste Befehl fordert die Anmeldeinformationen des Dienstprinzipals an und speichert sie in der `$Credential` Variablen.</span><span class="sxs-lookup"><span data-stu-id="16a45-130">The first command prompts for service principal credentials and stores them in the `$Credential` variable.</span></span> <span data-ttu-id="16a45-131">Geben Sie ihre Anwendungs-ID für den geheimen Benutzernamen und dienstprinzipal als Kennwort ein, wenn Sie dazu aufgefordert werden.</span><span class="sxs-lookup"><span data-stu-id="16a45-131">Enter your application ID for the username and service principal secret as the password when prompted.</span></span> <span data-ttu-id="16a45-132">Der zweite Befehl verbindet den angegebenen Azure-Mandanten mithilfe der Dienstprinzipalanmeldeinformationen, die in der Variablen gespeichert `$Credential` sind.</span><span class="sxs-lookup"><span data-stu-id="16a45-132">The second command connects the specified Azure tenant using the service principal credentials stored in the `$Credential` variable.</span></span> <span data-ttu-id="16a45-133">Der **Parameter ServicePrincipal** switch gibt an, dass sich das Konto als Dienstprinzipal authentifiziert.</span><span class="sxs-lookup"><span data-stu-id="16a45-133">The **ServicePrincipal** switch parameter indicates that the account authenticates as a service principal.</span></span>

```powershell
$Credential = Get-Credential
Connect-AzAccount -Credential $Credential -Tenant 'xxxx-xxxx-xxxx-xxxx' -ServicePrincipal
```

```Output
Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
xxxx-xxxx-xxxx-xxxx    Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

### <span data-ttu-id="16a45-134">Beispiel 4: Verwenden einer interaktiven Anmeldung zum Herstellen einer Verbindung mit einem bestimmten Mandanten und Abonnement</span><span class="sxs-lookup"><span data-stu-id="16a45-134">Example 4: Use an interactive login to connect to a specific tenant and subscription</span></span>

<span data-ttu-id="16a45-135">In diesem Beispiel wird eine Verbindung mit einem Azure-Konto mit dem angegebenen Mandanten und Abonnement hergestellt.</span><span class="sxs-lookup"><span data-stu-id="16a45-135">This example connects to an Azure account with the specified tenant and subscription.</span></span>

```powershell
Connect-AzAccount -Tenant 'xxxx-xxxx-xxxx-xxxx' -SubscriptionId 'yyyy-yyyy-yyyy-yyyy'
```

```Output
Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

### <span data-ttu-id="16a45-136">Beispiel 5: Herstellen einer Verbindung mit einer verwalteten Dienstidentität</span><span class="sxs-lookup"><span data-stu-id="16a45-136">Example 5: Connect using a Managed Service Identity</span></span>

<span data-ttu-id="16a45-137">In diesem Beispiel wird eine Verbindung mithilfe der Managed Service Identity (MSI) der Hostumgebung hergestellt.</span><span class="sxs-lookup"><span data-stu-id="16a45-137">This example connects using the Managed Service Identity (MSI) of the host environment.</span></span> <span data-ttu-id="16a45-138">Beispielsweise melden Sie sich von einem virtuellen Computer mit einem zugewiesenen MSI bei Azure an.</span><span class="sxs-lookup"><span data-stu-id="16a45-138">For example, you sign into Azure from a virtual machine that has an assigned MSI.</span></span>

```powershell
Connect-AzAccount -Identity
```

```Output
Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
MSI@50342              Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

### <span data-ttu-id="16a45-139">Beispiel 6: Herstellen einer Verbindung mit der Anmeldung für verwaltete Dienstidentität und ClientId</span><span class="sxs-lookup"><span data-stu-id="16a45-139">Example 6: Connect using Managed Service Identity login and ClientId</span></span>

<span data-ttu-id="16a45-140">In diesem Beispiel wird eine Verbindung mit der Verwalteten **Dienstidentität von myUserAssignedIdentity hergestellt.**</span><span class="sxs-lookup"><span data-stu-id="16a45-140">This example connects using the Managed Service Identity of **myUserAssignedIdentity**.</span></span> <span data-ttu-id="16a45-141">Es fügt dem virtuellen Computer die dem Benutzer zugewiesene Identität hinzu, und stellt dann eine Verbindung mit der ClientId der zugewiesenen Identität des Benutzers ein.</span><span class="sxs-lookup"><span data-stu-id="16a45-141">It adds the user assigned identity to the virtual machine, then connects using the ClientId of the user assigned identity.</span></span> <span data-ttu-id="16a45-142">Weitere Informationen finden Sie unter [Konfigurieren verwalteter Identitäten für Azure-Ressourcen auf einer Azure-VM.](/azure/active-directory/managed-identities-azure-resources/qs-configure-powershell-windows-vm)</span><span class="sxs-lookup"><span data-stu-id="16a45-142">For more information, see [Configure managed identities for Azure resources on an Azure VM](/azure/active-directory/managed-identities-azure-resources/qs-configure-powershell-windows-vm).</span></span>

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

### <span data-ttu-id="16a45-143">Beispiel 7: Herstellen einer Verbindung mit Zertifikaten</span><span class="sxs-lookup"><span data-stu-id="16a45-143">Example 7: Connect using certificates</span></span>

<span data-ttu-id="16a45-144">In diesem Beispiel wird eine Verbindung mit einem Azure-Konto mithilfe der zertifikatbasierten Dienstprinzipalauthentifizierung hergestellt.</span><span class="sxs-lookup"><span data-stu-id="16a45-144">This example connects to an Azure account using certificate-based service principal authentication.</span></span>
<span data-ttu-id="16a45-145">Der für die Authentifizierung verwendete Dienstprinzipal muss mit dem angegebenen Zertifikat erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="16a45-145">The service principal used for authentication must be created with the specified certificate.</span></span> <span data-ttu-id="16a45-146">Weitere Informationen zum Erstellen eines selbst signierten Zertifikats und zum Zuweisen von Berechtigungen finden Sie unter Verwenden von [Azure PowerShell](/azure/active-directory/develop/howto-authenticate-service-principal-powershell) zum Erstellen eines Dienstprinzipals mit einem Zertifikat.</span><span class="sxs-lookup"><span data-stu-id="16a45-146">For more information on creating a self-signed certificates and assigning them permissions, see [Use Azure PowerShell to create a service principal with a certificate](/azure/active-directory/develop/howto-authenticate-service-principal-powershell)</span></span>

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

## <span data-ttu-id="16a45-147">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="16a45-147">PARAMETERS</span></span>

### <span data-ttu-id="16a45-148">-AccessToken</span><span class="sxs-lookup"><span data-stu-id="16a45-148">-AccessToken</span></span>

<span data-ttu-id="16a45-149">Gibt ein Zugriffstoken an.</span><span class="sxs-lookup"><span data-stu-id="16a45-149">Specifies an access token.</span></span>

> [!CAUTION]
> <span data-ttu-id="16a45-150">Zugriffstoken sind eine Art von Anmeldeinformationen.</span><span class="sxs-lookup"><span data-stu-id="16a45-150">Access tokens are a type of credential.</span></span> <span data-ttu-id="16a45-151">Sie sollten die entsprechenden Sicherheitsvorkehrungen treffen, um sie vertraulich zu halten.</span><span class="sxs-lookup"><span data-stu-id="16a45-151">You should take the appropriate security precautions to keep them confidential.</span></span> <span data-ttu-id="16a45-152">Zugriffstoken timeoutn ebenfalls und können verhindern, dass Aufgaben mit langer Ausführungszeit abgeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="16a45-152">Access tokens also timeout and may prevent long running tasks from completing.</span></span>

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

### <span data-ttu-id="16a45-153">-AccountId</span><span class="sxs-lookup"><span data-stu-id="16a45-153">-AccountId</span></span>

<span data-ttu-id="16a45-154">Konto-ID für Zugriffstoken im **AccessToken-Parametersatz.**</span><span class="sxs-lookup"><span data-stu-id="16a45-154">Account ID for access token in **AccessToken** parameter set.</span></span> <span data-ttu-id="16a45-155">Konto-ID für verwalteten Dienst im **ManagedService-Parametersatz.**</span><span class="sxs-lookup"><span data-stu-id="16a45-155">Account ID for managed service in **ManagedService** parameter set.</span></span> <span data-ttu-id="16a45-156">Kann eine verwaltete Dienstressourcen-ID oder die zugeordnete Client-ID sein.</span><span class="sxs-lookup"><span data-stu-id="16a45-156">Can be a managed service resource ID, or the associated client ID.</span></span>
<span data-ttu-id="16a45-157">Wenn Sie die vom System zugewiesene Identität verwenden möchten, lassen Sie dieses Feld leer.</span><span class="sxs-lookup"><span data-stu-id="16a45-157">To use the system assigned identity, leave this field blank.</span></span>

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

### <span data-ttu-id="16a45-158">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="16a45-158">-ApplicationId</span></span>

<span data-ttu-id="16a45-159">Anwendungs-ID des Dienstprinzipals.</span><span class="sxs-lookup"><span data-stu-id="16a45-159">Application ID of the service principal.</span></span>

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

### <span data-ttu-id="16a45-160">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="16a45-160">-CertificateThumbprint</span></span>

<span data-ttu-id="16a45-161">Zertifikathash oder Fingerabdruck.</span><span class="sxs-lookup"><span data-stu-id="16a45-161">Certificate Hash or Thumbprint.</span></span>

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

### <span data-ttu-id="16a45-162">-ContextName</span><span class="sxs-lookup"><span data-stu-id="16a45-162">-ContextName</span></span>

<span data-ttu-id="16a45-163">Name des standardmäßigen Azure-Kontexts für diese Anmeldung.</span><span class="sxs-lookup"><span data-stu-id="16a45-163">Name of the default Azure context for this login.</span></span> <span data-ttu-id="16a45-164">Weitere Informationen zu Azure-Kontexten finden Sie unter [Azure PowerShell-Kontextobjekte.](/powershell/azure/context-persistence)</span><span class="sxs-lookup"><span data-stu-id="16a45-164">For more information about Azure contexts, see [Azure PowerShell context objects](/powershell/azure/context-persistence).</span></span>

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

### <span data-ttu-id="16a45-165">-Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="16a45-165">-Credential</span></span>

<span data-ttu-id="16a45-166">Gibt ein **PSCredential-Objekt** an.</span><span class="sxs-lookup"><span data-stu-id="16a45-166">Specifies a **PSCredential** object.</span></span> <span data-ttu-id="16a45-167">Weitere Informationen zum **PSCredential-Objekt** finden Sie unter `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="16a45-167">For more information about the **PSCredential** object, type `Get-Help Get-Credential`.</span></span> <span data-ttu-id="16a45-168">Das **PSCredential-Objekt** stellt die Benutzer-ID und das Kennwort für Organisations-ID-Anmeldeinformationen oder die Anwendungs-ID und den Geheimschutz für Dienstprinzipalanmeldeinformationen zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="16a45-168">The **PSCredential** object provides the user ID and password for organizational ID credentials, or the application ID and secret for service principal credentials.</span></span>

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

### <span data-ttu-id="16a45-169">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16a45-169">-DefaultProfile</span></span>

<span data-ttu-id="16a45-170">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="16a45-170">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="16a45-171">-Umgebung</span><span class="sxs-lookup"><span data-stu-id="16a45-171">-Environment</span></span>

<span data-ttu-id="16a45-172">Umgebung, die das Azure-Konto enthält.</span><span class="sxs-lookup"><span data-stu-id="16a45-172">Environment containing the Azure account.</span></span>

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

### <span data-ttu-id="16a45-173">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="16a45-173">-Force</span></span>

<span data-ttu-id="16a45-174">Überschreiben Sie den vorhandenen Kontext ohne Aufforderung mit demselben Namen.</span><span class="sxs-lookup"><span data-stu-id="16a45-174">Overwrite the existing context with the same name without prompting.</span></span>

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

### <span data-ttu-id="16a45-175">-GraphAccessToken</span><span class="sxs-lookup"><span data-stu-id="16a45-175">-GraphAccessToken</span></span>

<span data-ttu-id="16a45-176">AccessToken für Graph Service.</span><span class="sxs-lookup"><span data-stu-id="16a45-176">AccessToken for Graph Service.</span></span>

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

### <span data-ttu-id="16a45-177">-Identity</span><span class="sxs-lookup"><span data-stu-id="16a45-177">-Identity</span></span>

<span data-ttu-id="16a45-178">Melden Sie sich mit einer Verwalteten Dienstidentität an.</span><span class="sxs-lookup"><span data-stu-id="16a45-178">Login using a Managed Service Identity.</span></span>

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

### <span data-ttu-id="16a45-179">-KeyVaultAccessToken</span><span class="sxs-lookup"><span data-stu-id="16a45-179">-KeyVaultAccessToken</span></span>

<span data-ttu-id="16a45-180">AccessToken für KeyVault Service.</span><span class="sxs-lookup"><span data-stu-id="16a45-180">AccessToken for KeyVault Service.</span></span>

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

### <span data-ttu-id="16a45-181">-ManagedServiceHostName</span><span class="sxs-lookup"><span data-stu-id="16a45-181">-ManagedServiceHostName</span></span>

<span data-ttu-id="16a45-182">Veraltet.</span><span class="sxs-lookup"><span data-stu-id="16a45-182">Obsolete.</span></span> <span data-ttu-id="16a45-183">Wenn Sie benutzerdefinierte MSI-Endpunkte verwenden möchten, legen Sie die Umgebungsvariable MSI_ENDPOINT fest, z. B. " http://localhost:50342/oauth2/token ".</span><span class="sxs-lookup"><span data-stu-id="16a45-183">To use customized MSI endpoint, please set environment variable MSI_ENDPOINT, e.g. "http://localhost:50342/oauth2/token".</span></span> <span data-ttu-id="16a45-184">Hostname für den verwalteten Dienst.</span><span class="sxs-lookup"><span data-stu-id="16a45-184">Host name for the managed service.</span></span>

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

### <span data-ttu-id="16a45-185">-ManagedServicePort</span><span class="sxs-lookup"><span data-stu-id="16a45-185">-ManagedServicePort</span></span>

<span data-ttu-id="16a45-186">Veraltet.</span><span class="sxs-lookup"><span data-stu-id="16a45-186">Obsolete.</span></span> <span data-ttu-id="16a45-187">Wenn Sie benutzerdefinierte MSI-Endpunkte verwenden möchten, legen Sie die Umgebungsvariable MSI_ENDPOINT fest, z. B. " http://localhost:50342/oauth2/token ". Portnummer für den verwalteten Dienst.</span><span class="sxs-lookup"><span data-stu-id="16a45-187">To use customized MSI endpoint, please set environment variable MSI_ENDPOINT, e.g. "http://localhost:50342/oauth2/token".Port number for the managed service.</span></span>

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

### <span data-ttu-id="16a45-188">-ManagedServiceSecret</span><span class="sxs-lookup"><span data-stu-id="16a45-188">-ManagedServiceSecret</span></span>

<span data-ttu-id="16a45-189">Veraltet.</span><span class="sxs-lookup"><span data-stu-id="16a45-189">Obsolete.</span></span> <span data-ttu-id="16a45-190">Wenn Sie angepasste MSI-Geheimtipps verwenden möchten, legen Sie die Umgebungsvariablen MSI_SECRET.</span><span class="sxs-lookup"><span data-stu-id="16a45-190">To use customized MSI secret, please set environment variable MSI_SECRET.</span></span> <span data-ttu-id="16a45-191">Token für die Anmeldung für verwaltete Dienste.</span><span class="sxs-lookup"><span data-stu-id="16a45-191">Token for the managed service login.</span></span>

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

### <span data-ttu-id="16a45-192">-MaxContextPopulation</span><span class="sxs-lookup"><span data-stu-id="16a45-192">-MaxContextPopulation</span></span>

<span data-ttu-id="16a45-193">Maximale Abonnementnummer zum Auffüllen von Kontexten nach der Anmeldung.</span><span class="sxs-lookup"><span data-stu-id="16a45-193">Max subscription number to populate contexts after login.</span></span> <span data-ttu-id="16a45-194">Der Standardwert ist 25.</span><span class="sxs-lookup"><span data-stu-id="16a45-194">Default is 25.</span></span> <span data-ttu-id="16a45-195">Um alle Abonnements in Kontexte zu füllen, legen Sie auf -1 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="16a45-195">To populate all subscriptions to contexts, set to -1.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16a45-196">-Scope</span><span class="sxs-lookup"><span data-stu-id="16a45-196">-Scope</span></span>

<span data-ttu-id="16a45-197">Bestimmt den Umfang von Kontextänderungen, z. B. ob Änderungen nur für den aktuellen Prozess oder für alle von diesem Benutzer gestarteten Sitzungen gelten.</span><span class="sxs-lookup"><span data-stu-id="16a45-197">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="16a45-198">-ServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="16a45-198">-ServicePrincipal</span></span>

<span data-ttu-id="16a45-199">Gibt an, dass sich dieses Konto durch Bereitstellen von Dienstprinzipalanmeldeinformationen authentifiziert.</span><span class="sxs-lookup"><span data-stu-id="16a45-199">Indicates that this account authenticates by providing service principal credentials.</span></span>

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

### <span data-ttu-id="16a45-200">-SkipContextPopulation</span><span class="sxs-lookup"><span data-stu-id="16a45-200">-SkipContextPopulation</span></span>

<span data-ttu-id="16a45-201">Überspringt die Kontextgesamtheit, wenn keine Kontexte gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="16a45-201">Skips context population if no contexts are found.</span></span>

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

### <span data-ttu-id="16a45-202">-SkipValidation</span><span class="sxs-lookup"><span data-stu-id="16a45-202">-SkipValidation</span></span>

<span data-ttu-id="16a45-203">Überspringen sie die Überprüfung für das Zugriffstoken.</span><span class="sxs-lookup"><span data-stu-id="16a45-203">Skip validation for access token.</span></span>

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

### <span data-ttu-id="16a45-204">-Abonnement</span><span class="sxs-lookup"><span data-stu-id="16a45-204">-Subscription</span></span>

<span data-ttu-id="16a45-205">Abonnementname oder ID.</span><span class="sxs-lookup"><span data-stu-id="16a45-205">Subscription Name or ID.</span></span>

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

### <span data-ttu-id="16a45-206">-Mandant</span><span class="sxs-lookup"><span data-stu-id="16a45-206">-Tenant</span></span>

<span data-ttu-id="16a45-207">Optionaler Mandantname oder ID.</span><span class="sxs-lookup"><span data-stu-id="16a45-207">Optional tenant name or ID.</span></span>

> [!NOTE]
> <span data-ttu-id="16a45-208">Aufgrund von Einschränkungen der aktuellen API müssen Sie eine Mandanten-ID anstelle eines Mandantennamens verwenden, wenn Sie eine Verbindung mit einem Business-to-Business (B2B)-Konto herstellen.</span><span class="sxs-lookup"><span data-stu-id="16a45-208">Due to limitations of the current API, you must use a tenant ID instead of a tenant name when connecting with a business-to-business (B2B) account.</span></span>

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

### <span data-ttu-id="16a45-209">-UseDeviceAuthentication</span><span class="sxs-lookup"><span data-stu-id="16a45-209">-UseDeviceAuthentication</span></span>

<span data-ttu-id="16a45-210">Verwenden Sie die Gerätecodeauthentifizierung anstelle eines Browsersteuerelements.</span><span class="sxs-lookup"><span data-stu-id="16a45-210">Use device code authentication instead of a browser control.</span></span>

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

### <span data-ttu-id="16a45-211">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="16a45-211">-Confirm</span></span>

<span data-ttu-id="16a45-212">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="16a45-212">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="16a45-213">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="16a45-213">-WhatIf</span></span>

<span data-ttu-id="16a45-214">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="16a45-214">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="16a45-215">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="16a45-215">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="16a45-216">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16a45-216">CommonParameters</span></span>
<span data-ttu-id="16a45-217">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="16a45-217">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16a45-218">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="16a45-218">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16a45-219">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="16a45-219">INPUTS</span></span>

### <span data-ttu-id="16a45-220">System.String</span><span class="sxs-lookup"><span data-stu-id="16a45-220">System.String</span></span>

## <span data-ttu-id="16a45-221">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="16a45-221">OUTPUTS</span></span>

### <span data-ttu-id="16a45-222">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureProfile</span><span class="sxs-lookup"><span data-stu-id="16a45-222">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureProfile</span></span>

## <span data-ttu-id="16a45-223">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="16a45-223">NOTES</span></span>

## <span data-ttu-id="16a45-224">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="16a45-224">RELATED LINKS</span></span>
