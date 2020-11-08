---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: BF5E3E1A-14B6-4630-8168-628057009D5E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 284d1601746254b2e10fdfe042e5882e94ca1bd9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006558"
---
# <span data-ttu-id="891b9-101">Get-AzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="891b9-101">Get-AzureEnvironment</span></span>

## <span data-ttu-id="891b9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="891b9-102">SYNOPSIS</span></span>
<span data-ttu-id="891b9-103">Ruft Azure-Umgebungen ab</span><span class="sxs-lookup"><span data-stu-id="891b9-103">Gets Azure environments</span></span>

## <span data-ttu-id="891b9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="891b9-104">SYNTAX</span></span>

```
Get-AzureEnvironment [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="891b9-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="891b9-105">DESCRIPTION</span></span>
<span data-ttu-id="891b9-106">Das Cmdlet " **Get-AzureEnvironment** " Ruft die Azure-Umgebungen ab, die für Windows PowerShell verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="891b9-106">The **Get-AzureEnvironment** cmdlet gets the Azure environments that are available to Windows PowerShell.</span></span>

<span data-ttu-id="891b9-107">Eine Azure-Umgebung eine unabhängige Bereitstellung von Microsoft Azure, wie AzureCloud für Global Azure und AzureChinaCloud für Azure, betrieben von 21Vianet in China.</span><span class="sxs-lookup"><span data-stu-id="891b9-107">An Azure environment an independent deployment of Microsoft Azure, such as AzureCloud for global Azure and AzureChinaCloud for Azure operated by 21Vianet in China.</span></span>
<span data-ttu-id="891b9-108">Sie können auch lokale Azure-Umgebungen mithilfe von Azure Pack und den WAPack-Cmdlets erstellen.</span><span class="sxs-lookup"><span data-stu-id="891b9-108">You can also create on-premises Azure environments by using Azure Pack and the WAPack cmdlets.</span></span>
<span data-ttu-id="891b9-109">Weitere Informationen finden Sie unter [Azure Pack](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx)  ( https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) .</span><span class="sxs-lookup"><span data-stu-id="891b9-109">For more information, see [Azure Pack](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx)  (https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx).</span></span>

<span data-ttu-id="891b9-110">Das Cmdlet " **Get-AzureEnvironment** " ruft Umgebungen aus ihrer Abonnement Datendatei ab, nicht aus Azure.</span><span class="sxs-lookup"><span data-stu-id="891b9-110">The **Get-AzureEnvironment** cmdlet gets environments from your subscription data file, not from Azure.</span></span>
<span data-ttu-id="891b9-111">Wenn die Abonnement Datendatei veraltet ist, führen Sie das Cmdlet **Add-AzureAccount** oder **Import-PublishSettingsFile** aus, um die Datei zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="891b9-111">If the subscription data file is outdated, run the **Add-AzureAccount** or **Import-PublishSettingsFile** cmdlet to refresh it.</span></span>

<span data-ttu-id="891b9-112">In diesem Thema wird das Cmdlet in der 0.8.10-Version des Microsoft Azure PowerShell-Moduls beschrieben.</span><span class="sxs-lookup"><span data-stu-id="891b9-112">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="891b9-113">Wenn Sie die Version des verwendeten Moduls abrufen möchten, geben Sie in der Azure PowerShell-Konsole `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="891b9-113">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

## <span data-ttu-id="891b9-114">Beispiele</span><span class="sxs-lookup"><span data-stu-id="891b9-114">EXAMPLES</span></span>

### <span data-ttu-id="891b9-115">Beispiel 1: Abrufen aller Umgebungen</span><span class="sxs-lookup"><span data-stu-id="891b9-115">Example 1: Get all environments</span></span>
```
PS C:\> Get-AzureEnvironment

EnvironmentName               ServiceEndpoint               ResourceManagerEndpoint       PublishSettingsFileUrl
---------------               ---------------               -----------------------       ----------------------

AzureCloud                    https://management.core.wi... https://management.azure.com/ https://go.microsoft.com/fw... 
AzureChinaCloud               https://management.core.ch... https://not-supported-serv... https://go.microsoft.com/fw...
```

<span data-ttu-id="891b9-116">Dieser Befehl ruft alle Umgebungen ab, die für Windows PowerShell verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="891b9-116">This command gets all environments that are available to Windows PowerShell.</span></span>

### <span data-ttu-id="891b9-117">Beispiel 2: Abrufen einer Umgebung anhand des Namens</span><span class="sxs-lookup"><span data-stu-id="891b9-117">Example 2: Get an environment by name</span></span>
```
PS C:\> Get-AzureEnvironment -Name AzureCloud

Name                          : AzureCloud

PublishSettingsFileUrl        : https://go.microsoft.com/fwlink/?LinkID=301775

ServiceEndpoint               : https://management.core.windows.net/

ResourceManagerEndpoint       : https://management.azure.com/

ManagementPortalUrl           : https://go.microsoft.com/fwlink/?LinkId=254433

ActiveDirectoryEndpoint       : https://login.windows.net/

ActiveDirectoryCommonTenantId : common

StorageEndpointSuffix         : core.windows.net

StorageBlobEndpointFormat     : {0}://{1}.blob.core.windows.net/

StorageQueueEndpointFormat    : {0}://{1}.queue.core.windows.net/

StorageTableEndpointFormat    : {0}://{1}.table.core.windows.net/

GalleryEndpoint               : https://gallery.azure.com/
```

<span data-ttu-id="891b9-118">In diesem Beispiel wird die AzureCloud-Umgebung abgerufen.</span><span class="sxs-lookup"><span data-stu-id="891b9-118">This example gets the AzureCloud environment.</span></span>

### <span data-ttu-id="891b9-119">Beispiel 3: Abrufen aller Eigenschaften aller Umgebungen</span><span class="sxs-lookup"><span data-stu-id="891b9-119">Example 3: Get all properties of all environments</span></span>
```
PS C:\> Get-AzureEnvironment | ForEach-Object {Get-AzureEnvironment -Name $_.EnvironmentName}
```

<span data-ttu-id="891b9-120">Dieser Befehl ruft alle Eigenschaften aller Umgebungen ab.</span><span class="sxs-lookup"><span data-stu-id="891b9-120">This command gets all properties of all environments.</span></span>

<span data-ttu-id="891b9-121">Der Befehl verwendet das Cmdlet " **Get-AzureEnvironment** ", um alle Azure-Umgebungen für dieses Konto abzurufen.</span><span class="sxs-lookup"><span data-stu-id="891b9-121">The command uses the **Get-AzureEnvironment** cmdlet to get all Azure environments for this account.</span></span>
<span data-ttu-id="891b9-122">Anschließend wird mit dem Cmdlet " **ForEach-Object** " ein Befehl " **Get-AzureEnvironment** " mit dem **Name** -Parameter für jede Umgebung ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="891b9-122">Then, it uses the **Foreach-Object** cmdlet to run a **Get-AzureEnvironment** command with the **Name** parameter on each environment.</span></span>
<span data-ttu-id="891b9-123">Der Wert des **Name** -Parameters ist die **environmentname** -Eigenschaft jeder Umgebung.</span><span class="sxs-lookup"><span data-stu-id="891b9-123">The value of the **Name** parameter is the **EnvironmentName** property of each environment.</span></span>

<span data-ttu-id="891b9-124">Ohne Parameter ruft **Get-AzureEnvironment** nur ausgewählte Eigenschaften einer Umgebung ab.</span><span class="sxs-lookup"><span data-stu-id="891b9-124">Without parameters, **Get-AzureEnvironment** gets only selected properties of an environment.</span></span>

## <span data-ttu-id="891b9-125">Parameter</span><span class="sxs-lookup"><span data-stu-id="891b9-125">PARAMETERS</span></span>

### <span data-ttu-id="891b9-126">-Name</span><span class="sxs-lookup"><span data-stu-id="891b9-126">-Name</span></span>
<span data-ttu-id="891b9-127">Ruft nur die angegebene Umgebung ab.</span><span class="sxs-lookup"><span data-stu-id="891b9-127">Gets only the specified environment.</span></span>
<span data-ttu-id="891b9-128">Geben Sie den Namen der Umgebung ein.</span><span class="sxs-lookup"><span data-stu-id="891b9-128">Type the environment name.</span></span>
<span data-ttu-id="891b9-129">Bei dem Parameterwert wird die Groß-/Kleinschreibung beachtet.</span><span class="sxs-lookup"><span data-stu-id="891b9-129">The parameter value is case-sensitive.</span></span>
<span data-ttu-id="891b9-130">Platzhalterzeichen sind nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="891b9-130">Wildcard characters are not permitted.</span></span>

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

### <span data-ttu-id="891b9-131">-Profil</span><span class="sxs-lookup"><span data-stu-id="891b9-131">-Profile</span></span>
<span data-ttu-id="891b9-132">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="891b9-132">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="891b9-133">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="891b9-133">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="891b9-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="891b9-134">CommonParameters</span></span>
<span data-ttu-id="891b9-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="891b9-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="891b9-136">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="891b9-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="891b9-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="891b9-137">INPUTS</span></span>

### <span data-ttu-id="891b9-138">Keine</span><span class="sxs-lookup"><span data-stu-id="891b9-138">None</span></span>
<span data-ttu-id="891b9-139">Sie können die Eingabe an dieses Cmdlet nach Eigenschaftsname, aber nicht nach Wert übergeben.</span><span class="sxs-lookup"><span data-stu-id="891b9-139">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="891b9-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="891b9-140">OUTPUTS</span></span>

### <span data-ttu-id="891b9-141">System. Management. Automation. PSCustomObject</span><span class="sxs-lookup"><span data-stu-id="891b9-141">System.Management.Automation.PSCustomObject</span></span>
<span data-ttu-id="891b9-142">Standardmäßig gibt **Get-AzureEnvironment** ein benutzerdefiniertes Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="891b9-142">By default, **Get-AzureEnvironment** returns a custom object.</span></span>

### <span data-ttu-id="891b9-143">Microsoft. WindowsAzure. Commands. Utilities. Common. WindowsAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="891b9-143">Microsoft.WindowsAzure.Commands.Utilities.Common.WindowsAzureEnvironment</span></span>
<span data-ttu-id="891b9-144">Wenn Sie **Get-AzureEnvironment** mit dem Parameter **Name** ausführen, wird ein  **WindowsAzureEnvironment** -Objekt zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="891b9-144">When you run **Get-AzureEnvironment** with the **Name** parameter, it returns a  **WindowsAzureEnvironment** object.</span></span>

## <span data-ttu-id="891b9-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="891b9-145">NOTES</span></span>

## <span data-ttu-id="891b9-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="891b9-146">RELATED LINKS</span></span>

[<span data-ttu-id="891b9-147">Add-AzureAccount</span><span class="sxs-lookup"><span data-stu-id="891b9-147">Add-AzureAccount</span></span>](./Add-AzureAccount.md)

[<span data-ttu-id="891b9-148">Add-AzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="891b9-148">Add-AzureEnvironment</span></span>](./Add-AzureEnvironment.md)

[<span data-ttu-id="891b9-149">Get-AzurePublishSettingsFile</span><span class="sxs-lookup"><span data-stu-id="891b9-149">Get-AzurePublishSettingsFile</span></span>](./Get-AzurePublishSettingsFile.md)

[<span data-ttu-id="891b9-150">Importieren-AzurePublishSettingsFile</span><span class="sxs-lookup"><span data-stu-id="891b9-150">Import-AzurePublishSettingsFile</span></span>](./Import-AzurePublishSettingsFile.md)

[<span data-ttu-id="891b9-151">Remove-AzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="891b9-151">Remove-AzureEnvironment</span></span>](./Remove-AzureEnvironment.md)

[<span data-ttu-id="891b9-152">Satz-AzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="891b9-152">Set-AzureEnvironment</span></span>](./Set-AzureEnvironment.md)


