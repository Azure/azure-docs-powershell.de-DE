---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: FA868206-D8B0-4868-A1D1-D3F96BF3ADCC
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/set-Azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Set-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Set-AzWebAppSlot.md
ms.openlocfilehash: b6cb41e49695fa7fd9fa0efdefdbefb2b23229a5
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842676"
---
# <span data-ttu-id="39bde-101">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="39bde-101">Set-AzWebAppSlot</span></span>

## <span data-ttu-id="39bde-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="39bde-102">SYNOPSIS</span></span>
<span data-ttu-id="39bde-103">Ändert einen Azure Web App-Steckplatz.</span><span class="sxs-lookup"><span data-stu-id="39bde-103">Modifies an Azure Web App slot.</span></span>

## <span data-ttu-id="39bde-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="39bde-104">SYNTAX</span></span>

### <span data-ttu-id="39bde-105">S1</span><span class="sxs-lookup"><span data-stu-id="39bde-105">S1</span></span>
```
Set-AzWebAppSlot [[-AppServicePlan] <String>] [[-DefaultDocuments] <String[]>]
 [[-NetFrameworkVersion] <String>] [[-PhpVersion] <String>] [[-RequestTracingEnabled] <Boolean>]
 [[-HttpLoggingEnabled] <Boolean>] [[-DetailedErrorLoggingEnabled] <Boolean>] [[-AppSettings] <Hashtable>]
 [[-ConnectionStrings] <Hashtable>]
 [[-HandlerMappings] <System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]>]
 [[-ManagedPipelineMode] <String>] [[-WebSocketsEnabled] <Boolean>] [[-Use32BitWorkerProcess] <Boolean>]
 [-AutoSwapSlotName <String>] [-NumberOfWorkers <Int32>] [-ResourceGroupName] <String> [-Name] <String>
 [[-AssignIdentity] <Boolean>] [[HttpsOnly] <Boolean>] [-Slot] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="39bde-106">S2</span><span class="sxs-lookup"><span data-stu-id="39bde-106">S2</span></span>
```
Set-AzWebAppSlot [[-AppServicePlan] <String>] [[-DefaultDocuments] <String[]>]
 [[-NetFrameworkVersion] <String>] [[-PhpVersion] <String>] [[-RequestTracingEnabled] <Boolean>]
 [[-HttpLoggingEnabled] <Boolean>] [[-DetailedErrorLoggingEnabled] <Boolean>] [[-AppSettings] <Hashtable>]
 [[-ConnectionStrings] <Hashtable>]
 [[-HandlerMappings] <System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]>]
 [[-ManagedPipelineMode] <String>] [[-WebSocketsEnabled] <Boolean>] [[-Use32BitWorkerProcess] <Boolean>]
 [-AutoSwapSlotName <String>] [-NumberOfWorkers <Int32>] [-WebApp] <Site> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="39bde-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="39bde-107">DESCRIPTION</span></span>
<span data-ttu-id="39bde-108">Das Cmdlet " **Set-AzWebApp** " legt einen Azure Web App-Steckplatz fest.</span><span class="sxs-lookup"><span data-stu-id="39bde-108">The **Set-AzWebApp** cmdlet sets an Azure Web App Slot.</span></span>

## <span data-ttu-id="39bde-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="39bde-109">EXAMPLES</span></span>

### <span data-ttu-id="39bde-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="39bde-110">Example 1</span></span>
```
PS C:\> Set-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001" -HttpLoggingEnabled $true
```

<span data-ttu-id="39bde-111">Mit diesem Befehl wird HttpLoggingEnabled auf "true" festgelegt, wenn der Slot Slot001 in Bezug auf Web-App-ContosoWebApp, die mit der Ressourcengruppe Standard verknüpft sind-Web-westus</span><span class="sxs-lookup"><span data-stu-id="39bde-111">This command sets HttpLoggingEnabled to true for Slot Slot001 pertaining to Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="39bde-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="39bde-112">PARAMETERS</span></span>

### <span data-ttu-id="39bde-113">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="39bde-113">-AppServicePlan</span></span>
<span data-ttu-id="39bde-114">Name des App-Service Plans</span><span class="sxs-lookup"><span data-stu-id="39bde-114">App Service Plan Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39bde-115">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="39bde-115">-AppSettings</span></span>
<span data-ttu-id="39bde-116">Hashtable für App-Einstellungen</span><span class="sxs-lookup"><span data-stu-id="39bde-116">App Settings HashTable</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39bde-117">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="39bde-117">-AutoSwapSlotName</span></span>
<span data-ttu-id="39bde-118">Name des Ziel Steckplatzes für den automatischen Austausch</span><span class="sxs-lookup"><span data-stu-id="39bde-118">Destination slot name for auto swap</span></span>

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

### <span data-ttu-id="39bde-119">-ConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="39bde-119">-ConnectionStrings</span></span>
<span data-ttu-id="39bde-120">Hashtable für Verbindungszeichenfolgen</span><span class="sxs-lookup"><span data-stu-id="39bde-120">Connection Strings HashTable</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 11
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39bde-121">-DefaultDocuments</span><span class="sxs-lookup"><span data-stu-id="39bde-121">-DefaultDocuments</span></span>
<span data-ttu-id="39bde-122">Standard-Zeichenfolgen Array für Dokumente</span><span class="sxs-lookup"><span data-stu-id="39bde-122">Default Documents String Array</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39bde-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39bde-123">-DefaultProfile</span></span>
<span data-ttu-id="39bde-124">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="39bde-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="39bde-125">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="39bde-125">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="39bde-126">Detaillierte Fehlerprotokollierung aktiviert boolescher Wert</span><span class="sxs-lookup"><span data-stu-id="39bde-126">Detailed Error Logging Enabled Boolean</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39bde-127">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="39bde-127">-HandlerMappings</span></span>
<span data-ttu-id="39bde-128">Handler-Zuordnungen, IList</span><span class="sxs-lookup"><span data-stu-id="39bde-128">Handler Mappings IList</span></span>

```yaml
Type: System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 12
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39bde-129">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="39bde-129">-HttpLoggingEnabled</span></span>
<span data-ttu-id="39bde-130">HttpLoggingEnabled-boolescher Wert</span><span class="sxs-lookup"><span data-stu-id="39bde-130">HttpLoggingEnabled Boolean</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39bde-131">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="39bde-131">-ManagedPipelineMode</span></span>
<span data-ttu-id="39bde-132">Name des verwalteten Pipeline Modus</span><span class="sxs-lookup"><span data-stu-id="39bde-132">Managed Pipeline Mode Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Classic, Integrated

Required: False
Position: 13
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39bde-133">-Name</span><span class="sxs-lookup"><span data-stu-id="39bde-133">-Name</span></span>
<span data-ttu-id="39bde-134">Name des Webhosts</span><span class="sxs-lookup"><span data-stu-id="39bde-134">WebApp Name</span></span>

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

### <span data-ttu-id="39bde-135">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="39bde-135">-NetFrameworkVersion</span></span>
<span data-ttu-id="39bde-136">NET Framework-Version</span><span class="sxs-lookup"><span data-stu-id="39bde-136">Net Framework Version</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39bde-137">-NumberOfWorkers</span><span class="sxs-lookup"><span data-stu-id="39bde-137">-NumberOfWorkers</span></span>
<span data-ttu-id="39bde-138">Die Anzahl der Arbeitskräfte, die zugewiesen werden sollen</span><span class="sxs-lookup"><span data-stu-id="39bde-138">The number of workers to be allocated</span></span>

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

### <span data-ttu-id="39bde-139">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="39bde-139">-PhpVersion</span></span>
<span data-ttu-id="39bde-140">PHP-Version</span><span class="sxs-lookup"><span data-stu-id="39bde-140">Php Version</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39bde-141">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="39bde-141">-RequestTracingEnabled</span></span>
<span data-ttu-id="39bde-142">Anforderungs Ablaufverfolgung aktiviert boolescher Wert</span><span class="sxs-lookup"><span data-stu-id="39bde-142">Request Tracing Enabled Boolean</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39bde-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="39bde-143">-ResourceGroupName</span></span>
<span data-ttu-id="39bde-144">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="39bde-144">Resource Group Name</span></span>

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

### <span data-ttu-id="39bde-145">-Slot</span><span class="sxs-lookup"><span data-stu-id="39bde-145">-Slot</span></span>
<span data-ttu-id="39bde-146">Name des webslots</span><span class="sxs-lookup"><span data-stu-id="39bde-146">WebApp Slot Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39bde-147">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="39bde-147">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="39bde-148">Verwenden des 32-Bit-Workerprozess-booleschen Werts</span><span class="sxs-lookup"><span data-stu-id="39bde-148">Use 32-bit Worker Process Boolean</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 15
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39bde-149">-Webbasierte</span><span class="sxs-lookup"><span data-stu-id="39bde-149">-WebApp</span></span>
<span data-ttu-id="39bde-150">Webobjekt</span><span class="sxs-lookup"><span data-stu-id="39bde-150">WebApp Object</span></span>

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

### <span data-ttu-id="39bde-151">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="39bde-151">-WebSocketsEnabled</span></span>
<span data-ttu-id="39bde-152">Web Sockets enabled Boolescher Wert</span><span class="sxs-lookup"><span data-stu-id="39bde-152">Web Sockets Enabled Boolean</span></span>

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
### <span data-ttu-id="39bde-153">-HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="39bde-153">-HttpsOnly</span></span>
<span data-ttu-id="39bde-154">Aktivieren/Deaktivieren der Umleitung des gesamten Datenverkehrs an HTTPS auf einem vorhandenen Steckplatz</span><span class="sxs-lookup"><span data-stu-id="39bde-154">Enable/disable redirecting all traffic to HTTPS on an existing slot</span></span>

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
### <span data-ttu-id="39bde-155">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="39bde-155">-AssignIdentity</span></span>
<span data-ttu-id="39bde-156">Aktivieren/Deaktivieren von MSI für einen vorhandenen Steckplatz [Preview]</span><span class="sxs-lookup"><span data-stu-id="39bde-156">Enable/disable MSI on an existing slot [PREVIEW]</span></span>

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

### <span data-ttu-id="39bde-157">-AsJob</span><span class="sxs-lookup"><span data-stu-id="39bde-157">-AsJob</span></span>
<span data-ttu-id="39bde-158">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="39bde-158">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="39bde-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39bde-159">CommonParameters</span></span>
<span data-ttu-id="39bde-160">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="39bde-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39bde-161">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="39bde-161">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39bde-162">Eingaben</span><span class="sxs-lookup"><span data-stu-id="39bde-162">INPUTS</span></span>

### <span data-ttu-id="39bde-163">Int32</span><span class="sxs-lookup"><span data-stu-id="39bde-163">Int32</span></span>
<span data-ttu-id="39bde-164">Der Parameter ' NumberOfWorkers ' akzeptiert den Wert vom Typ ' Int32 ' aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="39bde-164">Parameter 'NumberOfWorkers' accepts value of type 'Int32' from the pipeline</span></span>

### <span data-ttu-id="39bde-165">Website</span><span class="sxs-lookup"><span data-stu-id="39bde-165">Site</span></span>
<span data-ttu-id="39bde-166">Der Parameter "WebStart" akzeptiert den Wert vom Typ "Website" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="39bde-166">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="39bde-167">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="39bde-167">OUTPUTS</span></span>

## <span data-ttu-id="39bde-168">Notizen</span><span class="sxs-lookup"><span data-stu-id="39bde-168">NOTES</span></span>

## <span data-ttu-id="39bde-169">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="39bde-169">RELATED LINKS</span></span>

[<span data-ttu-id="39bde-170">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="39bde-170">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="39bde-171">Neu – AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="39bde-171">New-AzWebAppSlot</span></span>](./New-AzWebAppSlot.md)

[<span data-ttu-id="39bde-172">Remove-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="39bde-172">Remove-AzWebAppSlot</span></span>](./Remove-AzWebAppSlot.md)

[<span data-ttu-id="39bde-173">Neustart-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="39bde-173">Restart-AzWebAppSlot</span></span>](./Restart-AzWebAppSlot.md)

[<span data-ttu-id="39bde-174">Anfang-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="39bde-174">Start-AzWebAppSlot</span></span>](./Start-AzWebAppSlot.md)

[<span data-ttu-id="39bde-175">Stopp-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="39bde-175">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="39bde-176">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="39bde-176">Get-AzAppServicePlan</span></span>](./Get-AzAppServicePlan.md)
