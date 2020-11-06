---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: 533982757e4ea953c1f5d07ba67ac70af2161a10
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93474925"
---
# <span data-ttu-id="c6013-101">Add-AzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="c6013-101">Add-AzureRmAccount</span></span>

## <span data-ttu-id="c6013-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c6013-102">SYNOPSIS</span></span>
<span data-ttu-id="c6013-103">Fügt ein authentifiziertes Konto hinzu, das für Azure Resource Manager-Cmdlet-Anforderungen verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="c6013-103">Adds an authenticated account to use for Azure Resource Manager cmdlet requests.</span></span>

## <span data-ttu-id="c6013-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c6013-104">SYNTAX</span></span>

### <span data-ttu-id="c6013-105">UserWithSubscriptionId (Standard)</span><span class="sxs-lookup"><span data-stu-id="c6013-105">UserWithSubscriptionId (Default)</span></span>
```
Add-AzureRmAccount [-Environment <String>] [[-Credential] <PSCredential>] [-TenantId <String>]
 [-SubscriptionId <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c6013-106">UserWithSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="c6013-106">UserWithSubscriptionName</span></span>
```
Add-AzureRmAccount [-Environment <String>] [[-Credential] <PSCredential>] [-TenantId <String>]
 -SubscriptionName <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c6013-107">ServicePrincipalWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c6013-107">ServicePrincipalWithSubscriptionId</span></span>
```
Add-AzureRmAccount [-Environment <String>] [-Credential] <PSCredential> [-ServicePrincipal] -TenantId <String>
 [-SubscriptionId <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c6013-108">ServicePrincipalWithSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="c6013-108">ServicePrincipalWithSubscriptionName</span></span>
```
Add-AzureRmAccount [-Environment <String>] [-Credential] <PSCredential> [-ServicePrincipal] -TenantId <String>
 -SubscriptionName <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c6013-109">ServicePrincipalCertificateWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c6013-109">ServicePrincipalCertificateWithSubscriptionId</span></span>
```
Add-AzureRmAccount [-Environment <String>] -CertificateThumbprint <String> -ApplicationId <String>
 [-ServicePrincipal] -TenantId <String> [-SubscriptionId <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c6013-110">ServicePrincipalCertificateWithSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="c6013-110">ServicePrincipalCertificateWithSubscriptionName</span></span>
```
Add-AzureRmAccount [-Environment <String>] -CertificateThumbprint <String> -ApplicationId <String>
 [-ServicePrincipal] -TenantId <String> -SubscriptionName <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c6013-111">AccessTokenWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c6013-111">AccessTokenWithSubscriptionId</span></span>
```
Add-AzureRmAccount [-Environment <String>] [-TenantId <String>] -AccessToken <String> -AccountId <String>
 [-SubscriptionId <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c6013-112">AccessTokenWithSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="c6013-112">AccessTokenWithSubscriptionName</span></span>
```
Add-AzureRmAccount [-Environment <String>] [-TenantId <String>] -AccessToken <String> -AccountId <String>
 -SubscriptionName <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c6013-113">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c6013-113">DESCRIPTION</span></span>
<span data-ttu-id="c6013-114">Das Add-AzureRmAcccount-Cmdlet fügt ein authentifiziertes Azure-Konto hinzu, das für Azure Resource Manager-Cmdlet-Anforderungen verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="c6013-114">The Add-AzureRmAcccount cmdlet adds an authenticated Azure account to use for Azure Resource Manager cmdlet requests.</span></span>

<span data-ttu-id="c6013-115">Sie können dieses authentifizierte Konto nur mit Azure Resource Manager-Cmdlets verwenden.</span><span class="sxs-lookup"><span data-stu-id="c6013-115">You can use this authenticated account only with Azure Resource Manager cmdlets.</span></span>
<span data-ttu-id="c6013-116">Verwenden Sie zum Hinzufügen eines authentifizierten Kontos zur Verwendung mit Dienst Verwaltungs-Cmdlets das Add-AzureAccount oder das Import-AzurePublishSettingsFile-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c6013-116">To add an authenticated account for use with Service Management cmdlets, use the Add-AzureAccount or the Import-AzurePublishSettingsFile cmdlet.</span></span>

## <span data-ttu-id="c6013-117">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c6013-117">EXAMPLES</span></span>

### <span data-ttu-id="c6013-118">Beispiel 1: Hinzufügen eines Kontos, das interaktive Anmeldung erfordert</span><span class="sxs-lookup"><span data-stu-id="c6013-118">Example 1: Add an account that requires interactive login</span></span>
```
PS C:\>Add-AzureRmAccount
Account: azureuser@contoso.com
Environment: AzureCloud
Subscription: xxxx-xxxx-xxxx-xxxx
Tenant: xxxx-xxxx-xxxx-xxxx
```

<span data-ttu-id="c6013-119">Mit diesem Befehl wird ein Azure Resource Manager-Konto hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="c6013-119">This command adds an Azure Resource Manager account.</span></span>

<span data-ttu-id="c6013-120">Zum Ausführen von Azure Resource Manager-Cmdlets mit diesem Konto müssen Sie an der Eingabeaufforderung Microsoft-Konto-oder Organisations-ID-Anmeldeinformationen angeben.</span><span class="sxs-lookup"><span data-stu-id="c6013-120">To run Azure Resource Manager cmdlets with this account, you must provide Microsoft account or organizational ID credentials at the prompt.</span></span>

<span data-ttu-id="c6013-121">Wenn die mehrstufige Authentifizierung für Ihre Anmeldeinformationen aktiviert ist, müssen Sie sich mit der interaktiven Option anmelden oder die Dienstprinzipal Authentifizierung verwenden.</span><span class="sxs-lookup"><span data-stu-id="c6013-121">If multi-factor authentication is enabled for your credentials, you must log in using the interactive option or use service principal authentication.</span></span>

### <span data-ttu-id="c6013-122">Beispiel 2: Hinzufügen eines Kontos, das sich mit den Anmeldeinformationen für die Organisations-ID authentifiziert</span><span class="sxs-lookup"><span data-stu-id="c6013-122">Example 2: Add an account that authenticates with organizational ID credentials</span></span>
```
PS C:\>$Credential = Get-Credential
PS C:\> Add-AzureRmAccount -Credential $Credential
Account: azureuser@contoso.com
Environment: AzureChinaCloud
Subscription: xxxx-xxxx-xxxx-xxxx
Tenant: xxxx-xxxx-xxxx-xxxx
```

<span data-ttu-id="c6013-123">Der erste Befehl ruft die Anmeldeinformationen des Benutzers ab und speichert Sie dann in der $Credential-Variablen.</span><span class="sxs-lookup"><span data-stu-id="c6013-123">The first command gets the user credentials, and then stores them in the $Credential variable.</span></span>

<span data-ttu-id="c6013-124">Mit dem zweiten Befehl wird ein Azure Resource Manager-Konto mit den Anmeldeinformationen in $Credential hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="c6013-124">The second command adds an Azure Resource Manager account with the credentials in $Credential.</span></span>

<span data-ttu-id="c6013-125">Dieses Konto authentifiziert sich beim Azure Resource Manager mit den Anmeldeinformationen für die Organisations-ID.</span><span class="sxs-lookup"><span data-stu-id="c6013-125">This account authenticates with Azure Resource Manager using organizational ID credentials.</span></span>
<span data-ttu-id="c6013-126">Sie können keine mehrstufigen Authentifizierungs-oder Microsoft-Kontoanmeldeinformationen verwenden, um Azure Resource Manager-Cmdlets mit diesem Konto auszuführen.</span><span class="sxs-lookup"><span data-stu-id="c6013-126">You cannot use multi-factor authentication or Microsoft account credentials to run Azure Resource Manager cmdlets with this account.</span></span>

### <span data-ttu-id="c6013-127">Beispiel 3: Hinzufügen eines Kontos, das mit den Dienstprinzipal Anmeldeinformationen authentifiziert wird</span><span class="sxs-lookup"><span data-stu-id="c6013-127">Example 3: Add an account that authenticates with service principal credentials</span></span>
```
PS C:\>$Credential = Get-Credential
PS C:\> Add-AzureRmAccount -Credential $Credential -Tenant "xxxx-xxxx-xxxx-xxxx" -ServicePrincipal
Account: xxxx-xxxx-xxxx-xxxx
Environment: AzureCloud
Subscription: yyyy-yyyy-yyyy-yyyy
Tenant: xxxx-xxxx-xxxx-xxxx
```

<span data-ttu-id="c6013-128">Der erste Befehl ruft die Anmeldeinformationen des Benutzers ab und speichert Sie dann in der $Credential-Variablen.</span><span class="sxs-lookup"><span data-stu-id="c6013-128">The first command gets the user credentials, and then stores them in the $Credential variable.</span></span>

<span data-ttu-id="c6013-129">Der zweite Befehl fügt ein Azure Resource Manager-Konto mit den Anmeldeinformationen hinzu, die in $Credential für den angegebenen Mandanten gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="c6013-129">The second command adds an Azure Resource Manager account with the credentials stored in $Credential for the specified Tenant.</span></span>
<span data-ttu-id="c6013-130">Der ServicePrincipal-Parameter "Switch" gibt an, dass sich das Konto als Dienstprinzipal authentifiziert.</span><span class="sxs-lookup"><span data-stu-id="c6013-130">The ServicePrincipal switch parameter indicates that the account authenticates as a service principal.</span></span>

### <span data-ttu-id="c6013-131">Beispiel 4: Hinzufügen eines Kontos für einen bestimmten Mandanten und ein Abonnement</span><span class="sxs-lookup"><span data-stu-id="c6013-131">Example 4: Add an account for a specific tenant and subscription</span></span>
```
PS C:\>Add-AzureRmAccount -Tenant "xxxx-xxxx-xxxx-xxxx" -SubscriptionId "yyyy-yyyy-yyyy-yyyy"
Account: pfuller@contoso.com
Environment: AzureCloud
Subscription: yyyy-yyyy-yyyy-yyyy
Tenant: xxxx-xxxx-xxxx-xxxx
```

<span data-ttu-id="c6013-132">Mit diesem Befehl wird ein Azure Resource Manager-Konto hinzugefügt, damit Cmdlets für den angegebenen Mandanten und das Abonnement standardmäßig ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="c6013-132">This command adds an Azure Resource Manager account to run cmdlets for the specified tenant and subscription by default.</span></span>

## <span data-ttu-id="c6013-133">Parameter</span><span class="sxs-lookup"><span data-stu-id="c6013-133">PARAMETERS</span></span>

### <span data-ttu-id="c6013-134">-Access Token</span><span class="sxs-lookup"><span data-stu-id="c6013-134">-AccessToken</span></span>
<span data-ttu-id="c6013-135">Gibt ein Zugriffstoken an.</span><span class="sxs-lookup"><span data-stu-id="c6013-135">Specifies an access token.</span></span>

```yaml
Type: String
Parameter Sets: AccessTokenWithSubscriptionId, AccessTokenWithSubscriptionName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6013-136">-Konto-Nr</span><span class="sxs-lookup"><span data-stu-id="c6013-136">-AccountId</span></span>
<span data-ttu-id="c6013-137">Konto-ID für Zugriffstoken</span><span class="sxs-lookup"><span data-stu-id="c6013-137">Account Id for access token</span></span>

```yaml
Type: String
Parameter Sets: AccessTokenWithSubscriptionId, AccessTokenWithSubscriptionName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6013-138">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="c6013-138">-ApplicationId</span></span>
<span data-ttu-id="c6013-139">SPN</span><span class="sxs-lookup"><span data-stu-id="c6013-139">SPN</span></span>

```yaml
Type: String
Parameter Sets: ServicePrincipalCertificateWithSubscriptionId, ServicePrincipalCertificateWithSubscriptionName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6013-140">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="c6013-140">-CertificateThumbprint</span></span>
<span data-ttu-id="c6013-141">Zertifikat Hash (Fingerabdruck)</span><span class="sxs-lookup"><span data-stu-id="c6013-141">Certificate Hash (Thumbprint)</span></span>

```yaml
Type: String
Parameter Sets: ServicePrincipalCertificateWithSubscriptionId, ServicePrincipalCertificateWithSubscriptionName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6013-142">– Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="c6013-142">-Credential</span></span>
<span data-ttu-id="c6013-143">Gibt ein PSCredential-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="c6013-143">Specifies a PSCredential object.</span></span>
<span data-ttu-id="c6013-144">Wenn Sie weitere Informationen zum PSCredential-Objekt wünschen, geben Sie Get-Help Get-Credential ein.</span><span class="sxs-lookup"><span data-stu-id="c6013-144">For more information about the PSCredential object, type Get-Help Get-Credential.</span></span>

<span data-ttu-id="c6013-145">Das PSCredential-Objekt enthält die Benutzer-ID und das Kennwort für die Anmeldeinformationen für die Organisations-ID oder die Anwendungs-ID und den Schlüssel für die Anmeldeinformationen des Dienst Prinzipals.</span><span class="sxs-lookup"><span data-stu-id="c6013-145">The PSCredential object provides the user ID and password for organizational ID credentials, or the application ID and secret for service principal credentials.</span></span>

```yaml
Type: PSCredential
Parameter Sets: UserWithSubscriptionId, UserWithSubscriptionName
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: PSCredential
Parameter Sets: ServicePrincipalWithSubscriptionId, ServicePrincipalWithSubscriptionName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6013-146">-Umgebung</span><span class="sxs-lookup"><span data-stu-id="c6013-146">-Environment</span></span>
<span data-ttu-id="c6013-147">Umgebung mit dem Konto, bei dem Sie sich anmelden können</span><span class="sxs-lookup"><span data-stu-id="c6013-147">Environment containing the account to log into</span></span>

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

### <span data-ttu-id="c6013-148">-ServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="c6013-148">-ServicePrincipal</span></span>
<span data-ttu-id="c6013-149">Gibt an, dass sich dieses Konto durch die Bereitstellung von Dienstprinzipal Anmeldeinformationen authentifiziert.</span><span class="sxs-lookup"><span data-stu-id="c6013-149">Indicates that this account authenticates by providing service principal credentials.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ServicePrincipalWithSubscriptionId, ServicePrincipalWithSubscriptionName, ServicePrincipalCertificateWithSubscriptionId, ServicePrincipalCertificateWithSubscriptionName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6013-150">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="c6013-150">-SubscriptionId</span></span>
<span data-ttu-id="c6013-151">Gibt die ID des Abonnements an.</span><span class="sxs-lookup"><span data-stu-id="c6013-151">Specifies the ID of the subscription.</span></span>
<span data-ttu-id="c6013-152">Wenn Sie diesen Parameter nicht angeben, wird das erste Abonnement aus der Abonnementliste verwendet.</span><span class="sxs-lookup"><span data-stu-id="c6013-152">If you do not specify this parameter, the first subscription from the subscription list is used.</span></span>

```yaml
Type: String
Parameter Sets: UserWithSubscriptionId, ServicePrincipalWithSubscriptionId, ServicePrincipalCertificateWithSubscriptionId, AccessTokenWithSubscriptionId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c6013-153">-Abonnementname</span><span class="sxs-lookup"><span data-stu-id="c6013-153">-SubscriptionName</span></span>
<span data-ttu-id="c6013-154">Name des Abonnements</span><span class="sxs-lookup"><span data-stu-id="c6013-154">Subscription Name</span></span>

```yaml
Type: String
Parameter Sets: UserWithSubscriptionName, ServicePrincipalWithSubscriptionName, ServicePrincipalCertificateWithSubscriptionName, AccessTokenWithSubscriptionName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c6013-155">-Mandanten-Nr</span><span class="sxs-lookup"><span data-stu-id="c6013-155">-TenantId</span></span>
<span data-ttu-id="c6013-156">Optionaler Mandantenname oder ID</span><span class="sxs-lookup"><span data-stu-id="c6013-156">Optional tenant name or ID</span></span>

```yaml
Type: String
Parameter Sets: UserWithSubscriptionId, UserWithSubscriptionName, AccessTokenWithSubscriptionId, AccessTokenWithSubscriptionName
Aliases: Domain

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ServicePrincipalWithSubscriptionId, ServicePrincipalWithSubscriptionName, ServicePrincipalCertificateWithSubscriptionId, ServicePrincipalCertificateWithSubscriptionName
Aliases: Domain

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6013-157">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c6013-157">-Confirm</span></span>
<span data-ttu-id="c6013-158">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c6013-158">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c6013-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c6013-159">-WhatIf</span></span>
<span data-ttu-id="c6013-160">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c6013-160">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c6013-161">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c6013-161">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c6013-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6013-162">CommonParameters</span></span>
<span data-ttu-id="c6013-163">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c6013-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6013-164">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c6013-164">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6013-165">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c6013-165">INPUTS</span></span>

## <span data-ttu-id="c6013-166">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c6013-166">OUTPUTS</span></span>

### <span data-ttu-id="c6013-167">PSAzureProfile</span><span class="sxs-lookup"><span data-stu-id="c6013-167">PSAzureProfile</span></span>

## <span data-ttu-id="c6013-168">Notizen</span><span class="sxs-lookup"><span data-stu-id="c6013-168">NOTES</span></span>

## <span data-ttu-id="c6013-169">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c6013-169">RELATED LINKS</span></span>

