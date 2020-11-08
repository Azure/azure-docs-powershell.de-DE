---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 9D821623-DEF9-49E4-9C44-10643A92A2E7
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7f6690aa45125a0d1b3383b08443234f47a1f7e3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005639"
---
# <span data-ttu-id="a8e4b-101">Set-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="a8e4b-101">Set-AzureWebsite</span></span>

## <span data-ttu-id="a8e4b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a8e4b-102">SYNOPSIS</span></span>
<span data-ttu-id="a8e4b-103">Konfiguriert eine Website, die in Azure ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a8e4b-103">Configures a website running in Azure.</span></span>

## <span data-ttu-id="a8e4b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a8e4b-104">SYNTAX</span></span>

```
Set-AzureWebsite [-NumberOfWorkers <Int32>] [-DefaultDocuments <String[]>] [-NetFrameworkVersion <String>]
 [-PhpVersion <String>] [-RequestTracingEnabled <Boolean>] [-HttpLoggingEnabled <Boolean>]
 [-DetailedErrorLoggingEnabled <Boolean>] [-HostNames <String[]>] [-AppSettings <Hashtable>]
 [-Metadata <System.Collections.Generic.List`1[Microsoft.WindowsAzure.Commands.Utilities.Websites.Services.WebEntities.NameValuePair]>]
 [-ConnectionStrings <ConnStringPropertyBag>] [-HandlerMappings <HandlerMapping[]>]
 [-SiteWithConfig <SiteWithConfig>] [-PassThru] [-ManagedPipelineMode <ManagedPipelineMode>]
 [-WebSocketsEnabled <Boolean>]
 [-RoutingRules <System.Collections.Generic.List`1[Microsoft.WindowsAzure.Commands.Utilities.Websites.Services.WebEntities.RoutingRule]>]
 [-Use32BitWorkerProcess <Boolean>] [-AutoSwapSlotName <String>]
 [-SlotStickyAppSettingNames <System.Collections.Generic.List`1[System.String]>]
 [-SlotStickyConnectionStringNames <System.Collections.Generic.List`1[System.String]>] [-Name <String>]
 [-Slot <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="a8e4b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a8e4b-105">DESCRIPTION</span></span>
<span data-ttu-id="a8e4b-106">In diesem Thema wird das Cmdlet in der 0.8.10-Version des Microsoft Azure PowerShell-Moduls beschrieben.</span><span class="sxs-lookup"><span data-stu-id="a8e4b-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="a8e4b-107">Wenn Sie die Version des verwendeten Moduls abrufen möchten, geben Sie in der Azure PowerShell-Konsole `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="a8e4b-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="a8e4b-108">Das Cmdlet " **Satz-AzureWebsite** " konfiguriert eine Website, die in Azure ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a8e4b-108">The **Set-AzureWebsite** cmdlet configures a website running in Azure.</span></span>

## <span data-ttu-id="a8e4b-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a8e4b-109">EXAMPLES</span></span>

### <span data-ttu-id="a8e4b-110">Beispiel 1: Aktivieren der HTTP-Protokollierung für eine Website</span><span class="sxs-lookup"><span data-stu-id="a8e4b-110">Example 1: Enable HTTP logging for a website</span></span>
```
PS C:\> Set-AzureWebsite -HttpLoggingEnabled 1
```

<span data-ttu-id="a8e4b-111">In diesem Beispiel wird die HTTP-Protokollierung aktiviert.</span><span class="sxs-lookup"><span data-stu-id="a8e4b-111">This example enables HTTP logging.</span></span>

### <span data-ttu-id="a8e4b-112">Beispiel 2: Einrichten von Speicher Anmeldeinformationen für eine Website</span><span class="sxs-lookup"><span data-stu-id="a8e4b-112">Example 2: Set storage credentials for a website</span></span>
```
PS C:\> $settings = New-Object Hashtable$settings["AZURE_STORAGE_ACCOUNT"= myaccountname$settings["AZURE_STORAGE_ACCESS_KEY"] = myaccesskeySet-AzureWebsite -AppSettings $settings myWebsite
```

<span data-ttu-id="a8e4b-113">In diesem Beispiel werden Speicher Anmeldeinformationen auf einer Website mit dem Namen mywebsite mit Umgebungsvariablen für AZURE_STORAGE_ACCOUNT und AZURE_STORAGE_ACCESS_KEY festgelegt.</span><span class="sxs-lookup"><span data-stu-id="a8e4b-113">This example sets storage credentials in a website named myWebsite with environment variables for AZURE_STORAGE_ACCOUNT and AZURE_STORAGE_ACCESS_KEY.</span></span>

## <span data-ttu-id="a8e4b-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="a8e4b-114">PARAMETERS</span></span>

### <span data-ttu-id="a8e4b-115">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="a8e4b-115">-AppSettings</span></span>
<span data-ttu-id="a8e4b-116">Gibt die Umgebungsvariablen an, die von der Website verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a8e4b-116">Specifies the environment variables that will be used by the website.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8e4b-117">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="a8e4b-117">-AutoSwapSlotName</span></span>
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

### <span data-ttu-id="a8e4b-118">-ConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="a8e4b-118">-ConnectionStrings</span></span>
<span data-ttu-id="a8e4b-119">Gibt die Verbindungszeichenfolgen an, die von der Website verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a8e4b-119">Specifies the connection strings used by the website.</span></span>

```yaml
Type: ConnStringPropertyBag
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8e4b-120">-DefaultDocuments</span><span class="sxs-lookup"><span data-stu-id="a8e4b-120">-DefaultDocuments</span></span>
<span data-ttu-id="a8e4b-121">Gibt die Dokumente an, die beim Durchsuchen der Website automatisch angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="a8e4b-121">Specifies the documents that are automatically displayed when browsing the website.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8e4b-122">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="a8e4b-122">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="a8e4b-123">Bestimmt, ob detaillierte IIS-Fehler für die Website protokolliert werden.</span><span class="sxs-lookup"><span data-stu-id="a8e4b-123">Determines whether detailed IIS errors are logged for the website.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8e4b-124">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="a8e4b-124">-HandlerMappings</span></span>
<span data-ttu-id="a8e4b-125">Gibt die Handler-Zuordnungen an, die von der Website verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a8e4b-125">Specifies the handler mappings used by the website.</span></span>

```yaml
Type: HandlerMapping[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8e4b-126">-Hostnames</span><span class="sxs-lookup"><span data-stu-id="a8e4b-126">-HostNames</span></span>
<span data-ttu-id="a8e4b-127">Gibt die vollqualifizierten Hostnamen an, die für den Zugriff auf die Website verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="a8e4b-127">Specifies the fully qualified host names that can be used to access the website.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8e4b-128">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="a8e4b-128">-HttpLoggingEnabled</span></span>
<span data-ttu-id="a8e4b-129">Bestimmt, ob die HTTP-Protokollierung für die Website aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="a8e4b-129">Determines whether http logging is enabled for the website.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8e4b-130">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="a8e4b-130">-ManagedPipelineMode</span></span>
<span data-ttu-id="a8e4b-131">Gibt den verwalteten Pipelinemodus an.</span><span class="sxs-lookup"><span data-stu-id="a8e4b-131">Specifies the managed pipeline mode.</span></span>

```yaml
Type: ManagedPipelineMode
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8e4b-132">-Metadaten</span><span class="sxs-lookup"><span data-stu-id="a8e4b-132">-Metadata</span></span>
<span data-ttu-id="a8e4b-133">Gibt die Metadaten für die Website an.</span><span class="sxs-lookup"><span data-stu-id="a8e4b-133">Specifies the metadata for the website.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.WindowsAzure.Commands.Utilities.Websites.Services.WebEntities.NameValuePair]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8e4b-134">-Name</span><span class="sxs-lookup"><span data-stu-id="a8e4b-134">-Name</span></span>
<span data-ttu-id="a8e4b-135">Gibt den Namen der Website an.</span><span class="sxs-lookup"><span data-stu-id="a8e4b-135">Specifies the name of the website.</span></span>

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

### <span data-ttu-id="a8e4b-136">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="a8e4b-136">-NetFrameworkVersion</span></span>
<span data-ttu-id="a8e4b-137">Gibt die Version von .NET Framework an, die von der Website benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="a8e4b-137">Specifies the version of the .Net Framework required by the website.</span></span>

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

### <span data-ttu-id="a8e4b-138">-NumberOfWorkers</span><span class="sxs-lookup"><span data-stu-id="a8e4b-138">-NumberOfWorkers</span></span>
<span data-ttu-id="a8e4b-139">Gibt die Anzahl der Arbeitsprozesse an, die die Website ausführen.</span><span class="sxs-lookup"><span data-stu-id="a8e4b-139">Specifies the number of worker processes running the website.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8e4b-140">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a8e4b-140">-PassThru</span></span>
<span data-ttu-id="a8e4b-141">Gibt an, dass dieses Cmdlet einen **booleschen** Wert zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="a8e4b-141">Indicates that this cmdlet returns a **Boolean** value.</span></span>

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

### <span data-ttu-id="a8e4b-142">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="a8e4b-142">-PhpVersion</span></span>
<span data-ttu-id="a8e4b-143">Gibt die für die Website erforderliche PHP-Version an.</span><span class="sxs-lookup"><span data-stu-id="a8e4b-143">Specifies the PHP version required by the website.</span></span>

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

### <span data-ttu-id="a8e4b-144">-Profil</span><span class="sxs-lookup"><span data-stu-id="a8e4b-144">-Profile</span></span>
<span data-ttu-id="a8e4b-145">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="a8e4b-145">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="a8e4b-146">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="a8e4b-146">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a8e4b-147">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="a8e4b-147">-RequestTracingEnabled</span></span>
<span data-ttu-id="a8e4b-148">Bestimmt, ob die Anforderungs Ablaufverfolgung für die Website aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="a8e4b-148">Determines whether request tracing is enabled for the website.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8e4b-149">-RoutingRules</span><span class="sxs-lookup"><span data-stu-id="a8e4b-149">-RoutingRules</span></span>
<span data-ttu-id="a8e4b-150">Gibt die Routingregeln an, die für Tests in der Produktion verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="a8e4b-150">Specifies the routing rules to use for testing in production.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.WindowsAzure.Commands.Utilities.Websites.Services.WebEntities.RoutingRule]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8e4b-151">-SiteWithConfig</span><span class="sxs-lookup"><span data-stu-id="a8e4b-151">-SiteWithConfig</span></span>
<span data-ttu-id="a8e4b-152">Gibt die von der Website verwendete Konfiguration an.</span><span class="sxs-lookup"><span data-stu-id="a8e4b-152">Specifies the configuration used by the website.</span></span>

```yaml
Type: SiteWithConfig
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8e4b-153">-Slot</span><span class="sxs-lookup"><span data-stu-id="a8e4b-153">-Slot</span></span>
<span data-ttu-id="a8e4b-154">Gibt den Steckplatznamen der Website an.</span><span class="sxs-lookup"><span data-stu-id="a8e4b-154">Specifies the slot name of the website.</span></span>

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

### <span data-ttu-id="a8e4b-155">-SlotStickyAppSettingNames</span><span class="sxs-lookup"><span data-stu-id="a8e4b-155">-SlotStickyAppSettingNames</span></span>
```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8e4b-156">-SlotStickyConnectionStringNames</span><span class="sxs-lookup"><span data-stu-id="a8e4b-156">-SlotStickyConnectionStringNames</span></span>
```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8e4b-157">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="a8e4b-157">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="a8e4b-158">Gibt an, ob der 32-Bit-Modus aktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="a8e4b-158">Specifies whether to enable 32-bit mode.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8e4b-159">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="a8e4b-159">-WebSocketsEnabled</span></span>
<span data-ttu-id="a8e4b-160">Gibt an, ob websockets aktiviert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="a8e4b-160">Specifies whether to enable WebSockets.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8e4b-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8e4b-161">CommonParameters</span></span>
<span data-ttu-id="a8e4b-162">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a8e4b-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8e4b-163">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a8e4b-163">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8e4b-164">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a8e4b-164">INPUTS</span></span>

## <span data-ttu-id="a8e4b-165">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a8e4b-165">OUTPUTS</span></span>

## <span data-ttu-id="a8e4b-166">Notizen</span><span class="sxs-lookup"><span data-stu-id="a8e4b-166">NOTES</span></span>

## <span data-ttu-id="a8e4b-167">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a8e4b-167">RELATED LINKS</span></span>

[<span data-ttu-id="a8e4b-168">Get-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="a8e4b-168">Get-AzureWebsite</span></span>](./Get-AzureWebsite.md)

[<span data-ttu-id="a8e4b-169">Neu – AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="a8e4b-169">New-AzureWebsite</span></span>](./New-AzureWebsite.md)

[<span data-ttu-id="a8e4b-170">Remove-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="a8e4b-170">Remove-AzureWebsite</span></span>](./Remove-AzureWebsite.md)


