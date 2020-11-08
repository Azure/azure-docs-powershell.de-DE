---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: 6185C6BA-460E-4EEA-B1EF-CD67629AA75E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 51c20ef378cd2629ea96f236339a97172fb3038e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006156"
---
# <span data-ttu-id="36292-101">Set-AzureSubscription</span><span class="sxs-lookup"><span data-stu-id="36292-101">Set-AzureSubscription</span></span>

## <span data-ttu-id="36292-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="36292-102">SYNOPSIS</span></span>
<span data-ttu-id="36292-103">Ändert ein Azure-Abonnement.</span><span class="sxs-lookup"><span data-stu-id="36292-103">Changes an Azure subscription.</span></span>

## <span data-ttu-id="36292-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="36292-104">SYNTAX</span></span>

### <span data-ttu-id="36292-105">UpdateSubscriptionByIdParameterSetName (Standard)</span><span class="sxs-lookup"><span data-stu-id="36292-105">UpdateSubscriptionByIdParameterSetName (Default)</span></span>
```
Set-AzureSubscription -SubscriptionId <String> [-Certificate <X509Certificate2>] [-ServiceEndpoint <String>]
 [-ResourceManagerEndpoint <String>] [-CurrentStorageAccountName <String>] [-Context <AzureStorageContext>]
 [-Environment <String>] [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="36292-106">UpdateSubscriptionByNameParameterSetName</span><span class="sxs-lookup"><span data-stu-id="36292-106">UpdateSubscriptionByNameParameterSetName</span></span>
```
Set-AzureSubscription -SubscriptionName <String> [-Certificate <X509Certificate2>] [-ServiceEndpoint <String>]
 [-ResourceManagerEndpoint <String>] [-CurrentStorageAccountName <String>] [-Context <AzureStorageContext>]
 [-Environment <String>] [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="36292-107">AddSubscriptionParameterSetName</span><span class="sxs-lookup"><span data-stu-id="36292-107">AddSubscriptionParameterSetName</span></span>
```
Set-AzureSubscription -SubscriptionName <String> -SubscriptionId <String> -Certificate <X509Certificate2>
 [-ServiceEndpoint <String>] [-ResourceManagerEndpoint <String>] [-CurrentStorageAccountName <String>]
 [-Context <AzureStorageContext>] [-Environment <String>] [-PassThru] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="36292-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="36292-108">DESCRIPTION</span></span>
<span data-ttu-id="36292-109">Das Cmdlet " **Satz-AzureSubscription** " erstellt und ändert die Eigenschaften eines Azure-Abonnementobjekts.</span><span class="sxs-lookup"><span data-stu-id="36292-109">The **Set-AzureSubscription** cmdlet establishes and changes the properties of an Azure subscription object.</span></span>
<span data-ttu-id="36292-110">Sie können dieses Cmdlet verwenden, um in einem Azure-Abonnement zu arbeiten, bei dem es sich nicht um Ihr Standardabonnement handelt, oder um Ihr aktuelles Speicherkonto zu ändern.</span><span class="sxs-lookup"><span data-stu-id="36292-110">You can use this cmdlet to work in an Azure subscription that is not your default subscription or to change your current storage account.</span></span>
<span data-ttu-id="36292-111">Informationen zu aktuellen und Standardabonnements finden Sie unter dem Cmdlet **Select-AzureSubscription** .</span><span class="sxs-lookup"><span data-stu-id="36292-111">For information about current and default subscriptions, see the **Select-AzureSubscription** cmdlet.</span></span>

<span data-ttu-id="36292-112">Dieses Cmdlet arbeitet für ein Azure-Abonnementobjekt und nicht für das tatsächliche Azure-Abonnement.</span><span class="sxs-lookup"><span data-stu-id="36292-112">This cmdlet operates on an Azure subscription object, not your actual Azure subscription.</span></span>
<span data-ttu-id="36292-113">Besuchen Sie zum Erstellen und Bereitstellen eines Azure-Abonnements das [Azure-Portal](https://azure.microsoft.com/) ( https://azure.microsoft.com/) .</span><span class="sxs-lookup"><span data-stu-id="36292-113">To create and provision an Azure subscription, visit the [Azure Portal](https://azure.microsoft.com/) (https://azure.microsoft.com/).</span></span>

<span data-ttu-id="36292-114">Mit diesem Cmdlet werden die Daten in der Abonnementdaten Datei geändert, die Sie erstellen, wenn Sie Windows PowerShell mithilfe des Cmdlets **Add-AzureAccount** oder **Import-AzurePublishSettingsFile** ein Azure-Konto hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="36292-114">This cmdlet changes the data in the subscription data file that you create when you use the **Add-AzureAccount** or **Import-AzurePublishSettingsFile** cmdlet to add an Azure account to Windows PowerShell.</span></span>

<span data-ttu-id="36292-115">In diesem Thema wird das Cmdlet in der 0.8.10-Version des Microsoft Azure PowerShell-Moduls beschrieben.</span><span class="sxs-lookup"><span data-stu-id="36292-115">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="36292-116">Wenn Sie die Version des verwendeten Moduls abrufen möchten, geben Sie in der Azure PowerShell-Konsole `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="36292-116">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

## <span data-ttu-id="36292-117">Beispiele</span><span class="sxs-lookup"><span data-stu-id="36292-117">EXAMPLES</span></span>

### <span data-ttu-id="36292-118">Beispiel 1: Ändern einer vorhandenen abonnement1</span><span class="sxs-lookup"><span data-stu-id="36292-118">Example 1: Change an existing subscription1</span></span>
```
C:\PS> $thumbprint = <Thumbprint-2>
C:\PS> $differentCert = Get-Item cert:\\CurrentUser\My\$thumbprint 
C:\PS> Set-AzureSubscription -SubscriptionName ContosoEngineering -Certificate $differentCert
```

<span data-ttu-id="36292-119">In diesem Beispiel wird das Zertifikat für das Abonnement mit dem Namen ContosoEngineering geändert.</span><span class="sxs-lookup"><span data-stu-id="36292-119">This example changes the certificate for the subscription named ContosoEngineering.</span></span>

### <span data-ttu-id="36292-120">Beispiel 2: Ändern des Dienstendpunkts</span><span class="sxs-lookup"><span data-stu-id="36292-120">Example 2: Change the service endpoint</span></span>
```
C:\PS> Set-AzureSubscription -SubscriptionName ContosoEngineering -ServiceEndpoint "https://management.core.contoso.com"
```

<span data-ttu-id="36292-121">Mit diesem Befehl wird ein benutzerdefinierter Dienstendpunkt für das ContosoEngineering-Abonnement hinzugefügt oder geändert.</span><span class="sxs-lookup"><span data-stu-id="36292-121">This command adds or changes a custom service endpoint for the ContosoEngineering subscription.</span></span>

### <span data-ttu-id="36292-122">Beispiel 3: Löschen von Eigenschaftswerten</span><span class="sxs-lookup"><span data-stu-id="36292-122">Example 3: Clear property values</span></span>
```
C:\PS> Set-AzureSubscription -SubscriptionName ContosoEngineering -Certificate $null -ResourceManagerEndpoint $Null
```

<span data-ttu-id="36292-123">Mit diesem Befehl werden die Werte der Eigenschaften Certificate und ResourceManagerEndpoint auf NULL ($null) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="36292-123">This command sets the values of the Certificate and ResourceManagerEndpoint properties to null ($Null).</span></span>
<span data-ttu-id="36292-124">Dadurch werden die Werte dieser Eigenschaften gelöscht, ohne dass andere Einstellungen geändert werden.</span><span class="sxs-lookup"><span data-stu-id="36292-124">This clears the values of those properties without changing other settings.</span></span>

### <span data-ttu-id="36292-125">Beispiel 4: Verwenden einer alternativen Abonnement Datendatei</span><span class="sxs-lookup"><span data-stu-id="36292-125">Example 4: Use an alternate subscription data file</span></span>
```
C:\PS> Set-AzureSubscription -SubscriptionName ContosoFinance -SubscriptionDataFile C:\Azure\SubscriptionData.xml -CurrentStorageAccount ContosoStorage01
```

<span data-ttu-id="36292-126">Mit diesem Befehl wird das aktuelle Speicherkonto des ContosoFinance-Abonnements in ContosoStorage01 geändert.</span><span class="sxs-lookup"><span data-stu-id="36292-126">This command changes the current storage account of the ContosoFinance subscription to ContosoStorage01.</span></span>
<span data-ttu-id="36292-127">Der Befehl verwendet den **SubscriptionDataFile** -Parameter, um die Daten in der C:\Azure\SubscriptionData.xml-Abonnement Datendatei zu ändern.</span><span class="sxs-lookup"><span data-stu-id="36292-127">The command uses the **SubscriptionDataFile** parameter to change the data in the C:\Azure\SubscriptionData.xml subscription data file.</span></span>
<span data-ttu-id="36292-128">Standardmäßig verwendet " **Satz-AzureSubscription** " die standardmäßige Abonnement Datendatei in Ihrem Roaming-Benutzerprofil.</span><span class="sxs-lookup"><span data-stu-id="36292-128">By default, **Set-AzureSubscription** uses the default subscription data file in your roaming user profile.</span></span>

## <span data-ttu-id="36292-129">Parameter</span><span class="sxs-lookup"><span data-stu-id="36292-129">PARAMETERS</span></span>

### <span data-ttu-id="36292-130">-Zertifikat</span><span class="sxs-lookup"><span data-stu-id="36292-130">-Certificate</span></span>
```yaml
Type: X509Certificate2
Parameter Sets: UpdateSubscriptionByIdParameterSetName, UpdateSubscriptionByNameParameterSetName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: X509Certificate2
Parameter Sets: AddSubscriptionParameterSetName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36292-131">-Context</span><span class="sxs-lookup"><span data-stu-id="36292-131">-Context</span></span>
```yaml
Type: AzureStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36292-132">-CurrentStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="36292-132">-CurrentStorageAccountName</span></span>
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

### <span data-ttu-id="36292-133">-Umgebung</span><span class="sxs-lookup"><span data-stu-id="36292-133">-Environment</span></span>
<span data-ttu-id="36292-134">Gibt eine Azure-Umgebung an.</span><span class="sxs-lookup"><span data-stu-id="36292-134">Specifies an Azure environment.</span></span>

<span data-ttu-id="36292-135">Eine Azure-Umgebung eine unabhängige Bereitstellung von Microsoft Azure, wie AzureCloud für Global Azure und AzureChinaCloud für Azure, betrieben von 21Vianet in China.</span><span class="sxs-lookup"><span data-stu-id="36292-135">An Azure environment an independent deployment of Microsoft Azure, such as AzureCloud for global Azure and AzureChinaCloud for Azure operated by 21Vianet in China.</span></span>
<span data-ttu-id="36292-136">Sie können auch lokale Azure-Umgebungen mithilfe von Azure Pack und den WAPack-Cmdlets erstellen.</span><span class="sxs-lookup"><span data-stu-id="36292-136">You can also create on-premises Azure environments by using Azure Pack and the WAPack cmdlets.</span></span>
<span data-ttu-id="36292-137">Weitere Informationen finden Sie unter [Azure Pack](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx)  ( https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) .</span><span class="sxs-lookup"><span data-stu-id="36292-137">For more information, see [Azure Pack](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx)  (https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx).</span></span>

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

### <span data-ttu-id="36292-138">-PassThru</span><span class="sxs-lookup"><span data-stu-id="36292-138">-PassThru</span></span>
<span data-ttu-id="36292-139">Gibt $true zurück, wenn der Befehl erfolgreich ist, und $false, wenn ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="36292-139">Returns $True if the command succeeds and $False if it fails.</span></span>
<span data-ttu-id="36292-140">Standardmäßig gibt dieses Cmdlet keine Ausgabe zurück.</span><span class="sxs-lookup"><span data-stu-id="36292-140">By default, this cmdlet does not return any output.</span></span>
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

### <span data-ttu-id="36292-141">-Profil</span><span class="sxs-lookup"><span data-stu-id="36292-141">-Profile</span></span>
<span data-ttu-id="36292-142">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="36292-142">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="36292-143">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="36292-143">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="36292-144">-ResourceManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="36292-144">-ResourceManagerEndpoint</span></span>
<span data-ttu-id="36292-145">Gibt den Endpunkt für Azure Resource Manager-Daten an, einschließlich Daten zu Ressourcengruppen, die dem Konto zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="36292-145">Specifies the endpoint for Azure Resource Manager data, including data about resource groups associated with the account.</span></span>
<span data-ttu-id="36292-146">Weitere Informationen zum Azure Resource Manager finden Sie unter [Azure Resource Manager-Cmdlets](https://go.microsoft.com/fwlink/?LinkID=394765)  ( https://go.microsoft.com/fwlink/?LinkID=394765) und [Verwenden von Windows PowerShell mit Ressourcen-Manager](https://go.microsoft.com/fwlink/?LinkID=394767)  ( https://go.microsoft.com/fwlink/?LinkID=394767) .</span><span class="sxs-lookup"><span data-stu-id="36292-146">For more information about Azure Resource Manager, see [Azure Resource Manager Cmdlets](https://go.microsoft.com/fwlink/?LinkID=394765)  (https://go.microsoft.com/fwlink/?LinkID=394765) and [Using Windows PowerShell with Resource Manager](https://go.microsoft.com/fwlink/?LinkID=394767)  (https://go.microsoft.com/fwlink/?LinkID=394767).</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36292-147">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="36292-147">-ServiceEndpoint</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36292-148">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="36292-148">-SubscriptionId</span></span>
```yaml
Type: String
Parameter Sets: UpdateSubscriptionByIdParameterSetName, AddSubscriptionParameterSetName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36292-149">-Abonnementname</span><span class="sxs-lookup"><span data-stu-id="36292-149">-SubscriptionName</span></span>
```yaml
Type: String
Parameter Sets: UpdateSubscriptionByNameParameterSetName, AddSubscriptionParameterSetName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36292-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36292-150">CommonParameters</span></span>
<span data-ttu-id="36292-151">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36292-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36292-152">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="36292-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36292-153">Eingaben</span><span class="sxs-lookup"><span data-stu-id="36292-153">INPUTS</span></span>

### <span data-ttu-id="36292-154">Keine</span><span class="sxs-lookup"><span data-stu-id="36292-154">None</span></span>
<span data-ttu-id="36292-155">Sie können die Eingabe an dieses Cmdlet nach Eigenschaftsname, aber nicht nach Wert übergeben.</span><span class="sxs-lookup"><span data-stu-id="36292-155">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="36292-156">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="36292-156">OUTPUTS</span></span>

### <span data-ttu-id="36292-157">None oder System. Boolean</span><span class="sxs-lookup"><span data-stu-id="36292-157">None or System.Boolean</span></span>
<span data-ttu-id="36292-158">Wenn Sie den *passthru* -Parameter verwenden, gibt dieses Cmdlet einen booleschen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="36292-158">When you use the *PassThru* parameter, this cmdlet returns a Boolean value.</span></span>
<span data-ttu-id="36292-159">Standardmäßig gibt dieses Cmdlet keine Ausgabe zurück.</span><span class="sxs-lookup"><span data-stu-id="36292-159">By default, this cmdlet does not return any output.</span></span>

## <span data-ttu-id="36292-160">Notizen</span><span class="sxs-lookup"><span data-stu-id="36292-160">NOTES</span></span>

## <span data-ttu-id="36292-161">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="36292-161">RELATED LINKS</span></span>

[<span data-ttu-id="36292-162">Add-AzureAccount</span><span class="sxs-lookup"><span data-stu-id="36292-162">Add-AzureAccount</span></span>](./Add-AzureAccount.md)

[<span data-ttu-id="36292-163">Get-AzureSubscription</span><span class="sxs-lookup"><span data-stu-id="36292-163">Get-AzureSubscription</span></span>](./Get-AzureSubscription.md)

[<span data-ttu-id="36292-164">Importieren-AzurePublishSettingsFile</span><span class="sxs-lookup"><span data-stu-id="36292-164">Import-AzurePublishSettingsFile</span></span>](./Import-AzurePublishSettingsFile.md)

[<span data-ttu-id="36292-165">Remove-AzureSubscription</span><span class="sxs-lookup"><span data-stu-id="36292-165">Remove-AzureSubscription</span></span>](./Remove-AzureSubscription.md)

[<span data-ttu-id="36292-166">SELECT-AzureSubscription</span><span class="sxs-lookup"><span data-stu-id="36292-166">Select-AzureSubscription</span></span>](./Select-AzureSubscription.md)


