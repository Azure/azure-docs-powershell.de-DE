---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 4166119F-D26A-45A1-B040-D7B2459833D6
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/set-Azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Set-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Set-AzWebApp.md
ms.openlocfilehash: 4478083a2ee98eceda08012b4346f3ece1657963
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842679"
---
# <span data-ttu-id="ba863-101">Set-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="ba863-101">Set-AzWebApp</span></span>

## <span data-ttu-id="ba863-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ba863-102">SYNOPSIS</span></span>
<span data-ttu-id="ba863-103">Ändert eine Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="ba863-103">Modifies an Azure Web App.</span></span>

## <span data-ttu-id="ba863-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ba863-104">SYNTAX</span></span>

### <span data-ttu-id="ba863-105">S1</span><span class="sxs-lookup"><span data-stu-id="ba863-105">S1</span></span>
```
Set-AzWebApp [[-AppServicePlan] <String>] [[-DefaultDocuments] <String[]>]
 [[-NetFrameworkVersion] <String>] [[-PhpVersion] <String>] [[-RequestTracingEnabled] <Boolean>]
 [[-HttpLoggingEnabled] <Boolean>] [[-DetailedErrorLoggingEnabled] <Boolean>] [[-AppSettings] <Hashtable>]
 [[-ConnectionStrings] <Hashtable>]
 [[-HandlerMappings] <System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]>]
 [[-ManagedPipelineMode] <String>] [[-WebSocketsEnabled] <Boolean>] [[-Use32BitWorkerProcess] <Boolean>]
 [[-AutoSwapSlotName] <String>] [-HostNames <String[]>] [-NumberOfWorkers <Int32>] [-AsJob] [[-AssignIdentity] <Boolean>]
 [[-HttpsOnly] <Boolean>] [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ba863-106">S2</span><span class="sxs-lookup"><span data-stu-id="ba863-106">S2</span></span>
```
Set-AzWebApp [[-Use32BitWorkerProcess] <Boolean>] [[-AutoSwapSlotName] <String>]
 [-NumberOfWorkers <Int32>] [-AsJob] [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ba863-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ba863-107">DESCRIPTION</span></span>
<span data-ttu-id="ba863-108">Das Cmdlet " **Set-AzWebApp** " legt eine Azure Web App fest.</span><span class="sxs-lookup"><span data-stu-id="ba863-108">The **Set-AzWebApp** cmdlet sets an Azure Web App.</span></span>

## <span data-ttu-id="ba863-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ba863-109">EXAMPLES</span></span>

### <span data-ttu-id="ba863-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ba863-110">Example 1</span></span>
```
PS C:\> Set-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -HttpLoggingEnabled $true
```

<span data-ttu-id="ba863-111">Mit diesem Befehl wird HttpLoggingEnabled für Web-App-ContosoWebApp festgelegt, die mit der Ressourcengruppe Standard verknüpft sind – Web-westus</span><span class="sxs-lookup"><span data-stu-id="ba863-111">This command sets HttpLoggingEnabled to true for Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="ba863-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="ba863-112">PARAMETERS</span></span>

### <span data-ttu-id="ba863-113">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="ba863-113">-AppServicePlan</span></span>
<span data-ttu-id="ba863-114">Name des App-Service Plans</span><span class="sxs-lookup"><span data-stu-id="ba863-114">App Service Plan Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba863-115">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="ba863-115">-AppSettings</span></span>
<span data-ttu-id="ba863-116">Hashtable für App-Einstellungen</span><span class="sxs-lookup"><span data-stu-id="ba863-116">App Settings HashTable</span></span>

```yaml
Type: Hashtable
Parameter Sets: S1
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba863-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ba863-117">-AsJob</span></span>
<span data-ttu-id="ba863-118">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="ba863-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ba863-119">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="ba863-119">-AssignIdentity</span></span>
<span data-ttu-id="ba863-120">Aktivieren/Deaktivieren von MSI für eine vorhandene Azure-webfunctionapp [Preview]</span><span class="sxs-lookup"><span data-stu-id="ba863-120">Enable/disable MSI on an existing azure webapp or functionapp [PREVIEW]</span></span>

```yaml
Type: Boolean
Parameter Sets: S1
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba863-121">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="ba863-121">-AutoSwapSlotName</span></span>
<span data-ttu-id="ba863-122">Name des Ziel Steckplatzes für den automatischen Austausch</span><span class="sxs-lookup"><span data-stu-id="ba863-122">Destination slot name for auto swap</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 15
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba863-123">-ConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="ba863-123">-ConnectionStrings</span></span>
<span data-ttu-id="ba863-124">Hashtable für Verbindungszeichenfolgen</span><span class="sxs-lookup"><span data-stu-id="ba863-124">Connection Strings HashTable</span></span>

```yaml
Type: Hashtable
Parameter Sets: S1
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba863-125">-DefaultDocuments</span><span class="sxs-lookup"><span data-stu-id="ba863-125">-DefaultDocuments</span></span>
<span data-ttu-id="ba863-126">Standard-Zeichenfolgen Array für Dokumente</span><span class="sxs-lookup"><span data-stu-id="ba863-126">Default Documents String Array</span></span>

```yaml
Type: String[]
Parameter Sets: S1
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba863-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba863-127">-DefaultProfile</span></span>
<span data-ttu-id="ba863-128">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ba863-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba863-129">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="ba863-129">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="ba863-130">Detaillierte Fehlerprotokollierung aktiviert boolescher Wert</span><span class="sxs-lookup"><span data-stu-id="ba863-130">Detailed Error Logging Enabled Boolean</span></span>

```yaml
Type: Boolean
Parameter Sets: S1
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba863-131">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="ba863-131">-HandlerMappings</span></span>
<span data-ttu-id="ba863-132">Handler-Zuordnungen, IList</span><span class="sxs-lookup"><span data-stu-id="ba863-132">Handler Mappings IList</span></span>

```yaml
Type: System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]
Parameter Sets: S1
Aliases: 

Required: False
Position: 11
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba863-133">-Hostnames</span><span class="sxs-lookup"><span data-stu-id="ba863-133">-HostNames</span></span>
<span data-ttu-id="ba863-134">Host-hostnames-Zeichenfolge Array</span><span class="sxs-lookup"><span data-stu-id="ba863-134">WebApp HostNames String Array</span></span>

```yaml
Type: String[]
Parameter Sets: S1
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba863-135">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="ba863-135">-HttpLoggingEnabled</span></span>
<span data-ttu-id="ba863-136">HttpLoggingEnabled-boolescher Wert</span><span class="sxs-lookup"><span data-stu-id="ba863-136">HttpLoggingEnabled Boolean</span></span>

```yaml
Type: Boolean
Parameter Sets: S1
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba863-137">-HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="ba863-137">-HttpsOnly</span></span>
<span data-ttu-id="ba863-138">Aktivieren/Deaktivieren der Umleitung des gesamten Datenverkehrs an HTTPS auf einer vorhandenen Azure-webfunctionapp</span><span class="sxs-lookup"><span data-stu-id="ba863-138">Enable/disable redirecting all traffic to HTTPS on an existing azure webapp or functionapp</span></span>

```yaml
Type: Boolean
Parameter Sets: S1
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba863-139">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="ba863-139">-ManagedPipelineMode</span></span>
<span data-ttu-id="ba863-140">Name des verwalteten Pipeline Modus</span><span class="sxs-lookup"><span data-stu-id="ba863-140">Managed Pipeline Mode Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 
Accepted values: Classic, Integrated

Required: False
Position: 12
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba863-141">-Name</span><span class="sxs-lookup"><span data-stu-id="ba863-141">-Name</span></span>
<span data-ttu-id="ba863-142">Name des Webhosts</span><span class="sxs-lookup"><span data-stu-id="ba863-142">WebApp Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba863-143">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="ba863-143">-NetFrameworkVersion</span></span>
<span data-ttu-id="ba863-144">NET Framework-Version</span><span class="sxs-lookup"><span data-stu-id="ba863-144">Net Framework Version</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba863-145">-NumberOfWorkers</span><span class="sxs-lookup"><span data-stu-id="ba863-145">-NumberOfWorkers</span></span>
<span data-ttu-id="ba863-146">Die Anzahl der Arbeitskräfte, die zugewiesen werden sollen</span><span class="sxs-lookup"><span data-stu-id="ba863-146">The number of workers to be allocated</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ba863-147">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="ba863-147">-PhpVersion</span></span>
<span data-ttu-id="ba863-148">PHP-Version</span><span class="sxs-lookup"><span data-stu-id="ba863-148">Php Version</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba863-149">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="ba863-149">-RequestTracingEnabled</span></span>
<span data-ttu-id="ba863-150">Anforderungs Ablaufverfolgung aktiviert</span><span class="sxs-lookup"><span data-stu-id="ba863-150">Request Tracing Enabled</span></span>

```yaml
Type: Boolean
Parameter Sets: S1
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba863-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba863-151">-ResourceGroupName</span></span>
<span data-ttu-id="ba863-152">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="ba863-152">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba863-153">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="ba863-153">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="ba863-154">Verwenden des 32-Bit-Workerprozess-booleschen Werts</span><span class="sxs-lookup"><span data-stu-id="ba863-154">Use 32-bit Worker Process Boolean</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 14
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba863-155">-Webbasierte</span><span class="sxs-lookup"><span data-stu-id="ba863-155">-WebApp</span></span>
<span data-ttu-id="ba863-156">Webobjekt</span><span class="sxs-lookup"><span data-stu-id="ba863-156">WebApp Object</span></span>

```yaml
Type: Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ba863-157">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="ba863-157">-WebSocketsEnabled</span></span>
<span data-ttu-id="ba863-158">WebSocketsEnabled-boolescher Wert</span><span class="sxs-lookup"><span data-stu-id="ba863-158">WebSocketsEnabled Boolean</span></span>

```yaml
Type: Boolean
Parameter Sets: S1
Aliases: 

Required: False
Position: 13
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba863-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba863-159">CommonParameters</span></span>
<span data-ttu-id="ba863-160">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ba863-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba863-161">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ba863-161">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba863-162">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ba863-162">INPUTS</span></span>

### <span data-ttu-id="ba863-163">Int32</span><span class="sxs-lookup"><span data-stu-id="ba863-163">Int32</span></span>
<span data-ttu-id="ba863-164">Der Parameter ' NumberOfWorkers ' akzeptiert den Wert vom Typ ' Int32 ' aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="ba863-164">Parameter 'NumberOfWorkers' accepts value of type 'Int32' from the pipeline</span></span>

### <span data-ttu-id="ba863-165">Website</span><span class="sxs-lookup"><span data-stu-id="ba863-165">Site</span></span>
<span data-ttu-id="ba863-166">Der Parameter "WebStart" akzeptiert den Wert vom Typ "Website" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="ba863-166">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="ba863-167">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ba863-167">OUTPUTS</span></span>

## <span data-ttu-id="ba863-168">Notizen</span><span class="sxs-lookup"><span data-stu-id="ba863-168">NOTES</span></span>

## <span data-ttu-id="ba863-169">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ba863-169">RELATED LINKS</span></span>

[<span data-ttu-id="ba863-170">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="ba863-170">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="ba863-171">Neu – AzWebApp</span><span class="sxs-lookup"><span data-stu-id="ba863-171">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="ba863-172">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="ba863-172">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="ba863-173">Neustart-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="ba863-173">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="ba863-174">Anfang-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="ba863-174">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="ba863-175">Stopp-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="ba863-175">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)
