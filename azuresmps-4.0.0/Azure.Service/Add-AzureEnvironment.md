---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: 6C435518-06EA-41B7-9585-44107B026FF1
online version: ''
schema: 2.0.0
ms.openlocfilehash: b04ceff5c4c49fe0e03e1e2c3da94c118323d653
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005936"
---
# <span data-ttu-id="0d2fa-101">Add-AzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="0d2fa-101">Add-AzureEnvironment</span></span>

## <span data-ttu-id="0d2fa-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0d2fa-102">SYNOPSIS</span></span>
<span data-ttu-id="0d2fa-103">Erstellt eine Azure-Umgebung.</span><span class="sxs-lookup"><span data-stu-id="0d2fa-103">Creates an Azure environment.</span></span>

## <span data-ttu-id="0d2fa-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0d2fa-104">SYNTAX</span></span>

```
Add-AzureEnvironment -Name <String> [-PublishSettingsFileUrl <String>] [-ServiceEndpoint <String>]
 [-ManagementPortalUrl <String>] [-StorageEndpoint <String>] [-ActiveDirectoryEndpoint <String>]
 [-ResourceManagerEndpoint <String>] [-GalleryEndpoint <String>]
 [-ActiveDirectoryServiceEndpointResourceId <String>] [-GraphEndpoint <String>]
 [-AzureKeyVaultDnsSuffix <String>] [-AzureKeyVaultServiceEndpointResourceId <String>]
 [-TrafficManagerDnsSuffix <String>] [-SqlDatabaseDnsSuffix <String>] [-EnableAdfsAuthentication]
 [-AdTenant <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="0d2fa-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0d2fa-105">DESCRIPTION</span></span>
<span data-ttu-id="0d2fa-106">Das Cmdlet **Add-AzureEnvironment** erstellt eine neue benutzerdefinierte Azure-Konto Umgebung und speichert Sie in Ihrem Roaming-Benutzerprofil.</span><span class="sxs-lookup"><span data-stu-id="0d2fa-106">The **Add-AzureEnvironment** cmdlet creates a new custom Azure account environment and saves it in your roaming user profile.</span></span>
<span data-ttu-id="0d2fa-107">Das Cmdlet gibt ein Objekt zurück, das die neue Umgebung darstellt.</span><span class="sxs-lookup"><span data-stu-id="0d2fa-107">The cmdlet returns an object that represents the new environment.</span></span>
<span data-ttu-id="0d2fa-108">Nach Abschluss des Befehls können Sie die Umgebung in Windows PowerShell verwenden.</span><span class="sxs-lookup"><span data-stu-id="0d2fa-108">When the command completes, you can use the environment in Windows PowerShell.</span></span>

<span data-ttu-id="0d2fa-109">Eine Azure-Umgebung eine unabhängige Bereitstellung von Microsoft Azure, wie AzureCloud für Global Azure und AzureChinaCloud für Azure, betrieben von 21Vianet in China.</span><span class="sxs-lookup"><span data-stu-id="0d2fa-109">An Azure environment an independent deployment of Microsoft Azure, such as AzureCloud for global Azure and AzureChinaCloud for Azure operated by 21Vianet in China.</span></span>
<span data-ttu-id="0d2fa-110">Sie können auch lokale Azure-Umgebungen mithilfe von Azure Pack und den WAPack-Cmdlets erstellen.</span><span class="sxs-lookup"><span data-stu-id="0d2fa-110">You can also create on-premises Azure environments by using Azure Pack and the WAPack cmdlets.</span></span>
<span data-ttu-id="0d2fa-111">Weitere Informationen finden Sie unter [Azure Pack](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) ( https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) .</span><span class="sxs-lookup"><span data-stu-id="0d2fa-111">For more information, see [Azure Pack](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) (https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx).</span></span>

<span data-ttu-id="0d2fa-112">Nur der **Name** -Parameter dieses Cmdlets ist obligatorisch.</span><span class="sxs-lookup"><span data-stu-id="0d2fa-112">Only the **Name** parameter of this cmdlet is mandatory.</span></span>
<span data-ttu-id="0d2fa-113">Wenn Sie einen Parameter nicht angeben, ist sein Wert NULL ($null), und der Dienst, der diesen Endpunkt verwendet, funktioniert möglicherweise nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="0d2fa-113">If you omit a parameter, its value is null ($Null), and the service that uses that endpoint might not function properly.</span></span>
<span data-ttu-id="0d2fa-114">Wenn Sie den Wert einer Umgebungseigenschaft hinzufügen oder ändern möchten, verwenden Sie das Cmdlet " **Satz-AzureEnvironment** ".</span><span class="sxs-lookup"><span data-stu-id="0d2fa-114">To add or change the value of an environment property, use the **Set-AzureEnvironment** cmdlet.</span></span>

<span data-ttu-id="0d2fa-115">Hinweis: das Ändern Ihrer Umgebung kann dazu führen, dass Ihr Konto fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="0d2fa-115">NOTE: Changing your environment can cause your account to fail.</span></span>
<span data-ttu-id="0d2fa-116">In der Regel werden Umgebungen nur zum Testen oder zur Problembehandlung hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="0d2fa-116">Typically, environments are added only for testing or troubleshooting.</span></span>

<span data-ttu-id="0d2fa-117">In diesem Thema wird das Cmdlet in der 0.8.10-Version des Microsoft Azure PowerShell-Moduls beschrieben.</span><span class="sxs-lookup"><span data-stu-id="0d2fa-117">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="0d2fa-118">Wenn Sie die Version des verwendeten Moduls abrufen möchten, geben Sie in der Azure PowerShell-Konsole `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="0d2fa-118">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

## <span data-ttu-id="0d2fa-119">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0d2fa-119">EXAMPLES</span></span>

### <span data-ttu-id="0d2fa-120">Beispiel 1: Hinzufügen einer Azure-Umgebung</span><span class="sxs-lookup"><span data-stu-id="0d2fa-120">Example 1: Add an Azure environment</span></span>
```
PS C:\> Add-AzureEnvironment -Name ContosoEnv -PublishSettingsFileUrl https://contoso.com/fwlink/?LinkID=101 -ServiceEndpoint https://contoso.com/fwlink/?LinkID=102

Name                          : ContosoEnv

PublishSettingsFileUrl        : https://contoso.com/fwlink/?LinkID=101

ServiceEndpoint               : https://contoso.com/fwlink/?LinkID=102

ResourceManagerEndpoint       : 

ManagementPortalUrl           : 

ActiveDirectoryEndpoint       : 

ActiveDirectoryCommonTenantId : 

StorageEndpointSuffix         : 

StorageBlobEndpointFormat     : 

StorageQueueEndpointFormat    : 

StorageTableEndpointFormat    : 

GalleryEndpoint               :
```

<span data-ttu-id="0d2fa-121">Mit diesem Befehl wird die ContosoEnv Azure-Umgebung erstellt.</span><span class="sxs-lookup"><span data-stu-id="0d2fa-121">This command creates the ContosoEnv Azure environment.</span></span>

## <span data-ttu-id="0d2fa-122">Parameter</span><span class="sxs-lookup"><span data-stu-id="0d2fa-122">PARAMETERS</span></span>

### <span data-ttu-id="0d2fa-123">-ActiveDirectoryEndpoint</span><span class="sxs-lookup"><span data-stu-id="0d2fa-123">-ActiveDirectoryEndpoint</span></span>
<span data-ttu-id="0d2fa-124">Gibt den Endpunkt für die Azure Active Directory-Authentifizierung in der neuen Umgebung an.</span><span class="sxs-lookup"><span data-stu-id="0d2fa-124">Specifies the endpoint for Azure Active Directory authentication in the new environment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AdEndpointUrl, ActiveDirectory, ActiveDirectoryAuthority

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d2fa-125">-ActiveDirectoryServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="0d2fa-125">-ActiveDirectoryServiceEndpointResourceId</span></span>
<span data-ttu-id="0d2fa-126">Gibt die Ressourcen-ID einer Verwaltungs-API an, deren Zugriff von Azure Active Directory verwaltet wird.</span><span class="sxs-lookup"><span data-stu-id="0d2fa-126">Specifies the resource ID of a management API whose access is managed by Azure Active Directory.</span></span>

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

### <span data-ttu-id="0d2fa-127">-Mandant</span><span class="sxs-lookup"><span data-stu-id="0d2fa-127">-AdTenant</span></span>
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

### <span data-ttu-id="0d2fa-128">-AzureKeyVaultDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="0d2fa-128">-AzureKeyVaultDnsSuffix</span></span>
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

### <span data-ttu-id="0d2fa-129">-AzureKeyVaultServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="0d2fa-129">-AzureKeyVaultServiceEndpointResourceId</span></span>
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

### <span data-ttu-id="0d2fa-130">-EnableAdfsAuthentication</span><span class="sxs-lookup"><span data-stu-id="0d2fa-130">-EnableAdfsAuthentication</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: OnPremise

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d2fa-131">-GalleryEndpoint</span><span class="sxs-lookup"><span data-stu-id="0d2fa-131">-GalleryEndpoint</span></span>
<span data-ttu-id="0d2fa-132">Gibt den Endpunkt für den Azure Resource Manager-Katalog an, in dem Ressourcengruppen-Katalogvorlagen gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="0d2fa-132">Specifies the endpoint for the Azure Resource Manager gallery, which stores resource group gallery templates.</span></span>
<span data-ttu-id="0d2fa-133">Weitere Informationen zu Azure-Ressourcengruppen und Katalogvorlagen finden Sie im Hilfethema zu Get-AzureResourceGroupGalleryTemplate https://go.microsoft.com/fwlink/?LinkID=393052 .</span><span class="sxs-lookup"><span data-stu-id="0d2fa-133">For more information about Azure resource groups and gallery templates, see the help topic for Get-AzureResourceGroupGalleryTemplatehttps://go.microsoft.com/fwlink/?LinkID=393052.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Gallery, GalleryUrl

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d2fa-134">-GraphEndpoint</span><span class="sxs-lookup"><span data-stu-id="0d2fa-134">-GraphEndpoint</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: Graph, GraphUrl

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d2fa-135">-ManagementPortalUrl</span><span class="sxs-lookup"><span data-stu-id="0d2fa-135">-ManagementPortalUrl</span></span>
<span data-ttu-id="0d2fa-136">Gibt die URL des Azure-Verwaltungsportals in der neuen Umgebung an.</span><span class="sxs-lookup"><span data-stu-id="0d2fa-136">Specifies the URL of the Azure Management Portal in the new environment.</span></span>

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

### <span data-ttu-id="0d2fa-137">-Name</span><span class="sxs-lookup"><span data-stu-id="0d2fa-137">-Name</span></span>
<span data-ttu-id="0d2fa-138">Gibt einen Namen für die Umgebung an.</span><span class="sxs-lookup"><span data-stu-id="0d2fa-138">Specifies a name for the environment.</span></span>
<span data-ttu-id="0d2fa-139">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="0d2fa-139">This parameter is required.</span></span>
<span data-ttu-id="0d2fa-140">Verwenden Sie nicht die Namen der Standardumgebungen AzureCloud und AzureChinaCloud.</span><span class="sxs-lookup"><span data-stu-id="0d2fa-140">Do not use the names of the default environments, AzureCloud and AzureChinaCloud.</span></span>

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

### <span data-ttu-id="0d2fa-141">-Profil</span><span class="sxs-lookup"><span data-stu-id="0d2fa-141">-Profile</span></span>
<span data-ttu-id="0d2fa-142">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="0d2fa-142">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="0d2fa-143">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="0d2fa-143">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="0d2fa-144">-PublishSettingsFileUrl</span><span class="sxs-lookup"><span data-stu-id="0d2fa-144">-PublishSettingsFileUrl</span></span>
<span data-ttu-id="0d2fa-145">Gibt die URL der Datei für die Veröffentlichungseinstellungen für Ihr Konto an.</span><span class="sxs-lookup"><span data-stu-id="0d2fa-145">Specifies the URL of the publish settings files for your account.</span></span>
<span data-ttu-id="0d2fa-146">Eine Azure Publish Settings-Datei ist eine XML-Datei, die Informationen zu Ihrem Konto und ein Verwaltungszertifikat enthält, mit dem Windows PowerShell sich in Ihrem Namen bei Ihrem Azure-Konto anmelden kann.</span><span class="sxs-lookup"><span data-stu-id="0d2fa-146">An Azure publish settings file is an XML file that contains information about your account and a management certificate that allows Windows PowerShell to sign into your Azure account on your behalf.</span></span>

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

### <span data-ttu-id="0d2fa-147">-ResourceManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="0d2fa-147">-ResourceManagerEndpoint</span></span>
<span data-ttu-id="0d2fa-148">Gibt den Endpunkt für Azure Resource Manager-Daten an, einschließlich Daten zu Ressourcengruppen, die dem Konto zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="0d2fa-148">Specifies the endpoint for Azure Resource Manager data, including data about resource groups associated with the account.</span></span>
<span data-ttu-id="0d2fa-149">Weitere Informationen zum Azure Resource Manager finden Sie unter [Azure Resource Manager-Cmdlets](https://go.microsoft.com/fwlink/?LinkID=394765)  ( https://go.microsoft.com/fwlink/?LinkID=394765) und [Verwenden von Windows PowerShell mit Ressourcen-Manager](https://go.microsoft.com/fwlink/?LinkID=394767)  ( https://go.microsoft.com/fwlink/?LinkID=394767) .</span><span class="sxs-lookup"><span data-stu-id="0d2fa-149">For more information about Azure Resource Manager, see [Azure Resource Manager Cmdlets](https://go.microsoft.com/fwlink/?LinkID=394765)  (https://go.microsoft.com/fwlink/?LinkID=394765) and [Using Windows PowerShell with Resource Manager](https://go.microsoft.com/fwlink/?LinkID=394767)  (https://go.microsoft.com/fwlink/?LinkID=394767).</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceManager, ResourceManagerUrl

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d2fa-150">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="0d2fa-150">-ServiceEndpoint</span></span>
<span data-ttu-id="0d2fa-151">Gibt die URL des Azure-Dienstendpunkts an.</span><span class="sxs-lookup"><span data-stu-id="0d2fa-151">Specifies the URL of the Azure service endpoint.</span></span>
<span data-ttu-id="0d2fa-152">Der Azure-Dienstendpunkt bestimmt, ob Ihre Anwendung von der globalen Azure-Plattform, Azure, die von 21Vianet in China betrieben wird, oder von einer privaten Azure-Installation verwaltet wird.</span><span class="sxs-lookup"><span data-stu-id="0d2fa-152">The Azure service endpoint determines whether your application is managed by the global Azure platform, Azure operated by 21Vianet in China, or a private Azure installation.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ServiceManagement, ServiceManagementUrl

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d2fa-153">-SqlDatabaseDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="0d2fa-153">-SqlDatabaseDnsSuffix</span></span>
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

### <span data-ttu-id="0d2fa-154">-StorageEndpoint</span><span class="sxs-lookup"><span data-stu-id="0d2fa-154">-StorageEndpoint</span></span>
<span data-ttu-id="0d2fa-155">Gibt den Standardendpunkt von Speicherdiensten in der neuen Umgebung an.</span><span class="sxs-lookup"><span data-stu-id="0d2fa-155">Specifies the default endpoint of storage services in the new environment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: StorageEndpointSuffix

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d2fa-156">-TrafficManagerDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="0d2fa-156">-TrafficManagerDnsSuffix</span></span>
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

### <span data-ttu-id="0d2fa-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d2fa-157">CommonParameters</span></span>
<span data-ttu-id="0d2fa-158">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0d2fa-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d2fa-159">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0d2fa-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d2fa-160">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0d2fa-160">INPUTS</span></span>

### <span data-ttu-id="0d2fa-161">Keine</span><span class="sxs-lookup"><span data-stu-id="0d2fa-161">None</span></span>
<span data-ttu-id="0d2fa-162">Sie können die Eingabe an dieses Cmdlet nach Eigenschaftsname, aber nicht nach Wert übergeben.</span><span class="sxs-lookup"><span data-stu-id="0d2fa-162">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="0d2fa-163">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0d2fa-163">OUTPUTS</span></span>

### <span data-ttu-id="0d2fa-164">Microsoft. WindowsAzure. Commands. Utilities. Common. WindowsAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="0d2fa-164">Microsoft.WindowsAzure.Commands.Utilities.Common.WindowsAzureEnvironment</span></span>

## <span data-ttu-id="0d2fa-165">Notizen</span><span class="sxs-lookup"><span data-stu-id="0d2fa-165">NOTES</span></span>

## <span data-ttu-id="0d2fa-166">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0d2fa-166">RELATED LINKS</span></span>

[<span data-ttu-id="0d2fa-167">Get-AzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="0d2fa-167">Get-AzureEnvironment</span></span>](./Get-AzureEnvironment.md)

[<span data-ttu-id="0d2fa-168">Remove-AzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="0d2fa-168">Remove-AzureEnvironment</span></span>](./Remove-AzureEnvironment.md)

[<span data-ttu-id="0d2fa-169">Satz-AzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="0d2fa-169">Set-AzureEnvironment</span></span>](./Set-AzureEnvironment.md)


