---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: 1094497D-2CBE-41DF-9ED1-8E7D3F14B05A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 82bd806d35f36a07958f2bdeeeda42853cd453b9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006173"
---
# <span data-ttu-id="eafac-101">Set-AzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="eafac-101">Set-AzureEnvironment</span></span>

## <span data-ttu-id="eafac-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="eafac-102">SYNOPSIS</span></span>
<span data-ttu-id="eafac-103">Ändert die Eigenschaften einer Azure-Umgebung.</span><span class="sxs-lookup"><span data-stu-id="eafac-103">Changes the properties of an Azure environment.</span></span>

## <span data-ttu-id="eafac-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="eafac-104">SYNTAX</span></span>

```
Set-AzureEnvironment -Name <String> [-PublishSettingsFileUrl <String>] [-ServiceEndpoint <String>]
 [-ManagementPortalUrl <String>] [-StorageEndpoint <String>] [-ActiveDirectoryEndpoint <String>]
 [-ResourceManagerEndpoint <String>] [-GalleryEndpoint <String>]
 [-ActiveDirectoryServiceEndpointResourceId <String>] [-GraphEndpoint <String>]
 [-AzureKeyVaultDnsSuffix <String>] [-AzureKeyVaultServiceEndpointResourceId <String>]
 [-TrafficManagerDnsSuffix <String>] [-SqlDatabaseDnsSuffix <String>] [-EnableAdfsAuthentication]
 [-AdTenant <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="eafac-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="eafac-105">DESCRIPTION</span></span>
<span data-ttu-id="eafac-106">Das Cmdlet " **Satz-AzureEnvironment** " ändert die Eigenschaften einer Azure-Umgebung.</span><span class="sxs-lookup"><span data-stu-id="eafac-106">The **Set-AzureEnvironment** cmdlet changes the properties of an Azure environment.</span></span>
<span data-ttu-id="eafac-107">Sie gibt ein Objekt zurück, das die Umgebung mit den neuen Eigenschaftswerten darstellt.</span><span class="sxs-lookup"><span data-stu-id="eafac-107">It returns an object that represents the environment with its new property values.</span></span>
<span data-ttu-id="eafac-108">Verwenden Sie den Parameter **Name** , um die Umgebung und die anderen Parameter zum Ändern von Eigenschaftswerten zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="eafac-108">Use the **Name** parameter to identify the environment and the other parameters to change property values.</span></span>
<span data-ttu-id="eafac-109">Sie können " **AzureEnvironment** " nicht verwenden, um den Namen einer Azure-Umgebung zu ändern.</span><span class="sxs-lookup"><span data-stu-id="eafac-109">You cannot use **Set-AzureEnvironment** to change the name of an Azure environment.</span></span>

<span data-ttu-id="eafac-110">Eine Azure-Umgebung eine unabhängige Bereitstellung von Microsoft Azure, wie AzureCloud für Global Azure und AzureChinaCloud für Azure, betrieben von 21Vianet in China.</span><span class="sxs-lookup"><span data-stu-id="eafac-110">An Azure environment an independent deployment of Microsoft Azure, such as AzureCloud for global Azure and AzureChinaCloud for Azure operated by 21Vianet in China.</span></span>
<span data-ttu-id="eafac-111">Sie können auch lokale Azure-Umgebungen mithilfe von Azure Pack und den WAPack-Cmdlets erstellen.</span><span class="sxs-lookup"><span data-stu-id="eafac-111">You can also create on-premises Azure environments by using Azure Pack and the WAPack cmdlets.</span></span>
<span data-ttu-id="eafac-112">Weitere Informationen finden Sie unter [Azure Pack](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) ( https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) .</span><span class="sxs-lookup"><span data-stu-id="eafac-112">For more information, see [Azure Pack](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) (https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx).</span></span>

<span data-ttu-id="eafac-113">Hinweis: Ändern Sie die Eigenschaften der AzureCloud-oder AzureChinaCloud-Umgebungen nicht.</span><span class="sxs-lookup"><span data-stu-id="eafac-113">NOTE:  Do not change the properties of the AzureCloud or AzureChinaCloud environments.</span></span>
<span data-ttu-id="eafac-114">Verwenden Sie dieses Cmdlet, um die Werte privater Umgebungen zu ändern, die Sie erstellen.</span><span class="sxs-lookup"><span data-stu-id="eafac-114">Use this cmdlet to change the values of private environments that you create.</span></span>

## <span data-ttu-id="eafac-115">Beispiele</span><span class="sxs-lookup"><span data-stu-id="eafac-115">EXAMPLES</span></span>

### <span data-ttu-id="eafac-116">Beispiel 1: Ändern von Umgebungseigenschaften</span><span class="sxs-lookup"><span data-stu-id="eafac-116">Example 1: Change environment properties</span></span>
```
PS C:\> Set-AzureEnvironment -Name ContosoEnv -PublishSettingsFileUrl "https://contoso.com" -StorageEndpoint "contoso.com"
```

<span data-ttu-id="eafac-117">Mit diesem Befehl werden die Werte der **PublishSettingsFileUrl** -und **StorageEndpoint** -Eigenschaft der ContosoEnv-Umgebung geändert.</span><span class="sxs-lookup"><span data-stu-id="eafac-117">This command changes the values of the **PublishSettingsFileUrl** and **StorageEndpoint** properties of the ContosoEnv environment.</span></span>

## <span data-ttu-id="eafac-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="eafac-118">PARAMETERS</span></span>

### <span data-ttu-id="eafac-119">-ActiveDirectoryEndpoint</span><span class="sxs-lookup"><span data-stu-id="eafac-119">-ActiveDirectoryEndpoint</span></span>
<span data-ttu-id="eafac-120">Ändert den Endpunkt für die Azure Active Directory-Authentifizierung in den angegebenen Wert.</span><span class="sxs-lookup"><span data-stu-id="eafac-120">Changes the endpoint for Azure Active Directory authentication to the specified value.</span></span>

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

### <span data-ttu-id="eafac-121">-ActiveDirectoryServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="eafac-121">-ActiveDirectoryServiceEndpointResourceId</span></span>
<span data-ttu-id="eafac-122">Gibt die Ressourcen-ID einer Verwaltungs-API an, deren Zugriff von Azure Active Directory verwaltet wird.</span><span class="sxs-lookup"><span data-stu-id="eafac-122">Specifies the resource ID of a management API whose access is managed by Azure Active Directory.</span></span>

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

### <span data-ttu-id="eafac-123">-Mandant</span><span class="sxs-lookup"><span data-stu-id="eafac-123">-AdTenant</span></span>
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

### <span data-ttu-id="eafac-124">-AzureKeyVaultDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="eafac-124">-AzureKeyVaultDnsSuffix</span></span>
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

### <span data-ttu-id="eafac-125">-AzureKeyVaultServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="eafac-125">-AzureKeyVaultServiceEndpointResourceId</span></span>
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

### <span data-ttu-id="eafac-126">-EnableAdfsAuthentication</span><span class="sxs-lookup"><span data-stu-id="eafac-126">-EnableAdfsAuthentication</span></span>
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

### <span data-ttu-id="eafac-127">-GalleryEndpoint</span><span class="sxs-lookup"><span data-stu-id="eafac-127">-GalleryEndpoint</span></span>
<span data-ttu-id="eafac-128">Ändert den Endpunkt für den Azure Resource Manager-Katalog in den angegebenen Wert.</span><span class="sxs-lookup"><span data-stu-id="eafac-128">Changes the endpoint for the Azure Resource Manager gallery to the specified value.</span></span>
<span data-ttu-id="eafac-129">Der Katalog Endpunkt ist der Speicherort für Ressourcengruppen-Katalogvorlagen.</span><span class="sxs-lookup"><span data-stu-id="eafac-129">The gallery endpoint is the location for resource group gallery templates.</span></span>
<span data-ttu-id="eafac-130">Weitere Informationen zu Azure-Ressourcengruppen und Katalogvorlagen finden Sie im Hilfethema zu [Get-AzureResourceGroupGalleryTemplate](https://go.microsoft.com/fwlink/?LinkID=393052).</span><span class="sxs-lookup"><span data-stu-id="eafac-130">For more information about Azure resource groups and gallery templates, see the help topic for [Get-AzureResourceGroupGalleryTemplate](https://go.microsoft.com/fwlink/?LinkID=393052).</span></span>

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

### <span data-ttu-id="eafac-131">-GraphEndpoint</span><span class="sxs-lookup"><span data-stu-id="eafac-131">-GraphEndpoint</span></span>
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

### <span data-ttu-id="eafac-132">-ManagementPortalUrl</span><span class="sxs-lookup"><span data-stu-id="eafac-132">-ManagementPortalUrl</span></span>
<span data-ttu-id="eafac-133">Ändert die URL des Azure-Verwaltungsportals auf den angegebenen Wert.</span><span class="sxs-lookup"><span data-stu-id="eafac-133">Changes the URL of the Azure Management Portal to the specified value.</span></span>

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

### <span data-ttu-id="eafac-134">-Name</span><span class="sxs-lookup"><span data-stu-id="eafac-134">-Name</span></span>
<span data-ttu-id="eafac-135">Identifiziert die Umgebung, die geändert wird.</span><span class="sxs-lookup"><span data-stu-id="eafac-135">Identifies the environment that is being changed.</span></span>
<span data-ttu-id="eafac-136">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="eafac-136">This parameter is required.</span></span>
<span data-ttu-id="eafac-137">Bei dem Parameterwert wird die Groß-/Kleinschreibung beachtet.</span><span class="sxs-lookup"><span data-stu-id="eafac-137">The parameter value is case-sensitive.</span></span>
<span data-ttu-id="eafac-138">Platzhalterzeichen sind nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="eafac-138">Wildcard characters are not permitted.</span></span>

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

### <span data-ttu-id="eafac-139">-Profil</span><span class="sxs-lookup"><span data-stu-id="eafac-139">-Profile</span></span>
<span data-ttu-id="eafac-140">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="eafac-140">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="eafac-141">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="eafac-141">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="eafac-142">-PublishSettingsFileUrl</span><span class="sxs-lookup"><span data-stu-id="eafac-142">-PublishSettingsFileUrl</span></span>
<span data-ttu-id="eafac-143">Ändert die URL für Veröffentlichungs Einstellungsdateien in der angegebenen Umgebung.</span><span class="sxs-lookup"><span data-stu-id="eafac-143">Changes the URL for publish settings files in the specified environment.</span></span>
<span data-ttu-id="eafac-144">Eine Azure Publish Settings-Datei ist eine XML-Datei, die Informationen zu Ihrem Konto und ein Verwaltungszertifikat enthält, mit dem Windows PowerShell sich in Ihrem Namen bei Ihrem Azure-Konto anmelden kann.</span><span class="sxs-lookup"><span data-stu-id="eafac-144">An Azure publish settings file is an XML file that contains information about your account and a management certificate that allows Windows PowerShell to sign into your Azure account on your behalf.</span></span>

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

### <span data-ttu-id="eafac-145">-ResourceManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="eafac-145">-ResourceManagerEndpoint</span></span>
<span data-ttu-id="eafac-146">Ändert den Endpunkt für Azure Resource Manager-Daten, einschließlich Daten zu Ressourcengruppen, die dem Konto zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="eafac-146">Changes the endpoint for Azure Resource Manager data, including data about resource groups associated with the account.</span></span>
<span data-ttu-id="eafac-147">Weitere Informationen zum Azure Resource Manager finden Sie unter [Azure Resource Manager-Cmdlets](https://go.microsoft.com/fwlink/?LinkID=394765)  ( https://go.microsoft.com/fwlink/?LinkID=394765) und [Verwenden von Windows PowerShell mit Ressourcen-Manager](https://go.microsoft.com/fwlink/?LinkID=394767)  ( https://go.microsoft.com/fwlink/?LinkID=394767) .</span><span class="sxs-lookup"><span data-stu-id="eafac-147">For more information about Azure Resource Manager, see [Azure Resource Manager Cmdlets](https://go.microsoft.com/fwlink/?LinkID=394765)  (https://go.microsoft.com/fwlink/?LinkID=394765) and [Using Windows PowerShell with Resource Manager](https://go.microsoft.com/fwlink/?LinkID=394767)  (https://go.microsoft.com/fwlink/?LinkID=394767).</span></span>

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

### <span data-ttu-id="eafac-148">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="eafac-148">-ServiceEndpoint</span></span>
<span data-ttu-id="eafac-149">Ändert die URL des Azure-Dienstendpunkts in der angegebenen Umgebung.</span><span class="sxs-lookup"><span data-stu-id="eafac-149">Changes the URL of the Azure service endpoint in the specified environment.</span></span>
<span data-ttu-id="eafac-150">Der Azure-Dienstendpunkt bestimmt, ob Ihre Anwendung von der globalen Azure-Plattform, Azure, die von 21Vianet in China betrieben wird, oder von einer privaten Azure-Installation verwaltet wird.</span><span class="sxs-lookup"><span data-stu-id="eafac-150">The Azure service endpoint determines whether your application is managed by the global Azure platform, Azure operated by 21Vianet in China, or a private Azure installation.</span></span>

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

### <span data-ttu-id="eafac-151">-SqlDatabaseDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="eafac-151">-SqlDatabaseDnsSuffix</span></span>
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

### <span data-ttu-id="eafac-152">-StorageEndpoint</span><span class="sxs-lookup"><span data-stu-id="eafac-152">-StorageEndpoint</span></span>
<span data-ttu-id="eafac-153">Ändert den Standardendpunkt von Speicherdiensten in der angegebenen Umgebung.</span><span class="sxs-lookup"><span data-stu-id="eafac-153">Changes the default endpoint of storage services in the specified environment.</span></span>

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

### <span data-ttu-id="eafac-154">-TrafficManagerDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="eafac-154">-TrafficManagerDnsSuffix</span></span>
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

### <span data-ttu-id="eafac-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eafac-155">CommonParameters</span></span>
<span data-ttu-id="eafac-156">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eafac-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eafac-157">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eafac-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eafac-158">Eingaben</span><span class="sxs-lookup"><span data-stu-id="eafac-158">INPUTS</span></span>

### <span data-ttu-id="eafac-159">Keine</span><span class="sxs-lookup"><span data-stu-id="eafac-159">None</span></span>
<span data-ttu-id="eafac-160">Sie können die Eingabe an dieses Cmdlet nach Eigenschaftsname, aber nicht nach Wert übergeben.</span><span class="sxs-lookup"><span data-stu-id="eafac-160">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="eafac-161">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="eafac-161">OUTPUTS</span></span>

### <span data-ttu-id="eafac-162">Microsoft. WindowsAzure. Commands. Utilities. Common. WindowsAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="eafac-162">Microsoft.WindowsAzure.Commands.Utilities.Common.WindowsAzureEnvironment</span></span>

## <span data-ttu-id="eafac-163">Notizen</span><span class="sxs-lookup"><span data-stu-id="eafac-163">NOTES</span></span>

## <span data-ttu-id="eafac-164">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="eafac-164">RELATED LINKS</span></span>

[<span data-ttu-id="eafac-165">Add-AzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="eafac-165">Add-AzureEnvironment</span></span>](./Add-AzureEnvironment.md)

[<span data-ttu-id="eafac-166">Get-AzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="eafac-166">Get-AzureEnvironment</span></span>](./Get-AzureEnvironment.md)

[<span data-ttu-id="eafac-167">Remove-AzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="eafac-167">Remove-AzureEnvironment</span></span>](./Remove-AzureEnvironment.md)


