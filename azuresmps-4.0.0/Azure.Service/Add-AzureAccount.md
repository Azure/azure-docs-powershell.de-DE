---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: 03EAFFB2-EA64-4227-A33B-D24EB4A75F71
online version: ''
schema: 2.0.0
ms.openlocfilehash: ac88bc2494bad975c6169262edd05c7b821061bb
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006602"
---
# <span data-ttu-id="93160-101">Add-AzureAccount</span><span class="sxs-lookup"><span data-stu-id="93160-101">Add-AzureAccount</span></span>

## <span data-ttu-id="93160-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="93160-102">SYNOPSIS</span></span>
<span data-ttu-id="93160-103">Fügt Windows PowerShell das Azure-Konto hinzu.</span><span class="sxs-lookup"><span data-stu-id="93160-103">Adds the Azure account to Windows PowerShell.</span></span>

## <span data-ttu-id="93160-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="93160-104">SYNTAX</span></span>

### <span data-ttu-id="93160-105">Benutzer (Standard)</span><span class="sxs-lookup"><span data-stu-id="93160-105">User (Default)</span></span>
```
Add-AzureAccount [-Environment <String>] [-Credential <PSCredential>] [-Tenant <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="93160-106">ServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="93160-106">ServicePrincipal</span></span>
```
Add-AzureAccount [-Environment <String>] -Credential <PSCredential> [-ServicePrincipal] -Tenant <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="93160-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="93160-107">DESCRIPTION</span></span>
<span data-ttu-id="93160-108">Mit dem Cmdlet **Add-AzureAccount** können Sie Ihr Azure-Konto und seine Abonnements in Windows PowerShell zur Verfügung stellen.</span><span class="sxs-lookup"><span data-stu-id="93160-108">The **Add-AzureAccount** cmdlet makes your Azure account and its subscriptions available in Windows PowerShell.</span></span>
<span data-ttu-id="93160-109">Es ist wie bei der Anmeldung bei Ihrem Azure-Konto in Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="93160-109">It's like logging into your Azure account in Windows PowerShell.</span></span>
<span data-ttu-id="93160-110">Zum Abmelden des Kontos verwenden Sie das Cmdlet **Remove-AzureAccount** .</span><span class="sxs-lookup"><span data-stu-id="93160-110">To log out of the account, use the **Remove-AzureAccount** cmdlet.</span></span>

<span data-ttu-id="93160-111">**Add-AzureAccount** downloadet Informationen zu Ihrem Azure-Konto und speichert Sie in einer Abonnement Datendatei in Ihrem Roaming-Benutzerprofil.</span><span class="sxs-lookup"><span data-stu-id="93160-111">**Add-AzureAccount** downloads information about your Azure account and saves it in a subscription data file in your roaming user profile.</span></span>
<span data-ttu-id="93160-112">Außerdem wird ein Zugriffstoken abgerufen, mit dem Windows PowerShell in Ihrem Auftrag auf Ihr Azure-Konto zugreifen kann.</span><span class="sxs-lookup"><span data-stu-id="93160-112">It also gets an access token that allows Windows PowerShell to access your Azure account on your behalf.</span></span>
<span data-ttu-id="93160-113">Nach Abschluss des Befehls können Sie Ihr Azure-Konto in Windows PowerShell verwalten.</span><span class="sxs-lookup"><span data-stu-id="93160-113">When the command completes, you can manage your Azure account in Windows PowerShell.</span></span>

<span data-ttu-id="93160-114">Es gibt zwei verschiedene Möglichkeiten, Ihr Azure-Konto für Windows PowerShell verfügbar zu machen.</span><span class="sxs-lookup"><span data-stu-id="93160-114">There are two different ways to make your Azure account available to Windows PowerShell.</span></span>
<span data-ttu-id="93160-115">Sie können das **Add-AzureAccount-** Cmdlet verwenden, das Azure Active Directory-Authentifizierungs Zugriffstoken (Azure AD) oder **Import-AzurePublishSettingsFile** verwendet, das ein Verwaltungszertifikat verwendet.</span><span class="sxs-lookup"><span data-stu-id="93160-115">You can use the **Add-AzureAccount** cmdlet, which uses Azure Active Directory (Azure AD) authentication access tokens, or **Import-AzurePublishSettingsFile** , which uses a management certificate.</span></span>
<span data-ttu-id="93160-116">Anleitungen zu den zu verwendenden Methoden finden Sie unter [so wird es gemacht: Herstellen einer Verbindung mit Ihrem Abonnement](https://azure.microsoft.com/documentation/articles/install-configure-powershell) ( https://azure.microsoft.com/documentation/articles/install-configure-powershell/#Connect) .</span><span class="sxs-lookup"><span data-stu-id="93160-116">For guidance on which method to use, see [How to: Connect to your subscription](https://azure.microsoft.com/documentation/articles/install-configure-powershell) (https://azure.microsoft.com/documentation/articles/install-configure-powershell/#Connect).</span></span>

<span data-ttu-id="93160-117">Wenn Sie **Add-AzureAccount** ausführen, wird ein interaktives Fenster angezeigt, in dem Sie aufgefordert werden, sich bei Ihrem Azure-Konto anzumeldet.</span><span class="sxs-lookup"><span data-stu-id="93160-117">When you run **Add-AzureAccount** , it displays an interactive window that prompts you to sign into your Azure account.</span></span>
<span data-ttu-id="93160-118">Diese Anmeldung ist gültig, bis das Zugriffstoken abläuft.</span><span class="sxs-lookup"><span data-stu-id="93160-118">This sign-in is valid until the access token expires.</span></span>
<span data-ttu-id="93160-119">Wenn es abläuft, werden Cmdlets, die Zugriff auf Ihr Konto benötigen, aufgefordert, **Add-AzureAccount** erneut auszuführen.</span><span class="sxs-lookup"><span data-stu-id="93160-119">When it expires, cmdlets that require access to your account prompt you to run **Add-AzureAccount** again.</span></span>

<span data-ttu-id="93160-120">In diesem Thema wird das Cmdlet in der 0.8.10-Version des Microsoft Azure PowerShell-Moduls beschrieben.</span><span class="sxs-lookup"><span data-stu-id="93160-120">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="93160-121">Wenn Sie die Version des verwendeten Moduls abrufen möchten, geben Sie in der Azure PowerShell-Konsole `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="93160-121">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

## <span data-ttu-id="93160-122">Beispiele</span><span class="sxs-lookup"><span data-stu-id="93160-122">EXAMPLES</span></span>

### <span data-ttu-id="93160-123">Beispiel 1: Hinzufügen eines Kontos</span><span class="sxs-lookup"><span data-stu-id="93160-123">Example 1: Add an account</span></span>
```
PS C:\> Add-AzureAccount
```

<span data-ttu-id="93160-124">Mit diesem Befehl wird Windows PowerShell ein Azure-Konto hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="93160-124">This command adds an Azure account to Windows PowerShell.</span></span>
<span data-ttu-id="93160-125">Wenn Sie den Befehl ausführen, wird ein Windows-Fenster eingeblendet, in dem Sie den Benutzernamen und das Kennwort des Kontos anfordern können.</span><span class="sxs-lookup"><span data-stu-id="93160-125">When you run the command, a windows pops up to request the user name and password of the account.</span></span>

### <span data-ttu-id="93160-126">Beispiel 2: Verwenden einer alternativen Abonnement Datendatei</span><span class="sxs-lookup"><span data-stu-id="93160-126">Example 2: Use an alternate subscription data file</span></span>
```
PS C:\> Add-AzureAccount -SubscriptionDataFile C:\Testing\SDF.xml
```

<span data-ttu-id="93160-127">Dieser Befehl verwendet den **SubscriptionDataFile** -Parameter, um **Add-AzureAccount** zu verweisen, um die Kontodaten anstelle der Standarddatei in der C:\Testing\SDF.xml Datei zu speichern.</span><span class="sxs-lookup"><span data-stu-id="93160-127">This command uses the **SubscriptionDataFile** parameter to direct **Add-AzureAccount** to store the account data in the C:\Testing\SDF.xml file, instead of the default file.</span></span>

## <span data-ttu-id="93160-128">Parameter</span><span class="sxs-lookup"><span data-stu-id="93160-128">PARAMETERS</span></span>

### <span data-ttu-id="93160-129">– Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="93160-129">-Credential</span></span>
```yaml
Type: PSCredential
Parameter Sets: User
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: PSCredential
Parameter Sets: ServicePrincipal
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93160-130">-Umgebung</span><span class="sxs-lookup"><span data-stu-id="93160-130">-Environment</span></span>
<span data-ttu-id="93160-131">Gibt eine Azure-Umgebung an.</span><span class="sxs-lookup"><span data-stu-id="93160-131">Specifies an Azure environment.</span></span>

<span data-ttu-id="93160-132">Eine Azure-Umgebung eine unabhängige Bereitstellung von Microsoft Azure, wie AzureCloud für Global Azure und AzureChinaCloud für Azure, betrieben von 21Vianet in China.</span><span class="sxs-lookup"><span data-stu-id="93160-132">An Azure environment an independent deployment of Microsoft Azure, such as AzureCloud for global Azure and AzureChinaCloud for Azure operated by 21Vianet in China.</span></span>
<span data-ttu-id="93160-133">Sie können auch lokale Azure-Umgebungen mithilfe von Azure Pack und den WAPack-Cmdlets erstellen.</span><span class="sxs-lookup"><span data-stu-id="93160-133">You can also create on-premises Azure environments by using Azure Pack and the WAPack cmdlets.</span></span>
<span data-ttu-id="93160-134">Weitere Informationen finden Sie unter [Azure Pack](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx)  ( https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) .</span><span class="sxs-lookup"><span data-stu-id="93160-134">For more information, see [Azure Pack](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx)  (https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx).</span></span>

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

### <span data-ttu-id="93160-135">-Profil</span><span class="sxs-lookup"><span data-stu-id="93160-135">-Profile</span></span>
<span data-ttu-id="93160-136">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="93160-136">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="93160-137">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="93160-137">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93160-138">-ServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="93160-138">-ServicePrincipal</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: ServicePrincipal
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93160-139">-Mandant</span><span class="sxs-lookup"><span data-stu-id="93160-139">-Tenant</span></span>
```yaml
Type: String
Parameter Sets: User
Aliases: TenantId

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ServicePrincipal
Aliases: TenantId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93160-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93160-140">CommonParameters</span></span>
<span data-ttu-id="93160-141">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="93160-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93160-142">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="93160-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93160-143">Eingaben</span><span class="sxs-lookup"><span data-stu-id="93160-143">INPUTS</span></span>

### <span data-ttu-id="93160-144">Keine</span><span class="sxs-lookup"><span data-stu-id="93160-144">None</span></span>
<span data-ttu-id="93160-145">Sie können keine Eingabe an dieses Cmdlet übergeben</span><span class="sxs-lookup"><span data-stu-id="93160-145">You cannot pipe input to this cmdlet</span></span>

## <span data-ttu-id="93160-146">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="93160-146">OUTPUTS</span></span>

### <span data-ttu-id="93160-147">Keine</span><span class="sxs-lookup"><span data-stu-id="93160-147">None</span></span>
<span data-ttu-id="93160-148">Dieses Cmdlet gibt keine Ausgabe zurück.</span><span class="sxs-lookup"><span data-stu-id="93160-148">This cmdlet does not return any output.</span></span>

## <span data-ttu-id="93160-149">Notizen</span><span class="sxs-lookup"><span data-stu-id="93160-149">NOTES</span></span>
* <span data-ttu-id="93160-150">**Add-AzureAccount** (und die Azure AD-Authentifizierungsmethode) hat Vorrang vor der **Import-AzurePublishSettings** (und der Management Certificate-Methode).</span><span class="sxs-lookup"><span data-stu-id="93160-150">**Add-AzureAccount** (and the Azure AD authentication method) takes precedence over **Import-AzurePublishSettings** (and the management certificate method).</span></span> <span data-ttu-id="93160-151">Wenn Sie **Add-AzureAccount** auch einmal für Ihr Konto verwenden, wird die Azure AD-Authentifizierungsmethode verwendet, und das Verwaltungszertifikat wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="93160-151">If you use **Add-AzureAccount** even once on your account, the Azure AD authentication method is used and the management certificate is ignored.</span></span> <span data-ttu-id="93160-152">Wenn Sie das Azure AD-Token entfernen und die Verwaltungszertifikat Methode wiederherstellen möchten, verwenden Sie das Cmdlet **Remove-AzureAccount** .</span><span class="sxs-lookup"><span data-stu-id="93160-152">To remove the Azure AD token and restore the management certificate method, use the **Remove-AzureAccount** cmdlet.</span></span> <span data-ttu-id="93160-153">Wenn Sie weitere Informationen benötigen, geben Sie Folgendes ein: **get-help Remove-AzureAccount**.</span><span class="sxs-lookup"><span data-stu-id="93160-153">For more information, type: **Get-Help Remove-AzureAccount**.</span></span>
* <span data-ttu-id="93160-154">Der Fehler "Ihre Anmeldeinformationen sind abgelaufen.</span><span class="sxs-lookup"><span data-stu-id="93160-154">The error, "Your credentials have expired.</span></span> <span data-ttu-id="93160-155">Bitte verwenden Sie Add-AzureAccount, um sich erneut anzumelden. "</span><span class="sxs-lookup"><span data-stu-id="93160-155">Please use Add-AzureAccount to log in again."</span></span> <span data-ttu-id="93160-156">Gibt an, dass das Zugriffstoken abgelaufen ist und Windows PowerShell nicht auf Ihr Azure-Konto zugreifen kann.</span><span class="sxs-lookup"><span data-stu-id="93160-156">indicates that your access token is expired and Windows PowerShell cannot access your Azure account.</span></span> <span data-ttu-id="93160-157">Wenn Sie den Zugriff auf Ihr Konto wiederherstellen möchten, führen **Sie Add-AzureAccount** erneut aus.</span><span class="sxs-lookup"><span data-stu-id="93160-157">To restore access to your account, run **Add-AzureAccount** again.</span></span>
* <span data-ttu-id="93160-158">Die Azure PowerShell-Konto-und Abonnement-Cmdlets erhalten Ihre Daten aus der Abonnement Datendatei, nicht aus dem Live Azure-Konto.</span><span class="sxs-lookup"><span data-stu-id="93160-158">The Azure PowerShell account and subscription cmdlets get their data from the  subscription data file, not from the live Azure account.</span></span> <span data-ttu-id="93160-159">Wenn Sie Ihr Konto oder Ihre Abonnements außerhalb von Windows PowerShell ändern, beispielsweise mithilfe des Azure-Verwaltungsportals, führen Sie **Add-AzureAccount** erneut aus, um die Abonnement Datendatei zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="93160-159">If you change your account or subscriptions outside of Windows PowerShell, such as by using the Azure Management Portal, run **Add-AzureAccount** again to refresh the subscription data file.</span></span>

## <span data-ttu-id="93160-160">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="93160-160">RELATED LINKS</span></span>

[<span data-ttu-id="93160-161">Add-AzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="93160-161">Add-AzureEnvironment</span></span>](./Add-AzureEnvironment.md)

[<span data-ttu-id="93160-162">Get-AzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="93160-162">Get-AzureEnvironment</span></span>](./Get-AzureEnvironment.md)

[<span data-ttu-id="93160-163">Importieren-AzurePublishSettingsFile</span><span class="sxs-lookup"><span data-stu-id="93160-163">Import-AzurePublishSettingsFile</span></span>](./Import-AzurePublishSettingsFile.md)

[<span data-ttu-id="93160-164">Get-AzureAccount</span><span class="sxs-lookup"><span data-stu-id="93160-164">Get-AzureAccount</span></span>](./Get-AzureAccount.md)

[<span data-ttu-id="93160-165">Remove-AzureAccount</span><span class="sxs-lookup"><span data-stu-id="93160-165">Remove-AzureAccount</span></span>](./Remove-AzureAccount.md)


