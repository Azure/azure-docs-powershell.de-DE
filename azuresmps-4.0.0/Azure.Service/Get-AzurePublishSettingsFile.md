---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: A5419F76-B85E-445D-84EA-CC695B175C8D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1364cf1bbec1fdca2a8c9901556d38de0b620358
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005839"
---
# <span data-ttu-id="da852-101">Get-AzurePublishSettingsFile</span><span class="sxs-lookup"><span data-stu-id="da852-101">Get-AzurePublishSettingsFile</span></span>

## <span data-ttu-id="da852-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="da852-102">SYNOPSIS</span></span>
<span data-ttu-id="da852-103">Lädt die Datei für die Veröffentlichungseinstellungen für ein Azure-Abonnement herunter.</span><span class="sxs-lookup"><span data-stu-id="da852-103">Downloads the publish settings file for an Azure subscription.</span></span>

## <span data-ttu-id="da852-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="da852-104">SYNTAX</span></span>

```
Get-AzurePublishSettingsFile [-Environment <String>] [-Realm <String>] [-PassThru] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="da852-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="da852-105">DESCRIPTION</span></span>
<span data-ttu-id="da852-106">Das Cmdlet " **Get-AzurePublishSettingsFile** " downloadet eine Datei für Veröffentlichungseinstellungen für ein Abonnement in Ihrem Konto.</span><span class="sxs-lookup"><span data-stu-id="da852-106">The **Get-AzurePublishSettingsFile** cmdlet downloads a publish settings file for a subscription in your account.</span></span>
<span data-ttu-id="da852-107">Nach Abschluss des Befehls können Sie das Cmdlet **Import-PublishSettingsFile** verwenden, um die Einstellungen in der Datei für Windows PowerShell zur Verfügung zu stellen.</span><span class="sxs-lookup"><span data-stu-id="da852-107">When the command completes, you can use the **Import-PublishSettingsFile** cmdlet to make the settings in the file available to Windows PowerShell.</span></span>

<span data-ttu-id="da852-108">Wenn Sie Ihr Azure-Konto für Windows PowerShell verfügbar machen möchten, können Sie eine Datei für Veröffentlichungseinstellungen oder das Cmdlet **Add-AzureAccount** verwenden.</span><span class="sxs-lookup"><span data-stu-id="da852-108">To make your Azure account available to Windows PowerShell, you can use a publish settings file or the **Add-AzureAccount** cmdlet.</span></span>
<span data-ttu-id="da852-109">Mit den Einstellungen für "Veröffentlichungseinstellungen" können Sie die Sitzung im Voraus vorbereiten, damit Skripts und Hintergrundaufträge unbeaufsichtigt ausgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="da852-109">Publish settings files let you prepare the session in advance so you can run scripts and background jobs unattended.</span></span>
<span data-ttu-id="da852-110">Allerdings unterstützen nicht alle Dienste Veröffentlichungs Einstellungsdateien.</span><span class="sxs-lookup"><span data-stu-id="da852-110">However, not all services support publish settings files.</span></span>
<span data-ttu-id="da852-111">Beispielsweise unterstützt das **AzureResourceManager** -Modul keine Veröffentlichungs Einstellungsdateien.</span><span class="sxs-lookup"><span data-stu-id="da852-111">For example, the **AzureResourceManager** module does not support publish settings files.</span></span>

<span data-ttu-id="da852-112">Wenn Sie **Get-AzurePublishSettingsFile** ausführen, wird der Standardbrowser geöffnet, und Sie werden aufgefordert, sich bei Ihrem Azure-Konto anzumelden, ein Abonnement auszuwählen und einen Speicherort für das Dateisystem für die Datei für die Veröffentlichungseinstellungen auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="da852-112">When you run **Get-AzurePublishSettingsFile** , it opens your default browser and prompts you to sign into your Azure account, select a subscription, and select a file system location for the publish settings file.</span></span>
<span data-ttu-id="da852-113">Anschließend wird die Datei für die Veröffentlichungseinstellungen Ihres Abonnements in der von Ihnen ausgewählten Datei heruntergeladen.</span><span class="sxs-lookup"><span data-stu-id="da852-113">Then, it downloads the publish settings file for your subscription into the file that you selected.</span></span>

<span data-ttu-id="da852-114">Eine "Veröffentlichungs Einstellungsdatei" ist eine XML-Datei mit der Dateinamenerweiterung publishsettings.</span><span class="sxs-lookup"><span data-stu-id="da852-114">A "publish settings file" is an XML file with a .publishsettings file name extension.</span></span>
<span data-ttu-id="da852-115">Die Datei enthält ein codiertes Zertifikat, das Verwaltungsanmeldeinformationen für Ihre Azure-Abonnements bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="da852-115">The file contains an encoded certificate that provides management credentials for your Azure subscriptions.</span></span>

<span data-ttu-id="da852-116">**Sicherheitshinweis:** Die Veröffentlichungs Einstellungsdateien enthalten Anmeldeinformationen, die zum Verwalten Ihrer Azure-Abonnements und-Dienste verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="da852-116">**Security Note:** Publish settings files contains credentials that are used to administer your Azure subscriptions and services.</span></span>
<span data-ttu-id="da852-117">Wenn böswillige Benutzer auf Ihre Veröffentlichungs Einstellungsdatei zugreifen, können Sie Ihre Azure-Dienste bearbeiten, erstellen und löschen.</span><span class="sxs-lookup"><span data-stu-id="da852-117">If  malicious users access your publish settings file,  they can edit, create, and delete your Azure services.</span></span>
<span data-ttu-id="da852-118">Aus Sicherheitsgründen empfiehlt es sich, die Datei an einem Speicherort im Ordner "Downloads" oder "Dokumente" zu speichern und diese dann nach Verwendung des Cmdlets " **Import-AzurePublishSettingsFile** " zu löschen, um die Einstellungen zu importieren.</span><span class="sxs-lookup"><span data-stu-id="da852-118">As a security best practice, save the file to a location in your Downloads or Documents folder and then delete it after using **Import-AzurePublishSettingsFile** cmdlet to import the settings.</span></span>

<span data-ttu-id="da852-119">In diesem Thema wird das Cmdlet in der 0.8.10-Version des Microsoft Azure PowerShell-Moduls beschrieben.</span><span class="sxs-lookup"><span data-stu-id="da852-119">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="da852-120">Wenn Sie die Version des verwendeten Moduls abrufen möchten, geben Sie in der Azure PowerShell-Konsole `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="da852-120">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

## <span data-ttu-id="da852-121">Beispiele</span><span class="sxs-lookup"><span data-stu-id="da852-121">EXAMPLES</span></span>

### <span data-ttu-id="da852-122">Beispiel 1: Herunterladen einer Datei für Veröffentlichungseinstellungen</span><span class="sxs-lookup"><span data-stu-id="da852-122">Example 1: Download a publish settings file</span></span>
```
PS C:\> Get-AzurePublishSettingsFile
```

<span data-ttu-id="da852-123">Mit diesem Befehl wird der Standardbrowser geöffnet, eine Verbindung mit Ihrem Windows Azure-Konto hergestellt und dann die publishsettings-Datei für Ihr Konto heruntergeladen.</span><span class="sxs-lookup"><span data-stu-id="da852-123">This command opens your default browser, connects to your Windows Azure account, and then downloads the .publishsettings file for your account.</span></span>

### <span data-ttu-id="da852-124">Beispiel 2: Angeben eines Bereichs</span><span class="sxs-lookup"><span data-stu-id="da852-124">Example 2: Specify a realm</span></span>
```
PS C:\> Get-AzurePublishSettingsFile -Realm contoso.com -Passthru
```

<span data-ttu-id="da852-125">Mit diesem Befehl wird die Datei für die Veröffentlichungseinstellungen für ein Konto in der contoso.com-Domäne heruntergeladen.</span><span class="sxs-lookup"><span data-stu-id="da852-125">This command downloads the publish settings file for an account in the contoso.com domain.</span></span>
<span data-ttu-id="da852-126">Verwenden Sie einen Befehl mit dem **Bereich** -Parameter, wenn Sie sich bei Azure mit einem organisationskonto anstatt mit einem Microsoft-Konto anmelden.</span><span class="sxs-lookup"><span data-stu-id="da852-126">Use a command with the **Realm** parameter when you sign into Azure with an organizational account, instead of a Microsoft account.</span></span>

## <span data-ttu-id="da852-127">Parameter</span><span class="sxs-lookup"><span data-stu-id="da852-127">PARAMETERS</span></span>

### <span data-ttu-id="da852-128">-Umgebung</span><span class="sxs-lookup"><span data-stu-id="da852-128">-Environment</span></span>
<span data-ttu-id="da852-129">Gibt eine Azure-Umgebung an.</span><span class="sxs-lookup"><span data-stu-id="da852-129">Specifies an Azure environment.</span></span>

<span data-ttu-id="da852-130">Eine Azure-Umgebung eine unabhängige Bereitstellung von Microsoft Azure, wie AzureCloud für Global Azure und AzureChinaCloud für Azure, betrieben von 21Vianet in China.</span><span class="sxs-lookup"><span data-stu-id="da852-130">An Azure environment an independent deployment of Microsoft Azure, such as AzureCloud for global Azure and AzureChinaCloud for Azure operated by 21Vianet in China.</span></span>
<span data-ttu-id="da852-131">Sie können auch lokale Azure-Umgebungen mithilfe von Azure Pack und den WAPack-Cmdlets erstellen.</span><span class="sxs-lookup"><span data-stu-id="da852-131">You can also create on-premises Azure environments by using Azure Pack and the WAPack cmdlets.</span></span>
<span data-ttu-id="da852-132">Weitere Informationen finden Sie unter [Azure Pack](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx)  ( https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) .</span><span class="sxs-lookup"><span data-stu-id="da852-132">For more information, see [Azure Pack](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx)  (https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx).</span></span>

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

### <span data-ttu-id="da852-133">-PassThru</span><span class="sxs-lookup"><span data-stu-id="da852-133">-PassThru</span></span>
<span data-ttu-id="da852-134">Gibt $true zurück, wenn der Befehl erfolgreich ist, und $false, wenn ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="da852-134">Returns $True if the command succeeds and $False if it fails.</span></span>
<span data-ttu-id="da852-135">Standardmäßig gibt dieses Cmdlet keine Ausgabe zurück.</span><span class="sxs-lookup"><span data-stu-id="da852-135">By default, this cmdlet does not return any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da852-136">-Profil</span><span class="sxs-lookup"><span data-stu-id="da852-136">-Profile</span></span>
<span data-ttu-id="da852-137">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="da852-137">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="da852-138">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="da852-138">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="da852-139">-Realm</span><span class="sxs-lookup"><span data-stu-id="da852-139">-Realm</span></span>
<span data-ttu-id="da852-140">Gibt die Organisation in einer Organisations-ID an.</span><span class="sxs-lookup"><span data-stu-id="da852-140">Specifies the organization in an organizational ID.</span></span>
<span data-ttu-id="da852-141">Wenn Sie sich beispielsweise bei Azure as anmelden admin@contoso.com , lautet der Wert des **Bereichs** Parameters contoso.com.</span><span class="sxs-lookup"><span data-stu-id="da852-141">For example, if you sign into Azure as admin@contoso.com, the value of the **Realm** parameter is contoso.com.</span></span>
<span data-ttu-id="da852-142">Verwenden Sie diesen Parameter, wenn Sie eine Organisations-ID verwenden, um sich beim Azure-Portal anzumeldet.</span><span class="sxs-lookup"><span data-stu-id="da852-142">Use this parameter when you use an organizational ID to sign into the Azure portal.</span></span>
<span data-ttu-id="da852-143">Dieser Parameter ist nicht erforderlich, wenn Sie ein Microsoft-Konto verwenden, beispielsweise ein Outlook.com-oder Live.com-Konto.</span><span class="sxs-lookup"><span data-stu-id="da852-143">This parameter is not required when you use a Microsoft account, such as an outlook.com or live.com account.</span></span>

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

### <span data-ttu-id="da852-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da852-144">CommonParameters</span></span>
<span data-ttu-id="da852-145">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da852-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da852-146">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="da852-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da852-147">Eingaben</span><span class="sxs-lookup"><span data-stu-id="da852-147">INPUTS</span></span>

### <span data-ttu-id="da852-148">Keine</span><span class="sxs-lookup"><span data-stu-id="da852-148">None</span></span>
<span data-ttu-id="da852-149">Sie können die Eingabe an dieses Cmdlet nach Eigenschaftsname, aber nicht nach Wert übergeben.</span><span class="sxs-lookup"><span data-stu-id="da852-149">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="da852-150">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="da852-150">OUTPUTS</span></span>

### <span data-ttu-id="da852-151">None oder System. Boolean</span><span class="sxs-lookup"><span data-stu-id="da852-151">None or System.Boolean</span></span>
<span data-ttu-id="da852-152">Wenn Sie den *passthru* -Parameter verwenden, gibt dieses Cmdlet einen booleschen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="da852-152">When you use the *PassThru* parameter, this cmdlet returns a Boolean value.</span></span>
<span data-ttu-id="da852-153">Andernfalls gibt dieses Cmdlet keine Ausgabe zurück.</span><span class="sxs-lookup"><span data-stu-id="da852-153">Otherwise, this cmdlet does not return any output</span></span>

## <span data-ttu-id="da852-154">Notizen</span><span class="sxs-lookup"><span data-stu-id="da852-154">NOTES</span></span>

## <span data-ttu-id="da852-155">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="da852-155">RELATED LINKS</span></span>

[<span data-ttu-id="da852-156">Add-AzureAccount</span><span class="sxs-lookup"><span data-stu-id="da852-156">Add-AzureAccount</span></span>](./Add-AzureAccount.md)

[<span data-ttu-id="da852-157">Importieren-AzurePublishSettingsFile</span><span class="sxs-lookup"><span data-stu-id="da852-157">Import-AzurePublishSettingsFile</span></span>](./Import-AzurePublishSettingsFile.md)


