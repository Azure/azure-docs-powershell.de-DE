---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: 79D64D7C-6671-4F03-8776-70A716F36512
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2bc0525ee7238de421842b74f52f7dd4fa59df1a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006467"
---
# <span data-ttu-id="aca4a-101">Import-AzurePublishSettingsFile</span><span class="sxs-lookup"><span data-stu-id="aca4a-101">Import-AzurePublishSettingsFile</span></span>

## <span data-ttu-id="aca4a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="aca4a-102">SYNOPSIS</span></span>
<span data-ttu-id="aca4a-103">Importiert eine Datei für Veröffentlichungseinstellungen, in der Sie Ihre Azure-Konten in Windows PowerShell verwalten können.</span><span class="sxs-lookup"><span data-stu-id="aca4a-103">Imports a publish settings file that lets you manage your Azure accounts in Windows PowerShell.</span></span>

## <span data-ttu-id="aca4a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="aca4a-104">SYNTAX</span></span>

```
Import-AzurePublishSettingsFile -PublishSettingsFile <String> [-Environment <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="aca4a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="aca4a-105">DESCRIPTION</span></span>
<span data-ttu-id="aca4a-106">Das Cmdlet " **Import-AzurePublishSettingsFile** " importiert eine Datei für Veröffentlichungseinstellungen (\*. publishsettings), die Informationen zu ihren Azure-Konten enthält, und speichert eine Abonnement Datendatei auf Ihrem Computer.</span><span class="sxs-lookup"><span data-stu-id="aca4a-106">The **Import-AzurePublishSettingsFile** cmdlet imports a publish settings file (\*.publishsettings) that contains information about your Azure accounts and saves a subscription data file on your computer.</span></span>
<span data-ttu-id="aca4a-107">Nach Abschluss des Cmdlets können Sie Ihre Azure-Konten in Windows PowerShell verwalten.</span><span class="sxs-lookup"><span data-stu-id="aca4a-107">When the cmdlet completes, you can manage your Azure accounts in Windows PowerShell.</span></span>

<span data-ttu-id="aca4a-108">Führen Sie vor dem Ausführen von **Import-AzurePublishSettingsFile** den Eintrag **Get-AzurePublishSettingsFile** aus, der die Datei für die Veröffentlichungseinstellungen downloadet und speichert, sodass Sie Sie importieren können.</span><span class="sxs-lookup"><span data-stu-id="aca4a-108">Before running **Import-AzurePublishSettingsFile** , run **Get-AzurePublishSettingsFile** , which downloads and saves the publish settings file so you can import it.</span></span>

<span data-ttu-id="aca4a-109">Wenn Sie Ihr Azure-Konto für Windows PowerShell verfügbar machen möchten, können Sie eine Datei für Veröffentlichungseinstellungen oder das Cmdlet **Add-AzureAccount** verwenden.</span><span class="sxs-lookup"><span data-stu-id="aca4a-109">To make your Azure account available to Windows PowerShell, you can use a publish settings file or the **Add-AzureAccount** cmdlet.</span></span>
<span data-ttu-id="aca4a-110">Mit den Einstellungen für "Veröffentlichungseinstellungen" können Sie die Sitzung im Voraus vorbereiten, damit Skripts und Hintergrundaufträge unbeaufsichtigt ausgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="aca4a-110">Publish settings files let you prepare the session in advance so you can run scripts and background jobs unattended.</span></span>
<span data-ttu-id="aca4a-111">Allerdings unterstützen nicht alle Dienste Veröffentlichungs Einstellungsdateien.</span><span class="sxs-lookup"><span data-stu-id="aca4a-111">However, not all services support publish settings files.</span></span>
<span data-ttu-id="aca4a-112">Beispielsweise unterstützt das **AzureResourceManager** -Modul keine Veröffentlichungs Einstellungsdateien.</span><span class="sxs-lookup"><span data-stu-id="aca4a-112">For example, the **AzureResourceManager** module does not support publish settings files.</span></span>

<span data-ttu-id="aca4a-113">**Sicherheitshinweis:** Dateien für Veröffentlichungseinstellungen enthalten ein Verwaltungszertifikat, das verschlüsselt, aber nicht verschlüsselt ist.</span><span class="sxs-lookup"><span data-stu-id="aca4a-113">**Security Note:** Publish settings files contain a management certificate that is encoded, but not encrypted.</span></span>
<span data-ttu-id="aca4a-114">Wenn böswillige Benutzer auf Ihre Veröffentlichungs Einstellungsdatei zugreifen, können Sie Ihre Azure-Dienste möglicherweise bearbeiten, erstellen und löschen.</span><span class="sxs-lookup"><span data-stu-id="aca4a-114">If  malicious users access your publish settings file,  they might be able to edit, create, and delete your Azure services.</span></span>
<span data-ttu-id="aca4a-115">Aus Sicherheitsgründen empfiehlt es sich, die Datei an einem Speicherort im Ordner "Downloads" oder "Dokumente" zu speichern und diese dann nach Verwendung des Cmdlets " **Import-AzurePublishSettingsFile** " zu löschen, um die Einstellungen zu importieren.</span><span class="sxs-lookup"><span data-stu-id="aca4a-115">As a security best practice, save the file to a location in your Downloads or Documents folder and then delete it after using **Import-AzurePublishSettingsFile** cmdlet to import the settings.</span></span>

## <span data-ttu-id="aca4a-116">Beispiele</span><span class="sxs-lookup"><span data-stu-id="aca4a-116">EXAMPLES</span></span>

### <span data-ttu-id="aca4a-117">Beispiel 1: Importieren einer Datei</span><span class="sxs-lookup"><span data-stu-id="aca4a-117">Example 1: Import a file</span></span>
```
PS C:\> Import-AzurePublishSettingsFile -PublishSettingsFile C:\Temp\MyAccount.publishsettings
```

<span data-ttu-id="aca4a-118">Dieser Befehl importiert die "C:\Temp\MyAccount.publishsettings"-Datei.</span><span class="sxs-lookup"><span data-stu-id="aca4a-118">This command imports the "C:\Temp\MyAccount.publishsettings" file.</span></span>

## <span data-ttu-id="aca4a-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="aca4a-119">PARAMETERS</span></span>

### <span data-ttu-id="aca4a-120">-Umgebung</span><span class="sxs-lookup"><span data-stu-id="aca4a-120">-Environment</span></span>
<span data-ttu-id="aca4a-121">Gibt eine Azure-Umgebung an.</span><span class="sxs-lookup"><span data-stu-id="aca4a-121">Specifies an Azure environment.</span></span>

<span data-ttu-id="aca4a-122">Eine Azure-Umgebung eine unabhängige Bereitstellung von Microsoft Azure, wie AzureCloud für Global Azure und AzureChinaCloud für Azure, betrieben von 21Vianet in China.</span><span class="sxs-lookup"><span data-stu-id="aca4a-122">An Azure environment an independent deployment of Microsoft Azure, such as AzureCloud for global Azure and AzureChinaCloud for Azure operated by 21Vianet in China.</span></span>
<span data-ttu-id="aca4a-123">Sie können auch lokale Azure-Umgebungen mithilfe von Azure Pack und den WAPack-Cmdlets erstellen.</span><span class="sxs-lookup"><span data-stu-id="aca4a-123">You can also create on-premises Azure environments by using Azure Pack and the WAPack cmdlets.</span></span>
<span data-ttu-id="aca4a-124">Weitere Informationen finden Sie unter [Azure Pack](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx)  ( https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) .</span><span class="sxs-lookup"><span data-stu-id="aca4a-124">For more information, see [Azure Pack](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx)  (https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx).</span></span>

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

### <span data-ttu-id="aca4a-125">-Profil</span><span class="sxs-lookup"><span data-stu-id="aca4a-125">-Profile</span></span>
<span data-ttu-id="aca4a-126">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="aca4a-126">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="aca4a-127">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="aca4a-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="aca4a-128">-PublishSettingsFile</span><span class="sxs-lookup"><span data-stu-id="aca4a-128">-PublishSettingsFile</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aca4a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aca4a-129">CommonParameters</span></span>
<span data-ttu-id="aca4a-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aca4a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aca4a-131">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aca4a-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aca4a-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="aca4a-132">INPUTS</span></span>

### <span data-ttu-id="aca4a-133">Keine</span><span class="sxs-lookup"><span data-stu-id="aca4a-133">None</span></span>
<span data-ttu-id="aca4a-134">Sie können die Eingabe an dieses Cmdlet nach Eigenschaftsname, aber nicht nach Wert übergeben.</span><span class="sxs-lookup"><span data-stu-id="aca4a-134">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="aca4a-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="aca4a-135">OUTPUTS</span></span>

### <span data-ttu-id="aca4a-136">Keine</span><span class="sxs-lookup"><span data-stu-id="aca4a-136">None</span></span>
<span data-ttu-id="aca4a-137">Dieses Cmdlet generiert keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="aca4a-137">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="aca4a-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="aca4a-138">NOTES</span></span>
* <span data-ttu-id="aca4a-139">Eine "Veröffentlichungs Einstellungsdatei" ist eine XML-Datei mit der Dateinamenerweiterung publishsettings.</span><span class="sxs-lookup"><span data-stu-id="aca4a-139">A "publish settings file" is an XML file with a .publishsettings file name extension.</span></span> <span data-ttu-id="aca4a-140">Die Datei enthält ein codiertes Zertifikat, das Verwaltungsanmeldeinformationen für Ihre Azure-Abonnements bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="aca4a-140">The file contains an encoded certificate that provides management credentials for your Azure subscriptions.</span></span> <span data-ttu-id="aca4a-141">Nachdem Sie diese Datei importiert haben, löschen Sie Sie, um Sicherheitsrisiken zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="aca4a-141">After you import this file, delete it to avoid security risks.</span></span>
* <span data-ttu-id="aca4a-142">Eine "Abonnement Datendatei" ist eine XML-Datei, die auf Ihrem Computer sicher gespeichert werden kann.</span><span class="sxs-lookup"><span data-stu-id="aca4a-142">A "subscription data file" is an XML file that can be saved on your computer safely.</span></span> <span data-ttu-id="aca4a-143">Standardmäßig wird es in Ihrem Roaming-Benutzerprofil ($Home/AppData/Roaming) gespeichert.</span><span class="sxs-lookup"><span data-stu-id="aca4a-143">By default, it's saved in your roaming user profile ($home/AppData/Roaming).</span></span>

## <span data-ttu-id="aca4a-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="aca4a-144">RELATED LINKS</span></span>

[<span data-ttu-id="aca4a-145">Installieren und Konfigurieren von Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="aca4a-145">How to Install and Configure Azure PowerShell</span></span>](https://azure.microsoft.com/documentation/articles/install-configure-powershell/)

[<span data-ttu-id="aca4a-146">Add-AzureAccount</span><span class="sxs-lookup"><span data-stu-id="aca4a-146">Add-AzureAccount</span></span>](./Add-AzureAccount.md)

[<span data-ttu-id="aca4a-147">Get-AzurePublishSettingsFile</span><span class="sxs-lookup"><span data-stu-id="aca4a-147">Get-AzurePublishSettingsFile</span></span>](./Get-AzurePublishSettingsFile.md)


