---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.profile
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Add-AzureRmAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Add-AzureRmAccount.md
ms.openlocfilehash: 11303438a50839bbe05139888cc665198ed09810
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504017"
---
# <span data-ttu-id="340a3-101">Add-AzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="340a3-101">Add-AzureRmAccount</span></span>

## <span data-ttu-id="340a3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="340a3-102">SYNOPSIS</span></span>
<span data-ttu-id="340a3-103">Fügt ein authentifiziertes Konto hinzu, das für Azure Resource Manager-Cmdlet-Anforderungen verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="340a3-103">Adds an authenticated account to use for Azure Resource Manager cmdlet requests.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="340a3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="340a3-104">SYNTAX</span></span>

### <span data-ttu-id="340a3-105">UserWithSubscriptionId (Standard)</span><span class="sxs-lookup"><span data-stu-id="340a3-105">UserWithSubscriptionId (Default)</span></span>
```
Add-AzureRmAccount [-Environment <String>] [[-Credential] <PSCredential>] [-TenantId <String>]
 [-Subscription <String>] [-ContextName <String>] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="340a3-106">ServicePrincipalWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="340a3-106">ServicePrincipalWithSubscriptionId</span></span>
```
Add-AzureRmAccount [-Environment <String>] [-Credential] <PSCredential> [-ServicePrincipal] -TenantId <String>
 [-Subscription <String>] [-ContextName <String>] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="340a3-107">ServicePrincipalCertificateWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="340a3-107">ServicePrincipalCertificateWithSubscriptionId</span></span>
```
Add-AzureRmAccount [-Environment <String>] -CertificateThumbprint <String> -ApplicationId <String>
 [-ServicePrincipal] -TenantId <String> [-Subscription <String>] [-ContextName <String>] [-Force]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="340a3-108">AccessTokenWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="340a3-108">AccessTokenWithSubscriptionId</span></span>
```
Add-AzureRmAccount [-Environment <String>] [-TenantId <String>] -AccessToken <String>
 [-GraphAccessToken <String>] [-KeyVaultAccessToken <String>] -AccountId <String> [-Subscription <String>]
 [-ContextName <String>] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="340a3-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="340a3-109">DESCRIPTION</span></span>
<span data-ttu-id="340a3-110">Das Add-AzureRmAcccount-Cmdlet fügt ein authentifiziertes Azure-Konto hinzu, das für Azure Resource Manager-Cmdlet-Anforderungen verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="340a3-110">The Add-AzureRmAcccount cmdlet adds an authenticated Azure account to use for Azure Resource Manager cmdlet requests.</span></span>

<span data-ttu-id="340a3-111">Sie können dieses authentifizierte Konto nur mit Azure Resource Manager-Cmdlets verwenden.</span><span class="sxs-lookup"><span data-stu-id="340a3-111">You can use this authenticated account only with Azure Resource Manager cmdlets.</span></span>
<span data-ttu-id="340a3-112">Verwenden Sie zum Hinzufügen eines authentifizierten Kontos zur Verwendung mit Dienst Verwaltungs-Cmdlets das Add-AzureAccount oder das Import-AzurePublishSettingsFile-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="340a3-112">To add an authenticated account for use with Service Management cmdlets, use the Add-AzureAccount or the Import-AzurePublishSettingsFile cmdlet.</span></span>

## <span data-ttu-id="340a3-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="340a3-113">EXAMPLES</span></span>

### <span data-ttu-id="340a3-114">Beispiel 1: Hinzufügen eines Kontos, das interaktive Anmeldung erfordert</span><span class="sxs-lookup"><span data-stu-id="340a3-114">Example 1: Add an account that requires interactive login</span></span>
```
PS C:\>Add-AzureRmAccount
Account: azureuser@contoso.com
Environment: AzureCloud
Subscription: xxxx-xxxx-xxxx-xxxx
Tenant: xxxx-xxxx-xxxx-xxxx
```

<span data-ttu-id="340a3-115">Mit diesem Befehl wird ein Azure Resource Manager-Konto hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="340a3-115">This command adds an Azure Resource Manager account.</span></span>

<span data-ttu-id="340a3-116">Zum Ausführen von Azure Resource Manager-Cmdlets mit diesem Konto müssen Sie an der Eingabeaufforderung Microsoft-Konto-oder Organisations-ID-Anmeldeinformationen angeben.</span><span class="sxs-lookup"><span data-stu-id="340a3-116">To run Azure Resource Manager cmdlets with this account, you must provide Microsoft account or organizational ID credentials at the prompt.</span></span>

<span data-ttu-id="340a3-117">Wenn die mehrstufige Authentifizierung für Ihre Anmeldeinformationen aktiviert ist, müssen Sie sich mit der interaktiven Option anmelden oder die Dienstprinzipal Authentifizierung verwenden.</span><span class="sxs-lookup"><span data-stu-id="340a3-117">If multi-factor authentication is enabled for your credentials, you must log in using the interactive option or use service principal authentication.</span></span>

### <span data-ttu-id="340a3-118">Beispiel 2: Hinzufügen eines Kontos, das sich mit den Anmeldeinformationen für die Organisations-ID authentifiziert</span><span class="sxs-lookup"><span data-stu-id="340a3-118">Example 2: Add an account that authenticates with organizational ID credentials</span></span>
```
PS C:\>$Credential = Get-Credential
PS C:\> Add-AzureRmAccount -Credential $Credential
Account: azureuser@contoso.com
Environment: AzureChinaCloud
Subscription: xxxx-xxxx-xxxx-xxxx
Tenant: xxxx-xxxx-xxxx-xxxx
```

<span data-ttu-id="340a3-119">Der erste Befehl ruft die Anmeldeinformationen des Benutzers ab und speichert Sie dann in der $Credential-Variablen.</span><span class="sxs-lookup"><span data-stu-id="340a3-119">The first command gets the user credentials, and then stores them in the $Credential variable.</span></span>

<span data-ttu-id="340a3-120">Mit dem zweiten Befehl wird ein Azure Resource Manager-Konto mit den Anmeldeinformationen in $Credential hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="340a3-120">The second command adds an Azure Resource Manager account with the credentials in $Credential.</span></span>

<span data-ttu-id="340a3-121">Dieses Konto authentifiziert sich beim Azure Resource Manager mit den Anmeldeinformationen für die Organisations-ID.</span><span class="sxs-lookup"><span data-stu-id="340a3-121">This account authenticates with Azure Resource Manager using organizational ID credentials.</span></span>
<span data-ttu-id="340a3-122">Sie können keine mehrstufigen Authentifizierungs-oder Microsoft-Kontoanmeldeinformationen verwenden, um Azure Resource Manager-Cmdlets mit diesem Konto auszuführen.</span><span class="sxs-lookup"><span data-stu-id="340a3-122">You cannot use multi-factor authentication or Microsoft account credentials to run Azure Resource Manager cmdlets with this account.</span></span>

### <span data-ttu-id="340a3-123">Beispiel 3: Hinzufügen eines Kontos, das mit den Dienstprinzipal Anmeldeinformationen authentifiziert wird</span><span class="sxs-lookup"><span data-stu-id="340a3-123">Example 3: Add an account that authenticates with service principal credentials</span></span>
```
PS C:\>$Credential = Get-Credential
PS C:\> Add-AzureRmAccount -Credential $Credential -Tenant "xxxx-xxxx-xxxx-xxxx" -ServicePrincipal
Account: xxxx-xxxx-xxxx-xxxx
Environment: AzureCloud
Subscription: yyyy-yyyy-yyyy-yyyy
Tenant: xxxx-xxxx-xxxx-xxxx
```

<span data-ttu-id="340a3-124">Der erste Befehl ruft die Anmeldeinformationen des Benutzers ab und speichert Sie dann in der $Credential-Variablen.</span><span class="sxs-lookup"><span data-stu-id="340a3-124">The first command gets the user credentials, and then stores them in the $Credential variable.</span></span>

<span data-ttu-id="340a3-125">Der zweite Befehl fügt ein Azure Resource Manager-Konto mit den Anmeldeinformationen hinzu, die in $Credential für den angegebenen Mandanten gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="340a3-125">The second command adds an Azure Resource Manager account with the credentials stored in $Credential for the specified Tenant.</span></span>
<span data-ttu-id="340a3-126">Der ServicePrincipal-Parameter "Switch" gibt an, dass sich das Konto als Dienstprinzipal authentifiziert.</span><span class="sxs-lookup"><span data-stu-id="340a3-126">The ServicePrincipal switch parameter indicates that the account authenticates as a service principal.</span></span>

### <span data-ttu-id="340a3-127">Beispiel 4: Hinzufügen eines Kontos für einen bestimmten Mandanten und ein Abonnement</span><span class="sxs-lookup"><span data-stu-id="340a3-127">Example 4: Add an account for a specific tenant and subscription</span></span>
```
PS C:\>Add-AzureRmAccount -Tenant "xxxx-xxxx-xxxx-xxxx" -SubscriptionId "yyyy-yyyy-yyyy-yyyy"
Account: pfuller@contoso.com
Environment: AzureCloud
Subscription: yyyy-yyyy-yyyy-yyyy
Tenant: xxxx-xxxx-xxxx-xxxx
```

<span data-ttu-id="340a3-128">Mit diesem Befehl wird ein Azure Resource Manager-Konto hinzugefügt, damit Cmdlets für den angegebenen Mandanten und das Abonnement standardmäßig ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="340a3-128">This command adds an Azure Resource Manager account to run cmdlets for the specified tenant and subscription by default.</span></span>

## <span data-ttu-id="340a3-129">Parameter</span><span class="sxs-lookup"><span data-stu-id="340a3-129">PARAMETERS</span></span>

### <span data-ttu-id="340a3-130">-Access Token</span><span class="sxs-lookup"><span data-stu-id="340a3-130">-AccessToken</span></span>
<span data-ttu-id="340a3-131">Gibt ein Zugriffstoken an.</span><span class="sxs-lookup"><span data-stu-id="340a3-131">Specifies an access token.</span></span>

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

### <span data-ttu-id="340a3-132">-Konto-Nr</span><span class="sxs-lookup"><span data-stu-id="340a3-132">-AccountId</span></span>
<span data-ttu-id="340a3-133">Konto-ID für Zugriffstoken</span><span class="sxs-lookup"><span data-stu-id="340a3-133">Account Id for access token</span></span>

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

### <span data-ttu-id="340a3-134">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="340a3-134">-ApplicationId</span></span>
<span data-ttu-id="340a3-135">SPN</span><span class="sxs-lookup"><span data-stu-id="340a3-135">SPN</span></span>

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

### <span data-ttu-id="340a3-136">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="340a3-136">-CertificateThumbprint</span></span>
<span data-ttu-id="340a3-137">Zertifikat Hash (Fingerabdruck)</span><span class="sxs-lookup"><span data-stu-id="340a3-137">Certificate Hash (Thumbprint)</span></span>

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

### <span data-ttu-id="340a3-138">-Contextname</span><span class="sxs-lookup"><span data-stu-id="340a3-138">-ContextName</span></span>
<span data-ttu-id="340a3-139">Der Name des Standardkontexts aus dieser Anmeldung.</span><span class="sxs-lookup"><span data-stu-id="340a3-139">Name of the default context from this login.</span></span>  <span data-ttu-id="340a3-140">Nachdem Sie sich angemeldet haben, können Sie diesen Kontext mit diesem Namen auswählen.</span><span class="sxs-lookup"><span data-stu-id="340a3-140">You will be able to select this context by this name after login.</span></span>

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

### <span data-ttu-id="340a3-141">– Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="340a3-141">-Credential</span></span>
<span data-ttu-id="340a3-142">Gibt ein PSCredential-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="340a3-142">Specifies a PSCredential object.</span></span>
<span data-ttu-id="340a3-143">Wenn Sie weitere Informationen zum PSCredential-Objekt wünschen, geben Sie Get-Help Get-Credential ein.</span><span class="sxs-lookup"><span data-stu-id="340a3-143">For more information about the PSCredential object, type Get-Help Get-Credential.</span></span>

<span data-ttu-id="340a3-144">Das PSCredential-Objekt enthält die Benutzer-ID und das Kennwort für die Anmeldeinformationen für die Organisations-ID oder die Anwendungs-ID und den Schlüssel für die Anmeldeinformationen des Dienst Prinzipals.</span><span class="sxs-lookup"><span data-stu-id="340a3-144">The PSCredential object provides the user ID and password for organizational ID credentials, or the application ID and secret for service principal credentials.</span></span>

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

### <span data-ttu-id="340a3-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="340a3-145">-DefaultProfile</span></span>
<span data-ttu-id="340a3-146">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="340a3-146">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="340a3-147">-Umgebung</span><span class="sxs-lookup"><span data-stu-id="340a3-147">-Environment</span></span>
<span data-ttu-id="340a3-148">Umgebung mit dem Konto, bei dem Sie sich anmelden können</span><span class="sxs-lookup"><span data-stu-id="340a3-148">Environment containing the account to log into</span></span>

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

### <span data-ttu-id="340a3-149">-Force</span><span class="sxs-lookup"><span data-stu-id="340a3-149">-Force</span></span>
<span data-ttu-id="340a3-150">Überschreiben Sie den vorhandenen Kontext mit dem gleichen Namen (sofern vorhanden).</span><span class="sxs-lookup"><span data-stu-id="340a3-150">Overwrite the existing context with the same name, if any.</span></span>

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

### <span data-ttu-id="340a3-151">-GraphAccessToken</span><span class="sxs-lookup"><span data-stu-id="340a3-151">-GraphAccessToken</span></span>
<span data-ttu-id="340a3-152">Access Token for Graph-Dienst</span><span class="sxs-lookup"><span data-stu-id="340a3-152">AccessToken for Graph Service</span></span>

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

### <span data-ttu-id="340a3-153">-KeyVaultAccessToken</span><span class="sxs-lookup"><span data-stu-id="340a3-153">-KeyVaultAccessToken</span></span>
<span data-ttu-id="340a3-154">Access Token für keyvault-Dienst</span><span class="sxs-lookup"><span data-stu-id="340a3-154">AccessToken for KeyVault Service</span></span>

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

### <span data-ttu-id="340a3-155">-Scope</span><span class="sxs-lookup"><span data-stu-id="340a3-155">-Scope</span></span>
<span data-ttu-id="340a3-156">Bestimmt den Bereich von Kontextänderungen, beispielsweise wheher Änderungen gelten nur für den cusrrent-Prozess oder für alle von diesem Benutzer gestarteten Sitzungen.</span><span class="sxs-lookup"><span data-stu-id="340a3-156">Determines the scope of context changes, for example, wheher changes apply only to the cusrrent process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="340a3-157">-ServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="340a3-157">-ServicePrincipal</span></span>
<span data-ttu-id="340a3-158">Gibt an, dass sich dieses Konto durch die Bereitstellung von Dienstprinzipal Anmeldeinformationen authentifiziert.</span><span class="sxs-lookup"><span data-stu-id="340a3-158">Indicates that this account authenticates by providing service principal credentials.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ServicePrincipalWithSubscriptionId, ServicePrincipalCertificateWithSubscriptionId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="340a3-159">-Abonnement</span><span class="sxs-lookup"><span data-stu-id="340a3-159">-Subscription</span></span>
<span data-ttu-id="340a3-160">Name oder ID des Abonnements</span><span class="sxs-lookup"><span data-stu-id="340a3-160">Subscription Name or ID</span></span>

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

### <span data-ttu-id="340a3-161">-Mandanten-Nr</span><span class="sxs-lookup"><span data-stu-id="340a3-161">-TenantId</span></span>
<span data-ttu-id="340a3-162">Optionaler Mandantenname oder ID</span><span class="sxs-lookup"><span data-stu-id="340a3-162">Optional tenant name or ID</span></span>

```yaml
Type: System.String
Parameter Sets: UserWithSubscriptionId, AccessTokenWithSubscriptionId
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

### <span data-ttu-id="340a3-163">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="340a3-163">-Confirm</span></span>
<span data-ttu-id="340a3-164">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="340a3-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="340a3-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="340a3-165">-WhatIf</span></span>
<span data-ttu-id="340a3-166">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="340a3-166">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="340a3-167">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="340a3-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="340a3-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="340a3-168">CommonParameters</span></span>
<span data-ttu-id="340a3-169">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="340a3-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="340a3-170">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="340a3-170">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="340a3-171">Eingaben</span><span class="sxs-lookup"><span data-stu-id="340a3-171">INPUTS</span></span>

### <span data-ttu-id="340a3-172">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="340a3-172">String</span></span>
<span data-ttu-id="340a3-173">Der Parameter "Abonnement-Nr" akzeptiert den Wert vom Typ "Zeichenfolge" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="340a3-173">Parameter 'SubscriptionId' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="340a3-174">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="340a3-174">String</span></span>
<span data-ttu-id="340a3-175">Der Parameter "subscriptionname" akzeptiert den Wert vom Typ "Zeichenfolge" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="340a3-175">Parameter 'SubscriptionName' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="340a3-176">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="340a3-176">OUTPUTS</span></span>

### <span data-ttu-id="340a3-177">PSAzureProfile</span><span class="sxs-lookup"><span data-stu-id="340a3-177">PSAzureProfile</span></span>
<span data-ttu-id="340a3-178">Informationen zu Anmeldeinformationen, Abonnements, Konten und Mandanten für den angemeldeten Benutzer.</span><span class="sxs-lookup"><span data-stu-id="340a3-178">Credentials, subscription, account, and tenant information for the logged in user.</span></span>

## <span data-ttu-id="340a3-179">Notizen</span><span class="sxs-lookup"><span data-stu-id="340a3-179">NOTES</span></span>

## <span data-ttu-id="340a3-180">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="340a3-180">RELATED LINKS</span></span>

